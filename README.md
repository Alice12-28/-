# 🧬 生物药研究进展 · 一键抓取助手

**Biopharma Research Tracker** —— 浏览器端单文件应用，一键检索全球生物药领域最新进展，**自动精读重点文献并生成中文摘要**，图文并茂日报一键导出 PDF。

---

## ✨ 核心功能

| 功能 | 说明 |
|------|------|
| 🚀 一键全网检索 | 浏览器端直连 PubMed / bioRxiv / ClinicalTrials.gov / WHO / ScienceDaily / Phys.org 六大公开数据源，无需服务器 |
| 🗂️ 六大分类浏览 | 学术文献、预印本、综述评论、临床试验、监管动态、产业新闻，自动分类与可视化统计 |
| 📊 **重点文献中文精读** | 智能筛选 Top 5 重点文献（顶刊 / 监管获批 / Ⅲ期临床优先），自动生成：<br/>• 中文要点标题<br/>• 研究类型标签（Ⅰ/Ⅱ/Ⅲ期临床、监管获批、综述、临床前…）<br/>• 疾病领域识别（肿瘤、自免、罕见病、基因治疗…）<br/>• **核心发现**（中文解读，关键术语自动高亮）<br/>• **行业意义点评**（顶刊/获批/关键临床会自动增强点评语）<br/>• ⭐ 推荐度星级（1–5★） |
| 📄 图文报告 + PDF 导出 | 封面 → KPI 摘要 → 分类分布条形图 → **重点精读** → 分类详情 → 数据方法，A4 排版一键导出 PDF |
| 💾 多格式导出 | 支持 PDF / JSON / Markdown 三种导出格式 |
| 🔒 隐私安全 | 所有 API 调用均在浏览器端直接完成，数据不经任何中间服务器 |

### 中文智能摘要引擎

内置基于 **关键词识别 + 分类模板 + 期刊权重** 的中文摘要引擎，覆盖：

- **术语词典**：单克隆抗体、ADC、双特异性抗体、CAR-T/CAR-NK、基因治疗/CRISPR、mRNA、免疫检查点抑制剂（PD-1/PD-L1/CTLA-4）、AAV 载体、溶瘤病毒、生物类似药等 25+ 专业术语，自动在摘要中高亮
- **研究类型识别**：Ⅰ/Ⅱ/Ⅲ期临床、FDA/NMPA 获批、临床前、综述/述评、荟萃分析、真实世界研究、生物标志物、病例报告等 10 类
- **疾病领域识别**：肿瘤学、自身免疫、罕见病、传染病疫苗、基因治疗、心血管、神经疾病、代谢疾病、生物药工艺、监管政策等 10 大方向
- **智能选篇**：按"顶刊(+100) > FDA获批(+80) > Ⅲ期临床(+60) > Ⅱ期(+40) > 新机制(+20) > 有摘要(+10)"打分排序，自动挑出最值得精读的 5 篇

---

## 🚀 部署到 GitHub Pages（推荐，5 分钟完成）

### 方法 1：GitHub 网页上传（最简单）

1. **下载并解压** `biopharma-tracker.zip`，得到 `index.html`、`README.md`、`.nojekyll` 三个文件
2. 登录 GitHub，点击右上角 **「+」→「New repository」**
   - Repository name 填写 `biopharma-tracker`（或任意名称）
   - 选择 **Public**
   - 点击 **Create repository**
3. 在仓库页面点击 **「uploading an existing file」**，将解压出的 3 个文件拖拽上传
4. 填写 Commit message 如 `init: deploy biopharma tracker`，点击 **Commit changes**
5. 进入仓库 **Settings → Pages**（左侧边栏）
   - **Source** 选择 `Deploy from a branch`
   - **Branch** 选择 `main`，文件夹选 `/ (root)`，点击 **Save**
6. 等待约 1 分钟，页面顶部会出现绿色提示 `Your site is live at https://<你的用户名>.github.io/biopharma-tracker/`
7. 点击该链接即可访问 🎉

### 方法 2：Git 命令行

```bash
# 1. 解压 zip
unzip biopharma-tracker.zip -d biopharma-tracker && cd biopharma-tracker

# 2. 新建仓库并推送
git init
git add .
git commit -m "init: deploy biopharma tracker with Chinese deep-read summaries"
git branch -M main
git remote add origin https://github.com/<你的用户名>/biopharma-tracker.git
git push -u origin main

# 3. 在 GitHub 仓库 Settings → Pages 启用 main 分支部署即可
```

---

## 🌐 其他部署方式

### Vercel（最快，无需 GitHub）
1. 访问 [vercel.com](https://vercel.com) 用 GitHub 账号登录
2. 点击 **Add New → Project → Upload**，直接拖入解压后的文件夹
3. 无需任何配置，几秒后即可获得 `https://xxx.vercel.app` 访问地址

### Netlify
1. 访问 [app.netlify.com/drop](https://app.netlify.com/drop)
2. 将解压后的文件夹直接拖入页面虚线框，即刻获得访问链接

### Cloudflare Pages
1. 登录 Cloudflare Dashboard → **Pages** → **Create a project** → **Direct Upload**
2. 上传文件夹 → 命名项目 → 部署完成即获 `https://xxx.pages.dev` 链接

### 本地预览（无需部署）
直接双击 `index.html` 用浏览器打开即可使用全部功能（推荐 Chrome/Edge/Safari 最新版）。

---

## 📖 使用流程

1. 打开页面，点击 **「🚀 立即开始全网检索」** 抓取真实最新数据
   - 也可先点 **「📖 查看示例」** 预览报告效果（页面打开即自动加载示例数据）
2. 等待 30–60 秒，六大数据源依次抓取，实时日志显示进度
3. 抓取完成后浏览分类卡片，也可点击分类标签筛选
4. 点击 **「📊 生成每日报告」** 打开报告预览模态框
   - 查看执行摘要、分类分布图
   - 阅读 **「重点文献精读」**：5 篇最具价值文献的中文解读，含核心发现与行业意义
   - 查看全部条目的分类详情
5. 点击 **「导出 PDF」** 将报告保存为 A4 格式 PDF 归档
   - 也可点击 **「🖨️ 打印」** 使用浏览器原生打印/另存为 PDF
6. 可选：点击 **「💾 导出 JSON」** 或 **「📝 导出 Markdown」** 导出原始数据用于二次分析

---

## 🛠️ 技术栈

- **纯前端单文件**：`index.html` 一个文件包含全部 HTML/CSS/JS，无构建步骤
- **Tailwind CSS CDN** + 自定义 CSS 变量，品牌色为青 (#0e7490) → 紫 (#7c3aed) → 橙 (#ea580c) 渐变
- **公开学术 API**：
  - PubMed E-utilities（NCBI）
  - bioRxiv API（Cold Spring Harbor Laboratory）
  - ClinicalTrials.gov v2 API
  - WHO News API
  - ScienceDaily / Phys.org RSS
- **html2pdf.js**（CDN）：浏览器端直接生成 PDF
- **CORS 代理池**：内置 allorigins / corsproxy.io / codetabs 三个公共代理自动容错
- **中文摘要引擎**：纯前端 JS 规则引擎，零依赖、零调用成本、隐私安全

---

## ⚠️ 注意事项

- 部分数据源需通过公共 CORS 代理访问，个别代理偶发不稳定时可点击"重新抓取"重试
- 中文摘要为**前端规则引擎自动生成**，目的是快速筛选线索，不能替代对原文的阅读；关键结论请以原文为准
- PDF 导出依赖 CDN 加载的 html2pdf.js，首次使用请保持网络通畅
- 覆盖数据源为公开学术与新闻 API，检索范围为近 3 天内更新的内容
- 本工具仅供科研信息参考，不构成任何医疗、投资或法律建议

---

## 📁 文件说明

```
biopharma-tracker/
├── index.html    # 主应用（单文件，含全部功能与中文精读引擎）
├── README.md     # 本说明文档
└── .nojekyll     # 告诉 GitHub Pages 不要用 Jekyll 处理，确保静态资源正常
```

---

© BioPharma Research Tracker · Powered by open academic APIs

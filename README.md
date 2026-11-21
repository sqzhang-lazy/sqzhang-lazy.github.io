# Shaoqing Zhang · Academic homepage

面向 GitHub Pages 的学术个人主页。无需安装 Node.js、依赖或构建工具。

## 预览

解压后双击 `index.html` 即可浏览。主要内容、样式和论文原图均包含在该文件中；预览不依赖外部字体或图片。论文、Scholar 和 GitHub 等外部链接需要联网。浏览器禁止本地文件访问剪贴板时，BibTeX 会被选中，可用 Ctrl/Cmd+C 复制。

## 发布到 GitHub Pages

1. 登录自己的 GitHub 账户。
2. 新建公开仓库 **sqzhang-lazy.github.io**。如果该仓库已存在，先备份并查看现有内容，再更新文件。
3. 把本目录中的 `index.html`、`.nojekyll` 和 `README.md` 上传到仓库根目录并提交。不要把整个文件夹作为一层子目录上传。`index.html` 必须位于所选发布目录的根部。
4. 在仓库 **Settings → Pages → Build and deployment** 中，将 Source 设为 **Deploy from a branch**。
5. 选择实际使用的分支（通常是 `main`）以及 **/(root)**，点击 Save。
6. 等待 GitHub 显示部署成功，然后访问 `https://sqzhang-lazy.github.io/`。这是配置后的目标地址；本压缩包本身不表示网站已经上线。

官方说明：https://docs.github.com/en/pages/quickstart

## 如何维护

- 姓名、院校、邮箱、社交链接、英文简介及论文：编辑 `index.html` 的 HTML 正文。
- 对应中文文案：编辑文件末尾的 `const zh` 对象及 `Object.assign(zh, ...)` 中对应键值。
- 引用：编辑文件末尾的 `const citations` 对象。
- 新增论文：复制一个 `article.pub`，填写年份、标题、作者、会议信息和链接；如需摘要，添加对应的双语文案键。代表作采用可滑动轮播，添加作品时需要同步更新卡片、圆点按钮和 `names` 数组。
- 添加照片：将照片放入本目录（例如 `portrait.jpg`），把 `.avatar` 图片的 `src` 改为 `portrait.jpg`。当前头像是从本人 GitHub 账户取得并嵌入页面的公开头像，后续可替换为照片。
- 加入简历：先放入真实的 `cv.pdf`，再添加链接。没有文件时不显示入口。
- 网站没有流量统计、第三方脚本或数据收集表单。语言偏好保存在访客浏览器本地。
- 手机和桌面使用同一页面，自适应布局；可直接用浏览器打印为 PDF。

## 内容依据及待补充资料

已确认：中文名张少卿、英文名 Shaoqing Zhang、哈尔滨工业大学计算机科学与技术学院博士生、Google Scholar 页面。自我介绍采用用户提供的两段中文，并同步提供英文翻译。哈尔滨工业大学、深圳、联系邮箱及D-PoT 与 GuidelineLLM 取自上传 README；GUITAR 由用户补充并通过 arXiv 页面和作者代码仓库核对。尚未提供导师、个人照片、简历和更新后的全部成果，因此未添加这些内容。请在公开发布前核对当前单位、城市和邮箱。

三篇论文的作者与发表信息按下列官方来源核对。原 README 的 D-PoT 链接 `2501.01149` 实际指向 A3，已经改为对应 ACL 官方页面。

- D-PoT：https://aclanthology.org/2024.findings-emnlp.70/
- GuidelineLLM：https://arxiv.org/abs/2412.10423
- GuidelineLLM 会议记录：https://ojs.aaai.org/index.php/AAAI/article/view/34784
- GUITAR：https://arxiv.org/abs/2609.34113
- GUITAR 作者代码仓库：https://github.com/sqzhang-lazy/GUITAR

GuidelineLLM 的 arXiv/PDF 标题使用 “Enhancing”，AAAI 元数据使用 “Enhance”。页面标题沿用论文 PDF，BibTeX 使用 AAAI 会议记录。

Highlight Work 的三幅图直接从论文 PDF 高清提取，保留原图内容与比例：GUITAR 第 2 页 Figure 1、D-PoT 第 4 页 Figure 3、GuidelineLLM 第 1 页 Figure 1。图片嵌入 HTML，可离线显示；点击图片或图注可打开对应论文页。研究进展使用论文集出版年月，不推断录用通知日期。本站展示 D-PoT、GuidelineLLM 及用户补充的 GUITAR。GUITAR 标注为 NeurIPS 2026 Evaluations & Datasets Track；录用 News 仅使用已确认的年份，不推断具体录用月份。GUITAR 引用暂使用 arXiv 条目，未编造会议卷号和页码。

## 文件

- `index.html`：完整网站，包含样式、交互、语言切换和引用。
- `.nojekyll`：让 GitHub Pages 直接提供静态文件。
- `README.md`：本说明，不会显示在主页正文中。

本版按 https://www.wenbo.io/ 的排版和布局重制：约 880px 单栏正文、无衬线字体、右上圆形头像、圆形社交入口、正文上方语言切换、News 时间线、横向代表作轮播、按作者和贡献组织的论文列表。未提供博客文章，因此导航保留 About、Publications、Contact。页面代码针对本主页编写，代表作配图使用作者论文中的原图。

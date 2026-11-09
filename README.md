# tombumd · 同步马

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE.txt)

**MIT licensed · MIT 开源许可** — 自有代码可按 MIT 协议使用、修改及再分发。

**Write in the preview, edit the source beside it — both stay in sync.**
**在预览里直接写，源码在旁边同步改。**

A lightweight, fully offline WYSIWYG Markdown editor. 轻量、完全离线的所见即所得 Markdown 编辑器。

## Install · 安装

[![Chrome Web Store](https://img.shields.io/badge/Chrome-Add%20to%20Chrome-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white)](https://chromewebstore.google.com/detail/tombumd-%E2%80%93-wysiwyg-markdow/gfbhjeeledbfhaomhmbkpejkoekpacla)
[![Microsoft Edge Add-ons](https://img.shields.io/badge/Edge-Get%20it%20for%20Edge-0078D7?style=for-the-badge&logo=microsoftedge&logoColor=white)](https://microsoftedge.microsoft.com/addons/detail/tombumd-%E2%80%93-wysiwyg-markdow/nhgcaiooioglcjhehljniaeffefmeimg)
[![VS Code Marketplace](https://img.shields.io/badge/VS%20Code-Install-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)](https://marketplace.visualstudio.com/items?itemName=tombumd.tombumd)

- **Chrome**: [Chrome Web Store](https://chromewebstore.google.com/detail/tombumd-%E2%80%93-wysiwyg-markdow/gfbhjeeledbfhaomhmbkpejkoekpacla)
- **Edge**: [Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/tombumd-%E2%80%93-wysiwyg-markdow/nhgcaiooioglcjhehljniaeffefmeimg)
- **VS Code**: [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=tombumd.tombumd)（或在扩展面板搜索 `tombumd` · or search `tombumd` in the Extensions view）
- **Open VSX**（VSCodium / Cursor 等）: [open-vsx.org](https://open-vsx.org/extension/tombumd/tombumd)

## Why tombumd · 为什么选同步马

- **WYSIWYG + source, side by side** — type in the rendered page like in Word, or in the Markdown source; content and caret follow each other both ways.
  **所见即所得 + 源码双栏**：像 Word 一样在预览里写，也可以直接改源码，内容和光标双向同步。
- **Small and self-contained** — plain HTML + CSS + JS, a single ~4 MB file, no install, no server, no network. Math (LaTeX), code highlighting, Mermaid diagrams and anchors included.
  **小巧、零依赖**：纯 HTML + CSS + JS，单个文件约 4 MB，免安装、无需服务器、不联网；支持公式、代码高亮、流程图、锚点跳转。
- **Built-in formula editor** — click into any formula to edit it, or use the formula palette (`Ctrl+M`) with hundreds of symbols; edits sync both ways with the document.
  **内置公式编辑器**：点进公式即可修改，或用公式面板（`Ctrl+M`，数百个符号与模板），与正文双向同步。
- **A4 pages** — turn on the A4 preview to see real pages with margins, page numbers and page breaks; PDF, PNG and Word exports break pages exactly where the preview does.
  **A4 分页**：开启 A4 预览即可看到带页边距、页码、分页符的真实页面；导出 PDF、PNG、Word 的分页与预览一致。
- **Rich Markdown** — ==highlight==, admonitions (`!!! title`), `:::` boxes, image and table captions, `[TOC]`, footnotes, task lists, with one-click buttons to leave or remove a block's formatting.
  **更丰富的 Markdown**：==高亮==、提示块（`!!! 标题`）、`:::` 黄底块、图片 / 表格标题、`[TOC]` 目录、脚注、任务列表；块里有「去格式 / 新行」按钮。
- **Export & copy** — export to HTML (works offline), Word `.docx` (editable equations), PDF, PNG, LaTeX; copy as Markdown, for Word, or for WeChat Official Accounts.
  **导出与复制**：导出 HTML（离线可看）、Word（公式可编辑）、PDF、PNG 长图、LaTeX；一键复制 Markdown / Word / 公众号格式。

## Try it online · 在线体验

**👉 <https://tombumd.github.io/tombumd/>**

Opens the full editor in your browser — nothing to install, and your documents never leave your computer.
直接在浏览器里打开完整编辑器，免安装；文档只在你的电脑上处理，不会上传。

## Downloads · 下载

Latest version · 最新版本：**7.2.72**（VS Code：**2.3.69**）。

All four files are on the [latest Release](https://github.com/tombumd/tombumd/releases/tag/v7.2.72). 四个文件见[最新 Release](https://github.com/tombumd/tombumd/releases/tag/v7.2.72)；历史版本见 [Releases 页面](https://github.com/tombumd/tombumd/releases)。

| File 文件 | What it is 说明 |
| --- | --- |
| [`tombumd-7.2.72.html`](https://github.com/tombumd/tombumd/releases/download/v7.2.72/tombumd-7.2.72.html) | Single-file offline edition — download and open it in a browser, works without network. 单文件离线版，下载后用浏览器打开，断网可用。 |
| [`tombumd-chrome-7.2.72.zip`](https://github.com/tombumd/tombumd/releases/download/v7.2.72/tombumd-chrome-7.2.72.zip) | Chrome extension — unzip, open `chrome://extensions`, turn on Developer mode, *Load unpacked*. Chrome 插件：解压后打开 `chrome://extensions`，开启开发者模式，点“加载已解压的扩展程序”。 |
| [`tombumd-edge-7.2.72.zip`](https://github.com/tombumd/tombumd/releases/download/v7.2.72/tombumd-edge-7.2.72.zip) | Microsoft Edge extension — same steps at `edge://extensions`. Edge 插件：在 `edge://extensions` 中同样操作。 |
| [`tombumd-2.3.69.vsix`](https://github.com/tombumd/tombumd/releases/download/v7.2.72/tombumd-2.3.69.vsix) | VS Code extension — `code --install-extension tombumd-2.3.69.vsix`. VS Code 插件。 |

[Privacy policy · 隐私政策](https://tombumd.github.io/tombumd/privacy-policy.html)

## Changelog · 修改历史

Full release notes for each version are on the [Releases page](https://github.com/tombumd/tombumd/releases). 各版本完整更新说明见 [Releases 页面](https://github.com/tombumd/tombumd/releases)。

### v7.2.72 · VS Code 2.3.69 (2026-11-09)
- **Unified formula toolbar · 公式工具栏合并与白底风格**: Multi-line formula alignment (`=`, left, right, center) and brace (`{`, `}`) buttons are merged into the top-right `tag / label` toolbar so they never overlap the selection toolbar; unified white background with dark gray text, light-blue active state, and automatic wrapping in narrow windows. 多行公式的对齐与大括号按钮合并到右上角 tag / label 工具栏，避免与选区格式栏重叠；统一白底深灰字与浅蓝激活态，窄窗口自动换行。
- **Formula alignment spacing & unbraced arguments · 对齐间距与无花括号参数修复**: Fixed leading spacing in `align` / `aligned` when font or color commands wrap a relation symbol across preview, DOCX, and LaTeX exports; fixed single-token parsing and caret placement in unbraced fractions, scripts (`x^12`, `x^1.2`), roots, and accents, auto-adding braces on edit without swallowing adjacent tokens. 修复 `align` / `aligned` 中字体或颜色包住关系符时的起始间距（预览、DOCX、LaTeX 导出同步一致）；修复无花括号分式、上下标（保留 `x^12`、`x^1.2` 单记号指数语义）、根号与重音的单记号参数定位，编辑时自动补花括号。
- **Document title (`===`) & structure protection · 文档标题与结构保护**: Added Document Title (`===`) to the format menu and `/title` slash command with one-click centering; protected setext heading underlines, footnote definitions (`[^id]:`), and closing `#` markers from accidental boundary deletion. 格式菜单与 `/title` 新增“文档标题（`===`）”并支持一键居中转换；保护下划线标题、脚注定义与闭合井号不被跨界误删。
- **Firefox / code-server fallback & Chinese punctuation `/` menu · 火狐宿主兼容与中文标点斜杠菜单**: Added an allowlisted host fallback channel with CSP nonce verification when Service Worker virtual resource requests fail in Firefox / code-server; fixed `/` slash command triggering after Chinese punctuation (`、`, `，`, `。`) and preserved directional TeX selection highlights when unfocused. 修复部分 Firefox / code-server 环境虚拟资源请求失败导致编辑器与公式卡在加载的问题；修复中文标点后 `/` 指令菜单触发及 TeX 源码双向选区高亮。

### v7.2.67 · VS Code 2.3.64 (2026-11-08)
- **Live LaTeX source editing & three-way sync · 公式源码实时编辑与三端同步**: Edit LaTeX source directly inside the formula editor with instant preview and Markdown sync, shared undo/redo, and unfocused caret/selection indicators; movable and resizable Mermaid / Infographic source panel. 公式编辑器内支持 LaTeX 源码实时编辑，与公式预览及 Markdown 正文共享撤销 / 重做并保持光标与选区三向同步；Mermaid / Infographic 独立源码面板支持拖动、缩放与复位。

### v7.2.16 · VS Code 2.3.16 (2026-10-29)
- **Markdown compatibility, formula styling & worker regex search · 语法兼容、公式样式与 Worker 正则查找**: Reference-style links/images, CRLF sync & three-way merge in VS Code, formula font size / clear-color actions, and terminable Web Worker regex search/replace. 支持引用式链接与图片、CRLF 同步与 VS Code 三方合并、公式字号与清除颜色，以及可超时终止的 Worker 正则查找替换。

### v7.2.12 · VS Code 2.3.12 (2026-10-25)
- **Selection toolbar, `/` slash commands, folding & annotations · 选区格式栏、斜杠指令、折叠与批注**: Floating selection toolbar, `/` slash menu, heading and code block folding, annotations, centered headings, and CJK whole-word search. 新增选中文字浮动格式栏、`/` 斜杠指令、标题与代码块折叠、批注、标题居中及中文全词匹配查找。

## License · 协议

tombumd's own code is released under the [MIT License](LICENSE.txt), © 2026 tombumd.
Bundled third-party libraries (DOMPurify, MathJax, highlight.js, gemoji, mermaid, html2canvas, jsPDF, jsdiff, AntV Infographic) keep their own licenses —
see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and [licenses/](licenses/).

你用同步马创作的文档归你所有。

同步马自身代码使用标准 [MIT 协议](LICENSE.txt)；随附的第三方库遵循各自的协议，见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) 与 [licenses/](licenses/)。

# tombumd · 同步马

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
- **Small and self-contained** — plain HTML + CSS + JS, a single ~3 MB file, no install, no server, no network. Math (LaTeX), code highlighting, Mermaid diagrams and anchors included.
  **小巧、零依赖**：纯 HTML + CSS + JS，单个文件约 3 MB，免安装、无需服务器、不联网；支持公式、代码高亮、流程图、锚点跳转。
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

All files are on the [Releases page](https://github.com/tombumd/tombumd/releases/latest). 所有文件见 [Releases 页面](https://github.com/tombumd/tombumd/releases/latest)。

| File 文件 | What it is 说明 |
| --- | --- |
| [`tombumd-7.1.3.html`](https://github.com/tombumd/tombumd/releases/download/v7.1.3/tombumd-7.1.3.html) | Single-file offline edition — download and open it in a browser, works without network. 单文件离线版，下载后用浏览器打开，断网可用。 |
| [`tombumd-chrome-7.1.3.zip`](https://github.com/tombumd/tombumd/releases/download/v7.1.3/tombumd-chrome-7.1.3.zip) | Chrome extension — unzip, open `chrome://extensions`, turn on Developer mode, *Load unpacked*. Chrome 插件：解压后打开 `chrome://extensions`，开启开发者模式，点“加载已解压的扩展程序”。 |
| [`tombumd-edge-7.1.3.zip`](https://github.com/tombumd/tombumd/releases/download/v7.1.3/tombumd-edge-7.1.3.zip) | Microsoft Edge extension — same steps at `edge://extensions`. Edge 插件：在 `edge://extensions` 中同样操作。 |
| [`tombumd-2.2.3.vsix`](https://github.com/tombumd/tombumd/releases/download/v7.1.3/tombumd-2.2.3.vsix) | VS Code extension — `code --install-extension tombumd-2.2.3.vsix`. VS Code 插件。 |

[Privacy policy · 隐私政策](https://tombumd.github.io/tombumd/privacy-policy.html)

## License · 协议

tombumd's own code is released under the [MIT License](LICENSE.txt), © 2026 tombumd.
Bundled third-party libraries (MathJax, highlight.js, mermaid, html2canvas, jsPDF, jsdiff) keep their own licenses —
see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and [licenses/](licenses/).

同步马自身代码使用 [MIT 协议](LICENSE.txt)；随附的第三方库遵循各自的协议，见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) 与 [licenses/](licenses/)。

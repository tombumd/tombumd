# Third-Party Notices · 第三方软件声明

All files in this repository (`index.html`, `tombumd-6.1.0.html`, `tombumd-chrome-6.1.0.zip`, `tombumd-edge-6.1.0.zip`, `tombumd-2.0.0.vsix`)
contain tombumd's (同步马) own code, released under the MIT License (`LICENSE.txt`), **plus the unmodified third-party libraries listed below**,
which keep their own licenses. Full license texts are in `licenses/`. Each package also carries its own copy of these notices
(the single HTML file at its end, the zip files and the `.vsix` as `LICENSE.txt` / `THIRD_PARTY_NOTICES.md` / `licenses/`).

本仓库所有发布文件都包含 tombumd（同步马）自己的代码（MIT 协议，见 `LICENSE.txt`）以及下列**未修改**的第三方库；第三方库遵循各自的协议，
协议全文在 `licenses/`。每个发布包里也各自带有一份声明（单文件 HTML 在文件末尾，zip 与 `.vsix` 里是 `LICENSE.txt` / `THIRD_PARTY_NOTICES.md` / `licenses/`）。

> The VS Code extension (`tombumd-2.0.0.vsix`) ships the same libraries except jsdiff, under `media/lib/`.
> VS Code 插件（`tombumd-2.0.0.vsix`）随附的库与下表相同（不含 jsdiff），位于 `media/lib/`。

---

| Library 库 | Version 版本 | File 文件 | License 协议 | Copyright 版权 | Used for 用途 |
| --- | --- | --- | --- | --- | --- |
| [MathJax](https://www.mathjax.org/) | 3.2.2 (npm `mathjax@3.2.2`, `es5/tex-svg-full.js`) | `lib/mathjax.js` | Apache-2.0 | © The MathJax Consortium | 公式渲染；有公式时内嵌进导出的 HTML · math rendering; embedded in exported HTML |
| [highlight.js](https://highlightjs.org/) | 11.10.0 (npm `@highlightjs/cdn-assets@11.10.0`, `highlight.min.js`) | `lib/highlight.min.js` | BSD-3-Clause | © 2006 Ivan Sagalaev; Josh Goebel and other contributors | 代码高亮 · code highlighting |
| [mermaid](https://mermaid.js.org/) | 11.17.2 (npm `mermaid`, `dist/mermaid.min.js`) | `lib/mermaid.min.js` | MIT | © 2014–2022 Knut Sveidqvist | 流程图（按需加载）· diagrams (loaded on demand) |
| [html2canvas](https://html2canvas.hertzen.com/) | 1.4.1 (npm `html2canvas`, `dist/html2canvas.min.js`) | `lib/html2canvas.min.js` | MIT | © 2012 Niklas von Hertzen | 导出 PNG / PDF（按需加载）· PNG / PDF export |
| [jsPDF](https://github.com/parallax/jsPDF) | 2.5.1 (npm `jspdf`, `dist/jspdf.umd.min.js`) | `lib/jspdf.umd.min.js` | MIT | © 2010–2021 James Hall; © 2015–2021 yWorks GmbH | 导出 PDF（按需加载）· PDF export |
| [jsdiff](https://github.com/kpdecker/jsdiff) | 5.2.0 (npm `diff`, `dist/diff.min.js`) | `lib/diff.min.js` | BSD-3-Clause | © 2009–2015 Kevin Decker | 版本面板的逐行差异 · line diff in the version panel |

## Notes · 说明

### MathJax (Apache-2.0)

- `lib/mathjax.js` = the official MathJax 3.2.2 `es5/tex-svg-full.js`, **byte-for-byte, unmodified**.
  `lib/mathjax.js` 是 MathJax 3.2.2 官方 `es5/tex-svg-full.js`，逐字节原样，未作任何修改。
- The offline configuration (it only sets `MathJax.tex.require.allow` so that `\require{…}` never tries to download extensions)
  lives in tombumd's own file `js/mathjax-shim.js` (bundled into `js/tombumd.js`), run before MathJax. In the web version (allv6) this shim was prepended
  to mathjax.js; the extension keeps it separate so the library stays identical to the official release.
  离线配置垫片放在 tombumd 自己的 `js/mathjax-shim.js`（打包进 `js/tombumd.js`），在 MathJax 之前执行；网页版 allv6 是把它拼在 mathjax.js 开头，插件版拆开，让第三方库与官方发布保持一致。
- The official file has no copyright header of its own (only the bundled mhchem parser, © Martin Hensel, Apache-2.0, keeps its header),
  so the Apache-2.0 text is shipped as `licenses/MathJax-LICENSE.txt`.
  官方文件本身没有版权头（只有内含的 mhchem 保留了头部注释），因此 Apache-2.0 全文放在 `licenses/MathJax-LICENSE.txt`。
- When tombumd exports HTML with formulas, it embeds MathJax in the exported page, preceded by a notice comment
  (`MathJax 3.2.2, (c) The MathJax Consortium, Apache License 2.0` + license URL) and the clearly marked tombumd shim.
  导出含公式的 HTML 时，内嵌的 MathJax 前面会加一段版权与协议说明注释，以及标明出处的 tombumd 垫片（满足 Apache-2.0 第 4 条的署名要求）。

### highlight.js (BSD-3-Clause)

- Redistribution requires keeping the copyright notice, the list of conditions and the disclaimer — the file header
  and `licenses/highlight.js-LICENSE.txt` do this. The names of the authors may not be used to endorse tombumd.
  再分发需保留版权声明、条件列表和免责声明（已保留）；不得用原作者名义为 tombumd 背书。

### mermaid (MIT) and the libraries it bundles

`mermaid.min.js` is the upstream single-file build. It bundles, among others (licenses from npm):

| Package | License |
| --- | --- |
| d3 | ISC |
| d3-sankey | BSD-3-Clause |
| dagre-d3-es, cytoscape, cytoscape-cose-bilkent, cytoscape-fcose, cose-base, layout-base | MIT |
| katex, marked, dayjs, khroma, roughjs, stylis, ts-dedent, uuid, es-toolkit, fastdom | MIT |
| @braintree/sanitize-url, @iconify/utils, @upsetjs/venn.js, @mermaid-js/parser, langium, vscode-languageserver-types, vscode-jsonrpc | MIT |
| chevrotain | Apache-2.0 (text: `licenses/MathJax-LICENSE.txt` is the same Apache-2.0 text) |
| DOMPurify 3.4.12 | MPL-2.0 OR Apache-2.0 — used under **Apache-2.0** (`licenses/DOMPurify-LICENSE.txt`) |

### jsPDF (MIT) and the code it bundles

`jspdf.umd.min.js` is the upstream build. Its license comments are preserved inside the file, including:
FileSaver.js (MIT), omggif (MIT, © Dean McNamee), png.js (MIT), the Adobe JPEG encoder port (BSD-3-Clause, © 2008 Adobe Systems Incorporated),
RGBColor (Stoyan Stefanov), fflate (MIT), and contributions by the authors listed in its header.

### jsdiff (BSD-3-Clause)

- The minified build has no license header of its own, so the full license text is shipped as `licenses/jsdiff-LICENSE.txt`
  (BSD-3-Clause requires reproducing the notice in the documentation of a binary/minified redistribution).
  压缩版文件里没有协议头，协议全文放在 `licenses/jsdiff-LICENSE.txt`（BSD-3 要求随分发附上声明）。

### html2canvas (MIT)

Includes tslib (© Microsoft Corporation, 0BSD-style permission notice, kept in the file header).

### Exported files · 导出的文件

- Exported HTML embeds MathJax (Apache-2.0) preceded by a copyright/license notice comment; if you publish exported pages, keep that comment.
  Highlighting in exported HTML is pre-rendered (only CSS class names and colours, no highlight.js code); diagrams are inline SVG produced by mermaid.
  导出的 HTML 内嵌的 MathJax 前面带有版权与协议说明注释，发布时请保留；代码高亮是预先生成的标记和配色（不含 highlight.js 代码）；流程图是 mermaid 生成的 SVG。

## What you must do when redistributing · 再分发时要做的事

1. Keep `LICENSE.txt`, `THIRD_PARTY_NOTICES.md` and the `licenses/` folder when you copy or publish this folder.
   复制或发布本文件夹时，保留 `LICENSE.txt`、本文件和 `licenses/` 文件夹。
2. Don't strip the license headers from the files in `lib/`. 不要删掉 `lib/` 里各文件开头的版权/协议注释。
3. If you modify a third-party file, say so in that file (Apache-2.0 §4(b)). 修改第三方文件时在文件里注明。
4. Don't use the names of MathJax / highlight.js authors to promote tombumd (BSD-3-Clause, Apache-2.0 §6). 不要用第三方作者或商标为 tombumd 背书。


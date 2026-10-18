# Third-Party Notices · 第三方软件声明

tombumd's (同步马) own code is © 2026 tombumd, released under the MIT License (see `LICENSE.txt`). The notices below apply only to the third-party libraries.
This browser extension (allv6_x_one) ships the following third-party libraries in `lib/`, **byte-for-byte identical** to the official
npm releases listed below (verified by file comparison). They are not minified, obfuscated or otherwise processed by our build.
The extension loads nothing from the network: every library is a local file.
Their licenses still apply to them; full license texts are in the `licenses/` folder.

tombumd 自身代码 © 2026 tombumd，使用 MIT 协议（见 `LICENSE.txt`），下面的声明只针对第三方库。本浏览器插件版（allv6_x_one）不连任何网络地址；`lib/` 里的第三方库与下表所列官方 npm 发布**逐字节一致**
（已逐个比对），构建时不压缩、不混淆、不做任何处理；它们仍遵循各自的协议，完整协议文本在 `licenses/` 文件夹。

| Library 库 | Version 版本 | File 文件 | License 协议 | Copyright 版权 | Used for 用途 |
| --- | --- | --- | --- | --- | --- |
| [MathJax](https://www.mathjax.org/) | 3.2.2 (npm `mathjax@3.2.2`, `es5/tex-svg-full.js`) | `lib/mathjax.js` | Apache-2.0 | © The MathJax Consortium | 公式渲染；有公式时内嵌进导出的 HTML · math rendering; embedded in exported HTML |
| [highlight.js](https://highlightjs.org/) | 11.10.0 (npm `@highlightjs/cdn-assets@11.10.0`, `highlight.min.js`) | `lib/highlight.min.js` | BSD-3-Clause | © 2006 Ivan Sagalaev; Josh Goebel and other contributors | 代码高亮 · code highlighting |
| [gemoji](https://github.com/github/gemoji) 名字表 · emoji names | 1837 names (from VS Code git extension `emojis.json`) | `lib/emoji.js` | MIT | © 2019 GitHub, Inc. | `:smile:` → 😄（按需加载；只是名字表，由 tombumd 转成 js，不是原样文件）· emoji shortcodes (loaded on demand; name table converted to js) |
| [mermaid](https://mermaid.js.org/) | 11.17.2 (npm `mermaid`, `dist/mermaid.min.js`) | `lib/mermaid.min.js` | MIT | © 2014–2022 Knut Sveidqvist | 流程图（按需加载）· diagrams (loaded on demand) |
| [html2canvas](https://html2canvas.hertzen.com/) | 1.4.1 (npm `html2canvas`, `dist/html2canvas.min.js`) | `lib/html2canvas.min.js` | MIT | © 2012 Niklas von Hertzen | 导出 PNG / PDF（按需加载）· PNG / PDF export |
| [jsPDF](https://github.com/parallax/jsPDF) | 2.5.1 (npm `jspdf`, `dist/jspdf.umd.min.js`) | `lib/jspdf.umd.min.js` | MIT | © 2010–2021 James Hall; © 2015–2021 yWorks GmbH | 导出 PDF（按需加载）· PDF export |
| [jsdiff](https://github.com/kpdecker/jsdiff) | 5.2.0 (npm `diff`, `dist/diff.min.js`) | `lib/diff.min.js` | BSD-3-Clause | © 2009–2015 Kevin Decker | 版本面板的逐行差异 · line diff in the version panel |
| [AntV Infographic](https://github.com/antvis/Infographic) | 0.2.20 (npm `@antv/infographic`, `dist/infographic.min.js`) | `lib/infographic.min.js` | MIT | © 2025 AntV | 信息图（```infographic 代码块，按需加载）· infographics (loaded on demand) |

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

### AntV Infographic (MIT) and the code it bundles

`infographic.min.js` is the upstream UMD build, unmodified (full license: `licenses/infographic-LICENSE.txt`). It bundles d3 (ISC), linkedom (ISC),
postcss, roughjs, lodash-es, culori, tinycolor2, eventemitter3, flru, measury, round-polygon, @antv/layout, @antv/hierarchy (all MIT).
The library would download fonts (assets.antv.antgroup.com) and search icons online (weavefox.cn); the editor hands it a fetch that only allows
data: / blob: URLs at load time and re-registers the built-in web fonts without URLs, so it never connects to the network.
本库原样内嵌；它默认会联网加载字体、搜索图标，编辑器在加载它时给它一个只放行 data: / blob: 的 fetch，并把内置网络字体改注册成无地址的同名字体，因此不会联网（条目里写的 icon 不显示）。

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

## Build tools (not distributed) · 构建工具（不随插件分发）

The build uses [terser](https://github.com/terser/terser) (BSD-2-Clause) to bundle and minify tombumd's own code and [fflate](https://github.com/101arrowz/fflate) (MIT)
to create zip files.
None of their code is included in the extension package.
构建时用 terser 合并压缩 tombumd 自己的代码、fflate 打 zip 包；它们的代码都不进入插件包。

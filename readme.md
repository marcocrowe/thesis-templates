# [Thesis Templates](https://github.com/markcrowe-com/thesis-templates)

A collection of example thesis templates with a sample Table of Contents with the relevant styles to get you started.  

## Thesis Sample Templates
- Sample AI Thesis: [sample-ai-thesis.docx](./sample-ai-thesis.docx)

## Recommended Editors

- [Microsoft Office Word](https://www.microsoft.com/microsoft-365/)
- [Microsoft Office Word Online at Microsoft 365](https://www.office.com/launch/word)
- [VS Code](https://code.visualstudio.com/):
  - [`Office Viewer`](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-office)

## Conversion Tools
- Brave Browser: [https://brave.com/](https://brave.com/) and extensions
  -  [`Markdown Viewer`](https://chrome.google.com/webstore/detail/markdown-viewer/ckkdlimhmcjmikdlpkmbgfkaikojcbjk)
  -  [`Link Shortener`](https://timleland.com/link-shortener-extension/)
- Pandoc: [https://pandoc.org/](https://pandoc.org/)

## Diagrams
- Mermaid: [https://mermaid-js.github.io/mermaid-live-editor/](https://mermaid-js.github.io/mermaid-live-editor/)

Command to convert Word to Markdown:
```bash
pandoc -f docx -t markdown sample-ai-thesis.docx -o sample-ai-thesis.md --extract=./images/sample-ai-thesis
```

---
Copyright (c) 2021 Mark Crowe <https://github.com/markcrowe-com>. All rights reserved. 
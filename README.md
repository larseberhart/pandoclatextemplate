## About

Heavily modified template files to typeset PDFs from Markdown using LaTeX/XeLaTeX and Pandoc.

## Usage

Two templates are included (template.tex and notiztemplate.tex). A note written in Markdown should have the document a document header with date, author and topic. If the date is left empty, the current date will be used. The included example shows the header formatting.

It shuold be:
```
---
date: xx.yy.zz or empty
author: put the name of the author here
topic: put the topic here
---
```

After saving the Markdown file, call Pandoc and a PDF file will be generated. 

The command for mytemplate.tex:
`pandoc input.md  --template=mytemplate.tex --pdf-engine=xelatex --variable mainfont="Helvetica" --variable linestretch=1.25  -o output.pdf`

The command for notiztemplate.tex:
`pandoc input.md --template=notiztemplate.tex --pdf-engine=xelatex --variable mainfont="Helvetica" -o output.pdf`

## Required Software

These templates were tested on macOS and should work under Linux. A LeTeX distribution and Pandoc are required.

LaTeX: tested with [MacTex](http://www.tug.org/mactex/)
Pandoc: tested with Pandoc installed from [MacPorts](https://www.macports.org).

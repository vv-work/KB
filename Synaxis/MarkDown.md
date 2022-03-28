Markdown

## Referecnes

- [StyleGuide](https://cirosantilli.com/markdown-style-guide/#option-header-atx)

## Tableo


`:TableFormat`

```
Before.

| h    | Long header |
|------|-------------|
| abc  | def       |
| abc2 | def2        |

After.
```


## Markdown for Vim

- [Github repo](https://github.com/preservim/vim-markdown)

### Create vertical navigable table

`:Toc`- create a quickfix vertical window navigable table of contents with the headers.
`:InsertToc`
`:InsertToc 3` for `H3`
:

### Folding

zr: reduces fold level throughout the buffer
zR: opens all folds

zm: increases fold level throughout the buffer
zM: folds everything all the way
za: open a fold your cursor is on
zA: open a fold your cursor is on recursively
zc: close a fold your cursor is on
`zC:` close a fold your cursor is on recursively

Try :help fold-expr and :help fold-commands for details.

## MarkDowa to PDF

- [project]://github.com/simonhaenisch/md-to-pdf)

`md-to-pdf ./**/*.md`

### Page break


```html
<div class="page-break"></div>
```

```PowerShell
$ md-to-pdf [options] path/to/file.md

Options:

  -h, --help ............... Output usage information
  -v, --version ............ Output version
  -w, --watch .............. Watch the current file(s) for changes
  --watch-options .......... Options for Chokidar's watch call
  --basedir ................ Base directory to be served by the file server
  --stylesheet ............. Path to a local or remote stylesheet (can be passed multiple times)
  --css .................... String of styles
  --document-title ......... Name of the HTML Document.
  --body-class ............. Classes to be added to the body tag (can be passed multiple times)
  --page-media-type ........ Media type to emulate the page with (default: screen)
  --highlight-style ........ Style to be used by highlight.js (default: github)
  --marked-options ......... Set custom options for marked (as a JSON string)
  --pdf-options ............ Set custom options for the generated PDF (as a JSON string)
  --launch-options ......... Set custom launch options for Puppeteer
  --gray-matter-options .... Set custom options for gray-matter
  --port ................... Set the port to run the http server on
  --md-file-encoding ....... Set the file encoding for the markdown file
  --stylesheet-encoding .... Set the file encoding for the stylesheet
  --as-html ................ Output as HTML instead
  --config-file ............ Path to a JSON or JS configuration file
  --devtools ............... Open the browser with devtools instead of creating PDF
```
## Custom image size

`<img src="drawing.jpg" alt="drawing" width="200"/>` - set custom image size

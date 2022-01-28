# Markdown

## Custom image size

`<img src="drawing.jpg" alt="drawing" width="200"/>` - set custom image size

## MarkDowa to PDF

- [project]://github.com/simonhaenisch/md-to-pdf)

```PowerShell
md-to-pdf ./**/*.md
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

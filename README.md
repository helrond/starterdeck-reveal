# starterdeck-reveal

## Credits

*   reveal.js
*   Jronallo
*   https://gist.github.com/aaronwolen/5017084

## Slide formats

### YAML front matter

    ---
    title: Advanced Archival Description - Week 1
    footer: footer text
    theme: simple
    css: week1.css
    transition: linear
    option:
      -history: true
      -controls: true
      -progress: true
    ---

## npm

*   markdown file
*   theme
*   transition

define file to watch
open up file in browser automatically
live reload

## CSS

Add theme
Additional CSS

## Pandoc

`pandoc -t html5 --template=template-revealjs.html  --self-contained --section-divs presentations/week1.md -o presentations/week1.html`

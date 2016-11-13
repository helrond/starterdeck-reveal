# starterdeck-reveal

## Credits

*   reveal.js
*   Jronallo
*   https://gist.github.com/aaronwolen/5017084

## Install

pandoc

`npm install`

`grunt --target=filename`

## Slide formats

[Pandoc documentation](http://pandoc.org/MANUAL.html#producing-slide-shows-with-pandoc)

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

## CSS

Add theme
Additional CSS

## Pandoc

`pandoc -t revealjs --template=template-revealjs.html  --slide-level=1 --self-contained --section-divs presentations/week1.md -o presentations/week1.html`

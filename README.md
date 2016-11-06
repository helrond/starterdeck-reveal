# starterdeck-reveal

## Credits

*   reveal.js
*   Jronallo
*   https://gist.github.com/aaronwolen/5017084

## Slide formats

## npm

*   markdown file
*   theme
*   transition
*   variable-highlight

define defaults
open up file in browser automatically
live reload

custom css? - maybe enter a filename for markdown, which is also html and css? Or specify these in the markdown?

## Pandoc

pandoc -t html5 --template=template-revealjs.html  --self-contained --section-divs presentations/week1.md -o presentations/week1.html


--variable theme="beige"
--variable transition="linear"
--variable highlight-style="css filename"

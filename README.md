# starterdeck-reveal

Starter slide deck for presentations, using [Pandoc](http://pandoc.org/) and [Reveal.js](http://lab.hakim.se/reveal-js/#/). The idea for this came from Jason Ronallo's [starterdeck-node](https://github.com/jronallo/starterdeck-node).

## Install

To get started, you'll need to [install pandoc](http://pandoc.org/installing.html). I like [homebrew](http://brew.sh/), so I just use `brew install pandoc`

After that, you can just download or clone the repository:

`git clone git@github.com:helrond/starterdeck-reveal.git`

and then install dependencies:

`npm install`

After that, it's just a matter of placing a Markdown file with your content in the `presentations/` directory (see below for formatting) and then running:

`grunt --target=filename`

where `filename` is the name of your Markdown file without an extension, to run pandoc and load the resulting HTML file in your browser.

## Slide formats

In order for slides to be properly formatted, you'll need to adhere to some simple rules. The [pandoc documentation](http://pandoc.org/MANUAL.html#producing-slide-shows-with-pandoc) has a number of examples and details.

### YAML front matter

In addition, each Markdown file contains a custom YML frontmatter block formatted as follows:

    ---
    title: Advanced Archival Description - Week 1
    footer: footer text
    theme: simple
    css: week1.css
    transition: linear
    slide-level: 1
    fonts:
    - "Raleway"
    - "Open+Sans"
    option:
    - "history: true"
    - "controls: true"
    - "progress: true"
    ---

  `title` - the title of the presentation, which is added to the `title` tag.

  `footer` - text to be added to a custom footer that appears on all slides.

  `theme` - the filename of a reveal.js theme located in the `css/themes/` directory.

  `css` - the filename of a custom css file located in the `css/` directory.

  `transition` - the slide transition, which can be one of `none/fade/slide/convex/concave/zoom`.

  `slide-level` - the level at which slides break. See [pandoc documentation](http://pandoc.org/MANUAL.html#structuring-the-slide-show) for more details.

  `fonts` - a list of Google Web fonts to be included in the document's head. These names are case-sensitive, need to be enclosed in quotation marks, and spaces must be replaced with `+`.

  `option` - a list of additional reveal.js options you want to add. See [official documentation](https://github.com/hakimel/reveal.js/#configuration) for more information.


## CSS

All standard reveal.js themes are available in the `css/themes/` directory. You can create your own, or extend one by adding additional CSS in the `css/` directory.

## Pandoc

If you want to convert the files manually, you can run the following command:

`pandoc -t revealjs --template=template-revealjs.html  --slide-level=1 --self-contained --section-divs presentations/presentation.md -o presentations/presentation.html`

where `presentation` is the filename of your Markdown file without the extension.

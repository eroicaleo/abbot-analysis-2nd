# Development Environment Steup

## Project page generation

* To make the project page, install `mkdocs`:

```sh
pip install mkdocs
```

* Then install `python-markdown-math`

```sh
pip install python-markdown-math
```

* To initialize the directory

```sh
mkdocs new .
```

* To generate the documentation

```sh
mkdocs serve
```

* To deploy to github

```sh
mkdocs gh-deploy
```

* And the updated document is available at [https://eroicaleo.github.io/abbot-analysis-2nd/](https://eroicaleo.github.io/abbot-analysis-2nd/)

### `mkdocs` reference

* [Official Site](https://www.mkdocs.org)
* [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
* [Creating a beautiful documentation site with MkDocs](https://www.blimped.nl/creating-a-beautiful-documentation-site-with-mkdocs/)

### How to display math properly

* I follow [this instructions](https://squidfunk.github.io/mkdocs-material/reference/math/).
    * I need to create a `docs/javascripts/mathjax.js`
    * I also need to do the following in `mkdocs.yml`
    * About mathjax version: see [here](https://www.mathjax.org/#gettingstarted).
```ymal
markdown_extensions:
  - pymdownx.arithmatex:
      generic: true

extra_javascript:
  - javascripts/mathjax.js
  - https://unpkg.com/mathjax@3/es5/tex-mml-chtml.js
```

* If I just need to use 2.7.7, then I can simply do:
    * See [here](https://docs.mathjax.org/en/v2.7-latest/configuration.html)

```ymal
extra_javascript: 
    - https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-AMS-MML_CHTML
```

## VScode extensions

* I use VScode as my IDE. To make typing equation easier in markdown file, the following 3 extensions have been installed:
    * `Markdown+Math`
    * [`Math Snippets`](https://github.com/thomanq/math-snippets/blob/master/snippets/snippets.json)
    * `Markdown All in One`

* With these 3 extensions, I can write equations easier, e.g.
    * Use `ii` to insert inline equations.
    * Use `dd` to insert display math.

* Other user defined latex snippet are located under `snippets/latex.json`. It's better to create a global user snippet and copy over the contents to there: (control palette -> "Snippets" -> "New Global").

* In addition, to make the intellisense work for markdown file, I need to edit the `settings.json`
  (control palette -> "open user settings") by adding the following lines.

```json
    "[markdown]": {
        "editor.quickSuggestions": {
            "other": true,
            "comments": false,
            "strings": false
        }
    }
```

* Furthurmore, I would like to use Tab key to cycle through the suggestions, so I need to edit the `keybindings.json` file (control palette -> "Preference: Open Keyboard Shortcuts (JSON)"). The reference is [here](https://stackoverflow.com/questions/48097507/visual-studio-code-use-tab-instead-of-arrow-keys-to-select-intellisense-sugge).

```json
{
        "key": "tab",
        "command": "selectNextSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
      },
      {
        "key": "down",
        "command": "-selectNextSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
      },
        {
        "key": "shift+tab",
        "command": "selectPrevSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
      },
      {
        "key": "up",
        "command": "-selectPrevSuggestion",
        "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
      }
```

## Similar Projects

* [linearalgebras.com](https://linearalgebras.com/solution-understanding-analysis.html)
* [github](https://github.com/mikinty/Understanding-Analysis-Abbott-Solutions)
* [github UlisseMini](https://github.com/UlisseMini/understanding-analysis-solutions)
* [solverer.com](https://solverer.com/library/stephen_abbott/understanding_analysis)
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

* To generate the documentation

```sh
mkdocs gh-deploy
```

* And the updated document is available at [https://eroicaleo.github.io/abbot-analysis-2nd/](https://eroicaleo.github.io/abbot-analysis-2nd/)
## VScode extensions

* I use VScode as my IDE. To make typing equation easier in markdown file, the following 3 extensions have been installed:
    * `Markdown+Math`
    * `Math Snippets`
    * `Markdown All in One`

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
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

## VScode extensions

* I use VScode as my IDE. To make typing equation easier in markdown file, the following 3 extensions have been installed:
    * `Markdown+Math`
    * [`Math Snippets`](https://github.com/thomanq/math-snippets/blob/master/snippets/snippets.json)
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

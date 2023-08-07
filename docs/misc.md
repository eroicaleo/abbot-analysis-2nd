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

## VScode extensions

* To make typing equation easier in markdown file, the following 3 extensions have been installed:
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
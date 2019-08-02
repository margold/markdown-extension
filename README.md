# VSCode Markdown Injection Grammar

This extension defines additional scopes for my personal notewriting purposes. Highlighting "TODO", for example. It won't be of much use to you directly, but you can clone and modify it to suit your own notetaking habits.

## Development

* Press `F5` to open a new window with your extension loaded. This works if you have a `.vscode/launch.json` file in your extension folder.
* Verify that syntax highlighting works and that the language configuration settings are working (`Developer: Inspect TM Scopes). Consult the [docs](https://code.visualstudio.com/api/language-extensions/syntax-highlight-guide) to learn more about TextMate grammars and the Scope Inspector. TextMate grammars use [Onigurumu regular expressions](https://macromates.com/manual/en/regular_expressions).
* You can relaunch the extension from the debug toolbar after making changes. Or you can reload (`Ctrl+R` or `Cmd+R` on Mac) the VS Code window with your extension to load your changes.

## Installation

* To start using your extension with Visual Studio Code copy it into the `<user home>/.vscode/extensions` folder and restart Code.
* To share your extension with the world, read on https://code.visualstudio.com/docs about publishing an extension.

## Styling

Once you defined the injection grammar, you also need to define a theme to style your new scopes. For small injections, you can add your styling to your workspace settings by adding them to `editor.tokenColorCustomizations` like so:

    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                "scope": [
                    "punctuation.definition.heading.markdown"
                ],
                "settings": {
                    "foreground": "#dc322f",
                    "fontStyle": "bold",
                }
            },
            {
                "scope": [
                    "markup.heading.markdown"
                ],
                "settings": {
                    "foreground": "#002b36",
                    "fontStyle": "bold",
                }
            },
            {
                "scope": [
                    "heading.unindented.listitem.markdown"
                ],
                "settings": {
                    "foreground": "#cb4b16",
                    "fontStyle": "bold",
                }
            },
            {
                "scope": [
                    "todo.any.listitem.markdown"
                ],
                "settings": {
                    "foreground": "#dc322f",
                    "fontStyle": "bold",
                }
            }
        ]
    }
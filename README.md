# SQLFLUFF config

Basic config for [sqlfluff](https://docs.sqlfluff.com/en/stable/) linter. By default it uses postgres dialect.

## Installation

1. Install [python](https://www.python.org/downloads/)
2. Install [sqlfluff](https://docs.sqlfluff.com/en/stable/gettingstarted.html#installing-sqlfluff)

    ```bash
    pip install sqlfluff
    ```

3. Install vs-code [sqlfluff extension](https://marketplace.visualstudio.com/items?itemName=dorzey.vscode-sqlfluff) for VSCode
4. Open VSCode preferences
5. Search for `sqlfluff`
6. Click on `Edit in settings.json` at one of the setting (should be in tab `User`)
7. Save [.sqlfluff](./.sqlfluff) file in somewhere in your computer (e.g. `C:/projects/config/.sqlfluff`)
8. Add settings template from [./.vscode/settings.json](./.vscode/settings.json) and modify it to your needs (e.g. change `"sqlfluff.config": "C:/projects/config/.sqlfluff"` to the path where you saved the `.sqlfluff` file)
9. Save the file
10. Open a `.sql` file and you should see the linter working

## Usage in individual projects

1. Do steps 1-5 from the installation section
2. Save [.sqlfluff](./.sqlfluff) file in your project (e.g. `${workspaceFolder}/.sqlfluff`)
3. Add settings template from [./.vscode/settings.json](./.vscode/settings.json) and change `sqlfluff.config` to the sqlfluff config file path in your project (e.g. `${workspaceFolder}/.sqlfluff`))
4. Save the file
5. Open a `.sql` file and you should see the linter working

## Tips and tricks

- You can use `Ctrl + Shift + P` to open the command palette and search for `sqlfluff` to see all the available commands _(vs-code default shortcut)_
- You can use `Ctrl + Alt + F` to format the current file _(vs-code default shortcut)_
- Run `sqlfluff parse .\path\to\sql\code_file.sql --dialect postgres` to see the parsed code _(you can change the dialect to any of the supported dialects)_. Replace `.\path\to\sql\code_file.sql` with the path to your sql file.
- Run `sqlfluff lint .\path\to\sql\code_file.sql --dialect postgres` to see the linting results _(you can change the dialect to any of the supported dialects)_. Replace `.\path\to\sql\code_file.sql` with the path to your sql file.
- Run `sqlfluff fix .\path\to\sql\code_file.sql --dialect postgres` to fix the linting errors _(you can change the dialect to any of the supported dialects)_. Replace `.\path\to\sql\code_file.sql` with the path to your sql file.

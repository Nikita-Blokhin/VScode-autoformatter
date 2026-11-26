# Сборник шаблонов и автоматизации форматирования кода

Необходимо использовать для ведения единой структуры проектов и стилистики кода

## Расширения и настройки VS code для автоформатирования кода и упрощения ведения разработки продуктов

### Общее

- Russian Language Pack for Visual Studio Code
- Format Files
- ENV

### Python

- Black Formatter
- isort
- Pylance
- Python
- Python Debugger
- Python Environments

### TS/JS

- ESLint
- JS/TS Import/Export Sorter
- Prettier - Code formatter
- TypeScript 7

### JAVA

- Java
- Google Java Format for VS Code

### Минимальный настройки в settings.json в VS code

Найстройки vscode находятся по пути:

1. WINDOWS:

```
C:\Users\{имя_пользователя}\AppData\Roaming\Code\User\settings.json
```

2. MAC:

```
$HOME/Library/Application Support/Code/User/settings.json
```

3. Linux:

```
$HOME/.config/Code/User/settings.json
```

Настройки, которые необходимы быть и использоваться во время разработки:

```json
{
    "editor.rulers": [79],
    "editor.formatOnSave": true,
    "editor.formatOnPaste": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "js/ts.preferences.quoteStyle": "single",
    "prettier.printWidth": 79,
    "prettier.tabWidth": 4,
    "prettier.singleQuote": true,
    "prettier.semi": false,
    "prettier.trailingComma": "none",
    "[typescript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[typescriptreact]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode",
        "editor.codeActionsOnSave": {
            "source.organizeImports": "always"
        }
    },
    "[jsonc]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[json]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[python]": {
        "editor.defaultFormatter": "ms-python.black-formatter",
        "editor.codeActionsOnSave": {
            "source.organizeImports": "always"
        }
    },
    "[java]": {
        "editor.defaultFormatter": "josevseb.google-java-format-for-vs-code"
    },
    "java.format.settings.google.style": "palantir",
    "js/ts.experimental.useTsgo": true,
    "black-formatter.args": ["--line-length", "79"],
    "isort.args": ["--profile", "black"],
    "files.associations": {
        "*.css": "tailwindcss",
        ".eslintrc": "jsonc"
    },
    "workbench.settings.applyToAllProfiles": [
        "editor.rulers",
        "editor.formatOnSave",
        "editor.formatOnPaste",
        "editor.defaultFormatter",
        "js/ts.preferences.quoteStyle",
        "prettier.printWidth",
        "prettier.semi",
        "prettier.singleQuote",
        "prettier.tabWidth",
        "js/ts.experimental.useTsgo",
        "black-formatter.args",
        "isort.args",
        "[typescript]",
        "[typescriptreact]",
        "[jsonc]",
        "[json]",
        "[python]"
    ]
}
```

# Форматирование всего проекта

За форматирование всего проекта отвечает расширение **Format Files**, методом вызова всех файлов репозитория и применения к ним настройки авто форматирование используемого и настроенного в среде разработки

##### Команда для форматирования всего проекта

```VScode
formatFiles.start.workspace
```

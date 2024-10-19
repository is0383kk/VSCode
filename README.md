# VSCode setting for myself
## settings.json
```json
{
  "workbench.settings.useSplitJSON": false, 
  "workbench.tree.indent": 24, 
  "workbench.layoutControl.enabled": true, 
  "workbench.activityBar.location": "top", 
  "workbench.editor.tabSizing": "shrink", 
  "workbench.iconTheme": "material-icon-theme", 

  "material-icon-theme.folders.color": "#f0e68c", 
  "material-icon-theme.files.color": "#a9a9a9", 

  "editor.fontFamily": "'UDEV Gothic 35NFLG'", 
  "editor.fontSize": 14,
  "editor.suggestSelection": "first", 
  "editor.renderLineHighlight": "all", 
  "editor.renderLineHighlightOnlyWhenFocus": true, 
  "editor.renderWhitespace": "boundary", 
  "editor.cursorBlinking": "phase",
  "editor.cursorSmoothCaretAnimation": "explicit", 
  "editor.formatOnSave": true,
  "editor.formatOnType": true, 
  "editor.renderControlCharacters": true, 
  "editor.dragAndDrop": false, 
  "editor.copyWithSyntaxHighlighting": false, 
  "editor.wordWrap": "on", 
  "editor.wordSeparators": "`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?　、。！？「」【】『』（）", 
  "editor.minimap.maxColumn": 100, 
  "editor.minimap.showSlider": "always", 
  "editor.minimap.size": "fit", 
  "editor.scrollBeyondLastLine": false, 
  "editor.insertSpaces": true, 
  "editor.tabSize": 2, 
  "editor.bracketPairColorization.enabled": true, 

  "explorer.incrementalNaming": "smart",

  "files.eol": "\n", 
  "files.insertFinalNewline": true, 
  "files.trimFinalNewlines": true,
  "files.trimTrailingWhitespace": true,

  "window.commandCenter": true,
  "window.zoomLevel": 0.3,

  "debug.inlineValues": "on", 
  "debug.internalConsoleOptions": "openOnSessionStart", 
  "debug.openDebug": "openOnSessionStart", 

  "search.showLineNumbers": true, 

  "terminal.integrated.copyOnSelection": true, 
  "terminal.integrated.scrollback": 10000, 

  "[python]": {
    "editor.defaultFormatter": "charliermarsh.ruff",
    "editor.codeActionsOnSave": {
      "source.fixAll.ruff": "always",
      "source.organizeImports.ruff": "always"
    },
    "editor.insertSpaces": true, 
    "editor.detectIndentation": true,
    "editor.tabSize": 4 
  },

  "json.schemaDownload.enable": true,
  "[json][jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.tabSize": 2,
    "editor.insertSpaces": true,
    "editor.formatOnSave": true,
    "files.insertFinalNewline": true,
    "editor.autoIndent": "advanced"
  },

  "yaml.format.enable": true, 
  "[yaml][dockercompose][github-actions-workflow]": {
    "editor.defaultFormatter": "redhat.vscode-yaml",
    "editor.tabSize": 2, 
    "editor.formatOnSave": true, 
    "editor.insertSpaces": true, 
    "files.insertFinalNewline": true, 
    "editor.autoIndent": "advanced", 
    "editor.quickSuggestions": {
      "other": true, 
      "comments": false, 
      "strings": true 
    }
  },

  "[toml]": {
    "editor.defaultFormatter": "tamasfe.even-better-toml", 
    "editor.insertSpaces": true, 
    "editor.formatOnSave": true, 
    "files.insertFinalNewline": true
  },
}
```
## Extensions
Install  
```powershell
$ code --install-extension
```
Show extensions list  
```Powershell
$ code --list-extensions
amazonwebservices.aws-toolkit-vscode
antfu.browse-lite
antfu.vite
charliermarsh.ruff
eamodio.gitlens
esbenp.prettier-vscode
github.vscode-github-actions
github.vscode-pull-request-github
gruntfuggly.todo-tree
hbenl.vscode-test-explorer
littlefoxteam.vscode-python-test-adapter
mhutchie.git-graph
ms-ceintl.vscode-language-pack-ja
ms-python.debugpy
ms-python.flake8
ms-python.mypy-type-checker
ms-python.python
ms-python.vscode-pylance
ms-vscode.live-server
ms-vscode.test-adapter-converter
njpwerner.autodocstring
oderwat.indent-rainbow
pkief.material-icon-theme
redhat.vscode-yaml
ryanluker.vscode-coverage-gutters
tamasfe.even-better-toml
uctakeoff.vscode-counter
vue.volar
```

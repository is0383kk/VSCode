# 個人用VSCode設定
# ■ 前提となる拡張機能  
- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [Ruff](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff)
- [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)
- [Even Better TOML](https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml)
- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

# ■ settings.json
```json
{
  /*
    必要な拡張機能
    ・Material Icon Theme：https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme
    ・Ruff：https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff
    ・YAML：https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml
    ・Even Better TOML：https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml
    ・Prettier - Code formatter：https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
    */

  /*
      Material Icon Themeに関連する設定
    */
  "workbench.iconTheme": "material-icon-theme", // アイコンテーマ
  "material-icon-theme.folders.color": "#f0e68c", // フォルダアイコンの色
  "material-icon-theme.files.color": "#a9a9a9", // ファイルアイコンの色

  /*
      workbench関連設定
    */
  "workbench.settings.useSplitJSON": false, // 設定画面からsetting.jsonを編集する際デフォルト設定とユーザ設定を同時に開く機能を無効化
  "workbench.tree.indent": 24, // ツリー（例: エクスプローラー）のインデント幅をピクセル単位で設定（デフォルトは10）
  "workbench.layoutControl.enabled": true, // 右上のレイアウトコントロールアイコンの表示切替
  "workbench.activityBar.location": "top", // アクティビティバーの位置（通常は左側）
  "workbench.editor.tabSizing": "shrink", // エディタ上部の開いているファイルのタブサイズ
  "workbench.editor.pinnedTabsOnSeparateRow": true, // ピン止めされたタブがピン止めされていないタブの上に表示
  "workbench.editor.wrapTabs": true, // タブが画面幅を超えたときに折り返す
  "workbench.list.smoothScrolling": true, // サイドバーのスクロールを滑らかにする
  "workbench.view.alwaysShowHeaderActions": true, // サイドバーのヘッダーアクションを常に表示
  "workbench.colorCustomizations": {
    "editorLineNumber.activeForeground": "#fffb00", // 編集中の行番号の色
    "editor.lineHighlightBackground": "#525252", // 編集中の行番号の強調表示色
    "editor.selectionBackground": "#0004ff" // 明るい青の背景
  },

  /*
      エディタ関連設定
    */
  "editor.fontFamily": "'UDEV Gothic 35NFLG'", // エディタで使用するフォント
  "editor.fontSize": 14, // エディタのフォントサイズ
  "editor.suggestSelection": "first", // サジェスト一覧の初期表示項目設定
  "editor.renderLineHighlight": "gutter", // エディタ内で現在行全体をハイライト表示
  "editor.renderLineHighlightOnlyWhenFocus": true, // エディタがフォーカスを持っている場合のみ行ハイライトを表示
  "editor.renderWhitespace": "boundary", // 空白文字表示設定（単語境界にのみ表示）
  "editor.cursorBlinking": "expand", // カーソルの点滅アニメーション（ゆっくりと点滅）
  "editor.cursorSmoothCaretAnimation": "explicit", // カーソルのスムースアニメーション（明示的モード）
  "editor.formatOnSave": true, // ファイル保存時に自動的にコードをフォーマット
  "editor.formatOnType": true, // コードを入力するたびに自動的にフォーマット
  "editor.renderControlCharacters": true, // 制御文字（タブや改行など）を表示
  "editor.dragAndDrop": false, // テキストのドラッグアンドドロップ
  "editor.copyWithSyntaxHighlighting": false, // コードをコピーするときにシンタックスハイライトをコピーしない
  "editor.wordWrap": "on", // エディタで長い行を折り返して表示
  "editor.wordSeparators": "`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?　、。！？「」【】『』（）", // 単語の区切り文字
  "editor.minimap.maxColumn": 100, // ミニマップの最大幅
  "editor.minimap.showSlider": "always", // ミニマップのスクロールバーを常に表示
  "editor.minimap.size": "fit", // ミニマップのサイズ
  "editor.smoothScrolling": true, // エディターのスクロールを滑らかにする
  "editor.scrollBeyondLastLine": false, // エディタの最後の行の後ろに余分なスペースをスクロールしない
  "editor.insertSpaces": true, // タブキーでスペースを挿入
  "editor.tabSize": 2, // タブの幅をスペース2つ分に設定
  "editor.bracketPairColorization.enabled": true, // カッコのペアを色分けして表示
  "editor.mouseWheelZoom": true, // Ctrl+マウスホイールでエディターをズーム
  "editor.wordSegmenterLocales": "ja", // Ctrl+矢印キーで日本語単語の先頭や末尾に移動できる
  "editor.wrappingIndent": "indent", // 折り返し行のインデントが元の行のインデント+1

  /*
      エクスプローラー関連設定
    */
  "explorer.incrementalNaming": "smart", // 新しいファイルやフォルダを作成する際に同名ファイルがある場合数字を加算して名前付け

  /*
      ファイル関連設定
    */
  "files.eol": "\n", // 改行文字をLF（\n）に設定
  "files.insertFinalNewline": true, // ファイルの最後に自動的に改行を追加
  "files.trimFinalNewlines": true, // ファイルの末尾の余分な改行を削除
  "files.trimTrailingWhitespace": true, // 行末の空白を自動的に削除
  "files.autoGuessEncoding": true, //ファイルのエンコーディングを自動で推測

  /*
      ウィンドウ関連設定
    */
  "window.commandCenter": true, // コマンドセンター（クイックアクセスをサポートする上部バー）
  "window.zoomLevel": 0.3, // ウィンドウのズームレベル

  /*
      デバッグ関連設定
    */
  "debug.inlineValues": "on", // デバッグ中にインラインで変数の値を表示
  "debug.internalConsoleOptions": "openOnSessionStart", // デバッグセッションが開始されたときに内部コンソールを自動的開く
  "debug.openDebug": "openOnSessionStart", // デバッグビューをセッション開始時に自動的に開く

  /*
      検索関連設定
    */
  "search.showLineNumbers": true, // 検索結果に行番号を表示

  /*
      ターミナル関連設定
    */
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.copyOnSelection": true, // ターミナルでテキストを選択すると自動的にコピー
  "terminal.integrated.scrollback": 10000, // ターミナルのスクロールバックバッファーの行数
  "terminal.integrated.enableVisualBell": true, // ターミナル名の横にベルマーク
  "terminal.integrated.mouseWheelZoom": true, // Ctrl+マウスホイールでエディターをズーム
  "terminal.integrated.smoothScrolling": true, // スクロールを滑らかにする

  /*
      ソース管理タブ設定
    */
  "scm.alwaysShowRepositories": true, // ソース管理タブでサイドバーにリポジトリを常に表示
  "scm.defaultViewMode": "tree", // デフォルトの変更ファイル一覧の表示をツリー表示
  "scm.diffDecorationsGutterWidth": 5, // 差分部分の緑色表示の幅の長さ
  "scm.inputFontFamily": "editor", // コミットメッセージをエディターと同じフォントに設定

  /*
      Python関連設定
    */
  "[python]": {
    "editor.defaultFormatter": "charliermarsh.ruff",
    "editor.codeActionsOnSave": {
      "source.fixAll.ruff": "always",
      "source.organizeImports.ruff": "always"
    },
    "editor.insertSpaces": true, // タブキーでスペースを挿入
    "editor.detectIndentation": true, // インデントを自動的に検出
    "editor.tabSize": 4 // タブの幅をスペース4つ分に設定
  },

  /*
      JSON関連設定
    */
  "json.schemaDownload.enable": true, // 設定しないとvscodeの設定ファイルでProblems loading referenceのエラーが出る時がある
  "[json][jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode", // JSON関連ファイルに対してprettier-vscodeのフォーマッターを使用
    "editor.tabSize": 2, // タブ幅をスペース
    "editor.insertSpaces": true, // タブキーでスペースを挿入
    "editor.detectIndentation": true, // インデントを自動的に検出
    "editor.formatOnSave": true, // ファイル保存時に自動的にコードをフォーマット
    "files.insertFinalNewline": true, // ファイルの最後に改行を自動的に挿入
    "editor.autoIndent": "advanced" // 高度なインデント機能を有効化
  },

  /*
      YAML関連設定
    */
  "yaml.format.enable": true, // YAMLファイルのフォーマットを有効化
  "[yaml][dockercompose][github-actions-workflow]": {
    "editor.defaultFormatter": "redhat.vscode-yaml", // YAML関連ファイルに対してRedHatのフォーマッターを使用
    "editor.tabSize": 2, // タブ幅をスペース
    "editor.formatOnSave": true, // 保存時に自動フォーマット
    "editor.insertSpaces": true, // タブキーでスペースを挿入
    "files.insertFinalNewline": true, // ファイルの最後に改行を自動的に挿入
    "editor.autoIndent": "advanced", // 高度なインデント機能を有効化
    "editor.quickSuggestions": {
      "other": true, // その他の項目に対してクイックサジェストを表示
      "comments": false, // コメント内でのクイックサジェストを無効化
      "strings": true // 文字列内でのクイックサジェストを有効化
    }
  },

  /*
      TOML関連設定
    */
  "[toml]": {
    "editor.defaultFormatter": "tamasfe.even-better-toml", // TOMLファイル用のEven Better TOMLフォーマッターをデフォルトに設定
    "editor.insertSpaces": true, // タブキーでスペースを挿入
    "editor.formatOnSave": true, // 保存時に自動でフォーマット
    "files.insertFinalNewline": true // ファイルの最後に改行を自動的に挿入
  }
}

```

# ■ その他拡張機能
## １．インストール済み拡張機能の確認
```Powershell
$ code --list-extensions
alefragnani.bookmarks
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
## ２．拡張機能のリストをテキストファイルにコピペ
```txt:extensions.txt
alefragnani.bookmarks
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

## ３．Powershell上で次のコマンドでインストール
```powershell
$ Get-Content extensions.txt | ForEach-Object { code --install-extension $_ }
```
※Linuxの場合
```bash
$ cat extensions.txt | xargs -n 1 code --install-extension
```

一個ずつインストールする場合
```powershell
$ code --install-extension 拡張機能名
```

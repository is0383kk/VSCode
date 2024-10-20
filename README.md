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
      外観設定
    */
  "workbench.colorTheme": "Default Dark Modern", // カラーテーマ
  "workbench.iconTheme": "material-icon-theme", // 【拡張機能】Material Icon Theme：https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme
  "material-icon-theme.folders.color": "#f0e68c", // フォルダアイコンの色
  "material-icon-theme.files.color": "#a9a9a9", // ファイルアイコンの色

  /*
      workbench設定
    */
  "workbench.settings.useSplitJSON": false, // 設定画面からsetting.jsonを編集する際デフォルト設定とユーザ設定を同時に開く機能を無効化
  "workbench.editor.enablePreview": true, // 未編集ファイルが勝手に閉じられるのを防止
  "workbench.editor.tabSizing": "shrink", // エディタ上部の開いているファイルのタブサイズ
  "workbench.editor.pinnedTabsOnSeparateRow": true, // ピン止めされたタブがピン止めされていないタブの上に表示
  "workbench.editor.wrapTabs": true, // タブが画面幅を超えたときに折り返す
  "workbench.tree.indent": 24, // ツリー（例: エクスプローラー）のインデント幅をピクセル単位で設定（デフォルトは10）
  "workbench.layoutControl.enabled": true, // 右上のレイアウトコントロールアイコンの表示切替
  "workbench.activityBar.location": "top", // アクティビティバーの位置（通常は左側）
  "workbench.sideBar.location": "left", // サイドバーを左に
  "workbench.list.smoothScrolling": true, // サイドバーのスクロールを滑らかにする
  "workbench.view.alwaysShowHeaderActions": true, // サイドバーのヘッダーアクションを常に表示

  /*
    各種色の設定
    */
  "workbench.colorCustomizations": {
    "editorLineNumber.activeForeground": "#fffb00", // 編集中の行番号の色
    "editor.lineHighlightBackground": "#525252", // 編集中の行の強調表示色
    "editor.selectionBackground": "#0004ff", // 選択範囲（ドラック操作やShift+矢印キーや全選択での選択）の色
    "editor.selectionHighlightBorder": "#fffb00", // ハイライト選択範囲の枠線
    "editorCursor.foreground": "#dddcc3c4", // カーソルの色
    "editor.wordHighlightBackground": "#3838386e", // カーソルがある単語や一致する部分の強調色
    "editorBracketMatch.border": "#fffb00" // カッコや括弧ペアの強調表示枠線
  },

  /*
      エディタ関連設定
    */
  "editor.fontFamily": "'UDEV Gothic 35NFLG'", // エディタで使用するフォント
  "editor.fontSize": 14, // エディタのフォントサイズ
  "editor.lineNumbers": "on", // 行番号の表示
  "editor.insertSpaces": true, // タブキーでスペースを挿入
  "editor.tabSize": 2, // タブの幅をスペース2つ分に設定
  "editor.guides.indentation": true, // インデントのガイドラインを表示
  "editor.autoIndent": "advanced", // 高度なインデント機能を有効化
  "editor.wrappingIndent": "indent", // 折り返し行のインデントが元の行のインデント+1
  "editor.wordSegmenterLocales": "ja", // 日本語の単語分割を有効化・Ctrl+矢印でカーソルを単語単位で移動
  "editor.wordWrap": "on", // エディタで長い行を折り返して表示
  "editor.wordSeparators": "`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?　、。！？「」【】『』（）", // 単語の区切り文字
  "editor.minimap.maxColumn": 100, // ミニマップの最大幅
  "editor.minimap.showSlider": "always", // ミニマップのスクロールバーを常に表示
  "editor.minimap.size": "fit", // ミニマップのサイズ
  "editor.renderLineHighlight": "gutter", // エディタ内で現在行全体をハイライト表示
  "editor.renderLineHighlightOnlyWhenFocus": true, // エディタがフォーカスを持っている場合のみ行ハイライトを表示
  "editor.renderWhitespace": "boundary", // 空白文字表示設定（単語境界にのみ表示）
  "editor.renderControlCharacters": true, // 制御文字（タブや改行など）を表示
  "editor.suggestSelection": "first", // サジェスト一覧の初期表示項目設定
  "editor.quickSuggestionsDelay": 0, // クイックサジェストの遅延をなくす
  "editor.autoClosingBrackets": "always", // 括弧を自動的に閉じる
  "editor.autoClosingQuotes": "always", // 引用符を自動的に閉じる
  "editor.autoSurround": "quotes", // 自動的に引用符で囲む
  "editor.formatOnSave": true, // ファイル保存時に自動的にコードをフォーマット
  "editor.formatOnType": true, // コードを入力するたびに自動的にフォーマット
  "editor.dragAndDrop": false, // テキストのドラッグアンドドロップ
  "editor.emptySelectionClipboard": false, // 誤って空の行をコピーできなくする
  "editor.copyWithSyntaxHighlighting": false, // コードをコピーするときにシンタックスハイライトをコピーしない
  "editor.smoothScrolling": true, // エディターのスクロールを滑らかにする
  "editor.scrollBeyondLastLine": false, // エディタの最後の行の後ろに余分なスペースをスクロールしない
  "editor.bracketPairColorization.enabled": true, // カッコのペアを色分けして表示
  "editor.mouseWheelZoom": true, // Ctrl+マウスホイールでエディターをズーム
  "editor.links": true, // ファイル内リンクをクリック可能に
  "editor.accessibilitySupport": "off", // 音をオフに
  "editor.largeFileOptimizations": true, // 大きなファイルの読み込みを最適化
  "editor.codeActionsOnSave": {
    "source.organizeImports": "always", // 未使用のインポートを消す
    "source.fixAll.eslint": "always" // ESLintの自動修正を有効化
  },
  "editor.cursorBlinking": "blink", // カーソルの点滅アニメーション
  "editor.cursorWidth": 3, // カーソル幅
  "editor.cursorSmoothCaretAnimation": "explicit", // カーソルのアニメーション

  /*
    パンくずリスト関連設定
    */
  "breadcrumbs.enabled": true, // パンくずリストの機能ON
  "breadcrumbs.filePath": "on", // ファイルパスを表示
  "breadcrumbs.icons": true, // ファイルアイコンを表示
  "breadcrumbs.showFunctions": true, // 関数名を表示

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
  "debug.toolBarLocation": "docked", // デバッグツールバーをデバッグウィンドウに埋め込む

  /*
      検索関連設定
    */
  "search.showLineNumbers": true, // 検索結果に行番号を表示

  /*
      ターミナル関連設定
    */
  "terminal.integrated.cursorBlinking": true, // ターミナルでカーソルを点滅
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
  "python.analysis.indexing": true, // Pythonのインデクシングを有効化（ファイル解析を高速化）
  "python.analysis.autoSearchPaths": true, // 自動でパスの検索を有効化
  "python.analysis.autoImportCompletions": true, // 自動インポート候補を表示
  "python.analysis.userFileIndexingLimit": 6000, // ユーザーがインデックスに登録できるファイルの上限
  "python.analysis.diagnosticMode": "openFilesOnly", // 開いているファイルのみの診断を実行
  "python.analysis.typeCheckingMode": "basic", // 基本的な型チェックを有効化
  "python.testing.pytestEnabled": true, // pytestをテストフレームワークとして有効化
  "python.testing.pytestArgs": ["--cov=.", "--cov-report", "xml"], // pytest実行時の引数設定
  "python.testing.autoTestDiscoverOnSaveEnabled": true, // 保存時にテストを自動的に再検出
  "coverage-gutters.showGutterCoverage": true, // コードカバレッジの結果をサイドバーのライン番号に表示
  "coverage-gutters.showLineCoverage": true, // 各行のカバレッジ結果を行番号に表示
  "coverage-gutters.showRulerCoverage": true, // ルーラー（エディタ上部のインジケーター）にカバレッジ情報を表示
  "[python]": {
    "editor.defaultFormatter": "charliermarsh.ruff", // Pythonファイルのデフォルトフォーマッタをruffに設定
    "editor.codeActionsOnSave": {
      "source.fixAll.ruff": "always",
      "source.organizeImports.ruff": "always"
    },
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
    "editor.detectIndentation": true, // インデントを自動的に検出
    "editor.formatOnSave": true // ファイル保存時に自動的にコードをフォーマット
  },

  /*
      YAML関連設定
    */
  "yaml.format.enable": true, // YAMLファイルのフォーマットを有効化
  "[yaml][dockercompose][github-actions-workflow]": {
    "editor.defaultFormatter": "redhat.vscode-yaml", // YAML関連ファイルに対してRedHatのフォーマッターを使用
    "editor.tabSize": 2, // タブ幅をスペース
    "editor.formatOnSave": true, // 保存時に自動フォーマット
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
    "editor.formatOnSave": true // 保存時に自動でフォーマット
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
＜extensions.txt＞
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

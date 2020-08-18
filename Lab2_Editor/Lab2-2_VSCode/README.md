# Visual Studio Code 基礎

## 1. 本コンテンツの目的とゴール
本コンテンツでは、Microsoftが提供するコードエディタ「Visual Studio Code」について學ことを目的とします。

基礎編では、はじめてエディタを利用される方を想定スキルとし、VS Codeの一般的によく使われている基本的な操作をベースに、VS Codeの基本操作や、Markdownによるファイル編集を例として操作ができるようになることをゴールとします。  
※VS Codeの応用操作などを含めたふべてを網羅するわけではありませんのでご了承ください。

## 2. VS Codeとは
Visual Studio Code (通称、VS Code)は、Microsoftがオープンソースとして提供しているコードエディタです。クロスプラットフォーム対応しており、Windows、macOS、Linux環境に対応しています。

* **VS Code 公式 Webサイト (英語)**  
https://code.visualstudio.com/

* **VS Code Marketplace (英語)**  
https://marketplace.visualstudio.com/

* **VS Code 公式 Twitterアカウント (英語)**  
https://twitter.com/code

## 3. VS Codeをはじめてみよう
### 3-1. VS Codeのインストール
VS Codeを利用するためには、自前のパソコン環境にインストールする必要があります。下記のVS Code公式サイトからインストールパッケージをダウンロードして、インストールを行ってください。

* **VS Code 公式 ダウンロードサイト**
https://code.visualstudio.com/Download

<img src="https://github.com/IBMDeveloperTokyo/DojoBasicLab/raw/master/Lab2_Editor/Lab2-2_VSCode/image/image01.png" width="500">

* 各OSごとのインストールに関する資料は下記の公式サイト(英語)で公開されています。
   * [Windows](https://code.visualstudio.com/docs/setup/windows)
   * [macOS](https://code.visualstudio.com/docs/setup/mac)
   * [Linux](https://code.visualstudio.com/docs/setup/linux)

### 3-2. VS Codeの日本語設定
VS Codeは、日本語のOS環境にインストールした場合でも、デフォルトでは英語設定になってします。そのため、「拡張機能」を使って日本語設定にする必要があります。
※インストールしたバージョンによって異なる場合があります。
1. VS Codeを起動する。
2. **[拡張機能]** アイコンをクリックする。
3. 検索ボックスで `Japanese` を入力し、Enterキーで検索する。
4. 検索結果から **[Japanese Language Pack for Visual Studio Code]** を選択する。
5. メイン画面に表示された拡張機能情報より **[Install]** をクリックしてインストールを行う。

## 4. 画面構成について理解しておこう
基本的に、VS Codeはデスクトップアプリケーションです。他の多くのソフトウェアと同様にユーザーインターフェースが用意され、各パーツの中でメニューやアイコンをクリックして操作を行うことができます。

### 4-1. 基本構成

<img src="https://code.visualstudio.com/assets/docs/getstarted/userinterface/hero.png" width="500">

A: Activity Bar (アクティビティバー)　　
B: Side Bar (サイドバー)　　
C: Editor Groups (エディタグループ)　　
D: Panel (パネル)　　
E: Status Bar (ステータスバー)
　　
* 参考文献: [VS Code Docs - User Interface](https://code.visualstudio.com/docs/getstarted/userinterface)

### 4-2. コマンドパレット
VS Codeでは **「コマンドパレット」** と呼ばれているコマンド実行するための機能が搭載されています。
1. コマンドパレットを呼び出す。
macOS: [表示]メニュー → [コマンドパレット]
Widnows: [表示]メニュー → [コマンドパレット]
2. 表示されたコマンドパレットのボックスに [PATH] を入力し、[シェルコマンド: PATH内に'code'コマンドをインストールします]を探して選択する。
3. パスを通すコマンドが実行される。

## 5. コマンドからVS Codeを起動してみる
1. ターミナル/コマンドプロンプトを起動する。
2. 作業領域に移動する。
3. `.code` と入力し、実行する。
4. VS Codeが起動すれば、コマンドからのVS Codeの起動は成功です。

## 6. 配色テーマ設定の変更
VS Codeは、**「配色テーマ」** を使用することで、ユーザーインターフェイスの色を変更して好みの作業環境を手に入れることができます。
1. VS Codeで **配色テーマ** の設定画面を表示する。  
**macOS**: [Code]メニュー → [基本設定] → [配色テーマ]  
**Windows** : [ファイル]メニュー→[ユーザー設定]→[配色テーマ] 
2. カーソルキーを使用して、テーマの色をプレビューする。
3. 好みのテーマのが見つかった場合は、Enterキーで適用する。
4. 好みのテーマが見つからない場合には **[その他の色のテーマをインストールする]** メニューを選択する。
5. [拡張機能: マーケットプレース]* 公開されているテーマに関する拡張機能が表示される。
6. 好みの拡張機能を選択し、[Install]ボタンでインストールする。

## 7. VS Codeの設定ファイルを見てみる
VS Codeの設定は、設定メニューもしくはJSONファイル(settings.json)で記述指定することができます。
1. VS Codeの画面左下の **[管理]** アイコン → **[設定]** を選択する。
2. 設定できる項目をチェックしてみる。例えば `File: Auto Save` をon に指定しておくと、編集しているファイルを自動的に保存できるようになる。(オプション)
3. 画面右上のファイルに矢印がついたアイコンをクリックする。
4. settings.jsonファイルが表示される。これが、VS Codeの設定ファイルと呼ばれているJSON形式のファイルです。設定したい内容によって、直接JSONを編集する必要があるため覚えておきましょう。

### 設定例
* ファイルの自動保存 **Files:Auto Save** - on/off
* 行番号の表示 **Editor: Line Numbers** - on/off
* フォントサイズの指定 **Editor: Font Size** - ピクセル単位で6以上の数値で指定
* 行の高さを指定 **Editor: Line Height** - フォントサイズに基づいて計算する場合は0、カスタマイズする場合は数値で指定
空白文字の表示 **Editor: Render Whitespace**
   * none 表示しない
   * boundary　単語間のスペースは表示しない
   * selection 選択した文字にのみ表示する
   * all すべてのスペースを表示する
* クリップボードに文字だけを貼り付ける **Editor: Copy With Syntax Hightlighting** - チェック外す

## 7. Markdownによるファイルを編集する
### 7-1. ファイル作成から始める
1. VS Codeを起動する。
2. ファイルを新規作成する。  
macOS: [ファイル]メニュー → [新規ファイル]  
Windows: [ファイル]メニュー → [新規ファイル]
3. 画面右下のステータスバーの `プレーンテキスト` を選択する。
4. `言語モードの選択` より `Markdown` を選択する。
5. ステータスバーの `プレーンテキスト` から `Markdown` に変更されたことを確認する。
### 7-2. Markdownのファイルを編集する
1. Markdown形式で何か入力してみる。Markdownを初めて書く方は下記のサンプルを見ながら、入力してください。

```
# IBM Developer Dojo
## 今日の学ぶこと
1. VS Codeの概要
```

2. ファイルを保存する。  
**macOS**: [ファイル]メニュー → [名前を付けて保存]  
**Windows**: [ファイル]メニュー → [名前を付けて保存]
3. VS Codeの画面右上の虫眼鏡がついたアイコンをクリックする。
4. Markdownのプレビューが表示される。
5. そのまま左側のエディタ画面で、編集を続ける。

```
2. VS Codeの設定 
3. VS CodeでMarkdownのファイル編集
```
6. リアルタイムに右側のプレビューに反映されることを確認する。

### 7.3. スニペット (Markdown)
ここでは、Markdownで議事録を作成するためのスニペットを作成してみます。

1. スニペット設定をメニューから呼び出す。
**macOS**: [Code]メニュー → [基本機能] → [ユーザースニペット]  
**Windows**: [ファイル]メニュー → [ユーザー設定] → [ユーザースニペット]
2. `Markdown` を選択する。
3. Markdown.jsonファイルが表示される。
4. すべてを下記の内容に置き換え、ファイルを保存する。
```
{
	"Print to console": {
		"prefix": "log",
		"body": [
			"console.log('$1');",
			"$2"
		],
		"description": "Log output to console"
	},

		"Meeting Minutes":{
			"prefix": "meeting",
				"body": [
				  "# 会議名",
				  "",
				  "## 日時・場所・出席者",
				  "",
				  "日時: $CURRENT_YEAR 年 $CURRENT_MONTH_NAME $CURRENT_DATE 日   ",
				  "場所: 会議室  ",
				  "出席者:  ",
				  "",
				  "## アジェンダ",
				  "",
				  "1. xxx",
				  "2. xxx",
				  "3. xxx",
				  "",
				  "## 議事内容",
				  "",
				  "1. xxx",
				  "2. xxx",
				  "3. xxx",
				  "",
				  "## 決定事項",
				  "",
				  "* [決定事項 1]  ",
				  "* [決定事項 2]  ",
				  "* [TODO]   (担当:   、期日:MM/DD)"
				],
			"description": "meeting munutes"
			}
}
```
5. 設定ファイル(Settings.json)に下記を追加し、ファイルを保存する。
```
"[markdown]": {
"editor.quickSuggestions": true
}
```
6. Markdownファイルに戻って、 `meeting` と入力する。
7. meetingのスニペットが表示され、それをクリックすると指定しておいたコード内容が自動的に呼び出される。あとはお好みで内容をアレンジしてみてください。

* 参考文献: [VS Code Docs - Snippets in Visual Studio Code](https://code.visualstudio.com/docs/editor/userdefinedsnippets)

### 7-5. 拡張機能 (Markdown) オプション
Markdownを編集する際に役立つ拡張機能が、VS Code Marketplaceで公開されています。自由に拡張機能を見つけて、インストールし操作を試してください。
1. VS Codeを起動する。
2. **[拡張機能]** アイコンをクリックする。
3. 検索ボックスで `Markdown` を入力し、Enterキーで検索する。
4. 例えば、検索結果から **[Markdown PDF]** を選択する。
5. メイン画面に表示された拡張機能情報より **[Install]** をクリックしてインストールを行う。
6. コマンドパレットで `markdown` と入力すると、PDFやWordなど異なる形式にファイル変換を行うためのメニューが表示される。
7. 例えば、`Markdown PDF: Export (PDF)` を選択すると、開いているMarkdownファイルがPDFファイル形式に変換されて保存される。
※PDFファイルを開いて確認するためには、お使いいただいているマシン環境にPDFファイルを開くことができるソフトウェアがインストールされている必要があります。

## 8. Visual Studio Live Shareを使ってペアプログラミング
Visual Studio Live Shareは、VS CodeもしくはVisual Studioを利用しているユーザー同士で、コードを共有しながら作業を進めることができます。この機能を利用するためには、双方の環境にVisual Studio Live Share拡張機能をインストールしてある必要があります。
### Visual Studio Live Shareのセットアップ
1. VS Codeを起動する。
2. **[拡張機能]** アイコンをクリックする。
3. 検索ボックスで `live share` を入力し、Enterキーで検索する。
4. 検索結果から **[Live Share]** もしくは **[Live Share Extension Pack]** を選択する。
5. メイン画面に表示された拡張機能情報より **[Install]** をクリックしてインストールを行う。

### Visual Studio Live Shareの利用方法
1. コード共有を行いたい側のマシン上で **[Live Share]** アイコンをクリックする。
2. 表示されたメニューよりMicrosoftアカウントもしくは、GitHubアカウントで画面に従ってサインインを行う。
<img src="https://github.com/IBMDeveloperTokyo/DojoBasicLab/raw/master/Lab2_Editor/Lab2-2_VSCode/image/image02.png" width="500">
3. 発行されたURLを、共有したい相手に共有する。
4. 共有された側は、URLにアクセスしてVisual Studio Live Shareを経由して、相手のコードを表示する。

**[Visual Studio Live Shareを利用する場合の注意点]**
一般的なコラボレーションツールと同様に、信頼できるユーザーのみと共有するようにしてください。
* 相手とURLを共有する場合には **権限** を気をつける。
   * 読み取り専用モードを希望する場合には必ず [Make read-only] を指定する
   <img src="https://github.com/IBMDeveloperTokyo/DojoBasicLab/raw/master/Lab2_Editor/Lab2-2_VSCode/image/image02.png" width="500">
   * ターミナルを共有する場合、共有した相手側からコマンド操作を実行することが可能な状態になることを理解しておく。
* 利用する際は、事前に相手とルールを決めておく。

# 9. まとめ
いかがでしたでしょうか。VS Codeは、コード編集するためのエディタとして軽量であり、拡張機能を追加することでさまざまな使いこなしができることをご理解いただけたと思います。今回は、基礎編のためごく一部の操作や機能の紹介になりますので、詳細が気になる方や、もっと他の機能についても触れてみたい方は、インターネットで公開されているVS Code関連記事や、書籍なども参考にしていただきながら、どんどん触ってみてください。

VS Codeは毎月バージョンが更新されるコードエディタのため、画面変更や操作手順が予告なしに変更される可能性があります。内容についてお気づきの点や、ご指摘がありました際は、こちらのGitHubより、Issueを上げてください。
# Dojo Basic: Lab1-2 IBM Cloud CLI

## 目的とゴール
### 目的
 - IBM Cloud CLI を通して、コマンド・ライン・インターフェースについて学びます。

### ゴール
 - クラウド開発でよく利用するコマンドが使えるようになる

### このLabの実施前提
 - Lab1-1で実施したコマンド実行環境、IBM Cloud　ライトアカウント
 
### このLabで体験できること
 - ローカル環境（各自のPC）にIBM Cloud CLIをインストールする
 - ローカル環境から、IBM Cloudにアプリケーションを作成する
 - IBM Cloud Shellを使用して、クラウド環境のCLIを操作する

 

# 事前準備_IBM Cloud CLIのインストール

Macの場合は[こちら](https://github.com/IBMDeveloperTokyo/DojoBasicLab/blob/master/Lab1_ShellCommand/Lab1-2_IBMCloudCLI/cli_install_mac.md)を参照ください。　

Windowsの場合は[こちら](https://github.com/IBMDeveloperTokyo/DojoBasicLab/tree/master/Lab1_ShellCommand/Lab1-2_IBMCloudCLI/cli_install_windows.md)を参照ください。　

[参考：インストールドキュメント](https://cloud.ibm.com/docs/cli?topic=cli-install-ibmcloud-cli&locale=ja)


### IBM CF インストール
```
ibmcloud cf install
```
### Git のインストール

Macの場合は[こちら](https://github.com/IBMDeveloperTokyo/DojoBasicLab/blob/master/Lab1_ShellCommand/Lab1-2_IBMCloudCLI/git_install_mac.md)を参照ください。　

Windowsの場合は[こちら](https://github.com/IBMDeveloperTokyo/DojoBasicLab/tree/master/Lab1_ShellCommand/Lab1-2_IBMCloudCLI/git_install_windows.md)を参照ください。　

# 1. IBM Cloud CLIとは
 - **IBM Cloud CLI** (Command Line Interface/コマンドラインインターフェース)はIBM IBM Cloudの**リソースを作成、管理するための統合ツール**です。
 - IBM Cloud上で、**アプリケーションの作成や削除、ユーザー管理、使用状況の確認**などが実行できます。
 - Docker, Kubernetes, Helm, Object Strage など**さまざまなプラグインを追加導入**することができます。
 - 操作に慣れるとGUIよりすばやく処理を行うことが可能です。
 - Mac, Windows 10 Pro, Linux(cURLも必要)にインストールできます。

# 2.IBM Cloud にログイン
 次のコマンドでibm cloudにログインしてください。
```
 ibmcloud login -r us-south
```
*参考　IBM Cloudのロケーション　https://cloud.ibm.com/docs/containers?topic=containers-regions-and-zones
# 3.Cloud Foundryにアプリをデプロイ
　次のコマンドで実行環境Cloud Foundryをターゲットにします。
```
 ibmcloud target --cf
```
 gitでソースコードを自分のPCにクローンしましょう。(gitについてはGitの会で詳しく紹介します）

```
 git clone https://github.com/IBM-Cloud/node-helloworld.git
 cd node-helloworld/
```
現在他に動いているアプリがないか確認
```
 ibmcloud app list
```
あれば止める
```
 ibmcloud app stop アプリ名
```
IBM cloudのCloud foundryにソースコードをアップします。
```
 ibmcloud cf push
```
アプリのURLを確認：アプリ名の右の方にURLが出てきます。
```
 ibmcloud app list
```
ブラウザーでそのURLにアクセスして動作確認

![hello1](images/hello1.png)
名前をいれてEnter
![hello2](images/hello2.png)
結果表示
![hello3](images/hello3.png)

curl コマンドでも確認できます。
```
 curl アプリURL
```

その他のコマンド例
https://cloud.ibm.com/docs/cli?topic=cli-ibmcloud_commands_apps&locale=ja

# 4. IBM Cloud Shellを操作する
IBM Cloud Shell はコンソールから即時にアクセス可能で、その他のインストールは不要です。


## 4.1.IBM Cloud Shell でのセッションの開始
### 特徴
IBM® Cloud Shell には、コマンドを実行できる個人ワークスペースとセッションが含まれています。 
最大 5 つの並行セッションを開くことができます。

IBM Cloud Shell を開くには、IBM Cloud コンソールから IBM Cloud Shell アイコン をクリックします。 
Cloud Shell セッションは、コマンド、スクリプト、その他ツールが実行できます。

### ディレクトリ構成
セッションを開く際には、Cloud Shell ワークスペースのホーム・ディレクトリー /home/<user-name> から操作を開始します。 
ホーム・ディレクトリー内のデータは保持されません。ファイルは削除されます。

### 保存
セッションは、1 時間使用されないと自動的に閉じられます。 
最後のセッションを閉じた後さらに 1 時間使用していない場合、ワークスペース内のファイルとデータはすべて消去されます。
保持が必要なファイルはダウンロードが必要です。

### 利用時間の制限
Cloud Shell は、リージョンごとに 1 週間に最長 30 時間まで使用できます。
使用時間を最小限に抑えるために、使い終わったセッションは閉じるようにしてください。
同時セッションは追加の使用時間としてカウントされません。

30時間に達する5分前にアラートが上がります。この時間を使用して、ダウンロードなど必要なタスクを完了してください。
使用量はCloud Shell メニュー・バーで、メニュー・アイコン その他アイコン をクリックし、「使用割り当て量 (Usage quota)」で表示できます。
30時間使い切った後は、一度の接続が5分までに制限されます。（翌週にはリセットされます。

### 利用可能な容量
Cloud Shellで使用可能な一時ストレージの容量は500 MBです。
容量の限度に達すると、Cloud Shell に対する接続が失われるという既知の問題があります。 
この問題が発生した場合、接続を修正するには Cloud Shellの再起動が必要でファイルは削除されます。
この問題を回避するために、Cloud Shellには大きなファイルをアップロードしないようにします。
かつ、rm などのコマンドを使用して未使用ファイルを削除してください。

### 最後に
IBM Cloud Shell は、IBM Cloud の管理と開発という目的を想定しています。 
長時間実行または計算主体のスクリプトやプログラムのサポート、あるいは機密データの処理は想定していません。 




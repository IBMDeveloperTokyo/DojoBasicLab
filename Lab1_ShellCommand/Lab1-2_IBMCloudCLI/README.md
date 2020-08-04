# Dojo Basic: Lab1-1 コマンドの基礎

## 目的とゴール
### 目的
 - IBM Cloud CLI を通して、Command Line Interfaceについて学びます。

### ゴール
 - クラウド開発によく利用するコマンドが使えるようになる

### このLabの実施前提
 - Lab1-1で実施したコマンド実行環境、IBM Cloud　ライトアカウント



# IBM cloud CLIのインストール

[インストールはこちらから](https://cloud.ibm.com/docs/cli?topic=cli-install-ibmcloud-cli&locale=ja)

# IBM CF インストール
```
ibmcloud cf install
```
# Git のインストール

Macの場合は[こちら](https://github.com/IBMDeveloperTokyo/DojoBasicLab/blob/master/Lab1_ShellCommand/Lab1-2_IBMCloudCLI/git_install_mac.md)を参照ください。　

Windowsの場合はこちらを参照ください。　

# IBM Cloud にログイン
 次のコマンドでibm cloudにログインしてください。
```
 ibmcloud login -r us-south
```
*参考　IBM Cloudのロケーション　https://cloud.ibm.com/docs/containers?topic=containers-regions-and-zones
# Cloud Foundryにアプリをデプロイ
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

 

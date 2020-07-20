# IBM cloud CLIのインストール

[インストールはこちらから](https://cloud.ibm.com/docs/cli?topic=cli-install-ibmcloud-cli&locale=ja)

# IBM Cloud にログイン
 次のコマンドでibm cloudにログインしてください。
```
 ibmcloud login -r us-south
```
*参考　IBM Cloudのロケーション　https://cloud.ibm.com/docs/containers?topic=containers-regions-and-zones
# Cloud Foundryにソフトをデプロイ
　次のコマンドで実行環境Cloud Foundryをターゲットにします。
```
 ibmcloud target --cf
```
 gitでソースコードを自分のPCにクローンしましょう。
```
 git clone https://*************
```
現在他に動いているアプ氏がないか確認
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
その他のコマンド例
https://cloud.ibm.com/docs/cli?topic=cli-ibmcloud_commands_apps&locale=ja

 

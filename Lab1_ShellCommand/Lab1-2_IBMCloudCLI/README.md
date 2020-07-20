# IBM cloud CLIのインストール

[インストールはこちらから](https://cloud.ibm.com/docs/cli?topic=cli-install-ibmcloud-cli&locale=ja)

# IBM Cloud にログイン
 次のコマンドでibm cloudにログインしてください。
```
 ibmcloud login -r us-south
```

# Cloud Foundryにソフトをデプロイ
　次のコマンドで実行環境Cloud Foundryをターゲットにします。
```
 ibmcloud target --cf
```
 gitでソースコードを自分のPCにクローンしましょう。
```
 git clone https://*************
```
IBM cloudのCloud foundryにソースコードをアップします。
```
 ibmcloud cf push
```

 

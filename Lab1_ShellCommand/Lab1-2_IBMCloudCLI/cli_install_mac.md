# MacにIBM Cloud CLIをインストール

ターミナルを起動して 
以下のコマンドを端末にコピー・アンド・ペーストして実行します。 
(参考　https://cloud.ibm.com/docs/cli?topic=cli-install-ibmcloud-cli&locale=ja
```
curl -fsSL https://clis.cloud.ibm.com/install/osx | sh
```
実行例
```
$ curl -fsSL https://clis.cloud.ibm.com/install/osx | sh
Current platform is macOS. Downloading corresponding IBM Cloud CLI...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   109  100   109    0     0     67      0  0:00:01  0:00:01 --:--:--    67
100 16.4M  100 16.4M    0     0   690k      0  0:00:24  0:00:24 --:--:--  583k
Download complete. Executing installer...
installer: Package name is IBM Cloud Command Line Interface
installer: Upgrading at base path /
installer: The upgrade was successful.
Install complete.

```
インストール確認
```
$ ibmcloud -v
```
実行例
```
$ ibmcloud -v
ibmcloud version 1.1.0+cc908fe-2020-04-29T09:33:25+00:00
```

アンインストールはこちらのコマンドを使ってください。
```
/usr/local/ibmcloud/uninstall
```

# Macにgitをインストール

手順
1. Homebrewのインストール
2. Hombrewを使ってGitをインストール

## 1. Homebrewのインストール
　https://brew.sh/index_ja からHomebrewをインストールしてください
  (参考：　https://qiita.com/zaburo/items/29fe23c1ceb6056109fd）

インストールの確認
```
$ brew -v
```
実行例  
```
$ brew -v
Homebrew 2.4.9
Homebrew/homebrew-core (git revision 4dd70; last commit 2020-08-04)
Homebrew/homebrew-cask (git revision eab76; last commit 2020-08-04)
```

## 2. Hombrewを使ってGitをインストール
次のコマンドでgitをインストールしてください。
```
$ brew install git
```
実行例  
```
$ brew install git
Updating Homebrew...
==> Auto-updated Homebrew!
Updated 1 tap (homebrew/core).
==> Updated Formulae
Updated 4 formulae.
..................
```

インストールの確認
```
$ git --version
```
実行例  
```
$ git --version
git version 2.28.0
```

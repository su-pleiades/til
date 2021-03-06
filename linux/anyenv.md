# 前提条件 
anyenvがインストール済みであること


## anyenvコマンド
複数言語のパッケージを管理するツール
```
$ anyenv install --list
  Renv
  crenv
  denv
  erlenv
  exenv
  goenv
  hsenv
  jenv
  luaenv
  nodenv
  phpenv
  plenv
  pyenv
  rbenv
  sbtenv
  scalaenv
  swiftenv
  tfenv
```
インストール済みのパッケージ管理ツールとそのバージョン
```
$ anyenv versions
nodenv:
  12.16.1
  13.10.1
pyenv:
  system
* 3.8.2 
```
# 今回は言語をnode.jsを使用する例にて説明
## nodenvコマンド
anyenvで管理されているnodenvを使用
```
$ nodenv versions
  12.16.1
  13.10.1
```
インストール可能なバージョンを確認
```
$ nodenv install --list
0.1.14
0.1.15
0.1.16
0.1.17
...
iojs-3.3.1
nightly
node-dev
rc
v8-canary
```
特定のバージョンの最新版を確認
```
// var.12の最新版
$ nodenv install --list | grep -v [a-zA-Z] | grep ^12 | tail -1
12.16.1
```
```
$ nodenv install 12.16.1
```

## プロジェクト（ディレクトリ）ごとに使用するバージョンを変える
```
$ nodenv local 10.19.0
$ nodenv version
10.19.0 
```

## npmコマンド
### npmでインストール済みのパッケージ一覧（直下）
```
$ npm ls --depth=0
```
### npmのパッケージ目録(packeage.json)を作成
```
$ npm init
```

## nodenv のインストール時に default-packages file not found と表示される問題
```
% nodenv install 10.19.0
nodenv: /Users/myname/.anyenv/envs/nodenv/versions/10.19.0 already exists
continue with installation? (y/N) y
Downloading node-v10.19.0-darwin-x64.tar.gz...
-> https://nodejs.org/dist/v10.19.0/node-v10.19.0-darwin-x64.tar.gz
Installing node-v10.19.0-darwin-x64...
Installed node-v10.19.0-darwin-x64 to /Users/myname/.anyenv/envs/nodenv/versions/10.19.0

nodenv: default-packages file not found
```

## 解決策
- default-packages file を作成する
```
% touch $(nodenv root)/default-packages
```

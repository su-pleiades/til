vimの操作で指定した２つのファイルをカラーで表示する機能

$ vimdiff {file1} {file2}

## viで分割、カーソル移動
```
: splitで水平分割。
: vsplitで垂直分割。
: onlyで自分だけのウィンドウにする。
: hideで自分のウィンドウを閉じる。
```

## vimdiffコマンド

vimdiffコマンドは左右にdiffを表示させるコマンド。
```
以下ショートカットキー。
当然ながらvimdiffに限らずviで分割時も使えます。
ctrl+w h 左のウィンドウをアクティブにする
ctrl+w j 下のウィンドウをアクティブにする
ctrl+w k 上のウィンドウをアクティブにする
ctrl+w l 右のウィンドウをアクティブにする
ctrl+w w アクティブウィンドウを順番に切り替え

ctrl+w H アクティブ画面を左へ、上下分割の場合左右分割に切り替わる
ctrl+w J アクティブ画面を下へ、左右分割の場合上下分割に切り替わる
ctrl+w K アクティブ画面を上へ、左右分割の場合上下分割に切り替わる
ctrl+w L アクティブ画面を右へ、上下分割の場合左右分割に切り替わる

ctrl+w < 分割された仕切りを一文字分左へ
ctrl+w > 分割された仕切りを一文字分右へ
ctrl+w + 分割された仕切りを一文字分下へ
ctrl+w - 分割された仕切りを一文字分上へ
ctrl+w = 分割された仕切りを中央へ

do vimdiff時相手のウィンドウの差分を受け入れる(obtain)
dp vimdiff時自分のウィンドウの差分を相手に渡す(push)

以下二つは同時押しじゃないので注意。
[ c vimdiff時前の変更箇所へ
] c vimdiff時次の変更箇所へ
```

# １ヶ月前を出力
```
date '+%Y%m'
# 202010

date -v-1m '+%Y%m%d'
# 20200903
```
https://mazeltov7.hateblo.jp/entry/2016/10/10/140222

## ０埋めなどのオプション
```
: man date
デフォルトでは0で日付の空白部分が埋められます。 次のオプションフラグを '%' の後に続けることができます:

-
(ハイフン) フィールドの空白を埋めない
_
(アンダースコア) フィールドの空白をスペースで埋める
0
(ゼロ) フィールドの空白を0で埋める
^
可能な場合は大文字を使用する
#
可能な場合は小文字を使用する
```
https://qiita.com/71713/items/63dc09faa9a5e1742c8f

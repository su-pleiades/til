ディレクトリ 配下全てのディレクトリ ・ファイルの権限変更
```
chmod -R 
```
ディレクトリ を775、ファイルを644などに一髪で変換したい場合
```
find {対象パス} -type d -exec chmod 755 {} +
find {対象パス} -type f -exec chmod 644 {} +
```

よく使うなら、
```
#.bashrc

function chmod-r(){
  find $1 -type $2 -exec chmod $3 {} +
}
```

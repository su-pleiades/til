# ln 

ln [オプション] {リンク元} {リンク先(別名)}
- リンク元とリンク先が別ディレクトリの場合は、リンク元のファイル名をフルパスで指定し、リンク先にフルパスで配置したいディレクトリを指定する
```sh
# 例
ln -n /home/user/testfile /tmp/
```


## オプション

-s　：シンボリックリンクを作成　

-b　：リンク先に同じ名前のリンクがあった場合は、末尾に「~」を加えて上書きしないようにする


## エラー

pythonファイルをリンクして、python3で実行した際に発生

シンボリックを別の階層（ディレクトリ）にファイル名だけ指定して作成したのが原因
```
python3: can't open file '{file name}': [Errno 40] Too many levels of symbolic links

# 解決策：リンク元のパスを絶対パスで指定する
```

## シンボリックリンク削除
```sh
unlink {path}
```

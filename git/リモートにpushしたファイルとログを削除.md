# 作業フロー
1. リモートにpush後、間違ったファイルをpushしてしまったことに気づく
2. ファイルの削除とログも一緒に削除したい
3. コミットのログを対象ファイルpush以前に戻す
4. リモートから対象ファイルを管理対象から外す
5. 強制的にpush

## 手順

```
# 過去のコミットを1行にまとめて、ハッシュ値等の値を出力
git log --oneline

# --softのオプションを付与し、リモートのログを対象まで戻す
git reset --soft {コミットのハッシュ値}

＃ -rのオプションでディレクトリを監視対象から外すこともできる
git rm --cache {ファイル名}

# 通常のgit pushでエラーが出た場合-fオプションを付与して再度実行
git push -f origin master
```

## 確認
- githubのコンソール上から対象ファイルがないことを確認
- historyから対象コミットログがないことを確認
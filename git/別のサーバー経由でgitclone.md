# イメージ
[GitLab] 
    |
[ServerA] :GitLabからclone可能
    |　<--ここの経路を作成して、cloneできるようにする
[ServerB] :GitLabからcloneできないが、ServerA経由でcloneしたいを


# 経路の確立
- [~/.ssh/config]ファイルに記載し、簡単にssh-フォワーディングできる様にする
```
Host ServerA
  Hostname  {ServerAのIP}
  IdentityFile ~/.ssh/{ServerAの秘密鍵}
  User {ServerAで接続するユーザー名}
  DynamicForward 10443
```

- １つ目のターミナルで接続を維持（ターミナルでssh接続切れば経路も簡単に切ることができる）
```
$ ssh ServerA
```

- ２つ目のターミナルでcloneなどの操作を行う
```
git clone --config http.proxy=socks5://localhost:10443 {GitLabでcloneしたいリポジトリを指定}
``` 

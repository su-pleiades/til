- 履歴を見ることができる
```md
kubectl rollout history deployment/hello
# deployment.apps/hello
# REVISION  CHANGE-CAUSE
# 1         <none>
# 2         <none>
```

- 元のバージョンに戻る
```
kubectl rollout undo deployment/hello
# deployment.apps/hello rolled back
```

if文の条件式に!と{変数}のみを加えた場合の挙動
変数に値が入っているかを判定して、! によって結果が逆転する(true -> false, false -> true)
```
var arr = "a"
if(!arr){ // false
    true
} else {
    false
}
```
変数に文字を入れなかった場合
```
var arr = ""
if(!arr){ // true
    true
} else {
    false
}
```

## break

 break文は繰り返しを中断してループから抜け出す
 
## continue

continue文は繰り返しを中断してループの先頭に戻る

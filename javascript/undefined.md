変数や配列の初期値はundefined　を返す

```
var str;
var str = "変数の中身は" + str + "です" 
// 変数の中身はundefinedです

var str2 = ""
var str2 = "変数の中身は" + str2 + "です" 
// 変数の中身はです

var　arr = [];
var arr =  "配列の中身は" + arr + "です" 
// 変数の中身はundefinedです

```

# !とundefinedでtrue

注意：falseや0もundefined扱いになってしまう
```
if (!a) {
  alert("aはfalseか0かundefinedかnull");
}
```

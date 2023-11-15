# プリミティブ型
- 文字列 string
- 数値
- 長整数
- 論理値
- undefined
- シンボル
- null

# string
変数名の前にstringをつける。その後にstringなら代入できる。
```
let name: string = "taro";
name = "jiro";
```
特定の文字列だけを許容する型も定義できる。型として"taro"を定義した場合は、"jiro"などを代入するとエラーが発生する。
```
let name: "taro" = "taro";
name = "jiro"; // Type '"jiro"' is not assignable to type '"taro"'.
```
taroもしくはjiroという風に複数の文字列を許容する場合はユニオン型を使う。|(パイプ)で挟む。
```
let name: "taro" | "jiro" = "taro";
name = "jiro";
```
# number
数値を扱うときは変数名の後にnumber
```
let age: number = 18;
```

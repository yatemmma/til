# データ型と変数

## データ型

* 値型 (value type)
* 参照型 (reference type)

### 基本的なデータ型

* 整数型 Int、UInt (基本的にIntの利用推奨)
* 実数型 Float、Double
* 論理型 Bool
* 文字型 Character (Unicodeの1文字を表す)
* 文字型 UnicodeScalar (Unicodeの文字コードを表す)
* 文字列 String (値型)

## 変数と定数

* 変数 (variable)
* 定数 (constant)

### 変数の定義

```
var age: Int = 18
var num = 100 // 初期値から型推論
```

### 定数の定義

```
let age: Int = 18
```

### 型変換

Swiftでは暗黙の型変換は行われず、型を揃えなければ代入や計算はできない。

```
let age: Int = 18
var num = 10.0
num = Double(age) * num
```

異なる型のリテラルが代入できるのは、コンストラクタが定義されているため。

```
var size: Float = 8
let s = size + 10
```

## 文字列

```
let name = "わたし"
var text = "hello"
text += "world"
```

"\u{xxx}"で文字コード指定

```
let specialKeys = "\u{2318}" // ⌘
```

文字列埋め込み(string interpolation)

```
let n = 8
let text = "\(n) * 2 = \(n * 2)"
```

## print関数

```
let n = 8
let text = "hoge"
print(n, text)
print(n, text, separator: ",")
print(n, text, terminator: ";")
```

## 配列

同じ型の要素のみ可

```
var a = [2, 3, 10, 8]
var b: [Int] = [2, 3, 10, 8]
a += [9, 0]
print(a, b.count)
```

空配列

```
var s = [String]()
var t: [String] = []
```

配列は値型のため、代入は値コピー

```
var a = [2,4,6]
var b = a
b[1] = 10
print(a) // [2,4,6]
print(b) // [2,10,6]
```

## 別名

```
typealias HogeInt = Int
```

## ジェネリクス

```
var a: [String] = []
var b: Array<String> = Array<String>()
```

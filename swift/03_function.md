# 関数

## 関数定義

```
func hoge1() {
  // xxx
}

func hoge2() -> Void {
  // xxx
}

func hoge3() -> () {
  // xxx
}
```

```
func count(n: Int) -> Int {
  return n
}
```

## 外部引数名 (キーワード引数名)

```
func area(h:Double, w:Double) -> Double {
  return h * w
}
area(1, w:2)
```

h,wを内部引数名(ローカル引数名)と呼ぶ

```
func area(height h:Double, width w:Double) -> Double {
  return h * w
}
area(height:1, width:2)
```

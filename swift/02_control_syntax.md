# 制御構文

## if文

```
if x > 0 {
  a = 1
} else if x > 100 {
  a = 10
} else {
  a = 100
}
```

```
if x > 0 { print(x) }
```

## while文

```
var i = -10
while i < 0 {
  if i == -1 {
    continue
  }
  print(i)
  i++
}
```

```
while true {
  break
}
```

## repeat-while文

元do-while文

```
var i = 1
repeat {
  print(i)
  i++
} while i < 0
```

## for文

```
for var i = 0; i < 10; i++ {
  print(i)
}
```

```
for var i = 0, j = 0; i < 10; i++, j += 10 {
    print(i)
    print(j)
}
```

```
var i = 0
for ;; {
    if i == 10 {
        break
    }
    print(i)
    i++
}
```

## for-in文

範囲演算子

```
1..<10
1...10
```

```
for x in 1...3 {
  print(x)
}
```

```
for x in [2,4,6] where x > 5 {
  print(x)
}
```

## switch文

```
let x = 0
switch x {
case 0,100:
    print("hoge")
    fallthrough
case 1..<50:
    print("piyo1")
case 50..<100: print("piyo2")
default:
    print("default")
}
```

## do文

```
var x = 1
var y = 2
do {
  var x = 10
  y = 20
}
print(x, y)
```

## ラベル

```
var x = 1
var y = 1
if1: if x > 0 {
    if2: if y > 0 {
        x++
        while1: while x < 10 {
            x++
            while2: while y < 10 {
                print(x, y)
                continue while1
            }
            break if1
        }
    } else {
        
    }
} else {
    
}
```

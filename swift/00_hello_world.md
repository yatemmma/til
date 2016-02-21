# 実行方法

## Playground

Xcodeから実行

## コマンドライン

```
$ swift
Welcome to Apple Swift version 2.1.1 (swiftlang-700.1.101.15 clang-700.1.81). Type :help for assistance.
  1> print("hello, world")
hello, world
```

Ctrl+D で終了

## コンパイル

```
$ echo 'print("hello, world")' > hello.swift 
$ swiftc hello.swift 
$ ./hello 
hello, world
```

複数ファイル

```
$ swiftc -o hello Module1.swift main.swift
```

## ソースコードを直接実行

```
$ echo 'print("hello, world")' > hello.swift 
$ swift hello.swift 
hello, world
```

```
$ echo '#!/usr/bin/swift' > hello
$ echo 'print("hello, world")' >> hello
$ chmod u+x hello
$ ./hello
hello, world
```

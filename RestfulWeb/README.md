# RESTful Web サービスの構築
 
http://localhost:8080/greeting

spring.pleiades.ioの最もシンプルなサンプル。

# 動作

http://localhost:8080/greeting

でアクセスすると

```
{
"id": 1,
"context": "Hello, World"
}
```

http://localhost:8080/greeting?name=Masa

でアクセスすると

```
{
"id": 2,
"context": "Hello, Masa"
}
```

# このサンプルで学んだこと

- パラメータにより出力文言の出し分けを行う実装がすごく簡単
- Getリクエストに対するJson返却がわずか2クラス追加するだけで実現できるので、Mockサービスを作る場合の選択肢の1つに加えられそう

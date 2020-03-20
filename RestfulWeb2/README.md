# RESTful Web サービスの使用

https://gturnquist-quoters.cfapps.io/api/random
の URL を呼び出すとランダムな文字列を含む Json が返却される。

例)

```
{
    "type": "success",
    "value": {
        "id": 3,
        "quote": "Spring has come quite a ways in addressing developer enjoyment and ease of use since the last time I built an application using it."
    }
}
```

今回はこの取得した Json をコンソールに出力するサンプルを作成

まずはじめに、この Json に対する

- 親クラスとして Quote クラス
- Value プロパティを格納する Value クラス

を作成する。

@JsonIgnoreProperties 　は、Json には存在するが、Jackson(※1)には存在しないプロパティを無視するもの。

今回のサンプルでは、そもそも Json の Property はすべて Jackson として定義しているので

```java
@JsonIgnoreProperties(ignoreUnknown = true)
```

を削っても変化しない

※1 Jackson は java のライブラリで、JSON オブジェクトを Java オブジェクトにマップしたりその逆を行うことができるもの

# 学び

- @JsonIgnoreProperties を使えば、Json には含まれているけど不要なプロパティを無視できる
- 外部サービスを呼び出して加工するとかも、簡単に実現できる

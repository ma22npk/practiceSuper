# practiceSuper
【Java】super について学習したことのアウトプット
# super
Java の 「 **super** 」について学んだ内容のアウトプットです。

## super とは
「super」は、「今より一つ内側の[インスタンス]部分」を表す予約語です。

これを利用すれば、**親インスタンス部分 の[メソッド]や[フィールド]に、小[インスタンス]からアクセスすることが出来ます。**

## super の記述の仕方
コンストラクタをオーバーライドする際は1行目に「super()」と記述する必要があります。


親インスタンス部分の[フィールド]を利用する時

```
super.フィールド名
```

親インスタンス部分の[メソッド]を呼び出す時

```
super.フィールド名([引数])
```

## superをつけないと？

例えば、親クラスに「attack()」 という[メソッド]があり、子[インスタンス]からアクセスしようとする場合を例でいうと、結論、、


super をつけないと**「外側で attack() を呼び続ける無限ループ」になってしまいます。**



super をつけないということは**`this.attack`**と同じ意味になってしまう。

[this]は「自分自身の[インスタンス]という意味」で、より正確には、「[インスタンス]の最も外側部分」を言う意味であるため上記の通り、[メソッド]の無い部分をずっとつづけることになる、ということになります。

## 「親の親」インスタンス部分へのアクセスは出来ない
下記のような継承関係の３つの[クラス]を例えにします。

- A[クラス] = 親の親
- B[クラス] = 親
- C[クラス] = 自分

C[クラス]から生成された[インスタンス]は3種構造になり、この時一番外側に相当するC[インスタンス]について考えます。

C[クラス]の[メソッド]は、一番外側の[インスタンス]部分（自分自身）には **[this], そして親[インスタンス]部分へは super でアクセスが出来ます。
しかし、残念ながら親の親に当たるA[クラス]の[インスタンス]にはアクセスする手段が準備されていないため、C →　A にはアクセスが出来ないということです。


[インスタンス]:https://qiita.com/takahirocook/items/ec01cdcbb440cf0d1cc4
[インスタンス化]:https://qiita.com/takahirocook/items/ec01cdcbb440cf0d1cc4
[アクセス修飾子]:https://qiita.com/takahirocook/items/e51b0b9d37d95ad587fe
[フィールド]:https://qiita.com/takahirocook/items/28df75a133049a74ece1
[フィールド変数]:https://qiita.com/takahirocook/items/28df75a133049a74ece1
[new演算子]:https://qiita.com/takahirocook/items/00f9f97592bf50831d39
[カプセル化]:https://qiita.com/takahirocook/items/e469a7c0539a0012868e
[クラス]:https://qiita.com/takahirocook/items/50cbbdca8e21539170e9
[メソッド]:https://qiita.com/takahirocook/items/5bfe43576d87a2a4006c
[mainメソッド]:https://qiita.com/takahirocook/items/f4635915337303de338c
[メソッドの呼び出し]:https://qiita.com/takahirocook/items/f4635915337303de338c
[コンストラクタ]:https://qiita.com/takahirocook/items/fa1822f2f22c3786593e
[引数]:https://qiita.com/takahirocook/items/5e5b0ba79e869f4a592e
[戻り値]:https://qiita.com/takahirocook/items/3b6fa670a1d6dd4a9386
[this]:https://qiita.com/takahirocook/items/d251ec4693c68f6b9538
[getter・setter]:https://qiita.com/takahirocook/items/27828bc8477735612021
[setter]:https://qiita.com/takahirocook/items/27828bc8477735612021
[getter]:https://qiita.com/takahirocook/items/27828bc8477735612021
[オブジェクト指向]:https://qiita.com/takahirocook/items/041ba7a096b71ab8ffd4
[継承]:https://qiita.com/takahirocook/items/6c84ea66a6e2ad536a37
[オーバーライド]:https://qiita.com/takahirocook/items/09dd8e5f56d6617ce45a
[オーバーロード]:https://qiita.com/takahirocook/items/b937c3c07126fe7e02a4
[this]:https://qiita.com/takahirocook/items/d251ec4693c68f6b9538

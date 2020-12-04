---
layout: post
title: 自キ活1年目で出来たものと、総当たりマトリクスのご紹介（ダイジェスト版）
author: Takeshi Nishio
tags:
- keyboard
- advent_calendar
date: 2020-12-05
published: true
---


この記事は [キーボード #2 Advent Calendar 2020](https://adventar.org/calendars/5307) の、5日目の記事です。

前の記事は、s-showさんの”[自作キーボード活動2年目の振り返り](https://kankodori-blog.com/?p=719)”でした。  
次の記事は、eswaiさんの”[今年やったことのまとめ]()”です。

---

この1年は、僕にとっての自作キーボード元年でした。  
なんやかんやで、自分で自分のキーボードを作れるようになった自キ活の1年目をふりかえります。  
また、キーボードを作る中で偶然（？）使えるようになった総当たりマトリクスについても紹介します。

<small>なお、こちらの記事はダイジェスト版となっております。  
お時間のある方は[フル版]({% post_url 2020-12-05-first-year-of-my-self-made-keyboard-activity %})をご覧ください。</small>


## 自キ活1年目で出来たもの

この1年の自作キーボード活動（＝自キ活）で出来たものを紹介します。

### 初めての自作キーボード [ErgoDash](https://yushakobo.jp/shop/ergodash/), 2019年11月

肩にやさしく、OTAKUっぽい分離型でエルゴノミクスを感じる配列の[ErgoDash](https://yushakobo.jp/shop/ergodash/)のキットを、初めての自作キーボードに選びました。

![初めての自作キーボード、ErgoDash](/assets/2020-12-05/IMG_0611.jpeg)




### ErgoDash用パームレスト一体型ハイプロアクリルケース, 2019年12月

ErgoDash純正のケースだとキーキャップ下側の角に手が引っかかるのが気になったので、フレーム付きのハイプロケースを作成しました。



![ErgoDash用パームレスト一体型ハイプロアクリルケース](/assets/2020-12-05/IMG_0631.jpeg)




### SU120基板発注, 2019年12月末
自分用のキーボードを作りたいという思いが強くなり、過去のアドベントカレンダーからe3w2q氏の”[レイアウトを試行錯誤しやすくするために作った自作キーボード用基板の開発で試行錯誤した話](https://e3w2q.github.io/7/)”という記事を見つけ、基板を作らずに自由なレイアウトが作れる[SU120](https://github.com/e3w2q/su120-keyboard)を発注しました。  

![Elecrowから到着したSU120 Rev.7基板](/assets/2020-12-05/IMG_0889.jpeg)


### 改造キーボード [NumAtreus_Plus8](https://github.com/jpskenn/NumAtreus_Plus8), 2020年1月

遊舎工房の福袋に入っていた[NumAtreus](https://yushakobo.jp/shop/numatreus-kit/)ですが、どう考えても40%キーボードなんて使える気がしないので、左右に1列ずつ増やす改造を加えて[NumAtreus_Plus8](https://github.com/jpskenn/NumAtreus_Plus8)を作成しました。


![NumAtreus Plus8](/assets/2020-12-05/DSC_6824.jpeg)





### 初めて自分で設計したキーボード [Colice（コリス）](https://github.com/jpskenn/Colice), 2020年1月〜5月

合体構造により左手、右手とテンキーの位置をを変えられ、一体型かつ分離型のキーボード、[Colice](https://github.com/jpskenn/Colice)を製作しました。  




![Colice, 完成](/assets/2020-12-05/DSC_6907.jpeg)






### 総当たりマトリクスを採用したキーボード [Atreus RR](https://github.com/jpskenn/AtreusRR), 2020年3月

Pro Micro1個でたくさんのキーを動作させる方法を調べていて、2乗マトリクスで色々やっているうちに偶然（？）不具合を回避する方法を発見し、総当たりマトリクスを採用した[Atreus RR](https://github.com/jpskenn/AtreusRR)が完成しました。

![NumAtreus_Plus8 RR, 手配線](/assets/2020-12-05/IMG_1353.jpeg)




### とても具合の良い60%キーボード [Jones（ジョーンズ）](https://github.com/jpskenn/Jones), 2020年5月末〜現在


通常のロースタガ配列でそこそこ満足という気持ちと、もうちょっと使いやすくしたいという想いから、ロースタガとオルソリニアを組み合わせたGH60型ケース互換の60%キーボード、[Jones](https://github.com/jpskenn/Jones)を作りました。  




![Jones v.0.3.1 w/ KBDfans 5° Case](/assets/2020-12-05/DSC_7266.jpeg)


総当たりマトリクスの採用や、ロータリーエンコーダや2音同時発音のスピーカーの搭載など、内部は今年1年で得た知識をフル動員した感じです。  

<blockquote class="twitter-tweet" data-dnt="true"><p lang="ja" dir="ltr">Gimme! Gimme! Gimme!<a href="https://twitter.com/hashtag/Jones_kbd?src=hash&amp;ref_src=twsrc%5Etfw">#Jones_kbd</a> <a href="https://t.co/frBi9FMDjq">pic.twitter.com/frBi9FMDjq</a></p>&mdash; Takeshi Nishio (@jpskenn) <a href="https://twitter.com/jpskenn/status/1319242096478310400?ref_src=twsrc%5Etfw">October 22, 2020</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


### STM32F303評価ボード [STMeishi](https://github.com/jpskenn/STMeishi), 2020年10月〜現在

大きなサイズのファームウェアを使いたくなり、STM32F303を使った名刺サイズの評価用マクロパッド、[STMeishi](https://github.com/jpskenn/STMeishi)を作りました。  

電源LEDが点灯するだけで、ひとっつも動作しません。  
失敗から何かを学ぶ予定です…

![STMeishi v.1](/assets/2020-12-05/IMG_2025.jpeg)

---

## 総当たりマトリクスのご紹介

Atreus RRの製作中に偶然使えるようになった”総当たりマトリクス”を紹介します。

### 総当たりマトリクスとは

IKeJI氏の”[キーボードのマトリクス方式の分類](https://blog.ikejima.org/make/keyboard/2019/12/14/keyboard-circuit.html)”で取りあげられている”2乗マトリクス”に、ゴースト回避方法を追加したマトリクス方式です。  
N個のピンで、N(N-1)個のキーを使用することができます。

回路図が総当たり戦のリーグ表ような形になるため、”総当たりマトリクス”という呼称にしました。  

今のところ、Pro Microを含むATMega32u4でのみ動作を確認しています。  

詳しくは[以前書いた記事](https://github.com/jpskenn/SMK-Supplements/tree/master/RoundRobinMatrix)をご覧ください。

#### 利点

- 少ないピンで非常にたくさんのキーを使用できる
- Duplex-Matrix（N個のピンで、N^2/2個のキー）よりも使用ピン数を少なくできる

#### 欠点

- ダイオードの使用数がちょっと増える  
- 回路設計、基板配線の手間が少し増える
- QMKファームウェア整備作業が多少増える  


### ゴースト回避方法

ピンから他のピンへ向かう箇所にダイオードを挿入します。

That's it! これだけです。


### マクロパッド作成例

総当たりマトリクスを使った、2行×3列で6キーのマクロパッドの作成例です。  

#### 回路設計

1. 使用するピンの数を決めます。  
    この例では6キーなので、3個のピンを使用して3(3-1)=6キーを接続します。

1. ピンとピンの間にスイッチを配置します。  

    | | Pin1 | Pin2 | Pin3|
    |:-:|:-:|:-:|:-:|
    |Pin1| - | SW21 | SW31 |
    |Pin2| SW12 | - | SW32 |
    |Pin3| SW13 | SW23 | - |  

1. ピンから他のピンへ向かう箇所にダイオード（D1, D5, D9）を挿入します。  
    ![回路図](/assets/2020-12-05/RoundRobinCircuitDiagram.png)


#### QMKファームウェア整備

- rules.mk  
カスタムマトリクス関連の指定をおこないます。

    - カスタムマトリクスを使用する設定と、総当たりマトリクス方式でのマトリクススキャン方法を記述した`matrix.c`を読み込む指定を追加します。  
        ```
        CUSTOM_MATRIX = yes
        SRC += matrix.c
        ```

    - `matrix.c`を`quantum/matrix.c（※）`を改変して作成し、rules.mkと同じフォルダへ配置します。  
    [ここ](/assets/2020-12-05/matrix.c)に雑なサンプルを用意しました。  

        ※：Pro Micro2個の分離型は、`quantum/split_common/matrix.c`を改変します。

- config.h  
使用するピン数と、ピン番号を指定します。  
総当たりマトリクスでは、ROW、COLともに同じピン数、同じピン番号になります。

    ```
    #define MATRIX_ROWS 3
    #define MATRIX_COLS 3

    #define MATRIX_ROW_PINS { B3, B2, B6 }
    #define MATRIX_COL_PINS { B3, B2, B6 }
    ```

- keyboard.h  
回路上のマトリクスと物理的なキー配置を対応づけします。  

    - 回路上のマトリクス（下半分）  
    3行×3列の回路上のマトリクスのうち、スイッチを配置していない箇所は`KC_NO`とします。

    - 物理的なキー配置（上半分）  
    回路上のマトリクスで`KC_NO`となっている部分を詰めて、2行×3列に配置します。

    ```
    #define LAYOUT( \
        K12, K21, K31, \
        K13, K23, K32  \
    ) \
    { \
        { KC_NO, K21,   K31   }, \
        { K12,   KC_NO, K32   }, \
        { K13,   K23,   KC_NO } \
    }
    ```

---

## 終わりに

ほぼ知識ゼロの状態からスタートした自キ活でしたが、「これは無理かも」と思うようなときは、”[サンボマスター / できっこないを やらなくちゃ](https://mora.jp/package/43000001/4988009064888/)”を聴いてなんとかやってこれました。  

また、これらのキーボードが作れたのは、先達の知恵のおかげです。  
特に[過去のアドベントカレンダー](https://scrapbox.io/self-made-kbds-ja/アドベントカレンダー)は知恵の宝庫で、読み返すたびに発見があり、何かしらの知識を与えてくれ、大変助かりました。  

さて、今後の自キ活ですが、Jonesにかなり満足してしまったので少しペースを落としつつ、Jones用オリジナルケースや分離型、STM32化などを進めていこうと思っています。  
また、手の大きさ（小ささ）に合わせた、狭ピッチなキーボードも試してみたいです。  

キーボードは何かをするための道具だと思っているので、具合の良い道具で楽しく快適に何かをやっていきたいです。

---

この記事は、[Jones](https://github.com/jpskenn/Jones)(v.0.3.1)のANSIスタイルをKBDfans 5°ケースと組み合わせ、流れるレインボーを見ながら書きました。

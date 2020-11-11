---
layout: post
title: "自キ活1年目で出来たものと、総当たりマトリクスのご紹介"
date: 2020-12-05
---

この記事は [キーボード #2 Advent Calendar 2020](https://adventar.org/calendars/5307) の、5日目の記事です。

前の記事は、s-showさんの”[自作キーボードについて考えていることなど]()”でした。  
次の記事は、eswaiさんの”[今年やったことのまとめ]()”です。

---

この1年は、僕にとっての自作キーボード元年でした。  
自作キーボードに出会い、キットの組み立てから始めて、オリジナルのケースやキープレートの製作、そして基板の製造までできるようになった自キ活の1年目をふりかえります。  
また、キーボードを作る中で偶然（？）使えるようになった総当たりマトリクスについても紹介します。


## 自己紹介

2020年現在、40歳代の中盤。  
情報処理系の学部をゆっくり卒業してソフトウェア開発会社に就職したけど、Javaをちゃんと理解する前になんだかしんどくなってやめちゃった人。  
今は事務職。紙とハンコとFAXと、Windows XPが現役の職場だよ♪

Java、Perl、VBAあたりの開発言語はわかるけど、他はあんまり…  
QMKのCは、なんとなくでやっています。  
gitとかよくわかんないし、QMKのプルリク（？）は怖くて手が出せていません。

電気・電子回路など、ハード面の知識はほぼゼロ。  
LEDの抵抗の計算は2019年10月に初めてやりました。

## 自キとの出会い

大学生の頃からキーボードに興味があり、ヤフオクでIBM Model Mを手に入れたり、計算機室にあったX端末のキーボードに惚れ込んだりしていました。

社会人になってしばらくはIBMのSpace Saver Keyboard IIを使っていましたが、英語配列のRealforce 101が発売されると割と早めに手に入れていました。また、ソフトウェア開発会社ではHHKB Professionalを使っていました。

事務職になってからはテンキー付きのRealforce 101を愛用していましたが、長年の使用でくたびれてきたためRealforce R2 静音30gに乗り換えたところ、とても具合がよく大満足しました。  
その大満足を受け、家のMacで使っていたLogicool K480のひどい打鍵感をなんとかしようと、ネットを彷徨って見つけたのが自作キーボードでした。


## 自キ活1年目で出来たもの

この1年の自キ活で出来上がったものを紹介します。

### 初めての自作キーボード [ErgoDash](https://yushakobo.jp/shop/ergodash/), 2019年11月

市販品のErgoDoxやKinesis Freestyleなどと比較しつつ、「分離型で、左手でYを打鍵する癖（現在は矯正済み）に対応できる7列で、エルゴノミクスを感じる配列」という要望を満たす、[ErgoDash](https://yushakobo.jp/shop/ergodash/)のキットを作成しました。

![初めての自作キーボード、ErgoDash](/assets/2020-12-05/IMG_0611.jpeg)

Mill-Maxソケットでソケット化する工夫をしたり、アンダーグローLEDを基板のおもて面につけるという定番のミスをやったりして、ハードを完成させました。  

[Catalina上でQMKのファームウェアを書き込めないトラブル](https://github.com/qmk/qmk_firmware/issues/6133)に遭遇し、ファームウェアを書き込めたのはハードの完成から数日後でした。

初めてのキット組み立てでは、自作キーボードがどういう部品で構成され、どのように組み立てるのか、またそれを動かすファームウェアについての基本的な知識を学びました。

### ErgoDash用パームレスト一体型ハイプロアクリルケース, 2019年12月

ErgoDash純正のケースだとキーキャップ下側の角に手が引っかかるのが気になったので、フレーム付きのハイプロケースを作成しました。



![ErgoDash用パームレスト一体型ハイプロアクリルケース](/assets/2020-12-05/IMG_0631.jpeg)

最初にできたものは[75%スケール](https://raw.githubusercontent.com/jpskenn/jpskenn.github.io/main/assets/2020-12-05/IMG_0624.jpeg)だったりしましたが、図面を正しく作り直して完成しました。  
ガラスエッジのアクリルケースは美しく、高さ調整式のパームレストで打鍵しやすくなりました。

ケース図面の描き方、キースイッチなどのサイズ、図面の出力は96dpiということを学び、誤発注の怖さを知りました。


### SU120基板発注, 2019年12月末
ErgoDashを使い込むうちに自分用のキーボードを作りたいという思いが強くなりましたが、ハード面の知識と経験がなかったため、基板の作成が大きな壁でした。  

そんなとき、過去のアドベントカレンダーからe3w2q氏の”[レイアウトを試行錯誤しやすくするために作った自作キーボード用基板の開発で試行錯誤した話](https://e3w2q.github.io/7/)”という記事を見つけ、基板を作らずに自由なレイアウトが作れる[SU120](https://github.com/e3w2q/su120-keyboard)の存在を知りました。  

![Elecrowから到着したSU120 Rev.7基板](/assets/2020-12-05/IMG_0889.jpeg)
「これなら基板設計なしでキーボードを作れる！」と、早速GitHubで公開されていた基板データをElecrowへ発注しましたが、一番安い発送方法のRegistered Mailにしたら到着まで1ヶ月ほど待たされました。


過去のアドベントカレンダーには先達の知識が詰まっていることを学びました。  
また、財布が許す限り、可能な限り早く受け取れる発送方法を選ぶのが、製作スピードとモチベーションを維持させるために重要だと体感しました。  

### 改造キーボード [NumAtreus_Plus8](https://github.com/jpskenn/NumAtreus_Plus8), 2020年1月

遊舎工房の福袋に入っていた[NumAtreus](https://yushakobo.jp/shop/numatreus-kit/)。  
どう考えても40%キーボードを使える気がしないのでメルカリにでも出そうかと悩みましたが、左右に1列ずつ増やす改造を加え、[NumAtreus_Plus8](https://github.com/jpskenn/NumAtreus_Plus8)を作成しました。


![NumAtreus Plus8](/assets/2020-12-05/DSC_6824.jpeg)
入門書片手に、KiCadでキープレート兼ベースプレートを設計し、サリチル酸氏の”[PCBのマスクとシルクでオリジナルプレートを作ろう！](https://salicylic-acid3.hatenablog.com/entry/introduction_to_pcb_design)”を参考に、赤レジストに首里城とシーサーのイラストをつけました。  


この改造では、キーボードを低くするための構造や、Pro Microのピンの使い方とQMKファームウェアの作り方、基板設計の基礎についての知識が深まりました。  
また、小さな部品の半田付け技術が少し向上しました。




### 初めて自分で設計したキーボード [Colice（コリス）](https://github.com/jpskenn/Colice), 2020年1月〜5月
合体構造により左手、右手とテンキーの位置をを変えられ、一体型かつ分離型で、カラムスタガなAlice風配列のキーボード、[Colice](https://github.com/jpskenn/Colice)を製作しました。  
自分で作る自分用のキーボードです。

![Colice, SU120によるプロト版](/assets/2020-12-05/IMG_0987.jpeg)
SU120を使って作成したプロト版。  
約5度の傾斜角をつけた段ボールに乗せ、普段使いしながらレイアウトを調整していました。  
プロト版では、Pro Microを2個使用した分離型キーボードの回路構成でした。

![Colice, 完成](/assets/2020-12-05/DSC_6907.jpeg)
合体構造を試行錯誤したり、総当たりマトリクスを採用してPro Micro1個だけで動作させたり、トップマウント構造に難儀したり…  
プロト版や試作版を経て、製作開始から5ヶ月で完成に至りました。  

キーやスタビライザーのサイズ、ケース構造、回路の設計、QMKファームウェアなど、自キ全般の知識と理解が深まり、製作に使用するKiCadやグラフィックツールなどの習熟度も上がりました。  
また、試作の重要性もわかりました。

少し大袈裟ですが、利用シーンや機能、アピール性など、モノとしての企画を管理、処理していくプロジェクトの進め方についても、多少は身についた感じがします。



### 総当たりマトリクスを採用したキーボード [Atreus RR](https://github.com/jpskenn/AtreusRR), 2020年3月

先ほどのColiceをPro Micro1個だけで動作させる方法を調べていて、過去のアドベントカレンダーから次の記事を見つけました。

- e3w2q氏の”[Duplex-Matrixを自作キーボードで使う方法](https://e3w2q.github.io/8/)”
- IKeJI氏の”[キーボードのマトリクス方式の分類](https://blog.ikejima.org/make/keyboard/2019/12/14/keyboard-circuit.html)”

雑に動作確認して、2乗マトリクスでNumAtreus_Plus8を作り直してみたところ、**見事に失敗しました**。  
特定のキーでゴーストが発生して、使い物になりませんでした。

![NumAtreus_Plus8 RR, 手配線](/assets/2020-12-05/IMG_1353.jpeg)
色々やっているうちに**奇跡的に不具合を回避する方法を発見し（※1）**、総当たりマトリクスを採用した[Atreus RR](https://github.com/jpskenn/AtreusRR)（※2）が完成しました。

電気回路がちょっとわかり、QMKファームウェアで独自マトリクスを使う方法を覚え、総当たりマトリクスが使えるようになりました。

※1：詳しくは後述の”総当たりマトリクスのご紹介”を参照  
※2：RRは、”総当たり”を意味する”*R*ound *R*obin”の略


### ロースタガとオルソリニアを組み合わせた、GH60型ケース互換の60%キーボード [Jones（ジョーンズ）](https://github.com/jpskenn/Jones), 2020年5月末〜現在


通常のロースタガ配列でそこそこ満足という気持ちと、左右対象じゃなかったり、右手のModキーが遠かったりするのをなんとかしたいという想いから、ロースタガとオルソリニアを組み合わせた、GH60型ケース互換の60%キーボード、[Jones](https://github.com/jpskenn/Jones)を作りました。  

![Jones v.0.3.1 w/ KBDfans 5° Case](/assets/2020-12-05/DSC_7266.jpeg)
回路と基板はai03氏の”[PCB Designer Guide](https://wiki.ai03.com/books/pcb-design/chapter/pcb-designer-guide)”と”[Voyager60](https://github.com/ai03-2725/Voyager60)”を参考にしつつ、2音同時発音のスピーカーや、ロータリーエンコーダを搭載し、総当たりマトリクスを採用しています。  

過去のアドベントカレンダーで、marksard氏も”[60%トレイマウントケースでTS配列](https://marksard.github.io/2019/12/13/about-treadstone60/)”という記事で、同様の手法でキーボードを作成されています。  


![Jones v.0.3 JPスタイル w/ 60%プラスチックケース](/assets/2020-12-05/DSC_7205.jpeg)

少しずつバージョンアップを重ね、v.0.3では[レイアウト](http://www.keyboard-layout-editor.com/#/gists/54a1c1fe1192d83c5ded8b8e7998a82b)が増え、JPスタイルの上下逆向きISOエンターでアピール度も高まりました。

その気になれば、さらっと曲を演奏したりもできます。
<blockquote class="twitter-tweet" data-dnt="true"><p lang="ja" dir="ltr">Gimme! Gimme! Gimme!<a href="https://twitter.com/hashtag/Jones_kbd?src=hash&amp;ref_src=twsrc%5Etfw">#Jones_kbd</a> <a href="https://t.co/frBi9FMDjq">pic.twitter.com/frBi9FMDjq</a></p>&mdash; Takeshi Nishio (@jpskenn) <a href="https://twitter.com/jpskenn/status/1319242096478310400?ref_src=twsrc%5Etfw">October 22, 2020</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

キーレイアウトの試行錯誤のしかたを身に付け、Pro Microを使わずにキーボードを作る方法を学び、部品の選定や配置、製造のやり方についても知ることができました。  
MCUなどの表面実装部品の半田付け技術が大きく向上しました。

### STM32F303評価ボード [STMeishi](https://github.com/jpskenn/STMeishi), 2020年10月〜現在

大きなサイズのファームウェアが使いたくなり、STM32F303を使った名刺サイズの評価用マクロパッド、[STMeishi](https://github.com/jpskenn/STMeishi)を作りました。

![STMeishi v.1](/assets/2020-12-05/IMG_2025.jpeg)
電源LEDが点灯するだけで、ひとっつも動作しません。  
ああああああああ…  
USBブートしてくれません。っていうかMCUが動作してるのかさえわからないです😭

失敗から何かを学ぶ予定。

## 総当たりマトリクスのご紹介

Atreus RRの製作中に、偶然使えるようになった総当たりマトリクスを紹介します。

### 総当たりマトリクスとは

IKeJI氏の”[キーボードのマトリクス方式の分類](https://blog.ikejima.org/make/keyboard/2019/12/14/keyboard-circuit.html)”で取りあげられている”2乗マトリクス”に、ATMega32u4向けのゴースト回避方法（※）を追加したマトリクス方式です。  
N個のピンで、N(N-1)個のキーが使用できます。

回路図が総当たり戦のリーグ表ような形になるため、”総当たりマトリクス”という呼称にしました。  

※：Pro Microを含む、ATMega32u4の特性に絞り込んだゴースト回避方法です。他のMCUでも、GPIOピンの特性が合えば動作するかもしれません。

#### 利点

- 少ないピンで非常にたくさんのキーを接続できる  

  例えば、11個のピンで11(11-1)=110キーが使用でき、フルキーボードのキーをまかなうことができます。  
  余ったピンを他の機能にまわすことができます。  

#### 欠点

- ダイオードの使用数がちょびっと増える  
- 回路設計の手間がちょっと増える
- QMKファームウェアの整備の手間が増える  


### ゴースト回避方法

GPIOピンから他のGPIOピンへ向かう箇所にダイオードを挿入します。

That's it! これだけです。

詳しい理由は、[以前書いた記事](https://github.com/jpskenn/SMK-Supplements/tree/master/RoundRobinMatrix)をご覧ください。

### マクロパッド作成例

総当たりマトリクスを使った、2行×3列、6キーのマクロパッドの作成例です。  
3個のピンを使用し、3(3-1)=6キーを扱います。

#### 回路設計

- ピンとピンの間にスイッチを配置します。  

    | | Pin1 | Pin2 | Pin3|
|:-:|:-:|:-:|:-:|
|Pin1| \ | SW21 | SW31 |
|Pin2| SW12 | \ | SW32 |
|Pin3| SW13 | SW23 | \ |

- GPIOピンから他のGPIOピンへ向かう箇所にダイオード（D1, D5, D9）を挿入します。  

![回路図](/assets/2020-12-05/RoundRobinCircuitDiagram.png)


#### QMKファームウェア整備

- rules.mk  
カスタムマトリクスを使用する設定と、総当たりマトリクス方式でのマトリクススキャン方法を記述したmatrix_rr.cを読み込む指定を追加します。  

    ```
CUSTOM_MATRIX = yes
SRC += matrix_rr.c
```

    matrix_rr.cはquantum/matrix.c（※）を改変して作成し、rules.mkと同じフォルダへ配置します。  
    [ここ](/assets/2020-12-05/matrix_rr.c)にサンプルを用意しました。

    ※：Pro Micro2個の分離型は、quantum/split_common/matrix.cを改変します。

- config.h  
使用するピンの数と、ピンの番号を指定します。  
総当たりマトリクスでは、ROW、COLともに同じピン数、同じピン番号になります。

    ```
    #define MATRIX_ROWS 3
    #define MATRIX_COLS 3

    #define MATRIX_ROW_PINS { B3, B2, B6 }
    #define MATRIX_COL_PINS { B3, B2, B6 }
    ```

- keyboard.h  
レイアウトを指定します。  
ピンとピンの間にスイッチを配置していない箇所は、KC_NOとします。

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

## まとめ

自作キーボードキットの組み立てから始めて、1年で

アドカレは一つの夢
アドカレは貴重な情報源
[クールなURIは変わらない](https://www.kanzaki.com/docs/Style/URI)
サンボを聴け
「売ってないから、自分で作る」という、とても単純なことを本気でやった製作
1、2年遅れ
キーボードはペン。ペンを作りたいんじゃなくて、書きやすいペンで何かを書いたり、作ったりしたいのがほんとのやりたいこと。
Jonesの満足度が高いので、しばらくはキーボードを作らずに生活できそう

---

この記事は、自分で設計した[Jones](https://github.com/jpskenn/Jones)(v.0.3.1)のANSIスタイルをKBDfans 5°ケースと組み合わせ、流れるレインボーを見ながら書きました。

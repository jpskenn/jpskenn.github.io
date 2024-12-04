---
layout: post
title: 自キにまつわる気持ちの問題と、1年半ぶりにEnd Gameを更新したSandyLPのご紹介
author: Takeshi Nishio
tags:
- keyboard
date: 2024-12-03
published: true
---

この記事は[キーボード #2 Advent Calendar 2024](https://adventar.org/calendars/10116)の5日目の記事です。

昨日は🌧️2d0さんの「"kokken72"についてのお話を」でした。  
〓感想

明日はis_wateringさんの「今年設計したキーボードについて」です。

---

RP2040を基板直乗せするとか、Vialなファームウェアの作り方とか、すでにどこかで解説されているので技術的なネタがありません。

というわけで、自キにまつわる気持ちの問題（精神論的な何か）をいくつかと、1年半ぶりに*End Game*を更新した[SandyLP](https://github.com/jpskenn/SandyLP)について書こうと思います。

## 自キ道

数年前、[Jones](https://github.com/jpskenn/Jones)の開発中に、右手のアルファ部を外側へずらしたレイアウトを思いつきました。

![アルファ部を外側へずらしたレイアウト](/assets/2024-12-05/wide_layout.png)

EnterやBackspaceが近くて打鍵しやすいとか、肩が楽になるといったメリットがありましたが、自作キーボードにありがちな「**YとBの右手？左手？問題**」にぶつかってしまいました。  
<small>今では考えられないことですが、その頃（2020年）の僕は、たまにYを左手で打鍵する癖がありました。</small>

このレイアウトを採用するか悩んだ結果、2020年8月のメモには次のような思いを書いていました。

*「ハード面、ソフト面だけでなく、自分自身の改良・変更をおこなうのも**自キ道**の範疇に含まれると考え、今回は左手Yの癖を矯正することにした。」*

**自キ道**（笑）

その「自キ道」を貫いた結果、Tの隣に背の高いキーキャップを取り付けて、左手Yしようとする人差し指をブロックするようにしました。1週間ほどで運指を矯正することができ、レイアウトはめでたく採用となりました。  
それ以来ずっとこのレイアウトを使い続けているので、4年ほど肩が楽に過ごせたことになります。

この話以外にも、左右のシフトキーを取り外して力技で親指シフトに移行したり、レイヤーに入れた数字や記号を何も考えずに打鍵できるようにしたり、スキーで右肩を脱臼したついで（ついで？）に左手でマウスを使えるようにしたり…と、いろんな自キ道があります。

キーボードやマウスは道具ですから、その道具を使う人間の修練や鍛錬もある程度必要ですよね。  
ましてや、1～2週間で身につけられるのであれば、今すぐ自キ道を始めた方がお得ですね！

## 優先事項

職場用の自キを持ち帰って完璧に整備したのに、家に忘れて来てしまい、F社のノートPCのキーボードを1日使うことになった残念な日のメモがこちらです。

*「スイッチの打鍵感や筐体などの要素は、二の次、三の次といったところであり、やはり配列が一番の肝である。」*

ノートPCのペチペチとした打鍵感やグラグラのキーキャップは、気持ち良くはないものの我慢できる許容範囲でしたが、レガシーなロウスタッガード配列は左手がつらすぎて窓から投げ捨てたい気分でした。  

「**うんこ味のカレーと、カレー味のうんこ。**」みたいな感じですが、皆さんならAとBのどちらを選ぶでしょうか？

A: レガシーなロウスタッガード配列 ＋ あなたの考える最高に気持ちの良いスイッチ

B: あなたにぴったりフィットするレイアウト ＋ ガサガサ・シャリシャリの謎スイッチ

僕は自分が使いやすいレイアウトに早くたどり着きたいと思って活動しているので、Bを選びました。（Bは後でスイッチ交換できそうだし。）

<small>（Aってカスタムキーボードですよね？）</small>

## キーは上から押すだけだと思っていないか？

[Sandy](https://github.com/jpskenn/sandy)の使用感を記録したメモに、

*「スペースキーとそれよりひとつ外側のキーのスイッチをTecsee Pudding Medium Linearに変更して少し低くし、一番外側のキーの角に親指がかかる感じにした。これで、キーの横から斜め下へ押下する具合にしたい。」*

と書いていました。  
さて、これはどういう意味でしょうか？

今さらこんなことを言うのも恥ずかしいのですが、キーは上からだけでなく斜めに押しても入力できます。  
キーキャップの天面がシリンドリカルやスフェリカルになっているのは、指の引っかかりをよくすることに加えて、キーを多少斜めに押してもスイッチへ力を伝えるためでもあります。  
これを拡大解釈すると、「キーは斜めに押しても入力できる」という理論が導き出されます。

この理論を実際の動作に応用すると、次の動画のようになります。  
<small>（指の動きが見えるように、ホームポジションから手をずらして撮影しています。）</small>

<blockquote class="twitter-tweet" data-media-max-width="560"><p lang="ja" dir="ltr">アドカレネタ <a href="https://t.co/tJreHhqj1g">pic.twitter.com/tJreHhqj1g</a></p>&mdash; Takeshi Nishio (@jpskenn) <a href="https://twitter.com/jpskenn/status/1863915297092293021?ref_src=twsrc%5Etfw">December 3, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

https://github.com/user-attachments/assets/7f23591e-8581-4c61-b161-3ef6f9905187

これは、段差をつけたキーの側面から天面の角あたりへ親指を当て、キーを押下している様子です。  
親指を曲げて横方向に動かすだけで、下方向にキーが押し込まれています。  

先程導き出した理論は間違いでしたね。  
正しくは、「**キーは横に押しても入力できる**」となります。  
使い所が限られるのでご注意ください。

<small>スイッチは、低いキーがメモに出てきたTecsee Pudding Medium Linearで、高いキーはKailh Deep Sea Silentです。
キーキャップは[G20プロファイル](https://spkeyboards.com/search?q=g20&options%5Bprefix%5D=last)の1.25uです。</small>

## 数日寝かせると命拾いする

基板の設計が終わったら、数日寝かせてから発注しましょう。  
思いも寄らないミスが見つかるかもしれませんよ。

今回ご紹介するSandyLPでも、寝かせる宣言から数時間で凡ミスが見つかりました。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">3日間でなんとかここまできたけれど、気になるところが出てきそうなので、発注までに1-2日は寝かせた方が良いな… <a href="https://t.co/nk1cmUBHSm">pic.twitter.com/nk1cmUBHSm</a></p>&mdash; Takeshi Nishio (@jpskenn) <a href="https://twitter.com/jpskenn/status/1835572650216964400?ref_src=twsrc%5Etfw">September 16, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">早速、びっくりするくらいの凡ミスを発見。しかも致命的なやつ💦<br><br>あと、JLCPCBのマーキングが無料で消せるようになっていたので、魔法の言葉「JLCJLCJLCJLC」を消して回りました。</p>&mdash; Takeshi Nishio (@jpskenn) <a href="https://twitter.com/jpskenn/status/1835651215901983138?ref_src=twsrc%5Etfw">September 16, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## SandyLP（サンディ エルピー）のご紹介

今年の10月、左右対称ロウスタッガードな所謂Jones配列（※）の最新版として[**SandyLP（サンディー エルピー）**](https://github.com/jpskenn/SandyLP)が完成しました。  
<small>※自分で「Jones配列」と言い始めたわけではないのですが、キボ界隈からそう呼ばれていて記述もしやすい呼称なので使わせてもらっています。</small>

![SandyLPビルド例](/assets/2024-12-05/DSC_8161.jpeg)

![SandyLPビルド例](/assets/2024-12-05/DSCF5294.jpeg)

![SandyLP基板裏面](/assets/2024-12-05/IMG_6834.jpeg)

- 左右対称ロウスタッガードな40%レイアウト
- スイッチを立体的に配置
- キーボード全体がそこそこ低い（Choc V2スイッチ使用）

というのが特徴です。（詳しくは[こちら](https://github.com/jpskenn/SandyLP)）

前作の[Sandy（サンディー）](https://github.com/jpskenn/Sandy)も*End Game*として1年半ほど使い続けてきたのですが、その1年半で得られた経験を可能な限り開発にフィードバックしたので、SandyLPが完成した瞬間から新たな*End Game*が始まることになりました。  

枯れた技術を使うようにしているので今回の開発に新しい技術はないのですが、RP2040の基板直乗せや、基板間の電気的接続をすべて金属スペーサーによる導通に変更したことは、開発におけるチャレンジングな部分でした。

また、使用するパーツとしてChoc V2スイッチとキーキャップとの干渉を心配していたのですが、お気に入りのキーキャップは以下の組み合わせで使えており、助かっています。  

- Kailh Deep Sea Silent MINI + Signature Plastics, DSS, Solarized Dark
- Kailh Deep Sea Silent MINI + ePBT, Cherry, Less But Better
- Kailh Lofree FLOW GHOST + Keyreative, KAT, Space Cadet

<small>（KATは少しスイッチに当たってるかも？ですが、気にならないレベル。）</small>

今後はケースやテンティングなどを設計・研究しつつ、*End Game*という長期ロードテストを楽しんでいこうと思っています。

皆さんも*End Game*を楽しんでください！！

---
この記事は、

- SandyLP 職場用（Kailh Deep Sea Silent MINI + ePBT Less But Better）
- SandyLP 自宅用（Kailh Deep Sea Silent MINI + DSS Solarized Dark）

で書きました。

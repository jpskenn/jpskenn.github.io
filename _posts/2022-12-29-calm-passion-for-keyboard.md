---
layout: post
title: キーボード熱が少し落ち着いている話
author: Takeshi Nishio
tags:
- keyboard
date: 2022-12-29
published: true
---

## まえがき

この数年、いわゆるEnd Gameと呼ばれるキーボードにたどり着くための活動を熱心に続けてきましたが、今年はその熱が少し落ち着いています。

開発関連のネタや新製品の情報などを追いかけることも無くなり、Twitterやコミュニティの閲覧もやめてしまっています。
「QMKのBreaking ChangeでRemapがやばい」なんて話題もTALPKEYBOARDさんのニュースメールで初めて知ったというありさまです。

<small>「うちのローカル環境のQMKは”0.16.9”です」と言えば、どのあたりで止まっているか伝わるでしょうか？</small>

さて、この記事では、キーボード熱が少し落ち着いた、その気分的なところを少し書いてみようと思います。

## キーボード熱が落ち着いた理由

まだEnd Gameは手に入れていませんし、End Gameなキーボードについての熱い想いは持ち続けていますが、表立った活動が落ち着いたのは以下のような理由です。

### Jonesの物理配列にハマりすぎて、欲しいキーボードがない

のっけから手前味噌で恐縮なのですが、Jonesの左右対称な物理配列の具合が良すぎて、欲しいキーボードが見つからないというのが一番の要因です。

僕は”左右対称の物理配列であること”を最優先にキーボードを選んでいるので、
「ガスケットだ〜、金属ケースだ〜、PCプレートだ〜、無線だ〜、トラックボールだ〜、Thoc! Thoc!」
と謳われていても、
「ぁ、普通のロースタガ…（そっ閉じ）」
で終わってしまうことがほとんどなのです。

そんな中、とりあえずひとつだけ、3D系の[Glove80](https://www.moergo.com)を2月にバックして到着を気長に待っているところです。

<small>同じ3D系の[Advantage 360](https://kinesis-ergo.com/keyboards/advantage360/)は、初回の供給数が少なすぎて朝起きたらすべて終わっていました。</small>

![Jones & Nora, symmetrical layout](/assets/2022-12-29/_DSF3262.jpeg)

JonesとNoraの左右対称な物理配列（ZをAより外側にして、右手側の記号を中央へ）

### 満足できるパーツが揃ってきたので、いろいろ試さなくてもよくなった

キーボードを構成するパーツのうち重要な部分を占めるスイッチとキーキャップですが、いろいろ試して満足できるレベル（※）のものが揃ってきたので、新製品を取っ替え引っ替えして試さなくてもよくなりました。

2019年11月にErgoDashで自作キーボードデビューしたので、2年〜2年半くらいかかったことになります。

※満足できるレベル
うまく説明できないんですが、

> 現在使ってるパーツは最も優れたパーツじゃ無いと暗黙的にわかっているけれど、
> 何かを探して買ってきてルブして組み替えて試して結局ハズレで元に戻す労力と費用と喪失感を考えたとき、
> 今の状態で使い続けた方が心の安定が保たれる、
> と思える程度・基準。

みたいなところを意図しています。

<details>
<summary>スイッチ</summary>

リニアのKailh Pro BurgundyとKailh Speed SilverをメインのJonesで使用しています。
押し始めは軽めの40gくらいで、押し込んで底つきする前にググッと重くなって押し戻してくれるような特性が好みです。
良い具合にルブしてから、上下ハウジングをセメダイン[BBX](https://www.cemedine.co.jp/home/adhesive/bbx/bbx.html)で固定してグラつきを低減させています。

サブのJonesで使ってるサイレントのKailh Silent Pinkは、ノイズが多めなのでちょっと不満です。
メイン機だったらすぐに交換するところですが、ほとんど使わないサブ機なので、実質的には問題なし。

NoraでもリニアのChoc Crystal Silverを使用しています。
スタビなしで静かなのと、40gという重さが気に入っています。
Chocは選択肢が少ないので、タクタイルの有無と、好みの重さで選ぶだけですね。

うるさくて普段使いには向かないのですが、クリッキー白軸のシャープなタクタイル感もかなり好きです。
</details>

<details>
<summary>キーキャップ</summary>

打鍵速度が一番早いのはKATですが、ホームポジションに手を置いたときに心地よいDSSプロファイルが気に入っています。

Choc用ではシリンドリカル形状のMCCプロファイルが好みです。
POM素材のツルッとした触り心地も良いです。
あまり使っていませんが、実はKailh純正のキーキャップが一番打鍵しやすい気がしています。（打鍵速度は一番でした）

GBしたキーキャップの到着待ちがいくつかあるので、しばらくは買わなくても良さそうです。
</details>

### End Gameが見えてきたので、闇雲な行動がなくなった（開発保留中）

いろいろなキーボードを作ったり使ったりした結果、経験値がけっこうたまりました。
その結果、どんなキーボードが自分のEnd Gameになるのか見えてきたので、闇雲に情報を探したり、研究・実験用品を買い漁ったりする必要がなくなりました。

また、End Game開発に向けた調査事項もわかったので、その教材であるGlove80が到着するまで、開発は一旦保留になっています。（来年、2023年の夏までには届くかな？）

たまった経験値の例（クリックでコメント表示）

<details>
<summary>カラムスタガ系の所感</summary>

手のサイズに合わないと、とっても打鍵しづらくなる。
設計者と自分の手の大きさが同じだったらラッキーだけど、そんなラッキーはまずない。
個人に合わせたカスタム設計が必須になるので、つらい。

実機を試打してから購入するか、[Pangaea](https://e3w2q.github.io/23/)による救済か。
</details>

<details>
<summary>ロースタガ系の所感</summary>

普通のロースタガでもそこまで打鍵しづらいということは無いし、Jonesのように2行目と3行目にずれがない変則的なロースタガでも普通に打鍵できちゃう。
横ずれ方向は手のサイズに対する許容範囲が大きいようで、だいたいなんでもOKな印象。（さすがにオルソリニアは許容範囲外だけど）

自然と手を置いたところにキーがあって欲しいので、Jonesの左右対称なロースタガに行き着いている。
</details>

<details>
<summary>3D的な打鍵のしやすさが重要</summary>

ホームポジションから遠いところ、たとえば60%キーボードの1行目は背の高いキーキャップにするかスイッチ自体を底上げして3D的に配置しないと、指が届きにくい。

MXスイッチでは、行ごとに高さの違うCherry, KAT, DSS, MT3プロファイルなどのキーキャップを使うことで、3D的な打鍵のしやすさが向上する。

Chocスイッチでは、普通に売ってるキーキャップだと各行が同じ形状しか選べないため、3D的にできなくてつらい。
Choc用の3D的なキーキャップは値段がつらい（使用感はめっちゃ良い）。
自分で作るのは加工がつらい。
3D的な基板設計はとてもつらい。

![MBK keycap, Modified for height adjustment](/assets/2022-12-29/IMG_4017.jpeg)
”QTYP”キーの打鍵しやすさ向上のため、MBKキーキャップに3D的な加工（2枚重ねして角を削る）をおこなった例
</details>

<details>
<summary>キーピッチ（狭ピッチ）の所感</summary>

MXのキーピッチ（たて19mm×よこ19mm）でも不満はないけれど、けっこう余裕があるので、ピッチを狭くして物理配列を最適化したい。
指の移動量が減って打鍵しやすくなるなど、狭ピッチ化によるメリットは多い。

Chocのキーピッチ（たて17mm×よこ18mm）はMXから乗り換えても何の違和感もなく打鍵できるし、もう少し狭いキーピッチ（たて17mm×よこ17mmくらい）でも少し使えばすぐに慣れる。

狭ピッチ用のキーキャップ選びがつらい。
Choc用キーキャップがつらくてつらすぎ。（前項参照）
</details>

<details>
<summary>究極的にはフルカスタムの3D系へ</summary>

キースイッチが平面上に配置される2D的なキーボードをいろいろと使ってきて、キーの物理配列で縦横（XY軸？）を最適化することに限界を感じている。
平面上だけではどうしても最適化しきれない箇所が出てくるので、そこをキーの高さを変えることで補おうと考えると、次に進むのは3D系。

行き着く先は、自分の手の大きさ、指の長さや可動範囲に合うように3D的にフルカスタムするのが究極的なところ。
もちろん、腕や手首がフィットするパームレストも組み合わせて。
設計つらい。製造つらい。試作資金つらい。
→ とりあえず3D系を体験してみるところから始めよう。
→ Glove80がそのうち来る予定。

</details>

<details>
<summary>既成概念・固定観念を破る</summary>

実現可能性はちょっと横へ置いておいて、普通じゃないところに、何か良いものが生まれそうな気がする。

「アルファ部のキーを列ごとに幅を変えてみたら？」とか、
「四角じゃないキーキャップにしたら、もう少し縦横の最適化ができないか？」とか。

「もうそろそろ普通のロースタガやめませんか？」ってのは、ずっと思ってる。
</details>

### 開発の保留で、他の趣味を楽しむ機会が増えた

開発が一旦保留になりパーツ漁りなどもしなくなったので、他の趣味を楽しむ機会が増えました。
ゲームをプレイしたり、音楽を作ったり、キーボード以外の趣味で心が満たされる時間が少し多かったです。

[![YouTube: Hirasawa?, Roland MC 101](https://img.youtube.com/vi/2jx3ShFpAl0/0.jpg)
YouTube: Hirasawa?, Roland MC 101](https://www.youtube.com/watch?v=2jx3ShFpAl0)

## まとめ

キーボード熱が少し落ち着いた、その気分的なところを書いてみましたが、
「今のところはJonesで満足していて、今後はEnd Gameの3D系キーボードに向けて進んでいくんだけど、教材が来ないので開発は保留中です」
という、単純な内容でした。

生存報告というか、死に損ないの悪あがきというか、何の意味があるのか自分でもよくわからない記事を、構想1ヶ月、執筆4日で書きあげました。

## その他

遊舎工房さんで委託販売していただいているJonesとNoraですが、以下の理由により、在庫補充せず、終売にする予定です。

- ちょっと設計が古い
- 円安傾向で製造費がつらい
- そんなに売れない（笑）

ご愛顧いただいている皆さま、ありがとうございます。

---
この記事は、
- Jones（Kailh Pro Burgundy & Kailh Speed Silver + DSS Solarized Dark）
- Nora（Kailh Choc V1 Crystal Silver + MCC POM）
- iPhone 8（フリック入力）

で書きました。
---
layout: post
title: 初めてのQMKプルリクエスト
author: Takeshi Nishio
tags:
- keyboard
- qmk
- git
- GitHub
date: 2020-12-08
published: true
---

初めておこなったQMKへのプルリクエストについて。  
どういう風におこなったのかをメモ。

## 前書き

自分で設計した[Jones](https://github.com/jpskenn/Jones)キーボードを訳あり版ながらも販売を始めたことをきっかけに、正規ルートでファームウェアを提供したいと思ってプルリクした。


## masterへコミットしてごめんなさい

1年くらい前に”[本家QMKのリポジトリ](https://github.com/qmk/qmk_firmware)”からフォークしていたものを使っているが、ErgoDashのキーマップやSU120を使った評価用キーボード、自分で設計したColiceやJonesのファイルを、（いちいちブランチを作ったり切り替えたりするのが面倒になり）**すべてmasterへコミット**していた。

そのままプルリクすると雑多なものまで送られてしまうため、一度リセットする必要があった。

ちょっと困った状況をツイートしたら、@mteiさんが解決方法を教えてくれた。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">こちらを読めば解決出来ると思います<a href="https://t.co/e2Z5T1mkZ3">https://t.co/e2Z5T1mkZ3</a></p>&mdash; m.tei / ishii (@mtei) <a href="https://twitter.com/mtei/status/1334263835201478658?ref_src=twsrc%5Etfw">December 2, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

自分がmasterへコミットしていたものを退避しておいて、この”[同期のとれていない git ブランチの再同期](https://docs.qmk.fm/#/ja/newbs_git_resynchronize_a_branch?id=同期のとれていない-git-ブランチの再同期)”の手順をおこなって、フォークしたリポジトリのmasterをクリーンな状態に戻した。

その後、開発用ブランチを作り、退避しておいたものを適宜コミットした。

退避していたものの中に`.gitsubmodule`が混入していたのに気づかず、ちょっと面倒なことになったが、  
```
git checkout [混入前のコミットハッシュ] .gitmodules
```
で、混入する前の状態に戻して解決。




## プルリク前


”[QMK キーボードガイドライン](https://docs.qmk.fm/#/ja/hardware_keyboard_guidelines?id=qmk-キーボードガイドライン)”を読み、キーボード、キーマップとして求められるファイルを用意する。

単にキーボードを動作させるためだけだったら必要ないもの、例えば`readme.md`や`info.json`などを追加。  
`info.json`はKeyboard Layout Editorのデータを元に作成したが、ちゃんとできてるかよくわからない。 QMK Configuratorへ読み込ませてみたが、Jones JPスタイルの逆向きISOエンターがちゃんと表示されない。

次に”[PR チェックリスト](https://docs.qmk.fm/#/ja/pr_checklist?id=pr-チェックリスト)”の”キーマップのPR”と”キーボードのPR”を読み、求められる要件に合わせる。

使っていないレイアウトやコメントアウトした処理を消したり、重複がないようにしたり。  
LOWERとRAISE同時押しでADJUSTレイヤーにする処理を書き換えたりもした。

以上を開発用ブランチ”[develop_Jones](https://github.com/jpskenn/qmk_firmware/tree/develop_Jones)”で色々やっておいて、「よっしゃ、これで完成や！」となったタイミングで、プルリクを出すためのブランチ”[Add-jones-v.0.3-and-v.0.3.1-keyboard](https://github.com/jpskenn/qmk_firmware/tree/Add-jones-v.0.3-and-v.0.3.1-keyboard)”を作成した。

## プルリクっ！！

GitHubで、プルリク用ブランチを表示して、”Pull Request”をポチッと。

![](/assets/2020-12-08/open_pr.png)  

”Open a pull request”の画面になる。  
*（別のブランチ（develop_Jones）でスクリーンショットを撮ってるので、ブランチ名が違ってるのは勘弁）*  


![](/assets/2020-12-08/pr_description.png)  

上部の枠内が、
```
本家のqmk_firmware　masterブランチ　←　自分のqmk_firmware　プルリク用ブランチ
```
になっていることを確認。

次のように必要事項を記入する。

- タイトル：このプルリクで何をやるのか簡潔に  
    ”Add jones v.0.3 and v.0.3.1 keyboard”
- Description：プルリクの説明  
    ”Initial PR for adding Jones v.0.3 and v.0.3.1 keyboard.”
- Types of Changes：何を変更したか→キーボードとキーマップ
    - [x] keyboard
    - [x] Keymap
- Issues Fixed or Closed：このプルリクで修正完了されるもの  
    何もないので、”None”
- Checklist：チェックリスト  
    - [x] Cのコーディング規約に準拠
    - [x] PRチェクリストを読みました
    - [x] 貢献、提供の文書を読みました

記入したら”Create pull request”をポチッとして、プルリクを発射。

## ブルリク後

### 自動チェックでFail

プルリク発射から数分以内に、自動チェックの”PR Lint Keyboards”でFailとなった。  
エラー内容を見てみると、「キーボードのディレクトリに”readme.md”が無い」のが原因だった。
```
☒ Missing keyboards/jones/v.0.3/readme.md
87
☒ Lint check failed!
88
linting jones/v.0.3.1
89
☒ Missing keyboards/jones/v.0.3.1/readme.md
90
☒ Lint check failed!
91
Error: Process completed with exit code 2.
```

キーボードの親ディレクトリに置いてあればOKだと思い違いをしていたので、見つからないファイルを正しく配置してプルリク用ブランチへコミット。  
GitHubの自分のqmk_firmwareへpushしてしばらくすると、全てのチェックでOKとなった。

![](/assets/2020-12-08/add_missing_file.png)  

### レビュー（その1）

自動チェックにパスしてから3日ほどで、最初のレビューがついた。

- 【提案】音楽モードのキーマップ定義を、各キーマップではなく、キーボードのCファイルに移動したら？
- 【変更】makeオプションの直書きをやめ、yes/noで書くように。
- 【変更・提案】カスタムマトリクスを、”matrix.c”を丸々入れ替えるのやめて、”lite”形式で読み込むようにできる？

カスタムマトリクスの”lite”化にちょっと手こずったけど、提案・変更依頼の通りの修正をプルリク用ブランチへコミットした。

### レビュー（その2）
それから半日ほどで、もう1件のレビューがついた。

- 【変更】キーボード名から”.（ドット）”を取り除いてください。

次のように変更して、プルリク用ブランチへコミットした。

- ”v0.3” → ”v03”
- ”v.0.3.1” → ”v03_1”

### レビューへの対応後

作業の流れがよくわからないけれど、”Changes requested”のところから、レビューしてくれた人の右側の”・・・”を押して”Re-request review”をポチッとしておいた。

![](/assets/2020-12-08/changes_requested.png)  

その後2日ほど進展なし。
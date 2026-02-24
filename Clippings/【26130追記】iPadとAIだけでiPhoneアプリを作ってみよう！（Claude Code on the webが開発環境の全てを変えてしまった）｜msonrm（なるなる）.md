---
title: "【26/1/30追記】iPadとAIだけでiPhoneアプリを作ってみよう！（Claude Code on the webが開発環境の全てを変えてしまった）｜msonrm（なるなる）"
source: "https://note.com/msonrm/n/nb551eb2e2843?after_purchase=true&scrollpos=paywall"
author:
  - "[[msonrm（なるなる）]]"
published: 2025-10-22
created: 2026-02-10
description:
tags:
  - "clippings"
  - "iPad"
---
![見出し画像](https://assets.st-note.com/production/uploads/images/223981327/rectangle_large_type_2_ce888d30ebc7eda8f8b4b304a459b626.png?width=1280)

## 【26/1/30追記】iPadとAIだけでiPhoneアプリを作ってみよう！（Claude Code on the webが開発環境の全てを変えてしまった）

[msonrm（なるなる）](https://note.com/msonrm)

購入済

以前の記事（ [知識ゼロでも大丈夫! AIとiPadではじめるiPhoneアプリ開発](https://note.com/msonrm/n/ndf4ad008086f) ）の置き換えです。こっちのほうがぜんぜん楽。  
  
（2026/1/30追記）  
なんかすごく購入されてるので、嬉しくなってます。ありがとうございます。なので、かなり追記と修正とを加えました！  
基本的にこの記事は「iPadだけでiOSアプリをお手軽に作ろう！」なんですが、末尾にオマケとして「 **ブラウザだけでiOSアプリをお手軽に作ろう！ あ、iPadとかiPhoneは動作確認用くらいね！ピュアSwiftUIだから他より速く安く良くできるよ！** 」なツールへのリンクを追加しました。オマケだけど、かなり使える。CryptoKit + Keychain + Share ExtensionでE2EEするアプリ、みたいな高度なのも作れる。  
作成サンプル↓

[**UnifyTextアプリ - App Store** *App Store でMasao Narumiの「UnifyText」をダウンロード。スクリーンショット、評価とレビュー、* *apps.apple.com*](https://apps.apple.com/jp/app/unifytext/id6756375313)

これはそのAndroid版。iOSとAndroid間でコピペっぽくできます。

[**UnifyText - Apps on Google Play** *Send encrypted text instantly. Easy QR pairing, alerts for su* *play.google.com*](https://play.google.com/store/apps/details?id=app.unifytext.unifytext)

あー、さて、ここから本編です

---

## はじめに

いままではアプリ開発って、プログラミングスキル（Java/JavaScript/Flutter/Swift/とかいろいろ）と、高性能な開発機材（メモリいっぱい積んだMac/PCとか）と、ややこしい環境構築（Xcode/AndroidStudio/VSCodeに必要なSDKやら拡張や入れて設定して随時アップデートして…）が必要だったけれど、先日登場したClaude Code on the web（わかりやすい記事→ [Web版 Claude Code の概要](https://note.com/npaka/n/n946509504d6a) ）が全てを変えてしまった。人間のスキルはAIが代替してくれる。高性能PCは不要、ブラウザさえ動けばいいからお安いiPadでOK。ちょっとした事前の設定をしておけば、あとは自然な言葉でAIにお願いしてテストして、がスムーズに進む。

貧乏人なのでiPadしか持ってないよ、でも有料アプリ作ってちょっとした小遣い稼ぎしたいよ！みたいな動機で始めてみてもいいんじゃないかな。

## 対象読者と、対象じゃない読者

**対象読者** ：作りたいiPhone/iPadアプリの構想はあるけれど、どうしたらいいかわかんないよ、Macとか持ってないし、って人。  
**対象じゃない読者** ：作りたいアプリの構想がない人。

## 用意するもの

- **アプリの構想** ：どういうアプリが作りたいのか、しっかりとした構想がないとAIが困ります。
- **iPad** ：無印iPadでいいです。最新じゃなくても大丈夫。iPad Proとか高性能マシンは必要ない。
- **Claude Proプラン** ：Claude Code on the webはこれ以上のプランじゃないと使えない。月20ドル。
- **Apple Developer Program** ：作ったアプリを全世界に公開できる。年11,800円。登録は今すぐじゃなくても、アプリ開発がうまくいく見込みがついてからでもぜんぜんOK。
- **その他** ：コードを書かないので、外付けキーボードは不要。以下のスクショではiPadですが、Claude Codeはスマホ（iPhoneでもAndroidスマホでも）で扱ったほうが楽。
- あと、GitとGitHubの概要も知っておくと理解が深まる。概要だけで十分、私も詳しくない。

## 大まかな流れ

こんなステップで進みます。1-3は下準備、4-7がメイン、8-10が仕上げ。

1. アプリをインストール（Swift Playground、Working Copy）
2. アカウントを準備（GitHub、Claude Pro）
3. リポジトリ作成
4. Claude Codeでコードを生成、コミット
5. Working CopyでiPadにクローン、ブランチ切り替え
6. Swift Playgroundでテスト
7. Claude Codeで修正しテスト、の繰り返し
8. プルリクエストをマージ
9. Swift Playgroundでアプリ設定し、App Store Connectにアップロード
10. （おまけ）更新履歴をつくろう

難しくないよ！  
じゃあ、ステップごとに解説していきます！

---

ここから先は有料部分です

## ①アプリをインストール（Swift Playground、Working Copy）

iPadは用意しましたか？ じゃあ、App Storeから「 [Swift Playground](https://apps.apple.com/jp/app/swift-playground/id908519492) 」と「 [Working Copy](https://apps.apple.com/jp/app/git-client-working-copy/id896694807) 」をインストールしてください。どちらも無料です。  
Swift Playgroundは、iPhone/iPadのアプリを作ったりプログラミング言語（Swift）の学習ができるアプリ。  
Working Copyはオンライン（GitHub）で管理しているプログラムのコードを管理できるアプリ。iPadにダウンロードしてSwift Playgroundに受け渡す目的で使います。使う機能によっては課金が必要ですが、この記事で紹介する方法は無料枠の範囲内です。

[**Swift Playground** *説明: Swift Playgroundでは、楽しみながらプログラミングを学び、本物のAppを作ることができます。“コ* *apps.apple.com*](https://apps.apple.com/jp/app/swift-playground/id908519492)

[**Git client - Working Copy** *Access Git repositories on the go. Clone, edit, commit and p* *apps.apple.com*](https://apps.apple.com/jp/app/git-client-working-copy/id896694807)

## ②アカウントを準備（GitHub、Claude Pro）

まず開発現場（GitHub）を用意します。Safariとかで [GitHub](https://github.co.jp/) を開き、アカウントを作成しましょう。画面右上の「サインアップ」から進んであれこれしてください。GoogleかAppleのアカウントから進むと楽かも。  
続いてAI（Claude）を使えるようにします。無料だとここでの方法（Claude Code on the web）が使えないし、使える量も少ないので、ちょっとお金がかかるけれど有料（月額20ドル＝約3,000円）のProプランの登録をします。 [Claude](https://claude.ai/) を開き、アカウントを作り、Proプランの登録をしましょう。クレジットカードの登録が必要ですが、メルカード（メルカリの後払いサービス）とかも使えたりします。

## ③リポジトリ作成

GitHub（Git）の「リポジトリ」とは、プログラム/アプリ開発の各プロジェクトのことです（ざっくりすぎる？）。リポジトリの中にコードや変更履歴などを保存して管理します。

GitHubの自分のページの右上、「＋」ボタンからNew repositoryを選択し、Repository name（リポジトリの名前）とDescription（リポジトリの概要）を入力し、Add READMEはオンにし（これしておくと楽→あらかじめmainブランチが作られるから）、Create repositoryボタンを押します。Public（公開）にしておいたほうがあとでちょっとだけ楽ですが、Private（非公開）でもいい。まあお好みで。  
**リポジトリの名前に注意点** がひとつ。この名前がアプリの実体（ファイル名）になるので、Swift Playgroundに認識できる名前（Swift Playgroundアプリ用のプロジェクト形式名）にする必要があります。アルファベットで名前をつけ、末尾に「.swiftpm」とつけましょう。ドットをお忘れなく。  
ここでは仮に「Test.swiftpm」としましょうか。

## ④Claude Codeでコードを生成、コミット

[Claude Code](https://claude.ai/code) を開き、Select repositoryから今作ったリポジトリを選択します。PrivateなリポジトリだとここでGitHubアプリをインストールしないと選択肢に現れないです。ブルタウンリストの一番下にそのへんのことが書いてあるので、タップして、あとは指示されるままにしてください。一瞬で終わります。  
GitHubへのログインを求められたら、ログインして連携を許可してあげてください。環境の選択はDefaultで大丈夫なはず。

いよいよAIによるコード生成です。まずは左上のチャット欄に

> SwiftUIでiOSアプリを開発します。リポジトリをiPadのSwift Playgroundsでプロジェクトとして開いてテストしますので、最低限必要なファイルを作成してください。iOS18以降を対象とし、最新のSwiftUIのベストプラクティスに従ってください。まずはテストUIとして、アプリ画面中央にはOKボタンを配置しましょう。

Claude Code on the webへの最初の指示

と入力し、リターンキーあるいはオレンジボタン押下。AIが色々考えてアプリの基礎を構成するファイルを作ってくれます！

![画像](https://assets.st-note.com/production/uploads/images/224009274/picture_pc_6072660ce62735a75d53a2859a33813a.png?width=1200)

Claude Code on the webの生成結果例

ファイルの作成と、ブランチ（幹に対する脇枝、本流に対する傍流。メインじゃなくってテスト環境、みたいな）への保存まで自動でしてくれます。

## ⑤Working CopyでiPadにクローン、ブランチ切り替え

今作ったファイルは、GitHubというオンライン環境にしか存在しないので、iPadにダウンロード（クローン）する必要があります。

Working Copyアプリを開き、GitHubにログインしてください（アプリの初回起動時にログインを促されたはず）。  
ログインできたら画面左上の指紋みたいなボタンからClone repository→さっき作ったリポジトリ（Test.swiftpm）を選択→右上のCloneボタン押下。これでひとまずiPadにダウンロードできた。  
次に、Claude Codeが作ったブランチに切り替えます。左サイドバーのmainという項目のアイコンをタップして出てくる吹き出しから、さきほどのブランチ（mainの下にある）を選択しましょう。すると、さっき作ったファイル（ContentView.swift等）がサイドバーに確認できると思います。これで、AIが作ったファイルがiPadにダウンロードできました。

## ⑥Swift Playgroundでテスト

では、今ダウンロードしたファイルを実際にSwift Playgroundで動かしてみましょう。

Swift Playgroundを起動し、画面下半分のファイル選択画面サイドバーからWorking Copyを選択します（もしなければサイドバー上の「…」から「サイドバーを編集」でWorking Copyをオンに）。すると、Test.swiftpmがありますね。これがAIが作ったファイルを取りまとめたパッケージです。タップして開きましょう。  
Claude Codeが正しくファイルを作ってくれてたら、ちゃんとしたアプリとして開けます。ダメだと右上に赤いバツ印のアイコンが表示され、タップでエラー内容が確認できます。  
さて、どうでしょうか？

![画像](https://assets.st-note.com/production/uploads/images/224014232/picture_pc_567d96e6605ca40f031bbf48685dc5df.png?width=1200)

Swift Playgroundのエラー表示

私のテストでは、うん、だめでした。AIに修正を依頼しましょう。

## ⑦Claude Codeで修正しテスト、の繰り返し

先ほどのエラー内容をそのままClaude Codeに投げます。  
エラー表示のスクショを撮り、右上のテキストアイコン押下で画像上のテキストが選択できるのでエラー内容をコピーし、Claude Codeに貼り付けて「こんなエラーが出ました」と伝えてみます。  
もし、開発はiPad、Claude Code操作はスマホ、としているのであれば、Googleレンズを使ったほうが楽です。iPad画面をスマホでスキャン→テキストを画面でコピー→Claude Codeに貼り付け。

![画像](https://assets.st-note.com/production/uploads/images/224015534/picture_pc_12db6afb2803fa6d3ddad57b92b7ebd4.png?width=1200)

スクリーンショットから文字列を選択してコピー

Claude Codeの右下欄にエラーメッセージをペーストしてリターンキー押下。あ、チャット欄で改行したいときはシフトキー＆リターンキーね。  
「こんなエラーで開けませんでした。」と冒頭に添えても良いですが、メッセージだけで意図は伝わります。

![画像](https://assets.st-note.com/production/uploads/images/224016314/picture_pc_76262e0d3f5be2595fc6971a008f110f.png?width=1200)

Claude Codeがエラーを確認して修正してくれる

これで修正されたはず。iPad側も更新してもう一度テストしましょう。  
Working Copyの左サイドバーを下に引っ張って離すと、最新情報に更新されます。緑色の部分をタップするとダウンロードしたものが上書き（マージ）されます。

![画像](https://assets.st-note.com/production/uploads/images/224017232/picture_pc_33faa6badfe279eeb7081cd8ecd807ce.png?width=1200)

Working Copyで、リポジトリに更新があった時の表示

Swift Playground左上の戻るアイコンからファイル選択に戻り、ふたたびTest.swiftpmを開いてみましょう。エラーがなければ、右上のアイコン（四角が重なってる）をタップするとアプリのプレビューができるはずです！

![画像](https://assets.st-note.com/production/uploads/images/224018365/picture_pc_25b05b736335f63f4eaa7cfb7982b9d5.png?width=1200)

Swift Playgroundでのアプリプレビュー

1回でうまくいかなくても、次にはうまくいくはず。エラーメッセージをClaude Codeに伝える→Working Copyを更新→Swift Playgroundで開きなおす、のパターンです。  
アプリ画面がプレビューできたら、アプリの基礎が完成したってことです！

さあ、 **ここからが本番** ですよ。Claude Codeにうまくいったことを報告し、いよいよ、作りたいアプリの概要を伝えてみましょう。できるだけ具体的に。

> アプリの構成を変えます。画面下部の「ダイスを振る」ボタンを押したら、1から6までの数字をランダムに画面中央に表示させ、2回目以降の押下では画面中央の数字表示の上に前回以前の数字の履歴を縦に並べて表示させます。上に行くほど数字は薄くなります。

アプリサンプル①

![画像](https://assets.st-note.com/production/uploads/images/224021950/picture_pc_83fe21a101ef08101e1c6ab6b965e6e1.png?width=1200)

アプリサンプル①のテスト画面

> こんなアプリにしてください：いわゆるポモドーロ・テクニック用のタイマーです。画面中央に大きくドーナツ上のグラフを描き、時間経過を表示します。画面下部に「開始」ボタンを置き、押下するとセッション数を尋ねるダイアログが出現し、そこから1セッションから5セッションまで選択できるようにします。1セッションは25分の作業時間と5分の休憩で構成されています。各経過時間が中央のグラフで確認できるようにしましょう。

アプリサンプル②

![画像](https://assets.st-note.com/production/uploads/images/224023704/picture_pc_b9c80e694f2ed3f0ffadc74e45ad5605.png?width=1200)

アプリサンプル②のテスト画面

あなたが満足するまで機能追加や改善を指示し、更新し、テストしていってください。  
このへんのコツは↓を参照してね。

コツの要点は「 **曖昧なままにしない** 」です。「疑問点あったら聞いてね」「実装前に実装計画を教えてね」「いまのやり方を詳しく教えて」「こうしたいけど、メリットとデメリットを教えて」……。あなたがいつも人になんか頼むときの姿勢そのもの、みたいじゃありませんか？  
あと、ある程度できたら、いったん捨てたほうがいい。試行錯誤がコード内に積もり積もってるから、クリアにするべき。「ソースコード全体を精査し、リファクタリングしてください。ファイル名、関数名、変数名などを機能に即して適切に変えてください。」って頼むか、「いまの機能をすべてSPEC.mdに整理して残してください。コードを全部消して、SPEC.mdに基づき作り直してください」としたほうがぜんぜん良くなります。ほんとだよ！

## ⑧プルリクエストをマージ

これでいいかな、となったら、いよいよ本採用しましょう。Claude Codeの右下、チャット欄の上に「Create PR」とあります。これが、いままでブランチで行っていた試行錯誤を正式採用として提案する（プルリクエスト）ためのものです。押下するとGitHubのプルリクエストの画面に切り替わります。必要な情報（タイトルとか更新内容）がすでに入力されているので、修正がなければそのまま緑の「Create pull request」ボタンを押しましょう。プルリクエストが提案され、あとはそれを承認してメインに取り込むだけです。自動チェックが終わったら「Merge pull request」ボタンを押しましょう。これで、メインのブランチにClaude Codeが作ったコードが正式採用されました！

なお、プルリクエストをマージした後にさらにClaude Codeで更新した場合は、Working Copyでダウンロードしたリポジトリを削除してから次に進んだ方がスムーズです。Working Copyの左上の戻るボタンからリポジトリの一覧に戻り、削除したいリポジトリを長押ししてdelete。ふたたびリポジトリをダウンロード→ブランチ切り替え、です。  

![画像](https://assets.st-note.com/production/uploads/images/224038302/picture_pc_a9b37bf75c1c7cebe56cef4fb092ab85.png?width=1200)

Working Copyでダウンロードしたリポジトリを削除

## ⑨Swift Playgroundでアプリ設定し、App Store Connectにアップロード

「これでいいかな」「ひとまず満足」となったら、いよいよApp Storeに公開、ですね。Apple Developer Programの登録（有料）が必要となります。  
Swift Playgroundで開き、左サイドバーのアプリ設定から各種設定をし、「App Store Connectにアップロード」で、実機でのテストやApp Storeへの審査提出ができます。  
ですが、ここから先は詳しく説明しません。各自で調べてみてね（長くなるから）。

## （おまけ）更新履歴をつくろう

これはやらなくてもいいんですけど、アプリの更新履歴を作っておくと良いですよ。Claude Codeに

> ここまでの更新を簡単にまとめて、CHANGELOG.mdに追記してください。

Claude Codeへの更新履歴追記の指示

って伝えるだけです。次の日に再開するときは「CHANGELOG.mdを読んで、次にやることを考えてください」って伝えるとお互いスムーズです。  
おまけとして、がんばった証が残るので達成感や自己肯定感が得られます。たぶん。

---

## おわりに

さらに高度なアプリを作りたくなったら？  
共有メニューに追加したい、顔認識させたい、標準の暗号化機能を使いたい、ダイナミックアイランドに通知を出したい、ウィジェットを作りたい……。  
普通なら「Mac実機買ってXcodeだね！10万円追加！」ってなりますが、私、貧乏なので、お金ではなく頭をつかいました。これです↓

これを使うと、iPadだけで（というかブラウザだけで）ピュアSwiftUIなiOSアプリが作れます。まあ、似たのではExpoとかReact NativeとかMonacaとかあるんだけど、間にいろいろかましてるからパフォーマンスや見た目が悪いし、最新技術が使えなかったりする。その点、↑のはピュアSwiftUIをオンラインMacで作るので速い安い良くできる。くわしくは中を覗いて、生成AIに聞いてね。お試しあれ。

---

あと、作ったアプリ「 [Geomancy Diary](https://apps.apple.com/jp/app/geomancy-diary/id6670341755) 」の紹介でもしようかな。ジオマンシーっていうマイナーだけど的確な答えが返ってくる占いがありまして、そのiPhone/iPadアプリを作りました。

[**Geomancy Diary** *毎日の出来事をただ記録するだけでなく、古くからの占いを使って自分自身をより深く理解してみませんか？ 『Geomancy* *apps.apple.com*](https://apps.apple.com/jp/app/geomancy-diary/id6670341755)

2024年9月に初公開した時には、有料アプリランキングで5位だったりしました。その後も、有料アプリのライフスタイル部門で常に100-150位前後には入っています。変動があるので、月に1回は10位以内に入ります。ありがとうございます。

このアプリの分析レポートはこちら。

その他のアプリはこちら。ほぼAI補助開発だけど、ブロック言語とかコード手書きのもあります。

感想やコメント、改善提案などあればぜひ。

## 高評価して応援しよう！

メンバーシップなら都度購入するよりもお得です

私、好奇心と向学心で行動してます。作ったもの、考えてること、思ったことをここで開放します！[このメンバーシップの詳細](https://note.com/msonrm/membership/join)

【26/1/30追記】iPadとAIだけでiPhoneアプリを作ってみよう！（Claude Code on the webが開発環境の全てを変えてしまった）｜msonrm（なるなる）
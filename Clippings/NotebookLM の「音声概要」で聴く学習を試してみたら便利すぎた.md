---
title: NotebookLM の「音声概要」で聴く学習を試してみたら便利すぎた
source: https://blog.g-gen.co.jp/entry/notebooklm-audio-overviews
author:
  - "[[ggen-kawamuramari]]"
  - "[[(記事一覧)]]"
published: 2025-05-27
created: 2025-07-13
description: 
tags:
  - clippings
  - LLM
---
G-gen の川村です。この記事では **NotebookLM** の **音声概要** 機能にフォーカスした活用方法を解説します。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250515/20250515201646.png)

## NotebookLM とは

**NotebookLM** とは、Google ドキュメント、PDF、音声、YouTube 動画などをソースとして指定し、その情報を基に要約・FAQ・メモを生成できる Google 提供の AI ノートサービスです。

一般的な生成 AI チャットアプリと異なり、回答の出典をユーザーが明示的に制御できるため、業務利用において高い信頼性が確保されます。

無償版で利用できる NotebookLM、有償版の NotebookLM in Pro、より企業向けの機能を強化した NotebookLM Enterprise があり、それぞれの機能の違いや活用ユースケースについては以下の記事を参照してください。

[blog.g-gen.co.jp](https://blog.g-gen.co.jp/entry/difference-between-notebooklm-free-pro-enterprise)

## 音声概要とは

NotebookLM の **音声概要** （Audio Overviews）とは、指定したソースに基づいて、 AI が2人の人間の自然な対話形式で内容を要約・解説する機能です。

2025年4月末から日本語を含む 50 以上の言語に対応し、日本語でも実用的なレベルで利用できるようになりました。Google 公式の紹介動画でも AI 生成と思えないような流暢な会話であることが確認できます。

![](https://www.youtube.com/watch?v=VJg37fVPy9I)[youtu.be](https://youtu.be/VJg37fVPy9I?si=G4SwUipmaBUZWf9i&t=31)

なお、利用回数制限は以下のとおりです。

- NotebookLM: 3回/日
- NotebookLM in Pro: 20回/日

参考: [NotebookLM の Pro 機能の詳細](https://support.google.com/notebooklm/answer/16206866?hl=ja)  
参考: [NotebookLM を Pro プランにアップグレードする](https://support.google.com/notebooklm/answer/16213268?hl=ja)

## 事前準備

## 言語設定

まず、NotebookLM の出力される言語設定を行います。

\[ 設定 \] 画面から\[ 言語設定 \]を選択します。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090855.png)

Google アカウントの言語設定がデフォルトで設定されていますが、明示的に \[日本語\] を選択できます。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090837.png)

## ソースの追加

続いて、NotebookLM に対象となるソースを追加します。

\[ソース\] からデータソースを追加後、\[Studio\] パネルの \[音声概要\] セクションの \[生成\] ボタンをクリックすると、音声概要が生成されます。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090834.png)

- 参照: [ソース](https://support.google.com/notebooklm/answer/14276468?hl=ja)

## 音声概要の使い方

## 音声概要の生成

今回は Google Cloud 資格の過去問題をまとめた資料（Google ドキュメント）をソースとして指定した例です。

\[音声概要\] セクションの \[生成\] ボタンを押すと、音声概要が生成されます。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090840.png)

生成には、数分かかります。生成完了後に再生ボタンを押すと、対話式の音声が再生されます。

実際に生成された音声はこちらです。

![](https://www.youtube.com/watch?v=nY4zqcuDHD4)[www.youtube.com](https://www.youtube.com/watch?v=nY4zqcuDHD4)

- 「試験のポイントとか、実践的な知識をギュッと抽出するのが目標です」
- 「〜っていうのはもう必須の知識ですよね」
- 「最後に 1 つだけあなたにも考えてみて欲しいことがあるんです」

このように対話には AI ホストによるソースの解釈に基づいて自然な相槌やコメント、さらには聞き手に対する問いかけもあります。まさにラジオ感覚で情報を耳から受け取りやすくなり内容の整理にも役立ちます。

## カスタマイズ機能

\[カスタマイズ\] ボタンをクリックすると、トピックや話し方のスタイルを指定できます。最大 500 文字まで入力可能です。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090843.png) ![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090846.png)

聞きたい内容やスタイルに沿ったラジオ番組のような音声を生成するために、以下のような具体的な指示を入力します。

入力例:

> 「VPC & Network Security」項目の内容を重点的に、且つ IT 初心者にもわかりやすい解説にして

![](https://www.youtube.com/watch?v=JkBwzvWS60E)[www.youtube.com](https://www.youtube.com/watch?v=JkBwzvWS60E)

- 「特に Network Security のところをちょっと深掘りしてみようかなと」
- 「ファイアーウォールはネットワークの門番みたいなものです」
- 「これ単なる『ログ』っていうよりは、ネットワークの「健康診断の記録」みたいなものですね」

先程生成した網羅的な音声と比べると、よりユーザーの意図（特定トピックに絞った内容且つ、 IT 初心者に向けの解説）に沿った音声概要が生成されます。

## 音声概要のダウンロード

生成された音声は三点リーダーをクリックすると表示されるプルダウンメニューからダウンロードできます。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090858.png)

音声ファイルはスマートフォンで再生したり、NotebookLM のソースとして再アップロードすることで、要約・メモに再利用することも可能です。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090849.png)

## インタラクティブモード（ベータ版）

2025年5月現在は英語版のみでの提供となりますが、再生中にユーザーが AI ホストに質問できる **インタラクティブモード** も試験提供されています。

再生中に「参加」ボタンを押すと AI ホストから声がかかり、アップロードされたソースに基づいて回答が得られます。質問への回答後、元の音声概要の再生が再開されます。（ユーザーの声ややりとりは保存されません）

公式動画での利用イメージは以下となります。

![](https://www.youtube.com/watch?v=SE753Tm913s)[www.youtube.com](https://www.youtube.com/watch?v=SE753Tm913s&t)

- 参考: [音声概要](https://support.google.com/notebooklm/answer/15731776?hl=ja)

## 活用シーン

## 1\. 通勤・移動中の情報収集を効率化

移動中や作業をしながら、耳で情報をインプットすることで効率的に学習や情報収集ができます。

- ニュース記事やブログ記事、会議の議事録などを音声概要化し、移動時間や作業中も情報収集に充てる
- ダウンロードした音声ファイルでオフライン環境や、端末（パソコンやスマートフォンなど）を選ばず再生可能
- NotebookLM モバイルアプリから、いつでもどこでも学習を開始 ※ 5月20日リリース
- 参照: [Google launches official NotebookLM mobile app](https://blog.google/technology/ai/notebooklm-app/)

## 2\. 目的別に学習を最適化

**カスタマイズ機能** で、解説してほしい内容や焦点を当てるべきトピックを指定し学習を効率化します。

- 目的に合わせて学習トピックを絞り学習を効率化
- 以下のような指示で音声の内容・口調を調整し理解を深める
	- 「セキュリティに関する側面を解説して」
	- 「小学生にもわかるように説明して」
	- 「合格までのステップを 5 つ以内で簡潔に解説して」

## 3\. 複雑な資料の理解を促進

難解で複雑な内容の資料（研究論文、専門記事、長文レポートなど）も音声概要を利用することで、手軽且つ効率的に理解を深めることができます。視覚情報よりも聴覚情報の方が頭に入りやすいと感じる方にも有効です。

- 膨大な資料（300 ページの書籍 PDF など）を深く読み込む前に、音声で概要を掴み情報整理を支援
- 視覚（テキスト）では難解な内容を、聴覚（AI ホストの対話形式）で情報の背景や文脈をストーリーとして理解促進

## 4\. 参加型の対話モードでリアルタイムに情報整理

2025年5月現在、英語のみでの提供ですが、インタラクティブモードを利用することで、ソースに対する AI ホストとの会話に参加できます。

- 再生中、疑問点が浮かんだ際にその場で解消
- 対話を通じて理解を深め、発想の幅を広げる

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090902.png)

## 5\. 多言語学習

50 を超える言語に対応しているため、多言語の学習にも大いに役立ちます。英語やフランス語など、さまざまな言語学習を効率的に行えます。出力言語の言語設定をすることで、任意の言語での生成を行うことができます。

- 英語で音声概要を生成・ダウンロードし、リスニング力を高める
- インタラクティブモードで AI ホストと対話し、スピーキング力を高める
- 生成した英語の音声ファイルをソースとして追加・テキスト化して、シャドーイングや単語学習に利用

**プロンプト例**

> この音声をセリフごとに分割し、それぞれの英語文と日本語訳を表で一覧化してください。

![](https://cdn-ak.f.st-hatena.com/images/fotolife/g/ggen-sugimura/20250527/20250527090852.png)

## 注意点

音声概要機能は便利ですが、以下の点にご注意ください。

- 利用回数制限あり（無償版は 1日3回、NotebookLM in Pro は1日20回まで）
- 漢字の誤読あり（ふりがなや指示で回避可能）
- 自動生成のため誤情報を含む可能性あり（ソースに基づいた生成のためハルシネーションが起こりにくいが、ファクトチェック推奨）
- 生成中はブラウザを閉じない事を推奨（生成に時間がかかる）
- 削除・再生成した音声は再生不可（必要であればダウンロード推奨）
- インタラクティブモードは現状英語のみ対応
- 現状日本語音声は10分弱となり、長編音声は未対応（英語のみ 30 分以上対応）

なお、今後のアップデートにより上記内容は改善される可能性があります。

[« Googleドライブの「やってはいけない」。…](https://blog.g-gen.co.jp/entry/restrict-public-acccess-for-google-drive) [NotebookLM vs Gemini アプリ:業務で使い… »](https://blog.g-gen.co.jp/entry/notebooklm-use-cases)
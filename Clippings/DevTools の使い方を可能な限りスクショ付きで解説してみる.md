---
title: "DevTools の使い方を可能な限りスクショ付きで解説してみる"
source: "https://zenn.dev/mizchi/scraps/c72e6a55deca18"
author:
  - "[[Zenn]]"
published: 2025/02/22にコメント追加
created: 2025-11-16
description:
tags:
  - "clippings"
---
以下の公開計測会でやったものを個別に解説してみる。

<iframe src="https://www.youtube-nocookie.com/embed/j0MtGpJX81E" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe>

細かいテクニックが多いのだが、それを可能な限りテキストとスクショで解説したい。使い方の解説が中心で、どういう意味があるかは解説しない。

Chrome131時点のスクリーンショットで、後で読む場合は頻繁にUIが変わっている点に注意。大事なのは意図。

宣伝: これを御社のサイトで解説する仕事をやっています。

デモのURL

これに意味はなく、今日偶然見ていただけで意図はない。関係ないがエッジランナーズは最高のアニメ。

## DevTools を開く

F12 or 右クリックから「検証」

![](https://storage.googleapis.com/zenn-user-upload/4d6ebb16d774-20241203.png)

## DevTools > Lighthouse

この状態で計測

![](https://storage.googleapis.com/zenn-user-upload/827967492095-20241203.png)

このとき、新しいプロファイルを作ったりして、可能な限り Chrome拡張が入ってない状態にすること。Chrome拡張による処理も計測に含まれてしまう。

## Lighthouse レポートの読み方

点数部分にマウスオーバーすると、内訳が見える

![](https://storage.googleapis.com/zenn-user-upload/48585ad38ccc-20241203.png)

See Calculator をクリックすると、Google側の現在のスコアの重みがわかる  
![](https://storage.googleapis.com/zenn-user-upload/d140631a4a3c-20241203.png)

View Treemap で簡易なJSチャンクのサイズ比率と、実行された行のカバレッジが見える。

![](https://storage.googleapis.com/zenn-user-upload/3c6e9d6cb9db-20241203.png)

![](https://storage.googleapis.com/zenn-user-upload/b5ee272e9bda-20241203.png)

## Lighthouse 計測環境の再現の仕方

レポート末尾に設定がある。この状態に合わせると再現できる

![](https://storage.googleapis.com/zenn-user-upload/6e898ba5f7eb-20241203.png)

## Lighthouse Dignosticsの読み方

上からスコア影響が大きいものが並んでいる。Show audits relevant to... で絞り込める

![](https://storage.googleapis.com/zenn-user-upload/7817acc82ad0-20241203.png)

クリックすると詳細が見える。これはLCPがいつ確定したかのレポート（大事）

![](https://storage.googleapis.com/zenn-user-upload/baca7bea3928-20241203.png)

## 複数のLighthouseレポートを比較

- で追加できる。

![](https://storage.googleapis.com/zenn-user-upload/c91c28c7db4d-20241203.png)

## DevTools > Performance

読み込み時間を取りたい場合、 Record ではなく Record and Reload を押す。  
この時、CPUやNetwork を低速化して、Lighthouse計測環境に合わせることができる

![](https://storage.googleapis.com/zenn-user-upload/9e7070f2ce88-20241203.png)

計測するとこうなる

![](https://storage.googleapis.com/zenn-user-upload/8da91340fd34-20241203.png)

大事なのは Network と Main(Thread)

### マウスホバーしてレンダリング状態を確認

そのタイムラインではどういう状態だったか、ここのマウスオーバーで確認できる

![](https://storage.googleapis.com/zenn-user-upload/76179f9adca2-20241203.png)

### Network

Network をクリックして展開する。LCP タイミングを意識しながらウォーターフォール図をみる。  
![](https://storage.googleapis.com/zenn-user-upload/d8a60fd2f7ae-20241203.png)

マウスドラッグで移動できる

範囲指定のボタンをドラッグすると、詳細な区間を絞り込むことが出来る

![](https://storage.googleapis.com/zenn-user-upload/c76dc784eadf-20241203.png)

区間はマウスホイールでも操作できる。

右上に赤いオーバーレイ表示があるのはレンダーブロッキングコンテンツで、順序指定があり他の読み込みを止める可能性がある。

マウスホバーでリクエストの状態がわかる。たとえばこれは画像が初期表示に含まれることがわかって、画像の読み込みプライオリティが Low -> High に上がっているところ。  
![](https://storage.googleapis.com/zenn-user-upload/6fb761f795bf-20241203.png)

各リクエストは右クリックして Networkの詳細に飛ぶこともできる。  
![](https://storage.googleapis.com/zenn-user-upload/2949b81befe1-20241203.png)

### Main

主に CPU で行われている=(ユーザー操作に割り込む)操作。

![](https://storage.googleapis.com/zenn-user-upload/96440acd213c-20241203.png)

赤いロングタスクがフレームに割り込んでる超過している部分になる。

ドラッグや範囲操作はNetworkと同じ。

タスクをクリックすると、下のタブで詳細がみえる。

![](https://storage.googleapis.com/zenn-user-upload/8b8180117c05-20241203.png)

下のタブから Bottom Up を選ぶとそのコールスタックの内訳がみえる。

![](https://storage.googleapis.com/zenn-user-upload/25eb6e16d25a-20241203.png)

## Source でリクエストを書き換える

準備として、 DevTools > Source > Overrides で `+ Select folder to overrides` を選択

![](https://storage.googleapis.com/zenn-user-upload/8f212c3ea014-20241203.png)

なんでもいいので、適当なディレクトリを作って(新規作成して)選択する

![](https://storage.googleapis.com/zenn-user-upload/eefde0a64974-20241203.png)

Chrome でこのポップアップが出るので許可する。

![](https://storage.googleapis.com/zenn-user-upload/d1346d2b7ec3-20241203.png)

キャッシュを保存するディレクトリができた。ここで Enable Local Overrides しておく。

![](https://storage.googleapis.com/zenn-user-upload/edffbc20b8b2-20241203.png)

ここまでやってから、ネットワークタブから右クリックして Override Content

![](https://storage.googleapis.com/zenn-user-upload/4ec53891080f-20241203.png)

ここでプレビューが編集可能になる。ここを書き換えると、そのリクエスト対象の内容を書き換えることができる。  
![](https://storage.googleapis.com/zenn-user-upload/ec17c6225c9c-20241203.png)

これは Lighthouse の計測時や再ロードで反映される。

書き換えたものは紫でマークが付く。

![](https://storage.googleapis.com/zenn-user-upload/71cbfba2f36f-20241203.png)

書き換えた内容は、強制的に HTTP1.1 扱いになるので注意。HTTP/2のストリーム処理にならずに、点が悪化したことがある。

ログインするとコメントできます
---
title: "Kaggle Expertになるまで勉強したことを全て書く"
source: "https://qiita.com/Yuki_Kaggler/items/8ffe2ffa6f020e09cfd3"
author:
  - "[[Yuki_Kaggler]]"
published: 2021-06-21
created: 2025-06-24
description:
tags:
  - "clippings"
---
![](https://relay-dsp.ad-m.asia/dmp/sync/bizmatrix?pid=c3ed207b574cf11376&d=x18o8hduaj&uid=)

## Qiitaにログインして、便利な機能を使ってみませんか？

[ログイン](https://qiita.com/login?callback_action=login_or_signup&redirect_to=%2FYuki_Kaggler%2Fitems%2F8ffe2ffa6f020e09cfd3&realm=qiita) [新規登録](https://qiita.com/signup?callback_action=login_or_signup&redirect_to=%2FYuki_Kaggler%2Fitems%2F8ffe2ffa6f020e09cfd3&realm=qiita)

この記事は最終更新日から3年以上が経過しています。

## はじめに

こんにちは。Yuki | Kagglerです！ 先日、Shopeeコンペの順位が確定して銀メダルをいただき、晴れてCompetition Expertになることができました。区切りがいいのでここまで取り組んできたことをまとめてみました。  
  
※ 6/28追記：Amazonのリンクが切れていたので貼り直しました！  

  

## この記事の対象者

- Kaggleをやってみたいが、何から始めればいいかわからない方
- 機械学習の勉強をしてみたいが、何から始めればいいかわからない方
- 機械学習の勉強をしているが、なかなか本屋に行けず、どの本を買えばいいかわからない方
- Kaggleを頑張っているが、中々上位にいけなかったり、最後まで走りきれずに悩んでいる方

上記にきれいに当てはまらなくても、何か参考になることがあるかもしれません！！  

## 目次

- [1.自己紹介](https://qiita.com/Yuki_Kaggler/items/#1-%E8%87%AA%E5%B7%B1%E7%B4%B9%E4%BB%8B)
- [2.注意事項](https://qiita.com/Yuki_Kaggler/items/#2-%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A0%85)
- [3.実際に書いていく](https://qiita.com/Yuki_Kaggler/items/#3-%E5%AE%9F%E9%9A%9B%E3%81%AB%E6%9B%B8%E3%81%84%E3%81%A6%E3%81%84%E3%81%8F)
- [4.まとめ](https://qiita.com/Yuki_Kaggler/items/#4-%E3%81%BE%E3%81%A8%E3%82%81)
- [5.今後の目標](https://qiita.com/Yuki_Kaggler/items/#5-%E4%BB%8A%E5%BE%8C%E3%81%AE%E7%9B%AE%E6%A8%99)

## 1\. 自己紹介

TwitterでYuki | Kagglerという名で活動している、東京大学理科一類2年生です。学部・学科は工学部物理工学科に進学予定で、量子機械学習を研究したいと考えています。元々は機械学習を学びたくて、色々なデータに触れて機械学習に対する興味を絞るためにKaggleを始めました。(と言いつつ最近は専ら画像コンペに出てます。)  

## 2\. 注意事項

この記事はあくまで僕がExpertになるまでにしたことを書いた記事であり、 **こうすればExpertになれる、といった類のものではありません** 。また、数学に関しては大学の授業に合わせて教科書で学んだため、機械学習を勉強するために学んだとは言い難いと判断して詳細は省きます。また、アフィリエイトは一切使っていません。  

## 3\. 実際に書いていく

基本的には1ヶ月単位で学んだこと、その時感じたことを書いていきます。  

### 勉強開始前(~2020年3月)

受験が終わったのでとりあえず線型代数を勉強し始めました。この時点では微積・統計の知識は高校生レベルで、線型代数は何も知りませんでした。ちなみに、僕の世代は行列は高校生では習わず、しかも統計も2Bの範囲は無しで受験できたのでせいぜい相関係数は知ってるよレベルです。正規分布なんて聞いたこともありませんでした。もちろんプログラミングはほとんどやったことがなく、ターミナルなんて触ったこともありません。本当に0からのスタートです。  

### 4月

- **「スッキリわかる Python入門」**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660274-431d1100-d1bb-11eb-8e0a-597732ce0c5b.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660274-431d1100-d1bb-11eb-8e0a-597732ce0c5b.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=0302d3a92e5a0ec8b437744464d8ad47)  
	この本でPythonを勉強し始めました。これ以上はないぐらい親切な内容で、1冊目として選んでよかったと感じています。  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/%E3%82%B9%E3%83%83%E3%82%AD%E3%83%AA%E3%82%8F%E3%81%8B%E3%82%8BPython%E5%85%A5%E9%96%80-%E3%82%B9%E3%83%83%E3%82%AD%E3%83%AA%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA-%E5%9B%BD%E6%9C%AC%E5%A4%A7%E6%82%9F/dp/4295006327)
- **Udemyの「実践Pythonデータサイエンス」講座**  
	  
	ここでnumpy, pandas, matplotlib, seabornなどを一通り学びましたが、はっきり言ってあまりわかってはいませんでした。udemyの講座に関してはもっといい講座に出会えたので後に書きます。最後の機械学習のパートを楽しみにしていたものの、そのパートが全くわからず途方に暮れて手を出したのが次の本です。  
	[リンクはこちら](https://www.udemy.com/course/python-jp/)
- **「Pythonではじめる機械学習」**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660301-65af2a00-d1bb-11eb-80f5-b36da93b0cb7.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660301-65af2a00-d1bb-11eb-80f5-b36da93b0cb7.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=3c7274bd0a4267883886426e3e08ca87)  
	あっという間に挫折しました。教師あり学習、教師なし学習、特徴量エンジニアリング、モデルの評価、テキストデータの処理などが網羅的に解説されている一冊です。機械学習そのものに関する内容ももちろん豊富ですが、scikit-learnの使い方の解説という趣も割と強かったと感じています。前述の講座であまりnumpyやmatplotlibがわからなかった上に、機械学習そのものも何も知らないという状況だったので、言ってることもコードもわからない箇所が多くて辛かったです。また、日本語が若干不自然なところが割と多く、不自然な日本語を頭の中で補正ができなかったことも、今振り返れば致命的なポイントでした。  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/Python%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92-%E2%80%95scikit-learn%E3%81%A7%E5%AD%A6%E3%81%B6%E7%89%B9%E5%BE%B4%E9%87%8F%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%A8%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%81%AE%E5%9F%BA%E7%A4%8E-Andreas-C-Muller/dp/4873117984/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=Python%E3%81%A7%E5%A7%8B%E3%82%81%E3%82%8B%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92&qid=1624889616&sr=8-1)

### 5月

- **courseraの「Machine Learning」**
[![スクリーンショット 2021-06-20 12 27 40](https://user-images.githubusercontent.com/70050531/122661233-ed4c6700-d1c2-11eb-9bfa-b74e892d297f.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122661233-ed4c6700-d1c2-11eb-9bfa-b74e892d297f.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=20a581ffabb4bc1c2301cd2b5b97550a) 腰を据えて機械学習を勉強しなければいけないと感じて受講しました。3ヶ月のコースでしたが、覚悟を決めて約10日で全て完了させました。機械学習について、初学者にもわかりやすく網羅的に解説されています。「Pythonではじめる機械学習」よりもっと詳しいので、本当の初心者でも最後までやっていけます。コーディング課題があるので知識が定着しやすいのもいいところです。courseraには有料の講座も多いですが、この講座は無料なのも嬉しいポイントです。全部英語でしたが、受験で英語はかなりやり込んだのもあり、だんだん慣れてきて後半は課題も全て翻訳なしで乗り切ることができました。英語が苦手でも、動画には日本語字幕をつけられますし、課題もDeeplに突っ込めばなんとかなると思うので、思い切って受講をしてしまうのがオススメです。この講座は本当に有名で、ネットにも解説記事が大量にあるので、困ったらそれらを活用するのも手ですね。使われている言語がPythonではなくoctave(またはMatlab)なのが少しネックではあります。ここが自分の中で大きな転換点になり、その後の勉強がうまくいったのでこれは本当にオススメです。 \[リンクはこちら\](https://ja.coursera.org/learn/machine-learning)  
- **「ゼロから作る Deep Learning」(以下ゼロつくと略記)**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122659996-55e21680-d1b8-11eb-903a-646ec379acb5.jpg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122659996-55e21680-d1b8-11eb-903a-646ec379acb5.jpg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=1968417395a3ec93874a80ca24a0d73d)  
	courseraで学ぶ中で深層学習が面白そうと感じて読みました。パーセプトロンから始まり、多層パーセプトロン、誤差逆伝播法、SGDやAdamといった最適化手法、CNNと豊富な内容で構成されています。この本は著者が日本人であることもあり、解説が非常にわかりやすくて日本語にも詰まることなく読めました。コードに関する説明も非常に詳しいので、Pythonに不安がある人でも十分読み切れると感じています。この本で深層学習(特にCNN)に感動して、この分野に人生をかけていいのではないかと思えたからこそ今があるので、僕の中で最高の一冊です。迷っている方はぜひ手に取ることを勧めます。  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/%E3%82%BC%E3%83%AD%E3%81%8B%E3%82%89%E4%BD%9C%E3%82%8BDeep-Learning-%E2%80%95Python%E3%81%A7%E5%AD%A6%E3%81%B6%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0%E3%81%AE%E7%90%86%E8%AB%96%E3%81%A8%E5%AE%9F%E8%A3%85-%E6%96%8E%E8%97%A4-%E5%BA%B7%E6%AF%85/dp/4873117585/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=%E3%82%BC%E3%83%AD%E3%81%8B%E3%82%89%E4%BD%9C%E3%82%8B&qid=1624889653&sr=8-1)
- **「Pythonで始める機械学習」**  
	  
	前回挫折したリベンジをしました。読み切れた理由としては、機械学習に強くなったお陰で違和感のある日本語に悩まされなくなった、ゼロつくを読むうちにコーディング力が上がっていた、などが挙げられます。  
	  
	中途半端にしか読んでいないので大きくは取り上げませんが、似た本に「Python 機械学習プログラミング」という本があります。この本の方が若干難易度は上がって数学力も求められますが、courseraの説明との親和性が高くてより詳しいので、こちらにチャレンジしてもいいかもしれないです。前半はDeepじゃない機械学習について、後半は深層学習がTensor Flowを用いて解説されています。僕は前半を読みながらコーディングしましたが、非常に勉強になりました。  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660324-91caab00-d1bb-11eb-9b01-83f0adf593c2.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660324-91caab00-d1bb-11eb-9b01-83f0adf593c2.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=158e60f22623b539c51872b715615ebe)  
	[Amazonのリンクはこちら](https://qiita.com/Yuki_Kaggler/items/www.amazon.co.jp/dp/4295010073)

### 6月

- **「ゼロから作る Deep Learning 2」**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660007-73af7b80-d1b8-11eb-8266-b211b1597d80.jpg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660007-73af7b80-d1b8-11eb-8266-b211b1597d80.jpg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=d6cb133250bfb9e26ec86891cad4ae23)  
	ゼロから作るDeep Learningの続編で、自然言語処理編です。前作の復習から始まり、word2vec、シンプルなRNN、LSTM、LSTMを用いたSeq2Seq、Attentionなどがフルスクラッチで作り上げられています。こちらの方が量が多くて難易度も上がっており、前作ほどスラスラとはいきませんでした。しかし説明は非常にわかりやすく力がつくので、ゼロつく1を読み終えた方、深層学習での自然言語処理に興味がある方は是非手に取ってみてください。(全然関係ありませんが、帯の言葉が大好きです。痺れますね〜)  
	  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/%E3%82%BC%E3%83%AD%E3%81%8B%E3%82%89%E4%BD%9C%E3%82%8BDeep-Learning-%E2%80%95Python%E3%81%A7%E5%AD%A6%E3%81%B6%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0%E3%81%AE%E7%90%86%E8%AB%96%E3%81%A8%E5%AE%9F%E8%A3%85-%E6%96%8E%E8%97%A4-%E5%BA%B7%E6%AF%85/dp/4873117585/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=%E3%82%BC%E3%83%AD%E3%81%8B%E3%82%89%E4%BD%9C%E3%82%8B&qid=1624889653&sr=8-1)
- **「ゼロから作る Deep Learning 3」**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660013-7e6a1080-d1b8-11eb-8ce6-21d5e56a45e1.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660013-7e6a1080-d1b8-11eb-8ce6-21d5e56a45e1.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=9d7f5684f8b0403406db1a027ae72d38)  
	これも前作からの続編で、フレームワークを作っていくというものです。最後には、ゼロから作ったフレームワークでCNNやLSTMを実装して動かすというワクワクするシナリオになっています。1, 2と比べると人気は劣るような印象ですが、個人的には1, 2と同じぐらい大好きです。この本のお陰で何の違和感もなく、むしろ感動してPyTorchを使い始めることができたという点で、今振り返るとこの本も非常に重要でした。さらに分厚いですが、前作や前々作の復習もすることができ、さらにPythonそのもの(特にクラスについて)に対して強くなれました。  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/%E3%82%BC%E3%83%AD%E3%81%8B%E3%82%89%E4%BD%9C%E3%82%8BDeep-Learning-%E2%80%95Python%E3%81%A7%E5%AD%A6%E3%81%B6%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0%E3%81%AE%E7%90%86%E8%AB%96%E3%81%A8%E5%AE%9F%E8%A3%85-%E6%96%8E%E8%97%A4-%E5%BA%B7%E6%AF%85/dp/4873117585/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=%E3%82%BC%E3%83%AD%E3%81%8B%E3%82%89%E4%BD%9C%E3%82%8B&qid=1624889653&sr=8-1)
- **G検定の教科書、問題集**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122659949-e9ffae00-d1b7-11eb-9c94-3045618944c8.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122659949-e9ffae00-d1b7-11eb-9c94-3045618944c8.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=e3b7ee300a2c0a4474adeb72e56a5084)  
	[![](https://user-images.githubusercontent.com/70050531/122660250-06e9b080-d1bb-11eb-9fd6-ddbae04120e4.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660250-06e9b080-d1bb-11eb-9fd6-ddbae04120e4.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=29f7406dd553d8950a8184ae4fbbd298)  
	G検定というものがあるということを知り、どうせなら受けてみようということで勉強しました。今振り返って必要だったかと言われると必要はなかったと思います。自分が勉強していなかった各分野を浅く知れました。  
	[教科書のAmazonのリンクはこちら](https://www.amazon.co.jp/%E5%BE%B9%E5%BA%95%E6%94%BB%E7%95%A5%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0G%E6%A4%9C%E5%AE%9A%E3%82%B8%E3%82%A7%E3%83%8D%E3%83%A9%E3%83%AA%E3%82%B9%E3%83%88%E5%95%8F%E9%A1%8C%E9%9B%86-%E7%AC%AC2%E7%89%88-%E5%BE%B9%E5%BA%95%E6%94%BB%E7%95%A5%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA-%E3%82%B9%E3%82%AD%E3%83%AB%E3%82%A2%E3%83%83%E3%83%97AI%E6%A0%AA%E5%BC%8F%E4%BC%9A%E7%A4%BE-%E6%98%8E%E6%9D%BE-ebook/dp/B0976LT94B/ref=sr_1_1_sspa?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=G%E6%A4%9C%E5%AE%9A&qid=1624889708&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEyMVUxVzJGVlpPWkdJJmVuY3J5cHRlZElkPUEwNjg1NDAzMlNYSzUwWFZGTkY3QiZlbmNyeXB0ZWRBZElkPUFMRkZBRDdWVTc1WFImd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl)  
	[問題集のAmazonのリンクはこちら](https://www.amazon.co.jp/%E5%BE%B9%E5%BA%95%E6%94%BB%E7%95%A5%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0G%E6%A4%9C%E5%AE%9A%E3%82%B8%E3%82%A7%E3%83%8D%E3%83%A9%E3%83%AA%E3%82%B9%E3%83%88%E5%95%8F%E9%A1%8C%E9%9B%86-%E7%AC%AC2%E7%89%88-%E5%BE%B9%E5%BA%95%E6%94%BB%E7%95%A5%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA-%E3%82%B9%E3%82%AD%E3%83%AB%E3%82%A2%E3%83%83%E3%83%97AI%E6%A0%AA%E5%BC%8F%E4%BC%9A%E7%A4%BE-%E6%98%8E%E6%9D%BE-ebook/dp/B0976LT94B/ref=sr_1_1_sspa?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=G%E6%A4%9C%E5%AE%9A&qid=1624889708&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEyMVUxVzJGVlpPWkdJJmVuY3J5cHRlZElkPUEwNjg1NDAzMlNYSzUwWFZGTkY3QiZlbmNyeXB0ZWRBZElkPUFMRkZBRDdWVTc1WFImd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl)

### 7月

- **G検定合格**  
	  
	ここまでゼロつくなど様々な本を読んでいたので機械学習に関しては余裕でしたが、法律に関してははっきり言って無理ゲーという他なかったので、教科書にある分だけ抑えて、本番でわからないところは40回以上ググってやっつけました。体感は8割5部ぐらいでした。積極的に受ける必要はないかと思いますが、勉強したついでに受けてみるのもそれはそれでいいと思います。G検定とゼロつくなら間違いなくゼロつくです。少なくともKaggleに繋がるのは後者です。個人の所感なのであくまでご参考までに。
- **「直感Deep Learning」(Keras)**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660354-da826400-d1bb-11eb-8a0c-049d02cf7caa.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660354-da826400-d1bb-11eb-8a0c-049d02cf7caa.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=a796f9bd27f48336771e4c23ac7d0fee)  
	途中で挫折してしまいました。僕はフレームワークを学ぶ前にゼロつく3を読んでいたためにフレームワークはこういうものだというイメージが頭の中に既にあったので、それにそぐわないKerasを受け入れることがどうしてもできませんでした。全然直感的じゃなかったです...(人によるとは思いますが。)  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/Deep-Learning-%E2%80%95Python%C3%97Keras%E3%81%A7%E3%82%A2%E3%82%A4%E3%83%87%E3%82%A2%E3%82%92%E5%BD%A2%E3%81%AB%E3%81%99%E3%82%8B%E3%83%AC%E3%82%B7%E3%83%94-Antonio-Gulli/dp/4873118263/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=%E7%9B%B4%E6%84%9FDeepLearning&qid=1624889756&sr=8-1)

あと、本筋からはそれるのですが、GitやDockerもこのタイミングで一度勉強しました。ゼロつく2、3あたりは1人でGitを使う練習も兼ねていました。  

### 8月

- **「実践Data Scienceシリーズ PythonではじめるKaggleスタートブック」**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660363-e706bc80-d1bb-11eb-9e36-7ea201870cc1.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660363-e706bc80-d1bb-11eb-9e36-7ea201870cc1.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=acd93f6465b3b574582707dfd532517b)  
	6月あたりに買ったものの、submitの仕方がわからないという理由で放置していたので引っ張り出してきました。Kaggleは全て英語で書かれているため心理的障壁が高くなりがちですが、この本を読めば取り組み方、コンペの種類など様々なことを知れるのでとてもよかったです。機械学習についての説明も優しく書かれていたので、この本から機械学習を始めるのもありなのかなと思いました。  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/%E5%AE%9F%E8%B7%B5Data-Science%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA-Python%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8BKaggle%E3%82%B9%E3%82%BF%E3%83%BC%E3%83%88%E3%83%96%E3%83%83%E3%82%AF-KS%E6%83%85%E5%A0%B1%E7%A7%91%E5%AD%A6%E5%B0%82%E9%96%80%E6%9B%B8-%E7%A5%A5%E5%A4%AA%E9%83%8E/dp/4065190061/ref=sr_1_4?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=kaggle&qid=1624889768&sr=8-4)
- **Kaggle Titanicコンペ ・ House Prise コンペ**  
	  
	Kaggleスタートブックを読んで、自分なりにEDAをしたりアンサンブルをしたりしてみました。ほとんどスコアは伸びなかったですが、これまでと違ってちゃんとデータにさわれてる感覚があってとても嬉しかったです。個人的には、Kaggleに取り組み始める前にしっかり勉強する、というよりはできると思ったら即参加してみる方がいいと思います。目標はそれぞれ違うとは思いますが、Kaggleで強くなりたいのであれば、Kaggleを肌で感じで目標を立てて進めた方が圧倒的に早いです(自戒です)。
- **「米国データサイエンティストがやさしく教えるデータサイエンスのためのPython講座」**

> udemyの講座に関してはもっといい講座に出会えたので後に書きます。

それがこの講座です。今まで何となく使っていたnumpyやpandas、matplotlibなどにしっかり向き合うことができたので非常によかったです。この講座は発売同時に買ったので4月時点では無かったですが、あの時にこの講座に出会えていたらもっとスラスラ他の本を進められていたんだろうなと考えてしまいます。この講座の作者の「かめさん」という方はこの講座の他にもDockerやGitの講座も出しており、全部わかりやすいです。また、最近、numpyなどのライブラリではなく純粋なPythonの講座を出したようなので、今から買うのであれば目的に応じて選ぶといいと思います。udemyのクーポンが取得できる、かめさんのブログ記事を貼っておきます。 [こちら](https://datawokagaku.com/ds_for_python_video_lecture/) からどうぞ。Pythonを学ぶならこの方の講座が一番だと思っています。  
[講座のリンクはこちら](https://www.udemy.com/course/ds_for_python/)  

- **「PyTorch for Deep Learning with Python Bootcamp」**  
	  
	udemyのPytorchの講座です。書き始めてすぐに、これが今まで求めてたものだと感動した覚えがあります。全て英語なので若干敷居が高いですが、発音がとても綺麗で聞き取りやすいですし、Pytorchがしっかり解説されている動画講座は意外と少ないのでとてもオススメです。  
	[Udemyのリンクはこちら](https://www.udemy.com/course/pytorch-for-deep-learning-with-python-bootcamp/)
- **OSICコンペ参加、挫折**
[![スクリーンショット 2021-06-20 12 24 00](https://user-images.githubusercontent.com/70050531/122661167-6a2b1100-d1c2-11eb-9327-704c6071fb68.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122661167-6a2b1100-d1c2-11eb-9327-704c6071fb68.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=139d5ddc905a44efa703aae2e5a1f65d) Pytorchを身につけた勢いで初めてメダルありのコンペに参加しました。しかし、実際のコンペのコードにとても苦戦し、おまけにセグメンテーションも必要かも知れないということに気づき、あっという間に撤退してしまいました。この後はこのギャップを何とか埋めるべく色々な本を漁ることになりますが、Kaggleで強くなりたいという目標からするとこの判断は非常にまずかったです。\*\*Kaggleで強くなるためにはKaggleに向き合うしかないです\*\*。1ヶ月ほどコーディングから離れますが、再び戻ってきて同じように絶望したので、ここからの1ヶ月はKaggleに関しての進歩はほぼゼロでした。  
- **E資格の勉強**  
	  
	G検定を受けたのだからE資格も受けてみようと思い、AVILENさんの講座を受講しました。G検定と比べればだいぶ理論が詳しく説明されていて、何となく誤魔化してきた部分をしっかり学習することができたと感じています。僕は大学1年の途中だったので、内容としては特異値分解あたりの話、そして情報理論は改めて勉強する必要がありました。また、強化学習に関してはここまで全く勉強してこなかったのでとても苦しみました。正直今でもあんまりわかってないです。そのほかの内容に関してはほぼこれまでの教材で網羅され尽くされていると感じています。色々な手法を知ることができたので、Kaggleで、この単語知らないなぁ...となることがだいぶ減って楽になりました。受験は2月なので、それまで何度も復習していくことになります。
- **「これならわかる深層学習入門」**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660379-09003f00-d1bc-11eb-901f-a98f613bc586.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660379-09003f00-d1bc-11eb-901f-a98f613bc586.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=2eac4b8d80ec2e537f384229264d6b87)  
	E資格のために、深層学習の理論面の勉強で用いた本です。E資格を受験する際にはよく「深層学習」というめちゃくちゃ厚い本を勧められますが、僕はあれは明らかにオーバーワークだと思ったのでやめて、そこで代わりに手に取りました。深層学習だけでなく、機械学習全般についてわかりやすく書かれており、coursera、はじパタで手に入れた理解をアップデートすることができました。個人的にはこの本は強化学習の章がとてもわかりやすく、E資格の勉強に際して何度も何度も読んで式変形を追いました。深層学習の理論を学ぶならイチオシの本です。  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%82%B9%E3%82%BF%E3%83%BC%E3%83%88%E3%82%A2%E3%83%83%E3%83%97%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA-%E3%81%93%E3%82%8C%E3%81%AA%E3%82%89%E3%82%8F%E3%81%8B%E3%82%8B%E6%B7%B1%E5%B1%A4%E5%AD%A6%E7%BF%92%E5%85%A5%E9%96%80-KS%E6%83%85%E5%A0%B1%E7%A7%91%E5%AD%A6%E5%B0%82%E9%96%80%E6%9B%B8-%E7%80%A7-%E9%9B%85%E4%BA%BA/dp/4061538284/ref=sr_1_1?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=%E3%81%93%E3%82%8C%E3%81%AA%E3%82%89%E3%82%8F%E3%81%8B%E3%82%8B%E6%B7%B1%E5%B1%A4%E5%AD%A6%E7%BF%92%E5%85%A5%E9%96%80&qid=1624889820&sr=8-1)

### 9月

- **統計、機械学習に関する諸々の本**  
	  
	OSICで撃沈してから、若干現実逃避気味になり色々な本(完全独習ベイズ統計入門、統計学入門、データ解析のための統計モデリング入門、多変量解析、これなら分かる最適化数学、はじパタ、...etc)を読みました。統計にもともと興味があったのでそれはそれでよかったのですが、Kaggleで強くなりためにはだいぶ遠回りをしたと思ってます。
- **「つくりながら学ぶ! Pytorchによる発展Deep Learning」**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122661011-11a74400-d1c1-11eb-940a-ac0a29e57229.jpg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122661011-11a74400-d1c1-11eb-940a-ac0a29e57229.jpg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=d0e5efa6dbedd63c3e8c44f7a6ca8619)  
	  
	物体検出やセグメンテーション、Transformerなどこれまで紹介した書籍には中々掲載されていない発展的な内容が詳しく解説されています。各章で独立しているため、必要に応じて章ごとに読むことができるのでとてもオススメです。ソースコードも豊富なので、基本的な書き方を一通り理解した後に実践的な書き方を学ぶのにちょうどよかったと感じています。多くの人がこの本でPytorchを学んでいる印象です。  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/%E3%81%A4%E3%81%8F%E3%82%8A%E3%81%AA%E3%81%8C%E3%82%89%E5%AD%A6%E3%81%B6-PyTorch%E3%81%AB%E3%82%88%E3%82%8B%E7%99%BA%E5%B1%95%E3%83%87%E3%82%A3%E3%83%BC%E3%83%97%E3%83%A9%E3%83%BC%E3%83%8B%E3%83%B3%E3%82%B0-%E5%B0%8F%E5%B7%9D%E9%9B%84%E5%A4%AA%E9%83%8E/dp/4839970254/ref=sr_1_5?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=Pytorch&qid=1624889840&sr=8-5)  
	  
	ちなみに、現在はPytorchの入門書として有名であった洋書が翻訳されたPytorch実践入門が出版されており、Pytorchを深く学ぶならばこの本がいいのかもしれないです。(僕はもうKaggleに何度も参戦してそこで学んだので特に必要性をあまり感じておらず、買ったものの積読状態です。)  
	  
	[![](https://user-images.githubusercontent.com/70050531/122661105-deb18000-d1c1-11eb-9cee-eb487a0aac8b.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122661105-deb18000-d1c1-11eb-9cee-eb487a0aac8b.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=911adae9bb116f284db1d16c6377ad40)  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/PyTorch%E5%AE%9F%E8%B7%B5%E5%85%A5%E9%96%80-Eli-Stevens/dp/4839974691/ref=sr_1_6?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=Pytorch&qid=1624889860&sr=8-6)
- **MoAコンぺ参加**
[![スクリーンショット 2021-06-20 12 22 03](https://user-images.githubusercontent.com/70050531/122661134-2afcc000-d1c2-11eb-9c59-84ff2c29ea20.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122661134-2afcc000-d1c2-11eb-9c59-84ff2c29ea20.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=b6c835b71e692e5489258ec3d8a76e3b) 初心者でも取り組みやすい雰囲気のテーブルデータコンペ・かつニューラルネットが効きそうだったので参加しました。これが初めての本格参戦になります。上でも書きましたが、OSICで苦戦したことはそっくりそのままこちらでも苦戦しました。ここで、Kaggleと向き合っておくべきだったと後悔しました。今度はやり通せたのはタスクの難易度がこちらの方が少し低いのとOSICコンペから逃げた後悔のおかげです。本を読んで力がついたからではないと感じています。  

### 10月

- **「Kaggleで勝つデータ分析の技術」(通称：Kaggle本)**  
	  
	[![](https://user-images.githubusercontent.com/70050531/122660386-27663a80-d1bc-11eb-8c56-2c696e910045.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122660386-27663a80-d1bc-11eb-8c56-2c696e910045.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=b5e60debe159dc84af6d2dedddb3ec79)  
	  
	MoAコンペに参加していた時に読みました。コンペに対する取り組み方、様々な手法、バリデーションの仕方、などKaggleで重要な部分をたくさん学ぶことができました。現在はテーブルデータのコンペが減ったためにこの本に書いていることがそのまま全部通用することは少なくなりましたが、それでも上述のようなコンペにおける重要な部分を学ぶことは非常に意義深いことだと思うので、持っていて損はしないと思います。色々なことが網羅的に書かれているため、辞書的な使い方をしています。長く使える一冊なので、Kaggleに取り組むならばおすすめです。  
	  
	[Amazonのリンクはこちら](https://www.amazon.co.jp/Kaggle%E3%81%A7%E5%8B%9D%E3%81%A4%E3%83%87%E3%83%BC%E3%82%BF%E5%88%86%E6%9E%90%E3%81%AE%E6%8A%80%E8%A1%93-%E9%96%80%E8%84%87-%E5%A4%A7%E8%BC%94/dp/4297108437/ref=sr_1_1_sspa?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&dchild=1&keywords=kaggle&qid=1624889784&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUExN0YxUlQ1WEpQQzFYJmVuY3J5cHRlZElkPUEwNDUyNzMxMjBBV0pMVjBIM1pPRSZlbmNyeXB0ZWRBZElkPUExMFVZNUZERktRSEtRJndpZGdldE5hbWU9c3BfYXRmJmFjdGlvbj1jbGlja1JlZGlyZWN0JmRvTm90TG9nQ2xpY2s9dHJ1ZQ==)

改めて書くことはしませんがMoAコンペを頑張り続けていました。  

### 11月

- **MoAコンペ終了**  
	  
	Top13%で敗北しました。その時の振り返り記事があるのでもしよければご覧になってください。初めてコンペをやり切った感想、反省を詳しく書いています。 [こちら](https://qiita.com/Yuki_Kaggler/items/9271755b65c704733292) から飛べます。
- **Gitの勉強**  
	  
	詳しくは振り返り記事を参照していただきたいですが、MoAコンペの終盤でNotebook管理が崩壊して失速してしまったため、それを反省して管理体制を見直そうと考え、改めてGitを勉強しました。その時に使ったのは「Git: もう怖くないGit! チーム開発で必要なGitを完全マスター」というudemyの講座です。この直後に、Kaggle Notebookで、特定のVersionにボタンひとつで戻れる機能がついたので結局Gitは使わなかったです。  
	[Udemyのリンクはこちら](https://www.udemy.com/course/unscared_git/learn/lecture/6680364?start=0#content)

### 12月~2月

いきなりまとめてすみません。Cassavaコンペにほぼ全振りしたので書くことが少ないです。  

- **Cassavaコンペ**
[![スクリーンショット 2021-06-20 12 23 09](https://user-images.githubusercontent.com/70050531/122661154-4ff13300-d1c2-11eb-89db-3b9b872897c8.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122661154-4ff13300-d1c2-11eb-89db-3b9b872897c8.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=708d0a31b42b9cde32afe3588c1d0264) もともと画像処理に一番興味があったので、MoAの雪辱を晴らすために参加しました。キャッサバの葉の画像を、病気や健康などのラベルに分類するタスクでした。ゼロつくで色々学んだとはいえやはり実際にコンペに取り組むとなるとハードルは高く、最初は非本質的でしょーもない実験も繰り返していました。この頃からKaggle日記(\[参考記事\](https://zenn.dev/fkubota/articles/3d8afb0e919b555ef068), fkubotaさん著)を使い始めました。これが自分の中でとてもヒットして、以降のコンペでもスムーズに実験を進めることができ、かつ結果をいつでも振り返れるので自分の経験値にしていくことができるようになり、成長が早まりました。結果はTop11%で終わってしまいました。終わった後はショックが大きすぎて本当にもうやめようかと思いましたが、腹いせに飲んだタピオカミルクティーがおいしかったので何とか元気を取り戻しました。振り返り記事は\[こちら\](https://qiita.com/Yuki\_Kaggler/items/59d29c0942956c90eec6)で、Kaggle日記は\[こちら\](https://github.com/Yuki-Tanaka-33937424/Kaggle\_Cassava\_Leaf\_Disease\_Classification)です。もしよろしければご覧ください。  
- **E資格合格**  
	  
	2月下旬の試験で無事合格することができました。かなり高額ですが、受けてよかったと感じています。Cassavaコンペにも大きく生きました。ただ、満点を取れなかったことが悔やまれます。

### 3月

- **RANZCRコンペ**
[![スクリーンショット 2021-02-23 18 48 36](https://user-images.githubusercontent.com/70050531/108826575-cbbde300-7607-11eb-9edd-35ac39b4e8cd.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F108826575-cbbde300-7607-11eb-9edd-35ac39b4e8cd.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=3e93ad0d48aa80b81dc3d169aca316c0) Cassavaコンペのリベンジを懸けて参加しました。CT画像を元に、カテーテルの種類などを分類するコンペでした。ここまで1人で戦ってきて全てだめだったので、思い切ってひらさんというかたにお声かけしてチームを組ませていただきました。チームを組むと自分で全部やる必要がなくなるため自分のやるべきことを深掘りできるようになったり、相手の戦い方を見たりして、1人では得られない学びをたくさん得ることができました。そして何より楽しかったです。画像処理の勉強をした甲斐があってTop6%で銅メダルを獲得することができました。  
[![スクリーンショット 2021-03-21 10 54 02](https://user-images.githubusercontent.com/70050531/111891151-f9921e00-8a33-11eb-8652-8c71b456b375.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F111891151-f9921e00-8a33-11eb-8652-8c71b456b375.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=7eb686469a4cb76553f4d676b2ddb736)  
Kaggle日記は\[こちら\](https://github.com/Yuki-Tanaka-33937424/kaggle-RANZCR)です。もしよろしければご覧ください。  
楽しさを伝えたいので、一番楽しかったときのslackでのやりとりを貼っておきます。  
[![スクリーンショット 2021-06-20 0 18 58](https://user-images.githubusercontent.com/70050531/122659739-bfacf100-d1b5-11eb-85b1-a96345dc9fb5.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F122659739-bfacf100-d1b5-11eb-85b1-a96345dc9fb5.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=bf2012bfb8b1c0931a740788644755e5)  

### 4月・5月

- **Shopeeコンペに参加**  
	  
	[![スクリーンショット 2021-04-12 22 08 49](https://user-images.githubusercontent.com/70050531/114399570-08579500-9bdc-11eb-95e0-2b519858cdc5.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F114399570-08579500-9bdc-11eb-95e0-2b519858cdc5.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=fd6d8cfa72f03c65b957affdee97e4bb)  
	  
	こちらもチームで、今回は4人で参加しました。shopeeという東南アジアのメルカリのようなサイトの商品の画像と文章を元にマッチングをするタスクでした。Top3%銀メダルを獲得することができ、Expertに昇格することができました。チームメイトの方々には本当に感謝です。  
	  
	[![スクリーンショット 2021-05-15 22 27 59](https://user-images.githubusercontent.com/70050531/118362922-d7002980-b5cc-11eb-9478-be8b8ffc9f4f.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fuser-images.githubusercontent.com%2F70050531%2F118362922-d7002980-b5cc-11eb-9478-be8b8ffc9f4f.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=cc6a620434a1df279c57488d834e654e)  
	  
	自然言語処理についてはBERTを動かすので精一杯だったので今後の課題です。Kaggle日記は [こちら](https://github.com/Yuki-Tanaka-33937424/kaggle-Shopee-Price-Match-Guarantee) で、KaggleのDiscussionに掲載している解法は [こちら](https://www.kaggle.com/c/shopee-product-matching/discussion/238079) です。もしよろしければご覧ください。

## 4\. まとめ

僕が偉そうに言えることは何もありませんが、とにかく伝えたいのはKaggleで強くなりたいならKaggleをするのが最も近道であるということです。本で勉強した後にKaggleのコンペに実際に参加するとギャップに苦しむことになる可能性が高いですが、Kaggleには公開NotebookやDiscussionなどヒントがたくさん落ちているので、腰を据えて(英語が苦手であればDeeplを使って)向き合っていくことが大切だと思います。  
  
そして、今回僕があえてExpertになった段階で勉強したことを全て公開したのは、Master以上の方々が書いた素晴らしい記事が既にたくさんあるからです。特に初心者の場合はMaster以上の方々との距離がだいぶ大きいので、距離が近い僕の記事にも価値があると判断しましたが、Master以上の方々の記事も是非ご覧になってください。僕自身も何度も見て参考にさせていただきました。  

## 5\. 今後の目標

言わずもがな、Kaggle Masterです。今年中に確実に昇格します。また、ここまでのメダルは全てチームでとっているため、どこかのタイミングでソロでメダルを取ります。  

ここまでご覧いただきありがとうございました！少しでもお役に立てたのであれば嬉しい限りです。Happy Kaggling!!

[9](https://qiita.com/Yuki_Kaggler/items/#comments)

コメント一覧へ移動

新規登録して、もっと便利にQiitaを使ってみよう

1. あなたにマッチした記事をお届けします
2. 便利な情報をあとで効率的に読み返せます
3. ダークテーマを利用できます
[ログインすると使える機能について](https://help.qiita.com/ja/articles/qiita-login-user)

[新規登録](https://qiita.com/signup?callback_action=login_or_signup&redirect_to=%2FYuki_Kaggler%2Fitems%2F8ffe2ffa6f020e09cfd3&realm=qiita) [ログイン](https://qiita.com/login?callback_action=login_or_signup&redirect_to=%2FYuki_Kaggler%2Fitems%2F8ffe2ffa6f020e09cfd3&realm=qiita)

[1093](https://qiita.com/Yuki_Kaggler/items/8ffe2ffa6f020e09cfd3/likers)

1082
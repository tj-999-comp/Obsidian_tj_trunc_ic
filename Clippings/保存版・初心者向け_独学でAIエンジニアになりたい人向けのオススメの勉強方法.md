---
title: 保存版・初心者向け_独学でAIエンジニアになりたい人向けのオススメの勉強方法
source: https://qiita.com/tani_AI_Academy/items/4da02cb056646ba43b9d
author:
  - "[[tani_AI_Academy]]"
published: 2018-05-07
created: 2025-06-02
description: 
tags:
  - clippings
  - Data_Science
  - Machine_Learning
---
![](https://relay-dsp.ad-m.asia/dmp/sync/bizmatrix?pid=c3ed207b574cf11376&d=x18o8hduaj&uid=)

## Qiitaにログインして、便利な機能を使ってみませんか？

[ログイン](https://qiita.com/login?callback_action=login_or_signup&redirect_to=%2Ftani_AI_Academy%2Fitems%2F4da02cb056646ba43b9d&realm=qiita) [新規登録](https://qiita.com/signup?callback_action=login_or_signup&redirect_to=%2Ftani_AI_Academy%2Fitems%2F4da02cb056646ba43b9d&realm=qiita)

この記事は最終更新日から1年以上が経過しています。

## 追記

【2020年版・初心者向け】独学でAIエンジニアになりたい人向けのオススメの勉強方法  
[【保存版・初心者向け】独学でAIエンジニアになりたい人向けのオススメのAI勉強方法](https://qiita.com/tani_AI_Academy/items/e47bf4d1316b66a0402b)

また、Pythonや機械学習がオンライン上で学べる [AI Academy](http://aiacademy.jp/) を [note](https://note.mu/kazu_t/n/n5ec08705f31f) でも書きましたが、 **3/17日からほとんどのコンテンツを永続的に無料で利用できる** よう致しましたので、是非使って頂けますと幸いです。

## AI Academy Bootcamp

我々が提供している個人向けオンラインAIブートキャンプのご紹介です。  
[AI Academy Bootcamp](https://aiacademy.jp/bootcamp)  
AI Academy Bootcampは、「短期間でAI活用スキルを付けたい」と考えている方や、  
「データサイエンティスト」や「機械学習エンジニア」として就業を目指している方向けの  
AI特化型オンラインブートキャンプです。  
講義動画とオンラインマンツーマンの演習授業により質の高い学習を進められます。

[６ヶ月35,000円にてチャットで質問し放題の環境で、機械学習やデータ分析が学べるサービス](https://aiacademy.jp/bootcamp) を提供しております。  
数十名在籍しているデータサイエンティストや機械学習エンジニアに質問し放題の環境でデータ分析、統計、機械学習、SQL等が学べます。AI人材に必要なスキルを効率よく体系的に身に付けたい方は是非ご検討ください！  
[![bootcamp_ad_72ppi.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/195675/f261ccc8-42db-a292-2511-6a742d1987f7.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F195675%2Ff261ccc8-42db-a292-2511-6a742d1987f7.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=83f55ec21cb98fd82d99d85ddf032a03)  
[https://aiacademy.jp/bootcamp](https://aiacademy.jp/bootcamp)

## はじめに

我々株式会社エーアイアカデミー(AI Academy,Inc)は2016年6月からオンライン・オフラインにて [AI Academy](http://aiacademy.jp/) というサービスを通じて、これまで1500名以上の方々に、プログラミング(Python)、統計的機械学習、深層学習(Deep Learning)、機械学習のための数学、確率・統計などを教えてきました。  
そんな中、 **サービスを通じて一人一人に最適な勉強方法\_\_を日々出会う初学者の方々に、私達なりの学習アドバイスを行なっていたのですが、1500名以上の初学者に教えていく中で、人工知能を勉強するにあたって、多くの** 『わからない』\_\_には、共通する点があることに気づきました。  
この記事では、我々が解決してきた受講生の方々の\_\_共通の『わからない』\_\_を体系的にまとめることで、  
これから\_\_機械学習エンジニア（AIエンジニア）になりたい、目指したい\_\_と考えている多くの初学者にとって、役に立てれるのではないかと思い記事にすることに致しました。  
今回の記事を通して、1人でも多くの方に何か参考になることがありましたら幸いです。

## この記事の対象者

・将来Pythonでデータ解析をしたいと考えているが、何から手をつけたら良いか知りたい方  
・将来、人工知能に関連した業務に携わりたいと検討中の初学者の方  
・未経験者からAIエンジニアになりたく、そのためにどのような知識が必要か知りたい方  
・AIプログラミングスクールや専門学校に進学しようか考えているが、独学で勉強できる方法を知りたいという方

## 対象ではない方

・既に業務でデータ解析している方  
・ディープラーニングを使ったWebアプリなどを作りたいと考えている方  
・ディープラーニングの資格試験の勉強方法  
などなどは対象としておりません。

## AIエンジニアに最低限必要な知識

まずは、AIエンジニアに最低限必要な知識を大きく6つに分けて見ました。  
ここでは、将来AIエンジニアとして業務を行うにあたり、大きく分けて\_\_6つの内容の基礎知識\_\_の全体像を把握してください。  
**①プログラミングスキル**

- Python
- numpy、pandas、matplotlib、scikit-learn、TensorFlowやkeras  
	この中で特にpandasを使いこなせると良いです。  
	機械学習を行う上で、データ前処理が必須なのですが、データ前処理を行う上で便利なライブラリです。  
	**②数学**
- 微分、線形代数、ベクトル、行列、確率など  
	**③統計の知識**
- 標準偏差、分散、確率分布、推定、検定などなど  
	**④機械学習の基礎知識**
- 教師あり学習と教師なし学習
- 前処理、特徴量設計、学習と評価
- 単回帰、重回帰分析、最小二乗法、パーセプトロン、ロジスティック回帰
- 決定木、ランダムフォレスト、サポートベクトルマシン、K-means
- ディープラーニングの実装スキル及び知識
- scikit-learn
- TensorFlowやKerasなどのフレームワークの知識
- scikit-learnで学習済みモデルを作るまでの流れなど。  
	  
	1.データの収集とデータの前処理欠損値の補完や外れ値の削除)  
	  
	2.特徴量の設計（特徴量の選択)  
	  
	3.モデル開発(モデルの選択と学習）  
	  
	4.モデル評価・・・交差検定、混合行列で評価など  
	  
	**⑤SQLを使ってデータベースを操作する知識**
- select、insert、update、delete、where、like、limit、sum、avg、max、group by、having、order by、テーブル結合、ビュー、サブクエリ、caseなどなど  
	**⓺クラウドの知識**
- AWSやGCPやAzureなどのクラウドインフラ回りの知識  
	大きく6つもあり意外と多いなと思われたかもしれませんが、一度に全てやるのではなく、まずは①と④の2つに絞ることをオススメします。  
	理由は、実際にプログラムを書き、目に見える形にすることで継続して学びやすくなるからです。  
	はじめに理論から入ると独学だと挫折してしまうので。

## 人工知能を独学で勉強するオススメの方法

必要な知識は前の節で紹介しましたが、どのようにそれらを学べば良いのでしょうか。  
①から⑥を学ぶ上で、以下のような順で知識を身につけていくことをオススメしています。  
フェーズ1 pythonによる機械学習プログラミングと人工知能概論を学ぶ  
フェーズ2 機械学習プログラミング  
フェーズ3 Kaggleに挑戦  
フェーズ4　 SQL、スクレイピング、クラウドなどの技術も身につける。  
フェーズ5 機械学習スキルを活用してプロダクト制作をする  
フェーズ6 教える  
このフェーズごとに学んでいくことがもっとも自分自身に負荷をかけず、楽しく学ぶことができると考えています。  
フェーズ1ではプログラミング初学者の方を指しております。  
もし、プログラミングを初めてという方は是非フェーズ1から目を通してください。  
フェーズ2では実際にフェーズ1で学んだ内容をベースに、機械学習プログラミングに関する勉強方法を説明して参ります。  
既にscikit-learnを使った機械学習プログラミングを行なっている方は飛ばして頂いても構いません。  
フェーズ3ではKaggleといったコンペティションを通じて実践的なプログラミングを学ぶ方法を記述しています。  
フェーズ4　機械学習をやる上で、データベースからデータを取り出すことは頻繁に行われますので、SQLの知識は必須です。ここでは、SQLの他にスクレイピング（データ収集用）、クラウドなどの技術の身につけ方を紹介します。  
フェーズ5 機械学習スキルを活用してプロダクト制作に取り掛かりましょう。このレベルまで到達した方は、プロダクトを通じて学ぶことが多いです。  
フェーズ6 人に教えることで自分の分かっていなかったことが明確になることがあります。なので、友人などに機械学習を教えて自分の理解を深めることもよいでしょう。  
以降、６つのフェーズごとに、どのようにこれらに取り組めば良いのか、\_\_オススメの書籍\_\_などを紹介しながら説明していきます。

### フェーズ1 pythonによる機械学習プログラミングと人工知能概論を学ぶ

独学で、書籍を使って、  
人工知能開発に最低限必要な知識は「機械学習の知識」と「Pythonの知識」と「機械学習のための数学と確率・統計学」です。  
このフェーズでは、「機械学習の知識」と「Pythonの知識」に絞り、一旦「機械学習のための数学と確率・統計学」は違うフェーズに回しても大丈夫です。  
数学や確率がわからなくても、機械学習用のライブラリを使えば機械学習を体験でき、理論だけの学びよりモチベーションが保ち安いからです。（人によっては理論からの方が継続できる方もいるかと思いますので断言はしません。）  
その後、ライブラリに頼った実装をした後に、中で何が行われているのか気になってから、一度立ち戻って数学・統計学などを学ぶことをオススメします。  
では、 **オススメ書籍を紹介していきます。**  
まず、プログラミング初心者または、Pythonの基本文法に自信がない方は下記書籍がオススメです。  
・Python3 入門ノート  
[![p.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/6b05e2ee-d7c4-4516-96ef-a3e23584beac.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F6b05e2ee-d7c4-4516-96ef-a3e23584beac.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=42160df50209589a92f2734b99c33bcf)  
[http://amzn.asia/8ccnGQH](http://amzn.asia/8ccnGQH)  
2894円  
こちらの書籍はpythonの基礎にあたる基本文法だけでなく、機械学習プログラミングに関する基礎も学べます。  
この書籍を一通り読み終えることで、pythonプログラミングの基礎力と、機械学習プログラミングの体験が出来ます。  
また、pythonプログラミングを始める際には、\_\_開発環境いらずのブラウザかつ無料で使える、CPU/GPUの機械学習環境が整った [Google Colaboratory](https://colab.research.google.com/notebooks/welcome.ipynb#recent=true) \_\_を利用してPythonプログラミングをしていきましょう。  
次に、人工知能の概要に関してさらっと学びたい方は下記の書籍をお勧めします。  
・人工知能は人間を超えるか ディープラーニングの先にあるもの (角川EPUB選書) \[単行本\]  
[![ai.png](https://qiita-image-store.s3.amazonaws.com/0/171715/191649fe-bb3c-cc7a-96a8-0ffcb06bb875.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F191649fe-bb3c-cc7a-96a8-0ffcb06bb875.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=5f9615277523200e8e436a9fc0513b7f)  
[http://amzn.asia/iW1Ms5S](http://amzn.asia/iW1Ms5S)  
1512円  
上記2冊はPythonの本を読み、出てくるプログラムを手を動かしながら進めてください。  
さて、上記2冊で人工知能に関する知識及びPythonプログラミングの基礎が固まった方は、  
機械学習の一連の流れと統計的機械学習のプログラミングを始めましょう。

### フェーズ2 機械学習プログラミング

・Pythonではじめる機械学習  
[![download.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/832c10ec-eb5c-a021-0c89-d859868df6f9.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F832c10ec-eb5c-a021-0c89-d859868df6f9.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=e3412cb5fab4e46890b6ac121cf6834f)  
こちらも手を動かしながらコードを書き、またその後コードを読む(写経)をおこなってください。  
ただ本を読むだけより、手を動かしながら進める方が理解が深まります。  
[http://amzn.asia/0GskuMa](http://amzn.asia/0GskuMa)  
3672円  
+α  
[![61qCGR2QqGL.SX390_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/36da4189-41c6-9c7d-cdc4-f7f0410a02d5.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F36da4189-41c6-9c7d-cdc4-f7f0410a02d5.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=a4ab0c1c915a88937338a799e2300b87)  
[http://amzn.asia/9EPUIpg](http://amzn.asia/9EPUIpg)  
4320円  
ここまで来てライブラリの中でどのような処理がされているか気になった方は、ニューラルネットワークをnumpyなどの最小限のライブラリを使って、実装してみましょう。  
数学の知識が不安な方は、下記で紹介している数学の本などを参考にしてみてください。  
・ **ニューラルネットワーク、ディープラーニング**  
ゼロから作るDeep Learning ―Pythonで学ぶディープラーニングの理論と実装  
[![download.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/b3cb1989-1f71-e402-0946-77279d6afdd1.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Fb3cb1989-1f71-e402-0946-77279d6afdd1.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=8d9cd290f7835c77680eb1338b59fec6)  
[http://amzn.asia/caXkYL3](http://amzn.asia/caXkYL3)  
こちらも実際に手を動かしながら、ニューラルネットを作りながら学びます。  
3672円  
・ **数学**  
やさしく学ぶ 機械学習を理解するための数学のきほん  
[![5149k70AUiL.SX348_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/ac665ed7-e3ee-28db-ec10-ceb25dbc9088.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Fac665ed7-e3ee-28db-ec10-ceb25dbc9088.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=6afaec59b8cb606e3fc9f9b726feb57b)  
[http://amzn.asia/b2XXln9](http://amzn.asia/b2XXln9)  
2786円  
+機械学習の技術書を読み、数式アレルギーが出た方はキカガク吉崎さんの動画をオススメします！  
+手書きで講義で数学が学べ、何より説明がわかりやすい！  
+数学がアレルギーの方は上記のほんと合わせて、2つの動画を利用することをオススメします。  
+  
\+ [【キカガク流】人工知能・機械学習 脱ブラックボックス講座 - 初級編 - | Udemy](https://www.udemy.com/kikagaku_blackbox_1/learn/v4/overview)  
+  
\+ [【キカガク流】人工知能・機械学習 脱ブラックボックス講座 - 中級編 - | Udemy](https://www.udemy.com/kikagaku_blackbox_2/learn/v4/overview)  
+  
+  
+  
・ **数学+α**  
Pythonで動かして学ぶ！ あたらしい機械学習の教科書  
[![51iDMtWhZxL.SX355_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/a5f81a18-0b6e-f3f1-62eb-a55b4d60d028.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Fa5f81a18-0b6e-f3f1-62eb-a55b4d60d028.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=62a0db8186b834f7e9e3bdbda57ba8bb)  
[http://amzn.asia/fzt2aXa](http://amzn.asia/fzt2aXa)  
・ **確率、統計学**  
Pythonで学ぶあたらしい統計学の教科書  
[![515zrlsaraL.SX350_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/7d0bcb28-ae18-0630-4ea1-d68083422f25.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F7d0bcb28-ae18-0630-4ea1-d68083422f25.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=3777d4e1746b3041df3684440c040fc8)  
[http://amzn.asia/1zA7oAJ](http://amzn.asia/1zA7oAJ)  
3240円  
・ **データ前処理**  
前処理大全\[データ分析のためのSQL/R/Python実践テクニック\]  
[![download.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/d1dbacab-1ae6-1b3b-6e20-d2def4526422.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Fd1dbacab-1ae6-1b3b-6e20-d2def4526422.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=18186ad7c1c4c67c459b08b4339f6161)  
[http://amzn.asia/aa5dHB0](http://amzn.asia/aa5dHB0)  
3240円  
次に、ライブラリを用いてDeepLearningの学習をしましょう。  
ライブラリはTensorFlowまたはKerasをオススメしています。  
初心者にオススメなのはKerasの方です。  
・Keras  
PythonとKerasによるディープラーニング  
[![51-0e4nTugL.SX387_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/d002e41e-5545-eaed-9865-3ba47507cea9.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Fd002e41e-5545-eaed-9865-3ba47507cea9.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=1cf9ea7594628605b5ec08256e098394)  
[http://amzn.asia/8Ya7Xu5](http://amzn.asia/8Ya7Xu5)  
4190円  
※日本版は2018年5/28日に発売予定です。  
英語版は下記から購入可能です。  
[Deep Learning with Python (英語)](http://amzn.asia/bOTkdgw)  
5891円  
・TensorFlow  
TensorFlowではじめるDeepLearning実装入門  
[![51+CSAP98RL.SX387_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/e99d4dc8-9427-7917-0715-f52ece7592e6.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Fe99d4dc8-9427-7917-0715-f52ece7592e6.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=65d2baf4f9b8c160a9f13084e91c908e)  
[http://amzn.asia/hLtvTDT](http://amzn.asia/hLtvTDT)  
2808円  
書籍以外にも、 [Udemy](https://www.udemy.com/) などがオススメです。  
次の動画も合わせてご利用してみてください。  
[Pythonで機械学習：scikit-learnで学ぶ識別入門](https://www.udemy.com/python-scikit-learn/)

### フェーズ3 Kaggleに挑戦

さて、フェーズ1,2では書店で販売されている機械学習関連の書籍を紹介しました。  
上記の書籍を順番に1〜3ヶ月ほど手を動かしながら進めると、機械学習の一連の流れや、自分で機械学習のモデルを読み書きできるレベルになっているはずです。  
ここでは、次のフェーズとして [Kaggle](https://www.kaggle.com/) や [SIGNATE(旧 DeepAnalytics)](https://signate.jp/) を使って、実践します。  
Kaggleは、世界中のデータサイエンティストが集まるコンペティションサイトです。  
企業などが分析してほしいデータをここに載せて、ユーザーが分析をして、分析の精度を競います。  
上位３位にはデータをあげた企業から賞金も出ます。  
Kaggleのオススメの使い方としては、Kernels（カーネル）という機能を使うことです。  
カーネルでは、各データセットに対して他のユーザーが構築したモデルのコードの説明などがわかりやすく書いてあります。  
**Kaggleで実際にデータ解析を行うとわかりますが、データの前処理が大変重要です。**  
**ここでのポイントとしては、pandasを上手く使いこなせるかが鍵になっております。**  
pandasのデータ加工でわからないことがあれば、  
[pandas公式 チュートリアル](https://pandas.pydata.org/pandas-docs/stable/tutorials.html) から再度復習してみてください。  
書籍としては [Pythonによるデータ分析入門](http://amzn.asia/1Al0GEt) がオススメです。

### フェーズ4　SQL、スクレイピング、クラウドなどの技術も身につける。

実データに関しては、Web上のデータであればデータベースに保存されていることが多いため、SQLの知識も必要になります。  
ここでは、SQLを使ってデータ分析をするための参考になる書籍を紹介します。  
・ProgateのSQL編（SQL初級者向け）  
[Progate\[プロゲート\] SQL](https://prog-8.com/languages/sql)  
・SQLを使って分析をする(SQL中級者向け)  
[ビッグデータ分析・活用のためのSQLレシピ](http://amzn.asia/4gDmIEe)  
[![61kzm62vzeL.SX382_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/83645d57-92e3-5660-d8a1-7c7746aee8f7.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F83645d57-92e3-5660-d8a1-7c7746aee8f7.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=6badd916f305dd76f72df378871e2729)  
データ収集はデータベースから行うこともあれば、スクレイピング等で行うこともあります。  
スクレイピングはWebサイトに掲載されている情報を収集するための技術です。  
ここでは、スクレイピングの技術習得のためにオススメの書籍を二冊紹介いたします。  
・1冊目にオススメ  
[Pythonによるスクレイピング&機械学習 開発テクニック BeautifulSoup,scikit-learn,TensorFlowを使ってみよう](http://amzn.asia/c7mpmzl)  
[![61sxmRFvyfL.SX376_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/f1db9b94-348c-601a-b1f8-bd9c55b454fc.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Ff1db9b94-348c-601a-b1f8-bd9c55b454fc.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=8edcbb795ae36f5f91ad845c2294de86)  
・2冊目にオススメ  
[Pythonクローリング&スクレイピング -データ収集・解析のための実践開発ガイド](http://amzn.asia/6ei5m41)  
[![51IiWeYB-7L.SX399_BO1,204,203,200.jpg](https://qiita-image-store.s3.amazonaws.com/0/171715/6f8f377a-0bde-7efc-c039-6f13378bc06b.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F6f8f377a-0bde-7efc-c039-6f13378bc06b.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=528d2498eefa0dec7f3234f0b449ced4)  
・クラウド  
ここではGoogle Cloud Platform(GCP)の簡単な説明をします。  
Google Cloud Platformは、Googleが保有する膨大なインフラストラクチャや機械学習等といったサービスを使った分だけの支払いで利用することができるクラウドサービスの総称であり、GCPを使うことでサービスを開発する上でのインフラ周りや、高性能なデータ分析・機械学習サービスを各種APIを通じて利用が出来ます。  
GCPとよく比較されるサービスとしてAmazonのAWS、Micro softのAzureなどがありますがそれらの違いは下記記事を参考にして見てください。  
[Google Cloud Platform とAWS、Azureの違い](https://clonos.jp/knowledge/detail01/)  
また、GCPのAPIをPythonで呼び出すことが出来ますが、下記画像にある通り画像認識・動画解析、音声認識、自然言語処理などのAPIが用意されています。  
自分の作りたいものを作るときに、0からscikit-learnやKerasなどを使って自前で作るより、APIを使った方が簡単にかつ、精度の良いものを作ることが出来ます。  
**自分にあったAPIを探し、ドキュメントや、Googleで検索したり、qiitaで調べたりして出てきた記事を参考にすれば実装が出来たりします。**  
[![スクリーンショット 2018-05-07 16.55.00.png](https://qiita-image-store.s3.amazonaws.com/0/171715/f6680ac4-e2df-71aa-407f-68e1bde158fd.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2Ff6680ac4-e2df-71aa-407f-68e1bde158fd.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=48ddeb1258810b4dccad49a50239fe49)  
[GOOGLE CLOUD PLATFORM での PYTHON](https://cloud.google.com/python/?hl=ja)

### フェーズ5 機械学習スキルを活用してプロダクト制作をする

フェーズ5まで、機械学習スキルやそれ以外の人工知能関連技術を学びました。  
ほとんど最後のフェーズですが、次のフェーズとしては\_\_プロダクト制作\_\_をすることをオススメします。  
プロダクトには様々な形があると思いますが、ひとまずWebアプリケーションが学習コストが少なく済むので、オススメです。  
次に、モバイルのアプリなどに取り組んで見ても良いでしょう。  
Webアプリケーション作成にはPyhonの他にも、HTML, CSS, JavaScriptの知識が必要です。  
これらの知識はプロゲート, ドットインストールなどを利用して身につけましょう。  
・HTML, CSS, JavaScript  
[プロゲート](https://prog-8.com/)  
[3分動画のドットインストール(dotinstall)](https://dotinstall.com/)  
また、PythonでのWebアプリケーション開発はDjango,Flaskなどのフレームワークが有効ですが、一人で学ぶには、Flaskが学びやすいです。  
FlaskはUdemyの動画を参考にすると良いでしょう。  
[Udemy](https://www.udemy.com/python-flask-course/)  
動画を見るだけでなく、動画のプログラムを打ち込みながら手を動かして進めるのがオススメです。  
さらに、Web開発を身につけた方は、Google CloudのAPIなども合わせ学び、これまで学んだことを合わせてあなたのアイデアを形にしてみてください。  
Google Cloudでは、画像・動画分析、音声認識、テキスト分析などを容易に扱うことが可能です。

### フェーズ6 教える

プログラミングや機械学習を学んだら、友人でも良いので誰かに教えることをオススメします。  
教える方法としては、イベントやセミナーを行うのも良いですし、Skypeなどを使い、友人にマンツーマンレッスンを行なったり、カフェで直接教えたりするのが良いです。  
教える以外にもQiitaやブログに記事を書いたり、本を書くとかも良いかと思います。  
AI Academyでは受講生の交流会やLT会もやっており、人前で教える機会も提供しておりますので、是非ご活用して見てください！

## 学習ロードマップ

[![スクリーンショット 2018-05-05 1.33.00.png](https://qiita-image-store.s3.amazonaws.com/0/171715/326feb92-c079-7c33-b2bf-1b3cc202f825.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.amazonaws.com%2F0%2F171715%2F326feb92-c079-7c33-b2bf-1b3cc202f825.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=ab6c6306636b93cf8853342d3bc4f956) 左の書籍(STEP1)から右の書籍(STEP4)まで順に読み進めてください。 すでにpythonプログラミングの基本がわかっている方はSTEP1を飛ばしても構いませんし、既にscikit-learnで機械学習プログラミングの基本や機械学習の数学もわかる方はSTEP2も飛ばしても構いません。 自分の現在のレベルにあったSTEPから初めてください。 もし、\_\_pythonプログラミングの経験がない方や、人工知能ってなに？という方はSTEP1から初めてください。\_\_ 何度も記述していることですが、ポイントなのが、基本的に書籍に出てくるコードは実際に書いて進めることです。 例えば、英語などを勉強するときも教材を眺めるだけより、書いたり読み上げたり聞いたりすることが有効だったりします。 プログラミング言語も同様で、ただ本を眺めるだけより、実際に写経することでより理解が深まります。 ただし、どの教材も１００％理解する必要はありません。 どのタイミングで、次のSTEPへ進むかの判断基準ですが、\_\_書籍に書いてあること全て理解せずに、7割理解できたかな\_\_というレベルで十分です。 そこに到達したら次へ進みましょう。 また、詳細は上記\_\_人工知能を独学で勉強するオススメの方法\_\_を参考に進めてください。 STEP1から始められる方で、○○のデータ解析ができるようになりたい！というのであれば、ニューラルネットワークやKerasによるディープラーニングの部分は飛ばしても構いません。 一旦、STEP1→STEP2→フェーズ3 Kaggleに挑戦→その後必要に応じて、ニューラルネットワーク実装&ディープラーニングライブラリ(TensorFlowやkerasなど)へ進めて頂ければと思います。 というのも、scikit-learnにもニューラルネットワークを使うことができますので、業務でディープラーニングを使うことが決まっていなかったり、データ解析をゴールにおいている場合はがっつりディープラーニングを学ぶ必要はそこまでないかなという理由です。 しかし、AIエンジニアとして就職・転職希望の方はしっかり『ゼロから作るディープラーニング』の中身は理解しておきましょう。 # まとめ ここまでの流れをまとめます。 フェーズ1 pythonによる機械学習プログラミングと人工知能概論を学ぶ フェーズ2 機械学習プログラミング フェーズ3 Kaggleに挑戦 フェーズ4 SQL、スクレイピング、クラウドなどの技術も身につける。 フェーズ5 機械学習スキルを活用してプロダクト制作をする フェーズ6 教える # 英語に自信がある方へ ここまでは、学習方法やオススメの書籍などを紹介しましたが、英語に自信がある方にはオススメのサービスを紹介します。 \_\_※英語苦手だとしてもCoursera　（コーセラ）の機械学習は是非受講することをオススメします。\_\_ ①Coursera　（コーセラ） \[Coursera Machine Laerning\](https://www.coursera.org/learn/machine-learning) コーセラは世界中の人に最高の教育を無料で提供するということを理念にしているオンライン教育サービスです。 特に機械学習のコースの講師はStanford Universityのアンドリュー・ウ(Andrew Ng)氏です。 アンドリュー氏は、人工知能の研究をしており、Google Brainの立ちあげやCouseraのファンダーでもあります。 シリコンバレーにあるBaiduの研究所で勤務しておられる方であり、機械学習を学ぶのに最も適した教材とも言え、機械学習の主要なアルゴリズムを直感的に理解し、実際にプログラミングできるように教えてくれます。 \[Andrew Ng氏\](https://twitter.com/AndrewYNg)は沢山褒めてくれるので、とても嬉しくなります笑 （※プログラミング言語はPythonではなく、Octave・MATLABです）!\[スクリーンショット 2018-05-07 0.01.55.png\](https://qiita-image-store.s3.amazonaws.com/0/171715/918b9c84-9e08-dc5d-af17-3e0ec70a8334.png) ②Learn with Google AI (ai.google education) \[Learn with Google AI\](https://ai.google/education#?modal\_active=none)!\[スクリーンショット 2018-05-07 0.01.23.png\](https://qiita-image-store.s3.amazonaws.com/0/171715/f2cc1f4b-46b8-aaa8-dca0-4d4f303cb569.png) Google社内教育プログラムで無料で利用可能です。 コンテンツは、大変わかりやすい動画です。 ## こちらもオススメ \[Udacity「Intro to Machine Learning\](https://www.udacity.com/course/intro-to-machine-learning--ud120)!\[スクリーンショット 2018-05-07 0.02.32.png\](https://qiita-image-store.s3.amazonaws.com/0/171715/8e78a867-0c1d-b77d-2079-31e6cffb0716.png) \[Machine Learning with Python (YouTube)\](https://www.youtube.com/playlist?list=PLQVvvaa0QuDfKTOs3Keq\_kaG2P55YRn5v)!\[スクリーンショット 2018-05-07 0.44.24.png\](https://qiita-image-store.s3.amazonaws.com/0/171715/93a16a21-e71a-eb00-134e-1fcd84e79750.png) # 本気でAIエンジニアを目指している方へ 上記内容を順に学んでいくことで、一定の基礎スキルが身につき、AIエンジニアとしての入り口に入れるかと思います。 ですが、実務でAIエンジニアとして活躍していくにはまだまだ知識的に足りない可能性があります。 その際には、以下に挙げる勉強法と、その書籍にも目を通していくことをオススメします。 1. C++及びJava言語で機械学習のアルゴリズムも書けるようにする。 2. \[『データ解析のための統計モデリング入門――一般化線形モデル・階層ベイズモデル・MCMC』\]( http://amzn.asia/5118g0M)以上の統計学の知識 と\[統計学入門 (基礎統計学Ⅰ)\](http://amzn.asia/6RuVPNl) 3. \[統計的学習の基礎 ―データマイニング・推論・予測\](http://amzn.asia/8mAkkJN)

## 終わりに

ここまでお読みいただきありがとうございました。  
弊社ではAI AcademyというオンラインAIプログラミング  
学習サービスを運営しており、AIを学びたい方の目標を最短で実現するサポートを行なっております。  
メインサービスとして行なっていることは、以下の３点です。  
・今回取り上げた書籍の中でもさらに必要な部分のみを抽出したテキストコンテンツ(スマホからでもPCからでも閲覧できます。)  
・チャットでの質問対応やコードレビュー(**※AI Academyのコンテンツ以外のことも質問可能です。**)  
・学習進捗サービス（作りたいプロダクトへの最短ルートの提示、次に何をしたらいいかの提示）  
これまで長々と書いておりましたが、上記した書籍を全て１から学ぶにはそれなりの学習コスト（最低でも６ヶ月程度）がかかります。  
弊社のような教育系サービスをご利用いただければ、大幅に学習コストを減らせるので、一度ご検討していただけると幸いです。  
[AI Academy Bootcamp](https://aiacademy.jp/bootcamp) は、「短期間でAI活用スキルを付けたい」と考えている方や、「データサイエンティスト」や「機械学習エンジニア」として就業を目指している方向けの  
AI特化型オンラインブートキャンプです。  
講義動画とオンラインマンツーマンの演習授業により質の高い学習を進められます。

## AI Academy Bootcamp

[６ヶ月35,000円にてチャットで質問し放題の環境で、機械学習やデータ分析が学べるサービス](https://aiacademy.jp/bootcamp) を提供しております。  
数十名在籍しているデータサイエンティストや機械学習エンジニアに質問し放題の環境でデータ分析、統計、機械学習、SQL等が学べます。AI人材に必要なスキルを効率よく体系的に身に付けたい方は是非ご検討ください！  
[![bootcamp_ad_72ppi.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/195675/f261ccc8-42db-a292-2511-6a742d1987f7.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F195675%2Ff261ccc8-42db-a292-2511-6a742d1987f7.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=83f55ec21cb98fd82d99d85ddf032a03)  
[https://aiacademy.jp/bootcamp](https://aiacademy.jp/bootcamp)

## この記事を書いた人

[株式会社エーアイアカデミー](https://aiacademy.co.jp/)  
代表取締役CEO　谷 一徳  
フォローお待ちしております！  
[Twitter](https://twitter.com/tankazunori0914)  
11,000名以上が参加しいてるAIコミュニティも運営しております。  
毎日AIに関する情報を提供しておりますので、こちらのご参加もお待ちしております！  
[人工知能研究コミュニティ](https://www.facebook.com/groups/aiacademy.jp)

[8](https://qiita.com/tani_AI_Academy/items/#comments)

新規登録して、もっと便利にQiitaを使ってみよう

1. あなたにマッチした記事をお届けします
2. 便利な情報をあとで効率的に読み返せます
3. ダークテーマを利用できます
[ログインすると使える機能について](https://help.qiita.com/ja/articles/qiita-login-user)

[新規登録](https://qiita.com/signup?callback_action=login_or_signup&redirect_to=%2Ftani_AI_Academy%2Fitems%2F4da02cb056646ba43b9d&realm=qiita) [ログイン](https://qiita.com/login?callback_action=login_or_signup&redirect_to=%2Ftani_AI_Academy%2Fitems%2F4da02cb056646ba43b9d&realm=qiita)

[2666](https://qiita.com/tani_AI_Academy/items/4da02cb056646ba43b9d/likers)

3585
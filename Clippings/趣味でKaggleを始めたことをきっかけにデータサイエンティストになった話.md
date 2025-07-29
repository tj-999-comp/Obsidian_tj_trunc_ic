---
title: "趣味でKaggleを始めたことをきっかけにデータサイエンティストになった話"
source: "https://qiita.com/Muji___rushi/items/7d107c9561a461118f61"
author:
  - "[[Muji___rushi]]"
published: 2023-12-20
created: 2025-07-29
description:
tags:
  - "clippings"
  - "Kaggle"
---
![](https://relay-dsp.ad-m.asia/dmp/sync/bizmatrix?pid=c3ed207b574cf11376&d=x18o8hduaj&uid=4098794)

この記事は最終更新日から1年以上が経過しています。

Kaggleアドベントカレンダー2023の19日目の記事です．

## TL;DR

- データ分析未経験からkaggleでどんなことを学んだか
- 想像していたデータ分析と実業務とのGap
- kaggleやっていて良かったこと、kaggleでは学ばなかったこと

## はじめに

趣味でkaggleを始めたことをきっかけに、現在はデータ分析の仕事をしています。

[Muj!rush!](https://www.kaggle.com/mujrush)というアカウントでKaggleをしています。Kaggle expertです。

kaggleを始めてから3年程度経過したので(この3年間は、地球の公転が早まってんのかってくらい時間が経つのが早かったです)、これまでを振り返ることで、今後kaggleを始めてデータサイエンティストを目指すような方への参考になれば幸いです。

Kaggleと出会ったことで仕事への向き合い方や、今後のキャリアの考え方が変わったので、  
僭越ながら一言だけ言わせてもらうと、 **"kaggleは人生の役に立つ"** 。

[![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2982345/ab931ac8-0ae7-d670-bd55-03b6983d749c.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2982345%2Fab931ac8-0ae7-d670-bd55-03b6983d749c.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=a915346fc02d8f5861882e6735bc0862)

※記事にある画像は全てchatgpt4で生成されています

## バックグランド

2023年現在、社会人8年目で、去年まではインフラエンジニアでした。

インフラエンジニア時代は、基本的には上流工程の要件定義がメイン業務で、エンジニアとはいえ高度なインフラ技術を持ち合わせているわけではなく、それでいて肩書きは「インフラエンジニア」。  
**本当にエンジニアと名乗っていいのか？自分は何者なんだ？の答えのない問い** が日々ありました。

[![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2982345/1b9db80b-a873-3426-9f87-9164c5ad0098.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2982345%2F1b9db80b-a873-3426-9f87-9164c5ad0098.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=f8c2f8ed7e96ae59b8fdf510da248dad)

## Kagglerへの道のり

### 1年目（2021年)... Kaggleに出会う

2021年の元旦1/1に、何者かになるために、自分の興味があることを「 **1年間で1000時間以上学ぶルール」を作り、実行しました** 。1000時間あれば何かしらのプロフェッショナルに近けるんじゃないかという、かなり浅い理由です。

元々データ分析は未経験でしたが、AIは基礎教養として知っといた方がいいのかなと思い、「 [独学プログラマー Python言語の基本から仕事のやり方まで](https://www.amazon.co.jp/%E7%8B%AC%E5%AD%A6%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9E%E3%83%BC-Python%E8%A8%80%E8%AA%9E%E3%81%AE%E5%9F%BA%E6%9C%AC%E3%81%8B%E3%82%89%E4%BB%95%E4%BA%8B%E3%81%AE%E3%82%84%E3%82%8A%E6%96%B9%E3%81%BE%E3%81%A7-%E3%82%B3%E3%83%BC%E3%83%AA%E3%83%BC%E3%83%BB%E3%82%A2%E3%83%AB%E3%82%BD%E3%83%95/dp/4822292274) 」や、 [米国データサイエンティストがやさしく教えるデータサイエンスのためのPython講座](https://www.udemy.com/course/ds_for_python/learn/lecture/21513714?start=0#overview) など見てpythonは少し学習してました。

その頃にkaggleの存在を知り、データ分析ってなんか賢そうということで、 [kaggleスタートブック](https://www.amazon.co.jp/%E5%AE%9F%E8%B7%B5Data-Science%E3%82%B7%E3%83%AA%E3%83%BC%E3%82%BA-Python%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8BKaggle%E3%82%B9%E3%82%BF%E3%83%BC%E3%83%88%E3%83%96%E3%83%83%E3%82%AF-KS%E6%83%85%E5%A0%B1%E7%A7%91%E5%AD%A6%E5%B0%82%E9%96%80%E6%9B%B8-%E7%A5%A5%E5%A4%AA%E9%83%8E/dp/4065190061/ref=sr_1_1?adgrpid=103335507030&gclid=CjwKCAiA-P-rBhBEEiwAQEXhH1GJTyqUsam8o0cAkB_5NLTfUwrZtXdNecYSGL38YCEx2N67z25WMRoC45IQAvD_BwE&hvadid=665685685367&hvdev=c&hvlocphy=1028850&hvnetw=g&hvqmt=e&hvrand=17316910797125606278&hvtargid=kwd-894758536268&hydadcr=27489_14701155&jp-ad-ap=0&keywords=kaggle+%E3%82%B9%E3%82%BF%E3%83%BC%E3%83%88%E3%83%96%E3%83%83%E3%82%AF&qid=1702908956&sr=8-1) や [kaggle本](https://www.amazon.co.jp/Kaggle%E3%81%A7%E5%8B%9D%E3%81%A4%E3%83%87%E3%83%BC%E3%82%BF%E5%88%86%E6%9E%90%E3%81%AE%E6%8A%80%E8%A1%93-%E9%96%80%E8%84%87-%E5%A4%A7%E8%BC%94/dp/4297108437/ref=sr_1_2?adgrpid=103335507030&gclid=CjwKCAiA-P-rBhBEEiwAQEXhH1GJTyqUsam8o0cAkB_5NLTfUwrZtXdNecYSGL38YCEx2N67z25WMRoC45IQAvD_BwE&hvadid=665685685367&hvdev=c&hvlocphy=1028850&hvnetw=g&hvqmt=e&hvrand=17316910797125606278&hvtargid=kwd-894758536268&hydadcr=27489_14701155&jp-ad-ap=0&keywords=kaggle+%E3%82%B9%E3%82%BF%E3%83%BC%E3%83%88%E3%83%96%E3%83%83%E3%82%AF&qid=1702908956&sr=8-2) などkaggle関連の本を数冊買って、kaggleを始めました。

**それでも最初の数ヶ月は、コンペでの具体的な議論や公開コードを見ても、全く理解できませんでした** 。

このため、まずは **基礎を身につけるために、kaggleで毎月開催されていた [Tabular Playground Series](https://www.kaggle.com/competitions/tabular-playground-series-apr-2021) に参加** して、テーブルデータの読み込みから予測までの実装を一通り写経することを繰り返していました。

そんな中、 [CommonLit Readability Prize](https://www.kaggle.com/c/commonlitreadabilityprize) というNLPコンペで、わけもわからず公開コードを適当にコピペしてアンサンブルの重みを変えたら、 **初めて銅メダルが取れました** 。  
当時は、「なんか銅色の丸が付いたけど、何コレ」みたいな感覚で、kaggleの楽しみ方すらわかっていない状況でした。

[![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2982345/b8127e94-1d75-54d6-9468-5071fa8a8612.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2982345%2Fb8127e94-1d75-54d6-9468-5071fa8a8612.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=bfc527e007fc06b2c041decc6f4015e2)

### 2年目（2022年）... Kaggleにハマる

2022年の1月に参加してた [Jigsaw Rate Severity of Toxic Comments](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/overview) という、文章が有害かどうかを分類するNLPコンペで **たまたま1submitで銀メダルがとれました** 。その時の模様は昨年のKaggle Advent Calendar 2022の [こちらの記事](https://qiita.com/Muji___rushi/items/d93384a6e1e3a5adabba) に書いています。

それ以降、NLP関連のコンペに参加して、Kaggle Discussionみて手法を学び、それを実践したらスコアが少しずつ上がっていきました。 **kaggleにおける'活用'と'探索'を繰り返している時期** で、大袈裟ですが、当時は **1日単位で新しい知識が身についているような感覚** があり、純粋に知らないことを学ぶのがとても楽しかったです。

**当時は、仕事終わった直後に体力回復のため2,3時間寝て、夜に起きてkaggleやって深夜の3,4時に寝る、という生活を数ヶ月続けてました** 。コンペ終盤は学習が終わる時間帯に夜中に起きて、別の学習を回してまた寝る、というモデルの学習時間に生活リズムがコントロールされている状況でした(既にAIに人間の生活が支配されてる、、)

当時の仕事はデータ分析やプログラミングとは一切関係なかったので、まだまだ実力不足と思いながらも **次第に仕事でデータ分析できたらいいなと思い始めました** 。このため、社内制度を使って異動希望を出したところ、無事に翌年から社内異動することが決定しました。

ちなみに、2年目もインプット1000時間ルールは継続実行していました(とはいえkaggleのdiscussion見る時間とかも含む)

[![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2982345/161b399c-94e2-f029-1509-61e7eab9d285.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2982345%2F161b399c-94e2-f029-1509-61e7eab9d285.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=e990aa1eb4be26eff904ea42128a3522)

### 3年目（2023年）... データサイエンティストになる

2023年2月からデータサイエンティストになりました。  
とにかく、世の中のKagglerに恥じないように頑張る、というモチベーションでした。  
[![スクリーンショット 2023-12-19 22.26.01.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2982345/1146ec0d-e802-08d5-e44e-e841c67f2bbd.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2982345%2F1146ec0d-e802-08d5-e44e-e841c67f2bbd.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=9ac7b2d784c83a3098f4f7956590c79f)

業務では、レコメンドなどを用いてユーザの行動変容を促す機械学習プロダクトなど、複数の分析チームの一員になりました。  
それまで、1人でPC画面の向かってデータについてあれこれ考えていたので、配属当初は生身の人間とデータ分析に関する会話を出来てるだけでとても楽しかった記憶があります。

また、 **プロダクトからどんな価値を出していくか、そのためにAPIのインターフェイスをどう設計するか、コールドスタートなどの機械学習の普遍的な課題対処** というようなことを日々検討しており(データサイエンティスト、アナリスト、機械学習エンジニア全部をやるイメージ)

商用化前のプロダクトについては、 **モデルの学習にはどんなデータが必要か、どれくらいデータがあればいいか、どうやって効果検証するか** 、なども考えます。

データ分析コンペへの参加も継続していて、 [KDDCUP2023](https://www.aicrowd.com/challenges/amazon-kdd-cup-23-multilingual-recommendation-challenge) (データマイニング国際会議であるKDDのワークショップ)に会社として参加して、 **幸運にも9位入賞してアメリカ現地発表(ポスター)と論文投稿** を行うことができました。また、位置情報系の国際会議である [SIGSPATIAL2023](https://sigspatial2023.sigspatial.org/) のワークショップ形式コンペ([HuMob Challenge 2023](https://connection.mit.edu/humob-challenge-2023))に会社の同僚とプライベートで参加して、 **3位入賞してドイツ現地にて発表する経験が出来ました** (優秀な会社の後輩のおかげ)。  
その他、kaggleでもOTTO, 火山コンペなどにも参加してNLPコンペ以外でも多く学ぶことができました。

ちなみに、3年目はインプットルールは撤廃しました（既に学ぶ習慣がついていたため）

[![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2982345/0c516da9-3d94-a3d0-f340-75e5980286d4.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2982345%2F0c516da9-3d94-a3d0-f340-75e5980286d4.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=706f4f0f2cb785d3bd2f90e2fd5c61ff)

## 想像していたデータ分析と実業務とのGap

- **データが生み出す価値を本気で考える** 。現場の課題に対してデータを使ってどんな価値を創れるを本気で考える経験もできました。
- **どんなデータを使うかは自分次第** 。社内データウェアハウスにあるデータを探すところから行う必要があります。もちろん、データ活用時には適切な社内決済をとります。
- **モデリングはデータサイエンスの一部** 。こちらは、kaggle始めた時からよく耳にしていたので、実際の業務でもモデリング検討時間は限られていますが、想定内でした。
- **Kaggleの外にも優秀なデータサイエンティストはたくさんいる** 。当たり前ですが、Kaggleの外にも優秀なデータサイエンティストがいるので、その方達と分析議論できるのは、とても大事な経験になっています

**総じてポジティブなGapしかなく** 、思い切って社内異動して本当に良かったと感じています。

## Kaggleやっていて良かったこと

- **知らないことも学べばいいだけマインド** 。多くのkagglerが、当たり前のように高度なモデルや手法を使いこなすしているので、自分もこれまで知らないモデルや手法であっても、特にハードルを感じずに実装を試すようになりました。結果的に自然とできることの幅が広がったように思います。
- **常にこれでいいかを自分に問い続ける** 。明日から強いKagglerが同じチームにきても恥ずかしくない精度か？を問うようになります。
- **課題やデータセットごとのベースラインや手法をアクセスできるようになる** 。上位解法を覚えてなくても参照先はわかる状態。レコメンドならこのコンペ、ベーシックなNLPならあのコンペ見ればきっと有益な情報あるはず、など。

## Kaggleでは学ばなかったこと

- **AWSなどのクラウド知識** 。クラウド知識は割と必須の知識になるかと思うので、業務の前に個人アプリ開発などを行い基礎知識は身につけておけば良かったと思いました（今からでも遅くないことは内緒です）
- **Gitなどチーム開発の知識** 。ソロ参加が多く必要性も感じなかったので仕事を始めてから学ぶようになりました（Kaggleでもチーム参加などで学ぶ機会はあると思います）
- **精度向上に対する費用対効果** 。業務を始めて、kaggleでもコンペ初期ベースラインと最終1位のスコア差や実装量などが気になるようになりました。

でも、大丈夫です、「 **知らないことも学べばいいだけ** 」なので。

## 最後に

Kaggleを始めたことで、 **自分の趣味を仕事にすることができ、キャリアについても自ら切り開いていくものだと気づき、実行できました** (それまでは、自発的に手を挙げて社内異動するような性格ではなかったです)

Kaggleを始める前に望んでいた、 **何者かになれたかはわかりませんが、データ分析を続けていくことで、きっと何者かになれるんじゃないかという希望があります** 。

Kaggleも業務もまだまだ発展途上なので、これからも成長して行きます！  
(2024年はKaggle Master目指して頑張ります)

[![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2982345/74c9794a-4efd-3beb-7eb8-603f4f10445a.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2982345%2F74c9794a-4efd-3beb-7eb8-603f4f10445a.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=d23be288d1d98ae133fe00375b0df800)

[1](https://qiita.com/Muji___rushi/items/#comments)

コメント一覧へ移動

[241](https://qiita.com/Muji___rushi/items/7d107c9561a461118f61/likers)

いいねしたユーザー一覧へ移動

188
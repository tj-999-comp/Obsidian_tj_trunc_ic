---
title: 統計Web_Step0_8
source: https://bellcurve.jp/statistics/course/20171.html
author:
  - "[[統計WEB]]"
published: 2019-02-12
created: 2025-06-02
description: 
tags:
  - clippings
  - Data_Science
  - Statistics
---
- Step0. 初級編
	- 8\. 確率の計算
		- [8-1.確率を求めてみよう](#8-1.確率を求めてみよう)
		- [8-2.いろいろな確率を求めよう](#8-2.いろいろな確率を求めよう)
		- [8-3.条件付き確率を求めてみよう](#8-3.条件付き確率を求めてみよう)

# 8-1.確率を求めてみよう
赤い葉や黄色い葉が美しく色づく11月―――学習発表会に向けて、歌や合奏の練習に熱が入ります。ちょうど先週、1年生の合唱曲が「世界中のこねこたちが」に決まったのです。

次の表は、1年生の合唱曲の候補となっていた曲をまとめたものです。

| 候補No. | 曲名 |
| --- | --- |
| 1 | 気球に乗ってどこへでも |
| 2 | おさんぽ |
| 3 | 世界中のこねこたちが |
| 4 | 肉球を太陽に |
| 5 | 歌えにゃんにゃん |
| 6 | 恐竜のバラード |

これらの候補曲の中から1曲が1年生の合唱曲として選ばれる確率について考えてみます。「確率」とは、物事の「起こりやすさ」を定量的に表す指標のことです。また、この「物事」のことを「事象（じしょう）」といいます。

いくつかの事象の起こりやすさがすべて等しいとき、「同様に確からしい」といいます。このとき、ある事象Aが起こる確率P(A)は次の式から計算できます。
$$\displaystyle P(A)=\frac{k}{N}$$
<!--![ \displaystyle P(A)=\frac{k}{N} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-69767a7cb86941b007ce4fdfa3002812_l3.svg "Rendered by QuickLaTeX.com"-->

Nは「起こりうるすべての場合の数」を、kは「事象Aが起こる場合の数」を表しています。

合唱曲は、この6曲の中からくじ引きで決めました。したがって、6曲のうちどの曲が選ばれる確率も等しいと考えられます。この6曲の中から「世界中のこねこたちが」が選ばれる（＝事象A）という確率（$＝P(A)$）は、

- 「起こりうるすべての場合の数」＝「候補曲の数」＝「6」
- 「事象Aが起こる場合の数」＝「『世界中のこねこたちが』が選ばれる場合の数」＝「1」

を用いて
$$ \displaystyle P(A)=\frac{1}{6}  $$

<!--![ \displaystyle P(A)=\frac{1}{6} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-7207d2b85341ccbec4f1a140a66c5423_l3.svg "Rendered by QuickLaTeX.com") -->

と計算できます。


合唱曲が無事に決まったので、次に指揮者を決めることになりました。指揮者は立候補制で、8匹の猫たちが立候補をしました（くろ、たま、ぶち、モカ、みみ、まる、ぷく、もも）。この中からくじ引きで1匹を選びました。このとき、「ぷく」が選ばれる確率P(A)は

$$\displaystyle P(A)=\frac{1}{8}$$
<!-- ![ \displaystyle P(A)=\frac{1}{8} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-0cbcdbcf84e82eee2c0617888e6cb4db_l3.svg "Rendered by QuickLaTeX.com" -->

となります。

また、合唱の伴奏者も決めました。立候補した4匹の猫（しろ、みけ、そら、うみ）の中からくじ引きで2匹を選びました。

4匹の中から2匹が選ばれるすべて場合の数は、次の表で示すとおり6です。

| 組み合わせNo. | 伴奏者 |
| --- | --- |
| 1 | しろ－みけ |
| 2 | しろ－そら |
| 3 | しろ－うみ |
| 4 | みけ－そら |
| 5 | みけ－うみ |
| 6 | そら－うみ |

このとき、「しろ」と「みけ」が選ばれる確率P(A)は
$$\displaystyle P(A) = \frac{1}{6}$$

<!--[ \displaystyle P(A) = \frac{1}{6} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-4317325d3f20d8e2f693c7a4a3a03120_l3.svg "Rendered by QuickLaTeX.com")-->

となります。

# 8-2.いろいろな確率を求めよう
合唱の練習と並行して、合奏の練習も行わなくてはなりません。そこで1年生100匹が音楽室に集まり、どの楽器を担当するかを決めることになりました。

次の表は、1年生100匹の楽器の割り当てをまとめたものです。

| 楽器 | 割り当て匹数 |
| --- | --- |
| ピアニカ | 53 |
| タンバリン | 12 |
| すず | 10 |
| カスタネット | 15 |
| 木琴 | 7 |
| 小太鼓 | 2 |
| 大太鼓 | 1 |

上に挙げた7種類の楽器の中から担当する楽器がランダムに選ばれる場合、ある猫が担当する楽器がタンバリンである確率P(A)は次のように計算できます。
$$ \displaystyle P(A) = \frac{12}{100} = \frac{3}{25}$$
<!--
![ \displaystyle P(A) = \frac{12}{100} = \frac{3}{25} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-437354b96aa50faeae6cfd6e23705006_l3.svg "Rendered by QuickLaTeX.com")
-->
また、ある猫が担当する楽器がタンバリン以外である確率は次のようになります。

ただし、「事象Aが起こる確率」は「1-事象Aが起こらない確率」として計算することができます。つまり、「ある猫が担当する楽器がタンバリン以外である確率」＝「1-『ある猫が担当する楽器がタンバリンである確率』」となるので、
$$\displaystyle P(A) = 1- \frac{3}{25} = \frac{22}{25} $$
<!--
![ \displaystyle P(A) = 1- \frac{3}{25} = \frac{22}{25} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-3e7537838fe29d25b7803c3157e291eb_l3.svg "Rendered by QuickLaTeX.com")
-->
と計算することもできます。

音楽室の隅に、小太鼓と大太鼓を希望する猫たちが集まってきました。小太鼓は2匹、大太鼓は1匹が担当できます。小太鼓を希望する猫は4匹（もち、ふく、あずき、しま）、大太鼓を希望する猫も4匹（のっぽ、ぶち、だいず、たま）のようです。実は「あずき」と「だいず」は双子の猫です。この2匹がそれぞれ小太鼓と大太鼓を担当する確率を求めてみます。

「もち、ふく、あずき、しま」の中から、2匹が選ばれるすべての組み合わせは「もち-ふく」「もち-あずき」「もち-しま」「ふく-あずき」「ふく-しま」「あずき-しま」の6通りです。このうち「あずき」が含まれるのは3通りなので、小太鼓希望の「あずき」が小太鼓担当となる確率P(A)は、次のようになります。
$$ \displaystyle P(A) = \frac{3}{6} = \frac{1}{2} $$
<!--
![ \displaystyle P(A) = \frac{3}{6} = \frac{1}{2} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-51410c6a273c5d81cf7fef8ab55d80bb_l3.svg "Rendered by QuickLaTeX.com")
-->
また、大太鼓希望の「だいず」が大太鼓担当となる確率P(A)は、次のようになります。
$$ \displaystyle P(A) = \frac{1}{4}$$
<!--
![ \displaystyle P(A) = \frac{1}{4} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-4c05f6f20ebd7626f616151831dfe1d4_l3.svg "Rendered by QuickLaTeX.com")
-->
小太鼓担当は小太鼓希望の4匹の猫だけで、大太鼓担当は大太鼓希望の4匹の猫だけで決めるので、小太鼓の担当猫決めの結果が大太鼓の担当猫決めの結果に影響を与えることはありません。同様に、大太鼓の担当猫決めの結果が小太鼓の担当猫決めの結果に影響を与えることはありません。このように、お互いの結果が影響しあうことがないとき、2つの事象は「独立である」と言います。

2つの事象が独立である場合、2つの事象が同時に起こる確率はそれぞれの事象の確率の積で計算することができます。したがって、「あずき」と「だいず」がそれぞれ小太鼓と大太鼓を担当する確率は次のようになります。
$$\displaystyle P(A) = \frac{1}{2} \times \frac{1}{4} = \frac{1}{8}$$
<!--
![ \displaystyle P(A) = \frac{1}{2} \times \frac{1}{4} = \frac{1}{8} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-5c54379c4c6a8f11f978da69b2083bbc_l3.svg "Rendered by QuickLaTeX.com")
-->
一方、木琴を希望する猫たちは全部で8匹いるようです。公平にじゃんけんをしてみた結果、6匹が勝ち、2匹（とら、ちゃちゃ）が負けてしまいました。残り1匹の木琴担当をかけて、2匹でじゃんけんを続けることになりました。

ただし、2匹の間で「じゃんけんで先に2回勝った方を勝ちとする。じゃんけんは勝負がつくまで行う（あいこは無し）。」という取り決めが交わされました。じゃんけん1回ごとの結果はそれぞれ「独立」なので、じゃんけんを繰り返し行った結果の確率は、1回ごとの結果の確率の積で求めることができます。じゃんけんを1回行うとき、「とらが勝つ確率」＝「ちゃちゃが勝つ確率」＝です。

ここではとらが勝つ確率について求めてみます。この場合、①とらが2連勝する、もしくは、②とらが2勝1敗する、のどちらかになります。

- ①とらが2連勝する場合
$$\displaystyle P(A) = \frac{1}{2} \times \frac{1}{2} = \frac{1}{4}$$
<!--
![ \displaystyle P(A) = \frac{1}{2} \times \frac{1}{2} = \frac{1}{4} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-02ca8e6cd202fadb9e1745b113bbd975_l3.svg "Rendered by QuickLaTeX.com")
-->
- ②とらが2勝1敗する場合

	とらが2勝1敗する場合というのは、3回目のじゃんけんでとらの勝ちが決まる場合です。この場合、次の2パターンが考えられます。
	- 勝ち－負け－勝ち
	- 負け－勝ち－勝ち
	それぞれのパターンの確率は、次のように計算できます。
$$\displaystyle P(A) = \frac{1}{2} \times \frac{1}{2} \times \frac{1}{2}= \frac{1}{8}$$
<!--
![ \displaystyle P(A) = \frac{1}{2} \times \frac{1}{2} \times \frac{1}{2}= \frac{1}{8} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-8f421937dd0d69b592413c2a11490f79_l3.svg "Rendered by QuickLaTeX.com")
-->
したがって、とらが勝つ確率は、①と②の確率をすべて足して
$$ \displaystyle P(A) = \frac{1}{4} + \frac{1}{8} + \frac{1}{8} = \frac{4}{8} = \frac{1}{2} $$
<!--
![ \displaystyle P(A) = \frac{1}{4} + \frac{1}{8} + \frac{1}{8} = \frac{4}{8} = \frac{1}{2} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-96f9020cc8f861378f472845824c8c3f_l3.svg "Rendered by QuickLaTeX.com")
-->
となります。

# 8-3.条件付き確率を求めてみよう
学習発表会は猛練習のおかげで大成功だったようです。本番直前は緊張のあまりぶるぶると震えている猫たちがたくさんいましたが、観客から割れんばかりの拍手をもらうと皆満面の笑顔を浮かべてステージを後にしたのでした。

1年生は他の学年の発表も食い入るように見つめ、大いに興味を持ったようです。次の表は1年生100匹が来年の学習発表会でやってみたいと思ったことを集計したものです。

| 演目     | オス  | メス  |
| ------ | --- | --- |
| 劇      | 10  | 10  |
| ダンス    | 15  | 15  |
| 和太鼓    | 25  | 2   |
| ミュージカル | 5   | 10  |
| 群読     | 5   | 3   |
| 合計     | 60  | 40  |

この結果を元に、100匹の中からランダムに選ばれた1匹が「劇をやってみたい」と答える確率は次のように計算できます。
$$ \displaystyle \frac{10+10}{100} = \frac{20}{100} = \frac{1}{5}$$
<!--
![ \displaystyle \frac{10+10}{100} = \frac{20}{100} = \frac{1}{5} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-85ee4bb479ce457f1a818f3f1d41a8df_l3.svg "Rendered by QuickLaTeX.com")
-->
もし、100匹の中からランダムに選ばれた1匹がオスであったときに、その1匹が「劇をやってみたい」と答える確率は次のように計算できます。
$$\displaystyle \frac{10}{60} = \frac{1}{6} $$
<!--
![ \displaystyle \frac{10}{60} = \frac{1}{6} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-e206234b71dc640c01f70fe22875c309_l3.svg "Rendered by QuickLaTeX.com")
-->
このように、何か条件がある場合の確率のことを「条件付き確率」といいます。条件付き確率は次の式から求められます。
$$\displaystyle P(B|A) = \frac{P(A \cap B)}{P(A)}$$
<!--
![ \displaystyle P(B|A) = \frac{P(A \cap B)}{P(A)} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-4dba7eabb0555453452b534f21c84870_l3.svg "Rendered by QuickLaTeX.com")
-->
このとき、P(B|A)は「Aという条件のもとでBが起こる確率」を、P(A∩B)は「AかつBが起こる確率」を、P(A)は「Aが起こる確率」を表します。
上に挙げた結果を使って実際に計算してみます。100匹の中からランダムに選ばれた1匹がオスであったとき（Aという事象とします）に、選ばれた1匹が「劇をやってみたい」と答える（Bという事象とします）確率をP(B|A)とします。ランダムに選ばれた1匹がオスである確率P(A)は
$$\displaystyle P(A)= \frac{60}{100} = \frac{3}{5}$$
<!--
![ \displaystyle P(A)= \frac{60}{100} = \frac{3}{5} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-ee0841704b971e670fd31e0c1ede4b64_l3.svg "Rendered by QuickLaTeX.com")
-->
であり、ランダムに選ばれた1匹が「オス」かつ「劇をやってみたい」と答える確率P(A∩B)は、
$$\displaystyle P(A \cap B)= \frac{10}{100} = \frac{1}{10} $$
<!--
![ \displaystyle P(A \cap B)= \frac{10}{100} = \frac{1}{10} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-606e6611ff2f671ee67842f514d85835_l3.svg "Rendered by QuickLaTeX.com")
-->
であることから、求める確率P(B|A)は次のように計算できます。
$$ \displaystyle P(B|A)= \frac{\frac{1}{10}}{\frac{3}{5}} = \frac{1}{6}$$
<!--
![ \displaystyle P(B|A)= \frac{\frac{1}{10}}{\frac{3}{5}} = \frac{1}{6} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-f124e5c4083660a81cc73ff3df1b4a2d_l3.svg "Rendered by QuickLaTeX.com")
-->
同様にして、100匹の中からランダムに選ばれた1匹が「ダンスをやってみたい」と答えるとき（Aという事象とします）、選ばれた1匹がメスである（Bという事象とします）確率P(B|A)を求めると、
$$\displaystyle P(B|A) = \frac{\frac{15}{100}}{\frac{15+15}{100}} = \frac{\frac{15}{100}}{\frac{30}{100}} = \frac{1}{2}$$
<!--
![ \displaystyle P(B|A) = \frac{\frac{15}{100}}{\frac{15+15}{100}} = \frac{\frac{15}{100}}{\frac{30}{100}} = \frac{1}{2} ](https://bellcurve.jp/statistics/wp-content/ql-cache/quicklatex.com-b494239b4fe0b6eeda73c051f1493de6_l3.svg "Rendered by QuickLaTeX.com")
-->
となります。

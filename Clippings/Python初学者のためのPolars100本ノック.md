---
title: "Python初学者のためのPolars100本ノック"
source: "https://qiita.com/kunishou/items/1386d14a136f585e504e"
author:
  - "[[kunishou]]"
published: 2023-02-12
created: 2025-08-26
description:
tags:
  - "clippings"
  - "Data_Science"
  - "Machine_Learning"
---
![](https://relay-dsp.ad-m.asia/dmp/sync/bizmatrix?pid=c3ed207b574cf11376&d=x18o8hduaj&uid=4098794)

この記事は最終更新日から1年以上が経過しています。

**Information**

**2024/1/8：**  
pandas, Polars など18を超えるライブラリを統一記法で扱える統合データ処理ライブラリ Ibis の100 本ノックを作成しました。長期目線でとてもメリットのあるライブラリです。こちらも興味があればご覧下さい。

Ibis 100 本ノック  
[https://qiita.com/kunishou/items/e0244aa2194af8a1fee9](https://qiita.com/kunishou/items/e0244aa2194af8a1fee9)

## はじめに

どうもこんにちは、kunishouです。  
  
この度、PythonライブラリであるPolarsを効率的に学ぶためのコンテンツとして ***「Python初学者のためのPolars100本ノック」*** を作成したので公開します。こちらは2020年9月に公開した [「Python初学者のためのpandas100本ノック」](https://qiita.com/kunishou/items/bd5fad9a334f4f5be51c) の問題内容をPolarsのメソッドに合わせて修正、再編したものになります。本コンテンツに取り組むことでPolarsを用いたひと通りのデータ前処理などを実施できるようになります。また、本コンテンツでは **Google Colab版も用意しているため、PCとインターネット環境があれば、Python環境を構築することなくすぐにコンテンツを利用することができます。**

**以下に、コンテンツのイメージ動画を載せておきます**  
※動画は過去に作成したpandas100本ノックのものであり、今回ランダムノック版は作成していません  
  

![](https://www.youtube.com/watch?v=apYJZbiM_D4)

## 作成の動機

2022年末に [「2022年 Python/データ分析関連の人気Qiita記事150選」](https://qiita.com/kunishou/items/2c46cf71c62a22945288) という記事を書かせていただきましたが、その150選にPolarsに関する記事が何本か入っていたことからPolarsというライブラリの存在を知り、どのようなライブラリなのか気になっていました。そんなことを思いながら2023年になりましたが、ちょうどKaggleでも大規模データを扱う推薦コンペでPolarsが活躍しているという話も聞こえてきました。現時点ではPolarsに特化した技術書籍などは出ておらず、手を動かして網羅的にPolarsを学習できるコンテンツもなかったことから、今回 Polars版の100本ノックを作ることにしました。

なお、今回の100本ノックを作成するにあたり、 [@shoku\_pan\_pan](https://twitter.com/shoku_pan_pan) さんより100本ノック化のアイディアをご提供いただき、また、作成した解答内容に誤りがないかのチェックの部分で [@yshr10ic](https://twitter.com/yshr_10ic) さんにご協力いただきました。誠にありがとうございました。

## Polarsとは

[![polars_github_logo_rect_dark_name.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/692165/29faf5ce-85f9-ba4c-2a31-74bd6bf08fc9.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F692165%2F29faf5ce-85f9-ba4c-2a31-74bd6bf08fc9.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=ee5354b5f4d330f3eb538922f3ba2fe5)  
Polarsとは、Pythonで高速にデータフレームを操作することが可能なライブラリになります。同様の処理をするライブラリとしてはpandasが有名ですが、pandasが比較的小規模なデータ向けで、Numpy配列でデータを持つ構造になっているのに対し、PolarsはRustベースで作成され、Apache Arrow memory modelという列指向のデータ構造になっているため、大規模データを高速に処理することが可能になっています。処理できるデータとしてはcsvをはじめ、jsonやApache Parquetなど多くの形式のデータを扱うことができます。また、APIがApache Sparkに似ているため、PySparkを使う方にとっては書きやすいようです。

- [Polars公式リファレンス](https://pola-rs.github.io/polars/py-polars/html/reference/index.html)
- [Polars公式ガイド](https://pola-rs.github.io/polars-book/user-guide/)
- [Github](https://github.com/pola-rs/polars)

処理速度がpandasとどれぐらい違うのかについては以下の記事を参考にして下さい（Kaggle Masterのざこぷろさんの記事です）。

- [pandas vs polars vs cudf 速度比較](https://zakopilo.hatenablog.jp/entry/2023/02/04/220552)

## Polars100本ノックの概要

#### Polars\_100\_knocks

- Notebook上のセルに記載されたPolarsメソッドに関する設問100問を解いていきます（タイタニック号の乗客データ等の実在するデータに対してPolarsメソッドで処理を実行していきます）。
- GithubのレポジトリにはGoogle Colab版とローカルPC版の2つが用意してあり、Google Colab版であればPython環境の構築不要で、すぐにコンテンツを利用することが可能です。
- セクションは、基礎(1-14)、抽出(15-36)、加工(37-64)、マージと連結(65-73)、統計(74-87)、ラベリング(88-89)、タイタニック号乗客の生存予測(90-100)の7つに分かれています。

例えば、Notebookのセルに以下のような問題が記載されています。ここに解答コードを記入し、実行して処理結果を確認します。

```text
# 【6】
# dfのfareの列で昇順に並び替えて表示
#print(ans[6]) #解答表示
df = initialize1() #初期化
```

解答を確認したい場合は、「#print(ans\[6\])」の「#」を削除して実行すると以下のように解答のコードやTipsを表示することができます。また、すべての解答に **pandasで書く場合の記法も載せています。**

```text
[answer6]

df.select(pl.all().sort_by('fare'))

----------------------------------------------

[Tips]
・要素でソートするときはsort_by()を使用
・デフォルトでは昇順
・降順でソートしたい場合は reverse=True を指定
・ソートする列を複数指定可能

ex) fare列で降順でソートした後にage列で降順にソートしたい場合は
　　以下のように書く
※ リスト内でage列を先に書く点に注意

df.select(pl.all().sort_by(['age', 'fare'], reverse=True))

・似たメソッドにsort()があるが、これはカラムごとに独立してソートされる点に注意
※ dataframe全体を前処理するようなときは基本的にsort_by()を使うのが良いと思います

ex) print(df.select(pl.col(['fare', 'age']).sort(reverse=True, nulls_last=True)).head())

実行結果)

sort()ではfare列、age列が独立してソートされているのが分かる

┌──────────┬──────┐
│ fare     ┆ age  │
│ ---      ┆ ---  │
│ f64      ┆ f64  │
╞══════════╪══════╡
│ 512.3292 ┆ 80.0 │
│ 512.3292 ┆ 76.0 │
│ 512.3292 ┆ 74.0 │
│ 512.3292 ┆ 71.0 │
│ 263.0    ┆ 71.0 │
└──────────┴──────┘

----------------------------------------------

[参考] pandas記法

df.sort_values('fare')
```

## 問題内容

| No. | 分類 | 問題 |
| --- | --- | --- |
| 1 | 基礎 | dfに読み込んだデータの最初の5行を表示 |
| 2 | 基礎 | glimpseを用いてdfに読み込んだデータの最初の要素10個を表示 |
| 3 | 基礎 | dfに読み込んだデータの最後の5行を表示 |
| 4 | 基礎 | dfのDataFrameサイズを確認 |
| 5 | 基礎 | inputフォルダ内のdata1.csvファイルを読み込みdf2に格納して、最初の5行を表示 |
| 6 | 基礎 | dfのfareの列で昇順に並び替えて表示 |
| 7 | 基礎 | df\_copyにdfをコピーして、最初の5行を表示 |
| 8 | 基礎 | ①dfの各列のデータ型を確認   ②dfのcabinの列のデータ型を確認 |
| 9 | 基礎 | ①dfのpclassの列のデータ型をschemaで確認   ②数値型から文字列型に変換し、データ型をschemaで確認 |
| 10 | 基礎 | dfのレコード数(行数)を確認 |
| 11 | 基礎 | dfのレコード数(行数)、各列のデータ型、欠損値の有無を確認 |
| 12 | 基礎 | dfのsex、cabinの列の要素を確認 |
| 13 | 基礎 | dfの列名一覧を表示 |
| 14 | 基礎 | dfのpclassの列をndarray形式で表示 |
| 15 | データ抽出 | selectを使ってdfのpclass列のみ表示 |
| 16 | データ抽出 | get\_columnを用いてdfのpclass列のみ表示 |
| 17 | データ抽出 | get\_columnsを用いてdfのpclass列のみ表示 |
| 18 | データ抽出 | selectを用いてdfのnameとsexの列のみ表示 |
| 19 | データ抽出 | get\_columnを用いてdfのnameとsexの列のみ表示 |
| 20 | データ抽出 | dfのname列以外を表示 |
| 21 | データ抽出 | dfの4行目までを表示   なお、確認のためにwith\_row\_countでインデックスを振る |
| 22 | データ抽出 | dfの4行目から10行目までを表示   なお、確認のためにwith\_row\_countで   インデックスを振る |
| 23 | データ抽出 | selectを使ってdf全体を表示 |
| 24 | データ抽出 | dfのnameからcabinまでの列を5行目まで表示 |
| 25 | データ抽出 | dfのname、age、sexの列のみ抽出しdf\_copyに格納   その後outputフォルダにcsvファイルで出力   出力ファイル名はsample.csv |
| 26 | データ抽出 | dfのage列の値が30以上のデータのみ抽出 |
| 27 | データ抽出 | dfのsex列がfemaleのデータのみ抽出 |
| 28 | データ抽出 | dfのsex列がfemaleでかつageが40以上のデータのみ抽出 |
| 29 | データ抽出 | dfのsex列がfemaleでかつageが40以上のデータを等号、不等号を使わずに抽出 |
| 30 | データ抽出 | dfのcabin列がnullでないデータを抽出 |
| 31 | データ抽出 | dfのage列が10以上、40以下のデータを等号、不等号を使わずに抽出 |
| 32 | データ抽出 | dfのname列に文字列「Mrs」が含まれるデータを表示 |
| 33 | データ抽出 | dfの中で文字列型の列のみを表示 |
| 34 | データ抽出 | dfの各列の要素数の確認 |
| 35 | データ抽出 | dfのembarked列の要素と出現回数の確認 |
| 36 | データ抽出 | dfのすべての列の要素と出現回数の確認 |
| 37 | データ加工 | dfにwith\_row\_count()でインデックスを振りrow\_nr列が「3」のage列を30から40に変更し、先頭の5行を表示 |
| 38 | データ加工 | dfのsex列にてmale→0、femlae→1に変更し、先頭の5行を表示 |
| 39 | データ加工 | dfのfare列に100を足して、先頭の5行を表示 |
| 40 | データ加工 | dfのfare列に2を掛けて、先頭の5行を表示 |
| 41 | データ加工 | dfのfare列に2を掛けて、age列に3を足して先頭の5行を表示 |
| 42 | データ加工 | applyを用いてdfのfare列に2を掛けて、age列に1を足して先頭の5行を表示 |
| 43 | データ加工 | dfのfare列を小数点以下で丸めて、先頭の5行を表示 |
| 44 | データ加工 | dfに列名「test」で値がすべて1のカラムを追加し、先頭の5行を表示 |
| 45 | データ加工 | dfに列名「test」で値がすべて1のカラムと列名「test2」で値がすべてnullのカラムを追加し、先頭の5行を表示 |
| 46 | データ加工 | dfにcabinとembarkedの列を「\_」で結合した列を追加(列名は「test」)し、先頭の5行を表示 |
| 47 | データ加工 | dfにageとembarkedの列を「\_」で結合した列を追加(列名は「test」)し、先頭の5行を表示 |
| 48 | データ加工 | dfにageとembarkedの列をconcat\_strを用いて「\_」で結合した列を追加(列名は「test」)し、先頭の5行を表示 |
| 49 | データ加工 | dfからbodyの列を削除し、最初の5行を表示 |
| 50 | データ加工 | dfにwith\_row\_count()でインデックスを振りrow\_nr列が「3」の行を削除し、最初の5行を表示 |
| 51 | データ加工 | df2の列名を'name'、'class'、'Biology'、'Physics'、'Chemistry'に変更   df2の最初の5行を表示 |
| 52 | データ加工 | df2の列名を'English'をBiology'に変更   df2の最初の5行を表示 |
| 53 | データ加工 | dfのすべての列の欠損値数を確認 |
| 54 | データ加工 | dfのage列の欠損値に30を代入   その後、ageの欠損値数を確認 |
| 55 | データ加工 | dfでひとつでも欠損値がある行を削除   その後、dfの欠損値数を確認 |
| 56 | データ加工 | dfのsurvivedの列をndarray形式(配列)で表示 |
| 57 | データ加工 | dfの行をシャッフルし、dfの最初の5行を表示 |
| 58 | データ加工 | ①df2の重複行数をカウント   ②df2の重複行を削除し、df2を表示 |
| 59 | データ加工 | dfのnameの列をすべて大文字に変換し表示 |
| 60 | データ加工 | dfのnameの列をすべて小文字に変換し表示 |
| 61 | データ加工 | dfのsex列に含まれる「female」という単語を「Python」に置換。その後、1行目の「female」が「Python」に置き換わったことを確認 |
| 62 | データ加工 | dfのname列1行目の「Allen、Miss.ElisabethWalton」の「Elisabeth」を消去(importreをインポート) |
| 63 | データ加工 | df5の都道府県列と市区町村列を空白がないように「\_」で結合(新規列名は「test2」)し、先頭5行を表示   ※df5の「test」列は通常通り結合した場合の結果 |
| 64 | データ加工 | df2の行と列を入れ替えて表示 |
| 65 | マージと連結 | df2にdf3を左結合（結合キーはname）し、df2に格納 |
| 66 | マージと連結 | df2にdf3を右結合（結合キーはname）し、df2に格納 |
| 67 | マージと連結 | df2にdf3を内部結合（結合キーはname）し、df2に格納 |
| 68 | マージと連結 | df2にdf3を外部結合し、df2に格納 |
| 69 | マージと連結 | df2にdf3を、df3にのみ存在するデータのみを残してて結合 |
| 70 | マージと連結 | df2にdf3を、df3に存在しないデータを残してて結合 |
| 71 | マージと連結 | df2とdf3のそれぞれの行を全通り組み合わせたdataframeを作成 |
| 72 | マージと連結 | df2とdf4を列方向に連結し、df2に格納 |
| 73 | マージと連結 | df2とdf4を行方向に連結し、df2に格納 |
| 74 | 統計 | dfのage列の平均値を確認 |
| 75 | 統計 | dfのage列の中央値を確認 |
| 76 | 統計 | ①df2の生徒ごとの合計点（行方向の合計）   ②df2の科目ごとの点数の総和（列方向の合計） |
| 77 | 統計 | df2のEnglishで得点の最大値 |
| 78 | 統計 | df2のEnglishで得点の最小値 |
| 79 | 統計 | df2においてclassでグルーピングし、クラスごとの科目の最大値、最小値、平均値を求める(name列は削除しておく) |
| 80 | 統計 | df2においてclassでグルーピングし、aggを用いて各科目の平均、最大値、最小値を求める   なお、各科目の平均、最大値、最小値には「\*\*\*\_mean」のようにsuffixを振ること |
| 81 | 統計 | dfの各列間の(Pearson)相関係数を確認 |
| 82 | 統計 | scikit-learnを用いてdf2のEnglish、Mathematics、History列を標準化する |
| 83 | 統計 | scikit-learnを用いてdf2のEnglish列を標準化する |
| 84 | 統計 | scikit-learnを用いてdf2のEnglish、Mathematics、History列をMin-Maxスケーリングする |
| 85 | 統計 | dfのfare列の最大値、最小値の行名を取得 |
| 86 | 統計 | dfのfare列の0、25、50、75、100パーセンタイルを取得 |
| 87 | 統計 | ①dfのage列の最頻値を取得   ②value\_counts()にてage列の要素数を確認し、①の結果の妥当性を確認 |
| 88 | ラベリング | dfのsex列をラベルエンコーディングし、dfの先頭5行を表示 |
| 89 | ラベリング | dfのsex列をOne-hotエンコーディングし、dfの先頭5行を表示 |
| 90 | タイタニック号の生存者予測 | df\_copyのsexとembarked列をラベルエンコーディング |
| 91 | タイタニック号の生存者予測 | df\_copyの欠損値を確認 |
| 92 | タイタニック号の生存者予測 | df\_copyのage、fare列の欠損値を各列の平均値で補完 |
| 93 | タイタニック号の生存者予測 | df\_copyの中で機械学習で使用しない不要な行を削除 |
| 94 | タイタニック号の生存者予測 | ①df\_copyのpclass、age、sex、fare、embarkedの列を抽出し、ndarray形式に変換   ②df\_copyのsurvivedの列を抽出し、ndarray形式に変換 |
| 96 | タイタニック号の生存者予測 | 学習データ(features、target)を用いランダムフォレストにて学習を実行 |
| 97 | タイタニック号の生存者予測 | test\_Xデータの乗客の生存を予測 |
| 98 | タイタニック号の生存者予測 | 予測結果がtest\_y(生存有無の答え)とどれぐらい整合していたかを確認(評価指標はaccuracy) |
| 99 | タイタニック号の生存者予測 | 学習における各列(特徴量)の重要度を表示 |
| 100 | タイタニック号の生存者予測 | test\_Xの予測結果をcsvでoutputフォルダに出力(ファイル名は「submission.csv」) |

## 利用方法

2通りの利用方法がありますが、Google Colab版ではPython環境を構築することなく利用可能なためおススメです。また、問題を解く前に以下の記事を一読しておくとより習熟しやすくなると思います。

## Google Colab版

[GitHub](https://github.com/kunishou/Polars_100_knocks) のページに移動し、「01\_Polars\_100\_Knocks\_for\_colab.ipynb」を開いたあとに、Colabリンクのアイコンをクリックする。以下のリンクからも直接Colabのページに移動できます。

- ipynbファイルを開いた後に、先頭のセルを実行すると解答ファイル、問題で使用するデータセットのダウンロードおよび読み込みがされます。使用するデータセットは、タイタニック号の乗客データ等になっています。
- 各設問のセル内に設問に対するコードを入力していきます。
- 答えが分からない場合は、設問セル内の「#print(ans\[\])」という記述から「#」を消して実行することで、解答例が表示されます。
- [「02\_Polars\_100\_Knocks\_for\_colab\_all\_answer\_displayed.ipynb」](https://github.com/kunishou/Polars_100_knocks/blob/main/02_Polars_100_Knocks_for_colab_all_answer_displayed.ipynb) ではすべての解答と出力結果を最初から表示しています。解答や出力結果をまとめて確認したいときにご活用下さい。 **Polarsを一度も触ったことのない方はまずこちらの解答全表示版のほうをさらっと流し見してひと通りメソッドを確認してみるのも良いと思います。**

## ローカルPC版

※Pythonをまだインストールしていない方は、以下の記事を参考に、まずAnacondaを自身のPCにインストールして下さい。問題内ではPandas以外にも、Scikit-learnなどのライブラリも使用します。

[5分で簡単！AnacondaでPython3をインストール(Windows/Mac編)](https://ai-inter1.com/python-install/)

- こちらの **[GitHubページ](https://github.com/kunishou/Polars_100_knocks)** よりZIPファイルをダウンロードした後に、自身のPCのローカル領域に展開する。
- 「notebook」フォルダに格納されているipynbファイルをJupyter Notebookで開く。
- Google Colab版と同様に先頭のセルを実行すると解答ファイル、問題で使用するデータセットが読み込まれます。以降はGoogle Colab版と同様の操作方法になります。

## ディレクトリ構成

Polars\_100\_knocks  
　├ notebook/　…　ipynbファイルが格納  
　├ input/ …　100問分の回答ファイル、問題で使用するデータセットが格納  
　└ output/ …　問題でファイル出力する際にここに格納  
　└ 01\_Polars\_100\_Knocks\_for\_colab.ipynb  
　└ 02\_Polars\_100\_Knocks\_for\_colab\_all\_answer\_displayed.ipynb

※ローカルPC上で実行する場合は、ZIPファイルから展開した後にこのディレクトリ構成は変えないで下さい（上手く動作しなくなります）。

## Polars100本ノック利用にあたっての留意点

- Python初学者が利用することを前提に作成しているため、内容は比較的簡易なものになっています。
- pandas100本ノックがもともと「Python3エンジニア 認定データ分析試験」の出題内容を意識して作成していたこともあり、Polars版は内容は網羅的になるよう再編したつもりですが今回紹介できていないメソッドもあります。
- **Polarsには、ひとつの処理をする場合でもいろいろな書き方があるため、ここに記載してる解答が唯一の解答ではありません** （ 例えば、selectを用いてデータ選択しているがget\_columnでも書けたりします）。
- 公式リファレンスの内容がまだまだ充実していないこともあり、冗長な書き方になっていると感じる解答も中にはあります。 **他にベストプラクティスな記法があれば知見を共有していただけると助かります。**

## 使用範囲／注意事項

- 使用範囲  
	個人・法人を問わず誰でも使用可能  
	(有志の勉強会や社内の研修で使う際、ご一報いただけると作者のモチベーションが上がります)
- 注意事項  
	コンテンツの再配布・改編は不可

## おわりに

今回、Polars100本ノックというコンテンツについて紹介させていただきました。  
本コンテンツに関して質問・要望があればご連絡下さい。

[8](https://qiita.com/kunishou/items/#comments)

コメント一覧へ移動

X（Twitter）でシェアする

Facebookでシェアする

はてなブックマークに追加する

[397](https://qiita.com/kunishou/items/1386d14a136f585e504e/likers)

いいねしたユーザー一覧へ移動

513
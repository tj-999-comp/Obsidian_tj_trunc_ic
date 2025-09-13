---
title: "PandasからPolarsへ移行した方がいいのか"
source: "https://qiita.com/inoshun/items/30e4e78cbf221bf11a86"
author:
  - "[[inoshun]]"
published: 2024-04-16
created: 2025-08-26
description:
tags:
  - "clippings"
---
![](https://relay-dsp.ad-m.asia/dmp/sync/bizmatrix?pid=c3ed207b574cf11376&d=x18o8hduaj&uid=4098794)

この記事は最終更新日から1年以上が経過しています。

## なぜこの記事を書くのか

皆さん、データ解析を行う際にどのようなライブラリを用いているでしょうか。  
おそらく大半の人は `pandas` を使っているのではないでしょうか。  
私もpandas使ってます。簡単だよね(´・ω・｀)

しかし、業務でバカクソでけえデータを読み込もうとしたときに、読み込み時間がとんでもなくかかったり、メモリ不足でそもそも読み込めもしないことが起きていました。  
読み込みにメモリ食われすぎて他の作業ができずに待機した挙句、燃え尽きたかのようにノーパソのファンが止まると同時にメモリ不足のエラーが出たときには切れ散らかします。

[![GJfbeNvaEAA2FPw.jpg](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/3524375/0e8c5849-cd0e-ff2e-dcae-cc16e87daa46.jpeg)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F3524375%2F0e8c5849-cd0e-ff2e-dcae-cc16e87daa46.jpeg?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=2e354ebfd7408368cecc572e16b7eb84)

（画像元： [葬送のフリーレン公式Xアカウントのポストより](https://twitter.com/FRIEREN_PR/status/1772126302994120747) ）

そんなこともあり、AWSなどのクラウドサービスでメモリに余裕を持たせるためにめちゃくちゃ良いインスタンスを使用していましたが、コストの問題で断念しました。  
しかし、どうしても読み込みたいということもあり、プログラミング言語の一種である `Julia言語` で読み込んだところ、爆速で読み込むことができました。

(/・ω・)/「今度からJulia使ってデータ解析しよう！社内の人にもJuliaを普及するか！」  
となっていましたが、JuliaではなくPythonから直接解決した方が良いのでは？と思い、 `Polars` の存在を思い出しました。  
前置きが長くなりました。ごめんなさい。  
ということで、JuliaではなくPolarsを採用することにしたので、Polarsの使用感についてまとめていったうえで、移行した方がいいのかについて触れていこうと思います。

## どっちがいいの？

Polarsとは、翻訳すると **白熊** になります。  
よくPolarsとPandasで性能の比較が行われていますが、どちらの方が優れているのでしょうか？

[![6d8bfc85-3063-4f32-b00b-95d6ef47fe3d.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/3524375/c1a23c78-12f3-011f-eefa-692e77711e9f.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F3524375%2Fc1a23c78-12f3-011f-eefa-692e77711e9f.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=298556bae5c45cab874a8e4e503d54ac)

白熊(オス)は体長200㎝~250㎝、体重340㎏~658㎏に対し、パンダ(オス)は体長120㎝~150㎝、体重100㎏です。  
また、白熊の主食はアザラシなどだそうですが、対するパンダは笹です。肉ですらないです。笹です。  
生物としてもパンダは白熊に勝てないのは明らかであって、PolarsとPandasを比較しても圧倒的な速度の差があり、ライブラリとしての性能もPolarsが圧勝しています。

[![069fd62d-afed-467b-8387-c6ba7cf1ad07.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/3524375/ef05c459-85a1-8417-bcd5-e2f4f38a91c5.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F3524375%2Fef05c459-85a1-8417-bcd5-e2f4f38a91c5.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=92dbb144e7f02975cf0b2b7ff806c529)

## Polarsの速度

では、どの程度の差があるのでしょうか。  
業務PCを用いたときの結果をメモした程度なので、信憑性はほとんどありませんが、約1GBのcsvファイルを読み込んだときの速度を比較したところ  
Polars：6秒  
Pandas：62秒  
でした。  
正直、かなり早い印象でした。  
公式サイトにも速度について触れられていますが、パフォーマンスがかなり高いことが分かります。

[![polars.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/3524375/e30b5531-d161-44de-7053-c14f637bda8a.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F3524375%2Fe30b5531-d161-44de-7053-c14f637bda8a.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=369743b55f137f4e457c80351f938c1c)

## Polarsの良いと感じた部分

私がPolarsを使用して、めっちゃいいなって感じたことを紹介します。

### Pandasライクな記法

Pandasに慣れている人からすると別のライブラリに移行するのは抵抗が…と思われるかもしれませんが、割とPandasに似ています。  
実際にどこまでPandasと同じ書き方で通用するか検証した方がいますので、是非記事の方覗いてみてください。  
私自身も使っていて、ここはPolars特有の書き方だな。ここはPandasと同じだな。って感じで使うことができたので、割と難なく使えると思っています。

### データフレームに型が表示されている。

Juliaもそうですが、データフレームを表示した際にデータの型が表示されています。

[![polars_df.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/3524375/cfe041b6-7819-8aef-24d7-7ab590152fba.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F3524375%2Fcfe041b6-7819-8aef-24d7-7ab590152fba.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=8e7cee0226f5262e301cf231493c31a9)

Pandasだと、type関数や `df.info()` で型を確認する必要がありますが、その手間が省けます。  
正直その程度ですが、型を頻繁に変換するような処理があるときにはデータフレームを表示するだけで確認できるのは非常に嬉しいと感じます。

## Polarsの悪いと感じた部分

簡単にまとめたいと思います。

- Polars特有の書き方に慣れる必要がある
- 欠損値の読み込み方などが面倒

ぐらいですかね。  
欠損値に関してはデータがおかしいだけなのかもしれませんが、csvファイルを読み込む時点で引数を指定する必要があったので、少し面倒だなと感じたことがあります（Pandasだと問題なく読み込めた）。  
機械学習のモデルを作成するときのデータの前処理にPolarsを用いて、問題なくモデル作成までいけるかについては現在検証中です。

## 結論

今までつらつらと文章を書き殴ってきましたが、結論移行した方がいいのか。  
**移行した方が良い** と感じています。  
理由としては、

1. 比較的新しいライブラリのため、今後の機能の拡充に期待できる
2. 今後、会社のデータは増えていくため、容量の大きなデータを扱う機会が増える
3. Pandasのパフォーマンスの低さから来るストレスから解放される

アップデート次第でもっと使いやすくなることは十分に期待できます。  
また、企業のデータ、特にメーカーはDXに力を入れ始めたのはここ2.3年の話です。  
私自身、メーカーに勤務していますが、データベースを用意できているメーカー企業なんてかなり少ないと感じているくらいには、DXが進んでいません。  
そのため、今後データベースに研究データや工場のプラントデータなどが溜まっていくと予想しています。  
そのときにPandasでは対応できないから、Polarsに移行しよう！となったときに移行まで時間がかかる可能性が高いです。  
移行しないにしても、早めにPolarsに慣れておくことは十分アリだと思います。  
最後に、ストレスからの解放ですね。  
早いは正義です。

## まとめ

いかがだったでしょうか。  
今回はPolarsについてまとめていきましたが、Polarsを実際に使ってみて良さを実感していただければと思います。  
Polarsの使い方がわからん！って方は以下を参考に練習してみてください。  
あとは `Claude3 Opus` が何とかしてくれます！  
それでは！！！

[6](https://qiita.com/inoshun/items/#comments)

コメント一覧へ移動

X（Twitter）でシェアする

Facebookでシェアする

はてなブックマークに追加する

[295](https://qiita.com/inoshun/items/30e4e78cbf221bf11a86/likers)

いいねしたユーザー一覧へ移動

304
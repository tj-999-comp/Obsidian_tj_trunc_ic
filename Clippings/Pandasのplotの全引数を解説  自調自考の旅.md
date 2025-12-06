---
title: Pandasのplotの全引数を解説 | 自調自考の旅
source: https://own-search-and-study.xyz/2016/08/03/pandas%E3%81%AEplot%E3%81%AE%E5%85%A8%E5%BC%95%E6%95%B0%E3%82%92%E4%BD%BF%E3%81%84%E3%81%93%E3%81%AA%E3%81%99/
author:
  - "[[Rosyuku]]"
published: 2016-08-03
created: 2025-09-17
description: Pythonモジュールのpandasにはplot関数があり、これを使えばpandasで読み込んだデータフレームを簡単に可視化することができます。特によく使うのは、kindやsubplotsですが、実に34個の引数があります。使いこなして、簡単にいろんなグラフを書きたいですね。
tags:
  - clippings
  - Machine_learning
  - Data_Science
---
## 概要

Pythonモジュールのpandasにはplot関数があり、これを使えばpandasで読み込んだデータフレームを簡単に可視化することができます。ただし、大量の引数（34個）があるにもかかわらず、 [公式マニュアル](http://pandas.pydata.org/pandas-docs/stable/pandas.pdf) を見ても引数の一部しか説明されておらず、一体何ができるのか整理したくなり、この記事を書きました。データはirisを使い、plotの各引数の効果を検証しました。

```
import pandas as pd
if __name__ == "__main__":   
    #元データ
    df = pd.read_csv('iris.csv', index_col=0)
```

## どんな引数があるのか？

df.plot?とヘルプを叩くことで、変数の一覧と説明（英語）を取得できます。実に34個の引数があるようです。使いこなして、簡単にいろんなグラフを書きたいですね。

| x | y | kind | lax |
| --- | --- | --- | --- |
| subplots | sharex | sharey | layout |
| figsize | use\_index | title | grid |
| legend | style | logx | logy |
| loglog | xticks | yticks | xlim |
| ylim | rot | fontsize | colormap |
| colorbar | position | table | yerr |
| xerr | stacked | sort\_columns | secondary\_y |
| mark\_right | kwds |  |  |

## デフォルトの結果

何も引数をつけずに、デフォルト設定でplotすると、以下のようなグラフが表示されます。以下では、この結果と比較していきます。

```
#引数なしの場合の結果
df.plot()
```

![f:id:Rosyuku:20160803233100p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803233100.png "f:id:Rosyuku:20160803233100p:plain")

## 各種変数を指定した場合の結果

## x

x軸の変数を指定する場合に使うパラメータ。デフォルトはNone（indexを使う）。以下では1つ目の変数(SepalLength)を指定しました。

```
df.plot(x=df.columns[0])
```

x軸は確かにSepalLengthになっています。  
![f:id:Rosyuku:20160803233549p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803233549.png "f:id:Rosyuku:20160803233549p:plain")

## y

プロットしたい変数を指定する場合に使うパラメータ。デフォルトはNone（全変数を使う）。以下では1つ目の変数(SepalLength)を指定しました。

```
df.plot(y=df.columns[0])
```

確かにSepalLengthのみプロットされています。  
![f:id:Rosyuku:20160803234025p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803234025.png "f:id:Rosyuku:20160803234025p:plain")

## kind

プロットするグラフの種類を指定するパラメータ。デフォルトはline（折れ線グラフ）。他にもbar, barh, hist, box, kde, density, area, pie, scatter, hexbin等が指定できるようです。

### line

デフォルト設定で書ける折れ線グラフです。

```
df.plot(kind='line')
#以下でも同様
df.plot.line()
```

![f:id:Rosyuku:20160803233100p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803233100.png "f:id:Rosyuku:20160803233100p:plain")

### bar

縦棒グラフ。

```
df.plot(kind='bar')
```

![f:id:Rosyuku:20160803235233p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235233.png "f:id:Rosyuku:20160803235233p:plain")

### barh

横棒グラフ。

```
df.plot(kind='barh')
```

![f:id:Rosyuku:20160803235257p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235257.png "f:id:Rosyuku:20160803235257p:plain")

### hist

ヒストグラム。

```
df.plot(kind='hist')
```

![f:id:Rosyuku:20160803235329p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235329.png "f:id:Rosyuku:20160803235329p:plain")

別のカラムで色分けを指定する方法を記事にしましたので併せて参考にしてみてください。

> [Pandasで目的変数別に色分けしたヒストグラムを作成する](http://own-search-and-study.xyz/2018/02/27/pandas%e3%81%a7%e7%9b%ae%e7%9a%84%e5%a4%89%e6%95%b0%e5%88%a5%e3%81%ab%e8%89%b2%e5%88%86%e3%81%91%e3%81%97%e3%81%9f%e3%83%92%e3%82%b9%e3%83%88%e3%82%b0%e3%83%a9%e3%83%a0%e3%82%92%e4%bd%9c%e6%88%90/)

### box

箱ひげ。

```
df.plot(kind='box')
```

![f:id:Rosyuku:20160803235918p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235918.png "f:id:Rosyuku:20160803235918p:plain")

### kde, density

カーネル密度推定。

```
df.plot(kind='kde')
#以下でも同様
df.plot(kind='density')
```

![f:id:Rosyuku:20160803235451p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235451.png "f:id:Rosyuku:20160803235451p:plain")

### area

折れ線グラフ＋塗りつぶし

```
df.plot(kind='area')
```

![f:id:Rosyuku:20160803235537p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235537.png "f:id:Rosyuku:20160803235537p:plain")

### pie

円グラフ。複数のcolumnを一つのグラフに書こうとするとエラー。

```
df.plot(kind='pie', y=df.columns[0])
```

![f:id:Rosyuku:20160803235653p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235653.png "f:id:Rosyuku:20160803235653p:plain")

### scatter

散布図。xとyを両方指定しないとエラー。

```
df.plot(kind='scatter', x=df.columns[0], y=df.columns[1])
```

![f:id:Rosyuku:20160803235803p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235803.png "f:id:Rosyuku:20160803235803p:plain")

### hexbin

散布図に似たかっこよさげな？グラフ。xとyを両方指定しないとエラー。

```
df.plot(kind='hexbin', x=df.columns[0], y=df.columns[1])
```

![f:id:Rosyuku:20160803235848p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803235848.png "f:id:Rosyuku:20160803235848p:plain")

## ax

ベースとなるmatplotlibのaxを指定する。デフォルトはNone（なし）。すでに書いたグラフに上書きしたい場合などに使う。

```
#ヒストグラムとカーネル密度を重ねてplot。
ax1 = df.plot(kind='hist')
#secondary_yを使ってy2軸を使用。
df.plot(kind='kde', ax=ax1, secondary_y=True)
```

![f:id:Rosyuku:20160804000946p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804000946.png "f:id:Rosyuku:20160804000946p:plain")

## subplots

columnを個別に表示したいときに指定する。デフォルトはFalse（全部を1つのグラフに表示）。さらに、subplotsがTrueの際に使えるパラメータ（sharex, sharey, layout）があります。

```
df.plot(subplots=True)
```

![f:id:Rosyuku:20160804001158p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804001158.png "f:id:Rosyuku:20160804001158p:plain")

### layout

subplotsをTrueにした際の攻勢を指定するパラメータ（行、列）。デフォルトは1列並び。

```
#2×2で配置
df.plot(subplots=True, layout=(2, 2))
```

![f:id:Rosyuku:20160804003131p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804003131.png "f:id:Rosyuku:20160804003131p:plain")

## figsize

グラフのサイズを指定するときに使うパラメータ（幅、高さ）。単位はインチ。

```
df.plot(figsize=(20, 10))
```

![f:id:Rosyuku:20160804003419p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804003419.png "f:id:Rosyuku:20160804003419p:plain")

## use\_index

index列をx軸に使用するかを指定するパラメータ。デフォルトはTrue。Falseを指定すると、indexを単純に連番に設定したグラフになる。

```
df.plot(use_index=False)
```

irisのデータは元々indexが連番なので変化なし。  
![f:id:Rosyuku:20160803233100p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160803/20160803233100.png "f:id:Rosyuku:20160803233100p:plain")

タイトルを指定したい場合に設定するパラメータ。

```
df.plot(title='test')
```

![f:id:Rosyuku:20160804003838p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804003838.png "f:id:Rosyuku:20160804003838p:plain")

## grid

grid線を表示するパラメータ。デフォルトはNone。

```
df.plot(grid=True)
```

![f:id:Rosyuku:20160804003951p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804003951.png "f:id:Rosyuku:20160804003951p:plain")

## legend

凡例の表示・非表示・反転を指定するパラメータ。デフォルトはTrue（表示）。

```
#非表示
df.plot(legend=False)
```

![f:id:Rosyuku:20160804004247p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804004247.png "f:id:Rosyuku:20160804004247p:plain")

```
#反転
df.plot(legend='reverse')
```

![f:id:Rosyuku:20160804004300p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804004300.png "f:id:Rosyuku:20160804004300p:plain")

## style

線の書式を指定するパラメータ。デフォルトは-（solid）。詳細は [lines — Matplotlib 1.5.1 documentation](http://matplotlib.org/api/lines_api.html) 参照。

```
#順番に、solid, dashed, dashdot, dottedを指定。
df.plot(style=['-', '--', '-.', ':'])
```

![f:id:Rosyuku:20160804004844p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804004844.png "f:id:Rosyuku:20160804004844p:plain")

## logx

x軸を対数目盛りとする場合に使用。デフォルトはFalse。

```
df.plot(logx=True)
```

![f:id:Rosyuku:20160804005239p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804005239.png "f:id:Rosyuku:20160804005239p:plain")

## logy

y軸を対数目盛りとする場合に使用。デフォルトはFalse。

```
df.plot(logy=True)
```

![f:id:Rosyuku:20160804005251p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804005251.png "f:id:Rosyuku:20160804005251p:plain")

## loglog

x、y軸を両方対数目盛りとする場合に使用。デフォルトはFalse。

```
df.plot(loglog=True)
```

![f:id:Rosyuku:20160804005309p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804005309.png "f:id:Rosyuku:20160804005309p:plain")

## xticks

x軸の目盛りを指定したい場合に使うパラメータ。目盛りをlistで渡して使用する。

```
df.plot(xticks=[0, 50, 100, 150])
```

![f:id:Rosyuku:20160804005539p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804005539.png "f:id:Rosyuku:20160804005539p:plain")

## yticks

y軸の目盛りを指定したい場合に使うパラメータ。目盛りをlistで渡して使用する。

```
df.plot(yticks=[0, 3, 8])
```

![f:id:Rosyuku:20160804005624p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804005624.png "f:id:Rosyuku:20160804005624p:plain")

## xlim

x軸の範囲を指定したい場合に使う。

```
df.plot(xlim=[0, 50])
```

![f:id:Rosyuku:20160804005816p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804005816.png "f:id:Rosyuku:20160804005816p:plain")

## ylim

y軸の範囲を指定したい場合に使う。

```
df.plot(ylim=[0, 50])
```

![f:id:Rosyuku:20160804005827p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804005827.png "f:id:Rosyuku:20160804005827p:plain")

## rot

x軸の目盛りを回転させたいときに使う。y軸の変え方は。。。？

```
df.plot(rot=45)
```

![f:id:Rosyuku:20160804010049p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804010049.png "f:id:Rosyuku:20160804010049p:plain")

## fontsize

x軸とy軸のメモリのフォントを指定したいときに使う。

```
df.plot(fontsize=20)
```

legendは変えられない。。。だと？  
![f:id:Rosyuku:20160804010237p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804010237.png "f:id:Rosyuku:20160804010237p:plain")

## colormap

カラーマップを指定したいときに使う。カラーマップについては [color example code: colormaps\_reference.py — Matplotlib 1.5.1 documentation](http://matplotlib.org/examples/color/colormaps_reference.html) を参照。

```
df.plot(colormap='BuGn')
```

![f:id:Rosyuku:20160804010526p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804010526.png "f:id:Rosyuku:20160804010526p:plain")

```
df.plot(colormap='viridis')
```

![f:id:Rosyuku:20160804010535p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804010535.png "f:id:Rosyuku:20160804010535p:plain")

## colorbar

kindでscatterかhexbinを指定し、さらにc（点の色の濃淡）を与えた場合、カラーバーを出力するオプション。デフォルトはTrue。

```
#カラーバーを表示（デフォルト）
df.plot(kind='scatter', x=df.columns[0], y=df.columns[1], c=df.columns[2])
```

![f:id:Rosyuku:20160804011038p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804011038.png "f:id:Rosyuku:20160804011038p:plain")

```
#カラーバーを非表示
df.plot(kind='scatter', x=df.columns[0], y=df.columns[1], c=df.columns[2], colorbar=False)
```

![f:id:Rosyuku:20160804011045p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804011045.png "f:id:Rosyuku:20160804011045p:plain")

## position

kindでbarを指定した際に、棒の位置を調整するパラメータ(0.0～1.0）。デフォルトは0.5（真ん中）。

```
#（デフォルト）
df.mean().plot(kind='bar', position=0.5)
```

![f:id:Rosyuku:20160804224851p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804224851.png "f:id:Rosyuku:20160804224851p:plain")

```
#（左寄せ）
df.mean().plot(kind='bar', position=0.0)
```

![f:id:Rosyuku:20160804224903p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804224903.png "f:id:Rosyuku:20160804224903p:plain")

```
#（右寄せ）
df.mean().plot(kind='bar', position=1.0)
```

![f:id:Rosyuku:20160804224911p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804224911.png "f:id:Rosyuku:20160804224911p:plain")

## table

グラフの下に表を付け足せる機能。デフォルトはFalse。xticksの位置と調整が必要そうです。

```
#xticksは表示しない要に設定
df.plot(table=df.ix[0:10].T, xlim=[0, 10], xticks=[])
```

![f:id:Rosyuku:20160804230349p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804230349.png "f:id:Rosyuku:20160804230349p:plain")

## yerr

指定した値だけy軸方向にエラーバーを付加します。

```
df.plot(yerr=0.1)
```

![f:id:Rosyuku:20160804230851p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804230851.png "f:id:Rosyuku:20160804230851p:plain")

## xerr

指定した値だけx軸方向にエラーバーを付加します。

```
df.plot(xerr=0.5)
```

![f:id:Rosyuku:20160804230943p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804230943.png "f:id:Rosyuku:20160804230943p:plain")

## stacked

kindでbarかareaを指定したとき、積み上げ表示にしたいときにTrueを指定します。

```
df.plot(kind='area', stacked=True)
```

![f:id:Rosyuku:20160804231218p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804231218.png "f:id:Rosyuku:20160804231218p:plain")

```
#積み上げない場合
df.plot(kind='area', stacked=False)
```

![f:id:Rosyuku:20160804234127p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804234127.png "f:id:Rosyuku:20160804234127p:plain")

## sort\_columns

[カラム名](http://d.hatena.ne.jp/keyword/%A5%AB%A5%E9%A5%E0%CC%BE) をソートしたいときに使う変数。デフォルトはFalse。試してみましたが結果変わらず、調査中です。

```
#カラム名を逆順に変更
ndf = pd.DataFrame(index=df.index, data=df.values, columns=[4, 3, 2, 1, 0])
#ソートしない場合
ndf.plot()
```

![f:id:Rosyuku:20160804232228p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804232228.png "f:id:Rosyuku:20160804232228p:plain")

```
#ソートを指定しても結果が変わらない
ndf.plot(sort_columns=True)
```

![f:id:Rosyuku:20160804232228p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804232228.png "f:id:Rosyuku:20160804232228p:plain")

## secondary\_y

y2軸を指定する際に使います。デフォルトはFalse。

```
df.plot(secondary_y=True)
```

![f:id:Rosyuku:20160804232502p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804232502.png "f:id:Rosyuku:20160804232502p:plain")

## mark\_right

y2軸を指定した際、凡例にrightを入れたくないときに使います。デフォルトはTrue（rightを表示）。

```
df.plot(secondary_y=True, mark_right=False)
```

![f:id:Rosyuku:20160804232744p:plain](https://cdn-ak.f.st-hatena.com/images/fotolife/R/Rosyuku/20160804/20160804232744.png "f:id:Rosyuku:20160804232744p:plain")

## kwds

「Options to pass to matplotlib plotting method」つまり、matplotlibのplotで使えるoptionを指定できるとのことです。この引数に関しては以下を参照。

> [Matplotlib.pyplotのplotの全引数を解説](http://own-search-and-study.xyz/2016/08/08/matplotlib-pyplot%e3%81%aeplot%e3%81%ae%e5%85%a8%e5%bc%95%e6%95%b0%e3%82%92%e4%bd%bf%e3%81%84%e3%81%93%e3%81%aa%e3%81%99/)

## まとめ

以上を見てみると、pandasのプロット機能だけで、いろんなグラフを簡単に書くことが出来ることが分かります。特によく使うのは、kindやsubplotsでしょうか。  
一方で、legendの位置や文字サイズを変えられなかったり、subplotの各グラフのタイトルを付けられなかったりと、細かいところまで調整することが出来ないことも分かります。というか、保存のコマンドすらないです。この辺りは、matplotlibを使って対策してあげる必要があるようです。ちなみに、参考までに、保存は以下で可能です。

```
ax = df.plot()
fig = ax.get_figure()
fig.savefig('test.png')
```

+8
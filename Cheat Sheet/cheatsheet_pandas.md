| No. | 機能                  | コマンド例                                       | 備考・詳細                           |            |
| --- | ------------------- | ------------------------------------------- | ------------------------------- | ---------- |
| 1   | データフレーム作成           | pd.DataFrame(data)                          | 辞書や配列から作成                       |            |
| 2   | CSV読み込み             | pd.read_csv('file.csv')                     | ファイルパス指定                        |            |
| 3   | Excel読み込み           | pd.read_excel('file.xlsx')                  | シートやカラム指定可能                     |            |
| 4   | 行列サイズ確認             | df.shape                                    | (行数, 列数)                        |            |
| 5   | カラム名一覧確認            | df.columns / df.columns.tolist()            | インデックス一覧も同様                     |            |
| 6   | データ型確認              | df.dtypes                                   | 各列の型                            |            |
| 7   | 型の確認 (dtypes/dtype) | df.dtypes / df["列名"].dtype                  | DataFrameはdtypes、Seriesはdtype   |            |
| 8   | 型変換                 | df.astype(str) / df["列名"].astype(float)     | 数値⇔文字列やfloat変換                  |            |
| 9   | レコード数（行数）           | len(df)                                     | shapeでも可                        |            |
| 10  | 情報（型・欠損）            | df.info()                                   | 行数・型一覧・欠損有無                     |            |
| 11  | ユニーク要素              | df["cabin"].unique()                        | 列のユニーク値                         |            |
| 12  | 列名一覧 (リスト)          | df.columns.tolist()                         | リスト形式取得                         |            |
| 13  | インデックス一覧 (配列)       | df.index.values                             | ndarray形式表示                     |            |
| 14  | 欠損値確認               | df.isnull()                                 | True/False                      |            |
| 15  | 欠損値削除               | df.dropna()                                 | 欠損含む行/列を削除                      |            |
| 16  | 欠損値補完               | df.fillna(値)                                | 欠損値を補完                          |            |
| 17  | 重複削除                | df.drop_duplicates()                        | 重複行除去                           |            |
| 18  | 条件抽出                | df[df['A'] > 5]                             | 条件で抽出                           |            |
| 19  | 行・列抽出               | df.iloc, df.loc['index1']                   | インデックス/ラベル抽出                    |            |
| 20  | 並べ替え                | df.sort_values('A')                         | 昇順・降順                           |            |
| 21  | locによる抽出            | df.loc[ラベル, 列名]                             | 行・列のラベル名で抽出（例：df.loc['A', 'B']） |            |
| 22  | 列名・インデックス変更         | df.rename({'old':'new'}, axis=1)            | 列名/インデックス変更                     |            |
| 23  | ilocによる抽出           | df.iloc[番号, 番号]                             | 行・列インデックス番号で抽出（例：df.iloc[0, 1]） |            |
| 24  | CSV出力               | df.to_csv('file.csv')                       | CSVファイルとして保存                    |            |
| 25  | 条件抽出（複数条件）          | df[(df['sex']=='female') & (df['age']>=40)] | 条件を複数指定し抽出                      |            |
| 26  | 条件抽出（OR条件等）         | df[(df['sex']=='female')                    | (df['age']>=40)]                | 論理演算子で条件抽出 |
| 27  | 条件抽出（複雑条件）          | df[(df['sex']=='female') & (df['age']>=40)] | and, orなど組み合わせ                  |            |
| 28  | queryによる抽出          | df.query('sex == \"female\" & age >= 40')   | SQL風文字列で条件記述                    |            |
| 29  | queryによる抽出（複数条件）    | df.query('sex == \"female\" or age >= 40')  | and/or組合せ                       |            |
| 30  | 型指定抽出               | df.select_dtypes(include='object')          | 指定型の列のみ抽出                       |            |
| 31  | 各列の要素数確認            | df.nunique()                                | 各列ごとのユニーク要素数                    |            |
| 32  | 値の出現回数確認            | df['embarked'].value_counts()               | 指定列の値の個数                        |            |
| 33  | 転置                  | df.T                                        | 行列交換                            |            |
| 34  | データフレームへの列追加        | df['新列'] = 値                                | 新しい列を追加                         |            |
| 35  | 列の削除                | df.drop('列名', axis=1)                       | 不要な列を削除                         |            |
| 36  | データ型の一括変換           | df.astype({'col1': int, 'col2': str})       | 複数列同時に型変換                       |            |
| 37  | カテゴリ型変換             | df['col1'].astype('category')               | 文字列をカテゴリへ                       |            |
| 38  | 欠損値の判定と個数           | df.isnull().sum()                           | 各列の欠損個数を返す                      |            |
| 39  | 値の置換                | df.replace({'old': 'new'})                  | 指定値の置換                          |            |
| 40  | 文字列処理（一括変換）         | df['col1'].str.lower()                      | 全て小文字に変換                        |            |
| 41  | 列の順番変更              | df = df\[\['col2','col1','col3']]           | カラム順を指定                         |            |
| 42  | グループごとの処理           | df.groupby('col1').mean()                   | グループごとの平均                       |            |
| 43  | describeによる基礎統計     | df.describe()                               | 全体の統計量                          |            |
| 44  | 列ごとにapply処理         | df['col1'].apply(lambda x: x*2)             | 関数適用                            |            |
| 45  | 複数列による条件抽出          | df[(df['A'] > 5) & (df['B'] == 0)]          | 複数列条件で抽出                        |            |

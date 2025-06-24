# Google Colab & Jupyter Notebook

## Google Colaboratory（Google Colab）とは

Google Colaboratory（通称Google Colab）は、Googleが無料で提供しているクラウドベースのPython開発環境です。ブラウザ上でJupyter Notebookのような対話型プログラミング環境を利用でき、機械学習の教育や研究用に特化して設計されています。

### 主な特徴

Google Colabの最も重要な特徴は以下の通りです：

- **完全クラウドベース**: ブラウザだけでPythonコードを記述・実行可能
- **GPU/TPU無料利用**: 高性能な計算リソースを無料で使用可能
- **環境構築不要**: 主要なライブラリがプリインストール済み
- **Google Drive連携**: ノートブックは自動的にGoogle Driveに保存

## Jupyter Notebookとは

Jupyter Notebookは、Webブラウザ上でPythonなどのプログラミング言語を実行しながら、その結果やコードを同じドキュメント内にまとめられるツールです[1][2]。「ジュピター・ノートブック」または「ジュパイター・ノートブック」と読まれ、以前は「IPython Notebook」という名前でした[2][3]。

### Jupyter Notebookの歴史

Jupyter Notebookは2001年にFernando Perezによって作成されたIPython（Interactive Python）から発展しました[3]。2005年にはIPython shellのノートブックインターフェースがリリースされ、その後RやJuliaなどの他言語もサポートされるようになりました[3]。2014年にはJupyterプロジェクトがIPythonの「スピンオフ」として創設され、Jupyterという名前はJulia、Python、Rの3つの言語から取られています[1][3]。

### 基本概念とアーキテクチャ

#### セルベースの構造

Jupyter Notebookは「セル」と呼ばれる小さな単位に分割されており、それぞれにコードやマークダウンテキストを入力できます[4][5]。セルは上から順番に実行されるため、セルの順番によって実行結果が異なることに注意が必要です[4]。

主要なセルタイプは以下の通りです：

- **Codeセル**: Pythonのコードが記述されるセルで、`In [ ]:`と表示されます[5]
- **Markdownセル**: 説明文やドキュメントが記述されるセルです[5]

#### カーネルシステム

Jupyter Notebookの中核となるのがカーネルシステムです[3]。カーネルはプログラミング言語の実行環境を提供し、IPythonがJupyter Notebookの主要なカーネルとして機能しています[3]。40種類以上のプログラミング言語をサポートしていますが、一般的にはPythonで使用されることが多いです[2]。

## Jupyter Notebookの機能と特徴

### 対話型プログラミング環境

Jupyter Notebookは対話型の開発環境として設計されており、前の実行結果に応じて次に実行するプログラムや作業を選択できます[2]。実行した結果は作業履歴として記録に残り、コードを記述して即座に実行し、結果をすぐに確認できるインタラクティブ性が特徴です[6]。

### ビジュアライゼーション機能

Jupyter Notebookでは、matplotlibやseabornなどのライブラリを使用して複雑な3Dグラフも表示でき、データ分析の結果をビジュアルで表現し確認することができます[7][6]。統計のモデリングや機械学習などデータ分析に使用されることが想定されており、データの視覚化などの作業に適しています[2]。

### Markdown機能

Jupyter NotebookではMarkdown（マークダウン）と呼ばれる記法を使用して、コードや実行結果も含めた技術的なドキュメントの作成や共有が可能です[7][8]。これにより、分析手順や結果をわかりやすく整理し、再現性や共有性に優れたドキュメントを構築できます[6]。

## 操作方法とモード

### エディットモードとコマンドモード

Jupyter Notebookには「エディットモード」と「コマンドモード」の2つのモードがあります[7][8][5]：

- **エディットモード**: セルの枠線が緑色で表示され、プログラムを記述するためのモードです[8][5]
- **コマンドモード**: セルの枠線が青色で表示され、セル自体の削除や追加といった操作を行うためのモードです[8][5]

### 便利なショートカットキー

Jupyter Notebookには効率的な作業を支援する多数のショートカットキーが用意されています[2][7][5]：

- **Shift + Enter**: セル内のプログラムを実行し、その下に新しいセルを追加[7][5]
- **Ctrl + Enter**: セルを実行するが新しいセルは追加せず[2][7]
- **ESC → D → D**: セルを削除（コマンドモードで）[2][7]
- **a**: 上にセルを挿入（コマンドモードで）[5]
- **b**: 下にセルを挿入（コマンドモードで）[5]

## 実用的な機能

### ヒストリー機能

Jupyter Notebookには`%history`マジックコマンドを使用して、コードの実行履歴を確認・保存する機能があります[9][10]。主要なオプションには以下があります：

- `-n`: 行番号を表示
- `-o`: 出力結果も表示
- `-f <FILENAME>`: ファイルに結果を保存
- `-t`: マジックコマンドをPythonコードに翻訳して表示

### 拡張機能

Jupyter Notebookでは、マジックコマンドを使用してPythonの機能を拡張することができます[4]。また、テーマの変更や様々な拡張機能を利用することで、より効率的な開発環境を構築できます[4]。

## 両者の比較と使い分け

### 共通点

- **Jupyter Notebook互換**: Google ColabはJupyter Notebookと同様のインターフェースを持つ
- **セルベース構造**: 両者ともセル単位でコードを実行する構造
- **Markdown対応**: テキスト説明とコードを組み合わせた文書作成が可能
- **データサイエンス用途**: 機械学習やデータ分析に最適化

### 主な違い

| 特徴 | Google Colab | Jupyter Notebook |
|------|-------------|------------------|
| 環境 | クラウドベース | ローカル/サーバー |
| 初期設定 | 不要 | インストール必要 |
| GPU/TPU | 無料利用可能 | 別途設定必要 |
| セッション制限 | 約90分 | 制限なし |
| 保存先 | Google Drive | ローカル/任意 |
| 言語サポート | 主にPython | 40種類以上 |

## 教育・研究での活用

### 教育現場での採用

Jupyter Notebookは世界中の教育機関で広く活用されており、プログラミング初心者から上級者まで、誰でも平等に高性能な計算リソースにアクセスできるため、経済的背景に関係なく最先端のAI・機械学習技術を学習できます[11][12]。COVID-19パンデミック期間中は、リモート学習への移行を支援する重要なツールとして機能しました[11][12]。

### 研究開発での応用

研究者は複雑な深層学習モデルの訓練から画像分類、自然言語処理まで幅広いタスクを実行でき[13][14]、ノートブック形式により実験プロセスの記録と再現性の確保が容易になります[15][16]。

## まとめ

Google ColabとJupyter Notebookは、それぞれ異なる利点を持つ強力なデータサイエンスツールです。Google Colabは環境構築の負担なしにすぐに始められる利便性が特徴で、Jupyter Notebookは柔軟性と拡張性に優れています。両者の特徴を理解し、プロジェクトの要件に応じて適切に選択することで、効率的なデータサイエンスワークフローを構築できるでしょう。

情報源
[1] Jupyter Notebookをしっかり理解する - インターネット・アカデミー https://www.internetacademy.co.jp/itlab/column-technology/python_stydy04.html
[2] 【初心者向け】Jupyter Notebookの使い方！インストール方法から ... https://udemy.benesse.co.jp/development/python-work/jupyter-notebook.html
[3] IPython: Discover the Python shell at the heart of Jupyter Notebook https://datascientest.com/en/ipython-discover-the-python-shell-at-the-heart-of-jupyter-notebook
[4] Jupyter Notebook - Wikibooks https://ja.wikibooks.org/wiki/Jupyter_Notebook
[5] Jupyter Notebook の使い方 - Pythonプログラミング入門 https://utokyo-ipp.github.io/appendix/1-jupyter-notebook.html
[6] Jupyter Notebook入門：Mac環境での導入からPythonコード実行まで https://zenn.dev/haruki1009/articles/045a07794899c2
[7] 図解！Jupyter Notebookを徹底解説！(インストール・使い方・起動 ... https://ai-inter1.com/jupyter-notebook/
[8] Jupyter Notebookとは。Python開発・仕事の効率化に便利 - Winserver https://www.winserver.ne.jp/column/jupyter-notebook/
[9] 【ipython】historyの基本的な使い方 https://www.tcom242242.net/entry/python-basic/ipython/%E3%80%90ipython%E3%80%91history%E3%81%AE%E5%9F%BA%E6%9C%AC%E7%9A%84%E3%81%AA%E4%BD%BF%E3%81%84%E6%96%B9/
[10] Jupyter Notebook のコード実行履歴を Python スクリプトとして保存 ... https://kioku-space.com/jupyter-command-history/
[11] Teaching Python programming for bioinformatics with Jupyter notebook in the Post‐COVID‐19 era https://iubmb.onlinelibrary.wiley.com/doi/10.1002/bmb.21746
[12] Enhancing Learning About Epidemiological Data Analysis Using R for Graduate Students in Medical Fields With Jupyter Notebook: Classroom Action Research https://mededu.jmir.org/2023/1/e47394
[13] Design and Implementation of a Data Preprocessing Automatic Assessment Module in Jupyter Notebook https://ijaseit.insightsociety.org/index.php/ijaseit/article/view/20233
[14] Research on the product recommendation algorithm based on PySpark and Jupyter notebook https://www.spiedigitallibrary.org/conference-proceedings-of-spie/12586/2670415/Research-on-the-product-recommendation-algorithm-based-on-PySpark-and/10.1117/12.2670415.full
[15] Histree: A Tree-Based Experiment History Tracking Tool for Jupyter Notebooks https://ieeexplore.ieee.org/document/10479422/
[16] Interactions for Untangling Messy History in a Computational Notebook https://ieeexplore.ieee.org/document/8506576/
[17] Menerapkan Metode Klasifikasi pada Data Uji Emisi Kendaraan di Jakarta dengan Menggunakan Jupyter Notebook https://journal.jis-institute.org/index.php/jpsii/article/view/1722
[18] Jupyter Notebook Attacks Taxonomy: Ransomware, Data Exfiltration, and Security Misconfiguration https://ieeexplore.ieee.org/document/10820752/
[19] Exploring digital signal processing using an interactive Jupyter notebook and smartphone accelerometer data https://iopscience.iop.org/article/10.1088/1361-6404/ad0790
[20] Comparison and Applications of Multiplying 2 by 2 Matrices Using Strassen Algorithm in Python IDLE, Jupyter Notebook, and Colab https://ieeexplore.ieee.org/document/10487273/
[21] IMPLEMENTASI APLIKASI JUPYTER NOTEBOOK SEBAGAI ANALISIS KRETERIA PLAGIASI DENGAN TEKNIK SIMANTIK https://jurnal.stkippgritulungagung.ac.id/index.php/jipi/article/view/3699
[22] On Code Reuse from StackOverflow: An Exploratory Study on Jupyter Notebook https://arxiv.org/abs/2302.11732
[23] Pythonのデータ操作もグラフも自由自在、「Jupyter Notebook」の ... https://xtech.nikkei.com/atcl/nxt/column/18/02232/102500003/
[24] Understanding the Characteristics of Visual Contents in Open Source Issue Discussions: A Case Study of Jupyter Notebook https://dl.acm.org/doi/10.1145/3530019.3534082
[25] PLNQ: Defining Coding Katas Using a Single Jupyter Notebook https://dl.acm.org/doi/10.1145/3641555.3705270
[26] Self-Contained Jupyter Notebook Labs Promote Scalable Signal Processing Education http://ocs.editorial.upv.es/index.php/HEAD/HEAd20/paper/view/11308
[27] Argovis API exposed in a Python Jupyter notebook: an easy access to Argo profiles, weather events, and gridded products https://essopenarchive.org/doi/full/10.1002/essoar.10504304.1
[28] Performance Prediction of Jupyter Notebook in JupyterHub using Machine Learning https://ieeexplore.ieee.org/document/8550030/
[29] DistilKaggle: A Distilled Dataset of Kaggle Jupyter Notebooks https://dl.acm.org/doi/10.1145/3643991.3644882
[30] Study on the use of a combination of IPython Notebook and an industry‐standard package in educating a CFD course https://onlinelibrary.wiley.com/doi/10.1002/cae.22273
[31] ipythonで過去に実行したコマンドを簡単に再実行する方法 - Qiita https://qiita.com/AnchorBlues/items/77c90f5d7e3e80ad6ce7
[32] Access IPython command history via key-bindings in Jupyter ... https://github.com/jupyterlab/jupyterlab/issues/9646
[33] How to Add a Kernel in Jupyter Notebook (2025) https://www.youtube.com/watch?v=mDdL6VvJ8EU&vl=ja
[34] Cline https://www.codingrules.ai/rules/core-architecture-standards-for-jupyter-notebooks
[35] Jupyter Notebooks’ Untold Story: How They Revolutionized Data Science, Research, Modern Education https://www.youtube.com/watch?v=ABUcJbRYMIo
[36] An Automated Evaluation Approach for Jupyter Notebook Code Cell Recommender Systems https://www.semanticscholar.org/paper/083244a43f2466637538eef6cfe8e53a5203c25b
[37] Using PharmaPy with Jupyter Notebook to teach digital design in pharmaceutical manufacturing https://onlinelibrary.wiley.com/doi/10.1002/cae.22660
[38] 【2023年版】Jupyter拡張機能・ショートカット完全まとめ - Qiita https://qiita.com/sashi_34/items/039b08c62caab9544f42
[39] Jupyter notebookの使い方[超基礎] #Python - Qiita https://qiita.com/taruto1215/items/df754a395e53834e17e4
[40] Japper: A Comprehensive Framework for Streamlining Jupyter-Based Scientific Web Application Development https://dl.acm.org/doi/10.1145/3626203.3670594
[41] Jupyter Technology as a Cartographer's Work Environment: A Case Study https://ica-proc.copernicus.org/articles/5/4/2023/
[42] IPython and Jupyter Notebook https://www.cambridge.org/core/product/identifier/9781108778039%23c5/type/book_part
[43] Creating and Grading IPython/Jupyter Notebook Assignments with NbGrader https://dl.acm.org/doi/10.1145/2839509.2850507
[44] Learning IPython for interactive computing and data visualization : get started with Python for data analysis and numerical computing in the Jupyter notebook https://www.semanticscholar.org/paper/cde14f47fb7ad043a875d18e1f5456b8cc6d4431
[45] Manual de uso de Jupyter Notebook para aplicaciones docentes https://www.semanticscholar.org/paper/822f08a37b094c9be1b71e1e01f43d75a8fc61c4
[46] Combine Stata with Python using the Jupyter Notebook https://www.semanticscholar.org/paper/6e413cd6e1bceef5d6c76c0297eaf4c1acd60575
[47] Jupyter Notebook App: Alternatif Teknologi Pembelajaran Fisika Berbasis Web Browser https://www.semanticscholar.org/paper/8d60af292644310861f6eedfac093c7d2214a74e
[48] "The evolutionary history of Neandertal and Denisovan Y chromosomes" - code and Jupyter notebooks https://zenodo.org/record/3941654
[49] GitHub - cptpiepmatz/nu-jupyter-kernel: 📓 A wip jupyter raw kernel for nu https://github.com/cptpiepmatz/nu-jupyter-kernel
[50] Jupyter Notebook Architecture https://www.herongyang.com/Python/Jupyter-Notebook-Architecture.html

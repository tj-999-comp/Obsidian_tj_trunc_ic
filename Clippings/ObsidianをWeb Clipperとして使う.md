---
title: ObsidianをWeb Clipperとして使う
source: https://zenn.dev/karaage0703/articles/52c3e016653003#github%E3%81%B8%E3%81%AE%E3%83%90%E3%83%83%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97
author:
  - "[[Zenn]]"
published: 2025-05-05
created: 2025-05-23
description: 
tags:
  - clippings
  - Obsidian
---
108

47[idea](https://zenn.dev/tech-or-idea)
[[Obsidian Web Clipper × AI でWebページを自動要約＆ストックしてみた  DevelopersIO]]
## Obsidianに入門しました

LLMとマークダウンの相性がよいということで話題になっているObsidianに入門しました。本も買って読みました。

[Obsidianで“育てる”最強ノート術](https://amzn.to/3EVuf8N)

そして、色々試行錯誤してみたのですが…結局自分の場合は、あんまり使い道がないことに気づきました。 [ノートはiPadでApple Pencilで手書きが好き](https://karaage.hatenadiary.jp/entry/2024/01/11/073000) なのと、デジタル的なまとめは、はてなブログやZennにブログとしてまとめているからです。Notionもメモとかノートというよりは、データ置き場って感じなんですよね。

ただ、Web Clipperは、PCでもiPhone/iPadでもクリック（タップ）一発で、ウェブサイトを保存できて便利で活用することにしたので、設定方法を残しておきます。

### Obsidianインストール

Homebrewインストール済みの場合は、以下コマンドでOKです。

```shell
$ brew install --cask obsidian
```

もちろん、 [公式サイト](https://obsidian.md/) から普通にインストールしてもOK。

### iCloudとの同期

iPhone/iPadとPCの同期のために、iCloudとの同期を設定しました。Windowsはあんまり相性良くないという噂なので辞めたほうがよいかもです。

iCloudの同期は、最初うまくいきませんでした。コツとしては、最初にモバイルアプリでObsidianを先にインストールして、Vaultを `Store in Cloud` のオプションをオンにして作成するところです。

![](https://storage.googleapis.com/zenn-user-upload/341ab9621167-20250504.png)

![](https://storage.googleapis.com/zenn-user-upload/0f83a6a82396-20250504.png)

これでiCloudに `Obsidian` というフォルダの中に、自分で設定したVault（自分の場合は `obsidian` ）が作成されます。

あとはPCのObsidianで「保管庫としてフォルダを開く」から、iCloud上のVaultを選択すればOKです。

### GitHubへのバックアップ

GitHubにもバックアップすると安心ですし便利ですね。

Git/GitHubを使える人なら簡単で、リポジトリを作成して（基本的にはリポジトリはプライベートがよいでしょう）、git cloneしたリポジトリをObsidianでVaultとして選択してやるだけです。実はObsidianのVaultの実体ってただのディレクトリ（フォルダ）で、その中に`.obsidian` ってディレクトリに設定作成しているだけなので、ファイルが壊れるとか気にせずにコピペとかして大丈夫です。

Obsidianの設定も、コミュニティプラグインでGitをインストールするだけです。プラグインを設定すれば、クリック一発でGitにコミットしてプッシュができます。自動でプッシュするような設定もできますが、私はiCloudで同期していることもあり、手動でプッシュする設定にしています。

### Web Clipperの設定と使用

PCの場合は以下サイトからChromeの拡張に追加するだけです。

あとは、拡張機能でWeb Clipperを使えばどんどんObsidianのVault（フォルダ）にマークダウンで保存してくれます。

iPhone/iPad関しても、ObsidianとObsidian Web Clipperをインストールして、左下の拡張機能ボタンから選択するだけです。ちなみに、今まで拡張機能ボタンの存在知りませんでした。

![](https://storage.googleapis.com/zenn-user-upload/058767d85781-20250504.png)

あとは、Obsidian Web Clipperをタップするだけ  
![](https://storage.googleapis.com/zenn-user-upload/c83bff5483ed-20250504.png)

毎回ペースト許可の確認が出てうっとおしいという人は設定から「アプリ→Obsidian→ほかのアプリからペースト許可」を設定すればスキップできます。

iPhone/iPadでクリップしたマークダウンファイルは、iCloudと同期されているので、瞬時にPCのObsidianにも同期されます。

### Kindle ハイライトの読み込み

~~これもやりたかったのですが、自分の場合はなぜか1部のデータしか同期しなくて諦めました。~~

本を開き直したら同期されました。同期されない方はお試しあれ（全部Kindle開くのなかなかキツイですが…）。こちらもオススメです。

設定などは以下記事が参考になりました。

### Notion Webクリッパー

単純にWebの情報を保存したいのであればNotion Webクリッパーを使えばよいというのはそれはそうです。ローカルにためるか、サーバに貯めるかの違いですね。

## まとめ

Obsidian、色々悩んだあげくWeb Clipper＋手軽なメモとして使っているという話でした。Obsidian、最初全然理解できなかったのですが（自分にとっては）拡張機能が便利なMarkdownエディタと理解すると、スッキリしました。

Notionと比較している人が結構いますが、自分にとってはObsidianはむしろVS Codeエディタとかのエディタと比べるものかなと思います。そう考えると、NotionとVS Codeエディタではできない、手軽なPC/iPhone/iPad間のデジタルテキストの同期・Web ClipperがObsidianの価値だなと行き着きました。

LLMとMarkdownに関しては、Markdownを集める方法が重要であって、別にそれはObsidianを使う必要はないかなという気がします（もちろんObsidian使ってもよいのですが、自分はデータが膨大なのでObsidianで扱うと多分逆に扱いづらい）。

Obsidianの使い方考えて、そういうことが整理できたことは良かったです。あとWeb Clippingは普通に便利なので今後活用していきたいと思います。他にも便利な使い方が見つかったら追記したいと思います。

[Obsidianで“育てる”最強ノート術](https://amzn.to/3EVuf8N)

## 参考

以下のサイトは、試してみたけど、ほとんど自分には使いこなせなかったり、使い方が適さなかったり、面倒になってやめてしまったものたちです。

[【Obsidian】知識のネットワークを作る究極のノート術【テンプレート配布】｜GitHub](https://www.youtube.com/watch?v=O4Ga14fe05w)

## 変更履歴

- 2025/05/07 Kindleハイライトに関して追記

108

47

### Discussion

![](https://static.zenn.studio/images/drawing/discussion.png)

ログインするとコメントできます
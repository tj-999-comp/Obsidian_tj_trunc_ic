---
title: "ObsidianのTemplaterの使い方と設定"
source: "https://eiji.page/blog/obsidian-templater-howto/"
author:
  - "[[eiji.page]]"
published: 2024-05-03
created: 2025-07-03
description:
tags:
  - "clippings"
  - "Obsidian"
---
Obsidianのプラグインである [Templater](https://silentvoid13.github.io/Templater/) の使い方を、初心者向けに画像付きで解説します。

具体的にどんなケースで使えばよいのかについても解説します。

## Templaterって何ができるの？

Templaterは柔軟にテンプレートを作成・呼び出しできるプラグインです。

<video alt="サンプルビデオ" controls="" height="470.5882352941177" src="https://storage.eiji.page/obsidian-templater-howto/templater-sample.mp4" width="800"></video>

うれしいポイントは次のとおりです。

- 日付操作ができる
- ファイル操作ができる
- JavaScriptを使える
- カーソルの移動も自動化できる

いつも似たようなことを入力していたり、ある程度フォーマットが決まっているノートにうってつけです。

## 一次情報まとめ

先によく見ることになるであろう一次情報の紹介です。

- [インストールリンク](https://obsidian.md/plugins?id=templater-obsidian)
- [Templaterの公式ドキュメント](https://silentvoid13.github.io/Templater/introduction.html)
- [GitHub](https://github.com/SilentVoid13/Templater)
- [ObsidianのAPIのドキュメント](https://docs.obsidian.md/Home)
	- Templaterとセットで使うこともあるため記載

## 使い方

テンプレートの書き方を解説する前に、設定方法と実際に使う時の流れを書いておきます。

### 設定

Templaterの設定 `Template folder location` にテンプレートファイルを置いておくフォルダを指定します。

![設定でフォルダを指定すること](https://storage.eiji.page/obsidian-templater-howto/templater-folder-location.avif)

### 流れ

Templaterを使う流れは次のとおりです。

1. （テンプレートファイルを作っておく）
2. コマンドを実行
3. （任意）カーソル移動

コマンドパレットからコマンドを呼び出せばテンプレートが適用できます。

![コマンドパレットで呼び出す例](https://storage.eiji.page/obsidian-templater-howto/command-palette.avif)

`Create new note from template` がテンプレートから新しくノートを作るコマンドです。  
テンプレートを現在のノートに挿入するコマンドは `Open Insert Template Modal` です。

どちらのコマンドでも「どのテンプレートを使うか」を選ぶ画面が出てきます。

![モーダルの例](https://storage.eiji.page/obsidian-templater-howto/which-create.avif)

## 書き方

まずはファイルを作りましょう。前述のとおり、テンプレートファイルは設定で指定したフォルダにノートとして保存します。

ただの文字列ならそのまま書くだけで終わりです。  
ただこれではTemplaterの真価を発揮できません。Templaterの真の姿、見たいですよね。

次のように `<%` と `%>` で囲んだ部分は、Templaterの特別な書き方として扱われます。

```js
<% tp.file.title %>
```

この囲んだ中に「日付やカーソル移動など操作（後述）」を書くと、テンプレート適用時に `<% ... %>` が指定した内容に書き換わります。

![テンプレートの使用例](https://storage.eiji.page/obsidian-templater-howto/before-after.avif)

### 日付を挿入

先にサクッと日付操作の例を解説します。

#### 現在の日時を挿入

一番使いそうな例から。 `tp.date.now()` を使うと現在の日付が挿入されます。

```text
現在の日時: <% tp.date.now() %>
```

```text
現在の日時: 2024-05-02
```

上下で比較すると、 `<%` と `%>` で囲んだ部分が `2024-05-02` 書き換わっていますね。

日付のフォーマットを指定する場合は、次のように括弧の中に書きます。

```text
フォーマットを指定した現在の日付: <% tp.date.now("YYYY年MM月DD日(ddd)") %>
```

```text
フォーマットを指定した現在の日付: 2024年05月02日(木)
```

たとえば `年-月-日 時:分:秒` （例： `2024-05-01 17:22:40` ）で書きたいなら `YYYY-MM-DD HH:mm:ss` と書きます。

詳しいフォーマットの書き方は [Moment.js](https://momentjs.com/docs/#/displaying/format/) を読みましょう。

#### N日後の日付を挿入

次の例は現在の7日後の日付を挿入しています。

```js
一週間後の日付: <% tp.date.now("YYYY-MM-DD", 7) %>
```

```text
一週間後の日付: 2024-05-09
```

2番目の引数（プログラムに渡す値）に数値を指定することで日付を前後できます。  
ちなみに `-7` だったら一週間前になります。

#### ファイルの作成日時を挿入

`tp.file.creation_date` ではテンプレートを適用されたファイルの作成日時を扱います。同じくフォーマットの指定が可能です。

```js
ファイルの作成日時: <% tp.file.creation_date("YYYY-MM-DD HH:mm:ss") %>
```

```text
ファイルの作成日時: 2024-05-01 17:22:40
```

- [tp.date](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/date-module.html#momentjs)
- [tp.file.creation\_date](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/file-module.html#tpfilecreation_dateformat-string--yyyy-mm-dd-hhmm)

### カーソル移動

書き込む場所が決まっているなら、テンプレート内にカーソル移動場所を定義しておくと便利です。

```js
<% tp.file.cursor() %>
```

<video alt="カーソル移動の例" controls="" height="129.87012987012986" src="https://storage.eiji.page/obsidian-templater-howto/cursor-move.mp4" width="500"></video>

コマンド `Jump to next cursor location` にホットキーを設定しておきましょう。

筆者はよく間違えてしまうのですが、スペルは”c **u** rsor”です（戒め）。補完を使っているのに手癖でぱぱっと入力し、痛い目に遭っています。

- [tp.file.cursor](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/file-module.html#tpfilecursororder-number)

### マルチカーソル

同じ文字列を別の場所にも書くなら、マルチカーソルにしておくと便利です。

<video alt="マルチカーソルの例" controls="" height="230.41474654377882" src="https://storage.eiji.page/obsidian-templater-howto/multi-cursor.mp4" width="500"></video>

`cursor(1)` のように文字列を使い回す箇所で同じ番号を振ると、入力が同期されます。  
入力が終わったらエスケープを押してマルチカーソルモードを抜けましょう。

```markdown
僕の名前は<% tp.file.cursor(1) %>です。
\`\`\`
はじめまして、<% tp.file.cursor(1) %>です。
よろしくお願いいたします。
\`\`\`
```

筆者はこの「コードブロック+マルチカーソル」の組み合わせをよく作っています。  
「自分のメモ用の文章」と「コピーしたり誰かに送る用の文章」を同時に作りたいときに重宝しています。

### プロンプト

プロンプトを使った入力もできます。

![プロンプト](https://storage.eiji.page/obsidian-templater-howto/prompt.avif)

`<%` と `%>` で囲んだ部分がプロンプトで入力した文字列に書き換わります。

```plaintext
僕の名前は<% tp.system.prompt("名前は？") %>です。
```

- [tp.system.prompt](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/system-module.html#tpsystempromptprompt_text-string-default_value-string-throw_on_cancel-boolean--false-multiline-boolean--false)

### tRとは？

ここまでは「 `<%` と `%>` で囲んだ部分の中身の実行結果」がそのまま文字列になっていました。  
ここからはJavaScriptで加工してから文字列を挿入するパターンです。

たとえば、次のようなJavaScriptの変数 `result` を挿入するにはどうすればよいでしょうか？このまま `<%` と `%>` で囲んでもエラーになります。

```js
let result = "";
if (tp.frontmatter.type === "ほのお") {
  result = "ほのおタイプの";
}
if (tp.file.tags.contains("#test")) {
  result += "テスト中です";
}
```

`<%*` と `%>` で囲み、変数 `tR` に挿入したい変数を足すのが正解です。 `*` と `tR` の登場です。

```js
<%*
let result = "";
if (tp.frontmatter.type === "ほのお") {
  result = "ほのおタイプの";
}
if (tp.file.tags.contains("#test")) {
  result += "テスト中です";
}
tR += result;
%>
```

開始タグを `<%*` のようにアスタリスク有りにすると、変数宣言やif文など、JavaScriptを書いて実行できます。  
単純にJavaScriptを実行したいだけであればここで終わりです。

変数に入れた文字列を挿入したいなら、Templaterで用意されている特別な変数 `tR` に足します。

`tR` はそれまでのTemplaterの実行結果を累積していく変数です。

**1点注意があります。**  
次のように `tR` に足さずに **代入してしまう** と、1行目の「現在の～」の行はテンプレートとして挿入されません。

```js
現在の日付: <% tp.date.now("YYYY-MM-DD (ddd)") %>
<%*
let result = "";
if (tp.frontmatter.type === "ほのお") {
  result = "ほのおタイプの";
}
if (tp.file.tags.contains("#test")) {
  result += "テスト中です";
}
tR = result;
%>
```

- [Execution Commands - Templater](https://silentvoid13.github.io/Templater/commands/execution-command.html#how-to-output-a-value-from-a-javascript-execution-command-)

frontmatterをテンプレートで書き換えたいなら2つの方法があります。

#### 直接書き換える

まずは普通にテンプレート内にYAML形式で仕込む書き方です。通常はこれで問題ありません。

```js
---
aliases:
tags:
created: <% tp.file.creation_date("YYYY-MM-DD HH:mm:ss") %>
---
```

#### 後から書き換える

次に何らかの事情で計算した値を元にプロパティを書き換えたい場合、少し複雑です。次のように書きます。

```js
<%*
const title = "foooooo";
tp.hooks.on_all_templates_executed(async () => {
  const file = tp.file.find_tfile(tp.file.path(true));
  await app.fileManager.processFrontMatter(file, (frontmatter) => {
    frontmatter["title"] = title;
  });
});
-%>
```

`tp.hooks.on_all_templates_executed` で他のテンプレートの適用が終わってから実行します。そうしないと現在開かれている別の意図していないファイルのfrontmatterが書き換えられてしまうため注意です。

`-%>` （ハイフン付きバージョン）は後で解説します。

関連する公式ドキュメントは次のとおりです。

- [tp.hooks - Templater](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/hooks-module.html)
- [tp.file.find\_tfile](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/file-module.html#tpfilefind_tfilefilename-string)
- [processFrontMatter - Developer Documentation](https://docs.obsidian.md/Reference/TypeScript+API/FileManager/processFrontMatter)

## 実例

ここからはもう少し実用的なテクニックの解説です。

### 特定のフォルダへ移動・リネーム

特定のフォルダへファイルを移動したい場合は `tp.file.move` を使います。

```js
<%*
const folder = "inbox";
const filename = tp.file.creation_date("YYYYMMDDHHmmss");
await tp.file.move(\`${folder}/${filename}\`);
-%>
```

単純にファイル名を変更したいだけなら `tp.file.rename` も用意されています。

- [tp.file.move](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/file-module.html#tpfilemovenew_path-string-file_to_move-tfile)
- [tp.file.rename](https://silentvoid13.github.io/Templater/internal-functions/internal-modules/file-module.html#tpfilerenamenew_title-string)

### 使った後に残る空行を消したい

TemplaterでJavaScriptの実行だけをして文字列を挿入しない場合、空行になります。  
空行を消したいなら終わりを `-%>` のようにダッシュを付けます。

![ホワイトスペースの比較](https://storage.eiji.page/obsidian-templater-howto/compare-white-space.avif)

先ほど紹介したファイル移動などで使えます。

```js
<%*
const folder = "inbox";
const filename = tp.file.creation_date("YYYYMMDDHHmmss");
await tp.file.move(\`${folder}/${filename}\`);
-%>
```

ホワイトスペースの扱いは何種類かありますが基本的には「最後に `-` ありで空行が消える」を覚えておくだけで事足ります。

ホワイトスペースに興味のある方は公式ドキュメント [Whitespace Control](https://silentvoid13.github.io/Templater/commands/whitespace-control.html) をご覧ください。

### 日時の言語を変えたい

曜日などの言語を変えたい場合、 `moment.locale` を使って変更します。

```js
<%* moment.locale('en') -%>
現在の日付: <% tp.date.now("YYYY-MM-DD (ddd)") %>
```

英語環境の方が日本語に変えたい場合は `en` の代わりに `ja` と書きます。

対応言語と指定すべき文字列の一覧は、次のコマンドを開発者ツールなりTemplaterのスクリプトなりで呼び出して確認してください。

```js
moment.locales()
```

ちなみに2024年5月2日現在は136の言語に対応しているようです。すごい！

- [Checking the current Moment.js locale](https://momentjs.com/docs/#/i18n/getting-locale/)

### ボタンでワンクリック

コマンドパレットから毎回テンプレートを選んで呼び出すのはやや面倒です。

筆者は「ワンクリックで指定したテンプレートからノートを作るボタン」を設置しています。便利です。

![横並びボタン](https://storage.eiji.page/obsidian-metabind-intro/horizontal-buttons.avif)

画像の例ではプラグイン [Meta Bind](https://www.moritzjung.dev/obsidian-meta-bind-plugin-docs/) を使っています。

詳しくは別の記事 [【Obsidian】ボタンを作れるプラグインMeta Bindの使い方](https://eiji.page/blog/obsidian-metabind-intro) に書きました。

---

Obsidianのプラグイン [Templater](https://silentvoid13.github.io/Templater/) の設定や使い方を解説しました。  
単なるテンプレートの挿入だけではなくJavaScriptが実行でき、ある程度ノート作りを自動化できるため重宝しています。
---
title: "Obsidianのタスク進捗をプログレスバーで一覧する｜⿶⿵⿷⿴⿳"
source: "https://note.com/unco3/n/n49b6afaef623"
author:
  - "[[⿶⿵⿷⿴⿳]]"
published: 2024-01-28
created: 2025-07-06
description:
tags:
  - "clippings"
  - "Obsidian"
---
![見出し画像](https://assets.st-note.com/production/uploads/images/129045437/rectangle_large_type_2_f71a4f23913bc82ac72fd06755dbfa9b.png?width=1200)

## Obsidianのタスク進捗をプログレスバーで一覧する

[⿶⿵⿷⿴⿳](https://note.com/unco3)

Obsidianのノートにタスクを記述しても、未消化のタスクが埋もれてしまったり、 **「達成率をパッと知りたい」** と思うことがあります。

そこで、 **Dataview** と **Metadata Menu** というプラグインを使って、ページ毎の進捗を動的なプログレスバーにして表示する方法を解説します。

## 完成品

![画像](https://assets.st-note.com/production/uploads/images/129045108/picture_pc_be021ce2623c420887c8f4e3ea15b5b3.gif?width=1200)

自動的に一覧のプログレスバーが更新

---

## Dataview のインストール

- Community plugins → Browse をクリック
![画像](https://assets.st-note.com/img/1706421461880-Rfg95utgMM.png?width=1200)

Community plugins → Browse をクリック

- 検索欄に **「brenan」** を入力してDataviewを見つけます
- Dataview関連のプラグインはとても多いので、この方法がおすすめです
![画像](https://assets.st-note.com/img/1706421086893-g5O4SFE8sI.png?width=1200)

コミュニティプラグイン一覧から検索し、クリック

- Install をクリック
![画像](https://assets.st-note.com/img/1706421198364-h8QqmarxPA.png?width=1200)

Install をクリック

- Enable をクリック
![画像](https://assets.st-note.com/img/1706421277205-1sMOMdx9U9.png?width=1200)

Enable をクリック

- Options をクリック
![画像](https://assets.st-note.com/img/1706421315552-CF2JcdKkvK.png?width=1200)

Options をクリック

- Enable JavaScript Queries → オン
- Enable Inline JavaScript Queries → オン
![画像](https://assets.st-note.com/img/1706421362810-WJDgCzIiiN.png?width=1200)

Enable JavaScript Queries と Enable Inline JavaScript Queries をオン

---

## Metadata Menu のインストール

![画像](https://assets.st-note.com/img/1706421461880-Rfg95utgMM.png?width=1200)

Community plugins → Browse

- Metadata Menu を検索し、クリック
![画像](https://assets.st-note.com/img/1706421580421-Ey6ofxcdoy.png?width=1200)

Metadata Menu を検索し、クリック

- Install をクリック
![画像](https://assets.st-note.com/img/1706421627879-mlICz0h9xo.png?width=1200)

Install をクリック

- Enable をクリック
![画像](https://assets.st-note.com/img/1706421660209-wWHotqQWRk.png?width=1200)

Enable をクリック

- Options をクリック
![画像](https://assets.st-note.com/img/1706421680020-dSZcPhEOOE.png?width=1200)

Options をクリック

---

## Metadata Menu の設定

### 設定 → Class Files path の指定

- 任意の場所に Fileclass を保存するフォルダを作成します
- 今回は Vault の一番上の階層に class という名前にしました
- Class Files path に作成したフォルダを指定し、保存
![画像](https://assets.st-note.com/img/1706421840899-EFEMXt5Yaj.png?width=1200)

Class Files path に作成したフォルダを指定し、保存

- 先ほど指定したフォルダの右に＋アイコンが表示されます
- ＋アイコンをクリックし、Classを作成
![画像](https://assets.st-note.com/img/1706421879908-VH8nhuoGNg.png?width=1200)

＋アイコンをクリックし、Classを作成

- 作成が完了すると、Fileclass settings が表示されます
![画像](https://assets.st-note.com/img/1706421927682-mI4yhSQDu2.png?width=1200)

作成が完了すると、Fileclass settings が表示されます

### Class → Fileclass field の追加

- Fileclass fields というタブをクリックし、項目を追加
- progress という項目を追加し、そのノートのタスクの完了率の数字を動的に適用させる
- Field Name → progress
- Field type → Formula
- Auto update this field → オン
- Javascript formula は 以下のように設定

```javascript
Math.round((current.file.tasks.where(t => t.completed).length / current.file.tasks.length) * 100)
```

- こんな感じになればOK
![画像](https://assets.st-note.com/img/1706422197069-YzAnWRTHTE.png?width=1200)

こんな感じになればOK

---

## 進捗を表示したいページの設定

- 個別のタスクページのフロントマターに、FileClass（tasks）を追加
- まだフロントマターに記述されていない項目（progress）を挿入
- この手続きが成功すれば、progress にはページ内のタスクの完了率 0-100 が動的に表示されるようになります
![画像](https://assets.st-note.com/production/uploads/images/129044715/picture_pc_ad94c894194036be32393443f5e2cc88.gif?width=1200)

完了率 0-100 が動的に表示

---

## 一覧を作成して進捗を可視化

- 一覧のためのページを作成
- 以下のDataviewコードを貼り付け

```php
\`\`\`dataview
TABLE WITHOUT ID
file.link AS リンク,
"<progress max=100 value="+progress+"></progress>　"+progress+"%" AS 進捗
WHERE progress !=null
\`\`\`
```

- Fileclass tasks が適用されたページで進捗に変化があると、自動的に一覧のプログレスバーが更新されるようになりました

## 完成

![画像](https://assets.st-note.com/production/uploads/images/129045108/picture_pc_be021ce2623c420887c8f4e3ea15b5b3.gif?width=1200)

自動的に一覧のプログレスバーが更新

みなさんの参考になれば幸いです。

## いいなと思ったら応援しよう！

- [
	#Obsidian
	](https://note.com/hashtag/Obsidian)
- [
	#dataview
	](https://note.com/hashtag/dataview)

[![note会員1000万人突破記念　1000万ポイントみんなで山分け祭　エントリー7/8（火）まで](https://assets.st-note.com/poc-image/manual/production/20250623_1000_top_notedetail.jpg?width=620&dpr=2)](https://note.com/info/n/ncceb4a6506fc)

Obsidianのタスク進捗をプログレスバーで一覧する｜⿶⿵⿷⿴⿳
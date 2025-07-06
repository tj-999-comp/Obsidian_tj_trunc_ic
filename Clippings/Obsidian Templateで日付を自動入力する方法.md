---
title: "Obsidian Templateで日付を自動入力する方法"
source: "https://notes.yurudream.com/00+Apps%2Cservice/Obsidian/Obsidian+Template%E3%81%A7%E6%97%A5%E4%BB%98%E3%82%92%E8%87%AA%E5%8B%95%E5%85%A5%E5%8A%9B%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95"
author:
  - "[[しおんの知識の庭]]"
published:
created: 2025-07-03
description: "Obsidian Templateで日付を自動入力する方法 - しおんの知識の庭"
tags:
  - "clippings"
  - "Obsidian"
---
[しおんの知識の庭](https://notes.yurudream.com/Welcome+to+Shion's+digital+garden)

デイリーノートで振り返りをするにあたり、dateを自動入力する機能をテンプレートに持たせたい。

- [Templater](https://notes.yurudream.com/Obsidian+plugin+Templater) を使用。
- [YAML](https://notes.yurudream.com/00+Apps%2Cservice/Obsidian/YAML+front+matter) に、created dateを自動入力。（夜判断力鈍って書いたなどを判定するために時間も入れる。）
- 日毎、週毎の振り返りで作成したノートを見ることができるように、ノート内にデイリーノートへのリンクを埋め込み

以下のテンプレートをテンプレートフォルダに保存。

YYYY-MM-DDとすると、時間を表示せずに、年月日のみを表示できる。

```
\`\`\`
---
title: 
aliases: 
date: <% tp.file.creation_date() %>
tag: [""]
---
\`\`\`

[[<% tp.file.creation_date("YYYY-MM-DD") %>]]
```

[2021-09-17](https://notes.yurudream.com/2021-09-17)

[#daily/2021/10/29](https://notes.yurudream.com/00+Apps%2Cservice/Obsidian/#daily/2021/10/29)

日付用テンプレートをタグでの管理へと変更した。

```
\`\`\`
---
aliases: 
date: <% tp.file.creation_date() %>
tag: ["dairy/<% tp.file.creation_date("YYYY/MM/DD") %>",""]
---
\`\`\`

<% tp.file.cursor() %>
```

![template_dairytag.jpg](https://publish-01.obsidian.md/access/febfeb490f9f417c1b131aa29dc72ca9/00%20Apps%2Cservice/Obsidian/%E6%B7%BB%E4%BB%98%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB/template_dairytag.jpg)

Obsidian Templateで日付を自動入力する方法

Interactive graph
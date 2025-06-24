---
title: "ギャル「オタクくんのVSCodeって黒くて見にくいよね」"
source: "https://qiita.com/moririn086/items/591c9de70368dc4c5333?utm_campaign=popular_items&utm_medium=feed&utm_source=popular_items"
author:
  - "[[moririn086]]"
published: 2024-11-27
created: 2025-06-24
description:
tags:
  - "clippings"
---
![](https://relay-dsp.ad-m.asia/dmp/sync/bizmatrix?pid=c3ed207b574cf11376&d=x18o8hduaj&uid=)

## Qiitaにログインして、便利な機能を使ってみませんか？

[ログイン](https://qiita.com/login?callback_action=login_or_signup&redirect_to=%2Fmoririn086%2Fitems%2F591c9de70368dc4c5333%3Futm_campaign%3Dpopular_items%26utm_medium%3Dfeed%26utm_source%3Dpopular_items&realm=qiita) [新規登録](https://qiita.com/signup?callback_action=login_or_signup&redirect_to=%2Fmoririn086%2Fitems%2F591c9de70368dc4c5333%3Futm_campaign%3Dpopular_items%26utm_medium%3Dfeed%26utm_source%3Dpopular_items&realm=qiita)

## てかさ～聞いて～！

ねぇ、オタクくんさ〜、VSCode使ってるの見たけど…なんか黒くて暗〜いテーマ使ってるじゃん？  
あれ、めちゃくちゃ目疲れるしテンション下がるよね😩？  
だからさ、あーしがかわいくしてあげた✨

## こんな感じでかわいいんだよ！🌟

とりあえず画面イメージ見てみて！👀✨  
[![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/2829066/94681691-ba1b-fbf2-6667-e9c83733548b.png)](https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-image-store.s3.ap-northeast-1.amazonaws.com%2F0%2F2829066%2F94681691-ba1b-fbf2-6667-e9c83733548b.png?ixlib=rb-4.0.0&auto=format&gif-q=60&q=75&s=d93f5e89bf56a04cd7ae3bc7b08d10d8)  
じゃじゃ～ん✨どう！？これ！

## このテーマのこだわりポイント🎀

ピンク多めで攻めたよ！ コード書いてても「かわいい〜♡」ってなるやつ🌸  
背景は目に優しいミスティローズ、長時間のコーディングでも疲れにくいっしょ👌  
選択範囲とかカーソルの色もちゃんとピンクで統一感バッチリ💯  
コメントとかキーワードの色でテンション爆上げ！コード読むのも楽しくなるよ💃

## 簡単に使える方法教えるね！

この設定を VSCode の `settings.json` に貼り付けるだけ！簡単っしょ？

```jsonc
{
  "workbench.colorTheme": "Default Light Modern",
  "editor.fontFamily": "'Rounded M+', 'Noto Sans JP', 'メイリオ', 'ＭＳ ゴシック', monospace",
  "workbench.colorCustomizations": {
    // エディタの背景とテキストの色
    "editor.background": "#FFE4E1", // ミスティローズ
    "editor.foreground": "#000000", // 黒色

    // 選択範囲と現在の行のハイライト
    "editor.selectionBackground": "#FFB6C1", // ライトピンク
    "editor.lineHighlightBackground": "#FFD1DC", // ピンク

    // カーソルの色
    "editorCursor.foreground": "#FF69B4", // ホットピンク

    // 行番号
    "editorLineNumber.foreground": "#DB7093", // パレバイオレットレッド
    "editorLineNumber.activeForeground": "#C71585", // ミディアムバイオレットレッド

    // 括弧のマッチング
    "editorBracketMatch.background": "#FFC0CB", // ピンク
    "editorBracketMatch.border": "#FF69B4", // ホットピンク

    // エラーと警告
    "editorError.foreground": "#FF4500", // オレンジレッド
    "editorWarning.foreground": "#FFA07A", // ライトサーモン

    // ステータスバー
    "statusBar.background": "#FFB6C1", // ライトピンク
    "statusBar.foreground": "#000000", // 黒色

    // サイドバー
    "sideBar.background": "#FFF0F5", // ラベンダーブラッシュ
    "sideBar.foreground": "#000000", // 黒色

    // アクティビティバー
    "activityBar.background": "#FFC0CB", // ピンク
    "activityBar.foreground": "#000000", // 黒色
    "activityBarBadge.background": "#FF69B4", // ホットピンク
    "activityBarBadge.foreground": "#FFFFFF", // 白色

    // タブ
    "tab.activeBackground": "#FFB6C1", // ライトピンク
    "tab.inactiveBackground": "#FFE4E1", // ミスティローズ
    "tab.activeForeground": "#000000", // 黒色
    "tab.inactiveForeground": "#696969", // ディムグレー

    // スクロールバー
    "scrollbarSlider.activeBackground": "#FF69B4AA", // 半透明ホットピンク
    "scrollbarSlider.background": "#FFB6C1AA", // 半透明ライトピンク
    "scrollbarSlider.hoverBackground": "#FF69B4AA" // 半透明ホットピンク
  },
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": "comment",
        "settings": {
          "foreground": "#A020F0" // パープル
        }
      },
      {
        "scope": "string",
        "settings": {
          "foreground": "#FF1493" // ディープピンク
        }
      },
      {
        "scope": "keyword",
        "settings": {
          "foreground": "#FF69B4" // ホットピンク
        }
      },
      {
        "scope": "entity.name.function",
        "settings": {
          "foreground": "#DB7093" // パレバイオレットレッド
        }
      },
      {
        "scope": "variable",
        "settings": {
          "foreground": "#C71585" // ミディアムバイオレットレッド
        }
      },
      {
        "scope": "constant.numeric",
        "settings": {
          "foreground": "#FF4500" // オレンジレッド
        }
      },
      {
        "scope": "storage.type",
        "settings": {
          "foreground": "#FF6347" // トマト
        }
      },
      {
        "scope": "keyword.operator",
        "settings": {
          "foreground": "#FF69B4" // ホットピンク
        }
      }
    ]
  }
}
```

[17](https://qiita.com/moririn086/items/?utm_campaign=popular_items&utm_medium=feed&utm_source=popular_items#comments)

コメント一覧へ移動

新規登録して、もっと便利にQiitaを使ってみよう

1. あなたにマッチした記事をお届けします
2. 便利な情報をあとで効率的に読み返せます
3. ダークテーマを利用できます
[ログインすると使える機能について](https://help.qiita.com/ja/articles/qiita-login-user)

[新規登録](https://qiita.com/signup?callback_action=login_or_signup&redirect_to=%2Fmoririn086%2Fitems%2F591c9de70368dc4c5333%3Futm_campaign%3Dpopular_items%26utm_medium%3Dfeed%26utm_source%3Dpopular_items&realm=qiita) [ログイン](https://qiita.com/login?callback_action=login_or_signup&redirect_to=%2Fmoririn086%2Fitems%2F591c9de70368dc4c5333%3Futm_campaign%3Dpopular_items%26utm_medium%3Dfeed%26utm_source%3Dpopular_items&realm=qiita)

[535](https://qiita.com/moririn086/items/591c9de70368dc4c5333/likers)

244
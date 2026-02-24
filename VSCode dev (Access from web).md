
## 前提ルール

- トンネル名は **20文字以内**    
    - 例: `taji-mini-20260117`（OK）、`taji-mac-mini-20260117`（21文字でNG）code.visualstudio+1
- 1日1トンネル運用
    - 例: 毎日 `taji-mini-YYYYMMDD` を新規作成
    - その日の作業が終わったらトンネルを「停止＋登録削除」しておく
---
## 1. その日のトンネルを作る
## 1-1. まっさら状態の確認（任意）
一応、変なものが残ってないか確認してから始める。
```bash
code tunnel status
```

- 理想:
    - `{"tunnel": null, "service_installed": false}`
    - もしくは `"tunnel": "Disconnected"` でも、どうせ今日の分を作り直すならこのあと消すのでOK。[[code.visualstudio](https://code.visualstudio.com/docs/remote/tunnels)]​
        
## 1-2. 手動でトンネルを立てる
日付入りの名前で起動（例: 2026-01-17 の場合）:

```bash
code tunnel --name taji-mini-20260117
```
- 初回やトークン期限切れ時はブラウザが開き、GitHub / Microsoft ログインが出るので、いつものアカウントでサインイン。stackoverflow+1
- 成功するとターミナルに:
	```text
	Open this link in your browser https://vscode.dev/tunnel/taji-mini-20260117
	```
のような URL が出るので、**その日の iPad 用 URL としてメモ**しておく。[[code.visualstudio](https://code.visualstudio.com/docs/remote/tunnels)]​

## 1-3. 別シェルから status を確認
さっき `code tunnel` を打ったターミナルはそのまま残しておき、**別のターミナル** で:

```bash
code tunnel status
```

- 良い状態:
    - `"tunnel": "Connected"`
    - `"last_fail_reason": null`
- これを確認してから iPad などクライアント側の接続テストをする。
---

## 2. iPad から接続する

1. iPad のブラウザで `https://vscode.dev` を開く
2. Mac mini と **同じ GitHub / Microsoft アカウント** でサインイン。
3. その日の URL にアクセス:

```text
https://vscode.dev/tunnel/taji-mini-20260117
```

4. VS Code Web が開いて、Mac mini 上のディレクトリとターミナルが使えればOK。
---

## 3. その日の作業終了時にやること（トンネルの消し方）
「停止」と「登録削除」の2段階です。

## 3-1. まずトンネルのプロセスを止める
## a. サービスを使っていない場合（その日だけ `code tunnel` 手動起動）
その日 `code tunnel` を起動したターミナルが残っていれば、そこで `Ctrl + C`。  
別シェルから:
```bash
code tunnel status
```

- `"tunnel": null` か `"tunnel": "Disconnected"` になっていればプロセスは止まっている。[[code.visualstudio](https://code.visualstudio.com/docs/remote/tunnels)]​
    
念のため、一括 kill コマンドも覚えておくと安心:
```bash
code tunnel kill
```

- そのあとに `code tunnel status` で確認。
    
## b. サービスとして動かしている場合
もし日中にサービス化しているなら、終了時に必ずサービスを外す。
```bash
code tunnel service uninstall 
code tunnel kill          # 念のため 
code tunnel status
```

- ここで `{"tunnel": null, "service_installed": false}` になっていれば「プロセスとしては何も残っていない」。[[code.visualstudio](https://code.visualstudio.com/docs/remote/tunnels)]​

## 3-2. トンネルの「登録情報」を消す（その日の分を破棄）
その日のトンネル名を VS Code / トンネルサービスから忘れさせる:
```bash
code tunnel unregister
```

- これは「このマシンに紐づいたトンネル登録」をクラウド側から削除するコマンド。ufl+1    
- 実行後:
    ```bash
	code tunnel status
	```

- `{"tunnel": null, "service_installed": false}` になっていれば、
    - プロセスなし
    - 自動起動サービスなし
    - 古いトンネル登録なし  
        の完全クリーン状態。
---

## 4. トラブったときの最低限チェック
日中に調子が悪くなったとき用に、「これだけ見ればよい」確認ポイントを2つだけ残しておきます。
## 4-1. Mac mini 側の状態
```bash
code tunnel status
```

- OK:
    - `"tunnel": "Connected"`    
    - `"last_fail_reason": null`
- NG 例:
    - `"tunnel": "Disconnected"`
    - `last_fail_reason` に `Error refreshing access token` や `connection closed before message completed` が入っている → クラウドとの通信 or トークン更新で死んでいる。
	この場合は一度:
	```bash
	code tunnel kill code tunnel --name taji-mini-YYYYMMDD   # その日の名前で再起動
	```
	で「今日のトンネルを立て直し」する感じで OK。

## 4-2. iPad 側
- 「トンネル名が見つかりません」 → アカウント不一致 or 古いトンネル名。
- 「タイムアウト」 → そのタイミングで `code tunnel status` を見て、`Disconnected` / `last_fail_reason` 付きになっていないか確認。
---

このルールどおりに運用していれば、
- 朝: `code tunnel --name taji-mini-YYYYMMDD` で、その日分のトンネルを作成
- 日中: 別シェルから `code tunnel status` を見て健康チェック
- 夜: `code tunnel kill` → `code tunnel unregister` でその日分を廃棄

という1日完結の運用になります。 
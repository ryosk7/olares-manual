# Olares 基本操作マニュアル

Olares（Olares One, OS 1.12.7）の基本的な使い方をまとめた、一般ユーザー向けの日本語マニュアルです。

**最新版のPDF:** [Releases](https://github.com/ryosk7/olares-manual/releases/latest) から次のファイルをダウンロードしてください。

- `olares-manual.pdf`：Olares 基本操作マニュアル
- `olares-voice-input.pdf`：音声入力マニュアル（Faster-Whisper と AnythingLLM で、話して入力する）

## 内容

1. Olaresにアクセスする・ログインする
2. LarePassとOlares ID
3. ユーザーを追加する（管理者向け）
4. デスクトップの画面構成
5. アプリを開く・ウィンドウを操作する
6. アプリのバッジと表示の見方
7. アプリを追加する（インストール）
8. アプリを停止する・再開する
9. アプリをアンインストールする
10. アプリの状態とリソースを確認する
11. ファイルマネージャー
12. 注意事項・よくある質問

## 音声入力マニュアルの内容

1. しくみと必要なもの
2. Faster-Whisper Large V3 を入れる（管理者）
3. AnythingLLM を入れる
4. AnythingLLM を設定する
5. マイクで話して入力する
6. 動作確認の結果
7. 注意事項・よくある質問

## 更新のしかた

- 原稿は `manual.html`（基本操作）と `voice-input.html`（音声入力）、画像は `shots/` にあります。
- `main` に push すると PDF がビルドされ、Actions の成果物として確認できます。
- 新しい版を公開するときは、変更内容をメッセージにした注釈付きタグを push します。

  ```sh
  git tag -a v1.1 -m "変更点を書く"
  git push origin v1.1
  ```

  GitHub Actions が PDF を作り、Releases に添付します。

## ローカルでのビルド（macOS）

```sh
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --no-pdf-header-footer \
  --print-to-pdf="$PWD/olares-manual.pdf" "file://$PWD/manual.html"
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --no-pdf-header-footer \
  --print-to-pdf="$PWD/olares-voice-input.pdf" "file://$PWD/voice-input.html"
```

## 出典

一部の画像は Olares 公式ドキュメントのものです。詳しくは [NOTICE](NOTICE) を参照してください。

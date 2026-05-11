# music-handaduke

アルバム「はんだづけはたのしいよ」 (Album: "Soldering is Fun")

このリポジトリには、AI生成音楽アルバム「はんだづけはたのしいよ」のデータと、ウェブベースの音楽プレイヤーが含まれています。楽曲は[Suno](https://suno.com/)を使用して作成されました。

## ▶️ ライブデモ

ウェブプレイヤーでアルバム全曲を聴くことができます:
**[https://code4fukui.github.io/music-handaduke/](https://code4fukui.github.io/music-handaduke/)**

プレイヤーの特徴:
- アルバム全曲のプレイリスト
- アルバムアート、歌詞、オリジナルのAI生成プロンプトの表示
- 再生中の曲のアートワークに合わせて動的に変化する、ぼかし背景
- ロック画面やリモート再生コントロールに対応する Media Session API の統合

## 音楽について

このアルバムは、以下の公開されているSunoプレイリストから生成されました:
- [https://suno.com/playlist/ca3142ba-48ab-411f-b837-44c60c97c1e6](https://suno.com/playlist/ca3142ba-48ab-411f-b837-44c60c97c1e6)

## プレイリストデータのダウンロード

Denoスクリプト `music-opendata-fukui` を使用すると、Sunoからオリジナルの音声ファイル、画像、メタデータをダウンロードできます。

```sh
deno run -A https://code4fukui.github.io/music-opendata-fukui/download.js https://suno.com/playlist/ca3142ba-48ab-411f-b837-44c60c97c1e6
```
このコマンドを実行すると、`playlist.json` ファイルと関連するすべてのメディアアセットを含むディレクトリが作成されます。

## ソースコード

このプロジェクトは、バニラHTML、CSS、JavaScriptで構築された自己完結型のウェブアプリケーションです。すべての音楽データはローカルの `playlist.json` ファイルから読み込まれます。

- **`index.html`**: 音楽プレイヤーのメインアプリケーションファイル。
- **`playlist.json`**: すべてのメタデータ、歌詞、およびアルバムの音声・画像ファイルへのローカルパスが含まれています。
- **`audio/` & `image_large/`**: ダウンロードしたメディアアセットが格納されているディレクトリ。

## クレジット

- 楽曲生成: [Suno](https://suno.com/)
- プロジェクト作成: [Code for FUKUI](https://github.com/code4fukui)

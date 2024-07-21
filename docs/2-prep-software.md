# 準備　- ソフトウェア編

## Cycling' 74 Maxのインストール

センサー用アプリケーションを実行するためのソフトウェアです。Maxは有料のソフトウェアですが、完成したプログラムを実行するだけなら無料で利用可能です。

以下のURLから、OSに合わせたものをダウンロードします。

バージョンは最新版（v8.3以上）のものを使用してください。

https://cycling74.com/downloads

![Maxのダウンロード画面のスクリーンショット](./img/dl_max.png)

ダウンロードしたら、zipファイルを解凍して、インストーラーアプリケーションを実行して、指示に従ってください。

<!-- todo:インストーラーダイアログの詳細な説明 -->

## センサー用アプリケーションのダウンロード

センサー用のアプリケーションは、以下のURLから最新版をダウンロードできます。

https://github.com/ccbtokyo/ccbt_tonechime_sensor/archive/refs/heads/main.zip

ダウンロードしたら、zipファイルを解凍して、フォルダごとデスクトップなどわかりやすい場所に移動しておきます。

`ccbt_tonechime_sensor/maxproject/ccbt_tonechime_sensor/ccbt_tonechime_sensor.maxproj`というファイルをダブルクリックすると、メインのアプリケーションが立ち上がります。

> [!NOTE]
> 設定のデータなどは`ccbt_tonechime_sensor/maxproject/ccbt_tonechime_sensor/data/main.json`というファイルに書き込まれています。もし新しいコンピューターで前の設定を引き継ぎたい場合は、フォルダを丸ごと前のコンピュータからコピーしてくるか、`main.json`を移動して上書きしてください。

## 映像アプリケーションのダウンロード

以下のURLから、最新のバージョンの`ToneChime_VideoSystem.zip`をダウンロードしてください。

https://github.com/ccbtokyo/ToneChime_VideoSystem/releases

ダウンロード後は、zipファイルを展開して、フォルダごとデスクトップなどわかりやすい場所に配置してください。

フォルダ内の、ToneChime_VideoSystemというアプリケーションが本体です。

[ダウンロードしてから初回の起動時はシステムに起動をブロックされることがありますが、回避可能です。トラブルシューティングを参照してください。](5-troubleshooting.md#_2)
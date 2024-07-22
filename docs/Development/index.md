## ドキュメント自体の開発

このドキュメントは、[MkDocs](https://www.mkdocs.org/)を使用して、Github Pages上にホストされています。

### 開発環境のインストール

開発環境はpoetryという、Python用のパッケージマネージャで管理されています。

poetryは、コマンドプロンプト（macOSならターミナル.app）を開き、以下のコマンドを実行することでインストールできます（インターネット接続が必要です）。

```zsh
curl -sSL https://install.python-poetry.org | python3 -
```

その後、本リポジトリの作業フォルダに移動して以下のコマンドを実行すると、MkDocsを含めた開発環境がインストールできます。

```zsh
$ cd <リポジトリのパス>
$ poetry install --no-root
```

### ローカル環境での確認

以下のコマンドを実行して、<https://localhost:8000>にアクセスすると、ローカル環境でビルドされたドキュメントが閲覧できます。

```zsh
$ poetry run mkdocs serve
```

### ビルド

静的なHTMLファイルを出力するには以下のコマンドを実行します。

```zsh
$ poetry run mkdocs build
```


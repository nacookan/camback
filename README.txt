# Camback - Up your moments.

RAWデータをローカルバックアップし、さらにS3 Glacier Deep Archiveにアップロードします。

採用フラグまたはレーティング☆1以上が対象になります。

## 準備
- `brew install exiftool`
- `brew install awscli`
- S3にバケットを作っておく
- `config.rb` を更新
- `.aws/config` を更新
- `.aws/credentials` を更新

## 実行
```
./run-camback
```

1時間に1回、バックアップ処理が動作します。中断するときは control-C　です。

差分バックアップなので、ファイルが多いと初回は時間がかかります。

## リストア
ローカルバックアップ先にはそのまま置いてあります。
S3のバケットの中にも同じディレクトリ構造で置いてあります。
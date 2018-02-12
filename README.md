# improvis

http://improvis.oto-no-sono.com のソースコード。

## 開発前提

- Docker

## 起動

```bash
docker-compose up
```

準備ができると http://localhost:4000 にアクセスできるようになります。

mp3 ファイルの容量が大きく、初回起動時のビルドに時間が掛かるため、注意してください。

## ビルド＆デプロイ

開発中に生成された `_site` は host がローカルを指しているので、
以下のコマンドで本番用のファイルを生成します。

__(fish shell)__
```
$ docker run -it -v (pwd):/app improvis_jekyll bash

root@09a0120712c0:/app# bundle exec jekyll build
```

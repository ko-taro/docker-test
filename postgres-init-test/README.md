# postgresqlで初期スクリプトを実行させる検証
* /docker-entrypoint-initdb.dにスクリプトを置いておけば実行してくれる
* スクリプトのプレフィックスに番号を入れておけばその順番に実行してくれる

# 実行方法
* docker volumeを作成する
```
$ docker volume create test-data
```

* 起動させる
```
$ docker-compose up
```
ログを見るとスクリプトが実行されていることが確認できる。
DBクライアントなどで接続すればデータが確認できる。
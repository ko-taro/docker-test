# postgresqlで初期スクリプトを実行させる検証
* /docker-entrypoint-initdb.dにスクリプトを置いておけば実行してくれる
* スクリプトのプレフィックスに番号を入れておけばその順番に実行してくれる

使い道
* ローカル開発環境を構築する時に利用できそう
* AWSのCodeBuild実行時などで、自動テストを行いたい時のDBとデータを用意するのに利用できそう

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
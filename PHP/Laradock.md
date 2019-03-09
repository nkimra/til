# Laradock

## インストール

- cloneする
~~~
$ mkdir laradock
$ cd laradock
$ git clone https://github.com/Laradock/laradock.git
~~~

- envファイルをコピーする
~~~
$ cd laradock
$ cp env-example .env
~~~

- ワークスペース起動
~~~
$ docker-compose up -d workspace
$ docker-compose exec workspace bash

# プロジェクト作成
composer create-project laravel/laravel guide
~~~

- envファイル編集
~~~
$ vi laradock/.env
# パスを修正
APP_CODE_PATH_HOST=../guide
PMA_DB_ENGINE=mariadb
~~~

- Apacheの設定
~~~
vi apache2/sites/default.apache.conf

ServerName localhost
DocumentRoot /var/www/public/
Options Indexes FollowSymLinks

<Directory "/var/www/public/">
~~~

- docker起動
~~~
docker-compose up -d mariadb apache2 phpmyadmin
~~~

- 画面確認
  - http://localhost/

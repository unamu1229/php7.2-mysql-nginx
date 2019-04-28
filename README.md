# Laravelのインストール
Laravelインストーラーはphp7.2-zipが無いのでダウンロードできない、Composer Create-Projectで作成する。
php7.2-zipを下記URLを参考に入れようとしたが、入らなかった。
https://www.rosehosting.com/blog/how-to-install-php-7-2-on-debian-9/

# DBコンテナの.envファイルの設定例
MYSQL_RANDOM_ROOT_PASSWORD=yes
MYSQL_DATABASE=laravel
MYSQL_USER=db_user
MYSQL_PASSWORD=password

一度作成したら.envファイルの設定を変えても反映されません。
volumes:
  db-data:
で最初の内容をホストに持っているから。
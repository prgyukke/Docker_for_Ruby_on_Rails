# [Docker_for_Ruby_on_Rails](https://github.com/prgyukke/Docker_for_Ruby_on_Rails)
## はじめに
Ruby on Rails開発環境用のDockerです。  
プロジェクトディレクトリを`app`コンテナ内の`/var/www/app`にマウントしています。  
OSXにて、[Docker For Mac](https://www.docker.com/docker-mac)のインストール前提です。  
[Docker Community Edition for Mac - Docker Store](https://store.docker.com/editions/community/docker-ce-desktop-mac)の[Get Docker]をクリックしてダウンロード後、インストールしてください。  

### 各バージョン
- Ruby 2.5
- Rails 5.1.6

## 環境構築
### 初回のみ
```
$ git clone git@github.com:prgyukke/Docker_for_Ruby.git
$ cd Docker_for_Ruby/
$ rm -rf .git
$ docker-compose up -d
```

### 2回目以降
```
$ cd Docker_for_Ruby/
$ docker-compose up -d
```

### コンテナに入る際
```
# mac上の`Docker_for_Ruby/docker/`にて
$ docker exec -it docker_for_ruby_on_rails_app_1 /bin/bash
```

### ビルトインサーバの立ち上げ
`http://localhost:3000/`で確認可能
```
# コンテナ上にて
# rails s -p 3000 -b '0.0.0.0'
```

### コンテナを抜ける際
```
# コンテナ上にて
# exit
```

### 開発終了時
```
$ docker-compose down
$ docker rmi docker_for_ruby_on_rails_app
```

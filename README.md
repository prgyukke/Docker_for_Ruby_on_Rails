# Docker_for_Ruby_on_Rails
## はじめに
Ruby on Rails開発環境用のDockerです。  
プロジェクトディレクトリをDocker内の`/work/app`にマウントしています。  
OSXにて、[Docker For Mac](https://www.docker.com/docker-mac)のインストール前提です。  
[Docker Community Edition for Mac - Docker Store](https://store.docker.com/editions/community/docker-ce-desktop-mac)の[Get Docker]をクリックしてダウンロード後、インストールしてください。  

### 各バージョン
- Ruby 2.5

## 環境構築
### 初回のみ
```
$ git clone git@github.com:prgyukke/Docker_for_Ruby.git
$ cd Docker_for_Ruby/
$ rm -rf .git
$ cd docker/
$ docker-compose up -d
```

### 2回目以降
```
$ cd Docker_for_Ruby/docker/
$ docker-compose up -d
```

### コンテナに入る際
```
# mac上の`Docker_for_Ruby/docker/`にて
$ docker exec -it docker_app_1 /bin/bash
```

### コンテナを抜ける際
```
# コンテナ上にて
# docker exec -it docker_app_1 /bin/bash
```

### 開発終了時
```
$ docker-compose down
$ docker rmi docker_app
```

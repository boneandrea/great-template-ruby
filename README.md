# What

Rails7-Ruby3-MySQL8 でのtemplate

# requirements
docker-compose

# 起動
```
git clone __WORKDIR__
cd __WORKDIR__
docker compose up
docker compose run --rm web rails db:migrate
docker compose run --rm web rails db:migrate RAILS_ENV=test
```
http://localhost:3000 で確認する

ポートを変更する場合は`.env`に
```
WEB_PORT=3005
```
と書く


注意:  
ホストOSの問題だと思われるが、`docker-compose up` だとCtrl-Cで止まらないかもしれない.  
`docker compose up` だと止まった


# テスト

/bin/rake
/bin/rspec
/bin/spring
を作る

```
docker compose run --rm web bundle exec spring binstub --all
```

実行
```
docker compose run --rm web bin/rspec
```


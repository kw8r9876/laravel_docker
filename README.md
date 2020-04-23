# laravel_docker

# ソースの格納場所
./app/frontend

以下を変更
package.json
```
  "scripts": {
    "dev": "NUXT_HOST=0.0.0.0 NUXT_PORT=3000 nuxt",
```

./app/backend

# 格dockerコンテナの起動
docker-compose up

# コンポーサーインストールとマイグレーション、シーディング
```
docker-compose exec php bash
```
```
composer install
```
```
php artisan migrate:refresh --seed --force
```

# nuxtjsの設定
nuxt.config.js
```
  proxy: {
    // "/api": "http://localhost:8000"
    "/api": "http://docker.for.mac.localhost:8000"
  }
```
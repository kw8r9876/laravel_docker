# laravel_docker

# 格dockerコンテナの起動
docker-compose up

# コンポーサーインストールとマイグレーション、シーディング
docker-compose exec php bash
composer install
php artisan migrate:refresh --seed --force

# nuxtjsの設定
nuxt.config.js
```
  proxy: {
    // "/api": "http://localhost:8000"
    "/api": "http://docker.for.mac.localhost:8000"
  }
```
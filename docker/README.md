# 環境構築手順

1. コンテナを作成・起動

```
docker compose up -d
```

2. A5M2 で接続

- ワークスペースを選択
- データベースを右クリック
- 追加するデータベースの接続タイプを選択
  - MariaDB(直接接続)を選択
- ユーザー ID,パスワード,ポート番号等を docker-compose.yml に記載のものに変更
- テスト接続
- OK

  3.Laravel 環境構築

  - composer create-project laravel/laravel uCRM

  - cd uCRM

  - DB 設定
    - .env の設定を以下の内容に
    ```
    DB_DATABASE=ucrm-db
    DB_USERNAME=laravel_ucrm
    DB_PASSWORD=password
    ```
  - php artisan migrate

  - composer require barryvdh/laravel-debugbar

  - composer require laravel/breeze --dev

  - php artisan breeze:install vue

  - package.json に以下を追加

  ```
  "@inertiajs/inertia": "^0.11.0",
  "@inertiajs/inertia-vue3": "^0.6.0"
  ```

  - npm install

  - npm run dev

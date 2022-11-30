# Laravel8 Render.comデプロイ （Docker + nginx）

Laravel5.8の説明は公式のドキュメントにあったので、8に合わせたサンプルアプリ

nginx-php-fpm のイメージをlocalのPHPバージョンに近いものに合わせました。

- local PHP 8.1.10
- Docker Image 8.1.12

`./Dockerfile`

```diff
- FROM richarvey/nginx-php-fpm:2.1.2
+ FROM richarvey/nginx-php-fpm:latest

  COPY . .
  
  # 省略
```

その他はドキュメント通りです。

- 参考
https://render.com/docs/deploy-php-laravel-docker
https://github.com/richarvey/nginx-php-fpm/blob/main/docs/versioning.md#php-8x

- このリポジトリのアプリURL
https://laravel-render-example-k70l.onrender.com/

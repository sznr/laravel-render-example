# Laravel8 Render.comデプロイ （Docker + nginx）

Laravel5.8の説明は公式のドキュメントにあったので、8に合わせたサンプルアプリ

nginx-php-fpm のイメージをlocalのPHPバージョンに近いものに合わせました。

- localのsail環境 PHP Version 8.1.10
- nginx-php-fpm PHP Version 8.1.12

`./Dockerfile`

```diff
- FROM richarvey/nginx-php-fpm:1.7.2
+ FROM richarvey/nginx-php-fpm:latest

  COPY . .
  
  # 省略
```

その他はドキュメント通りです。

- 参考
  - https://render.com/docs/deploy-php-laravel-docker

  - https://github.com/richarvey/nginx-php-fpm/blob/main/docs/versioning.md#php-8x

- このリポジトリのアプリURL
https://laravel-render-example-k70l.onrender.com/

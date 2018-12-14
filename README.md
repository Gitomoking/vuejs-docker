# vuejs-docker

## アプリケーションの作成

```sh
$ docker-compose up -d

$ docker-compose exec app sh
# npm install -g vue-cli
# vue -V

# vue init webpack my-project
```

## アプリケーションの起動

```sh
# cd my-project
# npm install
# npm run dev
```

アプリケーションは `localhost:80` で公開される．

`localhost:80` にアクセスできない場合は，webpack-dev-server の設定を変更する必要があるかもしれない．すなわち，以下のように `host:` を `0.0.0.0` に変更する．

```js:config/index.js
...
    // Various Dev Server settings
    // host: 'localhost', // can be overwritten by process.env.HOST // ここをコメントアウト
    host: '0.0.0.0' // これを追加
...
```

## 参考サイト

- [Vue.js ではじめるSPA開発](http://blog.hde.co.jp/entry/2018/03/05/130121)
- [vue.js-templates/webpack](https://github.com/vuejs-templates/webpack)
- [vue-cli のテンプレートを Docker 上で動かすときの注意](https://qiita.com/akagire/items/ed3bdcf29c07f9970f8f)

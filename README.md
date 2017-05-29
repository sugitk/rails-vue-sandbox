こちらを参考にしてやってみる
http://qiita.com/jnchito/items/30ab14ebf29b945559f6

```
$ gem install rails

$ rails -v
Rails 5.1.1

$ rails new rails-vue-sandbox --webpack=vue

$ cd rails-vue-sandbox
$ rails s
```

http://localhost:3000

```
$ brew install yarn
$ rails webpacker:install
```

hello_vue.js を表示する画面を作成。

```
$ bin/webpack でコンパイル
$ rails s
```

サンプルを入れてみる。
https://jp.vuejs.org/v2/examples/grid-component.html

- HTML (app/views/home/index.html.erb)
- JavaScript (app/javascript/packs/hello_vue.js)
- CSS (app/assets/stylesheets/home.scss)

```
$ yarn upgrade vue
$ bin/webpack
$ rails s
```

config/webpack/shared.js を修正しないと動作しなかった。

```
  resolve: {
    extensions: settings.extensions,
    modules: [
      resolve(settings.source_path),
      'node_modules'
    ],
    alias: {
      vue: 'vue/dist/vue.common.js'
    }
  },
```
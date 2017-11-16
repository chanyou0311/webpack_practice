# webpack_practice

## webpackとは
webpackとは、分割された複数のjsファイルやcssファイル、imgファイルなどを統合してくれるツール、という認識。

## インストール
### webpackのインストール
nodeとnpmのインストールはbrewでできると思う。環境に応じてググってください。

npmコマンドでwebpackインストールできます。プロジェクトのディレクトリに移動しているものとします。

```
$ npm init
# 設定項目。全部EnterでOKとのこと。
# 全部Enterするなら npm init -y でも可。

$ npm install webpack --save-dev
# package.jsonにwebpackを記述
```

`--save-dev` オプション以外にも `--save` などある。
詳細は[こちら](https://qiita.com/msakamoto_sf/items/a1ae46979a42d6948ebd#--save----save-dev----save-optional-%E3%81%AE%E9%81%95%E3%81%84)を参照

ちなみにグローバルにインストールも可能
```
$ npm install webpack -g
```

## ビルド
main.jsに出力処理、index.htmlでbundle.jsを読み込む記述をしておく。

```
$ node_modules/webpack/bin/webpack.js main.js bundle.js
```

でビルドできる。
index.htmlを開いてみるとmain.jsが実行される。すごいね。

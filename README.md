# npm-scripts_front-end
タスクランナーに頼らないシンプルな開発環境です。

## npm-scripts

![node%40lts-8.12.0-green.svg](https://img.shields.io/badge/node%40lts-8.16.0-green.svg) ![npm-6.4.1-green.svg](https://img.shields.io/badge/npm-6.4.1-green.svg)

##  前提条件

以下のバージョンのNode.jsインストールされていること。

![node%40lts-8.12.0-green.svg](https://img.shields.io/badge/node%40lts-8.16.0-green.svg)

```
~ node -v
v8.16.0
```

## 使用方法

1. githubから `npm-scripts_front-end` をダウンロードします。

2. `npm-scripts_front-end` ファイルを複製してリネームします。

3. 複製〜リネームしたフォルダに移動して `npm install` を実行します。

```
npm install
```

4. インストール終了後、`npm start` を実行します。

```
npm start
```
5. ローカルサーバが立ち上がり、ファイルの監視が始まります。


## ローカルサーバの停止方法

`ctrl` + `c` でローカルサーバを停止することができます。

## 他の開発環境で動かす場合(Wordpress等)

11行目を以下のように書き換えください。

```
  "serve": "browser-sync start --proxy $npm_package_config_proxy --files \"**/*.css, *.php\"",
```

## 注意事項
`package.json`15行目のconfigで環境変数を設定していますので、環境に合わせて適宜修正してください。  
設定を変更しないと上手く動かない事があります。

```
"config": {
  "proxy": "http://localhost:9000/", #動的サイトのホスト
  "scss": "./scss", #scssのディレクトリ
  "css": "./css" #cssのディレクトリ
},
```

## ディレクトリ構成

```
npm-scripts/
　├ package.json
　├ .stylelintrc.json #stylelint設定ファイル
　└ scss/
　 　└ style.scss
```

## パッケージ構成

|パッケージ|バージョン|詳細|
|--|--|--|
|autoprefixer|^9.1.5|プレフィックス自動付与|
|bootstrap|^4.1.3|CSSフレームワーク|
|browser-sync|^2.26.0|ブラウザ自動リロード|
|concurrently|^4.0.1|並列実行ツール|
|jquery|^3.3.1|JavaScriptライブラリ|
|node-sass|^4.9.3|sassコンパイル|
|parallelshell|^5.0.2|シェルコマンド並列実行ツール|
|popper.js|^1.14.4|ツールチップ実装スクリプト|
|postcss-cli|^6.0.0|PostCSSのCLI|
|stylelint|^9.6.0|style用linter|
|stylelint-order|^1.0.0|style自動修正ツール|
|stylelint-scss|^3.3.1|scss用linter|

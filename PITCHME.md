### nuxtjs_firebase_introduction
SPA×SSR×PWA×サーバーレスのWebアプリケーションについて


---

### Nuxt.js
* Vue.jsアプリケーションを作るためのフレームワーク
* サーバーサイドレンダリングや静的なVue.jsアプリケーションを簡単に作ることができる
* Vuexストアは標準で利用可能

---

### Firebase
* Googleが提供するモバイル開発プラットフォーム（mBaaS）
* 手間の掛かるバックエンドのあれこれをマネジメントしてくれる
* Firebase HostingとCloud Functions for Firebaseという2つのサービスを利用

---

### Firebase
* Firebase Hosting  
→静的ファイルのホスティングサービス、クライアントから直接参照されるファイルのホスティングに利用

* Cloud Functions  
→サーバーレスでアプリケーション開発を行えるサービス(Faas)

---
### 注意点
Cloud FunctionsではNode.js v6.11.5しか利用できない
そのため、Nuxt.jsのバージョンはNode.js v6.11.5をサポートしている1.0.0-rc11を利用し、依存関係も解決する必要

---
### 環境構築

vue-cliインストール

```
$ npm install -g vue-cli
```
プロジェクト作成
```
// プロジェクトディレクトリ作成
$ mkdir <project-name>

// Cloud Functions用ディレクトリ作成
$ cd <project-name>
$ mkdir functions

// Nuxt.jsスターターテンプレートをインストール
$ vue init nuxt-community/starter-template src
```
---
### 環境構築
詳しくは下記資料参考
https://inside.dmm.com/entry/2018/04/10/nuxt-firebase

---
### PWA導入

その前にPWAとは？

---
* Progressive Web Appsの略
* モバイルユーザーのUX向上を目的とした、WEBページ／WEBアプリケーションとネイティブアプリの利点をいいとこ取りできる仕組み
* モバイル端末でページを表示する時にネイティブアプリのような挙動をさせることが出来る

---
### PWAのメリット

* オフラインでも動く
* プッシュ通知の受信が可能
* インストール不要
* ストアの審査なくアップデートが可能
* ネイティブアプリのようなUIを実現できる
 * 「ホームに追加」ボタンを表示でき、ホームに追加されたページはインストールされたアプリのように扱える
 * ホーム画面のアイコンが設定できる
 * 起動時のスプラッシュ画面が設定できる
 * URL非表示
　
---
### PWA導入
インストール
```
 npm install --save-dev @nuxtjs/pwa
```
`src/nuxt.config.js`にPWAの設定を追記

```
module.exports = {
  modules: [
    '@nuxtjs/pwa'
  ],
  manifest: {
    name: 'project-name',
    lang: 'ja'
  }
};
```
PWA用のアイコン画像`src/static/icon.png`を設置
不要であれば`src/nuxt.config.js`を下記のように修正
```
modules: [
    ['@nuxtjs/pwa', { icon: false }],
],
```
---













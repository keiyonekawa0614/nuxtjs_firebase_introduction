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
下記資料参考
https://inside.dmm.com/entry/2018/04/10/nuxt-firebase











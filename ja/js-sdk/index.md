# code.js ライブラリについて

code.js ライブラリは、ユーザーとウェブサイトの接点を測定し、ウェブ接客を実施する JavaScript ライブラリです。このガイドでは、サイトに code.js を追加する方法について説明します。
初めてご利用になるお客様は[クイックスタート](./quick-start.html)よりご覧ください。

### 用途から見る

- [クイックスタート](./quick-start.html)
- [動的クリエイティブテンプレートを利用する](./dynamic-variable.html)

### 計測情報から見る

- [会員情報の計測](./user-tracking.html)
- [ECトラッキング](./ec-tracking.html)
- [サイト内検索](./page-tracking.html)

### メソッドから見る

- [init](#init): CodeConf情報を利用して初期化する
- [load](#load): conf設定を読み込む
- track: イベント情報を送信する
  - [user](#trackuser): クライアントサイト側で保持しているユーザー情報を送る
  - [item](#trackitem): 商品閲覧情報を送る
  - [transaction](#tracktransaction): 購入情報を送る
  - [cart](#trackcart): カート情報を送る
  - [favorite](#trackfavorite): お気に入り追加情報を送る
- [variable](#trackvariable): 動的テンプレートに埋め込む値（のうち、イベント情報には当てはまらないもの）をクライアント側から送る
- [仮想ページビュー設定](#仮想ページビュー設定): 送信するページURL・タイトルを変更する

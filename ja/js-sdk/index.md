# code.js ライブラリについて

code.js ライブラリは、ウェブサイトを訪れたユーザーを識別し、ウェブ接客を実施する JavaScript ライブラリです。このガイドでは、サイトに code.js を追加する方法について説明します。
初めてご利用になるお客様は[クイックスタート](./quick-start.html)よりご覧ください。

### 用途から見る

- [クイックスタート](./quick-start.html)
- [動的クリエイティブテンプレートを利用する](./client-variable.html)

### 計測情報から見る

- [会員情報の計測](./track-user.html)
- [Eコマース関連の情報の計測](./track-ec.html)
  - [閲覧アイテム情報の計測](./track-item.html)
  - [購入情報の計測](./track-transaction.html)
  - [カート情報の計測](./track-cart.html)
  - [お気に入り追加情報の計測](./track-favorite.html)
- [サイト内検索](./track-page.html)

### メソッドから見る

- track: イベント情報を送信する
  - [user](./track-user.html): クライアントサイト側で保持しているユーザー情報を送る
  - [item](./track-item.html): 商品閲覧情報を送る
  - [transaction](./track-transaction.html): 購入情報を送る
  - [cart](./track-cart.html): カート情報を送る
  - [favorite](./track-favorite.html): お気に入り追加情報を送る
  - [page](./track-page.html): ページURL・タイトルをカスタマイズして送信する
- [variable](./client-variable.html): 動的テンプレートに埋め込む値（のうち、イベント情報には当てはまらないもの）をクライアントサイト側から代入する

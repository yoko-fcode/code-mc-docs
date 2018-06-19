# code.js ライブラリについて

code.js ライブラリは、ウェブサイトを訪れたユーザーを識別し、ウェブ接客を実施する JavaScript ライブラリです。このガイドでは、サイトに code.js を設置する方法について説明します。

### code.js の設置方法

サイトの各ページのHTMLにJavaScript形式の計測タグを追加することでcode.js ライブラリを利用することができます。

### 追加する計測タグの種別

追加する計測タグは下記の2つに区別されます。

#### 1. 全ページ共通で貼り付けを実施する計測タグ

サイトの全ページに共通で貼り付ける計測タグです。詳しくは[計測タグの設置](./quick-start.html)よりご覧ください。

#### 2. 使用用途やページに合わせて追加で貼り分けを実施するカスタマイズタグ

「CODE Marketing Cloud」では、下記に関する計測タグのカスタマイズをオプション提供しています。
ページ内で1に加えてカスタマイズタグを設置することで、code.js ライブラリ内の指定のメソッドを呼び出すことができます。
これにより、動的クリエイティブテンプレートの利用などが可能となります。

##### 計測したい情報から見る

- [会員情報の計測](./track-user.html)
- [Eコマース関連の情報の計測](./track-ec.html)
  - [閲覧アイテム情報の計測](./track-item.html)
  - [購入情報の計測](./track-transaction.html)
  - [カート情報の計測](./track-cart.html)
  - [お気に入り追加情報の計測](./track-favorite.html)
- [サイト内検索](./track-page.html)
- [動的クリエイティブテンプレートを利用する](./client-variable.html)

##### メソッドから見る

- track: イベント情報を送信する
  - [user](./track-user.html): クライアントサイト側で保持しているユーザー情報を送る
  - [item](./track-item.html): 商品閲覧情報を送る
  - [transaction](./track-transaction.html): 購入情報を送る
  - [cart](./track-cart.html): カート情報を送る
  - [favorite](./track-favorite.html): お気に入り追加情報を送る
  - [page](./track-page.html): ページURL・タイトルをカスタマイズして送信する
- [variable](./client-variable.html): 動的テンプレートに埋め込む値（のうち、イベント情報には当てはまらないもの）をクライアントサイト側から代入する

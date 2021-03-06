# 2. 目標の設定

「CODE Marketing Cloud」でウェブ接客の成果を計測するために、サイトの目標を管理画面上で設定する必要があります。本ページでは目標の設定方法についてご説明します。

![画像](/ja/images/site-setting.PNG)

サイト設定では運用中サイトとして設定中のドメインの確認と目標の一覧確認及び追加が行なえます。

## 目標とは

購入や会員登録などのコンバージョンにおいて経由するURLや、経由するページ上に仕込まれたスクリプトによるイベント送信を紐づけることでコンバージョンは計測されます。この紐づけが目標であり、このページで一覧化されます。

## 目標の設定方法

目標の設定方法は下記の2種類があります。

- URLによる設定
  - 購入や会員登録などの特定のURLをユーザーが経由したことを計測する方法です。
- イベントトラッキングによる設定
  - 特定のURLにおいて、ユーザーが特定のイベントを発生させたことを計測する方法です。

### URLによる設定

![画像](/ja/images/add-goal.PNG)

- 目標の「対象ページの指定」には「前方一致」「完全一致」「正規表現一致」が選択できます。
- 通常はドメイン後のスラッシュから指定しますが、「URLの計測方法」について「httpからを指定」を設定している場合には、URLをhttpからの指定する必要があります。
- URLで目標を設定する場合、購入金額や商品数などの追加情報は収集できません。
- 「ステイタス」を「ON」として「目標の登録」を実施してください。

### イベントトラッキングによる設定

- 上記のURL指定に加えて、「イベントトラッキング」を設定します。
- 「特定のイベントをコンバージョンとして計測」にチェックを入れ、「対象の要素」「対象のイベント」をjQueryのセレクター・イベントの記載方法に沿ってご指定ください。
  - 例：スマホでの電話番号タップをイベントトラッキングにより目標として指定したい場合、 ``a[href^=tel]`` の ``click tap`` を指定

<!--
### イベント送信で目標を設定する

コンバージョンが発生するページにコンバージョンの内容を「CODE Marketing Cloud」に送信するタグスニペットを設置することでコンバージョンを測定できるようになります。詳細は [code.jsライブラリについて](/ja/js-sdk/)を参照ください。
-->

### 目標に関する留意点

- 追加できる目標は1サイトに50件までとなります。

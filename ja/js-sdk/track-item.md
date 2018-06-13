# 閲覧アイテム情報の計測

``track:item``メソッドのタグスニペットを設置することで、商品閲覧情報を「CODE Marketing Cloud」に連携することが可能です。

## ``track:item``メソッドについて

code.js 内で商品閲覧情報を収集するイベントを発生させるためのメソッドです。

## ``track:item``メソッドの設置が必要なケース

以下のケースで、``track:item``メソッドの設置が必須となります。

- 商品閲覧情報を活用する動的クリエイティブテンプレートを利用して接客を行いたい

## ``track:item``メソッドの設置場所

ログイン機能のあるサイトで商品閲覧情報を「CODE Marketing Cloud」に連携する場合は、その情報を取得できるページに``track:item``メソッドタグを設置してください。

## ``track:item``メソッドの設置方法

``track:item``メソッドタグの設置場所や内容は、サイト側の実装に大きく依存します。以下に記載した``track:item``メソッドタグの設置場所やサンプルコードを参考に、サイトに合わせた記述に書き換えてください。

### 例：商品閲覧情報を送信する

```
_cc('track', 'item', {
    itemId: "0001",
    name: "Tシャツ 黒",
    sku: "SKU1",
    price: 5000,
    quantity: 1,
    itemUrl: 'http://sample.com/detail/0001',
    itemImageUrl: 'http://sample.com/images/0001.png',
    category: "catA",
    brand: "brandB"
});
```

### ``track:item``コマンドの第三引数に利用できるプロパティ

第三引数に指定することで、下記の属性情報を収集することが可能です。

| プロパティ名 | 概要 | 例 | 型 |
|:--------:|:--------:|:--------:|:--------:|
| itemId | 商品ID | "0001" | 文字列 |
| name | 商品名 | "Tシャツ 黒" | 文字列 |
| sku | | "SKU1" | 文字列 |
| price | 商品単価 | 5000 | 数値 |
| quantity | 購入数量 | 1 | 数値 |
| itemUrl | アイテムページURL | "http://sample.com/detail/0001" | 文字列 |
| itemImageUrl | アイテム画像URL | "http://sample.com/images/0001.png" | 文字列 |
| category | 商品カテゴリ | "catA" | 文字列 |
| brand | 商品ブランド | "brandB" | 文字列 |

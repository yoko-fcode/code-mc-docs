# 購入情報の計測

``track:transaction``メソッドをタグスニペットに追加することで、購入情報を「CODE Marketing Cloud」に連携することが可能です。

## ``track:transaction``メソッドについて

code.js 内で購入情報を収集するイベントを発生させるためのメソッドです。

## ``track:transaction``メソッドの設置が必要なケース

以下のケースで、``track:transaction``メソッドの設置が必須となります。

- 購入情報を活用する動的クリエイティブテンプレートを利用して接客を行いたい
- 売上・購入アイテム数等を用いて成果計測をしたい

### ``track:transaction``メソッドの設置場所

ログイン機能のあるサイトで会員情報を「CODE Marketing Cloud」に連携する場合は、その情報を取得できるページに``track:transaction``メソッドタグを設置してください。

### ``track:transaction``メソッドのサンプルコード

#### 例：購入情報を送信する

```
var items = [{
    itemId: "0001", // 商品ID
    name: "Tシャツ 黒", // 商品名
    sku: "SKU1",
    price: 5000, // 商品単価
    quantity: 1, // 購入数量
    itemUrl: '',
    itemImageUrl: '',
    category: "catA", //商品カテゴリ
    brand: "brandA" //商品ブランド
}, {
    itemId: "0002",
    name: "Tシャツ 白",
    sku: "SKU2",
    price: 5000,
    quantity: 1,
    itemUrl: '',
    itemImageUrl: '',
    category: "catA",
    brand: "brandB"
}];

_cc('track', 'transaction', {
    transactionId: "00001", // ユニークなトランザクションID
    revenue: 10000, // 売上
    items: items, // 生成した個別の商品情報
    tax: 10, // 税額
    shipping: 100, // 配送料
    usedPoint: 100, // （例）100ポイント使用
    usedCoupon: 500 // （例）クーポン500円分使用
});
```

#### 例：カートから1つ商品を削除

```
_cc('track', 'cart', {
    action: 'remove',
    items: [{
      itemId: '003',
      name: 'テスト商品3',
      category: 'テストカテゴリ',
      price: 1980,
      quantity: 1
    }]
});
```

#### 例：カートを空にする処理。

- 購入完了ページなどで使用します。

```
_cc('track', 'cart', {
    price: 0,
    action: 'clear'
});
```

### ``track:transaction``メソッドの第三引数に利用できるプロパティ

| プロパティ名 | 概要 | 例 | 型 |
|:--------:|:--------:|:--------:|:--------:|
| transactionId | ユニークなトランザクションID | "00001" | 文字列 |
| revenue | 売上 | 10000 | 数値 |
| items | 生成した個別の商品情報 | items | itemフォーマットのオブジェクトの配列 |
| tax | 税額 | 10 | 数値 |
| shipping | 配送料 | 100 | 数値 |
| usedPoint | 使用したポイント(Xポイント使用) | 100 | 数値 |
| usedCoupon | 使用したクーポン(X円分使用) | 500 | 数値 |

- itemフォーマットの詳細については[閲覧アイテム情報の計測](./track-item.html)ページをご覧ください。

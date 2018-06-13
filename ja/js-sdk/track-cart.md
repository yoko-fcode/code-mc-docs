# カートに対する追加／削除等の情報の計測

``track:cart``メソッドのタグスニペットを設置することで、カートに対する追加／削除等の情報を「CODE Marketing Cloud」に連携することが可能です。

## ``track:cart``メソッドについて

code.js 内でカートに対する追加／削除等の情報を収集するイベントを発生させるためのメソッドです。

## ``track:cart``メソッドの設置が必要なケース

以下のケースで、``track:cart``メソッドの設置が必須となります。

- カートに対する追加／削除等の情報を活用する動的クリエイティブテンプレートを利用して接客を行いたい

## ``track:cart``メソッドの設置場所

ログイン機能のあるサイトでカートに対する追加／削除等の情報を「CODE Marketing Cloud」に連携する場合は、その情報を取得できるページに``track:cart``メソッドタグを設置してください。

## ``track:cart``メソッドの設置方法

``track:cart``メソッドタグの設置場所や内容は、サイト側の実装に大きく依存します。以下に記載した``track:cart``メソッドタグの設置場所やサンプルコードを参考に、サイトに合わせた記述に書き換えてください。

### 例：カートに商品が追加

```
_cc('track', 'cart', {
    action: 'add',
    items: [{
        itemId: '001',
        name: 'テスト商品1',
        category: 'テストカテゴリ',
        price: 1000,
        quantity: 1
    }, {
        itemId: '002',
        name: 'テスト商品2',
        category: 'テストカテゴリ',
        price: 980,
        quantity: 2
    }, {
        itemId: '003',
        name: 'テスト商品3',
        category: 'テストカテゴリ',
        price: 1980,
        quantity: 1
    }]
});
```

### 例：カートから1つ商品を削除

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

### 例：カートを空にする処理

- 購入完了ページなどで使用します。

```
_cc('track', 'cart', {
    price: 0,
    action: 'clear'
});
```

### track:cartコマンドの第三引数に利用できるプロパティ

| プロパティ名 | 概要 | 例 | 型 |
|:--------:|:--------:|:--------:|:--------:|
| action | カートへのアクション種別 | "add" | 文字列("add" or "remove" or "clear") |
| category | カートの種別 | "shopA" | 文字列 |
| items | 生成した個別の商品情報 | items | itemフォーマットのオブジェクトの配列 |

- itemフォーマットの詳細については[閲覧アイテム情報の計測](./track-item.html)ページをご覧ください。
- category属性は、モールサイトなど、1サイト内にカートが複数ある場合に使用します。
# カートに入れた商品が一定時間購入されない場合ポップアップでお知らせ

ユーザーがカートに商品を入れた後に一定期間購入しないままサイトに滞在すると、買い忘れ防止を呼びかけるポップアップを表示します。
* 通知までの時間は固定で30分間です。
* カート内のアイテムが更新された最後のタイミングから30分間経過後にポップアップが表示されます。
* 30分経過を待たずに購入によりカートが空になった、またはカート内アイテム削除によりカートが空になった場合にはポップアップは表示されません。

* このテンプレートを利用するにはカート内の状況を補足するタグによるメソッド呼出が必要です。
* タグによるメソッド呼び出しについては[こちら](/ja/js-sdk/track-cart.md)をご確認ください。

# 導入事例

``load``メソッドの引数もしくは``track:page``メソッドの引数を指定することで、「CODE Marketing Cloud」に収集するページURL・タイトル・参照元URLのカスタマイズが可能です。

## 本カスタマイズが必要なケース

以下のケースで、本カスタマイズを推奨します。

- ページURLに基づいてターゲティングを行う場合に、ページURLを実際のURLから変更したい
- ページURLに基づいてコンバージョン計測を行う場合に、ページURLを実際のURLから変更したい
- サイト内検索をPOST送信で実装しているサイトにおいて、サイト内検索キーワードも「ページターゲティング条件」の設定に使用したい

## 本カスタマイズの実施方法

- ページ表示時に``load``メソッドの第三引数内に``pageInfo``オブジェクトを作成し、その変数としてページ情報をセットする必要があります。[^1]
```
_cc('load', '@ACCOUNT_ID', '@SITE_ID',{
  pageInfo: {
    'url': "/casestudy/",
    'title' : "導入事例",
    'referrer' : "https://facebook.com"
  }
});
```

- Ajaxなど非同期通信による検索結果の更新をトラッキングする場合は、更新が実施されるごとに下記のメソッドを呼び出すことをおすすめします。
```
_cc('track', 'page', {
  'url': "/casestudy/",
  'title' : "導入事例",
  'referrer' : "https://facebook.com"
});
```

### ``load``メソッドの第四引数もしくは``track:page``メソッドの第三引数に利用できるプロパティ

第三引数に指定することで、下記の属性情報を収集することが可能です。

| プロパティ名 | 必須 | 概要 | 例 | 型 |
|:--------:|:--------:|:--------:|:--------:|:--------:|
| url | × | ページURL | "/casestudy/" or "https://codemarketing.cloud/casestudy/" | 文字列 |
| title | × | ページタイトル | "導入事例" | 文字列 |
| referrer | × | 参照元URL | "https://facebook.com" | 文字列 |

#### 留意点

- URLパラメータ（「?」以降の文字列）やフラグメント（「#」以降の文字列）を使用しておりページ計測やターゲティング条件の判別等に使用したい場合、``url``プロパティ上にURLパラメータも付与するようにしてください。
  - 例：https://codemarketing.cloud/casestudy/?paramater_x=xxxx#internal_link_yyyy
- ``url``プロパティ上で送信するURLの形式は、下記の通り、「サイト設定」において「URLの形式」に沿って作成するようにしてください。

| URLの形式 | 例 |
|:--------:|:--------:|
| ドメイン後のスラッシュ(/)からの文字列 | "/casestudy/" |
| httpからの文字列 | "https://codemarketing.cloud/casestudy/" |

## 注

[^1]: ``@ACCOUNT_ID``・``@SITE_ID``の扱いについては[JavaScript トラッキング スニペット](./quick-start.html)をご覧ください。

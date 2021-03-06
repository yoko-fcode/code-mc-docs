# 計測タグの設置

ウェブサイトを訪れたユーザーを識別し、ウェブ接客を実施するためにサイトの全ページに共通で貼り付けるコード（JavaScript トラッキング スニペット）を「CODE Marketing Cloud」では計測タグと読んでいます。
このページでは、サイトに計測タグを設置する方法について説明します。

## 計測タグの内容

計測タグの内容は下記の通りです。

```
<script async src="@CODE_TAG_URL"></script>
<script>
  window._cq = window._cq || [];
  function _cc(){_cq.push(arguments);}
  _cc('load', '@ACCOUNT_ID', '@SITE_ID');
</script>
```

- また、上記のうち、@で始まる文字列部分にはそれぞれサイトごとに固有の値が入ります。詳しくは「CODE Marketing Cloud」管理画面内の[「タグの確認」画面](/ja/in-browser/tracker-tag.html)をご覧ください。

| 文字列 | 概要 | 例 |
|:--------:|:--------:|:--------:|
| @CODE_TAG_URL | code.js ライブラリ | //codemarketing.cloud/js-sdk/code-1.0.min.js |
| @ACCOUNT_ID | アカウントID | 0001 |
| @SITE_ID | サイトID | 0122 |

- ページURL・タイトルを実際のものから変更したい場合は専用のメソッドにより[ページURL・タイトルをカスタマイズして送信する](./track-page.html)ことが可能です。

## タグの貼り付け位置

貼り付け位置に関しては、下記の位置をおすすめします。

1. このコードは ``<head>`` タグの先頭付近で、他のスクリプトや CSS タグの前に追加することをおすすめします。
1. 上記が難しい場合、 ``<body>`` タグの先頭付近、他のスクリプトや CSS タグの前に追加することをおすすめします。

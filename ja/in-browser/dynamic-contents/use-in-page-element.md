# ページ内要素を利用した動的表示

ページ内要素を利用した動的表示ではユーザーが閲覧中のページ内の情報を利用して動的なコンテンツを表示します。ここではカート内金額を表示するページ内要素を利用し、送料無料までの金額を表示するクリエイティブを例として説明します。


## カート内金額を表示するページ内要素をサイト設定から登録
「CODE Marketing Cloud」をご利用のサイトでカート内金額を示すページ内要素をセレクタ名で指定します。
* セレクタに対して値が2つ以上ある場合、正しくない値が表示される場合があります。


### 取得した値の置換
取得した値に対して置換を行うことができます。これは余計な文字列を取り除くためです。（円マークやカンマなど）

#### 置換用正規表現
置換する文字を指定する正規表現を入力します。

#### 置換用正規表現のオプション
置換用正規表現のオプションを指定します。

|オプション修飾子	|意味|
|:----:|:----|
|i	| 大文字と小文字を区別せずにマッチを行う|
|x	| パターンの中の空白やコメントを無視する|
|s| 	メタ文字(.)が改行にマッチ|
|m| 	対象の文字列を複数行として扱う|
|o	| 正規表現のコンパイルを1回だけ行う|
|g	| 繰り返しマッチを行う|
|e | 	置換を行った結果を式として処理する|

通常は ``g`` と記入してください。

#### 置換後文字列
置換後の文字列を入力します、通常は空白のままにしてください。

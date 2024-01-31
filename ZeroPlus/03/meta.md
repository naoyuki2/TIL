# meta

https://zeroplus.notion.site/meta-d7c12f30f15342b7876831841ab35106

`head`タグ内に記述する、Webページの情報を記載するためのタグ。

適切に設定することでSEOで上位を獲得できる。

# charset

文字コードを設定する

# viewport

サイトのページが表示される画面の大きさを指定する

レスポンシブの際にも必要

# title

検索結果でWebページのタイトルになるタグ

# description

検索結果でタイトルの下に表示されてるやつ

# format-detection

スマホでアクセスしたときに、8桁の数字に対して間違って電話しないように機能を無効化できる

# favicon

ブラウザのタグに表示されるアイコン

# apple-touch-icon

ショートカット作成時のアイコン

# OGP

`Open Graph Protocol`の略

SNSでシェアされたときに表示される情報

# Webページに最低限書いておくべきmetaタグ

```
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>ページタイトル</title>
<meta name="description" content="ページの説明" />
<meta name="format-detection" content="telephone=no" />
<link rel="icon" href="favicon.png" type="image/png" />
<link rel="icon" href="favicon.svg" type="image/svg+xml" />
<link rel="apple-touch-icon" href="webclip.png" />
<meta property="og:site_name" content="ページタイトル" />
<meta property="og:url" content="URL" />
<meta property="og:type" content="website or article" />
<meta property="og:title" content="ページのタイトル" />
<meta property="og:description" content="ページの説明" />
<meta property="og:image" content="URL" />
<meta property="og:locale" content="ja_JP" />
<meta property="fb:app_id" content="AppID">
<meta name="twitter:card" content="summary_large_image or summary" />
<meta name="twitter:site" content="@twitter_id" />
<meta name="twitter:description" content="ページの説明" />
<meta name="twitter:image:src" content="URL" />`
```

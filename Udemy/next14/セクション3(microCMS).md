# 初期設定
microCMSのドキュメント  
https://document.microcms.io/tutorial/next/next-app-router-getting-started

service-domain は左上の'nbookcommerce'が該当。または、上記URLのxxxx.microcmsioのxxxxのところ。
<img width="454" alt="image" src="https://github.com/naoyuki2/TIL/assets/135786069/a5aae061-fc4e-4d9d-86b1-0334e5045196">

apiKey はサイドバーにある。

上記二つは一応envファイルにまとめておく。NEXT_PUBLICというプレフィックスをつけると本番環境でもアクセスできる。
```
NEXT_PUBLIC_SERVICE_DOMAIN="nbookcommerce"
NEXT_PUBLIC_API_KEY="xxxxx"
```
client.tsは下記
```
import { createClient } from 'microcms-js-sdk'

export const client = createClient({
    serviceDomain: process.env.NEXT_PUBLIC_SERVICE_DOMAIN!,
    apiKey: process.env.NEXT_PUBLIC_API_KEY!,
})
```
!は || "" または空と同じ意味。tsだから配慮しましょう。
# アイテム取得
getList()で取得
https://blog.microcms.io/nextjs13-microcms-rsc/

useClientではasync/awaitが使えない

画像が出力できない時はnextconfig.jsにまたかきこめ
```
{
    protocol: 'https',
    hostname: 'images.microcms-assets.io',
},
```

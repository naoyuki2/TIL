# GraphQLとは

APIのクエリ言語

APIに問い合わせをする言語

### クエリ

クエリは問い合わせ

※googleに対して`youtube`というクエリを打ち込んでいる

### API

クライアントとサーバの仲介役

# REST APIとの違い

`REST API`は情報を取得する際にひとつづつAPIリクエストが必要

対して`GraphQLは`一つのエンドポイントで複数のデータを取得できる

![image](https://github.com/naoyuki2/TIL/assets/135786069/b2ca1e39-936a-416f-82fd-dd95bb35478e)

`REAR API`は`id`の情報だけが欲しくても他のデータを取ってきてしまう

オーバーフェッチング`と呼ばれる。

![image](https://github.com/naoyuki2/TIL/assets/135786069/3c521667-9809-4d67-afb0-d717fe664b06)

対して`GraphQL`は、リクエストの際に欲しい情報を指定できる

![image](https://github.com/naoyuki2/TIL/assets/135786069/e577929e-2ae6-4ce1-92b9-c7c9042c9e64)

# メリット

![image](https://github.com/naoyuki2/TIL/assets/135786069/51362f03-008f-4629-b5ff-b5461ff88cee)


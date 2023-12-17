# Prismaとは
次世代オープンソースORM
https://www.prisma.io/docs

# ORM(object relational mapping)
SQL知らん人のためにJSのメソッドでクエリが書けるようにしたもの。

<img width="960" alt="image" src="https://github.com/naoyuki2/TIL/assets/135786069/46c7b999-04ba-46f8-a6aa-0c09cae862cd">

# model
modelの後にテーブル名 
カラム名　型　ディティール  
@カラム名で主キー
```
model User {
  id    Int     @id @default(autoincrement())
  email String  @unique
  name  String?
}
```
# CRUD
すべて非同期処理で実装する  
https://www.prisma.io/docs/orm/prisma-client/queries/crud
# Node.jsでのcreate文の例
```
app.post("/", async (req,res) => {
  const {title, body} = req.body;
  const user = await prisma.posts.create({
    data: {
      email: 'elsa@prisma.io',
      name: 'Elsa Prisma',
    },
  })
  return res.json(posts)
})
```
# Migration
jsの記述から実際にテーブルを作成するためのコマンド
https://www.prisma.io/migrate

# Studio
テーブルの内容をGUIでわかりやすく表示してくれるコマンド
https://www.prisma.io/studio

# Relations
リレーションの作成コード。  

```
//1
model User {
  id    Int    @id @default(autoincrement())
  posts Post[]
}
//多
model Post {
  id       Int  @id @default(autoincrement())
  author   User @relation(fields: [authorId], references: [id])
  authorId Int
}
```

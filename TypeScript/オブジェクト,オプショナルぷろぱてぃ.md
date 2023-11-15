# オブジェクトの型
以下のフォーマットで定義する
```
{
  <プロパティ名>: <型>;
  <プロパティ名>: <型>;
}
```
string型のnameとnumber型のageを持つPersonオブジェクトの型
```
type Person = {
  name: string;
  age: number;
};

const taro: Person = {
  name: "taro",
  age: 18,
};
```
# オプショナルプロパティ
定義するかは任意にできるやつ。taroとjiroはほとんど同じプロパティだけど、jiroにはhobbyを持たせたくない。そんな時はPersonの型定義の際に、?をつけよう。
```
type Person = {
  name: string;
  age: number;
  hobby?: string;
};

const taro: Person = {
  name: "taro",
  age: 18,
  hobby: "game",
};

const jiro: Person = {
  name: "jiro",
  age: 16,
};
```
# readonly
読み取り専用にしたいときに変数名の前に記述する。代入不可。
```
type Person = {
  readonly name: string;
  age: number;
};

const taro: Person = {
  name: "taro",
  age: 18,
};

taro.name = "TARO"; // Cannot assign to 'name' because it is a read-only property.
```
# オブジェクトのネスト
オブジェクトの中にオブジェクトが入る場合でも問題なく定義できる。
```
type Person = {
  name: string;
  age: number;
  parent: {
    name: string;
  };
};

const taro = {
  name: "taro",
  age: 18,
  parent: {
    name: "hanako",
  },
};
```

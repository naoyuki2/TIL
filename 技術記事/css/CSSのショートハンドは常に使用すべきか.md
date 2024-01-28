https://foolish-pine.com/posts/2021/06/css-shorthand

# ロングハンド

```
margin-top: 20px;
margin-right: 20px;
margin-bottom: 20px;
margin-left: 20px;
```

### メリット

- 可読性、保守性が上がる。
- 

### デメリット

- 記述量が増える。
- 

# ショートハンド
```
margin: 20px 20px 20px 20px;
```

### メリット

- 記述量が減る

### デメリット

- 以前に設定した値を上書きする可能性がある。
  - 下記のように`背景色を赤`にした後、ショートハンドで`background`プロパティを指定しているが、`color`プロパティが省略されているため、`color`が`初期値`になってしまう。
```
background-color: red;
background: url(images/bg.gif) no-repeat left top;
```

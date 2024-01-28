# gap

https://zero-plus.io/media/css-gap-how-to-use/

flexアイテム間の余白を指定できるプロパティ。

外側は指定できない

※`display:flex;`と同時に使う必要あり。

疑似クラスを使わなくてよい。

個別に指定はできない。

```
.flexbox {
  display: flex;
  gap: 20px;/*縦・横で同じ余白*/
  gap: 20px 30px;/*縦20px、横30pxの指定*/
  column-gap:; /* 縦の余白 */
  row-gap:; /* 横の余白 */
}
```

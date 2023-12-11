# イベント
クリックとかホバーとかスクロールとかマウス動いたとかのこと。それをもとに発火されるのがイベントリスナー。
```
セレクタ.addEventListener("イベント名",() => {
  //実行する処理
});
```
# 例
```
<button class="btn">
    クリックしてね
</button>
```
```
const btn = document.querySelector(".btn"); // セレクタを指定

btn.addEventListener("click", () => { // ボタンをクリックしたとき
    console.log("クリックされたよ"); // コンソールに「クリックされたよ」と表示する
})
```

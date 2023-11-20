HTMLのaタグでリンク先指定
```
<a href="/pay-split">PAY SPLIT</a>
```
app.tsでフォルダごとのRouterをインポート。.useで"/pay-split"を指定されたらpaySplitRouterに渡す。
```
import {paySplitRouter} from "./routes/pay_split";

app.use("/pay-split", paySplitRouter);
```
pay_split.tsでpaySplitRouterを定義。パスによって渡すファイルを定義する。
```
import express from "express";

const paySplitRouter = express.Router();

paySplitRouter.get("/",(req,res) => {
    res.render("pay_split/index");
});

export {paySplitRouter};
```

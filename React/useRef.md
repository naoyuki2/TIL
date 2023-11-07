React hooks の一つ。書き換え可能な値を.current プロパティ内に保持することができる箱。

# 1.DOM へのアクセス

タグ内に ref 属性で useRef の変数を渡すと、current プロパティで DOM 要素にアクセスできる。(例)input にフォーカスする。

```
import { useRef } from "react";

const inputRef = useRef(null);

useEffect(() => {
  inputRef.current.focus();
}, []);
```

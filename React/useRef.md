React hooks の一つ。書き換え可能な値を.current プロパティ内に保持することができる箱。

# １．DOM へのアクセス

タグ内に ref 属性で useRef の変数を渡すと、current プロパティで DOM 要素にアクセスできる。(例)input にフォーカスする。
(解説)インポートする。useRefをnullで代入する。useEffect(第２引数を空配列)で、レンダリング時に一度だけinput要素にフォーカスする。input要素のref属性に宣言したuseRefを代入する。
```
import { useRef } from "react";

const inputRef = useRef(null);

useEffect(() => {
  inputRef.current.focus();
}, []);

<Input type="text" ref={inputRef} />
```

# ２．値の保持
useStateと違って、値を更新しても再レンダリングが起きない。そのため、前のpropsやstateを記憶するのに使える。

# useEffect
React Hooksの一つ。副作用を扱うためのもの。

# １．依存配列
第２引数に依存配列を指定する。この配列に含まれる値が変化したときのみ、useEffect内の関数が実行される。依存配列が空([])の場合、useEffect内の関数は初回レンダリング後に一度だけ実行される。
```
import React, { useEffect } from 'react';

const Example = () => {
  useEffect(() => {
    console.log('Component did mount');//この行は一度だけ実行される
  }, []); // 空の配列を指定

  return <div>Example Component</div>;
}

export default Example;
```
# ２．クリーンアップ関数
```
import React, { useEffect } from 'react';

const Example = () => {
  useEffect(() => {
    console.log('Component did mount');

    // クリーンアップ関数
    return () => {
      console.log('Component will unmount');
    };
  }, []); // 空の配列を指定

  return <div>Example Component</div>;
}

export default Example;
```

作成
```
npm create vite@latest プロジェクト名
```
- Reactを選択
- TypeScript + SWC を選択した方が高速にビルドしてくれる
```
cd プロジェクト名
```
```
npm install
```
```
npm run dev
```
```
 % npm i @chakra-ui/react @emotion/react @emotion/styled framer-motion
```
```
code .
```
ルートコンポーネントをChakra Providerでwrapする
```
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';
import { ChakraProvider } from '@chakra-ui/react';

ReactDOM.createRoot(document.getElementById('root') as HTMLElement).render(
  <React.StrictMode>
    <ChakraProvider>
      <App />
    </ChakraProvider>
  </React.StrictMode>
);
```

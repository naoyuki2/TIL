インストール
```
npm install react-router-dom
```
main.jsxにBrowserRouterでラップする
```
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App.jsx';
import { BrowserRouter } from 'react-router-dom';

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </React.StrictMode>
);
```
App.jsxファイルにRoutes,Routeをインポートし表示するルートで表示するコンポーネントを設定
```
import { Routes, Route } from 'react-router-dom';
import Home from './routes/home';

function App() {
  return (
    <div className="App">
      <h1>Hello React Router v6</h1>
      <Routes>
        <Route path="/" element={<Home />} />
      </Routes>
    </div>
  );
}

export default App;
```
Linkタグの設定、aタグの代わりとしてLinkタグが使用できる
```
import { Link } from '@chakra-ui/react'
import React from 'react'

const Home = () => {
  return (
    <>
      <h1>Reactアプリ100本ノック</h1>
      <ul>
        <li>
          <Link href="/001">001 HelloWorld</Link>
        </li>
      </ul>
    </>
  )
}

export default Home

```

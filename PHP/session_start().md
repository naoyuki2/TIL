セッションが開始されているのに再度session_startをするとエラーになるため下記のように記す
```
  if (session_status() == PHP_SESSION_NONE) {
  session_start();
}
```

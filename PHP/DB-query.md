# 接続
```
$pdo = new PDO($connect,USER,PASS);
```
# SELECT
```
$sql = $pdo->query('select * from products');
foreach($sql as $row){
  //省略
}
```
```
$stmt=$pdo->prepare('select * from cart where user_id = ?');
$stmt->execute([$_SESSION['id']]);
$cart = $stmt->fetch();
echo $cart['cart_id'];
```
# INSERT
```
$sql=$pdo->prepare('insert into cart values(null,?)');
$sql->execute([$_SESSION['id']]);
```
Insert後の最新のレコードのIDを取得  
直近のINSERT後にのみ使用できる。挿入した行のauto_incrementのIDを取得することができる。
```
$last_id = $pdo->lastInsertId();
```
# DELETE
```
$stmt = $pdo->prepare('DELETE FROM cartDetails');
$stmt->execute();
```

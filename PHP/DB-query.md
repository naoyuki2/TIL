# SELECT
```
$sql = $pdo->query('select * from products');
foreach($sql as $row){
  //省略
}
```
```
$sql=$pdo->prepare('select cart_id from cart where user_id = ?');
$sql->execute([$_SESSION['id']]);
$cart_id = $sql->fetchColumn();
```
# INSERT
```
$sql=$pdo->prepare('insert into cart values(null,?)');
$sql->execute([$_SESSION['id']]);
```

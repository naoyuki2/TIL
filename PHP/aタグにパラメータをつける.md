# aタグにパラメータをつける
リンク先の後ろに?をつけてパラメータ名＝値とする
```
echo '<a href="productDetail.php?product_id='.$row['product_id'].'">';
```
$_GET['パラメータ名']で受け取れる
```
<?php
  if(isset($_GET['product_id'])){
      $product_id = $_GET['product_id'];
      echo $product_id;
  } else {
      echo '製品IDが指定されていません。';
  }
?>
```

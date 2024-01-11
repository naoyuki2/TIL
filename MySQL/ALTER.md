# 追加
現在のテーブルにカラムを追加
```
ALTER TABLE user
ADD COLUMN admin_flg INT DEFAULT 0;
```
# 削除
現在のテーブルからdelete_flgカラムを削除  
```
ALTER TABLE user
DROP COLUMN delete_flg;
```
# 変更
```
ALTER TABLE recipe_ingredient_link
MODIFY quantity VARCHAR(100);
```

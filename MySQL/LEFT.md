postsテーブルのcontentカラムを先頭の20文字だけ表示
```
select id, left(content,20), posted_at from posts;
```

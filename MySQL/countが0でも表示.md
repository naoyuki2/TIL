left join でlikesの方が空になっていても表示できる
```
select posts.id as post_id, content, count(likes.post_id) as likes_count
from posts
left join likes on posts.id = likes.post_id
group by posts.id, content
order by count(likes.post_id) desc, posted_at desc
;
```

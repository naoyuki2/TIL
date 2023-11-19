それは可能ですが、一般的にはJOIN句を使った方が効率的で、SQLの意図が明確になります。JOINを使わない場合、クエリはすべてのレコードの組み合わせを生成し、その後WHERE句で絞り込みます。これは大量のデータを扱う場合、パフォーマンスに影響を及ぼす可能性があります。

しかし、JOINを使うと、必要なレコードの組み合わせだけが最初から生成されます。これにより、データベースエンジンは効率的に動作し、必要なデータだけを返すことができます。

したがって、users.id = posts.user_idのような条件を使ってテーブル間で関連付けを行う場合、以下のようにJOIN句を使うことをお勧めします。
```
SELECT ...
FROM users
JOIN posts ON users.id = posts.user_id
WHERE ...

```
３つ以上
```
SELECT ...
FROM users
JOIN posts ON users.id = posts.user_id
JOIN comments ON posts.id = comments.post_id
WHERE ...
```

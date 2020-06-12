# Simple DBAL

Database abstraction for personal projects.

Wraps around PDO.  No ORM or anything, just some handy methods.

Usage:

```
$db = new \Umonkey\Database([
    'name' => 'mysql:dbname=foobar',
    'user' => 'alice',
    'password' => 'secret',
]);

$rows = $db->fetch('SELECT * FROM rows');

$db->insert('rows', [
    'name' => 'foobar',
]);

$db->update('rows', [
    'name' => 'foobar',
], [
    'id' => 1,
]);

$users = $db->fetchkv('SELECT id, name FROM users');
```

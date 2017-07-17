# Phalcon - MS SQL Server (PDO) Adapter

- Phalcon 3.2.0 support

```php
$di->set('db', function() use ($config) {
	return new \Phalcon\Db\Adapter\Pdo\Sqlsrv(array(
		"host"         => $config->database->host,
		"username"     => $config->database->username,
		"password"     => $config->database->password,
		"dbname"       => $config->database->name
	));
});

```

- Note

In this branch(nolock), I make every select statement with no lock hint.


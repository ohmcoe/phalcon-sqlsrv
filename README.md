Phalcon - MS SQL Server (PDO) Adapter
===================

 - Phalcon 3.2 supported 

## Get started

Install

```bash

cd <git repo> # go to your git repo
git submodule add https://github.com/xxx/phalcon-sqlsrv.git <your library path>
```

Setting

```php

//1. load 
'Phalcon\Db'    => __DIR__ . '/../library/phalcon-sqlsrv/Phalcon/Db',

//2. new instance
$di->set('db', function() use ($config) {
    return new \Phalcon\Db\Adapter\Pdo\Sqlsrv([
        "host"         => $config->database->host,
        "username"     => $config->database->username,
        "password"     => $config->database->password,
        "dbname"       => $config->database->name,
        "pdoType"      => 'sqlsrv'  //If you didn't speicif, it will make sqlsrv as default.
    ]); 
});

```

> **Note:**

> - There is another branch - "nolock" which makes every select statement with no lock hint.

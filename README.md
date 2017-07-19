# larasimple

laravel框架核心精简版composer 搭建

compsoer直接拉取laravel核心MVC结构

```json
 "require": {
    "php": ">=5.6.4",
    "illuminate/routing": "^5.4",
    "illuminate/events": "^5.4",
    "illuminate/database": "^5.4",
    "illuminate/view": "^5.4"
  },
  "autoload": {
    "psr-4": {
      "App\\": "app/"
    }
  }
```

### 数据库配置
`larasimple/config/database.php`

```php
<?php
/**
 * Created by PhpStorm.
 * User: ADKi
 * Date: 2017/7/19 0019
 * Time: 10:28
 * @author DukeAnn
 */
return [
    'driver' => "mysql",
    'host' => "localhost",
    'database' => "laratest",
    'username' => "root",
    'password' => "root",
    'charset' => "utf8",
    'collation' => 'utf8_general_ci',
    'prefix' => ''
];
```

### 路由文件

`app/Http/routes.php`
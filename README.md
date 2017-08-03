# larasimple

## laravel框架核心精简版composer 搭建

- 根据书《Laravel框架关键技术》
- [一个使用 Composer 构建的极简 Laravel 核心功能框架 larasimple](https://laravel-china.org/articles/5357/a-minimalist-laravel-core-functionality-framework-built-using-composer-larasimple)

composer直接拉取laravel核心MVC结构

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

## 使用方法

创建一个名为laratest的数据库

执行以下sql创建测试数据库
```sql
/*
Navicat MySQL Data Transfer

Source Server         : localhost
Source Server Version : 50717
Source Host           : localhost:3306
Source Database       : laratest

Target Server Type    : MYSQL
Target Server Version : 50717
File Encoding         : 65001

Date: 2017-07-19 11:56:41
*/

SET FOREIGN_KEY_CHECKS=0;

-- ----------------------------
-- Table structure for students
-- ----------------------------
DROP TABLE IF EXISTS `students`;
CREATE TABLE `students` (
  `id` int(10) NOT NULL AUTO_INCREMENT,
  `name` varchar(255) NOT NULL,
  `age` int(10) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=latin1;

-- ----------------------------
-- Records of students
-- ----------------------------
INSERT INTO `students` VALUES ('1', 'wshuo', '21');

```


# yii2-advanced-improved-template-restful-api
A fully featured Advanced Improved Template with RESTful Api support.

Yii2-advanced-improved-template-restful-api is based on yii2-advanced-template created by [nenad-zivkovic](https://github.com/nenad-zivkovic/yii2-advanced-template).
The base template is upgraded with inbuilt REST Api support.

Installation
-------------------
1. Clone the repository ``` git clone https://github.com/choxx/yii2-advanced-improved-template-restful-api.git ```.
2. Now open terminal and navigate to **yii2-advanced-improved-template-restful-api/_protected**.
3. Now type the command ```php init``` and press **0** for development mode.
4. Press **yes** to continue initializing the template.
5. Now navigate to root directory of app via hitting ```cd ..```.
6. Run command ```sudo composer update``` to build/update the dependencies.
7. After completion, configure you database in **common/config/main-local.php**.
8. Now navigate to _protected ```cd _protected```.
9. Apply migrations by hitting ```yii migrate```.
10. Apply RBAC migration by hitting ```yii rbac/init```.
11. Now create table **country** with sample data
```
CREATE TABLE `country` (
  `code` CHAR(2) NOT NULL PRIMARY KEY,
  `name` CHAR(52) NOT NULL,
  `population` INT(11) NOT NULL DEFAULT '0'
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

INSERT INTO `Country` VALUES ('AU','Australia',18886000);
INSERT INTO `Country` VALUES ('BR','Brazil',170115000);
INSERT INTO `Country` VALUES ('CA','Canada',1147000);
INSERT INTO `Country` VALUES ('CN','China',1277558000);
INSERT INTO `Country` VALUES ('DE','Germany',82164700);
INSERT INTO `Country` VALUES ('FR','France',59225700);
INSERT INTO `Country` VALUES ('GB','United Kingdom',59623400);
INSERT INTO `Country` VALUES ('IN','India',1013662000);
INSERT INTO `Country` VALUES ('RU','Russia',146934000);
INSERT INTO `Country` VALUES ('US','United States',278357000);
```

Running the application
-------------------
>Navigate to the root directory of application **yii2-advanced-improved-template-restful-api/_protected** and create a localserver by hitting ```php -S localhost:7872``` and you are ready with your template.

1. Check for frontend **http://localhost:7872**.
2. Check for backend **http://localhost:7872/backend**.
3. Check for REST api 

GET
-------------------

1. **http://localhost:7872/api/v1/countries**
2. **http://localhost:7872/api/v1/countries/AU**

POST
-------------------
**http://localhost:7872/api/v1/countries**

>Parameters

code - SU

name - Sudan

population - 7872

PUT
-------------------
**http://localhost:7872/api/v1/countries/SU**

>Parameters

population - 10000

DELETE
-------------------
**http://localhost:7872/api/v1/countries/SU**

[![Yii2](https://img.shields.io/badge/Powered_by-Yii_Framework-green.svg?style=flat)](http://www.yiiframework.com/)

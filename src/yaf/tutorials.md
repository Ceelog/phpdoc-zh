范例
====

**示例 \#1 一个典型的应用目录结构**

    - index.php 
    - .htaccess 
    + conf
      |- application.ini //application config
    - application/
      - Bootstrap.php   
      + controllers
         - Index.php //default controller
      + views    
         |+ index   
            - index.phtml //view template for default action
      + modules 
      - library
      - models  
      - plugins 

**示例 \#2 入口文件**

顶层目录下的index.php是整个应用的唯一入口，应该把所有请求都重定向到这个文件（在Apache+php\_mod模式下可以使用.htaccess）。

``` php
<?php
define("APPLICATION_PATH",  dirname(__FILE__));

$app  = new Yaf_Application(APPLICATION_PATH . "/conf/application.ini");
$app->bootstrap() //call bootstrap methods defined in Bootstrap.php
 ->run();
?>
```

**示例 \#3 重写规则**

    #for apache (.htaccess)
    RewriteEngine On
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule .* index.php

    #for nginx
    server {
      listen ****;
      server_name  domain.com;
      root   document_root;
      index  index.php index.html index.htm;

      if (!-e $request_filename) {
        rewrite ^/(.*)  /index.php/$1 last;
      }
    }

    #for lighttpd
    $HTTP["host"] =~ "(www.)?domain.com$" {
      url.rewrite = (
         "^/(.+)/?$"  => "/index.php/$1",
      )
    }

**示例 \#4 应用配置文件**

``` ini
[yaf]
;APPLICATION_PATH is the constant defined in index.php
application.directory=APPLICATION_PATH "/application/" 

;product section inherit from yaf section
[product:yaf]
foo=bar
```

**示例 \#5 默认控制器**

``` php
<?php
class IndexController extends Yaf_Controller_Abstract {
   /* default action */
   public function indexAction() {
       $this->_view->word = "hello world";
       //or
       // $this->getView()->word = "hello world";
   }
}
?>
```

**示例 \#6 默认视图文件**

``` php
<html>
 <head>
   <title>Hello World</title>
 </head>
 <body>
   <?php echo $word;?>
 </body>
</html>
```

**示例 \#7 运行应用**

以上例程的输出类似于：

    <html>
     <head>
       <title>Hello World</title>
     </head>
     <body>
       hello world
     </body>
    </html>

> **Note**:
>
> 在yaf@github上有Yaf代码生成器，你也可以用它来生成上面的例子。

内置Web Server
--------------

PHP 5.4.0起， CLI SAPI 提供了一个内置的Web服务器。

这个内置的Web服务器主要用于本地开发使用，不可用于线上产品环境。

URI请求会被发送到PHP所在的的工作目录（Working
Directory）进行处理，除非你使用了-t参数来自定义不同的目录。

如果请求未指定执行哪个PHP文件，则默认执行目录内的index.php 或者
index.html。如果这两个文件都不存在，服务器会返回404错误。

当你在命令行启动这个Web
Server时，如果指定了一个PHP文件，则这个文件会作为一个“路由”脚本，意味着每次请求都会先执行这个脚本。如果这个脚本返回
**`false`**
，那么直接返回请求的文件（例如请求静态文件不作任何处理）。否则会把输出返回到浏览器。

**示例 \#1 启动Web服务器**

``` shell
$ cd ~/public_html
$ php -S localhost:8000
```

终端窗口会显示:

    PHP 5.4.0 Development Server started at Thu Jul 21 10:43:28 2011
    Listening on localhost:8000
    Document root is /home/me/public_html
    Press Ctrl-C to quit

接着访问http://localhost:8000/和http://localhost:8000/myscript.html，窗口会显示：

    PHP 5.4.0 Development Server started at Thu Jul 21 10:43:28 2011
    Listening on localhost:8000
    Document root is /home/me/public_html
    Press Ctrl-C to quit.
    [Thu Jul 21 10:48:48 2011] ::1:39144 GET /favicon.ico - Request read
    [Thu Jul 21 10:48:50 2011] ::1:39146 GET / - Request read
    [Thu Jul 21 10:48:50 2011] ::1:39147 GET /favicon.ico - Request read
    [Thu Jul 21 10:48:52 2011] ::1:39148 GET /myscript.html - Request read
    [Thu Jul 21 10:48:52 2011] ::1:39149 GET /favicon.ico - Request read

**示例 \#2 启动时指定根目录**

``` shell
$ cd ~/public_html
$ php -S localhost:8000 -t foo/
```

终端窗口显示：

    PHP 5.4.0 Development Server started at Thu Jul 21 10:50:26 2011
    Listening on localhost:8000
    Document root is /home/me/public_html/foo
    Press Ctrl-C to quit

**示例 \#3 使用路由（Router）脚本**

请求图片直接显示图片，请求HTML则显示“Welcome to PHP”

``` php
<?php
// router.php
if (preg_match('/\.(?:png|jpg|jpeg|gif)$/', $_SERVER["REQUEST_URI"]))
    return false;    // 直接返回请求的文件
else { 
    echo "<p>Welcome to PHP</p>";
}
?>
```

``` shell
$ php -S localhost:8000 router.php
```

执行之后终端显示：

    PHP 5.4.0 Development Server started at Thu Jul 21 10:53:19 2011
    Listening on localhost:8000
    Document root is /home/me/public_html
    Press Ctrl-C to quit.
    [Thu Jul 21 10:53:45 2011] ::1:55801 GET /mylogo.jpg - Request read
    [Thu Jul 21 10:53:52 2011] ::1:55803 GET /abc.html - Request read
    [Thu Jul 21 10:53:52 2011] ::1:55804 GET /favicon.ico - Request read

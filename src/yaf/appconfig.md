应用配置
========

你需要传递一个config数组或ini配置文件（参见 <span
class="classname">Yaf\_Config\_Ini</span>） 给 <span
class="methodname">Yaf\_Application::\_\_construct</span>.

Yaf的配置文件会和用户的配置文件合并。区别在于，Yaf的配置文件是以"yaf."或"application."开头，如果两项都存在，则"application."生效。

**示例 \#1 config为数组的例子**

``` php
<?php
    $configs = array(
            "application" => array(
                "directory" => dirname(__FILE__),
                "dispatcher" => array(
                      "catchException" => 0,
                    ),
                "view" => array(
                       "ext" => "phtml",
                    ),
                ),
           );
    $app = new Yaf_Application($config);
?>
```

**示例 \#2 config为ini文件的例子**

``` ini
[yaf]
yaf.directory = APPLICATION_PATH "/appliation"
yaf.dispatcher.catchException = 0

[product : yaf]
; user configuration list here
```

| 名字                                     | 默认                                                   | 更新日志 |
|------------------------------------------|--------------------------------------------------------|----------|
| application.directory                    |                                                        |          |
| application.ext                          | "php"                                                  |          |
| application.view.ext                     | "phtml"                                                |          |
| application.modules                      | "index"                                                |          |
| application.library                      | application.directory . "/library"                     |          |
| application.library.directory            | application.directory . "/library"                     |          |
| application.library.namespace            | ""                                                     |          |
| application.bootstrap                    | application.directory . "/Bootstrap" . application.ext |          |
| application.baseUri                      | ""                                                     |          |
| application.dispatcher.defaultRoute      |                                                        |          |
| application.dispatcher.throwException    | 1                                                      |          |
| application.dispatcher.catchException    | 0                                                      |          |
| application.dispatcher.defaultModule     | "index"                                                |          |
| application.dispatcher.defaultController | "index"                                                |          |
| application.dispatcher.defaultAction     | "index"                                                |          |
| application.system                       |                                                        |          |

这是配置指令的简短说明。

`application.directory` <span class="type">string</span>  
应用程序的目录，包含"controllers", "views", "models",
"plugins"等子目录。

> **Note**:
>
> 这是唯一一个没有默认值的配置项，你需要手动指定它。

`application.ext` <span class="type">string</span>  
PHP脚本的扩展名，类的自动加载需要用到它( <span
class="classname">Yaf\_Loader</span>)。

`application.view.ext` <span class="type">string</span>  
视图模板扩展名。

`application.modules` <span class="type">string</span>  
注册的模块列表，以逗号分隔，用于路由处理，特别是当PATH\_INFO超过三段的时候，

Yaf需要用它来判断第一段是否是一个模块。

`application.library` <span class="type">string</span>  
本地类库的目录，参见<span class="classname">Yaf\_Loader</span> 和
<a href="/yaf/setup.html#" class="link">yaf.library</a>。

> **Note**:
>
> Yaf2.1.6以后，该配置项也可以是一个数组，当它是数组的时候，类库的路径将尝试使用<a href="/yaf/appconfig.html#" class="link">application.library.directory</a>的值。

`application.library.directory` <span class="type">string</span>  
Alias of
<a href="/yaf/appconfig.html#" class="link">application.library</a>.
Introduced in Yaf 2.1.6

`application.library.namespace` <span class="type">string</span>  
逗号分隔的本地类库命名空间前缀。

Yaf2.1.6以后加入

`application.bootstrap` <span class="type">string</span>  
Bootstrap类脚本文件的绝对路径。

`application.baseUri` <span class="type">string</span>  
路由处理中需要忽略的路径前缀。举个例子，请求"/prefix/controller/action"时。如果你将application.baseUri设置为"/prefix"，那么只有"/controller/action"会被当做路由路径。

通常不需要设置此值。

`application.dispatcher.throwException` <span class="type">bool</span>  
开启此项，Yaf会在发生错误的地方抛出异常。参见 <span
class="methodname">Yaf\_Dispatcher::throwException</span>。

`application.dispatcher.catchException` <span class="type">bool</span>  
开启此项，如果有未捕获的异常，Yaf将会把它定向到Error controller, Error
Action。参见 <span
class="methodname">Yaf\_Dispatcher::catchException</span>。

`application.dispatcher.defaultRoute` <span class="type">string</span>  
默认路由，如果未指定，静态路由会被当做是默认路由，参见： <span
class="methodname">Yaf\_Router::addRoute</span>。

`application.dispatcher.defaultModule` <span class="type">string</span>  
默认模块名，参见 <span
class="methodname">Yaf\_Dispatcher::setDefaultModule</span>。

`application.dispatcher.defaultController` <span class="type">string</span>  
默认控制器名，参见 <span
class="methodname">Yaf\_Dispatcher::setDefaultController</span>。

`application.dispatcher.defaultAction` <span class="type">string</span>  
默认动作名，参见 <span
class="methodname">Yaf\_Dispatcher::setDefaultAction</span>。

`application.system` <span class="type">string</span>  
在application.ini中设置Yaf运行时配置，如：
<a href="/yaf/setup.html#" class="link">application.system.lowcase_path</a>

> **Note**:
>
> 仅有PHP\_INI\_ALL配置项能这样设置

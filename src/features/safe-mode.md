安全模式
========

**目录**

-   [保安措施和安全模式](/ini/sect/safe-mode.html)
-   [被安全模式限制或屏蔽的函数](/features/safe-mode/functions.html)

PHP
的安全模式是为了试图解决共享服务器（shared-server）安全问题而设立的。在结构上，试图在
PHP 层上解决这个问题是不合理的，但修改 web
服务器层和操作系统层显得非常不现实。因此许多人，特别是
ISP，目前使用安全模式。

**Warning**

本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

| 版本  | 说明                                                                                 |
|-------|--------------------------------------------------------------------------------------|
| 5.4.0 | Removed from PHP, and generates a fatal **`E_CORE_ERROR`** level error when enabled. |
| 5.3.0 | Deprecated, and **`E_DEPRECATED`** errors were added.                                |

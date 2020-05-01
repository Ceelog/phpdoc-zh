安装／配置
==========

**目录**

-   [需求](/pht/setup.html#需求)
-   [安装](/pht/setup.html#安装)
-   [运行时配置](/pht/setup.html#运行时配置)

需求
----

pht requires a ZTS (Zend Thread Safety) version of PHP. Currently, only
PHP 7.2 is supported. Support for PHP 7.3 (which will be released at the
end of 2018) will be coming soon. PHP 7.0 and 7.1 are unsafe to support,
due to race conditions in ZTS mode.

pht should be compatible for any OS with the pthread library (or
pthread-win32 library, which is for Windows).

安装
----

pht releases are hosted (along with its source code) on the
<a href="https://github.com/tpunt/pht" class="link external">» pht GitHub repository</a>.
Unix developers will need to build from source
(<a href="https://github.com/tpunt/pht#installation" class="link external">» instructions here</a>).
Windows developers can download the appropriate .dll file from the
<a href="https://github.com/tpunt/pht/releases" class="link external">» repository's releases page</a>.
They will need to ensure that the provided pthreadVC2.dll file (which is
distributed alongside the extension's .dll file) is made available in
their `PATH` environment variable.

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

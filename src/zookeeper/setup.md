安装／配置
==========

**目录**

-   [需求](/zookeeper/setup.html#需求)
-   [安装](/zookeeper/setup.html#安装)
-   [运行时配置](/zookeeper/setup.html#运行时配置)
-   [资源类型](/zookeeper/setup.html#资源类型)

需求
----

This extension requires
<a href="https://zookeeper.apache.org/" class="link external">» ZooKeeper</a>
C Binding (version 3.4.1 or greater). For more information, see
<a href="https://zookeeper.apache.org/doc/trunk/zookeeperProgrammers.html#C+Binding" class="link external">» ZooKeeper Programmer's Guide</a>.

This extension requires PHP version 5.2.0 or higher. Since 0.6.0, it
requires PHP version 7.0.0 or higher.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/zookeeper" class="link external">» https://pecl.php.net/package/zookeeper</a>.

To enable zookeeper support, configure with
**--with-libzookeeper-dir=DIR**. DIR is the install prefix of ZooKeeper
C Binding, which must contain the `include/zookeeper/zookeeper.h`

PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.legacy.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                       | 默认   | 可修改范围       | Changelog |
|----------------------------------------------------------------------------|--------|------------------|-----------|
| <a href="/zookeeper/setup.html#" class="link">zookeeper.recv_timeout</a>   | 10000  | PHP\_INI\_ALL    |           |
| <a href="/zookeeper/setup.html#" class="link">zookeeper.session_lock</a>   | 1      | PHP\_INI\_SYSTEM |           |
| <a href="/zookeeper/setup.html#" class="link">zookeeper.sess_lock_wait</a> | 150000 | PHP\_INI\_ALL    |           |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`zookeeper.recv_timeout` <span class="type">int</span>  
Default the timeout for any ZooKeeper session.

`zookeeper.session_lock` <span class="type">int</span>  
Enable PHP session locking.

`zookeeper.sess_lock_wait` <span class="type">int</span>  
PHP Session spin lock retry wait time in microseconds. Be carefull when
setting this value. Valid values are integers, where 0 is interpreted as
the default value. Negative values result in a reduces locking to a try
lock.

资源类型
--------

此扩展没有定义资源类型。

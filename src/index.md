PHP 手册
========

**目录**

-   [版权信息](/copyright.html)
-   [PHP 手册](/manual.html)
    -   [序言](/preface.html)
-   [入门指引](/getting-started.html)
    -   [简介](/introduction.html)
    -   [简明教程](/tutorial.html)
-   [安装与配置](/install.html)
    -   [安装前需要考虑的事项](/install/general.html)
    -   [Unix 系统下的安装](/install/unix.html)
    -   [Mac OS X 系统下的安装](/install/macosx.html)
    -   [Windows 系统下的安装](/install/windows.html)
    -   [云计算平台上的安装](/install/cloud.html)
    -   [FastCGI 进程管理器（FPM）](/install/fpm.html)
    -   [PECL 扩展库安装](/install/pecl.html)
    -   [还有问题？](/install/problems.html)
    -   [运行时配置](/configuration.html)
-   [语言参考](/langref.html)
    -   [基本语法](/language/basic-syntax.html)
    -   [类型](/language/types.html)
    -   [变量](/language/variables.html)
    -   [常量](/language/constants.html)
    -   [表达式](/language/expressions.html)
    -   [运算符](/language/operators.html)
    -   [流程控制](/language/control-structures.html)
    -   [函数](/language/functions.html)
    -   [类与对象](/language/oop5.html)
    -   [命名空间](/language/namespaces.html)
    -   [Errors](/language/errors.html)
    -   [异常处理](/language/exceptions.html)
    -   [生成器](/language/generators.html)
    -   [Attributes](/language/attributes.html)
    -   [引用的解释](/language/references.html)
    -   [预定义变量](/reserved/variables.html)
    -   [预定义异常](/reserved/exceptions.html)
    -   [预定义接口](/reserved/interfaces.html)
    -   [上下文（Context）选项和参数](/context.html)
    -   [支持的协议和封装协议](/wrappers.html)
-   [安全](/security.html)
    -   [简介](/security/intro.html)
    -   [总则](/security/general.html)
    -   [以 CGI 模式安装时](/security/cgi-bin.html)
    -   [以 Apache 模块安装时](/security/apache.html)
    -   [会话（Session）安全](/security/sessions.html)
    -   [文件系统安全](/security/filesystem.html)
    -   [数据库安全](/security/database.html)
    -   [错误报告](/security/errors.html)
    -   [使用 Register Globals](/security/globals.html)
    -   [用户提交的数据](/security/variables.html)
    -   [魔术引号](/security/magicquotes.html)
    -   [隐藏 PHP](/security/hiding.html)
    -   [保持更新](/security/current.html)
-   [特点](/features.html)
    -   [用 PHP 进行 HTTP 认证](/features/http-auth.html)
    -   [Cookie](/features/cookies.html)
    -   [会话](/features/sessions.html)
    -   [处理 XForms](/features/xforms.html)
    -   [文件上传处理](/features/file-upload.html)
    -   [使用远程文件](/features/remote-files.html)
    -   [连接处理](/features/connection-handling.html)
    -   [数据库持久连接](/features/persistent-connections.html)
    -   [PHP 的命令行模式](/features/commandline.html)
    -   [垃圾回收机制](/features/gc.html)
    -   [DTrace 动态跟踪](/features/dtrace.html)
-   [函数参考](/funcref.html)
    -   [影响 PHP 行为的扩展](/refs/basic/php.html)
    -   [音频格式操作](/refs/utilspec/audio.html)
    -   [身份认证服务](/refs/remote/auth.html)
    -   [针对命令行的扩展](/refs/utilspec/cmdline.html)
    -   [压缩与归档扩展](/refs/compression.html)
    -   [加密扩展](/refs/crypto.html)
    -   [数据库扩展](/refs/database.html)
    -   [日期与时间相关扩展](/refs/calendar.html)
    -   [文件系统相关扩展](/refs/fileprocess/file.html)
    -   [国际化与字符编码支持](/refs/international.html)
    -   [图像生成和处理](/refs/utilspec/image.html)
    -   [邮件相关扩展](/refs/remote/mail.html)
    -   [数学扩展](/refs/math.html)
    -   [非文本内容的 MIME 输出](/refs/utilspec/nontext.html)
    -   [进程控制扩展](/refs/fileprocess/process.html)
    -   [其它基本扩展](/refs/basic/other.html)
    -   [其它服务](/refs/remote/other.html)
    -   [搜索引擎扩展](/refs/search.html)
    -   [针对服务器的扩展](/refs/utilspec/server.html)
    -   [Session 扩展](/refs/basic/session.html)
    -   [文本处理](/refs/basic/text.html)
    -   [变量与类型相关扩展](/refs/basic/vartype.html)
    -   [Web 服务](/refs/webservice.html)
    -   [Windows 专用扩展](/refs/utilspec/windows.html)
    -   [XML 操作](/refs/xml.html)
    -   [图形用户界面(GUI) 扩展](/refs/ui.html)
-   [PHP 核心：骇客指南](/internals2.html)
    -   [序言](/internals2/preface.html)
    -   [内存管理](/internals2/memory.html)
    -   [变量的使用](/internals2/variables.html)
    -   [函数的编写](/internals2/funcs.html)
    -   [类和对象的使用](/internals2/objects.html)
    -   [资源的使用](/internals2/resources.html)
    -   [INI 设置的使用](/internals2/ini.html)
    -   [流的使用](/internals2/streams.html)
    -   ["counter" 扩展 - 一个连续的实例](/internals2/counter.html)
    -   [PHP 5 构建系统](/internals2/buildsys.html)
    -   [扩展的结构](/internals2/structure.html)
    -   [PDO 驱动](/internals2/pdo.html)
    -   [扩展相关 FAQ](/internals2/faq.html)
    -   [Zend Engine 2 API 参考](/internals2/apiref.html)
    -   [Zend Engine 2 操作码列表](/internals2/opcodes.html)
    -   [Zend Engine 1](/internals2/ze1.html)
-   [FAQ](/faq.html) — FAQ：常见问题
    -   [一般信息](/faq/general.html) — 一般信息
    -   [邮件列表](/faq/mailinglist.html) — 邮件列表
    -   [获取 PHP](/faq/obtaining.html) — 获取 PHP
    -   [数据库问题](/faq/databases.html) — 数据库问题
    -   [安装](/faq/installation.html) — 安装常见问题
    -   [编译问题](/faq/build.html) — 编译问题
    -   [使用 PHP](/faq/using.html) — 使用 PHP
    -   [密码散列](/faq/passwords.html) — 密码散列安全
    -   [PHP 和 HTML](/faq/html.html) — PHP 和 HTML
    -   [PHP 和 COM](/faq/com.html) — PHP 和 COM
    -   [其他问题](/faq/misc.html) — 其他问题
-   [附录](/appendices.html)
    -   [PHP 及其相关工程的历史](/history.html)
    -   [从 PHP 7.4.x 移植到 PHP 8.0.x](/migration80.html)
    -   [从 PHP 7.3.x 移植到 PHP 7.4.x](/migration74.html)
    -   [从 PHP 7.2.x 移植到 PHP 7.3.x](/migration73.html)
    -   [从 PHP 7.1.x 移植到 PHP 7.2.x](/migration72.html)
    -   [从 PHP 7.0.x 移植到 PHP 7.1.x](/migration71.html)
    -   [从 PHP 5.6.x 移植到 PHP 7.0.x](/migration70.html)
    -   [从 PHP 5.5.x 移植到 PHP 5.6.x](/migration56.html)
    -   [从 PHP 5.4.x 迁移到 PHP 5.5.x](/migration55.html)
    -   [从 PHP 5.3.X 迁移到 PHP 5.4.X](/migration54.html)
    -   [从 PHP 5.2.x 移植到 PHP 5.3.x](/migration53.html)
    -   [Migrating from PHP 5.1.x to PHP 5.2.x](/migration52.html)
    -   [Migrating from PHP 5.0.x to PHP 5.1.x](/migration51.html)
    -   [从 PHP 4 移植到 PHP 5](/migration5.html)
    -   [PHP 的调试](/debugger.html)
    -   [配置选项](/configure.html)
    -   [php.ini 配置](/ini.html)
    -   [扩展库列表／归类](/extensions.html)
    -   [函数别名列表](/aliases.html)
    -   [保留字列表](/reserved.html)
    -   [资源类型列表](/resource.html)
    -   [可用过滤器列表](/filters.html)
    -   [所支持的套接字传输器（Socket
        Transports）列表](/transports.html)
    -   [PHP 类型比较表](/types/comparisons.html)
    -   [解析器代号列表](/tokens.html)
    -   [用户空间命名指南](/userlandnaming.html)
    -   [关于本手册](/about.html)
    -   [Creative Commons Attribution 3.0](/cc/license.html)
    -   [索引](/indexes.html)
    -   [更新日志](/doc/changelog.html)

**by**:  
<span class="personname fn"> <span
class="firstname given-name">Mehdi</span> <span
class="surname family-name">Achour</span> </span>

<span class="personname fn"> <span
class="firstname given-name">Friedhelm</span> <span
class="surname family-name">Betz</span> </span>

<span class="personname fn"> <span
class="firstname given-name">Antony</span> <span
class="surname family-name">Dovgal</span> </span>

<span class="personname fn"> <span
class="firstname given-name">Nuno</span> <span
class="surname family-name">Lopes</span> </span>

<span class="personname fn"> <span
class="firstname given-name">Hannes</span> <span
class="surname family-name">Magnusson</span> </span>

<span class="personname fn"> <span
class="firstname given-name">Georg</span> <span
class="surname family-name">Richter</span> </span>

<span class="personname fn"> <span
class="firstname given-name">Damien</span> <span
class="surname family-name">Seguy</span> </span>

<span class="personname fn"> <span
class="firstname given-name">Jakub</span> <span
class="surname family-name">Vrana</span> </span>

<span class="personname fn"> <span class="othername">
<a href="/preface.html#contributors" class="link">其他贡献者</a> </span>
</span>

2021-03-22

**Edited By**: <span class="personname fn"> <span
class="firstname given-name">Peter</span> <span
class="surname family-name">Cowburn</span> </span>

<span class="personname fn">中文翻译人员：</span>

<span class="personname fn">戴劼</span>

<span class="personname fn">乔楚</span>

<span class="personname fn">袁玉强</span>

<span class="personname fn">王远之</span>

<span class="personname fn">段小强</span>

<span class="personname fn">陈伯乐</span>

<span class="personname fn">周梦康</span>

<span class="personname fn">肖理达</span>

<span class="personname fn">肖盛文</span>

<span class="personname fn">褚兆玮</span>

© <span class="year">1997-2021</span> <span class="holder">PHP
文档组</span>

数据库安全
==========

**目录**

-   [设计数据库](/security/database/design.html)
-   [连接数据库](/security/database/connection.html)
-   [加密存储模型](/security/database/storage.html)
-   [SQL 注入](/security/database/sql-injection.html)

今时今日，数据库系统已经成为各个动态网站上 web
应用程序的重要组成部分。由于非常敏感和机密的数据有可能保存在数据库中，所以对数据库实施保护就显得尤为重要了。

要从数据库中提取或者存入数据，就必须经过连接数据库、发送一条合法查询、获取结果、关闭连接等步骤。目前，能完成这一系列动作的最常用的查询语言是结构化查询语言
Structured Query Language
(SQL)。可以看看攻击者是如何<a href="/security/database/sql-injection.html" class="link">篡改 SQL 查询语句的</a>。

PHP 本身并不能保护数据库的安全。下面的章节只是讲述怎样用 PHP
脚本对数据库进行基本的访问和操作。

记住一条简单的原则：深入防御。保护数据库的措施越多，攻击者就越难获得和使用数据库内的信息。正确地设计和应用数据库可以减少被攻击的担忧。

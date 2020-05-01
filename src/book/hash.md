哈希信息摘要框架
================

**目录**

-   [简介](/intro/hash.html)
-   [安装／配置](/hash/setup.html)
    -   [需求](/hash/setup.html#需求)
    -   [安装](/hash/setup.html#安装)
    -   [运行时配置](/hash/setup.html#运行时配置)
    -   [资源类型](/hash/setup.html#资源类型)
-   [预定义常量](/hash/constants.html)
-   [Hash 函数](/ref/hash.html)
    -   [hash\_algos](/ref/hash.html#hash_algos) —
        返回已注册的哈希算法列表
    -   [hash\_copy](/ref/hash.html#hash_copy) — 拷贝哈希运算上下文
    -   [hash\_equals](/ref/hash.html#hash_equals) —
        可防止时序攻击的字符串比较
    -   [hash\_file](/ref/hash.html#hash_file) —
        使用给定文件的内容生成哈希值
    -   [hash\_final](/ref/hash.html#hash_final) —
        结束增量哈希，并且返回摘要结果
    -   [hash\_hkdf](/ref/hash.html#hash_hkdf) — Generate a HKDF key
        derivation of a supplied key input
    -   [hash\_hmac\_algos](/ref/hash.html#hash_hmac_algos) — Return a
        list of registered hashing algorithms suitable for hash\_hmac
    -   [hash\_hmac\_file](/ref/hash.html#hash_hmac_file) — 使用 HMAC
        方法和给定文件的内容生成带密钥的哈希值
    -   [hash\_hmac](/ref/hash.html#hash_hmac) — 使用 HMAC
        方法生成带有密钥的哈希值
    -   [hash\_init](/ref/hash.html#hash_init) —
        初始化增量哈希运算上下文
    -   [hash\_pbkdf2](/ref/hash.html#hash_pbkdf2) — 生成所提供密码的
        PBKDF2 密钥导出
    -   [hash\_update\_file](/ref/hash.html#hash_update_file) —
        从文件向活跃的哈希运算上下文中填充数据
    -   [hash\_update\_stream](/ref/hash.html#hash_update_stream) —
        从打开的流向活跃的哈希运算上下文中填充数据
    -   [hash\_update](/ref/hash.html#hash_update) —
        向活跃的哈希运算上下文中填充数据
    -   [hash](/ref/hash.html#hash) — 生成哈希值 （消息摘要）

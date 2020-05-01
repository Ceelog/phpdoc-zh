Mcrypt
======

**目录**

-   [](/intro/mcrypt.html)
-   [安装／配置](/mcrypt/setup.html)
    -   [需求](/mcrypt/setup.html#需求)
    -   [安装](/mcrypt/setup.html#安装)
    -   [运行时配置](/mcrypt/setup.html#运行时配置)
    -   [资源类型](/mcrypt/setup.html#资源类型)
-   [预定义常量](/mcrypt/constants.html)
-   [Mcrypt 密码](/mcrypt/ciphers.html)
-   [范例](/mcrypt/examples.html)
-   [Mcrypt 函数](/ref/mcrypt.html)
    -   [mcrypt\_cbc](/ref/mcrypt.html#mcrypt_cbc) — 以 CBC
        模式加解密数据
    -   [mcrypt\_cfb](/ref/mcrypt.html#mcrypt_cfb) — 以 CFB
        模式加解密数据
    -   [mcrypt\_create\_iv](/ref/mcrypt.html#mcrypt_create_iv) —
        从随机源创建初始向量
    -   [mcrypt\_decrypt](/ref/mcrypt.html#mcrypt_decrypt) —
        使用给定参数解密密文
    -   [mcrypt\_ecb](/ref/mcrypt.html#mcrypt_ecb) — 已废弃：使用 ECB
        模式加解密数据
    -   [mcrypt\_enc\_get\_algorithms\_name](/ref/mcrypt.html#mcrypt_enc_get_algorithms_name)
        — 返回打开的算法名称
    -   [mcrypt\_enc\_get\_block\_size](/ref/mcrypt.html#mcrypt_enc_get_block_size)
        — 返回打开的算法的分组大小
    -   [mcrypt\_enc\_get\_iv\_size](/ref/mcrypt.html#mcrypt_enc_get_iv_size)
        — 返回打开的算法的初始向量大小
    -   [mcrypt\_enc\_get\_key\_size](/ref/mcrypt.html#mcrypt_enc_get_key_size)
        — 返回打开的模式所能支持的最长密钥
    -   [mcrypt\_enc\_get\_modes\_name](/ref/mcrypt.html#mcrypt_enc_get_modes_name)
        — 返回打开的模式的名称
    -   [mcrypt\_enc\_get\_supported\_key\_sizes](/ref/mcrypt.html#mcrypt_enc_get_supported_key_sizes)
        — 以数组方式返回打开的算法所支持的密钥长度
    -   [mcrypt\_enc\_is\_block\_algorithm\_mode](/ref/mcrypt.html#mcrypt_enc_is_block_algorithm_mode)
        — 检测打开的模式是否支持分组加密
    -   [mcrypt\_enc\_is\_block\_algorithm](/ref/mcrypt.html#mcrypt_enc_is_block_algorithm)
        — 检测打开模式的算法是否为分组算法
    -   [mcrypt\_enc\_is\_block\_mode](/ref/mcrypt.html#mcrypt_enc_is_block_mode)
        — 检测打开的模式是否以分组方式输出
    -   [mcrypt\_enc\_self\_test](/ref/mcrypt.html#mcrypt_enc_self_test)
        — 在打开的模块上进行自检
    -   [mcrypt\_encrypt](/ref/mcrypt.html#mcrypt_encrypt) —
        使用给定参数加密明文
    -   [mcrypt\_generic\_deinit](/ref/mcrypt.html#mcrypt_generic_deinit)
        — 对加密模块进行清理工作
    -   [mcrypt\_generic\_end](/ref/mcrypt.html#mcrypt_generic_end) —
        终止加密
    -   [mcrypt\_generic\_init](/ref/mcrypt.html#mcrypt_generic_init) —
        初始化加密所需的缓冲区
    -   [mcrypt\_generic](/ref/mcrypt.html#mcrypt_generic) — 加密数据
    -   [mcrypt\_get\_block\_size](/ref/mcrypt.html#mcrypt_get_block_size)
        — 获得加密算法的分组大小
    -   [mcrypt\_get\_cipher\_name](/ref/mcrypt.html#mcrypt_get_cipher_name)
        — 获取加密算法名称
    -   [mcrypt\_get\_iv\_size](/ref/mcrypt.html#mcrypt_get_iv_size) —
        返回指定算法/模式组合的初始向量大小
    -   [mcrypt\_get\_key\_size](/ref/mcrypt.html#mcrypt_get_key_size) —
        获取指定加密算法的密钥大小
    -   [mcrypt\_list\_algorithms](/ref/mcrypt.html#mcrypt_list_algorithms)
        — 获取支持的加密算法
    -   [mcrypt\_list\_modes](/ref/mcrypt.html#mcrypt_list_modes) —
        获取所支持的模式
    -   [mcrypt\_module\_close](/ref/mcrypt.html#mcrypt_module_close) —
        关闭加密模块
    -   [mcrypt\_module\_get\_algo\_block\_size](/ref/mcrypt.html#mcrypt_module_get_algo_block_size)
        — 返回指定算法的分组大小
    -   [mcrypt\_module\_get\_algo\_key\_size](/ref/mcrypt.html#mcrypt_module_get_algo_key_size)
        — 获取打开模式所支持的最大密钥大小
    -   [mcrypt\_module\_get\_supported\_key\_sizes](/ref/mcrypt.html#mcrypt_module_get_supported_key_sizes)
        — 以数组形式返回打开的算法所支持的密钥大小
    -   [mcrypt\_module\_is\_block\_algorithm\_mode](/ref/mcrypt.html#mcrypt_module_is_block_algorithm_mode)
        — 返回指定模块是否是分组加密模式
    -   [mcrypt\_module\_is\_block\_algorithm](/ref/mcrypt.html#mcrypt_module_is_block_algorithm)
        — 检测指定算法是否为分组加密算法
    -   [mcrypt\_module\_is\_block\_mode](/ref/mcrypt.html#mcrypt_module_is_block_mode)
        — 检测指定模式是否以分组方式输出
    -   [mcrypt\_module\_open](/ref/mcrypt.html#mcrypt_module_open) —
        打开算法和模式对应的模块
    -   [mcrypt\_module\_self\_test](/ref/mcrypt.html#mcrypt_module_self_test)
        — 在指定模块上执行自检
    -   [mcrypt\_ofb](/ref/mcrypt.html#mcrypt_ofb) — 使用 OFB
        模式加密/解密数据
    -   [mdecrypt\_generic](/ref/mcrypt.html#mdecrypt_generic) —
        解密数据

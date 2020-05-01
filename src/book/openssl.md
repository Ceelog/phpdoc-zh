OpenSSL
=======

**目录**

-   [简介](/intro/openssl.html)
-   [安装／配置](/openssl/setup.html)
    -   [需求](/openssl/setup.html#需求)
    -   [安装](/openssl/setup.html#安装)
    -   [运行时配置](/openssl/setup.html#运行时配置)
    -   [资源类型](/openssl/setup.html#资源类型)
-   [预定义常量](/openssl/constants.html)
    -   [目的检查标志](/openssl/constants.html#目的检查标志)
    -   [非对称加密的填充标志](/openssl/constants.html#非对称加密的填充标志)
    -   [密钥类型](/openssl/constants.html#密钥类型)
    -   [PKCS7 标志/常量](/openssl/constants.html#PKCS7%20标志/常量)
    -   [Signature
        Algorithms](/openssl/constants.html#Signature%20Algorithms)
    -   [Ciphers](/openssl/constants.html#Ciphers)
    -   [Version constants](/openssl/constants.html#Version%20constants)
    -   [Server Name Indication
        constants](/openssl/constants.html#Server%20Name%20Indication%20constants)
-   [密钥/证书参数](/openssl/certparams.html)
-   [证书验证](/openssl/cert/verification.html)
-   [OpenSSL 函数](/ref/openssl.html)
    -   [openssl\_cipher\_iv\_length](/ref/openssl.html#openssl_cipher_iv_length)
        — 获取密码iv长度
    -   [openssl\_csr\_export\_to\_file](/ref/openssl.html#openssl_csr_export_to_file)
        — 将CSR导出到文件
    -   [openssl\_csr\_export](/ref/openssl.html#openssl_csr_export) —
        将CSR作为字符串导出
    -   [openssl\_csr\_get\_public\_key](/ref/openssl.html#openssl_csr_get_public_key)
        — 返回CSR的公钥
    -   [openssl\_csr\_get\_subject](/ref/openssl.html#openssl_csr_get_subject)
        — 返回CSR的主题
    -   [openssl\_csr\_new](/ref/openssl.html#openssl_csr_new) —
        生成一个 CSR
    -   [openssl\_csr\_sign](/ref/openssl.html#openssl_csr_sign) —
        用另一个证书签署 CSR (或者本身) 并且生成一个证书
    -   [openssl\_decrypt](/ref/openssl.html#openssl_decrypt) — 解密数据
    -   [openssl\_dh\_compute\_key](/ref/openssl.html#openssl_dh_compute_key)
        — 计算远程DH密钥(公钥)和本地DH密钥的共享密钥
    -   [openssl\_digest](/ref/openssl.html#openssl_digest) — 计算摘要
    -   [openssl\_encrypt](/ref/openssl.html#openssl_encrypt) — 加密数据
    -   [openssl\_error\_string](/ref/openssl.html#openssl_error_string)
        — 返回 openSSL 错误消息
    -   [openssl\_free\_key](/ref/openssl.html#openssl_free_key) —
        释放密钥资源
    -   [openssl\_get\_cert\_locations](/ref/openssl.html#openssl_get_cert_locations)
        — 检索可用的证书位置
    -   [openssl\_get\_cipher\_methods](/ref/openssl.html#openssl_get_cipher_methods)
        — 获取可用的加密算法
    -   [openssl\_get\_curve\_names](/ref/openssl.html#openssl_get_curve_names)
        — 获得ECC的可用曲线名称列表
    -   [openssl\_get\_md\_methods](/ref/openssl.html#openssl_get_md_methods)
        — 获取可用的摘要算法
    -   [openssl\_get\_privatekey](/ref/openssl.html#openssl_get_privatekey)
        — 别名 openssl\_pkey\_get\_private
    -   [openssl\_get\_publickey](/ref/openssl.html#openssl_get_publickey)
        — 别名 openssl\_pkey\_get\_public
    -   [openssl\_open](/ref/openssl.html#openssl_open) — 打开密封的数据
    -   [openssl\_pbkdf2](/ref/openssl.html#openssl_pbkdf2) — 生成一个
        PKCS5 v2 PBKDF2 字符串
    -   [openssl\_pkcs12\_export\_to\_file](/ref/openssl.html#openssl_pkcs12_export_to_file)
        — 输出一个 PKCS\#12 兼容的证书存储文件
    -   [openssl\_pkcs12\_export](/ref/openssl.html#openssl_pkcs12_export)
        — 将 PKCS\#12 兼容证书存储文件导出到变量
    -   [openssl\_pkcs12\_read](/ref/openssl.html#openssl_pkcs12_read) —
        将 PKCS\#12 证书存储区解析到数组中
    -   [openssl\_pkcs7\_decrypt](/ref/openssl.html#openssl_pkcs7_decrypt)
        — 解密一个 S/MIME 加密的消息
    -   [openssl\_pkcs7\_encrypt](/ref/openssl.html#openssl_pkcs7_encrypt)
        — 加密一个 S/MIME 消息
    -   [openssl\_pkcs7\_read](/ref/openssl.html#openssl_pkcs7_read) —
        将PKCS7文件导出为PEM格式证书的数组
    -   [openssl\_pkcs7\_sign](/ref/openssl.html#openssl_pkcs7_sign) —
        对一个 S/MIME 消息进行签名
    -   [openssl\_pkcs7\_verify](/ref/openssl.html#openssl_pkcs7_verify)
        — 校验一个已签名的 S/MIME 消息的签名
    -   [openssl\_pkey\_export\_to\_file](/ref/openssl.html#openssl_pkey_export_to_file)
        — 将密钥导出到文件中
    -   [openssl\_pkey\_export](/ref/openssl.html#openssl_pkey_export) —
        将一个密钥的可输出表示转换为字符串
    -   [openssl\_pkey\_free](/ref/openssl.html#openssl_pkey_free) —
        释放一个私钥
    -   [openssl\_pkey\_get\_details](/ref/openssl.html#openssl_pkey_get_details)
        — 返回包含密钥详情的数组
    -   [openssl\_pkey\_get\_private](/ref/openssl.html#openssl_pkey_get_private)
        — 获取私钥
    -   [openssl\_pkey\_get\_public](/ref/openssl.html#openssl_pkey_get_public)
        — 从证书中解析公钥，以供使用。
    -   [openssl\_pkey\_new](/ref/openssl.html#openssl_pkey_new) —
        生成一个新的私钥
    -   [openssl\_private\_decrypt](/ref/openssl.html#openssl_private_decrypt)
        — 使用私钥解密数据
    -   [openssl\_private\_encrypt](/ref/openssl.html#openssl_private_encrypt)
        — 使用私钥加密数据
    -   [openssl\_public\_decrypt](/ref/openssl.html#openssl_public_decrypt)
        — 使用公钥解密数据
    -   [openssl\_public\_encrypt](/ref/openssl.html#openssl_public_encrypt)
        — 使用公钥加密数据
    -   [openssl\_random\_pseudo\_bytes](/ref/openssl.html#openssl_random_pseudo_bytes)
        — 生成一个伪随机字节串
    -   [openssl\_seal](/ref/openssl.html#openssl_seal) — 密封 (加密)
        数据
    -   [openssl\_sign](/ref/openssl.html#openssl_sign) — Generate
        signature
    -   [openssl\_spki\_export\_challenge](/ref/openssl.html#openssl_spki_export_challenge)
        — 导出与签名公钥和挑战相关的挑战字符串
    -   [openssl\_spki\_export](/ref/openssl.html#openssl_spki_export) —
        通过签名公钥和挑战导出一个可用的PEM格式的公钥
    -   [openssl\_spki\_new](/ref/openssl.html#openssl_spki_new) —
        生成一个新的签名公钥和挑战
    -   [openssl\_spki\_verify](/ref/openssl.html#openssl_spki_verify) —
        验证签名公钥和挑战。
    -   [openssl\_verify](/ref/openssl.html#openssl_verify) — 验证签名
    -   [openssl\_x509\_check\_private\_key](/ref/openssl.html#openssl_x509_check_private_key)
        — 检查私钥是否对应于证书
    -   [openssl\_x509\_checkpurpose](/ref/openssl.html#openssl_x509_checkpurpose)
        — 验证是否可以为特定目的使用证书
    -   [openssl\_x509\_export\_to\_file](/ref/openssl.html#openssl_x509_export_to_file)
        — 导出证书至文件
    -   [openssl\_x509\_export](/ref/openssl.html#openssl_x509_export) —
        以字符串格式导出证书
    -   [openssl\_x509\_fingerprint](/ref/openssl.html#openssl_x509_fingerprint)
        — 计算一个给定的x.509证书的指纹或摘要
    -   [openssl\_x509\_free](/ref/openssl.html#openssl_x509_free) —
        释放证书资源
    -   [openssl\_x509\_parse](/ref/openssl.html#openssl_x509_parse) —
        解析一个X509证书并作为一个数组返回信息
    -   [openssl\_x509\_read](/ref/openssl.html#openssl_x509_read) —
        解析一个x.509证书并返回一个资源标识符
    -   [openssl\_x509\_verify](/ref/openssl.html#openssl_x509_verify) —
        Verifies digital signature of x509 certificate against a public
        key

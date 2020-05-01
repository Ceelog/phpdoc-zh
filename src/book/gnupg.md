GNU Privacy Guard
=================

**目录**

-   [简介](/intro/gnupg.html)
-   [安装／配置](/gnupg/setup.html)
    -   [需求](/gnupg/setup.html#需求)
    -   [安装](/gnupg/setup.html#安装)
    -   [运行时配置](/gnupg/setup.html#运行时配置)
    -   [资源类型](/gnupg/setup.html#资源类型)
-   [预定义常量](/gnupg/constants.html)
-   [范例](/gnupg/examples.html)
    -   [Clearsign text](/gnupg/examples.html#Clearsign%20text)
-   [GnuPG 函数](/ref/gnupg.html)
    -   [gnupg\_adddecryptkey](/ref/gnupg.html#gnupg_adddecryptkey) —
        Add a key for decryption
    -   [gnupg\_addencryptkey](/ref/gnupg.html#gnupg_addencryptkey) —
        Add a key for encryption
    -   [gnupg\_addsignkey](/ref/gnupg.html#gnupg_addsignkey) — Add a
        key for signing
    -   [gnupg\_cleardecryptkeys](/ref/gnupg.html#gnupg_cleardecryptkeys)
        — Removes all keys which were set for decryption before
    -   [gnupg\_clearencryptkeys](/ref/gnupg.html#gnupg_clearencryptkeys)
        — Removes all keys which were set for encryption before
    -   [gnupg\_clearsignkeys](/ref/gnupg.html#gnupg_clearsignkeys) —
        Removes all keys which were set for signing before
    -   [gnupg\_decrypt](/ref/gnupg.html#gnupg_decrypt) — Decrypts a
        given text
    -   [gnupg\_decryptverify](/ref/gnupg.html#gnupg_decryptverify) —
        Decrypts and verifies a given text
    -   [gnupg\_encrypt](/ref/gnupg.html#gnupg_encrypt) — Encrypts a
        given text
    -   [gnupg\_encryptsign](/ref/gnupg.html#gnupg_encryptsign) —
        Encrypts and signs a given text
    -   [gnupg\_export](/ref/gnupg.html#gnupg_export) — Exports a key
    -   [gnupg\_geterror](/ref/gnupg.html#gnupg_geterror) — Returns the
        errortext, if a function fails
    -   [gnupg\_getprotocol](/ref/gnupg.html#gnupg_getprotocol) —
        Returns the currently active protocol for all operations
    -   [gnupg\_import](/ref/gnupg.html#gnupg_import) — Imports a key
    -   [gnupg\_init](/ref/gnupg.html#gnupg_init) — Initialize a
        connection
    -   [gnupg\_keyinfo](/ref/gnupg.html#gnupg_keyinfo) — Returns an
        array with information about all keys that matches the given
        pattern
    -   [gnupg\_setarmor](/ref/gnupg.html#gnupg_setarmor) — Toggle
        armored output
    -   [gnupg\_seterrormode](/ref/gnupg.html#gnupg_seterrormode) — Sets
        the mode for error\_reporting
    -   [gnupg\_setsignmode](/ref/gnupg.html#gnupg_setsignmode) — Sets
        the mode for signing
    -   [gnupg\_sign](/ref/gnupg.html#gnupg_sign) — Signs a given text
    -   [gnupg\_verify](/ref/gnupg.html#gnupg_verify) — Verifies a
        signed text

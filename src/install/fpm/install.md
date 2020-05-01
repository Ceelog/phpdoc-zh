安装
----

### 从源代码编译

编译 PHP 时需要 *--enable-fpm* 配置选项来激活 FPM 支持。

以下为 FPM 编译的具体配置参数（全部为可选参数）：

-   *--with-fpm-user* - 设置 FPM 运行的用户身份（默认 - nobody）

-   *--with-fpm-group* - 设置 FPM 运行时的用户组（默认 - nobody）

-   *--with-fpm-systemd* - 启用 systemd 集成 (默认 - no)

-   *--with-fpm-acl* - 使用POSIX 访问控制列表 (默认 - no)
    5.6.5版本起有效

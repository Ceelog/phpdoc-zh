FTP
===

**目录**

-   [简介](/intro/ftp.html)
-   [安装／配置](/ftp/setup.html)
    -   [需求](/ftp/setup.html#需求)
    -   [安装](/ftp/setup.html#安装)
    -   [运行时配置](/ftp/setup.html#运行时配置)
    -   [资源类型](/ftp/setup.html#资源类型)
-   [预定义常量](/ftp/constants.html)
-   [范例](/ftp/examples.html)
    -   [基本用法](/ftp/examples.html#基本用法)
-   [FTP 函数](/ref/ftp.html)
    -   [ftp\_alloc](/ref/ftp.html#ftp_alloc) — 为要上传的文件分配空间
    -   [ftp\_append](/ref/ftp.html#ftp_append) — Append the contents of
        a file to another file on the FTP server
    -   [ftp\_cdup](/ref/ftp.html#ftp_cdup) — 切换到当前目录的父目录
    -   [ftp\_chdir](/ref/ftp.html#ftp_chdir) — 在 FTP
        服务器上改变当前目录
    -   [ftp\_chmod](/ref/ftp.html#ftp_chmod) — 设置 FTP
        服务器上的文件权限
    -   [ftp\_close](/ref/ftp.html#ftp_close) — 关闭一个 FTP 连接
    -   [ftp\_connect](/ref/ftp.html#ftp_connect) — 建立一个新的 FTP
        连接
    -   [ftp\_delete](/ref/ftp.html#ftp_delete) — 删除 FTP
        服务器上的一个文件
    -   [ftp\_exec](/ref/ftp.html#ftp_exec) — 请求运行一条 FTP 命令
    -   [ftp\_fget](/ref/ftp.html#ftp_fget) — 从 FTP
        服务器上下载一个文件并保存到本地一个已经打开的文件中
    -   [ftp\_fput](/ref/ftp.html#ftp_fput) — 上传一个已经打开的文件到
        FTP 服务器
    -   [ftp\_get\_option](/ref/ftp.html#ftp_get_option) — 返回当前 FTP
        连接的各种不同的选项设置
    -   [ftp\_get](/ref/ftp.html#ftp_get) — 从 FTP 服务器上下载一个文件
    -   [ftp\_login](/ref/ftp.html#ftp_login) — 登录 FTP 服务器
    -   [ftp\_mdtm](/ref/ftp.html#ftp_mdtm) — 返回指定文件的最后修改时间
    -   [ftp\_mkdir](/ref/ftp.html#ftp_mkdir) — 建立新目录
    -   [ftp\_mlsd](/ref/ftp.html#ftp_mlsd) — Returns a list of files in
        the given directory
    -   [ftp\_nb\_continue](/ref/ftp.html#ftp_nb_continue) —
        连续获取／发送文件（non-blocking）
    -   [ftp\_nb\_fget](/ref/ftp.html#ftp_nb_fget) — 从 FTP
        服务器获取文件并写入到一个打开的文件（非阻塞）
    -   [ftp\_nb\_fput](/ref/ftp.html#ftp_nb_fput) — 将文件存储到 FTP
        服务器 （非阻塞）
    -   [ftp\_nb\_get](/ref/ftp.html#ftp_nb_get) — 从 FTP
        服务器上获取文件并写入本地文件（non-blocking）
    -   [ftp\_nb\_put](/ref/ftp.html#ftp_nb_put) — 存储一个文件至 FTP
        服务器（non-blocking）
    -   [ftp\_nlist](/ref/ftp.html#ftp_nlist) — 返回给定目录的文件列表
    -   [ftp\_pasv](/ref/ftp.html#ftp_pasv) — 返回当前 FTP
        被动模式是否打开
    -   [ftp\_put](/ref/ftp.html#ftp_put) — 上传文件到 FTP 服务器
    -   [ftp\_pwd](/ref/ftp.html#ftp_pwd) — 返回当前目录名
    -   [ftp\_quit](/ref/ftp.html#ftp_quit) — ftp\_close 的 别名
    -   [ftp\_raw](/ref/ftp.html#ftp_raw) — 向 FTP 服务器发送命令
    -   [ftp\_rawlist](/ref/ftp.html#ftp_rawlist) —
        返回指定目录下文件的详细列表
    -   [ftp\_rename](/ref/ftp.html#ftp_rename) — 更改 FTP
        服务器上的文件或目录名
    -   [ftp\_rmdir](/ref/ftp.html#ftp_rmdir) — 删除 FTP
        服务器上的一个目录
    -   [ftp\_set\_option](/ref/ftp.html#ftp_set_option) — 设置各种 FTP
        运行时选项
    -   [ftp\_site](/ref/ftp.html#ftp_site) — 向服务器发送 SITE 命令
    -   [ftp\_size](/ref/ftp.html#ftp_size) — 返回指定文件的大小
    -   [ftp\_ssl\_connect](/ref/ftp.html#ftp_ssl_connect) — 打开
        SSL-FTP 连接
    -   [ftp\_systype](/ref/ftp.html#ftp_systype) — 返回远程 FTP
        服务器的操作系统类型

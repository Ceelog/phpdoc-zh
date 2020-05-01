网络
====

**目录**

-   [简介](/intro/network.html)
-   [安装／配置](/network/setup.html)
    -   [需求](/network/setup.html#需求)
    -   [安装](/network/setup.html#安装)
    -   [运行时配置](/network/setup.html#运行时配置)
    -   [资源类型](/network/setup.html#资源类型)
-   [预定义常量](/network/constants.html)
-   [网络 函数](/ref/network.html)
    -   [checkdnsrr](/ref/network.html#checkdnsrr) —
        给指定的主机（域名）或者IP地址做DNS通信检查
    -   [closelog](/ref/network.html#closelog) — 关闭系统日志链接
    -   [define\_syslog\_variables](/ref/network.html#define_syslog_variables)
        — Initializes all syslog related variables
    -   [dns\_check\_record](/ref/network.html#dns_check_record) — 别名
        checkdnsrr
    -   [dns\_get\_mx](/ref/network.html#dns_get_mx) — 别名 getmxrr
    -   [dns\_get\_record](/ref/network.html#dns_get_record) —
        获取指定主机的DNS记录
    -   [fsockopen](/ref/network.html#fsockopen) —
        打开一个网络连接或者一个Unix套接字连接
    -   [gethostbyaddr](/ref/network.html#gethostbyaddr) —
        获取指定的IP地址对应的主机名
    -   [gethostbyname](/ref/network.html#gethostbyname) —
        返回主机名对应的 IPv4地址。
    -   [gethostbynamel](/ref/network.html#gethostbynamel) —
        获取互联网主机名对应的 IPv4 地址列表
    -   [gethostname](/ref/network.html#gethostname) — 获取主机名
    -   [getmxrr](/ref/network.html#getmxrr) — 获取互联网主机名对应的 MX
        记录
    -   [getprotobyname](/ref/network.html#getprotobyname) — Get
        protocol number associated with protocol name
    -   [getprotobynumber](/ref/network.html#getprotobynumber) — Get
        protocol name associated with protocol number
    -   [getservbyname](/ref/network.html#getservbyname) —
        获取互联网服务协议对应的端口
    -   [getservbyport](/ref/network.html#getservbyport) — Get Internet
        service which corresponds to port and protocol
    -   [header\_register\_callback](/ref/network.html#header_register_callback)
        — 调用一个 header 函数
    -   [header\_remove](/ref/network.html#header_remove) —
        删除之前设置的 HTTP 头
    -   [header](/ref/network.html#header) — 发送原生 HTTP 头
    -   [headers\_list](/ref/network.html#headers_list) — 返回已发送的
        HTTP 响应头（或准备发送的）
    -   [headers\_sent](/ref/network.html#headers_sent) — 检测 HTTP
        头是否已经发送
    -   [http\_response\_code](/ref/network.html#http_response_code) —
        获取/设置响应的 HTTP 状态码
    -   [inet\_ntop](/ref/network.html#inet_ntop) — Converts a packed
        internet address to a human readable representation
    -   [inet\_pton](/ref/network.html#inet_pton) — Converts a human
        readable IP address to its packed in\_addr representation
    -   [ip2long](/ref/network.html#ip2long) — 将 IPV4
        的字符串互联网协议转换成长整型数字
    -   [long2ip](/ref/network.html#long2ip) —
        将长整型转化为字符串形式带点的互联网标准格式地址（IPV4）
    -   [openlog](/ref/network.html#openlog) — Open connection to system
        logger
    -   [pfsockopen](/ref/network.html#pfsockopen) —
        打开一个持久的网络连接或者Unix套接字连接。
    -   [setcookie](/ref/network.html#setcookie) — 发送 Cookie
    -   [setrawcookie](/ref/network.html#setrawcookie) — 发送未经 URL
        编码的 cookie
    -   [socket\_get\_status](/ref/network.html#socket_get_status) —
        别名 stream\_get\_meta\_data
    -   [socket\_set\_blocking](/ref/network.html#socket_set_blocking) —
        别名 stream\_set\_blocking
    -   [socket\_set\_timeout](/ref/network.html#socket_set_timeout) —
        别名 stream\_set\_timeout
    -   [syslog](/ref/network.html#syslog) — Generate a system log
        message

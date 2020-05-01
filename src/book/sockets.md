Sockets
=======

**目录**

-   [简介](/intro/sockets.html)
-   [安装／配置](/sockets/setup.html)
    -   [需求](/sockets/setup.html#需求)
    -   [安装](/sockets/setup.html#安装)
    -   [运行时配置](/sockets/setup.html#运行时配置)
    -   [资源类型](/sockets/setup.html#资源类型)
-   [预定义常量](/sockets/constants.html)
-   [范例](/sockets/examples.html)
-   [Socket Errors](/sockets/errors.html)
-   [Socket 函数](/ref/sockets.html)
    -   [socket\_accept](/ref/sockets.html#socket_accept) — Accepts a
        connection on a socket
    -   [socket\_addrinfo\_bind](/ref/sockets.html#socket_addrinfo_bind)
        — Create and bind to a socket from a given addrinfo
    -   [socket\_addrinfo\_connect](/ref/sockets.html#socket_addrinfo_connect)
        — Create and connect to a socket from a given addrinfo
    -   [socket\_addrinfo\_explain](/ref/sockets.html#socket_addrinfo_explain)
        — Get information about addrinfo
    -   [socket\_addrinfo\_lookup](/ref/sockets.html#socket_addrinfo_lookup)
        — Get array with contents of getaddrinfo about the given
        hostname
    -   [socket\_bind](/ref/sockets.html#socket_bind) — 给套接字绑定名字
    -   [socket\_clear\_error](/ref/sockets.html#socket_clear_error) —
        清除套接字或者最后的错误代码上的错误
    -   [socket\_close](/ref/sockets.html#socket_close) — 关闭套接字资源
    -   [socket\_cmsg\_space](/ref/sockets.html#socket_cmsg_space) —
        Calculate message buffer size
    -   [socket\_connect](/ref/sockets.html#socket_connect) —
        开启一个套接字连接
    -   [socket\_create\_listen](/ref/sockets.html#socket_create_listen)
        — Opens a socket on port to accept connections
    -   [socket\_create\_pair](/ref/sockets.html#socket_create_pair) —
        Creates a pair of indistinguishable sockets and stores them in
        an array
    -   [socket\_create](/ref/sockets.html#socket_create) —
        创建一个套接字（通讯节点）
    -   [socket\_export\_stream](/ref/sockets.html#socket_export_stream)
        — Export a socket extension resource into a stream that
        encapsulates a socket
    -   [socket\_get\_option](/ref/sockets.html#socket_get_option) —
        Gets socket options for the socket
    -   [socket\_getopt](/ref/sockets.html#socket_getopt) — 别名
        socket\_get\_option
    -   [socket\_getpeername](/ref/sockets.html#socket_getpeername) —
        Queries the remote side of the given socket which may either
        result in host/port or in a Unix filesystem path, dependent on
        its type
    -   [socket\_getsockname](/ref/sockets.html#socket_getsockname) —
        Queries the local side of the given socket which may either
        result in host/port or in a Unix filesystem path, dependent on
        its type
    -   [socket\_import\_stream](/ref/sockets.html#socket_import_stream)
        — Import a stream
    -   [socket\_last\_error](/ref/sockets.html#socket_last_error) —
        Returns the last error on the socket
    -   [socket\_listen](/ref/sockets.html#socket_listen) — Listens for
        a connection on a socket
    -   [socket\_read](/ref/sockets.html#socket_read) — Reads a maximum
        of length bytes from a socket
    -   [socket\_recv](/ref/sockets.html#socket_recv) —
        从已连接的socket接收数据
    -   [socket\_recvfrom](/ref/sockets.html#socket_recvfrom) — Receives
        data from a socket whether or not it is connection-oriented
    -   [socket\_recvmsg](/ref/sockets.html#socket_recvmsg) — Read a
        message
    -   [socket\_select](/ref/sockets.html#socket_select) — Runs the
        select() system call on the given arrays of sockets with a
        specified timeout
    -   [socket\_send](/ref/sockets.html#socket_send) — Sends data to a
        connected socket
    -   [socket\_sendmsg](/ref/sockets.html#socket_sendmsg) — Send a
        message
    -   [socket\_sendto](/ref/sockets.html#socket_sendto) — Sends a
        message to a socket, whether it is connected or not
    -   [socket\_set\_block](/ref/sockets.html#socket_set_block) — Sets
        blocking mode on a socket resource
    -   [socket\_set\_nonblock](/ref/sockets.html#socket_set_nonblock) —
        Sets nonblocking mode for file descriptor fd
    -   [socket\_set\_option](/ref/sockets.html#socket_set_option) —
        Sets socket options for the socket
    -   [socket\_setopt](/ref/sockets.html#socket_setopt) — 别名
        socket\_set\_option
    -   [socket\_shutdown](/ref/sockets.html#socket_shutdown) — Shuts
        down a socket for receiving, sending, or both
    -   [socket\_strerror](/ref/sockets.html#socket_strerror) — Return a
        string describing a socket error
    -   [socket\_write](/ref/sockets.html#socket_write) — Write to a
        socket
    -   [socket\_wsaprotocol\_info\_export](/ref/sockets.html#socket_wsaprotocol_info_export)
        — Exports the WSAPROTOCOL\_INFO Structure
    -   [socket\_wsaprotocol\_info\_import](/ref/sockets.html#socket_wsaprotocol_info_import)
        — Imports a Socket from another Process
    -   [socket\_wsaprotocol\_info\_release](/ref/sockets.html#socket_wsaprotocol_info_release)
        — Releases an exported WSAPROTOCOL\_INFO Structure

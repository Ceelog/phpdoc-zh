预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`AF_UNIX`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`AF_INET`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`AF_INET6`** (<span class="type">integer</span>)  
<span class="simpara"> 只有在编译时加入 IPv6 支持的时候才有效。 </span>

**`SOCK_STREAM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCK_DGRAM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCK_RAW`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCK_SEQPACKET`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCK_RDM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MSG_OOB`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MSG_WAITALL`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MSG_PEEK`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MSG_DONTROUTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`MSG_EOR`** (<span class="type">integer</span>)  
<span class="simpara"> 在 Windows 平台上无效。 </span>

**`MSG_EOF`** (<span class="type">integer</span>)  
<span class="simpara"> 在 Windows 平台上无效。 </span>

**`SO_DEBUG`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_REUSEADDR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_REUSEPORT`** (<span class="type">integer</span>)  
<span class="simpara">
该常量在PHP5.4.10及以上版本，并且支持**`SO_REUSEPORT`**socket选项的平台上可用。包括Mac
OS X和FreeBSD，不包括Linux和Windows。 </span>

**`SO_KEEPALIVE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_DONTROUTE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_LINGER`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_BROADCAST`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_OOBINLINE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_SNDBUF`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_RCVBUF`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_SNDLOWAT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_RCVLOWAT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_SNDTIMEO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_RCVTIMEO`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_TYPE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SO_ERROR`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`TCP_NODELAY`** (<span class="type">integer</span>)  
<span class="simpara"> Used to disable Nagle TCP algorithm. Added in PHP
5.2.7. </span>

**`SOL_SOCKET`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PHP_NORMAL_READ`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`PHP_BINARY_READ`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOL_TCP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOL_UDP`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

以下常量在Windows和类UNIX平台上被定义。每个常量只有在平台上有该常量值的时候才会被定义。

**`SOCKET_EINTR`** (<span class="type">integer</span>)  
<span class="simpara"> 中断系统调用。 </span>

**`SOCKET_EBADF`** (<span class="type">integer</span>)  
<span class="simpara"> 坏文件编号。 </span>

**`SOCKET_EACCES`** (<span class="type">integer</span>)  
<span class="simpara"> 拒绝访问。 </span>

**`SOCKET_EFAULT`** (<span class="type">integer</span>)  
<span class="simpara"> 错误的地址。 </span>

**`SOCKET_EINVAL`** (<span class="type">integer</span>)  
<span class="simpara"> 无效的参数。 </span>

**`SOCKET_EMFILE`** (<span class="type">integer</span>)  
<span class="simpara"> 打开的文件太多。 </span>

**`SOCKET_ENAMETOOLONG`** (<span class="type">integer</span>)  
<span class="simpara"> 文件名过长。 </span>

**`SOCKET_ENOTEMPTY`** (<span class="type">integer</span>)  
<span class="simpara"> 目录不为空。 </span>

**`SOCKET_ELOOP`** (<span class="type">integer</span>)  
<span class="simpara"> Too many symbolic links encountered. </span>

**`SOCKET_EWOULDBLOCK`** (<span class="type">integer</span>)  
<span class="simpara"> 操作将阻塞。 </span>

**`SOCKET_EREMOTE`** (<span class="type">integer</span>)  
<span class="simpara"> 对象是远程。 </span>

**`SOCKET_EUSERS`** (<span class="type">integer</span>)  
<span class="simpara"> 太多用户。 </span>

**`SOCKET_ENOTSOCK`** (<span class="type">integer</span>)  
<span class="simpara"> 非socket套接字操作。 </span>

**`SOCKET_EDESTADDRREQ`** (<span class="type">integer</span>)  
<span class="simpara"> 需要目的地址。 </span>

**`SOCKET_EMSGSIZE`** (<span class="type">integer</span>)  
<span class="simpara"> 消息太长。 </span>

**`SOCKET_EPROTOTYPE`** (<span class="type">integer</span>)  
<span class="simpara"> socket协议类型错误。 </span>

**`SOCKET_EPROTONOSUPPORT`** (<span class="type">integer</span>)  
<span class="simpara"> 不支持的协议。 </span>

**`SOCKET_ESOCKTNOSUPPORT`** (<span class="type">integer</span>)  
<span class="simpara"> 不支持的socket类型。 </span>

**`SOCKET_EOPNOTSUPP`** (<span class="type">integer</span>)  
<span class="simpara"> 传输断点不支持的操作。 </span>

**`SOCKET_EPFNOSUPPORT`** (<span class="type">integer</span>)  
<span class="simpara"> 不支持的协议族。 </span>

**`SOCKET_EAFNOSUPPORT`** (<span class="type">integer</span>)  
<span class="simpara"> 协议不支持的地址族。 </span>

**`SOCKET_EADDRNOTAVAIL`** (<span class="type">integer</span>)  
<span class="simpara"> 不能分配请求的地址。 </span>

**`SOCKET_ENETDOWN`** (<span class="type">integer</span>)  
<span class="simpara"> 网络出现故障。 </span>

**`SOCKET_ENETUNREACH`** (<span class="type">integer</span>)  
<span class="simpara"> 网络不可达。 </span>

**`SOCKET_ENETRESET`** (<span class="type">integer</span>)  
<span class="simpara"> 复位，网络掉线。 </span>

**`SOCKET_ECONNABORTED`** (<span class="type">integer</span>)  
<span class="simpara"> 软件导致连接中止。 </span>

**`SOCKET_ECONNRESET`** (<span class="type">integer</span>)  
<span class="simpara"> 对方重置连接。 </span>

**`SOCKET_ENOBUFS`** (<span class="type">integer</span>)  
<span class="simpara"> 无可用的缓存区空间。 </span>

**`SOCKET_EISCONN`** (<span class="type">integer</span>)  
<span class="simpara"> 传输端点已经连接。 </span>

**`SOCKET_ENOTCONN`** (<span class="type">integer</span>)  
<span class="simpara"> 传输端点未连接。 </span>

**`SOCKET_ESHUTDOWN`** (<span class="type">integer</span>)  
<span class="simpara"> 传输端点关闭，无法发送。 </span>

**`SOCKET_ETIMEDOUT`** (<span class="type">integer</span>)  
<span class="simpara"> 连接超时。 </span>

**`SOCKET_ECONNREFUSED`** (<span class="type">integer</span>)  
<span class="simpara"> 连接被拒绝。 </span>

**`SOCKET_EHOSTDOWN`** (<span class="type">integer</span>)  
<span class="simpara"> 主机已关闭。 </span>

**`SOCKET_EHOSTUNREACH`** (<span class="type">integer</span>)  
<span class="simpara"> 没有路由到主机。 </span>

**`SOCKET_EALREADY`** (<span class="type">integer</span>)  
<span class="simpara"> 操作已在进行中。 </span>

**`SOCKET_EINPROGRESS`** (<span class="type">integer</span>)  
<span class="simpara"> 操作正在进行中。 </span>

以下常量只能在windows中定义。

**`SOCKET_ENOPROTOOPT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_EADDRINUSE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_ETOOMYREFS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_EPROCLIM`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_EDUOT`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_ESTALE`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_EDISCON`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_SYSNOTREADY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_VERNOTSUPPORTED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_NOTINITIALISED`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_HOST_NOT_FOUND`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_TRY_AGAIN`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_NO_RECOVERY`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_NO_DATA`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

**`SOCKET_NO_ADDRESS`** (<span class="type">integer</span>)  
<span class="simpara"> </span>

以下常量仅适用于类UNIX。 每个常量只有在该平台上此值可用时被定义。

**`SOCKET_EPERM`** (<span class="type">integer</span>)  
<span class="simpara"> 操作不允许。 </span>

**`SOCKET_ENOENT`** (<span class="type">integer</span>)  
<span class="simpara"> 文件或目录不存在。 </span>

**`SOCKET_EIO`** (<span class="type">integer</span>)  
<span class="simpara"> I/O错误。 </span>

**`SOCKET_ENXIO`** (<span class="type">integer</span>)  
<span class="simpara"> 未找到设备或地址。 </span>

**`SOCKET_E2BIG`** (<span class="type">integer</span>)  
<span class="simpara"> 参数列表太长。 </span>

**`SOCKET_EAGAIN`** (<span class="type">integer</span>)  
<span class="simpara"> 请重试。 </span>

**`SOCKET_ENOMEM`** (<span class="type">integer</span>)  
<span class="simpara"> 内存不足。 </span>

**`SOCKET_ENOTBLK`** (<span class="type">integer</span>)  
<span class="simpara"> 需要块设备。 </span>

**`SOCKET_EBUSY`** (<span class="type">integer</span>)  
<span class="simpara"> 设备或资源忙。 </span>

**`SOCKET_EEXIST`** (<span class="type">integer</span>)  
<span class="simpara"> 文件存在。 </span>

**`SOCKET_EXDEV`** (<span class="type">integer</span>)  
<span class="simpara"> 跨设备链路。 </span>

**`SOCKET_ENODEV`** (<span class="type">integer</span>)  
<span class="simpara"> 设备不存在。 </span>

**`SOCKET_ENOTDIR`** (<span class="type">integer</span>)  
<span class="simpara"> 非目录。 </span>

**`SOCKET_EISDIR`** (<span class="type">integer</span>)  
<span class="simpara"> 是目录。 </span>

**`SOCKET_ENFILE`** (<span class="type">integer</span>)  
<span class="simpara"> 文件表溢出。 </span>

**`SOCKET_ENOTTY`** (<span class="type">integer</span>)  
<span class="simpara"> 不是打字机。 </span>

**`SOCKET_ENOSPC`** (<span class="type">integer</span>)  
<span class="simpara"> 设备上没有剩余空间。 </span>

**`SOCKET_ESPIPE`** (<span class="type">integer</span>)  
<span class="simpara"> 非法查找。 </span>

**`SOCKET_EROFS`** (<span class="type">integer</span>)  
<span class="simpara"> 文件系统只读。 </span>

**`SOCKET_EMLINK`** (<span class="type">integer</span>)  
<span class="simpara"> 链路太多。 </span>

**`SOCKET_EPIPE`** (<span class="type">integer</span>)  
<span class="simpara"> 管道断开。 </span>

**`SOCKET_ENOLCK`** (<span class="type">integer</span>)  
<span class="simpara"> 无可用的记录锁。 </span>

**`SOCKET_ENOSYS`** (<span class="type">integer</span>)  
<span class="simpara"> 函数未实现。 </span>

**`SOCKET_ENOMSG`** (<span class="type">integer</span>)  
<span class="simpara"> 无需要类型的消息。 </span>

**`SOCKET_EIDRM`** (<span class="type">integer</span>)  
<span class="simpara"> 标识符被删除。 </span>

**`SOCKET_ECHRNG`** (<span class="type">integer</span>)  
<span class="simpara"> 通道数超出范围。 </span>

**`SOCKET_EL2NSYNC`** (<span class="type">integer</span>)  
<span class="simpara"> 2级未同步。 </span>

**`SOCKET_EL3HLT`** (<span class="type">integer</span>)  
<span class="simpara"> 3级停止。 </span>

**`SOCKET_EL3RST`** (<span class="type">integer</span>)  
<span class="simpara"> 3级重置。 </span>

**`SOCKET_ELNRNG`** (<span class="type">integer</span>)  
<span class="simpara"> 链接数超出范围。 </span>

**`SOCKET_EUNATCH`** (<span class="type">integer</span>)  
<span class="simpara"> 协议驱动没有安装。 </span>

**`SOCKET_ENOCSI`** (<span class="type">integer</span>)  
<span class="simpara"> 没有可用的CSI结构。 </span>

**`SOCKET_EL2HLT`** (<span class="type">integer</span>)  
<span class="simpara"> 2级停止。 </span>

**`SOCKET_EBADE`** (<span class="type">integer</span>)  
<span class="simpara"> 无效的交换。 </span>

**`SOCKET_EBADR`** (<span class="type">integer</span>)  
<span class="simpara"> 无效的请求描述符。 </span>

**`SOCKET_EXFULL`** (<span class="type">integer</span>)  
<span class="simpara"> 交换满了。 </span>

**`SOCKET_ENOANO`** (<span class="type">integer</span>)  
<span class="simpara"> 无阳极。 </span>

**`SOCKET_EBADRQC`** (<span class="type">integer</span>)  
<span class="simpara"> 无效的请求代码。 </span>

**`SOCKET_EBADSLT`** (<span class="type">integer</span>)  
<span class="simpara"> 无效的插槽。 </span>

**`SOCKET_ENOSTR`** (<span class="type">integer</span>)  
<span class="simpara"> 设备不是流。 </span>

**`SOCKET_ENODATA`** (<span class="type">integer</span>)  
<span class="simpara"> 无可用的数据。 </span>

**`SOCKET_ETIME`** (<span class="type">integer</span>)  
<span class="simpara"> 计时器过期。 </span>

**`SOCKET_ENOSR`** (<span class="type">integer</span>)  
<span class="simpara"> 流资源不够用。 </span>

**`SOCKET_ENONET`** (<span class="type">integer</span>)  
<span class="simpara"> 机器不在网络上。 </span>

**`SOCKET_ENOLINK`** (<span class="type">integer</span>)  
<span class="simpara"> 链接已被切断。 </span>

**`SOCKET_EADV`** (<span class="type">integer</span>)  
<span class="simpara"> 通知错误。 </span>

**`SOCKET_ESRMNT`** (<span class="type">integer</span>)  
<span class="simpara"> Srmount错误。 </span>

**`SOCKET_ECOMM`** (<span class="type">integer</span>)  
<span class="simpara"> 发送时通信错误。 </span>

**`SOCKET_EPROTO`** (<span class="type">integer</span>)  
<span class="simpara"> 协议错误。 </span>

**`SOCKET_EMULTIHOP`** (<span class="type">integer</span>)  
<span class="simpara"> 多跳尝试。 </span>

**`SOCKET_EBADMSG`** (<span class="type">integer</span>)  
<span class="simpara"> 不是一个数据消息。 </span>

**`SOCKET_ENOTUNIQ`** (<span class="type">integer</span>)  
<span class="simpara"> 名称在网络上不唯一。 </span>

**`SOCKET_EBADFD`** (<span class="type">integer</span>)  
<span class="simpara"> 文件描述符处于错误状态。 </span>

**`SOCKET_EREMCHG`** (<span class="type">integer</span>)  
<span class="simpara"> 远程地址改变。 </span>

**`SOCKET_ERESTART`** (<span class="type">integer</span>)  
<span class="simpara"> 中断的系统调用应该被重新启动。 </span>

**`SOCKET_ESTRPIPE`** (<span class="type">integer</span>)  
<span class="simpara"> 流管道错误。 </span>

**`SOCKET_EPROTOOPT`** (<span class="type">integer</span>)  
<span class="simpara"> 协议不可用。 </span>

**`SOCKET_ADDRINUSE`** (<span class="type">integer</span>)  
<span class="simpara"> 地址已经被占用。 </span>

**`SOCKET_ETOOMANYREFS`** (<span class="type">integer</span>)  
<span class="simpara"> 过多的引用：无法接合。 </span>

**`SOCKET_EISNAM`** (<span class="type">integer</span>)  
<span class="simpara"> 是一个已命名类型的文件。 </span>

**`SOCKET_EREMOTEIO`** (<span class="type">integer</span>)  
<span class="simpara"> 远程I/O错误。 </span>

**`SOCKET_EDQUOT`** (<span class="type">integer</span>)  
<span class="simpara"> 超过配额。 </span>

**`SOCKET_ENOMEDIUM`** (<span class="type">integer</span>)  
<span class="simpara"> 未找到媒体。 </span>

**`SOCKET_EMEDIUMTYPE`** (<span class="type">integer</span>)  
<span class="simpara"> 错误的媒体类型。 </span>

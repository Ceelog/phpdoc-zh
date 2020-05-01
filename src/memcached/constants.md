预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`Memcached::OPT_COMPRESSION`**  
开启或关闭压缩功能。当开启的时候，item的值超过某个阈值（当前是100bytes）时，会首先对值进行压缩然后存储，并
在获取该值时进行解压缩然后返回，使得压缩对应用层透明。

类型: *boolean*, 默认: **`TRUE`**.

**`Memcached::OPT_SERIALIZER`**  
指定对于非标量值进行序列化的序列化工具。可用的值有**`Memcached::SERIALIZER_PHP`**
和**`Memcached::SERIALIZER_IGBINARY`**。后者仅在memcached配置时开启
*--enable-memcached-igbinary*选项并且 *igbinary*扩展被加载时才有效。

类型: *integer*, 默认: **`Memcached::SERIALIZER_PHP`**.

**`Memcached::SERIALIZER_PHP`**  
默认的PHP序列化工具（即serialize方法）。

**`Memcached::SERIALIZER_IGBINARY`**  
<a href="https://github.com/igbinary/igbinary" class="link external">» igbinary</a>序列化工具。它将php的数据结构
存储为紧密的二进制形式，在时间和空间上都有所改进。

**`Memcached::SERIALIZER_JSON`**  
JSON序列化，需要 PHP 5.2.10以上。

**`Memcached::OPT_PREFIX_KEY`**  
可以用于为key创建“域”。这个值将会被作为每个key的前缀，它不能长于*128*个字符，
并且将会缩短最大可允许的key的长度。这个前缀仅仅用于被存储的元素的key，而不会用于服务器key。

类型: *string*, 默认: *""*.

**`Memcached::OPT_HASH`**  
指定存储元素key使用的hash算法。可用的值是**`Memcached::HASH_*`**系列的常量。
每种hash算法都有它的优势和劣势，在你不了解或不确定哪种算法对你更有利时，请使用默认值。

类型: *integer*, 默认: **`Memcached::HASH_DEFAULT`**

**`Memcached::HASH_DEFAULT`**  
默认的(Jenkins one-at-a-time)元素key hash算法

**`Memcached::HASH_MD5`**  
md5元素key hash算法。

**`Memcached::HASH_CRC`**  
CRC元素key hash算法。

**`Memcached::HASH_FNV1_64`**  
FNV1\_64元素key hash算法。

**`Memcached::HASH_FNV1A_64`**  
FNV1\_64A元素key hash算法。

**`Memcached::HASH_FNV1_32`**  
FNV1\_32元素key hash算法。

**`Memcached::HASH_FNV1A_32`**  
FNV1\_32A元素key hash算法。

**`Memcached::HASH_HSIEH`**  
Hsieh元素key hash算法。

**`Memcached::HASH_MURMUR`**  
Murmur元素key hash算法。

**`Memcached::OPT_DISTRIBUTION`**  
指定元素key分布到各个服务器的方法。当前支持的方法有余数分步法合一致性hash算法两种。一致性hash算法提供
了更好的分配策略并且在添加服务器到集群时可以最小化缓存丢失。

类型: *integer*, 默认: **`Memcached::DISTRIBUTION_MODULA.`**

**`Memcached::DISTRIBUTION_MODULA`**  
余数分布算法。

**`Memcached::DISTRIBUTION_CONSISTENT`**  
一致性分布算法(基于libketama).

**`Memcached::OPT_LIBKETAMA_COMPATIBLE`**  
开启或关闭兼容的libketama类行为。当开启此选项后，元素key的hash算法将会被设置为md5并且分布算法将会
采用带有权重的一致性hash分布。这一点非常有用因为其他基于libketama的客户端（比如python，urby）在同样
的服务端配置下可以透明的访问key。

> **Note**:
>
> 如果你要使用一致性hash算法强烈建议开启此选项，并且这个选项可能在未来的发布版中被设置为默认开启。

类型: *boolean*, 默认: **`FALSE`**.

**`Memcached::OPT_BUFFER_WRITES`**  
开启或关闭I/O缓存。开启I/O缓存会导致存储命令不实际发送而是存储到缓冲区中。任意的检索数据操作都会导致
缓存中的数据被发送到远程服务端。退出连接或关闭连接也会导致缓存数据被发送到远程服务端。

类型: *boolean*, 默认: **`FALSE`**.

**`Memcached::OPT_BINARY_PROTOCOL`**  
开启使用二进制协议。请注意这个选项不能在一个打开的连接上进行切换。

类型: *boolean*, 默认: **`FALSE`**.

**`Memcached::OPT_NO_BLOCK`**  
开启或关闭异步I/O。这将使得存储函数传输速度最大化。

类型: *boolean*, 默认: **`FALSE`**.

**`Memcached::OPT_TCP_NODELAY`**  
开启或关闭已连接socket的无延迟特性（在某些幻境可能会带来速度上的提升）。

类型: *boolean*, 默认: **`FALSE`**.

**`Memcached::OPT_SOCKET_SEND_SIZE`**  
socket发送缓冲的最大值。

类型: *integer*, 默认: 根据不同的平台/内核配置不同

**`Memcached::OPT_SOCKET_RECV_SIZE`**  
socket接收缓冲的最大值。

类型: *integer*, 默认: 根据不同的平台/内核配置不同

**`Memcached::OPT_CONNECT_TIMEOUT`**  
在非阻塞模式下这里设置的值就是socket连接的超时时间，单位是毫秒。

类型: *integer*, 默认: *1000*.

**`Memcached::OPT_RETRY_TIMEOUT`**  
等待失败的连接重试的时间，单位秒。

类型: *integer*, 默认: *0*.

**`Memcached::OPT_SEND_TIMEOUT`**  
socket发送超时时间，单位微秒。在这种情况下您不能使用非阻塞I/O，这将使得您仍然有数据会发送超时。

类型: *integer*, 默认: *0*.

**`Memcached::OPT_RECV_TIMEOUT`**  
socket读取超时时间，单位微秒。在这种情况下您不能使用非阻塞I/O，这将使得您仍然有数据会读取超时。

类型: *integer*, 默认: *0*.

**`Memcached::OPT_POLL_TIMEOUT`**  
poll连接超时时间，单位毫秒。

类型: *integer*, 默认: *1000*.

**`Memcached::OPT_CACHE_LOOKUPS`**  
开启或禁用DNS查找缓存。

类型: *boolean*, 默认: **`FALSE`**.

**`Memcached::OPT_SERVER_FAILURE_LIMIT`**  
指定一个服务器连接的失败重试次数限制。在达到此数量的失败重连后此服务器将被从服务器池中移除。

类型: *integer*, 默认: *0*.

**`Memcached::HAVE_IGBINARY`**  
指示是否支持igbinary的序列化。

类型: *boolean*.

**`Memcached::HAVE_JSON`**  
指示是否支持json的序列化。

类型: *boolean*.

**`Memcached::GET_PRESERVE_ORDER`**  
一个用于<span class="function">Memcached::getMulti</span>和 <span
class="function">Memcached::getMultiByKey</span>的标记用以确保返回的key和请求的key顺序保持一致。
不存在的key将会得到一个NULL值。

**`Memcached::RES_SUCCESS`**  
操作成功。

**`Memcached::RES_FAILURE`**  
某种方式的操作失败。

**`Memcached::RES_HOST_LOOKUP_FAILURE`**  
DNS查找失败。

**`Memcached::RES_UNKNOWN_READ_FAILURE`**  
读取网络数据失败。

**`Memcached::RES_PROTOCOL_ERROR`**  
错误的memcached协议命令。

**`Memcached::RES_CLIENT_ERROR`**  
客户端错误。

**`Memcached::RES_SERVER_ERROR`**  
服务端错误。

**`Memcached::RES_WRITE_FAILURE`**  
向网络写数据失败。

**`Memcached::RES_DATA_EXISTS`**  
比较并交换值操作失败（cas方法）：尝试向服务端存储数据时由于自此连接最后一次取此key对应数据之后被改变导致失败。

**`Memcached::RES_NOTSTORED`**  
元素没有被存储，但并不是因为一个错误。这通常表明add（元素已存在）或replace（元素不存在）方式存储数据失败或者元素已经在一个删除序列中（延时删除）。

**`Memcached::RES_NOTFOUND`**  
元素未找到（通过get或cas操作时）。

**`Memcached::RES_PARTIAL_READ`**  
局部网络数据读错误。

**`Memcached::RES_SOME_ERRORS`**  
在多key获取的时候发生错误。

**`Memcached::RES_NO_SERVERS`**  
服务器池空。

**`Memcached::RES_END`**  
结果集到结尾了。

**`Memcached::RES_ERRNO`**  
系统错误。

**`Memcached::RES_BUFFERED`**  
操作被缓存。

**`Memcached::RES_TIMEOUT`**  
操作超时。

**`Memcached::RES_BAD_KEY_PROVIDED`**  
提供了无效的key。

**`Memcached::RES_CONNECTION_SOCKET_CREATE_FAILURE`**  
创建网络socket失败。

**`Memcached::RES_PAYLOAD_FAILURE`**  
不能压缩/解压缩或序列化/反序列化值。

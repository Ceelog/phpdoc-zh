Sessions支持
============

memcached提供了一个自定义的session处理器可以被用于存储用户session数据到memcached服务端。
一个完全独立的memcached实例将会在内部使用，因此如果需要您可以设置一个不同的服务器池。session的
key被存储在前缀*memc.sess.key.*之下，因此,
如果你对session和通常的缓存使用了 同样的服务器池，请注意这一点。
译注：另外一个session和通常缓存分离的原因是当通常的缓存占满了memcached服务端后，可能会导致你的session被
从缓存中踢除，导致用户莫名的掉线。

`session.save_handler` <span class="type">string</span>  
设置为*memcached*开启memcached的session处理器。

`session.save_path` <span class="type">string</span>  
定义一个逗号分隔的*hostname:port*样式的session缓存服务器池，例如：
*"sess1:11211, sess2:11211"*.

OPcache 通过将 PHP 脚本预编译的字节码存储到共享内存中来提升 PHP 的性能，
存储预编译字节码的好处就是 省去了每次加载和解析 PHP 脚本的开销。

PHP 5.5.0 及后续版本中已经绑定了 OPcache 扩展。 对于 PHP 5.2，5.3 和 5.4
版本可以使用
<a href="https://pecl.php.net/package/ZendOpcache" class="link external">» PECL</a>
扩展中的 OPcache 库。

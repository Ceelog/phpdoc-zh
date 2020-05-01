Cookie
======

PHP 透明地支持 HTTP cookie。cookie
是一种在远程浏览器端储存数据并以此来跟踪和识别用户的机制。可以用 <span
class="function">setcookie</span> 或 <span
class="function">setrawcookie</span> 函数来设置 cookie。cookie 是 HTTP
标头的一部分，因此 <span class="function">setcookie</span>
函数必须在其它信息被输出到浏览器前调用，这和对 <span
class="function">header</span>
函数的限制类似。可以使用<a href="/ref/outcontrol.html" class="link">输出缓冲函数</a>来延迟脚本的输出，直到按需要设置好了所有的
cookie 或者其它HTTP头。

如果
<a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
中包括“C”，则任何从客户端发送的 cookie 都会被自动包括进 `$_COOKIE`
自动全局数组。如果希望对一个 cookie 变量设置多个值，则需在 cookie
的名称后加 *\[\]* 符号。

根据
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
的设置，可以从 cookie 建立普通的 PHP
变量。但是不推荐依赖于此特性，因为出于安全原因此选项通常是关闭的。

关于更多细节以及有关浏览器问题的注意事项，参见 <span
class="function">setcookie</span> 和 <span
class="function">setrawcookie</span> 函数。

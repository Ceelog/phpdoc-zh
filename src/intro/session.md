会话支持在 PHP
中是在并发访问时由一个方法来保存某些数据.从而使你能够构建更多的定制程序
从而提高你的 web 网站的吸引力.

一个访问者访问你的 web 网站将被分配一个唯一的 id, 就是所谓的会话 id.
这个 id 可以存储在用户端的一个 cookie 中，也可以通过 URL 进行传递.

会话支持允许你将请求中的数据保存在超全局数组`$_SESSION`中.
当一个访问者访问你的网站，PHP 将自动检查(如果
<a href="/session/setup.html#" class="link">session.auto_start</a>
被设置为 1）或者在你要求下检查(明确通过 <span
class="function">session\_start</span> 或者隐式通过 <span
class="function">session\_register</span>) 当前会话 id
是否是先前发送的请求创建. 如果是这种情况， 那么先前保存的环境将被重建.

**Caution**

如果你打开了
<a href="/session/setup.html#" class="link">session.auto_start</a> 那么
将对象放入会话的唯一方法是使用
<a href="/ini/core.html#ini.auto-prepend-file" class="link">auto_prepend_file</a>
来加载定义这个对象的类，其中，在加载的定义的类时，你不得不使用 <span
class="function">serialize</span> 你得对象，并且事后 <span
class="function">unserialize</span> 它.

`$_SESSION` (和所有已注册得变量) 将被 PHP
使用内置的序列化方法在请求完成时 进行序列化.序列化方法可以通过
<a href="/session/setup.html#" class="link">session.serialize_handler</a>
这个 PHP
配置选项中来设置一个指定的方法.注册的变量未定义将被标记为未定义.在并发访问时,这些变量不会被会话模块
定义除非用户后来定义了它们.

**Warning**

因为会话数据是被序列化的，<span class="type">resource</span>
变量不能被存储在会话中.

序列化句柄 (*php* 和 *php\_binary*) 会受到 register\_globals 的限制.
而且，数字索引或者字符串索引包含的特殊字符(*\|* 和 *!*) 不能被使用.
使用这些字符将脚本执行关闭时的最后出现错误. *php\_serialize*
没有这样的限制.*php\_serialize* 从 PHP 5.5.4 以后可用.

> **Note**:
>
> 请注意当会话工作时，会话的记录并没有被创建 直到一个变量已经被使用
> <span class="function">session\_register</span>
> 注册或者被添加一个新元素到 `$_SESSION` 全局数组中.
> 这点一直有效，无论是否使用 <span
> class="function">session\_start</span> 函数 来开始会话.

> **Note**:
>
> 在 PHP 5.2.2 有一个没有在文档中说明的特性是用文件存储时，即使是 在
> <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
> 被启用，并且 "/tmp" 没有被添加到 允许路径列表中，也能将会话存储到
> "/tmp" 目录. 这个特性在 PHP 5.3.0 时已经从 PHP 中被移除了.

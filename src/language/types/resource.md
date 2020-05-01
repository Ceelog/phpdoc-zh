Resource 资源类型
-----------------

资源 <span class="type">resource</span>
是一种特殊变量，保存了到外部资源的一个引用。资源是通过专门的函数来建立和使用的。所有这些函数及其相应资源类型见<a href="/resource.html" class="link">附录</a>。

参见 <span class="function">get\_resource\_type</span>。

### 转换为资源

由于资源类型变量保存有为打开文件、数据库连接、图形画布区域等的特殊句柄，因此将其它类型的值转换为资源没有意义。

### 释放资源

引用计数系统是 Zend 引擎的一部分，可以自动检测到一个资源不再被引用了（和
Java
一样）。这种情况下此资源使用的所有外部资源都会被垃圾回收系统释放。因此，很少需要手工释放内存。

> **Note**: <span class="simpara">
> 持久数据库连接比较特殊，它们*不会*被垃圾回收系统销毁。参见<a href="/features/persistent-connections.html" class="link">数据库永久连接</a>一章。
> </span>

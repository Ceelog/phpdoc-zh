memcache\_debug
===============

转换调试输出的开/关

### 说明

<span class="type">bool</span> <span
class="methodname">memcache\_debug</span> ( <span
class="methodparam"><span class="type">bool</span> `$on_off`</span> )

<span class="function">memcache\_debug</span>在参数
`on_off`设置为**`true`**时打开调试输出，在值为
**`false`**时关闭调试输出。

> **Note**:
>
> <span
> class="function">memcache\_debug</span>仅仅在PHP以--enable-debug方式编译时可以访问，并且
> 总是返回**`true`**，其他情况下此函数不会产生任何影响并总是返回**`false`**。

### 参数

`on_off`  
**`true`**表明打开调试输出。 **`false`**表明关闭调试输出。

### 返回值

当PHP以--enalbe-debug选项构建时返回**`true`**其他情况下返回**`false`**。

**目录**

-   [memcache\_debug](/ref/memcache.html#memcache_debug) —
    转换调试输出的开/关

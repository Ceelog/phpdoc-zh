fastcgi\_finish\_request
========================

冲刷(flush)所有响应的数据给客户端

### 说明

<span class="type">bool</span> <span
class="methodname">fastcgi\_finish\_request</span> ( <span
class="methodparam">void</span> )

此函数冲刷(flush)所有响应的数据给客户端并结束请求。
这使得客户端结束连接后，需要大量时间运行的任务能够继续运行。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

**目录**

-   [fastcgi\_finish\_request](/ref/fpm.html#fastcgi_finish_request) —
    冲刷(flush)所有响应的数据给客户端

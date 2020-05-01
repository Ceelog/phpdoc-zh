预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`COUNTER_FLAG_PERSIST`** (<span class="type">integer</span>)  
<span class="simpara"> 有此标志的计数器会作为持久化资源进行创建。
</span>

**`COUNTER_FLAG_SAVE`** (<span class="type">integer</span>)  
<span class="simpara"> 有此标志的计数器会在启动 PHP 间保存。 </span>

**`COUNTER_FLAG_NO_OVERWRITE`** (<span class="type">integer</span>)  
<span class="simpara"> 此标志触发 <span
class="function">counter\_create</span>
函数以避免覆盖一个名称已存在的计数器而创建一个新的。 </span>

**`COUNTER_META_NAME`** (<span class="type">string</span>)  
<span class="simpara"> 传递此常量以获取计数器资源/对象的名称。 </span>

**`COUNTER_META_IS_PERISTENT`** (<span class="type">string</span>)  
<span class="simpara"> 传递此常量来指定计数器资源/对象进行持久化 (有
**`COUNTER_FLAG_PERSIST`** 标志) </span>

**`COUNTER_RESET_NEVER`** (<span class="type">integer</span>)  
<span class="simpara"> 此计数器不会被重置。 </span>

**`COUNTER_RESET_PER_LOAD`** (<span class="type">integer</span>)  
<span class="simpara"> 此计数器每次启动 PHP 时都会被重置。 </span>

**`COUNTER_RESET_PER_REQUEST`** (<span class="type">integer</span>)  
<span class="simpara"> 此计数器每次请求时都会被重置。 </span>

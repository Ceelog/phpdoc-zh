预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`PTHREADS_INHERIT_ALL`** (<span class="type">integer</span>)  
<span class="simpara"> 线程的默认选项。线程开始的时候，pthreads
扩展会将环境复制到线程上下文中。 </span>

**`PTHREADS_INHERIT_NONE`** (<span class="type">integer</span>)  
<span class="simpara"> 新线程开始时，不继承任何内容。 </span>

**`PTHREADS_INHERIT_INI`** (<span class="type">integer</span>)  
<span class="simpara"> 新线程开始时，仅继承 INI 配置。 </span>

**`PTHREADS_INHERIT_CONSTANTS`** (<span class="type">integer</span>)  
<span class="simpara"> 新线程开始时，继承用户定义的常量。 </span>

**`PTHREADS_INHERIT_CLASSES`** (<span class="type">integer</span>)  
<span class="simpara"> 新线程开始时，继承用户定义的类。 </span>

**`PTHREADS_INHERIT_FUNCTIONS`** (<span class="type">integer</span>)  
<span class="simpara"> 新线程开始时，继承用户定义的函数。 </span>

**`PTHREADS_INHERIT_INCLUDES`** (<span class="type">integer</span>)  
<span class="simpara"> 新线程开始时，继承包含文件。 </span>

**`PTHREADS_INHERIT_COMMENTS`** (<span class="type">integer</span>)  
<span class="simpara"> 新线程开始时，继承所有的注释。 </span>

**`PTHREADS_ALLOW_HEADERS`** (<span class="type">integer</span>)  
<span class="simpara">
允许新线程向标准输出发送头信息（通常情况下是被禁止的）。 </span>

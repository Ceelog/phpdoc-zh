运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名称                   | 默认值                       | 可变性        | 修改日志 |
|------------------------|------------------------------|---------------|----------|
| counter.reset\_time    | COUNTER\_RESET\_PER\_REQUEST | PHP\_INI\_ALL |          |
| counter.save\_path     | ""                           | PHP\_INI\_ALL |          |
| counter.initial\_value | "0"                          | PHP\_INI\_ALL |          |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

`counter.reset_time` <span class="type">integer</span>  
<span class="simpara"> `counter.reset_time` 使 "counter"
使用简单接口进行重置。 可使用类似 **`COUNTER_RESET_*`** 的常量(见下文)。
</span>

`counter.save_path` <span class="type">string</span>  
<span class="simpara"> 告诉 "counter" 在哪保存那些在启动 PHP
间必需持久化的数据 (比如，计数器包含COUNTER\_RESET\_NEVER 或
COUNTER\_FLAG\_SAVE 选项)。一个文件将创建在此路径下，运行 PHP
的用户对此路径必须有可读写权限。 </span>

`counter.initial_value` <span class="type">integer</span>  
<span class="simpara"> 使用简单接口设置进行重置时，设定的计数器初始值。
</span>

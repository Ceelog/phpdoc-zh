预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SEASLOG_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> </span>

**`SEASLOG_AUTHOR`** (<span class="type">string</span>)  
<span class="simpara"> </span>

**`SEASLOG_ALL`** (<span class="type">string</span>)  
<span class="simpara"> "ALL" </span>

**`SEASLOG_DEBUG`** (<span class="type">string</span>)  
<span class="simpara"> "DEBUG" - 详细的调试信息。细粒度的信息事件。
</span>

**`SEASLOG_INFO`** (<span class="type">string</span>)  
<span class="simpara"> "INFO" - 重要事件、强调应用程序的运行过程。
</span>

**`SEASLOG_NOTICE`** (<span class="type">string</span>)  
<span class="simpara"> "NOTICE" -
一般重要性事件、执行过程中较INFO级别更为重要的信息。 </span>

**`SEASLOG_WARNING`** (<span class="type">string</span>)  
<span class="simpara"> "WARNING" -
出现了非错误性的异常信息、潜在异常信息、需要关注并且需要修复。 </span>

**`SEASLOG_ERROR`** (<span class="type">string</span>)  
<span class="simpara"> "ERROR" -
运行时出现的错误，不需要立刻采取行动，但必须记录下来以备检测。 </span>

**`SEASLOG_CRITICAL`** (<span class="type">string</span>)  
<span class="simpara"> "CRITICAL" -
紧急情况、需要立刻进行修复、程序组件已经不可用。 </span>

**`SEASLOG_ALERT`** (<span class="type">string</span>)  
<span class="simpara"> "ALERT" -
必级立即采取行动的紧急事件、需要立即通知相关人员紧急修复。 </span>

**`SEASLOG_EMERGENCY`** (<span class="type">string</span>)  
<span class="simpara"> "EMERGENCY" - 系统不可用。 </span>

**`SEASLOG_DETAIL_ORDER_ASC`** (<span class="type">integer</span>)  
<span class="simpara"> 1 </span>

**`SEASLOG_DETAIL_ORDER_DESC`** (<span class="type">integer</span>)  
<span class="simpara"> 2 </span>

**`SEASLOG_APPENDER_FILE`** (<span class="type">integer</span>)  
<span class="simpara"> 1 </span>

**`SEASLOG_APPENDER_TCP`** (<span class="type">integer</span>)  
<span class="simpara"> 2 </span>

**`SEASLOG_APPENDER_UDP`** (<span class="type">integer</span>)  
<span class="simpara"> 3 </span>

**`SEASLOG_CLOSE_LOGGER_STREAM_MOD_ALL`** (<span class="type">integer</span>)  
<span class="simpara"> 1 </span>

**`SEASLOG_CLOSE_LOGGER_STREAM_MOD_ASSIGN`** (<span class="type">integer</span>)  
<span class="simpara"> 2 </span>

**`SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT`** (<span class="type">integer</span>)  
<span class="simpara"> 1 </span>

**`SEASLOG_REQUEST_VARIABLE_REQUEST_URI`** (<span class="type">integer</span>)  
<span class="simpara"> 2 </span>

**`SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD`** (<span class="type">integer</span>)  
<span class="simpara"> 3 </span>

**`SEASLOG_REQUEST_VARIABLE_CLIENT_IP`** (<span class="type">integer</span>)  
<span class="simpara"> 4 </span>

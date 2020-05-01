预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SID`** (<span class="type">string</span>)  
<span class="simpara"> 包含着会话名以及会话 ID 的常量，格式为
*"name=ID"*，或者如果会话 ID 已经在适当的会话 cookie
中设定时则为空字符串。 这和 <span class="function">session\_id</span>
返回的是同一个 ID。 </span>

**`PHP_SESSION_DISABLED`** (<span class="type">int</span>)  
<span class="simpara"> 自 PHP 5.4.0 起。如果会话已禁用则返回 <span
class="function">session\_status</span> 的值。 </span>

**`PHP_SESSION_NONE`** (<span class="type">int</span>)  
<span class="simpara"> 自 PHP 5.4.0
起。在会话已启用但是没有会话的时候返回 <span
class="function">session\_status</span> 的值。 </span>

**`PHP_SESSION_ACTIVE`** (<span class="type">int</span>)  
<span class="simpara"> 自 PHP 5.4.0 起。在一个会话已启用并存在时返回
<span class="function">session\_status</span> 的值。 </span>

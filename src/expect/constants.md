预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`EXP_GLOB`** (<span class="type">integer</span>)  
<span class="simpara"> Indicates that the pattern is a glob-style string
pattern. </span>

**`EXP_EXACT`** (<span class="type">integer</span>)  
<span class="simpara"> Indicates that the pattern is an exact string.
</span>

**`EXP_REGEXP`** (<span class="type">integer</span>)  
<span class="simpara"> Indicates that the pattern is a regexp-style
string pattern. </span>

**`EXP_EOF`** (<span class="type">integer</span>)  
<span class="simpara"> Value, returned by <span
class="function">expect\_expectl</span>, when EOF is reached. </span>

**`EXP_TIMEOUT`** (<span class="type">integer</span>)  
<span class="simpara"> Value, returned by <span
class="function">expect\_expectl</span> upon timeout of seconds,
specified in value of
<a href="/expect/setup.html#" class="link">expect.timeout</a> </span>

**`EXP_FULLBUFFER`** (<span class="type">integer</span>)  
<span class="simpara"> Value, returned by <span
class="function">expect\_expectl</span> if no pattern have been matched.
</span>

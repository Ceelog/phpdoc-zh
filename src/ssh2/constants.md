预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`SSH2_FINGERPRINT_MD5`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span
class="function">ssh2\_fingerprint</span> requesting hostkey fingerprint
as an MD5 hash. </span>

**`SSH2_FINGERPRINT_SHA1`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span
class="function">ssh2\_fingerprint</span> requesting hostkey fingerprint
as an SHA1 hash. </span>

**`SSH2_FINGERPRINT_HEX`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span
class="function">ssh2\_fingerprint</span> requesting hostkey fingerprint
as a string of hexits. </span>

**`SSH2_FINGERPRINT_RAW`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span
class="function">ssh2\_fingerprint</span> requesting hostkey fingerprint
as a raw string of 8-bit characters. </span>

**`SSH2_TERM_UNIT_CHARS`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span class="function">ssh2\_shell</span>
specifying that `width` and `height` are provided as character sizes.
</span>

**`SSH2_TERM_UNIT_PIXELS`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span class="function">ssh2\_shell</span>
specifying that `width` and `height` are provided in pixel units.
</span>

**`SSH2_DEFAULT_TERM_WIDTH`** (<span class="type">int</span>)  
<span class="simpara"> Default terminal width requested by <span
class="function">ssh2\_shell</span>. </span>

**`SSH2_DEFAULT_TERM_HEIGHT`** (<span class="type">int</span>)  
<span class="simpara"> Default terminal height requested by <span
class="function">ssh2\_shell</span>. </span>

**`SSH2_DEFAULT_TERM_UNIT`** (<span class="type">int</span>)  
<span class="simpara"> Default terminal units requested by <span
class="function">ssh2\_shell</span>. </span>

**`SSH2_STREAM_STDIO`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span
class="function">ssh2\_fetch\_stream</span> requesting STDIO subchannel.
</span>

**`SSH2_STREAM_STDERR`** (<span class="type">int</span>)  
<span class="simpara"> Flag to <span
class="function">ssh2\_fetch\_stream</span> requesting STDERR
subchannel. </span>

**`SSH2_DEFAULT_TERMINAL`** (<span class="type">string</span>)  
<span class="simpara"> Default terminal type (e.g. vt102, ansi, xterm,
vanilla) requested by <span class="function">ssh2\_shell</span>. </span>

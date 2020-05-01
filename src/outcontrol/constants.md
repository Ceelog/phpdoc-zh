预定义常量
==========

下列常量作为 PHP 核心的一部分总是可用的。

**`PHP_OUTPUT_HANDLER_START`** (<span class="type">integer</span>)  
Indicates that output buffering has begun.

**`PHP_OUTPUT_HANDLER_WRITE`** (<span class="type">integer</span>)  
Indicates that the output buffer is being flushed, and had data to
output.

Available since PHP 5.4.

**`PHP_OUTPUT_HANDLER_FLUSH`** (<span class="type">integer</span>)  
Indicates that the buffer has been flushed.

Available since PHP 5.4.

**`PHP_OUTPUT_HANDLER_CLEAN`** (<span class="type">integer</span>)  
Indicates that the output buffer has been cleaned.

Available since PHP 5.4.

**`PHP_OUTPUT_HANDLER_FINAL`** (<span class="type">integer</span>)  
Indicates that this is the final output buffering operation.

Available since PHP 5.4.

**`PHP_OUTPUT_HANDLER_CONT`** (<span class="type">integer</span>)  
Indicates that the buffer has been flushed, but output buffering will
continue.

As of PHP 5.4, this is an alias for **`PHP_OUTPUT_HANDLER_WRITE`**.

**`PHP_OUTPUT_HANDLER_END`** (<span class="type">integer</span>)  
Indicates that output buffering has ended.

As of PHP 5.4, this is an alias for **`PHP_OUTPUT_HANDLER_FINAL`**.

**`PHP_OUTPUT_HANDLER_CLEANABLE`** (<span class="type">integer</span>)  
Controls whether an output buffer created by <span
class="function">ob\_start</span> can be cleaned.

Available since PHP 5.4.

**`PHP_OUTPUT_HANDLER_FLUSHABLE`** (<span class="type">integer</span>)  
Controls whether an output buffer created by <span
class="function">ob\_start</span> can be flushed.

Available since PHP 5.4.

**`PHP_OUTPUT_HANDLER_REMOVABLE`** (<span class="type">integer</span>)  
Controls whether an output buffer created by <span
class="function">ob\_start</span> can be removed before the end of the
script.

Available since PHP 5.4.

**`PHP_OUTPUT_HANDLER_STDFLAGS`** (<span class="type">integer</span>)  
The default set of output buffer flags; currently equivalent to
**`PHP_OUTPUT_HANDLER_CLEANABLE`** \| **`PHP_OUTPUT_HANDLER_FLUSHABLE`**
\| **`PHP_OUTPUT_HANDLER_REMOVABLE`**.

Available since PHP 5.4.

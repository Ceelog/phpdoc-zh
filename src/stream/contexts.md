Stream Contexts
===============

A *context* is a set of *parameters* and wrapper specific *options*
which modify or enhance the behavior of a stream. *Contexts* are created
using <span class="function">stream\_context\_create</span> and can be
passed to most filesystem related stream creation functions (i.e. <span
class="function">fopen</span>, <span class="function">file</span>, <span
class="function">file\_get\_contents</span>, etc...).

*Options* can be specified when calling <span
class="function">stream\_context\_create</span>, or later using <span
class="function">stream\_context\_set\_option</span>. A list of wrapper
specific *options* can be found in the
<a href="/context.html" class="xref">上下文（Context）选项和参数</a>
chapter.

*Parameters* can be specified for *contexts* using the <span
class="function">stream\_context\_set\_params</span> function.

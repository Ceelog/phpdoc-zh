预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`XSL_CLONE_AUTO`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`XSL_CLONE_NEVER`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`XSL_CLONE_ALWAYS`** (<span class="type">int</span>)  
<span class="simpara"> </span>

**`LIBXSLT_VERSION`** (<span class="type">int</span>)  
<span class="simpara"> libxslt version like 10117. Available as of PHP
5.1.2. </span>

**`LIBXSLT_DOTTED_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> libxslt version like 1.1.17. Available as of PHP
5.1.2. </span>

**`LIBEXSLT_VERSION`** (<span class="type">int</span>)  
<span class="simpara"> libexslt version like 813. Available as of PHP
5.1.2. </span>

**`LIBEXSLT_DOTTED_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> libexslt version like 1.1.17. Available as of PHP
5.1.2. </span>

**`XSL_SECPREF_NONE`** (<span class="type">int</span>)  
<span class="simpara">Deactivate all security restrictions. </span>

**`XSL_SECPREF_READ_FILE`** (<span class="type">int</span>)  
<span class="simpara"> Disallows reading files. </span>

**`XSL_SECPREF_WRITE_FILE`** (<span class="type">int</span>)  
<span class="simpara"> Disallows writing files. </span>

**`XSL_SECPREF_CREATE_DIRECTORY`** (<span class="type">int</span>)  
<span class="simpara"> Disallows creating directories. </span>

**`XSL_SECPREF_READ_NETWORK`** (<span class="type">int</span>)  
<span class="simpara"> Disallows reading network files. </span>

**`XSL_SECPREF_WRITE_NETWORK`** (<span class="type">int</span>)  
<span class="simpara"> Disallows writing network files. </span>

**`XSL_SECPREF_DEFAULT`** (<span class="type">int</span>)  
<span class="simpara"> Disallows all write access, i.e. a bitmask of
**`XSL_SECPREF_WRITE_NETWORK`** \| **`XSL_SECPREF_CREATE_DIRECTORY`** \|
**`XSL_SECPREF_WRITE_FILE`**. </span>

预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`LIBXML_BIGLINES`** (<span class="type">integer</span>)  
<span class="simpara"> Allows line numbers greater than 65535 to be
reported correctly. </span>

> **Note**:
>
> Only available as of PHP 7.0.0 with Libxml \>= 2.9.0

**`LIBXML_COMPACT`** (<span class="type">integer</span>)  
<span class="simpara"> Activate small nodes allocation optimization.
This may speed up your application without needing to change the code.
</span>

> **Note**:
>
> Only available in Libxml \>= 2.6.21

**`LIBXML_DTDATTR`** (<span class="type">integer</span>)  
<span class="simpara"> Default DTD attributes </span>

**`LIBXML_DTDLOAD`** (<span class="type">integer</span>)  
<span class="simpara"> Load the external subset </span>

**`LIBXML_DTDVALID`** (<span class="type">integer</span>)  
<span class="simpara"> Validate with the DTD </span>

**`LIBXML_HTML_NOIMPLIED`** (<span class="type">integer</span>)  
<span class="simpara"> Sets HTML\_PARSE\_NOIMPLIED flag, which turns off
the automatic adding of implied html/body... elements. </span>

> **Note**:
>
> Only available in Libxml \>= 2.7.7 (as of PHP \>= 5.4.0)

**`LIBXML_HTML_NODEFDTD`** (<span class="type">integer</span>)  
<span class="simpara"> Sets HTML\_PARSE\_NODEFDTD flag, which prevents a
default doctype being added when one is not found. </span>

> **Note**:
>
> Only available in Libxml \>= 2.7.8 (as of PHP \>= 5.4.0)

**`LIBXML_NOBLANKS`** (<span class="type">integer</span>)  
<span class="simpara"> Remove blank nodes </span>

**`LIBXML_NOCDATA`** (<span class="type">integer</span>)  
<span class="simpara"> Merge CDATA as text nodes </span>

**`LIBXML_NOEMPTYTAG`** (<span class="type">integer</span>)  
<span class="simpara"> Expand empty tags (e.g. *\<br/\>* to
*\<br\>\</br\>*) </span>

> **Note**:
>
> This option is currently just available in the
> <a href="/class/domdocument.html#DOMDocument::save" class="xref"></a>
> and
> <a href="/class/domdocument.html#DOMDocument::saveXML" class="xref"></a>
> functions.

**`LIBXML_NOENT`** (<span class="type">integer</span>)  
<span class="simpara"> Substitute entities </span>

**`LIBXML_NOERROR`** (<span class="type">integer</span>)  
<span class="simpara"> Suppress error reports </span>

**`LIBXML_NONET`** (<span class="type">integer</span>)  
<span class="simpara"> Disable network access when loading documents
</span>

**`LIBXML_NOWARNING`** (<span class="type">integer</span>)  
<span class="simpara"> Suppress warning reports </span>

**`LIBXML_NOXMLDECL`** (<span class="type">integer</span>)  
<span class="simpara"> Drop the XML declaration when saving a document
</span>

> **Note**:
>
> Only available in Libxml \>= 2.6.21

**`LIBXML_NSCLEAN`** (<span class="type">integer</span>)  
<span class="simpara"> Remove redundant namespace declarations </span>

**`LIBXML_PARSEHUGE`** (<span class="type">integer</span>)  
<span class="simpara"> Sets XML\_PARSE\_HUGE flag, which relaxes any
hardcoded limit from the parser. This affects limits like maximum depth
of a document or the entity recursion, as well as limits of the size of
text nodes. </span>

> **Note**:
>
> Only available in Libxml \>= 2.7.0 (as of PHP \>= 5.3.2 and PHP \>=
> 5.2.12)

**`LIBXML_PEDANTIC`** (<span class="type">integer</span>)  
<span class="simpara"> Sets XML\_PARSE\_PEDANTIC flag, which enables
pedantic error reporting. </span>

> **Note**:
>
> Available as of PHP \>= 5.4.0

**`LIBXML_XINCLUDE`** (<span class="type">integer</span>)  
<span class="simpara"> Implement XInclude substitution </span>

**`LIBXML_ERR_ERROR`** (<span class="type">integer</span>)  
<span class="simpara"> A recoverable error </span>

**`LIBXML_ERR_FATAL`** (<span class="type">integer</span>)  
<span class="simpara"> A fatal error </span>

**`LIBXML_ERR_NONE`** (<span class="type">integer</span>)  
<span class="simpara"> No errors </span>

**`LIBXML_ERR_WARNING`** (<span class="type">integer</span>)  
<span class="simpara"> A simple warning </span>

**`LIBXML_VERSION`** (<span class="type">integer</span>)  
<span class="simpara"> libxml version like 20605 or 20617 </span>

**`LIBXML_DOTTED_VERSION`** (<span class="type">string</span>)  
<span class="simpara"> libxml version like 2.6.5 or 2.6.17 </span>

**`LIBXML_SCHEMA_CREATE`** (<span class="type">integer</span>)  
<span class="simpara"> Create default/fixed value nodes during XSD
schema validation </span>

> **Note**:
>
> Only available in Libxml \>= 2.6.14 (as of PHP \>= 5.5.2)

Stream Filters
==============

A *filter* is a final piece of code which may perform operations on data
as it is being read from or written to a stream. Any number of filters
may be stacked onto a stream. Custom filters can be defined in a PHP
script using <span class="function">stream\_filter\_register</span> or
in an extension using the API Reference in
<a href="/internals2/streams.html" class="xref">流的使用</a>. To access
the list of currently registered filters, use <span
class="function">stream\_get\_filters</span>.

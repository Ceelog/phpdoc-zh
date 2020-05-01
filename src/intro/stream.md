Streams are the way of generalizing file, network, data compression, and
other operations which share a common set of functions and uses. In its
simplest definition, a *stream* is a *resource* object which exhibits
streamable behavior. That is, it can be read from or written to in a
linear fashion, and may be able to <span class="function">fseek</span>
to an arbitrary location within the stream.

A *wrapper* is additional code which tells the stream how to handle
specific protocols/encodings. For example, the *http* wrapper knows how
to translate a URL into an *HTTP/1.0* request for a file on a remote
server. There are many wrappers built into PHP by default (See
<a href="/wrappers.html" class="xref">支持的协议和封装协议</a>), and
additional, custom wrappers may be added either within a PHP script
using <span class="function">stream\_wrapper\_register</span>, or
directly from an extension using the API Reference in
<a href="/internals2/streams.html" class="xref">流的使用</a>. Because
any variety of wrapper may be added to PHP, there is no set limit on
what can be done with them. To access the list of currently registered
wrappers, use <span class="function">stream\_get\_wrappers</span>.

A stream is referenced as: `scheme`://`target`

-   <span class="simpara"> `scheme`(string) - The name of the wrapper to
    be used. Examples include: file, http, https, ftp, ftps,
    compress.zlib, compress.bz2, and php. See
    <a href="/wrappers.html" class="xref">支持的协议和封装协议</a> for a
    list of PHP built-in wrappers. If no wrapper is specified, the
    function default is used (typically *file*://). </span>
-   <span class="simpara"> `target` - Depends on the wrapper used. For
    filesystem related streams this is typically a path and filename of
    the desired file. For network related streams this is typically a
    hostname, often with a path appended. Again, see
    <a href="/wrappers.html" class="xref">支持的协议和封装协议</a> for a
    description of targets for built-in streams. </span>

> **Note**:
>
> Information on using streams within the PHP source code can be found
> in the
> <a href="/internals2/ze1/streams.html" class="link">Streams API for PHP Extension Authors reference</a>.

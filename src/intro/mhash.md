These functions are intended to work with
<a href="http://mhash.sourceforge.net/" class="link external">» mhash</a>.
Mhash can be used to create checksums, message digests, message
authentication codes, and more.

This is an interface to the mhash library. Mhash supports a wide variety
of hash algorithms such as MD5, SHA1, GOST, and many others. For a
complete list of supported hashes, refer to the
<a href="/mhash/constants.html" class="link">constants page</a>. The
general rule is that you can access the hash algorithm from PHP with
**`MHASH_hashname`**. For example, to access TIGER you use the PHP
constant **`MHASH_TIGER`**.

> **Note**:
>
> This extension is obsoleted by
> <a href="/book/hash.html" class="link">Hash</a>.

> **Note**:
>
> As of PHP 7.0.0 the Mhash extension has been fully integrated into the
> <a href="/book/hash.html" class="link">Hash</a> extension. Therefore,
> it is no longer possible to detect Mhash support with <span
> class="function">extension\_loaded</span>; use <span
> class="function">function\_exists</span> instead. Furthermore, Mhash
> is no longer reported by <span
> class="function">get\_loaded\_extensions</span> and related features.

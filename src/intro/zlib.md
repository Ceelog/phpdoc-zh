This module enables you to transparently read and write gzip (.gz)
compressed files, through versions of most of the
<a href="/book/filesystem.html" class="link">filesystem</a> functions
which work with gzip-compressed files (and uncompressed files, too, but
not with sockets).

> **Note**:
>
> Version 4.0.4 introduced a fopen-wrapper for `.gz`-files, so that you
> can use a special `zlib:` URL to access compressed files transparently
> using the normal f\*() file access functions if you prefix the
> filename or path with `zlib:` when calling <span
> class="function">fopen</span>. This feature requires a C runtime
> library that provides the *fopencookie()* function. Up to now the GNU
> libc seems to be the only library that provides this feature.
>
> In PHP 4.3.0, `zlib:` has been changed to `compress.zlib://` to
> prevent ambiguities with filenames containing '*:*' characters. The
> *fopencookie()* function is no longer required. More information is
> available in the section about
> <a href="/wrappers/compression.html" class="xref">zlib://</a>.

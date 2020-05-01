PHP supports the direct io functions as described in the Posix Standard
(Section 6) for performing I/O functions at a lower level than the
C-Language stream I/O functions (<span class="function">fopen</span>,
<span class="function">fread</span>,..). The use of the DIO functions
should be considered only when direct control of a device is needed. In
all other cases, the standard
<a href="/book/filesystem.html" class="link">filesystem</a> functions
are more than adequate.

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。5.1.0.

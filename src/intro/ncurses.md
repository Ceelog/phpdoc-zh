ncurses (new curses) is a free software emulation of curses in System V
Rel 4.0 (and above). It uses terminfo format, supports pads, colors,
multiple highlights, form characters and function key mapping. Because
of the interactive nature of this library, it will be of little use for
writing Web applications, but may be useful when writing scripts meant
<a href="/features/commandline.html" class="link">using PHP from the command line</a>.

The features available, such as colors, depend on the terminal that you
are using. Use functions such as <span
class="function">ncurses\_has\_colors</span>, <span
class="function">ncurses\_can\_change\_color</span>, and <span
class="function">ncurses\_has\_ic</span> to check for individual
capabilities.

> **Note**:
>
> 此扩展已被移至
> <a href="https://pecl.php.net/" class="link external">» PECL</a>
> 资源库且不再与 PHP 捆绑。5.3.0.

ncurses is available for the following platforms:

-   <span class="simpara">AIX</span>
-   <span class="simpara">BeOS</span>
-   <span class="simpara">BSD variants (FreeBSD, NetBSD, OpenBSD)</span>
-   <span class="simpara">Cygwin</span>
-   <span class="simpara">Digital Unix (aka OSF1)</span>
-   <span class="simpara">GNU/Linux</span>
-   <span class="simpara">HPUX</span>
-   <span class="simpara">IRIX64</span>
-   <span class="simpara">macOS</span>
-   <span class="simpara">OS/2</span>
-   <span class="simpara">QNX</span>
-   <span class="simpara">SCO OpenServer</span>
-   <span class="simpara">Solaris</span>
-   <span class="simpara">Tru64</span>

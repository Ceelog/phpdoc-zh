**小贴士**

PHP also supports regular expressions using a Perl-compatible syntax
using the <a href="/book/pcre.html" class="link">PCRE functions</a>.
Those functions support non-greedy matching, assertions, conditional
subpatterns, and a number of other features not supported by the
POSIX-extended regular expression syntax.

**Warning**

These regular expression functions are not binary-safe. The
<a href="/book/pcre.html" class="link">PCRE functions</a> are.

> **Note**:
>
> 从PHP5.3.0开始本扩展不再建议使用，所有调用本扩展中函数都将提示**`E_DEPRECATED`**
> 错误。

Regular expressions are used for complex string manipulation. PHP uses
the POSIX extended regular expressions as defined by POSIX 1003.2. For a
full description of POSIX regular expressions see the
<a href="http://www.tin.org/bin/man.cgi?section=7&amp;topic=regex" class="link external">» regex man pages</a>
included in the regex directory in the PHP distribution. It's in manpage
format, so you'll want to do something along the lines of **man
/usr/local/src/regex/regex.7** in order to read it.

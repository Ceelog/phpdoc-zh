范例
====

Howto start?

-   <span class="simpara">get a radius resource</span>
-   <span class="simpara">configure the library</span>
-   <span class="simpara">create the request</span>
-   <span class="simpara">put attributes</span>
-   <span class="simpara">send the request</span>
-   <span class="simpara">receive attributes</span>
-   <span class="simpara">close the radius resource (optional)</span>

Take also a look at the examples in this package.

The package contains an example php script. This script demonstrates
howto authenticate with radius using PAP or CHAP (md5). If you
authenticate with Microsoft Radius servers then its not possible to use
CHAP (md5). If you would like to authenticate with Microsoft Servers you
have to use MS-CHAPv1 or MS-CHAPv2, but its more complicated, because
you need md4, sha1 and des to generate the right data. The enclosed
examples demonstrate all authentication-methods, including MS-CHAPv1 and
MS-CHAPv2. To get the MS-CHAP to work you need the
<a href="/ref/mcrypt.html" class="link">mcrypt</a> and the
<a href="/ref/mhash.html" class="link">mhash</a> extension, starting
with version 1.2 of the package, the mcrypt extension is no longer
needed.

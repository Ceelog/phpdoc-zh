Creating Phar Archives
======================

**目录**

-   [Creating Phar Archives:
    Introduction](/phar/creating.html#Creating%20Phar%20Archives:%20Introduction)

Creating Phar Archives: Introduction
------------------------------------

To be written fully in the near future. Before reading this, be sure to
read
<a href="/phar/using.html" class="link">How to use Phar Archives</a>.

A great place to start is by reading about <span
class="function">Phar::buildFromIterator</span>, and the specifics of
the <a href="/phar/fileformat.html" class="link">file format</a> choices
available for archives. A healthy understanding of what a stub is and
does is crucial to phar archive creation, and so <span
class="function">Phar::setStub</span> and <span
class="function">Phar::createDefaultStub</span> are good places to start
as well. If you are distributing a web-based application, it is crucial
to know about <span class="function">Phar::webPhar</span> and related
method <span class="function">Phar::mungServer</span>. Any application
that accesses its own files should also consider using <span
class="function">Phar::interceptFileFuncs</span>.

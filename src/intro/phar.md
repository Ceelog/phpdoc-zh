The phar extension provides a way to put entire PHP applications into a
single file called a "phar" (PHP Archive) for easy distribution and
installation. In addition to providing this service, the phar extension
also provides a file-format abstraction method for creating and
manipulating tar and zip files through the <span
class="classname">PharData</span> class, much as PDO provides a unified
interface for accessing different databases. Unlike PDO, which cannot
convert between different databases, Phar also can convert between tar,
zip and phar file formats with a single line of code. see <span
class="function">Phar::convertToExecutable</span> for one example.

What is phar? Phar archives are best characterized as a convenient way
to group several files into a single file. As such, a phar archive
provides a way to distribute a complete PHP application in a single file
and run it from that file without the need to extract it to disk.
Additionally, phar archives can be executed by PHP as easily as any
other file, both on the commandline and from a web server. Phar is kind
of like a thumb drive for PHP applications.

Phar implements this functionality through a
<a href="/book/stream.html" class="link">Stream Wrapper</a>. Normally,
to use an external file within a PHP script, you would use <span
class="function">include</span>

**示例 \#1 Using an external file**

``` php
<?php
 include '/path/to/external/file.php';
 ?>
```

PHP can be thought of as actually translating
*/path/to/external/file.php* into a stream wrapper as
*file:///path/to/external/file.php*, and under the hood it does in fact
use the plain file stream wrapper stream functions to access all local
files.

To use a file named *file.php* contained with a phar archive
*/path/to/myphar.phar*, the syntax is very similar to the *file://*
syntax above.

**示例 \#2 Using a file within a phar archive**

``` php
<?php
 include 'phar:///path/to/myphar.phar/file.php';
 ?>
```

In fact, one can treat a phar archive exactly as if it were an external
disk, using any of <span class="function">fopen</span>-related
functions, <span class="function">opendir</span> and <span
class="function">mkdir</span>-related functions to read, change, or
create new files and directories within the phar archive. This allows
complete PHP applications to be distributed in a single file and run
directly from that file.

The most common usage for a phar archive is to distribute a complete
application in a single file. For instance, the PEAR Installer that is
bundled with PHP versions is distributed as a phar archive. To use a
phar archive distributed in this way, the archive can be executed on the
command-line or via a web server.

Phar archives can be distributed as *tar* archives, *zip* archives, or
as the custom *phar* file format designed specifically for the phar
extension. Each file format has advantages and disadvantages. The tar
and zip file formats can be read or extracted by any third-party tool
that can read the format, but require the phar extension in order to run
with PHP. The phar file format is customized and unique to the phar
extension, and can only be created by the phar extension or the PEAR
package
<a href="https://pear.php.net/package/PHP_Archive" class="link external">» PHP_Archive</a>,
but has the advantage that applications created in this format will run
even if the phar extension is not enabled.

In other words, even with the phar extension disabled, one can execute
or include a phar-based archive. Accessing individual files within a
phar archive is only possible with the phar extension unless the phar
archive was created by PHP\_Archive.

The phar extension is also capable of converting a phar archive from tar
to zip or to phar file format in a single command:

**示例 \#3 Converting a phar archive from phar to tar file format**

``` php
<?php
 $phar = new Phar('myphar.phar');
 $pgz = $phar->convertToExecutable(Phar::TAR, Phar::GZ); // makes myphar.phar.tar.gz
 ?>
```

Phar can compress individual files or an entire archive using
<a href="/book/zlib.html" class="link">gzip</a> compression or
<a href="/book/bzip2.html" class="link">bzip2</a> compression, and can
verify archive integrity automatically through the use of MD5, SHA-1,
SHA-256 or SHA-512 signatures.

Lastly, the Phar extension is security-conscious, and disables write
access to executable phar archives by default, and requires system-level
disabling of the *phar.readonly* php.ini setting in order to create or
modify phar archives. Normal tar and zip archives without an executable
stub can always be created or modified using the <span
class="classname">PharData</span> class.

If you are creating applications for distribution, you will want to read
<a href="/phar/creating.html" class="link">How to create Phar Archives</a>.
If you want more information on the differences between the three file
formats that phar supports, you should read
<a href="/phar/fileformat.html" class="link">Phar, Tar and Zip</a>.

If you are using phar applications, there are helpful tips in
<a href="/phar/using.html" class="link">How to use Phar Archives</a>

The word *phar* is a portmanteau of *PHP* and *Archive* and is based
loosely on the *jar* (Java Archive) familiar to Java developers.

The implementation for Phar archives is based on the PEAR package
<a href="https://pear.php.net/package/PHP_Archive" class="link external">» PHP_Archive</a>,
and the implementation details are similar, although the Phar extension
is much more powerful. In addition, the Phar extension allows most PHP
applications to be run unmodified while PHP\_Archive-based phar archives
often require extensive modification in order to work.

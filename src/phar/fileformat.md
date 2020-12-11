What makes a phar a phar and not a tar or a zip?
================================================

**目录**

-   [Ingredients of all Phar archives, independent of file
    format](/phar/fileformat.html#Ingredients%20of%20all%20Phar%20archives,%20independent%20of%20file%20format)
-   [Phar file stub](/phar/fileformat.html#Phar%20file%20stub)
-   [Head-to-head comparison of Phar, Tar and
    Zip](/phar/fileformat.html#Head-to-head%20comparison%20of%20Phar,%20Tar%20and%20Zip)
-   [Tar-based phars](/phar/fileformat.html#Tar-based%20phars)
-   [Zip-based phars](/phar/fileformat.html#Zip-based%20phars)
-   [Phar File Format](/phar/fileformat.html#Phar%20File%20Format)
-   [Global Phar bitmapped
    flags](/phar/fileformat.html#Global%20Phar%20bitmapped%20flags)
-   [Phar manifest file entry
    definition](/phar/fileformat.html#Phar%20manifest%20file%20entry%20definition)
-   [Phar Signature
    format](/phar/fileformat.html#Phar%20Signature%20format)

Ingredients of all Phar archives, independent of file format
------------------------------------------------------------

All Phar archives contain three to four sections:

1.  a stub

2.  a manifest describing the contents

3.  the file contents

4.  \[optional\] a signature for verifying Phar integrity (phar file
    format only)

Phar file stub
--------------

A Phar's stub is a simple PHP file. The smallest possible stub follows:

``` php
<?php __HALT_COMPILER();
```

A stub must contain as a minimum, the *\_\_HALT\_COMPILER();* token at
its conclusion. Typically, a stub will contain loader functionality like
so:

``` php
<?php
Phar::mapPhar();
include 'phar://myphar.phar/index.php';
__HALT_COMPILER();
```

There are no restrictions on the contents of a Phar stub, except for the
requirement that it conclude with *\_\_HALT\_COMPILER();*. The closing
PHP tag

    ?>

may be included or omitted, but there can be no more than 1 space
between the *;* and the close tag

    ?>

or the phar extension will be unable to process the Phar archive's
manifest.

In a tar or zip-based phar archive, the stub is stored in the
*.phar/stub.php* file. The default stub for phar-based Phar archives
contains approximately 7k of code to extract the contents of the phar
and execute them. See <span
class="function">Phar::createDefaultStub</span> for more detail.

The phar alias is stored in a tar or zip-based phar archive in the
*.phar/alias.txt* file as plain text.

Head-to-head comparison of Phar, Tar and Zip
--------------------------------------------

What are the good and the bad things about the three supported file
formats in the phar extension? This table attempts to address that
question.

| Feature                                                                                               | Phar | Tar | Zip              |
|-------------------------------------------------------------------------------------------------------|------|-----|------------------|
| Standard File Format                                                                                  | No   | Yes | Yes              |
| Can be executed without the Phar Extension <a href="/phar/fileformat.html#" class="link">[1]</a>      | Yes  | No  | No               |
| Per-file compression                                                                                  | Yes  | No  | Yes              |
| Whole-archive compression                                                                             | Yes  | Yes | No               |
| Whole-archive signature validation                                                                    | Yes  | Yes | Yes (PHP 5.3.1+) |
| Web-specific application support                                                                      | Yes  | Yes | Yes              |
| Per-file Meta-data                                                                                    | Yes  | Yes | Yes              |
| Whole-Archive Meta-data                                                                               | Yes  | Yes | Yes              |
| Archive creation/modification <a href="/phar/fileformat.html#" class="link">[2]</a>                   | Yes  | Yes | Yes              |
| Full support for all stream wrapper functions                                                         | Yes  | Yes | Yes              |
| Can be created/modified even if phar.readonly=1 <a href="/phar/fileformat.html#" class="link">[3]</a> | No   | Yes | Yes              |

**小贴士**

\[1\] PHP can only directly access the contents of a Phar archive
without the Phar extension if it is using a *stub* that extracts the
contents of the phar archive. The stub created by <span
class="function">Phar::createDefaultStub</span> extracts the phar
archive and runs its contents from a temporary directory if no phar
extension is found.

**小贴士**

\[2\] All write access requires *phar.readonly* to be disabled in
php.ini or on the command-line directly.

**小贴士**

\[3\] Only tar and zip archives without *.phar* in their filename and
without an executable stub *.phar/stub.php* can be created if
phar.readonly=1.

Tar-based phars
---------------

Archives based on the tar file format follow the more modern USTAR file
format. The design of the tar file header makes them more efficient to
access than the zip file format, and almost as efficient as the phar
file format. File names are limited to 255 bytes, including full path
within the phar archive. There is no limit on the number of files within
a tar-based phar archive. These archives can fully compressed in gzip or
bzip2 format and still be executed by the Phar extension.

To compress an entire archive, use <span
class="function">Phar::compress</span>. To decompress an entire archive,
use <span class="function">Phar::decompress</span>.

Zip-based phars
---------------

Archives based on the zip file format support several features built
into the zip file format. Per-file and whole-archive metadata is stored
in the zip file comment and zip archive comment as a serialized string.
Pre-existing zip comments will be successfully read as a string.
Per-file compression read/write is supported with zlib DEFLATE
compression, and read access is supported with bzip2 compression. There
is no limit on the number of files within a zip-based phar archive.
Empty directories are stored in the zip archive as files with a trailing
slash like *my/directory/*

Phar File Format
----------------

The phar file format is literally laid out as
stub/manifest/contents/signature, and stores the crucial information of
what is included in the phar archive in its *manifest*.

The Phar manifest is a highly optimized format that allows per-file
specification of file compression, file permissions, and even
user-defined meta-data such as file user or group. All values greater
than 1 byte are stored in little-endian byte order, with the exception
of the API version, which for historical reasons is stored as 3 nibbles
in big-endian order.

All unused flags are reserved for future use, and must not be used to
store custom information. Use the per-file meta-data facility to store
customized information about particular files.

The basic file format of a Phar archive manifest is as follows:

| Size in bytes                          | Description                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| 4 bytes                                | Length of manifest in bytes (1 MB limit)                                            |
| 4 bytes                                | Number of files in the Phar                                                         |
| 2 bytes                                | API version of the Phar manifest (currently 1.0.0)                                  |
| 4 bytes                                | Global Phar bitmapped flags                                                         |
| 4 bytes                                | Length of Phar alias                                                                |
| ??                                     | Phar alias (length based on previous)                                               |
| 4 bytes                                | Length of Phar metadata (*0* for none)                                              |
| ??                                     | Serialized Phar Meta-data, stored in <span class="function">serialize</span> format |
| at least 24 \* number of entries bytes | entries for each file                                                               |

Global Phar bitmapped flags
---------------------------

Here are the bitmapped flags currently recognized by the Phar extension
for the global Phar flat bitmap:

| Value        | Description                                                                                 |
|--------------|---------------------------------------------------------------------------------------------|
| *0x00010000* | If set, this Phar contains a verification signature                                         |
| *0x00001000* | If set, this Phar contains at least 1 file that is compressed with zlib DEFLATE compression |
| *0x00002000* | If set, this Phar contains at least 1 file that is compressed with bzip2 compression        |

Phar manifest file entry definition
-----------------------------------

Each file in the manifest contains the following information:

| Size in bytes | Description                                                                         |
|---------------|-------------------------------------------------------------------------------------|
| 4 bytes       | Filename length in bytes                                                            |
| ??            | Filename (length specified in previous)                                             |
| 4 bytes       | Un-compressed file size in bytes                                                    |
| 4 bytes       | Unix timestamp of file                                                              |
| 4 bytes       | Compressed file size in bytes                                                       |
| 4 bytes       | CRC32 checksum of un-compressed file contents                                       |
| 4 bytes       | Bit-mapped File-specific flags                                                      |
| 4 bytes       | Serialized File Meta-data length (*0* for none)                                     |
| ??            | Serialized File Meta-data, stored in <span class="function">serialize</span> format |

Note that as of API version 1.1.1, empty directories are stored as
filenames with a trailing slash like *my/directory/*

The File-specific bitmap values recognized are:

| Value        | Description                                                                                                                                                                                             |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *0x000001FF* | These bits are reserved for defining specific file permissions of a file. Permissions are used for <span class="function">fstat</span> and can be used to recreate desired permissions upon extraction. |
| *0x00001000* | If set, this file is compressed with zlib DEFLATE compression                                                                                                                                           |
| *0x00002000* | If set, this file is compressed with bzip2 compression                                                                                                                                                  |

Phar Signature format
---------------------

Phars containing a signature always have the signature appended to the
end of the Phar archive after the loader, manifest, and file contents.
The signature formats supported at this time are MD5, SHA1, SHA256,
SHA512, and OPENSSL.

| Length in bytes | Description                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| varying         | The actual signature, 20 bytes for an SHA1 signature, 16 bytes for an MD5 signature, 32 bytes for an SHA256 signature, and 64 bytes for an SHA512 signature. The length of an OPENSSL signature depends on the size of the private key.                                                                                                                                                                            |
| 4 bytes         | Signature flags. *0x0001* is used to define an MD5 signature, *0x0002* is used to define an SHA1 signature, *0x0003* is used to define an SHA256 signature, and *0x0004* is used to define an SHA512 signature. The SHA256 and SHA512 signature support is available as of API version 1.1.0. *0x0010* is used to define an OPENSSL signature, what is available as of API version 1.1.1, if OpenSSL is available. |
| 4 bytes         | Magic *GBMB* used to define the presence of a signature.                                                                                                                                                                                                                                                                                                                                                           |

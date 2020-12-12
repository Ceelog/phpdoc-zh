Phar
====

**目录**

-   [简介](/intro/phar.html)
-   [安装／配置](/phar/setup.html)
    -   [需求](/phar/setup.html#需求)
    -   [安装](/phar/setup.html#安装)
    -   [运行时配置](/phar/setup.html#运行时配置)
    -   [资源类型](/phar/setup.html#资源类型)
-   [预定义常量](/phar/constants.html)
-   [Using Phar Archives](/phar/using.html)
    -   [Using Phar Archives:
        Introduction](/phar/using.html#Using%20Phar%20Archives:%20Introduction)
    -   [Using Phar Archives: the phar stream
        wrapper](/phar/using.html#Using%20Phar%20Archives:%20the%20phar%20stream%20wrapper)
    -   [Using Phar Archives: the Phar and PharData
        class](/phar/using.html#Using%20Phar%20Archives:%20the%20Phar%20and%20PharData%20class)
-   [Creating Phar Archives](/phar/creating.html)
    -   [Creating Phar Archives:
        Introduction](/phar/creating.html#Creating%20Phar%20Archives:%20Introduction)
-   [What makes a phar a phar and not a tar or a
    zip?](/phar/fileformat.html)
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
-   [Phar](/class/phar.html) — The Phar class
    -   [Phar::addEmptyDir](/class/phar.html#Phar::addEmptyDir) —
        添加一个空目录到 phar 档案
    -   [Phar::addFile](/class/phar.html#Phar::addFile) —
        将一个文件从文件系统添加到 phar 档案中
    -   [Phar::addFromString](/class/phar.html#Phar::addFromString) —
        以字符串的形式添加一个文件到 phar 档案
    -   [Phar::apiVersion](/class/phar.html#Phar::apiVersion) — Returns
        the api version
    -   [Phar::buildFromDirectory](/class/phar.html#Phar::buildFromDirectory)
        — Construct a phar archive from the files within a directory
    -   [Phar::buildFromIterator](/class/phar.html#Phar::buildFromIterator)
        — Construct a phar archive from an iterator
    -   [Phar::canCompress](/class/phar.html#Phar::canCompress) —
        Returns whether phar extension supports compression using either
        zlib or bzip2
    -   [Phar::canWrite](/class/phar.html#Phar::canWrite) — Returns
        whether phar extension supports writing and creating phars
    -   [Phar::compress](/class/phar.html#Phar::compress) — Compresses
        the entire Phar archive using Gzip or Bzip2 compression
    -   [Phar::compressFiles](/class/phar.html#Phar::compressFiles) —
        Compresses all files in the current Phar archive
    -   [Phar::\_\_construct](/class/phar.html#Phar::__construct) —
        Construct a Phar archive object
    -   [Phar::convertToData](/class/phar.html#Phar::convertToData) —
        Convert a phar archive to a non-executable tar or zip file
    -   [Phar::convertToExecutable](/class/phar.html#Phar::convertToExecutable)
        — Convert a phar archive to another executable phar archive file
        format
    -   [Phar::copy](/class/phar.html#Phar::copy) — Copy a file internal
        to the phar archive to another new file within the phar
    -   [Phar::count](/class/phar.html#Phar::count) — Returns the number
        of entries (files) in the Phar archive
    -   [Phar::createDefaultStub](/class/phar.html#Phar::createDefaultStub)
        — Create a phar-file format specific stub
    -   [Phar::decompress](/class/phar.html#Phar::decompress) —
        Decompresses the entire Phar archive
    -   [Phar::decompressFiles](/class/phar.html#Phar::decompressFiles)
        — Decompresses all files in the current Phar archive
    -   [Phar::delMetadata](/class/phar.html#Phar::delMetadata) —
        Deletes the global metadata of the phar
    -   [Phar::delete](/class/phar.html#Phar::delete) — 删除 phar
        档案中的一个文件
    -   [Phar::extractTo](/class/phar.html#Phar::extractTo) — Extract
        the contents of a phar archive to a directory
    -   [Phar::getAlias](/class/phar.html#Phar::getAlias) — Get the
        alias for Phar
    -   [Phar::getMetadata](/class/phar.html#Phar::getMetadata) —
        Returns phar archive meta-data
    -   [Phar::getModified](/class/phar.html#Phar::getModified) — Return
        whether phar was modified
    -   [Phar::getPath](/class/phar.html#Phar::getPath) — Get the real
        path to the Phar archive on disk
    -   [Phar::getSignature](/class/phar.html#Phar::getSignature) —
        Return MD5/SHA1/SHA256/SHA512/OpenSSL signature of a Phar
        archive
    -   [Phar::getStub](/class/phar.html#Phar::getStub) — Return the PHP
        loader or bootstrap stub of a Phar archive
    -   [Phar::getSupportedCompression](/class/phar.html#Phar::getSupportedCompression)
        — Return array of supported compression algorithms
    -   [Phar::getSupportedSignatures](/class/phar.html#Phar::getSupportedSignatures)
        — Return array of supported signature types
    -   [Phar::getVersion](/class/phar.html#Phar::getVersion) — Return
        version info of Phar archive
    -   [Phar::hasMetadata](/class/phar.html#Phar::hasMetadata) —
        Returns whether phar has global meta-data
    -   [Phar::interceptFileFuncs](/class/phar.html#Phar::interceptFileFuncs)
        — Instructs phar to intercept fopen, file\_get\_contents,
        opendir, and all of the stat-related functions
    -   [Phar::isBuffering](/class/phar.html#Phar::isBuffering) — Used
        to determine whether Phar write operations are being buffered,
        or are flushing directly to disk
    -   [Phar::isCompressed](/class/phar.html#Phar::isCompressed) —
        Returns Phar::GZ or PHAR::BZ2 if the entire phar archive is
        compressed (.tar.gz/tar.bz and so on)
    -   [Phar::isFileFormat](/class/phar.html#Phar::isFileFormat) —
        Returns true if the phar archive is based on the tar/phar/zip
        file format depending on the parameter
    -   [Phar::isValidPharFilename](/class/phar.html#Phar::isValidPharFilename)
        — Returns whether the given filename is a valid phar filename
    -   [Phar::isWritable](/class/phar.html#Phar::isWritable) — Returns
        true if the phar archive can be modified
    -   [Phar::loadPhar](/class/phar.html#Phar::loadPhar) — Loads any
        phar archive with an alias
    -   [Phar::mapPhar](/class/phar.html#Phar::mapPhar) — Reads the
        currently executed file (a phar) and registers its manifest
    -   [Phar::mount](/class/phar.html#Phar::mount) — Mount an external
        path or file to a virtual location within the phar archive
    -   [Phar::mungServer](/class/phar.html#Phar::mungServer) — Defines
        a list of up to 4 $\_SERVER variables that should be modified
        for execution
    -   [Phar::offsetExists](/class/phar.html#Phar::offsetExists) —
        Determines whether a file exists in the phar
    -   [Phar::offsetGet](/class/phar.html#Phar::offsetGet) — Gets a
        PharFileInfo object for a specific file
    -   [Phar::offsetSet](/class/phar.html#Phar::offsetSet) — Set the
        contents of an internal file to those of an external file
    -   [Phar::offsetUnset](/class/phar.html#Phar::offsetUnset) — Remove
        a file from a phar
    -   [Phar::running](/class/phar.html#Phar::running) — Returns the
        full path on disk or full phar URL to the currently executing
        Phar archive
    -   [Phar::setAlias](/class/phar.html#Phar::setAlias) — Set the
        alias for the Phar archive
    -   [Phar::setDefaultStub](/class/phar.html#Phar::setDefaultStub) —
        Used to set the PHP loader or bootstrap stub of a Phar archive
        to the default loader
    -   [Phar::setMetadata](/class/phar.html#Phar::setMetadata) — Sets
        phar archive meta-data
    -   [Phar::setSignatureAlgorithm](/class/phar.html#Phar::setSignatureAlgorithm)
        — Set the signature algorithm for a phar and apply it
    -   [Phar::setStub](/class/phar.html#Phar::setStub) — Used to set
        the PHP loader or bootstrap stub of a Phar archive
    -   [Phar::startBuffering](/class/phar.html#Phar::startBuffering) —
        Start buffering Phar write operations, do not modify the Phar
        object on disk
    -   [Phar::stopBuffering](/class/phar.html#Phar::stopBuffering) —
        Stop buffering write requests to the Phar archive, and save
        changes to disk
    -   [Phar::unlinkArchive](/class/phar.html#Phar::unlinkArchive) —
        Completely remove a phar archive from disk and from memory
    -   [Phar::webPhar](/class/phar.html#Phar::webPhar) — mapPhar for
        web-based phars. front controller for web applications
-   [PharData](/class/phardata.html) — The PharData class
    -   [PharData::addEmptyDir](/class/phardata.html#PharData::addEmptyDir)
        — Add an empty directory to the tar/zip archive
    -   [PharData::addFile](/class/phardata.html#PharData::addFile) —
        Add a file from the filesystem to the tar/zip archive
    -   [PharData::addFromString](/class/phardata.html#PharData::addFromString)
        — Add a file from the filesystem to the tar/zip archive
    -   [PharData::buildFromDirectory](/class/phardata.html#PharData::buildFromDirectory)
        — Construct a tar/zip archive from the files within a directory
    -   [PharData::buildFromIterator](/class/phardata.html#PharData::buildFromIterator)
        — Construct a tar or zip archive from an iterator
    -   [PharData::compress](/class/phardata.html#PharData::compress) —
        Compresses the entire tar/zip archive using Gzip or Bzip2
        compression
    -   [PharData::compressFiles](/class/phardata.html#PharData::compressFiles)
        — Compresses all files in the current tar/zip archive
    -   [PharData::\_\_construct](/class/phardata.html#PharData::__construct)
        — Construct a non-executable tar or zip archive object
    -   [PharData::convertToData](/class/phardata.html#PharData::convertToData)
        — Convert a phar archive to a non-executable tar or zip file
    -   [PharData::convertToExecutable](/class/phardata.html#PharData::convertToExecutable)
        — Convert a non-executable tar/zip archive to an executable phar
        archive
    -   [PharData::copy](/class/phardata.html#PharData::copy) — Copy a
        file internal to the phar archive to another new file within the
        phar
    -   [PharData::decompress](/class/phardata.html#PharData::decompress)
        — Decompresses the entire Phar archive
    -   [PharData::decompressFiles](/class/phardata.html#PharData::decompressFiles)
        — Decompresses all files in the current zip archive
    -   [PharData::delMetadata](/class/phardata.html#PharData::delMetadata)
        — Deletes the global metadata of a zip archive
    -   [PharData::delete](/class/phardata.html#PharData::delete) —
        Delete a file within a tar/zip archive
    -   [PharData::extractTo](/class/phardata.html#PharData::extractTo)
        — Extract the contents of a tar/zip archive to a directory
    -   [PharData::isWritable](/class/phardata.html#PharData::isWritable)
        — Returns true if the tar/zip archive can be modified
    -   [PharData::offsetSet](/class/phardata.html#PharData::offsetSet)
        — Set the contents of a file within the tar/zip to those of an
        external file or string
    -   [PharData::offsetUnset](/class/phardata.html#PharData::offsetUnset)
        — Remove a file from a tar/zip archive
    -   [PharData::setAlias](/class/phardata.html#PharData::setAlias) —
        Dummy function (Phar::setAlias is not valid for PharData)
    -   [PharData::setDefaultStub](/class/phardata.html#PharData::setDefaultStub)
        — Dummy function (Phar::setDefaultStub is not valid for
        PharData)
    -   [Phar::setMetadata](/class/phardata.html#Phar::setMetadata) —
        Sets phar archive meta-data
    -   [Phar::setSignatureAlgorithm](/class/phardata.html#Phar::setSignatureAlgorithm)
        — Set the signature algorithm for a phar and apply it
    -   [PharData::setStub](/class/phardata.html#PharData::setStub) —
        Dummy function (Phar::setStub is not valid for PharData)
-   [PharFileInfo](/class/pharfileinfo.html) — The PharFileInfo class
    -   [PharFileInfo::chmod](/class/pharfileinfo.html#PharFileInfo::chmod)
        — Sets file-specific permission bits
    -   [PharFileInfo::compress](/class/pharfileinfo.html#PharFileInfo::compress)
        — Compresses the current Phar entry with either zlib or bzip2
        compression
    -   [PharFileInfo::\_\_construct](/class/pharfileinfo.html#PharFileInfo::__construct)
        — Construct a Phar entry object
    -   [PharFileInfo::decompress](/class/pharfileinfo.html#PharFileInfo::decompress)
        — Decompresses the current Phar entry within the phar
    -   [PharFileInfo::delMetadata](/class/pharfileinfo.html#PharFileInfo::delMetadata)
        — Deletes the metadata of the entry
    -   [PharFileInfo::getCRC32](/class/pharfileinfo.html#PharFileInfo::getCRC32)
        — Returns CRC32 code or throws an exception if CRC has not been
        verified
    -   [PharFileInfo::getCompressedSize](/class/pharfileinfo.html#PharFileInfo::getCompressedSize)
        — Returns the actual size of the file (with compression) inside
        the Phar archive
    -   [PharFileInfo::getContent](/class/pharfileinfo.html#PharFileInfo::getContent)
        — Get the complete file contents of the entry
    -   [PharFileInfo::getMetadata](/class/pharfileinfo.html#PharFileInfo::getMetadata)
        — Returns file-specific meta-data saved with a file
    -   [PharFileInfo::getPharFlags](/class/pharfileinfo.html#PharFileInfo::getPharFlags)
        — Returns the Phar file entry flags
    -   [PharFileInfo::hasMetadata](/class/pharfileinfo.html#PharFileInfo::hasMetadata)
        — Returns the metadata of the entry
    -   [PharFileInfo::isCRCChecked](/class/pharfileinfo.html#PharFileInfo::isCRCChecked)
        — Returns whether file entry has had its CRC verified
    -   [PharFileInfo::isCompressed](/class/pharfileinfo.html#PharFileInfo::isCompressed)
        — Returns whether the entry is compressed
    -   [PharFileInfo::setMetadata](/class/pharfileinfo.html#PharFileInfo::setMetadata)
        — Sets file-specific meta-data saved with a file
-   [PharException](/class/pharexception.html) — The PharException class

简介
----

The Phar class provides a high-level interface to accessing and creating
phar archives.

类摘要
------

**Phar**

<span class="ooclass"> class **Phar** </span> <span class="ooclass">
<span class="modifier">extends</span> **RecursiveDirectoryIterator**
</span> <span class="oointerface">implements <span
class="interfacename">Countable</span> </span> <span
class="oointerface">, <span class="interfacename">ArrayAccess</span>
</span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_AS_PATHNAME` <span class="initializer"> =
32</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_AS_FILEINFO` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_AS_SELF` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_MODE_MASK` <span class="initializer"> =
240</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::KEY_AS_PATHNAME` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::KEY_AS_FILENAME` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::FOLLOW_SYMLINKS` <span class="initializer"> =
512</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::KEY_MODE_MASK` <span class="initializer"> =
3840</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::NEW_CURRENT_AND_KEY` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::SKIP_DOTS` <span class="initializer"> = 4096</span>
;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::UNIX_PATHS` <span class="initializer"> =
8192</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addEmptyDir</span> ( <span
class="methodparam"><span class="type">string</span> `$dirname`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addFile</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$localname`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">addFromString</span> ( <span
class="methodparam"><span class="type">string</span> `$localname`</span>
, <span class="methodparam"><span class="type">string</span>
`$contents`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">apiVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">buildFromDirectory</span> ( <span
class="methodparam"><span class="type">string</span> `$base_dir`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$regex`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">buildFromIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span> `$iter`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$base_directory`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">canCompress</span> (\[ <span
class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">canWrite</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">compress</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$extension`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">compressFiles</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
)

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$fname`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \]\] )

<span class="modifier">public</span> <span class="type">PharData</span>
<span class="methodname">convertToData</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$compression`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\]\]\] )

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">convertToExecutable</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$compression`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">copy</span> ( <span class="methodparam"><span
class="type">string</span> `$oldfile`</span> , <span
class="methodparam"><span class="type">string</span> `$newfile`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">count</span> ( <span class="methodparam">void</span>
)

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">createDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$indexfile`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$webindexfile`</span> \]\] )

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">decompress</span> (\[ <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">decompressFiles</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delete</span> ( <span class="methodparam"><span
class="type">string</span> `$entry`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">extractTo</span> ( <span
class="methodparam"><span class="type">string</span> `$pathto`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">array</span><span
class="type">null</span></span> `$files`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$overwrite`<span class="initializer"> =
**`false`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getAlias</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">getModified</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getSignature</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getStub</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">getSupportedCompression</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">getSupportedSignatures</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">interceptFileFuncs</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isBuffering</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">isCompressed</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isFileFormat</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">isValidPharFilename</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$executable`<span class="initializer"> = **`true`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isWritable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">loadPhar</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">mapPhar</span> (\[ <span
class="methodparam"><span class="type">string</span> `$alias`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dataoffset`<span class="initializer"> = 0</span></span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">mount</span> ( <span class="methodparam"><span
class="type">string</span> `$pharpath`</span> , <span
class="methodparam"><span class="type">string</span>
`$externalpath`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">mungServer</span> ( <span
class="methodparam"><span class="type">array</span> `$munglist`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

<span class="modifier">public</span> <span
class="type">PharFileInfo</span> <span
class="methodname">offsetGet</span> ( <span class="methodparam"><span
class="type">string</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">running</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$retphar`<span
class="initializer"> = **`true`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setAlias</span> ( <span
class="methodparam"><span class="type">string</span> `$alias`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$index`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$webindex`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMetadata</span> ( <span
class="methodparam"><span class="type">mixed</span> `$metadata`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setSignatureAlgorithm</span> ( <span
class="methodparam"><span class="type">int</span> `$sigtype`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$privatekey`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setStub</span> ( <span
class="methodparam"><span class="type">string</span> `$stub`</span> \[,
<span class="methodparam"><span class="type">int</span> `$len`<span
class="initializer"> = -1</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">startBuffering</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">stopBuffering</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">unlinkArchive</span> ( <span
class="methodparam"><span class="type">string</span> `$archive`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">webPhar</span> (\[ <span
class="methodparam"><span class="type">string</span> `$alias`</span> \[,
<span class="methodparam"><span class="type">string</span> `$index`<span
class="initializer"> = "index.php"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$f404`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$mimetypes`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$rewrites`</span> \]\]\]\]\] )

}

Phar::addEmptyDir
=================

添加一个空目录到 phar 档案

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addEmptyDir</span> ( <span
class="methodparam"><span class="type">string</span> `$dirname`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

通过这个方法，可以创建一个以 *dirname* 为路径名的空目录。 这个方法和
<span class="function">ZipArchive::addEmptyDir</span> 类似。

### 参数

`dirname`  
需要在 phar 档案中创建的空目录名称

### 返回值

没有返回值, 失败时抛出异常（exception）。

### 范例

**示例 \#1 一个 <span class="function">Phar::addEmptyDir</span> 示例**

``` php
<?php
try {
    $a = new Phar('/path/to/phar.phar');

    $a->addEmptyDir('/full/path/to/file');
    // demonstrates how this file is stored
    $b = $a['full/path/to/file']->isDir();
} catch (Exception $e) {
    // handle errors here
}
?>
```

### 参见

-   <span class="function">PharData::addEmptyDir</span>
-   <span class="function">Phar::addFile</span>
-   <span class="function">Phar::addFromString</span>

Phar::addFile
=============

将一个文件从文件系统添加到 phar 档案中

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addFile</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$localname`</span> \] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

通过这个方法，任何文件或者 URL 可以被添加到 phar
档案中。如果第二个可选参数 *localname* 被设定，
那么文件则会以该参数为名称保存到档案中，此外，*file*
参数会被作为路径保存在档案中。 URLs 必须提交 localname
参数，否则会抛出异常。 这个方法与 <span
class="function">ZipArchive::addFile</span> 类似。

### 参数

`file`  
需要添加到 phar 档案的文件在磁盘上的完全（绝对）或者相对路径。

`localname`  
文件保存到档案时的路径。

### 返回值

没有返回值，失败时会抛出异常。

### 范例

**示例 \#1 一个 <span class="function">Phar::addFile</span> 示例**

``` php
<?php
try {
    $a = new Phar('/path/to/phar.phar');

    $a->addFile('/full/path/to/file');
    // demonstrates how this file is stored
    $b = $a['full/path/to/file']->getContent();

    $a->addFile('/full/path/to/file', 'my/file.txt');
    $c = $a['my/file.txt']->getContent();

    // demonstrate URL usage
    $a->addFile('http://www.example.com', 'example.html');
} catch (Exception $e) {
    // handle errors here
}
?>
```

### 参见

-   <span class="function">Phar::offsetSet</span>
-   <span class="function">PharData::addFile</span>
-   <span class="function">Phar::addFromString</span>
-   <span class="function">Phar::addEmptyDir</span>

Phar::addFromString
===================

以字符串的形式添加一个文件到 phar 档案

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addFromString</span> ( <span
class="methodparam"><span class="type">string</span> `$localname`</span>
, <span class="methodparam"><span class="type">string</span>
`$contents`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

通过这个方法，任何字符串都可以被添加到 phar 档案中。 文件将会以
*localname* 为路径保存到档案中。 这个方法与 <span
class="function">ZipArchive::addFromString</span> 类似。

### 参数

`localname`  
文件保存到档案时的路径。

`contents`  
要保存的文件内容。

### 返回值

没有返回值，失败时会抛出异常。

### 范例

**示例 \#1 一个 <span class="function">Phar::addFromString</span> 示例**

``` php
<?php
try {
    $a = new Phar('/path/to/phar.phar');

    $a->addFromString('path/to/file.txt', 'my simple file');
    $b = $a['path/to/file.txt']->getContent();

    // to add contents from a stream handle for large files, use offsetSet()
    $c = fopen('/path/to/hugefile.bin');
    $a['largefile.bin'] = $c;
    fclose($c);
} catch (Exception $e) {
    // handle errors here
}
?>
```

### 参见

-   <span class="function">Phar::offsetSet</span>
-   <span class="function">PharData::addFromString</span>
-   <span class="function">Phar::addFile</span>
-   <span class="function">Phar::addEmptyDir</span>

Phar::apiVersion
================

Returns the api version

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">Phar::apiVersion</span> ( <span
class="methodparam">void</span> )

Return the API version of the phar file format that will be used when
creating phars. The Phar extension supports reading API version 1.0.0 or
newer. API version 1.1.0 is required for SHA-256 and SHA-512 hash, and
API version 1.1.1 is required to store empty directories.

### 参数

### 返回值

The API version string as in *"1.0.0"*.

### 范例

**示例 \#1 A <span class="function">Phar::apiVersion</span> example**

``` php
<?php
echo Phar::apiVersion();
?>
```

以上例程会输出：

    1.1.1

Phar::buildFromDirectory
========================

Construct a phar archive from the files within a directory

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::buildFromDirectory</span> ( <span
class="methodparam"><span class="type">string</span> `$base_dir`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$regex`</span> \] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Populate a phar archive from directory contents. The optional second
parameter is a regular expression (pcre) that is used to exclude files.
Any filename that matches the regular expression will be included, all
others will be excluded. For more fine-grained control, use <span
class="function">Phar::buildFromIterator</span>.

### 参数

`base_dir`  
The full or relative path to the directory that contains all files to
add to the archive.

`regex`  
An optional pcre regular expression that is used to filter the list of
files. Only file paths matching the regular expression will be included
in the archive.

### 返回值

<span class="function">Phar::buildFromDirectory</span> returns an
associative array mapping internal path of file to the full path of the
file on the filesystem.

### 错误／异常

This method throws <span class="classname">BadMethodCallException</span>
when unable to instantiate the internal directory iterators, or a <span
class="classname">PharException</span> if there were errors saving the
phar archive.

### 范例

**示例 \#1 A <span class="function">Phar::buildFromDirectory</span>
example**

``` php
<?php
// create with alias "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
// add all files in the project
$phar->buildFromDirectory(dirname(__FILE__) . '/project');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));

$phar2 = new Phar('project2.phar', 0, 'project2.phar');
// add all files in the project, only include php files
$phar2->buildFromDirectory(dirname(__FILE__) . '/project', '/\.php$/');
$phar2->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

### 参见

-   <span class="function">Phar::buildFromIterator</span>

Phar::buildFromIterator
=======================

Construct a phar archive from an iterator

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::buildFromIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span> `$iter`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$base_directory`</span> \] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Populate a phar archive from an iterator. Two styles of iterators are
supported, iterators that map the filename within the phar to the name
of a file on disk, and iterators like DirectoryIterator that return
SplFileInfo objects. For iterators that return SplFileInfo objects, the
second parameter is required.

### 参数

`iter`  
Any iterator that either associatively maps phar file to location or
returns SplFileInfo objects

`base_directory`  
For iterators that return SplFileInfo objects, the portion of each
file's full path to remove when adding to the phar archive

### 返回值

<span class="function">Phar::buildFromIterator</span> returns an
associative array mapping internal path of file to the full path of the
file on the filesystem.

### 范例

**示例 \#1 A <span class="function">Phar::buildFromIterator</span> with
SplFileInfo**

For most phar archives, the archive will reflect an actual directory
layout, and the second style is the most useful. For instance, to create
a phar archive containing the files in this sample directory layout:

``` examples
/path/to/project/
                 config/
                        dist.xml
                        debug.xml
                 lib/
                     file1.php
                     file2.php
                 src/
                     processthing.php
                 www/
                     index.php
                 cli/
                     index.php
```

This code could be used to add these files to the "project.phar" phar
archive:

``` php
<?php
// create with alias "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new RecursiveDirectoryIterator('/path/to/project')),
    '/path/to/project');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

The file project.phar can then be used immediately. <span
class="function">Phar::buildFromIterator</span> does not set values such
as compression, metadata, and this can be done after creating the phar
archive.

As an interesting note, <span
class="function">Phar::buildFromIterator</span> can also be used to copy
the contents of an existing phar archive, as the Phar object descends
from <span class="classname">DirectoryIterator</span>:

``` php
<?php
// create with alias "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new Phar('/path/to/anotherphar.phar')),
    'phar:///path/to/anotherphar.phar/path/to/project');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

**示例 \#2 A <span class="function">Phar::buildFromIterator</span> with
other iterators**

The second form of the iterator can be used with any iterator that
returns a key =\> value mapping, such as an <span
class="classname">ArrayIterator</span>:

``` php
<?php
// create with alias "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
$phar->buildFromIterator(
    new ArrayIterator(
     array(
        'internal/file.php' => dirname(__FILE__) . '/somefile.php',
        'another/file.jpg' => fopen('/path/to/bigfile.jpg', 'rb'),
     )));
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

### 错误／异常

This method returns <span
class="classname">UnexpectedValueException</span> when the iterator
returns incorrect values, such as an integer key instead of a string, a
<span class="classname">BadMethodCallException</span> when an
SplFileInfo-based iterator is passed without a `base_directory`
parameter, or a <span class="classname">PharException</span> if there
were errors saving the phar archive.

### 参见

-   <span class="function">Phar::buildFromDirectory</span>

Phar::canCompress
=================

Returns whether phar extension supports compression using either zlib or
bzip2

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::canCompress</span> (\[ <span
class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = 0</span></span> \] )

This should be used to test whether compression is possible prior to
loading a phar archive containing compressed files.

### 参数

`type`  
Either *Phar::GZ* or *Phar::BZ2* can be used to test whether compression
is possible with a specific compression algorithm (zlib or bzip2).

### 返回值

**`true`** if compression/decompression is available, **`false`** if
not.

### 范例

**示例 \#1 A <span class="function">Phar::canCompress</span> example**

``` php
<?php
if (Phar::canCompress()) {
    echo file_get_contents('phar://compressedphar.phar/internal/file.txt');
} else {
    echo 'no compression available';
}
?>
```

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::decompressFiles</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">Phar::convertToExecutable</span>
-   <span class="function">Phar::convertToData</span>

Phar::canWrite
==============

Returns whether phar extension supports writing and creating phars

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::canWrite</span> ( <span
class="methodparam">void</span> )

This static method determines whether write access has been disabled in
the system php.ini via the
<a href="/phar/setup.html#" class="link">phar.readonly</a> ini variable.

### 参数

### 返回值

**`true`** if write access is enabled, **`false`** if it is disabled.

### 范例

**示例 \#1 A <span class="function">Phar::canWrite</span> example**

``` php
<?php
if (Phar::canWrite()) {
    file_put_contents('phar://myphar.phar/file.txt', 'hi there');
}
?>
```

### 参见

-   <a href="/phar/setup.html#" class="link">phar.readonly</a>
-   <span class="function">Phar::isWritable</span>

Phar::compress
==============

Compresses the entire Phar archive using Gzip or Bzip2 compression

### 说明

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">Phar::compress</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$extension`</span> \] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

For tar-based and phar-based phar archives, this method compresses the
entire archive using gzip compression or bzip2 compression. The
resulting file can be processed with the gunzip command/bunzip command,
or accessed directly and transparently with the Phar extension.

For Zip-based phar archives, this method fails with an exception. The
<a href="/ref/zlib.html" class="link">zlib</a> extension must be enabled
to compress with gzip compression, the
<a href="/ref/bzip2.html" class="link">bzip2</a> extension must be
enabled in order to compress with bzip2 compression. As with all
functionality that modifies the contents of a phar, the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
must be off in order to succeed.

In addition, this method automatically renames the archive, appending
*.gz*, *.bz2* or removing the extension if passed *Phar::NONE* to remove
compression. Alternatively, a file extension may be specified with the
second parameter.

### 参数

`compression`  
Compression must be one of *Phar::GZ*, *Phar::BZ2* to add compression,
or *Phar::NONE* to remove compression.

`extension`  
By default, the extension is *.phar.gz* or *.phar.bz2* for compressing
phar archives, and *.phar.tar.gz* or *.phar.tar.bz2* for compressing tar
archives. For decompressing, the default file extensions are *.phar* and
*.phar.tar*.

### 返回值

Returns a <span class="classname">Phar</span> object.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
is on, the <a href="/ref/zlib.html" class="link">zlib</a> extension is
not available, or the <a href="/ref/bzip2.html" class="link">bzip2</a>
extension is not enabled.

### 范例

**示例 \#1 A <span class="function">Phar::compress</span> example**

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
$p1 = $p->compress(Phar::GZ); // copies to /path/to/my.phar.gz
$p2 = $p->compress(Phar::BZ2); // copies to /path/to/my.phar.bz2
$p3 = $p2->compress(Phar::NONE); // exception: /path/to/my.phar already exists
?>
```

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">PharData::compress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::decompress</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::decompressFiles</span>

Phar::compressFiles
===================

Compresses all files in the current Phar archive

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::compressFiles</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
)

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

For tar-based phar archives, this method throws a <span
class="classname">BadMethodCallException</span>, as compression of
individual files within a tar archive is not supported by the file
format. Use <span class="function">Phar::compress</span> to compress an
entire tar-based phar archive.

For Zip-based and phar-based phar archives, this method compresses all
files in the Phar archive using the specified compression. The
<a href="/ref/zlib.html" class="link">zlib</a> or
<a href="/ref/bzip2.html" class="link">bzip2</a> extensions must be
enabled to take advantage of this feature. In addition, if any files are
already compressed using bzip2/zlib compression, the respective
extension must be enabled in order to decompress the files prior to
re-compressing. As with all functionality that modifies the contents of
a phar, the <a href="/phar/setup.html#" class="link">phar.readonly</a>
INI variable must be off in order to succeed.

### 参数

`compression`  
Compression must be one of *Phar::GZ*, *Phar::BZ2* to add compression,
or *Phar::NONE* to remove compression.

### 返回值

没有返回值。

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
is on, the <a href="/ref/zlib.html" class="link">zlib</a> extension is
not available, or if any files are compressed using bzip2 compression
and the <a href="/ref/bzip2.html" class="link">bzip2</a> extension is
not enabled.

### 范例

**示例 \#1 A <span class="function">Phar::compressFiles</span> example**

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
$p->compressFiles(Phar::GZ);
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
?>
```

以上例程会输出：

    string(10) "myfile.txt"
    bool(false)
    bool(false)
    bool(false)
    string(11) "myfile2.txt"
    bool(false)
    bool(false)
    bool(false)
    string(10) "myfile.txt"
    int(4096)
    bool(false)
    bool(true)
    string(11) "myfile2.txt"
    int(4096)
    bool(false)
    bool(true)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::decompressFiles</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::decompress</span>

Phar::\_\_construct
===================

Construct a Phar archive object

### 说明

<span class="modifier">public</span> <span
class="methodname">Phar::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$fname`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \]\] )

### 参数

`fname`  
Path to an existing Phar archive or to-be-created archive. The file
name's extension must contain .phar.

`flags`  
Flags to pass to parent class <span
class="classname">RecursiveDirectoryIterator</span>.

`alias`  
Alias with which this Phar archive should be referred to in calls to
stream functionality.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if called
twice, <span class="classname">UnexpectedValueException</span> if the
phar archive can't be opened.

### 范例

**示例 \#1 A <span class="function">Phar::\_\_construct</span> example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', FilesystemIterator::CURRENT_AS_FILEINFO | FilesystemIterator::KEY_AS_FILENAME,
                  'my.phar');
} catch (UnexpectedValueException $e) {
    die('Could not open my.phar');
} catch (BadMethodCallException $e) {
    echo 'technically, this cannot happen';
}
// this works now
echo file_get_contents('phar://my.phar/example.txt');
// and works as if we had typed
echo file_get_contents('phar:///path/to/my.phar/example.txt');
?>
```

Phar::convertToData
===================

Convert a phar archive to a non-executable tar or zip file

### 说明

<span class="modifier">public</span> <span class="type">PharData</span>
<span class="methodname">Phar::convertToData</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$compression`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\]\]\] )

This method is used to convert an executable phar archive to either a
tar or zip file. To make the tar or zip non-executable, the phar stub
and phar alias files are removed from the newly created archive.

If no changes are specified, this method throws a <span
class="classname">BadMethodCallException</span> if the archive is in
phar file format. For archives in tar or zip file format, this method
converts the archive to a non-executable archive.

If successful, the method creates a new archive on disk and returns a
<span class="classname">PharData</span> object. The old archive is not
removed from disk, and should be done manually after the process has
finished.

### 参数

`format`  
This should be one of *Phar::TAR* or *Phar::ZIP*. If set to **`null`**,
the existing file format will be preserved.

`compression`  
This should be one of *Phar::NONE* for no whole-archive compression,
*Phar::GZ* for zlib-based compression, and *Phar::BZ2* for bzip-based
compression.

`extension`  
This parameter is used to override the default file extension for a
converted archive. Note that *.phar* cannot be used anywhere in the
filename for a non-executable tar or zip archive.

If converting to a tar-based phar archive, the default extensions are
*.tar*, *.tar.gz*, and *.tar.bz2* depending on specified compression.
For zip-based archives, the default extension is *.zip*.

### 返回值

The method returns a <span class="classname">PharData</span> object on
success and throws an exception on failure.

### 错误／异常

This method throws <span class="classname">BadMethodCallException</span>
when unable to compress, an unknown compression method has been
specified, the requested archive is buffering with <span
class="function">Phar::startBuffering</span> and has not concluded with
<span class="function">Phar::stopBuffering</span>, and a <span
class="classname">PharException</span> if any problems are encountered
during the phar creation process.

### 范例

**示例 \#1 A <span class="function">Phar::convertToData</span> example**

Using Phar::convertToData():

``` php
<?php
try {
    $tarphar = new Phar('myphar.phar.tar');
    // note that myphar.phar.tar is *not* unlinked
    // convert it to the non-executable tar file format
    // creates myphar.tar
    $tar = $tarphar->convertToData();
    // convert to non-executable zip format, creates myphar.zip
    $zip = $tarphar->convertToData(Phar::ZIP);
    // create myphar.tbz
    $tgz = $tarphar->convertToData(Phar::TAR, Phar::BZ2, '.tbz');
    // creates myphar.phar.tgz
    $phar = $tarphar->convertToData(Phar::PHAR); // throws exception
} catch (Exception $e) {
    // handle the error here
}
?>
```

### 参见

-   <span class="function">Phar::convertToExecutable</span>
-   <span class="function">PharData::convertToExecutable</span>
-   <span class="function">PharData::convertToData</span>

Phar::convertToExecutable
=========================

Convert a phar archive to another executable phar archive file format

### 说明

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">Phar::convertToExecutable</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$compression`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\]\]\] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

This method is used to convert a phar archive to another file format.
For instance, it can be used to create a tar-based executable phar
archive from a zip-based executable phar archive, or from an executable
phar archive in the phar file format. In addition, it can be used to
apply whole-archive compression to a tar or phar-based archive.

If no changes are specified, this method throws a <span
class="classname">BadMethodCallException</span>.

If successful, the method creates a new archive on disk and returns a
<span class="classname">Phar</span> object. The old archive is not
removed from disk, and should be done manually after the process has
finished.

### 参数

`format`  
This should be one of *Phar::PHAR*, *Phar::TAR*, or *Phar::ZIP*. If set
to **`null`**, the existing file format will be preserved.

`compression`  
This should be one of *Phar::NONE* for no whole-archive compression,
*Phar::GZ* for zlib-based compression, and *Phar::BZ2* for bzip-based
compression.

`extension`  
This parameter is used to override the default file extension for a
converted archive. Note that all zip- and tar-based phar archives must
contain *.phar* in their file extension in order to be processed as a
phar archive.

If converting to a phar-based archive, the default extensions are
*.phar*, *.phar.gz*, or *.phar.bz2* depending on the specified
compression. For tar-based phar archives, the default extensions are
*.phar.tar*, *.phar.tar.gz*, and *.phar.tar.bz2*. For zip-based phar
archives, the default extension is *.phar.zip*.

### 返回值

The method returns a <span class="classname">Phar</span> object on
success and throws an exception on failure.

### 错误／异常

This method throws <span class="classname">BadMethodCallException</span>
when unable to compress, an unknown compression method has been
specified, the requested archive is buffering with <span
class="function">Phar::startBuffering</span> and has not concluded with
<span class="function">Phar::stopBuffering</span>, an <span
class="classname">UnexpectedValueException</span> if write support is
disabled, and a <span class="classname">PharException</span> if any
problems are encountered during the phar creation process.

### 范例

**示例 \#1 A <span class="function">Phar::convertToExecutable</span>
example**

Using Phar::convertToExecutable():

``` php
<?php
try {
    $tarphar = new Phar('myphar.phar.tar');
    // convert it to the phar file format
    // note that myphar.phar.tar is *not* unlinked
    $phar = $tarphar->convertToExecutable(Phar::PHAR); // creates myphar.phar
    $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
    // creates myphar.phar.tgz
    $compressed = $phar->convertToExecutable(Phar::TAR, Phar::GZ, '.phar.tgz');
} catch (Exception $e) {
    // handle the error here
}
?>
```

### 参见

-   <span class="function">Phar::convertToData</span>
-   <span class="function">PharData::convertToExecutable</span>
-   <span class="function">PharData::convertToData</span>

Phar::copy
==========

Copy a file internal to the phar archive to another new file within the
phar

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::copy</span> ( <span
class="methodparam"><span class="type">string</span> `$oldfile`</span> ,
<span class="methodparam"><span class="type">string</span>
`$newfile`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Copy a file internal to the phar archive to another new file within the
phar. This is an object-oriented alternative to using <span
class="function">copy</span> with the phar stream wrapper.

### 参数

`oldfile`  

`newfile`  

### 返回值

returns **`true`** on success, but it is safer to encase method call in
a try/catch block and assume success if no exception is thrown.

### 错误／异常

throws <span class="classname">UnexpectedValueException</span> if the
source file does not exist, the destination file already exists, write
access is disabled, opening either file fails, reading the source file
fails, or a <span class="classname">PharException</span> if writing the
changes to the phar fails.

### 范例

**示例 \#1 A <span class="function">Phar::copy</span> example**

This example shows using <span class="function">Phar::copy</span> and
the equivalent stream wrapper performance of the same thing. The primary
difference between the two approaches is error handling. All Phar
methods throw exceptions, whereas the stream wrapper uses <span
class="function">trigger\_error</span>.

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar['a'] = 'hi';
    $phar->copy('a', 'b');
    echo $phar['b']; // outputs "hi"
} catch (Exception $e) {
    // handle error
}

// the stream wrapper equivalent of the above code.
// E_WARNINGS are triggered on error rather than exceptions.
copy('phar://myphar.phar/a', 'phar//myphar.phar/c');
echo file_get_contents('phar://myphar.phar/c'); // outputs "hi"
?>
```

Phar::count
===========

Returns the number of entries (files) in the Phar archive

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Phar::count</span> ( <span
class="methodparam">void</span> )

### 参数

### 返回值

The number of files contained within this phar, or *0* (the number zero)
if none.

### 范例

**示例 \#1 A <span class="function">Phar::count</span> example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
} catch (Exception $e) {
    echo 'Could not create phar:', $e;
}
echo 'The new phar has ' . $p->count() . " entries\n";
$p['file.txt'] = 'hi';
echo 'The new phar has ' . $p->count() . " entries\n";
?>
```

以上例程会输出：

    The new phar has 0 entries
    The new phar has 1 entries

Phar::createDefaultStub
=======================

Create a phar-file format specific stub

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">Phar::createDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$indexfile`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$webindexfile`</span> \]\] )

This method is intended for creation of phar-file format-specific stubs,
and is not intended for use with tar- or zip-based phar archives.

Phar archives contain a bootstrap loader, or *stub* written in PHP that
is executed when the archive is executed in PHP either via include:

``` php
<?php
include 'myphar.phar';
?>
```

or by simple execution:

    php myphar.phar
        

This method provides a simple and easy method to create a stub that will
run a startup file from the phar archive. In addition, different files
can be specified for running the phar archive from the command line
versus through a web server. The loader stub also calls <span
class="function">Phar::interceptFileFuncs</span> to allow easy bundling
of a PHP application that accesses the file system. If the phar
extension is not present, the loader stub will extract the phar archive
to a temporary directory and then operate on the files. A shutdown
function erases the temporary files on exit.

### 返回值

Returns a string containing the contents of a customized bootstrap
loader (stub) that allows the created Phar archive to work with or
without the Phar extension enabled.

### 错误／异常

Throws <span class="classname">UnexpectedValueException</span> if either
parameter is longer than 400 bytes.

### 范例

**示例 \#1 A <span class="function">Phar::createDefaultStub</span>
example**

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
} catch (Exception $e) {
    // handle errors
}
?>
```

### 参见

-   <span class="function">Phar::setStub</span>
-   <span class="function">Phar::getStub</span>

Phar::decompress
================

Decompresses the entire Phar archive

### 说明

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">Phar::decompress</span> (\[ <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

For tar-based and phar-based phar archives, this method decompresses the
entire archive.

For Zip-based phar archives, this method fails with an exception. The
<a href="/ref/zlib.html" class="link">zlib</a> extension must be enabled
to decompress an archive compressed with gzip compression, and the
<a href="/ref/bzip2.html" class="link">bzip2</a> extension must be
enabled in order to decompress an archive compressed with bzip2
compression. As with all functionality that modifies the contents of a
phar, the <a href="/phar/setup.html#" class="link">phar.readonly</a> INI
variable must be off in order to succeed.

In addition, this method automatically changes the file extension of the
archive, *.phar* by default for phar archives, or *.phar.tar* for
tar-based phar archives. Alternatively, a file extension may be
specified with the second parameter.

### 参数

`extension`  
For decompressing, the default file extensions are *.phar* and
*.phar.tar*. Use this parameter to specify another file extension. Be
aware that all executable phar archives must contain *.phar* in their
filename.

### 返回值

A <span class="classname">Phar</span> object is returned.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
is on, the <a href="/ref/zlib.html" class="link">zlib</a> extension is
not available, or the <a href="/ref/bzip2.html" class="link">bzip2</a>
extension is not enabled.

### 范例

**示例 \#1 A <span class="function">Phar::decompress</span> example**

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar.gz');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
$p3 = $p2->decompress(); // creates /path/to/my.phar
?>
```

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">PharData::compress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::decompressFiles</span>

Phar::decompressFiles
=====================

Decompresses all files in the current Phar archive

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::decompressFiles</span> ( <span
class="methodparam">void</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

For tar-based phar archives, this method throws a <span
class="classname">BadMethodCallException</span>, as compression of
individual files within a tar archive is not supported by the file
format. Use <span class="function">Phar::compress</span> to compress an
entire tar-based phar archive.

For Zip-based and phar-based phar archives, this method decompresses all
files in the Phar archive. The
<a href="/ref/zlib.html" class="link">zlib</a> or
<a href="/ref/bzip2.html" class="link">bzip2</a> extensions must be
enabled to take advantage of this feature if any files are compressed
using bzip2/zlib compression. As with all functionality that modifies
the contents of a phar, the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
must be off in order to succeed.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
is on, the <a href="/ref/zlib.html" class="link">zlib</a> extension is
not available, or if any files are compressed using bzip2 compression
and the <a href="/ref/bzip2.html" class="link">bzip2</a> extension is
not enabled.

### 范例

**示例 \#1 A <span class="function">Phar::decompressFiles</span>
example**

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
$p->compressFiles(Phar::GZ);
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
$p->decompressFiles();
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
?>
```

以上例程会输出：

    string(10) "myfile.txt"
    int(4096)
    bool(false)
    bool(true)
    string(11) "myfile2.txt"
    int(4096)
    bool(false)
    bool(true)
    string(10) "myfile.txt"
    bool(false)
    bool(false)
    bool(false)
    string(11) "myfile2.txt"
    bool(false)
    bool(false)
    bool(false)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::decompress</span>

Phar::delMetadata
=================

Deletes the global metadata of the phar

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::delMetadata</span> ( <span
class="methodparam">void</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Deletes the global metadata of the phar

### 参数

### 返回值

returns **`true`** on success, but it is better to check for thrown
exception, and assume success if none is thrown.

### 错误／异常

Throws <span class="classname">PharException</span> if errors occur
while flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">Phar::delMetaData</span> example**

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    var_dump($phar->getMetadata());
    $phar->setMetadata("hi there");
    var_dump($phar->getMetadata());
    $phar->delMetadata();
    var_dump($phar->getMetadata());
} catch (Exception $e) {
    // handle errors
}
?>
```

以上例程会输出：

    NULL
    string(8) "hi there"
    NULL

### 参见

-   <span class="function">Phar::getMetadata</span>
-   <span class="function">Phar::setMetadata</span>
-   <span class="function">Phar::hasMetadata</span>

Phar::delete
============

删除 phar 档案中的一个文件

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::delete</span> ( <span
class="methodparam"><span class="type">string</span> `$entry`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

删除档案中的一个文件。这个方法与下面示例中调用 <span
class="function">unlink</span> 处理数据流包装器的方式等价。

### 参数

`entry`  
需要删除的文件在档案中的路径。

### 返回值

成功时返回
**`true`**，但是最好还是检查一下是否抛出了异常，如果没有抛出，可以认定操作成功。

### 错误／异常

如果将修改保存到磁盘时发生了错误，会抛出 <span
class="classname">PharException</span> 异常。

### 范例

**示例 \#1 一个 <span class="function">Phar::delete</span> 示例**

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->delete('unlink/me.php');
    // this is equivalent to:
    unlink('phar://myphar.phar/unlink/me.php');
} catch (Exception $e) {
    // handle errors
}
?>
```

### 参见

-   <span class="function">PharData::delete</span>
-   <span class="function">Phar::unlinkArchive</span>

Phar::extractTo
===============

Extract the contents of a phar archive to a directory

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::extractTo</span> ( <span
class="methodparam"><span class="type">string</span> `$pathto`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">array</span><span
class="type">null</span></span> `$files`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$overwrite`<span class="initializer"> =
**`false`**</span></span> \]\] )

Extract all files within a phar archive to disk. Extracted files and
directories preserve permissions as stored in the archive. The optional
parameters allow optional control over which files are extracted, and
whether existing files on disk can be overwritten. The second parameter
`files` can be either the name of a file or directory to extract, or an
array of names of files and directories to extract. By default, this
method will not overwrite existing files, the third parameter can be set
to true to enable overwriting of files. This method is similar to <span
class="function">ZipArchive::extractTo</span>.

### 参数

`pathto`  
Path to extract the given `files` to

`files`  
The name of a file or directory to extract, or an array of
files/directories to extract, **`null`** to skip this param

`overwrite`  
Set to **`true`** to enable overwriting existing files

### 返回值

returns **`true`** on success, but it is better to check for thrown
exception, and assume success if none is thrown.

### 错误／异常

Throws <span class="classname">PharException</span> if errors occur
while flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">Phar::extractTo</span> example**

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->extractTo('/full/path'); // extract all files
    $phar->extractTo('/another/path', 'file.txt'); // extract only file.txt
    $phar->extractTo('/this/path',
        array('file1.txt', 'file2.txt')); // extract 2 files only
    $phar->extractTo('/third/path', null, true); // extract all files, and overwrite
} catch (Exception $e) {
    // handle errors
}
?>
```

### 参见

-   <span class="function">PharData::extractTo</span>

Phar::getAlias
==============

Get the alias for Phar

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getAlias</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Returns the alias or **`null`** if there's no alias.

Phar::getMetadata
=================

Returns phar archive meta-data

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Phar::getMetadata</span> ( <span
class="methodparam">void</span> )

Retrieve archive meta-data. Meta-data can be any PHP variable that can
be serialized.

### 参数

No parameters.

### 返回值

any PHP variable that can be serialized and is stored as meta-data for
the Phar archive, or **`null`** if no meta-data is stored.

### 范例

**示例 \#1 A <span class="function">Phar::getMetadata</span> example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.php'] = '<?php echo "hello";';
    $p->setMetadata(array('bootstrap' => 'file.php'));
    var_dump($p->getMetadata());
} catch (Exception $e) {
    echo 'Could not modify phar:', $e;
}
?>
```

以上例程会输出：

    array(1) {
      ["bootstrap"]=>
      string(8) "file.php"
    }

### 参见

-   <span class="function">Phar::setMetadata</span>
-   <span class="function">Phar::delMetadata</span>
-   <span class="function">Phar::hasMetadata</span>

Phar::getModified
=================

Return whether phar was modified

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::getModified</span> ( <span
class="methodparam">void</span> )

This method can be used to determine whether a phar has either had an
internal file deleted, or contents of a file changed in some way.

### 参数

No parameters.

### 返回值

**`true`** if the phar has been modified since opened, **`false`** if
not.

Phar::getPath
=============

Get the real path to the Phar archive on disk

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getPath</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

Phar::getSignature
==================

Return MD5/SHA1/SHA256/SHA512/OpenSSL signature of a Phar archive

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::getSignature</span> ( <span
class="methodparam">void</span> )

Returns the verification signature of a phar archive in a hexadecimal
string.

### 参数

### 返回值

Array with the opened archive's signature in *hash* key and *MD5*,
*SHA-1*, *SHA-256*, *SHA-512*, or *OpenSSL* in *hash\_type*. This
signature is a hash calculated on the entire phar's contents, and may be
used to verify the integrity of the archive. A valid signature is
absolutely required of all executable phar archives if the
<a href="/phar/setup.html#" class="link">phar.require_hash</a> INI
variable is set to true.

Phar::getStub
=============

Return the PHP loader or bootstrap stub of a Phar archive

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getStub</span> ( <span
class="methodparam">void</span> )

Phar archives contain a bootstrap loader, or *stub* written in PHP that
is executed when the archive is executed in PHP either via include:

``` php
<?php
include 'myphar.phar';
?>
```

or by simple execution:

    php myphar.phar
        

### 返回值

Returns a string containing the contents of the bootstrap loader (stub)
of the current Phar archive.

### 错误／异常

Throws <span class="classname">RuntimeException</span> if it is not
possible to read the stub from the Phar archive.

### 范例

**示例 \#1 A <span class="function">Phar::getStub</span> example**

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
echo $p->getStub();
echo "==NEXT==\n";
$p->setStub("<?php
function __autoload($class)
{
    include 'phar://' . str_replace('_', '/', $class);
}
Phar::mapPhar('myphar.phar');
include 'phar://myphar.phar/startup.php';
__HALT_COMPILER(); ?>");
echo $p->getStub();
?>
```

以上例程会输出：

    <?php __HALT_COMPILER(); ?>
    ==NEXT==
    <?php
    function __autoload($class)
    {
        include 'phar://' . str_replace('_', '/', $class);
    }
    Phar::mapPhar('myphar.phar');
    include 'phar://myphar.phar/startup.php';
    __HALT_COMPILER(); ?>

### 参见

-   <span class="function">Phar::setStub</span>
-   <span class="function">Phar::createDefaultStub</span>

Phar::getSupportedCompression
=============================

Return array of supported compression algorithms

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">Phar::getSupportedCompression</span> ( <span
class="methodparam">void</span> )

### 参数

No parameters.

### 返回值

Returns an array containing any of *Phar::GZ* or *Phar::BZ2*, depending
on the availability of the
<a href="/book/zlib.html" class="link">zlib</a> extension or the
<a href="/book/bzip2.html" class="link">bz2</a> extension.

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::decompress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::decompressFiles</span>

Phar::getSupportedSignatures
============================

Return array of supported signature types

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">Phar::getSupportedSignatures</span> ( <span
class="methodparam">void</span> )

Return array of supported signature types

### 参数

No parameters.

### 返回值

Returns an array containing any of *MD5*, *SHA-1*, *SHA-256*, *SHA-512*,
or *OpenSSL*.

### 参见

-   <span class="function">Phar::getSignature</span>
-   <span class="function">Phar::setSignatureAlgorithm</span>

Phar::getVersion
================

Return version info of Phar archive

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getVersion</span> ( <span
class="methodparam">void</span> )

Returns the API version of an opened Phar archive.

### 参数

### 返回值

The opened archive's API version. This is not to be confused with the
API version that the loaded phar extension will use to create new phars.
Each Phar archive has the API version hard-coded into its manifest. See
<a href="/phar/fileformat.html" class="link">Phar file format</a>
documentation for more information.

### 参见

-   <span class="function">Phar::apiVersion</span>

Phar::hasMetadata
=================

Returns whether phar has global meta-data

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::hasMetadata</span> ( <span
class="methodparam">void</span> )

Returns whether phar has global meta-data set.

### 参数

No parameters.

### 返回值

Returns **`true`** if meta-data has been set, and **`false`** if not.

### 范例

**示例 \#1 A <span class="function">Phar::hasMetadata</span> example**

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    var_dump($phar->hasMetadata());
    $phar->setMetadata(array('thing' => 'hi'));
    var_dump($phar->hasMetadata());
    $phar->delMetadata();
    var_dump($phar->hasMetadata());
} catch (Exception $e) {
    // handle error
}
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">Phar::getMetadata</span>
-   <span class="function">Phar::setMetadata</span>
-   <span class="function">Phar::delMetadata</span>

Phar::interceptFileFuncs
========================

Instructs phar to intercept fopen, file\_get\_contents, opendir, and all
of the stat-related functions

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::interceptFileFuncs</span> ( <span
class="methodparam">void</span> )

instructs phar to intercept <span class="function">fopen</span>, <span
class="function">readfile</span>, <span
class="function">file\_get\_contents</span>, <span
class="function">opendir</span>, and all of the stat-related functions.
If any of these functions is called from within a phar archive with a
relative path, the call is modified to access a file within the phar
archive. Absolute paths are assumed to be attempts to load external
files from the filesystem.

This function makes it possible to run PHP applications designed to run
off of a hard disk as a phar application.

### 参数

No parameters.

### 返回值

### 范例

**示例 \#1 A <span class="function">Phar::interceptFileFuncs</span>
example**

``` php
<?php
Phar::interceptFileFuncs();
include 'phar://' . __FILE__ . '/file.php';
?>
```

Assuming that this phar is at */path/to/myphar.phar* and it contains
*file.php* and *file2.txt*, if *file.php* contains this code:

**示例 \#2 A <span class="function">Phar::interceptFileFuncs</span>
example**

``` php
<?php
echo file_get_contents('file2.txt');
?>
```

Normally PHP would search the current directory for *file2.txt*, which
would translate as the directory of file.php, or the current directory
of a command-line user. <span
class="function">Phar::interceptFileFuncs</span> instructs PHP to
consider the current directory to be *phar:///path/to/myphar.phar/* and
so opens *phar:///path/to/myphar.phar/file2.txt* in the above example
code.

Phar::isBuffering
=================

Used to determine whether Phar write operations are being buffered, or
are flushing directly to disk

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::isBuffering</span> ( <span
class="methodparam">void</span> )

This method can be used to determine whether a Phar will save changes to
disk immediately, or whether a call to <span
class="function">Phar::stopBuffering</span> is needed to enable saving
changes.

Phar write buffering is per-archive, buffering active for the *foo.phar*
Phar archive does not affect changes to the *bar.phar* Phar archive.

### 返回值

Returns **`true`** if the write operations are being buffer, **`false`**
otherwise.

### 范例

**示例 \#1 A <span class="function">Phar::isBuffering</span> example**

``` php
<?php
$p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
$p2 = new Phar('existingphar.phar');
$p['file1.txt'] = 'hi';
var_dump($p->isBuffering());
var_dump($p2->isBuffering());
?>
=2=
<?php
$p->startBuffering();
var_dump($p->isBuffering());
var_dump($p2->isBuffering());
$p->stopBuffering();
?>
=3=
<?php
var_dump($p->isBuffering());
var_dump($p2->isBuffering());
?>
```

以上例程会输出：

    bool(false)
    bool(false)
    =2=
    bool(true)
    bool(false)
    =3=
    bool(false)
    bool(false)

### 参见

-   <span class="function">Phar::startBuffering</span>
-   <span class="function">Phar::stopBuffering</span>

Phar::isCompressed
==================

Returns Phar::GZ or PHAR::BZ2 if the entire phar archive is compressed
(.tar.gz/tar.bz and so on)

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Phar::isCompressed</span> ( <span
class="methodparam">void</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Returns Phar::GZ or PHAR::BZ2 if the entire phar archive is compressed
(.tar.gz/tar.bz and so on). Zip-based phar archives cannot be compressed
as a file, and so this method will always return **`false`** if a
zip-based phar archive is queried.

### 参数

No parameters.

### 返回值

*Phar::GZ*, *Phar::BZ2* or **`false`**

### 范例

**示例 \#1 A <span class="function">Phar::isCompressed</span> example**

``` php
<?php
try {
    $phar1 = new Phar('myphar.zip.phar');
    var_dump($phar1->isCompressed());
    $phar2 = new Phar('myuncompressed.tar.phar');
    var_dump($phar2->isCompressed());
    $phar2->compress(Phar::GZ);
    var_dump($phar2->isCompressed() == Phar::GZ);
} catch (Exception $e) {
}
?>
```

以上例程会输出：

    bool(false)
    bool(false)
    bool(true)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">Phar::decompress</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::decompressFiles</span>
-   <span class="function">Phar::getSupportedCompression</span>

Phar::isFileFormat
==================

Returns true if the phar archive is based on the tar/phar/zip file
format depending on the parameter

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::isFileFormat</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> )

### 参数

`format`  
Either *Phar::PHAR*, *Phar::TAR*, or *Phar::ZIP* to test for the format
of the archive.

### 返回值

Returns **`true`** if the phar archive matches the file format requested
by the parameter

### 错误／异常

<span class="classname">PharException</span> is thrown if the parameter
is an unknown file format specifier.

### 参见

-   <span class="function">Phar::convertToExecutable</span>
-   <span class="function">Phar::convertToData</span>

Phar::isValidPharFilename
=========================

Returns whether the given filename is a valid phar filename

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::isValidPharFilename</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$executable`<span class="initializer"> = **`true`**</span></span> \] )

Returns whether the given filename is a valid phar filename that will be
recognized as a phar archive by the phar extension. This can be used to
test a name without having to instantiate a phar archive and catch the
inevitable Exception that will be thrown if an invalid name is
specified.

### 参数

`filename`  
The name or full path to a phar archive not yet created

`executable`  
This parameter determines whether the filename should be treated as a
phar executable archive, or a data non-executable archive

### 返回值

Returns **`true`** if the filename is valid, **`false`** if not.

Phar::isWritable
================

Returns true if the phar archive can be modified

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::isWritable</span> ( <span
class="methodparam">void</span> )

This method returns **`true`** if *phar.readonly* is *0*, and the actual
phar archive on disk is not read-only.

### 参数

No parameters.

### 返回值

Returns **`true`** if the phar archive can be modified

### 参见

-   <span class="function">Phar::canWrite</span>
-   <span class="function">PharData::isWritable</span>

Phar::loadPhar
==============

Loads any phar archive with an alias

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::loadPhar</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \] )

This can be used to read the contents of an external Phar archive. This
is most useful for assigning an alias to a phar so that subsequent
references to the phar can use the shorter alias, or for loading Phar
archives that only contain data and are not intended for
execution/inclusion in PHP scripts.

### 参数

`filename`  
the full or relative path to the phar archive to open

`alias`  
The alias that may be used to refer to the phar archive. Note that many
phar archives specify an explicit alias inside the phar archive, and a
<span class="classname">PharException</span> will be thrown if a new
alias is specified in this case.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

<span class="classname">PharException</span> is thrown if an alias is
passed in and the phar archive already has an explicit alias

### 范例

**示例 \#1 A <span class="function">Phar::loadPhar</span> example**

Phar::loadPhar can be used anywhere to load an external Phar archive,
whereas Phar::mapPhar should be used in a loader stub for a Phar.

``` php
<?php
try {
    Phar::loadPhar('/path/to/phar.phar', 'my.phar');
    echo file_get_contents('phar://my.phar/file.txt');
} catch (PharException $e) {
    echo $e;
}
?>
```

### 参见

-   <span class="function">Phar::mapPhar</span>

Phar::mapPhar
=============

Reads the currently executed file (a phar) and registers its manifest

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::mapPhar</span> (\[ <span
class="methodparam"><span class="type">string</span> `$alias`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dataoffset`<span class="initializer"> = 0</span></span> \]\] )

This static method can only be used inside a Phar archive's loader stub
in order to initialize the phar when it is directly executed, or when it
is included in another script.

### 参数

`alias`  
The alias that can be used in *phar://* URLs to refer to this archive,
rather than its full path.

`dataoffset`  
Unused variable, here for compatibility with PEAR's PHP\_Archive.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

<span class="classname">PharException</span> is thrown if not called
directly within PHP execution, if no \_\_HALT\_COMPILER(); token is
found in the current source file, or if the file cannot be opened for
reading.

### 范例

**示例 \#1 A <span class="function">Phar::mapPhar</span> example**

mapPhar should be used only inside a phar's loader stub. Use loadPhar to
load an external phar into memory.

Here is a sample Phar loader stub that uses mapPhar.

``` php
<?php
function __autoload($class)
{
    include 'phar://me.phar/' . str_replace('_', '/', $class) . '.php';
}
try {
    Phar::mapPhar('me.phar');
    include 'phar://me.phar/startup.php';
} catch (PharException $e) {
    echo $e->getMessage();
    die('Cannot initialize Phar');
}
__HALT_COMPILER();
```

### 参见

-   <span class="function">Phar::loadPhar</span>

Phar::mount
===========

Mount an external path or file to a virtual location within the phar
archive

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::mount</span> ( <span
class="methodparam"><span class="type">string</span> `$pharpath`</span>
, <span class="methodparam"><span class="type">string</span>
`$externalpath`</span> )

Much like the unix file system concept of mounting external devices to
paths within the directory tree, <span
class="function">Phar::mount</span> allows referring to external files
and directories as if they were inside of an archive. This allows
powerful abstraction such as referring to external configuration files
as if they were inside the archive.

### 参数

`pharpath`  
The internal path within the phar archive to use as the mounted path
location. This must be a relative path within the phar archive, and must
not already exist.

`externalpath`  
A path or URL to an external file or directory to mount within the phar
archive

### 返回值

No return. <span class="classname">PharException</span> is thrown on
failure.

### 错误／异常

Throws <span class="classname">PharException</span> if any problems
occur mounting the path.

### 范例

**示例 \#1 A <span class="function">Phar::mount</span> example**

The following example shows accessing an external configuration file as
if it were a path within a phar archive.

First, the code inside of a phar archive:

``` php
<?php
$configuration = simplexml_load_string(file_get_contents(
    Phar::running(false) . '/config.xml'));
?>
```

Next the external code used to mount the configuration file:

``` php
<?php
// first set up the association between the abstract config.xml
// and the actual one on disk
Phar::mount('phar://config.xml', '/home/example/config.xml');
// now run the application
include '/path/to/archive.phar';
?>
```

Another method is to put the mounting code inside the stub of the phar
archive. Here is an example of setting up a default configuration file
if no user configuration is specified:

``` php
<?php
// first set up the association between the abstract config.xml
// and the actual one on disk
if (defined('EXTERNAL_CONFIG')) {
    Phar::mount('config.xml', EXTERNAL_CONFIG);
    if (file_exists(__DIR__ . '/extra_config.xml')) {
        Phar::mount('extra.xml', __DIR__ . '/extra_config.xml');
    }
} else {
    Phar::mount('config.xml', 'phar://' . __FILE__ . '/default_config.xml');
    Phar::mount('extra.xml', 'phar://' . __FILE__ . '/default_extra.xml');
}
// now run the application
include 'phar://' . __FILE__ . '/index.php';
__HALT_COMPILER();
?>
```

...and the code externally to load this phar archive:

``` php
<?php
define('EXTERNAL_CONFIG', '/home/example/config.xml');
// now run the application
include '/path/to/archive.phar';
?>
```

Phar::mungServer
================

Defines a list of up to 4 $\_SERVER variables that should be modified
for execution

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::mungServer</span> ( <span
class="methodparam"><span class="type">array</span> `$munglist`</span> )

<span class="function">Phar::mungServer</span> should only be called
within the stub of a phar archive.

Defines a list of up to 4 `$_SERVER` variables that should be modified
for execution. Variables that can be modified to remove traces of phar
execution are *REQUEST\_URI*, *PHP\_SELF*, *SCRIPT\_NAME* and
*SCRIPT\_FILENAME*.

On its own, this method does nothing. Only when combined with <span
class="function">Phar::webPhar</span> does it take effect, and only when
the requested file is a PHP file to be parsed. Note that the
*PATH\_INFO* and *PATH\_TRANSLATED* variables are always modified.

The original values of variables that are modified are stored in the
SERVER array with *PHAR\_* prepended, so for instance *SCRIPT\_NAME*
would be saved as *PHAR\_SCRIPT\_NAME*.

### 参数

`munglist`  
an array containing as string indices any of *REQUEST\_URI*,
*PHP\_SELF*, *SCRIPT\_NAME* and *SCRIPT\_FILENAME*. Other values trigger
an exception, and <span class="function">Phar::mungServer</span> is
case-sensitive.

### 返回值

No return.

### 错误／异常

Throws <span class="classname">UnexpectedValueException</span> if any
problems are found with the passed in data.

### 范例

**示例 \#1 A <span class="function">Phar::mungServer</span> example**

``` php
<?php
// example stub
Phar::mungServer(array('REQUEST_URI'));
Phar::webPhar();
__HALT_COMPILER();
?>
```

### 参见

-   <span class="function">Phar::webPhar</span>
-   <span class="function">Phar::setStub</span>

Phar::offsetExists
==================

Determines whether a file exists in the phar

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

This is an implementation of the <span
class="interfacename">ArrayAccess</span> interface allowing direct
manipulation of the contents of a Phar archive using array access
brackets.

offsetExists() is called whenever <span class="function">isset</span> is
called.

### 参数

`offset`  
The filename (relative path) to look for in a Phar.

### 返回值

Returns **`true`** if the file exists within the phar, or **`false`** if
not.

### 范例

**示例 \#1 A <span class="function">Phar::offsetExists</span> example**

``` php
<?php
$p = new Phar(dirname(__FILE__) . '/my.phar', 0, 'my.phar');
$p['firstfile.txt'] = 'first file';
$p['secondfile.txt'] = 'second file';
// the next set of lines call offsetExists() indirectly
var_dump(isset($p['firstfile.txt']));
var_dump(isset($p['nothere.txt']));
?>
```

以上例程会输出：

    bool(true)
    bool(false)

### 参见

-   <span class="function">Phar::offsetGet</span>
-   <span class="function">Phar::offsetSet</span>
-   <span class="function">Phar::offsetUnset</span>

Phar::offsetGet
===============

Gets a <span class="classname">PharFileInfo</span> object for a specific
file

### 说明

<span class="modifier">public</span> <span
class="type">PharFileInfo</span> <span
class="methodname">Phar::offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

This is an implementation of the <span
class="interfacename">ArrayAccess</span> interface allowing direct
manipulation of the contents of a Phar archive using array access
brackets. <span class="methodname">Phar::offsetGet</span> is used for
retrieving files from a Phar archive.

### 参数

`offset`  
The filename (relative path) to look for in a Phar.

### 返回值

A <span class="classname">PharFileInfo</span> object is returned that
can be used to iterate over a file's contents or to retrieve information
about the current file.

### 错误／异常

This method throws <span class="classname">BadMethodCallException</span>
if the file does not exist in the Phar archive.

### 范例

**示例 \#1 <span class="function">Phar::offsetGet</span> example**

As with all classes that implement the <span
class="classname">ArrayAccess</span> interface, <span
class="methodname">Phar::offsetGet</span> is automatically called when
using the *\[\]* angle bracket operator.

``` php
<?php
$p = new Phar(dirname(__FILE__) . '/myphar.phar', 0, 'myphar.phar');
$p['exists.txt'] = "file exists\n";
try {
    // automatically calls offsetGet()
    echo $p['exists.txt'];
    echo $p['doesnotexist.txt'];
} catch (BadMethodCallException $e) {
    echo $e;
}
?>
```

以上例程会输出：

    file exists
    Entry doesnotexist.txt does not exist

### 参见

-   <span class="function">Phar::offsetExists</span>
-   <span class="function">Phar::offsetSet</span>
-   <span class="function">Phar::offsetUnset</span>

Phar::offsetSet
===============

Set the contents of an internal file to those of an external file

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

This is an implementation of the <span
class="interfacename">ArrayAccess</span> interface allowing direct
manipulation of the contents of a Phar archive using array access
brackets. offsetSet is used for modifying an existing file, or adding a
new file to a Phar archive.

### 参数

`offset`  
The filename (relative path) to modify in a Phar.

`value`  
Content of the file.

### 返回值

No return values.

### 错误／异常

if <a href="/phar/setup.html#" class="link">phar.readonly</a> is *1*,
<span class="classname">BadMethodCallException</span> is thrown, as
modifying a Phar is only allowed when phar.readonly is set to *0*.
Throws <span class="classname">PharException</span> if there are any
problems flushing changes made to the Phar archive to disk.

### 范例

**示例 \#1 A <span class="function">Phar::offsetSet</span> example**

offsetSet should not be accessed directly, but instead used via array
access with the *\[\]* operator.

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
try {
    // calls offsetSet
    $p['file.txt'] = 'Hi there';
} catch (Exception $e) {
    echo 'Could not modify file.txt:', $e;
}
?>
```

### 参见

-   <span class="function">Phar::offsetExists</span>
-   <span class="function">Phar::offsetGet</span>
-   <span class="function">Phar::offsetUnset</span>

Phar::offsetUnset
=================

Remove a file from a phar

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

This is an implementation of the <span
class="interfacename">ArrayAccess</span> interface allowing direct
manipulation of the contents of a Phar archive using array access
brackets. offsetUnset is used for deleting an existing file, and is
called by the <span class="function">unset</span> language construct.

### 参数

`offset`  
The filename (relative path) to modify in a Phar.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

if <a href="/phar/setup.html#" class="link">phar.readonly</a> is *1*,
<span class="classname">BadMethodCallException</span> is thrown, as
modifying a Phar is only allowed when phar.readonly is set to *0*.
Throws <span class="classname">PharException</span> if there are any
problems flushing changes made to the Phar archive to disk.

### 范例

**示例 \#1 A <span class="function">Phar::offsetUnset</span> example**

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
try {
    // deletes file.txt from my.phar by calling offsetUnset
    unset($p['file.txt']);
} catch (Exception $e) {
    echo 'Could not delete file.txt: ', $e;
}
?>
```

### 参见

-   <span class="function">Phar::offsetExists</span>
-   <span class="function">Phar::offsetGet</span>
-   <span class="function">Phar::offsetSet</span>
-   <span class="function">Phar::unlinkArchive</span>
-   <span class="function">Phar::delete</span>

Phar::running
=============

Returns the full path on disk or full phar URL to the currently
executing Phar archive

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">Phar::running</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$retphar`<span
class="initializer"> = **`true`**</span></span> \] )

Returns the full path to the running phar archive. This is intended for
use much like the *\_\_FILE\_\_* magic constant, and only has effect
inside an executing phar archive.

Inside the stub of an archive, <span
class="function">Phar::running</span> returns *""*. Simply use
**`__FILE__`** to access the current running phar inside a stub.

### 参数

`retphar`  
If **`false`**, the full path on disk to the phar archive is returned.
If **`true`**, a full phar URL is returned.

### 返回值

Returns the filename if valid, empty string otherwise.

### 范例

**示例 \#1 A <span class="function">Phar::running</span> example**

For the following example, assume the phar archive is located at
*/path/to/phar/my.phar*.

``` php
<?php
$a = Phar::running(); // $a is "phar:///path/to/my.phar"
$b = Phar::running(false); // $b is "/path/to/my.phar"
?>
```

Phar::setAlias
==============

Set the alias for the Phar archive

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::setAlias</span> ( <span
class="methodparam"><span class="type">string</span> `$alias`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Set the alias for the Phar archive, and write it as the permanent alias
for this phar archive. An alias can be used internally to a phar archive
to ensure that use of the *phar* stream wrapper to access internal files
always works regardless of the location of the phar archive on the
filesystem. Another alternative is to rely upon Phar's interception of
<span class="function">include</span> or to use <span
class="function">Phar::interceptFileFuncs</span> and use relative paths.

### 参数

`alias`  
A shorthand string that this archive can be referred to in *phar* stream
wrapper access.

### 返回值

### 错误／异常

Throws <span class="classname">UnexpectedValueException</span> when
write access is disabled, and <span
class="classname">PharException</span> if the alias is already in use or
any problems were encountered flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">Phar::setAlias</span> example**

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->setAlias('myp.phar');
} catch (Exception $e) {
    // handle error
}
?>
```

### 参见

-   <span class="function">Phar::\_\_construct</span>
-   <span class="function">Phar::interceptFileFuncs</span>

Phar::setDefaultStub
====================

Used to set the PHP loader or bootstrap stub of a Phar archive to the
default loader

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::setDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$index`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$webindex`</span> \]\] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

This method is a convenience method that combines the functionality of
<span class="function">Phar::createDefaultStub</span> and <span
class="function">Phar::setStub</span>.

### 参数

`index`  
Relative path within the phar archive to run if accessed on the
command-line

`webindex`  
Relative path within the phar archive to run if accessed through a web
browser

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

<span class="classname">UnexpectedValueException</span> is thrown if
<a href="/phar/setup.html#" class="link">phar.readonly</a> is enabled in
php.ini. <span class="classname">PharException</span> is thrown if any
problems are encountered flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">Phar::setDefaultStub</span>
example**

``` php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->setDefaultStub('cli.php', 'web/index.php');
    // this is the same as:
    // $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
} catch (Exception $e) {
    // handle errors
}
?>
```

### 参见

-   <span class="function">Phar::setStub</span>
-   <span class="function">Phar::createDefaultStub</span>

Phar::setMetadata
=================

Sets phar archive meta-data

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setMetadata</span> ( <span
class="methodparam"><span class="type">mixed</span> `$metadata`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

<span class="function">Phar::setMetadata</span> should be used to store
customized data that describes something about the phar archive as a
complete entity. <span class="function">PharFileInfo::setMetadata</span>
should be used for file-specific meta-data. Meta-data can slow down the
performance of loading a phar archive if the data is large.

Some possible uses for meta-data include specifying which file within
the archive should be used to bootstrap the archive, or the location of
a file manifest like
<a href="https://pear.php.net/" class="link external">» PEAR</a>'s
package.xml file. However, any useful data that describes the phar
archive may be stored.

### 参数

`metadata`  
Any PHP variable containing information to store that describes the phar
archive

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">Phar::setMetadata</span> example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.php'] = '<?php echo "hello"';
    $p->setMetadata(array('bootstrap' => 'file.php'));
    var_dump($p->getMetadata());
} catch (Exception $e) {
    echo 'Could not create and/or modify phar:', $e;
}
?>
```

以上例程会输出：

    array(1) {
      ["bootstrap"]=>
      string(8) "file.php"
    }

### 参见

-   <span class="function">Phar::getMetadata</span>
-   <span class="function">Phar::delMetadata</span>
-   <span class="function">Phar::hasMetadata</span>

Phar::setSignatureAlgorithm
===========================

Set the signature algorithm for a phar and apply it

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setSignatureAlgorithm</span> ( <span
class="methodparam"><span class="type">int</span> `$sigtype`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$privatekey`</span> \] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

set the signature algorithm for a phar and apply it. The signature
algorithm must be one of *Phar::MD5*, *Phar::SHA1*, *Phar::SHA256*,
*Phar::SHA512*, or *Phar::OPENSSL*.

Note that all executable phar archives have a signature created
automatically, *SHA1* by default. data tar- or zip-based archives
(archives created with the <span class="classname">PharData</span>
class) must have their signature created and set explicitly via <span
class="function">Phar::setSignatureAlgorithm</span>.

### 参数

`sigtype`  
One of *Phar::MD5*, *Phar::SHA1*, *Phar::SHA256*, *Phar::SHA512*, or
*Phar::OPENSSL*

`privatekey`  
The contents of an OpenSSL private key, as extracted from a certificate
or OpenSSL key file:

``` php
<?php
$private = openssl_get_privatekey(file_get_contents('private.pem'));
$pkey = '';
openssl_pkey_export($private, $pkey);
$p->setSignatureAlgorithm(Phar::OPENSSL, $pkey);
?>
```

See <a href="/phar/using.html" class="link">phar introduction</a> for
instructions on naming and placement of the public key file.

### 返回值

没有返回值。

### 错误／异常

Throws <span class="classname">UnexpectedValueException</span> for many
errors, and a <span class="classname">PharException</span> if any
problems occur flushing changes to disk.

### 参见

-   <span class="function">Phar::getSupportedSignatures</span>
-   <span class="function">Phar::getSignature</span>

Phar::setStub
=============

Used to set the PHP loader or bootstrap stub of a Phar archive

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::setStub</span> ( <span
class="methodparam"><span class="type">string</span> `$stub`</span> \[,
<span class="methodparam"><span class="type">int</span> `$len`<span
class="initializer"> = -1</span></span> \] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

This method is used to add a PHP bootstrap loader stub to a new Phar
archive, or to replace the loader stub in an existing Phar archive.

The loader stub for a Phar archive is used whenever an archive is
included directly as in this example:

``` php
<?php
include 'myphar.phar';
?>
```

The loader is not accessed when including a file through the *phar*
stream wrapper like so:

``` php
<?php
include 'phar://myphar.phar/somefile.php';
?>
```

### 参数

`stub`  
A string or an open stream handle to use as the executable stub for this
phar archive.

`len`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

<span class="classname">UnexpectedValueException</span> is thrown if
<a href="/phar/setup.html#" class="link">phar.readonly</a> is enabled in
php.ini. <span class="classname">PharException</span> is thrown if any
problems are encountered flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">Phar::setStub</span> example**

``` php
<?php
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['a.php'] = '<?php var_dump("Hello");';
    $p->setStub('<?php var_dump("First"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>');
    include 'phar://brandnewphar.phar/a.php';
    var_dump($p->getStub());
    $p['b.php'] = '<?php var_dump("World");';
    $p->setStub('<?php var_dump("Second"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>');
    include 'phar://brandnewphar.phar/b.php';
    var_dump($p->getStub());
} catch (Exception $e) {
    echo 'Write operations failed on brandnewphar.phar: ', $e;
}
?>
```

以上例程会输出：

    string(5) "Hello"
    string(82) "<?php var_dump("First"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>"
    string(5) "World"
    string(83) "<?php var_dump("Second"); Phar::mapPhar("brandnewphar.phar"); __HALT_COMPILER(); ?>"

### 参见

-   <span class="function">Phar::getStub</span>
-   <span class="function">Phar::createDefaultStub</span>

Phar::startBuffering
====================

Start buffering Phar write operations, do not modify the Phar object on
disk

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::startBuffering</span> ( <span
class="methodparam">void</span> )

Although technically unnecessary, the <span
class="function">Phar::startBuffering</span> method can provide a
significant performance boost when creating or modifying a Phar archive
with a large number of files. Ordinarily, every time a file within a
Phar archive is created or modified in any way, the entire Phar archive
will be recreated with the changes. In this way, the archive will be
up-to-date with the activity performed on it.

However, this can be unnecessary when simply creating a new Phar
archive, when it would make more sense to write the entire archive out
at once. Similarly, it is often necessary to make a series of changes
and to ensure that they all are possible before making any changes on
disk, similar to the relational database concept of transactions. the
<span class="function">Phar::startBuffering</span>/<span
class="function">Phar::stopBuffering</span> pair of methods is provided
for this purpose.

Phar write buffering is per-archive, buffering active for the *foo.phar*
Phar archive does not affect changes to the *bar.phar* Phar archive.

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">Phar::startBuffering</span>
example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
} catch (Exception $e) {
    echo 'Could not create phar:', $e;
}
echo 'The new phar has ' . $p->count() . " entries\n";
$p->startBuffering();
$p['file.txt'] = 'hi';
$p['file2.txt'] = 'there';
$p['file2.txt']->setCompressedGZ();
$p['file3.txt'] = 'babyface';
$p['file3.txt']->setMetadata(42);
$p->setStub("<?php
function __autoload($class)
{
    include 'phar://myphar.phar/' . str_replace('_', '/', $class) . '.php';
}
Phar::mapPhar('myphar.phar');
include 'phar://myphar.phar/startup.php';
__HALT_COMPILER();");
$p->stopBuffering();
?>
```

### 参见

-   <span class="function">Phar::stopBuffering</span>
-   <span class="function">Phar::isBuffering</span>

Phar::stopBuffering
===================

Stop buffering write requests to the Phar archive, and save changes to
disk

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::stopBuffering</span> ( <span
class="methodparam">void</span> )

<span class="function">Phar::stopBuffering</span> is used in conjunction
with the <span class="function">Phar::startBuffering</span> method.
<span class="function">Phar::startBuffering</span> can provide a
significant performance boost when creating or modifying a Phar archive
with a large number of files. Ordinarily, every time a file within a
Phar archive is created or modified in any way, the entire Phar archive
will be recreated with the changes. In this way, the archive will be
up-to-date with the activity performed on it.

However, this can be unnecessary when simply creating a new Phar
archive, when it would make more sense to write the entire archive out
at once. Similarly, it is often necessary to make a series of changes
and to ensure that they all are possible before making any changes on
disk, similar to the relational database concept of transactions. The
<span class="function">Phar::startBuffering</span>/<span
class="function">Phar::stopBuffering</span> pair of methods is provided
for this purpose.

Phar write buffering is per-archive, buffering active for the *foo.phar*
Phar archive does not affect changes to the *bar.phar* Phar archive.

### 返回值

没有返回值。

### 错误／异常

<span class="classname">PharException</span> is thrown if any problems
are encountered flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">Phar::stopBuffering</span> example**

``` php
<?php
$p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
$p['file1.txt'] = 'hi';
$p->startBuffering();
var_dump($p->getStub());
$p->setStub("<?php
function __autoload(\$class)
{
    include 'phar://brandnewphar.phar/' . str_replace('_', '/', \$class) . '.php';
}
Phar::mapPhar('brandnewphar.phar');
include 'phar://brandnewphar.phar/startup.php';
__HALT_COMPILER();");
$p->stopBuffering();
var_dump($p->getStub());
?>
```

以上例程会输出：

    string(24) "<?php __HALT_COMPILER();"
    string(195) "<?php
    function __autoload($class)
    {
        include 'phar://' . str_replace('_', '/', $class);
    }
    Phar::mapPhar('brandnewphar.phar');
    include 'phar://brandnewphar.phar/startup.php';
    __HALT_COMPILER();"

### 参见

-   <span class="function">Phar::startBuffering</span>
-   <span class="function">Phar::isBuffering</span>

Phar::unlinkArchive
===================

Completely remove a phar archive from disk and from memory

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::unlinkArchive</span> ( <span
class="methodparam"><span class="type">string</span> `$archive`</span> )

Removes a phar archive from disk and memory.

### 参数

`archive`  
The path on disk to the phar archive.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

<span class="classname">PharException</span> is thrown if there are any
open file pointers to the phar archive, or any existing <span
class="classname">Phar</span>, <span class="classname">PharData</span>,
or <span class="classname">PharFileInfo</span> objects referring to the
phar archive.

### 范例

**示例 \#1 A <span class="function">Phar::unlinkArchive</span> example**

``` php
<?php
// simple usage
Phar::unlinkArchive('/path/to/my.phar');

// more common example:
$p = new Phar('my.phar');
$fp = fopen('phar://my.phar/file.txt', 'r');
// this creates 'my.phar.gz'
$gp = $p->compress(Phar::GZ);
// remove all references to the archive
unset($p);
fclose($fp);
// now remove all traces of the archive
Phar::unlinkArchive('my.phar');
?>
```

### 参见

-   <span class="function">Phar::delete</span>
-   <span class="function">Phar::offsetUnset</span>

Phar::webPhar
=============

mapPhar for web-based phars. front controller for web applications

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::webPhar</span> (\[ <span
class="methodparam"><span class="type">string</span> `$alias`</span> \[,
<span class="methodparam"><span class="type">string</span> `$index`<span
class="initializer"> = "index.php"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$f404`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$mimetypes`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$rewrites`</span> \]\]\]\]\] )

<span class="function">Phar::mapPhar</span> for web-based phars. This
method parses `$_SERVER['REQUEST_URI']` and routes a request from a web
browser to an internal file within the phar archive. In essence, it
simulates a web server, routing requests to the correct file, echoing
the correct headers and parsing PHP files as needed. This powerful
method is part of what makes it easy to convert an existing PHP
application into a phar archive. Combined with <span
class="function">Phar::mungServer</span> and <span
class="function">Phar::interceptFileFuncs</span>, any web application
can be used unmodified from a phar archive.

<span class="function">Phar::webPhar</span> should only be called from
the stub of a phar archive (see
<a href="/phar/fileformat.html#Phar%20file%20stub" class="link">here</a>
for more information on what a stub is).

### 参数

`alias`  
The alias that can be used in *phar://* URLs to refer to this archive,
rather than its full path.

`index`  
The location within the phar of the directory index.

`f404`  
The location of the script to run when a file is not found. This script
should output the proper HTTP 404 headers.

`mimetypes`  
An array mapping additional file extensions to MIME type. If the default
mapping is sufficient, pass an empty array. By default, these extensions
are mapped to these MIME types:

``` php
<?php
$mimes = array(
    'phps' => Phar::PHPS, // pass to highlight_file()
    'c' => 'text/plain',
    'cc' => 'text/plain',
    'cpp' => 'text/plain',
    'c++' => 'text/plain',
    'dtd' => 'text/plain',
    'h' => 'text/plain',
    'log' => 'text/plain',
    'rng' => 'text/plain',
    'txt' => 'text/plain',
    'xsd' => 'text/plain',
    'php' => Phar::PHP, // parse as PHP
    'inc' => Phar::PHP, // parse as PHP
    'avi' => 'video/avi',
    'bmp' => 'image/bmp',
    'css' => 'text/css',
    'gif' => 'image/gif',
    'htm' => 'text/html',
    'html' => 'text/html',
    'htmls' => 'text/html',
    'ico' => 'image/x-ico',
    'jpe' => 'image/jpeg',
    'jpg' => 'image/jpeg',
    'jpeg' => 'image/jpeg',
    'js' => 'application/x-javascript',
    'midi' => 'audio/midi',
    'mid' => 'audio/midi',
    'mod' => 'audio/mod',
    'mov' => 'movie/quicktime',
    'mp3' => 'audio/mp3',
    'mpg' => 'video/mpeg',
    'mpeg' => 'video/mpeg',
    'pdf' => 'application/pdf',
    'png' => 'image/png',
    'swf' => 'application/shockwave-flash',
    'tif' => 'image/tiff',
    'tiff' => 'image/tiff',
    'wav' => 'audio/wav',
    'xbm' => 'image/xbm',
    'xml' => 'text/xml',
);
?>
```

`rewrites`  
The rewrites function is passed a string as its only parameter and must
return a <span class="type">string</span> or **`false`**.

If you are using fast-cgi or cgi then the parameter passed to the
function is the value of the `$_SERVER['PATH_INFO']` variable.
Otherwise, the parameter passed to the function is the value of the
`$_SERVER['REQUEST_URI']` variable.

If a string is returned it is used as the internal file path. If
**`false`** is returned then webPhar() will send a HTTP 403 Denied Code.

### 返回值

没有返回值。

### 错误／异常

Throws <span class="classname">PharException</span> when unable to open
the internal file to output, or if called from a non-stub. If an invalid
array value is passed into `mimetypes` or an invalid callback is passed
into `rewrites`, then <span
class="classname">UnexpectedValueException</span> is thrown.

### 范例

**示例 \#1 A <span class="function">Phar::webPhar</span> example**

With the example below, the created phar will display *Hello World* if
one browses to */myphar.phar/index.php* or to */myphar.phar*, and will
display the source of *index.phps* if one browses to
*/myphar.phar/index.phps*.

``` php
<?php
// creating the phar archive:
try {
    $phar = new Phar('myphar.phar');
    $phar['index.php'] = '<?php echo "Hello World"; ?>';
    $phar['index.phps'] = '<?php echo "Hello World"; ?>';
    $phar->setStub('<?php
Phar::webPhar();
__HALT_COMPILER(); ?>');
} catch (Exception $e) {
    // handle error here
}
?>
```

### 参见

-   <span class="function">Phar::mungServer</span>
-   <span class="function">Phar::interceptFileFuncs</span>

简介
----

The PharData class provides a high-level interface to accessing and
creating non-executable tar and zip archives. Because these archives do
not contain a stub and cannot be executed by the phar extension, it is
possible to create and manipulate regular zip and tar files using the
PharData class even if *phar.readonly* php.ini setting is *1*.

类摘要
------

**PharData**

<span class="ooclass"> class **PharData** </span> <span class="ooclass">
<span class="modifier">extends</span> **RecursiveDirectoryIterator**
</span> {

/\* 继承的常量 \*/

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_AS_PATHNAME` <span class="initializer"> =
32</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_AS_FILEINFO` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_AS_SELF` <span class="initializer"> =
16</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::CURRENT_MODE_MASK` <span class="initializer"> =
240</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::KEY_AS_PATHNAME` <span class="initializer"> =
0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::KEY_AS_FILENAME` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::FOLLOW_SYMLINKS` <span class="initializer"> =
512</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::KEY_MODE_MASK` <span class="initializer"> =
3840</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::NEW_CURRENT_AND_KEY` <span class="initializer"> =
256</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::SKIP_DOTS` <span class="initializer"> = 4096</span>
;

<span class="modifier">const</span> <span class="type">int</span>
`FilesystemIterator::UNIX_PATHS` <span class="initializer"> =
8192</span> ;

/\* 方法 \*/

<span class="type">void</span> <span
class="methodname">addEmptyDir</span> ( <span class="methodparam"><span
class="type">string</span> `$dirname`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addFile</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$localname`</span> \] )

<span class="type">void</span> <span
class="methodname">addFromString</span> ( <span
class="methodparam"><span class="type">string</span> `$localname`</span>
, <span class="methodparam"><span class="type">string</span>
`$contents`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::buildFromDirectory</span> ( <span
class="methodparam"><span class="type">string</span> `$base_dir`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$regex`</span> \] )

<span class="type">array</span> <span
class="methodname">buildFromIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span> `$iter`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$base_directory`</span> \] )

<span class="type">PharData</span> <span
class="methodname">compress</span> ( <span class="methodparam"><span
class="type">int</span> `$compression`</span> \[, <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\] )

<span class="type">void</span> <span
class="methodname">compressFiles</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
)

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$fname`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \[, <span class="methodparam"><span
class="type">int</span> `$format`<span class="initializer"> =
**`Phar::TAR`**</span></span> \]\]\] )

<span class="type">PharData</span> <span
class="methodname">convertToData</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$compression`</span> \[, <span class="methodparam"><span
class="type">string</span> `$extension`</span> \]\]\] )

<span class="type">Phar</span> <span
class="methodname">convertToExecutable</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$compression`</span> \[, <span class="methodparam"><span
class="type">string</span> `$extension`</span> \]\]\] )

<span class="type">bool</span> <span class="methodname">copy</span> (
<span class="methodparam"><span class="type">string</span>
`$oldfile`</span> , <span class="methodparam"><span
class="type">string</span> `$newfile`</span> )

<span class="type">PharData</span> <span
class="methodname">decompress</span> (\[ <span class="methodparam"><span
class="type">string</span> `$extension`</span> \] )

<span class="type">bool</span> <span
class="methodname">decompressFiles</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span
class="methodname">delMetadata</span> ( <span
class="methodparam">void</span> )

<span class="type">bool</span> <span class="methodname">delete</span> (
<span class="methodparam"><span class="type">string</span>
`$entry`</span> )

<span class="type">bool</span> <span class="methodname">extractTo</span>
( <span class="methodparam"><span class="type">string</span>
`$pathto`</span> \[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">array</span><span
class="type">null</span></span> `$files`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$overwrite`<span class="initializer"> =
**`false`**</span></span> \]\] )

<span class="type">bool</span> <span
class="methodname">isWritable</span> ( <span
class="methodparam">void</span> )

<span class="type">void</span> <span class="methodname">offsetSet</span>
( <span class="methodparam"><span class="type">string</span>
`$offset`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

<span class="type">bool</span> <span
class="methodname">offsetUnset</span> ( <span class="methodparam"><span
class="type">string</span> `$offset`</span> )

<span class="type">bool</span> <span class="methodname">setAlias</span>
( <span class="methodparam"><span class="type">string</span>
`$alias`</span> )

<span class="type">bool</span> <span
class="methodname">setDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$index`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$webindex`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setMetadata</span> ( <span
class="methodparam"><span class="type">mixed</span> `$metadata`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setSignatureAlgorithm</span> ( <span
class="methodparam"><span class="type">int</span> `$sigtype`</span> )

<span class="type">bool</span> <span class="methodname">setStub</span> (
<span class="methodparam"><span class="type">string</span>
`$stub`</span> \[, <span class="methodparam"><span
class="type">int</span> `$len`<span class="initializer"> =
-1</span></span> \] )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addEmptyDir</span> ( <span
class="methodparam"><span class="type">string</span> `$dirname`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addFile</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$localname`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addFromString</span> ( <span
class="methodparam"><span class="type">string</span> `$localname`</span>
, <span class="methodparam"><span class="type">string</span>
`$contents`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">Phar::apiVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::buildFromDirectory</span> ( <span
class="methodparam"><span class="type">string</span> `$base_dir`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$regex`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::buildFromIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span> `$iter`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$base_directory`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::canCompress</span> (\[ <span
class="methodparam"><span class="type">int</span> `$type`<span
class="initializer"> = 0</span></span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::canWrite</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">Phar::compress</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$extension`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::compressFiles</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
)

<span class="modifier">public</span> <span
class="methodname">Phar::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$fname`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \]\] )

<span class="modifier">public</span> <span class="type">PharData</span>
<span class="methodname">Phar::convertToData</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$compression`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\]\]\] )

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">Phar::convertToExecutable</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$compression`<span
class="initializer"> = 9021976</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\]\]\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::copy</span> ( <span
class="methodparam"><span class="type">string</span> `$oldfile`</span> ,
<span class="methodparam"><span class="type">string</span>
`$newfile`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Phar::count</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">Phar::createDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$indexfile`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$webindexfile`</span> \]\] )

<span class="modifier">public</span> <span class="type">Phar</span>
<span class="methodname">Phar::decompress</span> (\[ <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::decompressFiles</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::delMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::delete</span> ( <span
class="methodparam"><span class="type">string</span> `$entry`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::extractTo</span> ( <span
class="methodparam"><span class="type">string</span> `$pathto`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">array</span><span
class="type">null</span></span> `$files`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$overwrite`<span class="initializer"> =
**`false`**</span></span> \]\] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getAlias</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Phar::getMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::getModified</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::getSignature</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getStub</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">Phar::getSupportedCompression</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">array</span>
<span class="methodname">Phar::getSupportedSignatures</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Phar::getVersion</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::hasMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::interceptFileFuncs</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::isBuffering</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Phar::isCompressed</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::isFileFormat</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::isValidPharFilename</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">bool</span>
`$executable`<span class="initializer"> = **`true`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::isWritable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::loadPhar</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::mapPhar</span> (\[ <span
class="methodparam"><span class="type">string</span> `$alias`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$dataoffset`<span class="initializer"> = 0</span></span> \]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::mount</span> ( <span
class="methodparam"><span class="type">string</span> `$pharpath`</span>
, <span class="methodparam"><span class="type">string</span>
`$externalpath`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::mungServer</span> ( <span
class="methodparam"><span class="type">array</span> `$munglist`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::offsetExists</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

<span class="modifier">public</span> <span
class="type">PharFileInfo</span> <span
class="methodname">Phar::offsetGet</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">string</span>
<span class="methodname">Phar::running</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$retphar`<span
class="initializer"> = **`true`**</span></span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::setAlias</span> ( <span
class="methodparam"><span class="type">string</span> `$alias`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::setDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$index`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$webindex`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setMetadata</span> ( <span
class="methodparam"><span class="type">mixed</span> `$metadata`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setSignatureAlgorithm</span> ( <span
class="methodparam"><span class="type">int</span> `$sigtype`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$privatekey`</span> \] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Phar::setStub</span> ( <span
class="methodparam"><span class="type">string</span> `$stub`</span> \[,
<span class="methodparam"><span class="type">int</span> `$len`<span
class="initializer"> = -1</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::startBuffering</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::stopBuffering</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">bool</span>
<span class="methodname">Phar::unlinkArchive</span> ( <span
class="methodparam"><span class="type">string</span> `$archive`</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Phar::webPhar</span> (\[ <span
class="methodparam"><span class="type">string</span> `$alias`</span> \[,
<span class="methodparam"><span class="type">string</span> `$index`<span
class="initializer"> = "index.php"</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$f404`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$mimetypes`</span> \[, <span class="methodparam"><span
class="type">callable</span> `$rewrites`</span> \]\]\]\]\] )

}

PharData::addEmptyDir
=====================

Add an empty directory to the tar/zip archive

### 说明

<span class="type">void</span> <span
class="methodname">PharData::addEmptyDir</span> ( <span
class="methodparam"><span class="type">string</span> `$dirname`</span> )

With this method, an empty directory is created with path *dirname*.
This method is similar to <span
class="function">ZipArchive::addEmptyDir</span>.

### 参数

`dirname`  
The name of the empty directory to create in the phar archive

### 返回值

no return value, exception is thrown on failure.

### 范例

**示例 \#1 A <span class="function">PharData::addEmptyDir</span>
example**

``` php
<?php
try {
    $a = new PharData('/path/to/my.tar');

    $a->addEmptyDir('/full/path/to/file');
    // demonstrates how this file is stored
    $b = $a['full/path/to/file']->isDir();
} catch (Exception $e) {
    // handle errors here
}
?>
```

### 参见

-   <span class="function">Phar::addEmptyDir</span>
-   <span class="function">PharData::addFile</span>
-   <span class="function">PharData::addFromString</span>

PharData::addFile
=================

Add a file from the filesystem to the tar/zip archive

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::addFile</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$localname`</span> \] )

With this method, any file or URL can be added to the tar/zip archive.
If the optional second parameter *localname* is specified, the file will
be stored in the archive with that name, otherwise the *file* parameter
is used as the path to store within the archive. URLs must have a
localname or an exception is thrown. This method is similar to <span
class="function">ZipArchive::addFile</span>.

### 参数

`file`  
Full or relative path to a file on disk to be added to the phar archive.

`localname`  
Path that the file will be stored in the archive.

### 返回值

no return value, exception is thrown on failure.

### 范例

**示例 \#1 A <span class="function">PharData::addFile</span> example**

``` php
<?php
try {
    $a = new PharData('/path/to/my.tar');

    $a->addFile('/full/path/to/file');
    // demonstrates how this file is stored
    $b = $a['full/path/to/file']->getContent();

    $a->addFile('/full/path/to/file', 'my/file.txt');
    $c = $a['my/file.txt']->getContent();

    // demonstrate URL usage
    $a->addFile('http://www.example.com', 'example.html');
} catch (Exception $e) {
    // handle errors here
}
?>
```

### 参见

-   <span class="function">PharData::offsetSet</span>
-   <span class="function">Phar::addFile</span>
-   <span class="function">PharData::addFromString</span>
-   <span class="function">PharData::addEmptyDir</span>

PharData::addFromString
=======================

Add a file from the filesystem to the tar/zip archive

### 说明

<span class="type">void</span> <span
class="methodname">PharData::addFromString</span> ( <span
class="methodparam"><span class="type">string</span> `$localname`</span>
, <span class="methodparam"><span class="type">string</span>
`$contents`</span> )

With this method, any string can be added to the tar/zip archive. The
file will be stored in the archive with *localname* as its path. This
method is similar to <span
class="function">ZipArchive::addFromString</span>.

### 参数

`localname`  
Path that the file will be stored in the archive.

`contents`  
The file contents to store

### 返回值

no return value, exception is thrown on failure.

### 范例

**示例 \#1 A <span class="function">PharData::addFromString</span>
example**

``` php
<?php
try {
    $a = new PharData('/path/to/my.tar');

    $a->addFromString('path/to/file.txt', 'my simple file');
    $b = $a['path/to/file.txt']->getContent();

    // to add contents from a stream handle for large files, use offsetSet()
    $c = fopen('/path/to/hugefile.bin');
    $a['largefile.bin'] = $c;
    fclose($c);
} catch (Exception $e) {
    // handle errors here
}
?>
```

### 参见

-   <span class="function">PharData::offsetSet</span>
-   <span class="function">Phar::addFromString</span>
-   <span class="function">PharData::addFile</span>
-   <span class="function">PharData::addEmptyDir</span>

PharData::buildFromDirectory
============================

Construct a tar/zip archive from the files within a directory

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Phar::buildFromDirectory</span> ( <span
class="methodparam"><span class="type">string</span> `$base_dir`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$regex`</span> \] )

Populate a tar/zip archive from directory contents. The optional second
parameter is a regular expression (pcre) that is used to exclude files.
Any filename that matches the regular expression will be included, all
others will be excluded. For more fine-grained control, use <span
class="function">PharData::buildFromIterator</span>.

### 参数

`base_dir`  
The full or relative path to the directory that contains all files to
add to the archive.

`regex`  
An optional pcre regular expression that is used to filter the list of
files. Only file paths matching the regular expression will be included
in the archive.

### 返回值

<span class="function">Phar::buildFromDirectory</span> returns an
associative array mapping internal path of file to the full path of the
file on the filesystem.

### 错误／异常

This method throws <span class="classname">BadMethodCallException</span>
when unable to instantiate the internal directory iterators, or a <span
class="classname">PharException</span> if there were errors saving the
phar archive.

### 范例

**示例 \#1 A <span class="function">PharData::buildFromDirectory</span>
example**

``` php
<?php
$phar = new PharData('project.tar');
// add all files in the project
$phar->buildFromDirectory(dirname(__FILE__) . '/project');

$phar2 = new PharData('project2.zip');
// add all files in the project, only include php files
$phar2->buildFromDirectory(dirname(__FILE__) . '/project', '/\.php$/');
?>
```

### 参见

-   <span class="function">Phar::buildFromDirectory</span>
-   <span class="function">PharData::buildFromIterator</span>

PharData::buildFromIterator
===========================

Construct a tar or zip archive from an iterator

### 说明

<span class="type">array</span> <span
class="methodname">PharData::buildFromIterator</span> ( <span
class="methodparam"><span class="type">Iterator</span> `$iter`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$base_directory`</span> \] )

Populate a tar or zip archive from an iterator. Two styles of iterators
are supported, iterators that map the filename within the tar/zip to the
name of a file on disk, and iterators like DirectoryIterator that return
SplFileInfo objects. For iterators that return SplFileInfo objects, the
second parameter is required.

### 范例

**示例 \#1 A <span class="function">PharData::buildFromIterator</span>
with SplFileInfo**

For most tar/zip archives, the archive will reflect an actual directory
layout, and the second style is the most useful. For instance, to create
a tar/zip archive containing the files in this sample directory layout:

``` examples
/path/to/project/
                 config/
                        dist.xml
                        debug.xml
                 lib/
                     file1.php
                     file2.php
                 src/
                     processthing.php
                 www/
                     index.php
                 cli/
                     index.php
```

This code could be used to add these files to the "project.tar" tar
archive:

``` php
<?php
$phar = new PharData('project.tar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new RecursiveDirectoryIterator('/path/to/project')),
    '/path/to/project');
?>
```

The file *project.tar* can then be used immediately. <span
class="function">PharData::buildFromIterator</span> does not set values
such as compression, metadata, and this can be done after creating the
tar/zip archive.

As an interesting note, <span
class="function">PharData::buildFromIterator</span> can also be used to
copy the contents of an existing phar, tar or zip archive, as the
PharData object descends from <span
class="classname">DirectoryIterator</span>:

``` php
<?php
$phar = new PharData('project.tar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new Phar('/path/to/anotherphar.phar')),
    'phar:///path/to/anotherphar.phar/path/to/project');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

**示例 \#2 A <span class="function">PharData::buildFromIterator</span>
with other iterators**

The second form of the iterator can be used with any iterator that
returns a key =\> value mapping, such as an <span
class="classname">ArrayIterator</span>:

``` php
<?php
$phar = new PharData('project.tar');
$phar->buildFromIterator(
    new ArrayIterator(
     array(
        'internal/file.php' => dirname(__FILE__) . '/somefile.php',
        'another/file.jpg' => fopen('/path/to/bigfile.jpg', 'rb'),
     )));
?>
```

### 参数

`iter`  
Any iterator that either associatively maps tar/zip file to location or
returns SplFileInfo objects

`base_directory`  
For iterators that return SplFileInfo objects, the portion of each
file's full path to remove when adding to the tar/zip archive

### 返回值

<span class="function">PharData::buildFromIterator</span> returns an
associative array mapping internal path of file to the full path of the
file on the filesystem.

### 错误／异常

This method returns <span
class="classname">UnexpectedValueException</span> when the iterator
returns incorrect values, such as an integer key instead of a string, a
<span class="classname">BadMethodCallException</span> when an
SplFileInfo-based iterator is passed without a `base_directory`
parameter, or a <span class="classname">PharException</span> if there
were errors saving the phar archive.

### 参见

-   <span class="function">Phar::buildFromIterator</span>

PharData::compress
==================

Compresses the entire tar/zip archive using Gzip or Bzip2 compression

### 说明

<span class="type">PharData</span> <span
class="methodname">PharData::compress</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$extension`</span> \] )

For tar archives, this method compresses the entire archive using gzip
compression or bzip2 compression. The resulting file can be processed
with the gunzip command/bunzip command, or accessed directly and
transparently with the Phar extension.

For zip archives, this method fails with an exception. The
<a href="/ref/zlib.html" class="link">zlib</a> extension must be enabled
to compress with gzip compression, the
<a href="/ref/bzip2.html" class="link">bzip2</a> extension must be
enabled in order to compress with bzip2 compression.

In addition, this method automatically renames the archive, appending
*.gz*, *.bz2* or removing the extension if passed *Phar::NONE* to remove
compression. Alternatively, a file extension may be specified with the
second parameter.

### 参数

`compression`  
Compression must be one of *Phar::GZ*, *Phar::BZ2* to add compression,
or *Phar::NONE* to remove compression.

`extension`  
By default, the extension is *.tar.gz* or *.tar.bz2* for compressing a
tar, and *.tar* for decompressing.

### 返回值

A <span class="classname">PharData</span> object is returned.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/ref/zlib.html" class="link">zlib</a> extension is not
available, or the <a href="/ref/bzip2.html" class="link">bzip2</a>
extension is not enabled.

### 范例

**示例 \#1 A <span class="function">PharData::compress</span> example**

``` php
<?php
$p = new PharData('/path/to/my.tar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
$p1 = $p->compress(Phar::GZ); // copies to /path/to/my.tar.gz
$p2 = $p->compress(Phar::BZ2); // copies to /path/to/my.tar.bz2
$p3 = $p2->compress(Phar::NONE); // exception: /path/to/my.tar already exists
?>
```

### 参见

-   <span class="function">Phar::compress</span>

PharData::compressFiles
=======================

Compresses all files in the current tar/zip archive

### 说明

<span class="type">void</span> <span
class="methodname">PharData::compressFiles</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
)

For tar-based archives, this method throws a <span
class="classname">BadMethodCallException</span>, as compression of
individual files within a tar archive is not supported by the file
format. Use <span class="function">PharData::compress</span> to compress
an entire tar-based archive.

For Zip-based archives, this method compresses all files in the archive
using the specified compression. The
<a href="/ref/zlib.html" class="link">zlib</a> or
<a href="/ref/bzip2.html" class="link">bzip2</a> extensions must be
enabled to take advantage of this feature. In addition, if any files are
already compressed using bzip2/zlib compression, the respective
extension must be enabled in order to decompress the files prior to
re-compressing.

### 参数

`compression`  
Compression must be one of *Phar::GZ*, *Phar::BZ2* to add compression,
or *Phar::NONE* to remove compression.

### 返回值

没有返回值。

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
is on, the <a href="/ref/zlib.html" class="link">zlib</a> extension is
not available, or if any files are compressed using bzip2 compression
and the <a href="/ref/bzip2.html" class="link">bzip2</a> extension is
not enabled.

### 范例

**示例 \#1 A <span class="function">PharData::compressFiles</span>
example**

``` php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
$p->compressFiles(Phar::GZ);
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
?>
```

以上例程会输出：

    string(10) "myfile.txt"
    bool(false)
    bool(false)
    bool(false)
    string(11) "myfile2.txt"
    bool(false)
    bool(false)
    bool(false)
    string(10) "myfile.txt"
    int(4096)
    bool(false)
    bool(true)
    string(11) "myfile2.txt"
    int(4096)
    bool(false)
    bool(true)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">PharData::decompressFiles</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">PharData::compress</span>
-   <span class="function">PharData::decompress</span>

PharData::\_\_construct
=======================

Construct a non-executable tar or zip archive object

### 说明

<span class="methodname">PharData::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$fname`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$alias`</span> \[, <span class="methodparam"><span
class="type">int</span> `$format`<span class="initializer"> =
**`Phar::TAR`**</span></span> \]\]\] )

### 参数

`fname`  
Path to an existing tar/zip archive or to-be-created archive

`flags`  
Flags to pass to <span class="classname">Phar</span> parent class <span
class="classname">RecursiveDirectoryIterator</span>.

`alias`  
Alias with which this Phar archive should be referred to in calls to
stream functionality.

`format`  
One of the
<a href="/phar/constants.html#Phar%20file%20format%20constants" class="link">file format constants</a>
available within the <span class="classname">Phar</span> class.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if called
twice; <span class="classname">UnexpectedValueException</span> if the
Phar archive can't be opened.

### 范例

**示例 \#1 A <span class="function">PharData::\_\_construct</span>
example**

``` php
<?php
try {
    $p = new PharData('/path/to/my.tar', Phar::CURRENT_AS_FILEINFO | Phar::KEY_AS_FILENAME);
} catch (UnexpectedValueException $e) {
    die('Could not open my.tar');
} catch (BadMethodCallException $e) {
    echo 'technically, this cannot happen';
}
echo file_get_contents('phar:///path/to/my.tar/example.txt');
?>
```

PharData::convertToData
=======================

Convert a phar archive to a non-executable tar or zip file

### 说明

<span class="type">PharData</span> <span
class="methodname">PharData::convertToData</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$compression`</span> \[, <span class="methodparam"><span
class="type">string</span> `$extension`</span> \]\]\] )

This method is used to convert a non-executable tar or zip archive to
another non-executable format.

If no changes are specified, this method throws a <span
class="classname">BadMethodCallException</span>. This method should be
used to convert a tar archive to zip format or vice-versa. Although it
is possible to simply change the compression of a tar archive using this
method, it is better to use the <span
class="function">PharData::compress</span> method for logical
consistency.

If successful, the method creates a new archive on disk and returns a
<span class="classname">PharData</span> object. The old archive is not
removed from disk, and should be done manually after the process has
finished.

### 参数

`format`  
This should be one of *Phar::TAR* or *Phar::ZIP*. If set to **`null`**,
the existing file format will be preserved.

`compression`  
This should be one of *Phar::NONE* for no whole-archive compression,
*Phar::GZ* for zlib-based compression, and *Phar::BZ2* for bzip-based
compression.

`extension`  
This parameter is used to override the default file extension for a
converted archive. Note that *.phar* cannot be used anywhere in the
filename for a non-executable tar or zip archive.

If converting to a tar-based phar archive, the default extensions are
*.tar*, *.tar.gz*, and *.tar.bz2* depending on specified compression.
For zip-based archives, the default extension is *.zip*.

### 返回值

The method returns a <span class="classname">PharData</span> object on
success and throws an exception on failure.

### 错误／异常

This method throws <span class="classname">BadMethodCallException</span>
when unable to compress, an unknown compression method has been
specified, the requested archive is buffering with <span
class="function">Phar::startBuffering</span> and has not concluded with
<span class="function">Phar::stopBuffering</span>, and a <span
class="classname">PharException</span> if any problems are encountered
during the phar creation process.

### 范例

**示例 \#1 A <span class="function">PharData::convertToData</span>
example**

Using PharData::convertToData():

``` php
<?php
try {
    $tarphar = new PharData('myphar.tar');
    // note that myphar.tar is *not* unlinked
    // convert it to the non-executable tar file format
    // creates myphar.zip
    $zip = $tarphar->convertToData(Phar::ZIP);
    // create myphar.tbz
    $tgz = $zip->convertToData(Phar::TAR, Phar::BZ2, '.tbz');
    // creates myphar.phar.tgz
    $phar = $tarphar->convertToData(Phar::PHAR); // throws exception
} catch (Exception $e) {
    // handle the error here
}
?>
```

### 参见

-   <span class="function">Phar::convertToExecutable</span>
-   <span class="function">Phar::convertToData</span>
-   <span class="function">PharData::convertToExecutable</span>

PharData::convertToExecutable
=============================

Convert a non-executable tar/zip archive to an executable phar archive

### 说明

<span class="type">Phar</span> <span
class="methodname">PharData::convertToExecutable</span> (\[ <span
class="methodparam"><span class="type">int</span> `$format`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$compression`</span> \[, <span class="methodparam"><span
class="type">string</span> `$extension`</span> \]\]\] )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

This method is used to convert a non-executable tar or zip archive to an
executable phar archive. Any of the three executable file formats (phar,
tar or zip) can be used, and whole-archive compression can also be
performed.

If no changes are specified, this method throws a <span
class="classname">BadMethodCallException</span>.

If successful, the method creates a new archive on disk and returns a
<span class="classname">Phar</span> object. The old archive is not
removed from disk, and should be done manually after the process has
finished.

### 参数

`format`  
This should be one of *Phar::PHAR*, *Phar::TAR*, or *Phar::ZIP*. If set
to **`null`**, the existing file format will be preserved.

`compression`  
This should be one of *Phar::NONE* for no whole-archive compression,
*Phar::GZ* for zlib-based compression, and *Phar::BZ2* for bzip-based
compression.

`extension`  
This parameter is used to override the default file extension for a
converted archive. Note that all zip- and tar-based phar archives must
contain *.phar* in their file extension in order to be processed as a
phar archive.

If converting to a phar-based archive, the default extensions are
*.phar*, *.phar.gz*, or *.phar.bz2* depending on the specified
compression. For tar-based phar archives, the default extensions are
*.phar.tar*, *.phar.tar.gz*, and *.phar.tar.bz2*. For zip-based phar
archives, the default extension is *.phar.zip*.

### 返回值

The method returns a <span class="classname">Phar</span> object on
success and throws an exception on failure.

### 错误／异常

This method throws <span class="classname">BadMethodCallException</span>
when unable to compress, an unknown compression method has been
specified, the requested archive is buffering with <span
class="function">Phar::startBuffering</span> and has not concluded with
<span class="function">Phar::stopBuffering</span>, an <span
class="classname">UnexpectedValueException</span> if write support is
disabled, and a <span class="classname">PharException</span> if any
problems are encountered during the phar creation process.

### 范例

**示例 \#1 A <span class="function">PharData::convertToExecutable</span>
example**

Using PharData::convertToExecutable():

``` php
<?php
try {
    $tarphar = new PharData('myphar.tar');
    // convert it to the phar file format
    // note that myphar.tar is *not* unlinked
    $phar = $tarphar->convertToExecutable(Phar::PHAR); // creates myphar.phar
    $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
    // creates myphar.phar.tgz
    $compressed = $tarphar->convertToExecutable(Phar::TAR, Phar::GZ, '.phar.tgz');
} catch (Exception $e) {
    // handle the error here
}
?>
```

### 参见

-   <span class="function">Phar::convertToExecutable</span>
-   <span class="function">Phar::convertToData</span>
-   <span class="function">PharData::convertToData</span>

PharData::copy
==============

Copy a file internal to the phar archive to another new file within the
phar

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::copy</span> ( <span
class="methodparam"><span class="type">string</span> `$oldfile`</span> ,
<span class="methodparam"><span class="type">string</span>
`$newfile`</span> )

Copy a file internal to the tar/zip archive to another new file within
the same archive. This is an object-oriented alternative to using <span
class="function">copy</span> with the phar stream wrapper.

### 参数

`oldfile`  

`newfile`  

### 返回值

returns **`true`** on success, but it is safer to encase method call in
a try/catch block and assume success if no exception is thrown.

### 错误／异常

throws <span class="classname">UnexpectedValueException</span> if the
source file does not exist, the destination file already exists, write
access is disabled, opening either file fails, reading the source file
fails, or a <span class="classname">PharException</span> if writing the
changes to the phar fails.

### 范例

**示例 \#1 A <span class="function">PharData::copy</span> example**

This example shows using <span class="function">PharData::copy</span>
and the equivalent stream wrapper performance of the same thing. The
primary difference between the two approaches is error handling. All
PharData methods throw exceptions, whereas the stream wrapper uses <span
class="function">trigger\_error</span>.

``` php
<?php
try {
    $phar = new PharData('myphar.tar');
    $phar['a'] = 'hi';
    $phar->copy('a', 'b');
    echo $phar['b']; // outputs "phar://myphar.tar/b"
} catch (Exception $e) {
    // handle error
}

// the stream wrapper equivalent of the above code.
// E_WARNINGS are triggered on error rather than exceptions.
copy('phar://myphar.tar/a', 'phar//myphar.tar/c');
echo file_get_contents('phar://myphar.tar/c'); // outputs "hi"
?>
```

PharData::decompress
====================

Decompresses the entire Phar archive

### 说明

<span class="type">PharData</span> <span
class="methodname">PharData::decompress</span> (\[ <span
class="methodparam"><span class="type">string</span> `$extension`</span>
\] )

For tar-based archives, this method decompresses the entire archive.

For Zip-based archives, this method fails with an exception. The
<a href="/ref/zlib.html" class="link">zlib</a> extension must be enabled
to decompress an archive compressed with gzip compression, and the
<a href="/ref/bzip2.html" class="link">bzip2</a> extension must be
enabled in order to decompress an archive compressed with bzip2
compression.

In addition, this method automatically renames the file extension of the
archive, *.tar* by default. Alternatively, a file extension may be
specified with the `extension` parameter.

### 参数

`extension`  
For decompressing, the default file extension is *.tar*. Use this
parameter to specify another file extension. Be aware that only
executable archives can contain *.phar* in their filename.

### 返回值

A <span class="classname">PharData</span> object is returned.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/ref/zlib.html" class="link">zlib</a> extension is not
available, or the <a href="/ref/bzip2.html" class="link">bzip2</a>
extension is not enabled.

### 范例

**示例 \#1 A <span class="function">PharData::decompress</span>
example**

``` php
<?php
$p = new PharData('/path/to/my.tar.gz');
$p->decompress(); // creates /path/to/my.tar
?>
```

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">PharData::compress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">PharData::compress</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">PharData::compressFiles</span>
-   <span class="function">PharData::decompressFiles</span>

PharData::decompressFiles
=========================

Decompresses all files in the current zip archive

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::decompressFiles</span> ( <span
class="methodparam">void</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

For tar-based archives, this method throws a <span
class="classname">BadMethodCallException</span>, as compression of
individual files within a tar archive is not supported by the file
format. Use <span class="function">PharData::compress</span> to compress
an entire tar-based archive.

For Zip-based archives, this method decompresses all files in the
archive. The <a href="/ref/zlib.html" class="link">zlib</a> or
<a href="/ref/bzip2.html" class="link">bzip2</a> extensions must be
enabled to take advantage of this feature if any files are compressed
using bzip2/zlib compression.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/ref/zlib.html" class="link">zlib</a> extension is not
available, or if any files are compressed using bzip2 compression and
the <a href="/ref/bzip2.html" class="link">bzip2</a> extension is not
enabled.

### 范例

**示例 \#1 A <span class="function">PharData::decompressFiles</span>
example**

``` php
<?php
$p = new PharData('/path/to/my.zip');
$p['myfile.txt'] = 'hi';
$p['myfile2.txt'] = 'hi';
$p->compressFiles(Phar::GZ);
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
$p->decompressFiles();
foreach ($p as $file) {
    var_dump($file->getFileName());
    var_dump($file->isCompressed());
    var_dump($file->isCompressed(Phar::BZ2));
    var_dump($file->isCompressed(Phar::GZ));
}
?>
```

以上例程会输出：

    string(10) "myfile.txt"
    int(4096)
    bool(false)
    bool(true)
    string(11) "myfile2.txt"
    int(4096)
    bool(false)
    bool(true)
    string(10) "myfile.txt"
    bool(false)
    bool(false)
    bool(false)
    string(11) "myfile2.txt"
    bool(false)
    bool(false)
    bool(false)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">PharData::compressFiles</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">PharData::compress</span>
-   <span class="function">PharData::decompress</span>

PharData::delMetadata
=====================

Deletes the global metadata of a zip archive

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::delMetadata</span> ( <span
class="methodparam">void</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Deletes the global metadata of the zip archive

### 参数

### 返回值

returns **`true`** on success, but it is better to check for thrown
exception, and assume success if none is thrown.

### 错误／异常

Throws <span class="classname">PharException</span> if errors occur
while flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">PharData::delMetaData</span>
example**

``` php
<?php
try {
    $phar = new PharData('myphar.zip');
    var_dump($phar->getMetadata());
    $phar->setMetadata("hi there");
    var_dump($phar->getMetadata());
    $phar->delMetadata();
    var_dump($phar->getMetadata());
} catch (Exception $e) {
    // handle errors
}
?>
```

以上例程会输出：

    NULL
    string(8) "hi there"
    NULL

### 参见

-   <span class="function">Phar::delMetadata</span>

PharData::delete
================

Delete a file within a tar/zip archive

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::delete</span> ( <span
class="methodparam"><span class="type">string</span> `$entry`</span> )

Delete a file within an archive. This is the functional equivalent of
calling <span class="function">unlink</span> on the stream wrapper
equivalent, as shown in the example below.

### 参数

`entry`  
Path within an archive to the file to delete.

### 返回值

returns **`true`** on success, but it is better to check for thrown
exception, and assume success if none is thrown.

### 错误／异常

Throws <span class="classname">PharException</span> if errors occur
while flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">PharData::delete</span> example**

``` php
<?php
try {
    $phar = new PharData('myphar.zip');
    $phar->delete('unlink/me.php');
    // this is equivalent to:
    unlink('phar://myphar.phar/unlink/me.php');
} catch (Exception $e) {
    // handle errors
}
?>
```

### 参见

-   <span class="function">Phar::delete</span>

PharData::extractTo
===================

Extract the contents of a tar/zip archive to a directory

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::extractTo</span> ( <span
class="methodparam"><span class="type">string</span> `$pathto`</span>
\[, <span class="methodparam"><span class="type"><span
class="type">string</span><span class="type">array</span><span
class="type">null</span></span> `$files`<span class="initializer"> =
**`null`**</span></span> \[, <span class="methodparam"><span
class="type">bool</span> `$overwrite`<span class="initializer"> =
**`false`**</span></span> \]\] )

Extract all files within a tar/zip archive to disk. Extracted files and
directories preserve permissions as stored in the archive. The optional
parameters allow optional control over which files are extracted, and
whether existing files on disk can be overwritten. The second parameter
*files* can be either the name of a file or directory to extract, or an
array of names of files and directories to extract. By default, this
method will not overwrite existing files, the third parameter can be set
to true to enable overwriting of files. This method is similar to <span
class="function">ZipArchive::extractTo</span>.

### 参数

`pathto`  
Path to extract the given *files* to

`files`  
The name of a file or directory to extract, or an array of
files/directories to extract

`overwrite`  
Set to **`true`** to enable overwriting existing files

### 返回值

returns **`true`** on success, but it is better to check for thrown
exception, and assume success if none is thrown.

### 错误／异常

Throws <span class="classname">PharException</span> if errors occur
while flushing changes to disk.

### 范例

**示例 \#1 A <span class="function">PharData::extractTo</span> example**

``` php
<?php
try {
    $phar = new PharData('myphar.tar');
    $phar->extractTo('/full/path'); // extract all files
    $phar->extractTo('/another/path', 'file.txt'); // extract only file.txt
    $phar->extractTo('/this/path',
        array('file1.txt', 'file2.txt')); // extract 2 files only
    $phar->extractTo('/third/path', null, true); // extract all files, and overwrite
} catch (Exception $e) {
    // handle errors
}
?>
```

### 参见

-   <span class="function">Phar::extractTo</span>

PharData::isWritable
====================

Returns true if the tar/zip archive can be modified

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::isWritable</span> ( <span
class="methodparam">void</span> )

This method returns **`true`** if the tar/zip archive on disk is not
read-only. Unlike <span class="function">Phar::isWritable</span>,
data-only tar/zip archives can be modified even if *phar.readonly* is
set to *1*.

### 参数

No parameters.

### 返回值

Returns **`true`** if the tar/zip archive can be modified

### 参见

-   <span class="function">Phar::canWrite</span>
-   <span class="function">Phar::isWritable</span>

PharData::offsetSet
===================

Set the contents of a file within the tar/zip to those of an external
file or string

### 说明

<span class="type">void</span> <span
class="methodname">PharData::offsetSet</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

This is an implementation of the <span
class="interfacename">ArrayAccess</span> interface allowing direct
manipulation of the contents of a tar/zip archive using array access
brackets. offsetSet is used for modifying an existing file, or adding a
new file to a tar/zip archive.

### 参数

`offset`  
The filename (relative path) to modify in a tar or zip archive.

`value`  
Content of the file.

### 返回值

No return values.

### 错误／异常

Throws <span class="classname">PharException</span> if there are any
problems flushing changes made to the tar/zip archive to disk.

### 范例

**示例 \#1 A <span class="function">PharData::offsetSet</span> example**

offsetSet should not be accessed directly, but instead used via array
access with the *\[\]* operator.

``` php
<?php
$p = new PharData('/path/to/my.tar');
try {
    // calls offsetSet
    $p['file.txt'] = 'Hi there';
} catch (Exception $e) {
    echo 'Could not modify file.txt:', $e;
}
?>
```

### 参见

-   <span class="function">Phar::offsetSet</span>

PharData::offsetUnset
=====================

Remove a file from a tar/zip archive

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::offsetUnset</span> ( <span
class="methodparam"><span class="type">string</span> `$offset`</span> )

This is an implementation of the <span
class="interfacename">ArrayAccess</span> interface allowing direct
manipulation of the contents of a tar/zip archive using array access
brackets. offsetUnset is used for deleting an existing file, and is
called by the <span class="function">unset</span> language construct.

### 参数

`offset`  
The filename (relative path) to modify in the tar/zip archive.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws <span class="classname">PharException</span> if there are any
problems flushing changes made to the tar/zip archive to disk.

### 范例

**示例 \#1 A <span class="function">PharData::offsetUnset</span>
example**

``` php
<?php
$p = new PharData('/path/to/my.zip');
try {
    // deletes file.txt from my.zip by calling offsetUnset
    unset($p['file.txt']);
} catch (Exception $e) {
    echo 'Could not delete file.txt: ', $e;
}
?>
```

### 参见

-   <span class="function">Phar::offsetUnset</span>

PharData::setAlias
==================

Dummy function (Phar::setAlias is not valid for PharData)

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::setAlias</span> ( <span
class="methodparam"><span class="type">string</span> `$alias`</span> )

Non-executable tar/zip archives cannot have an alias, so this method
simply throws an exception.

### 参数

`alias`  
A shorthand string that this archive can be referred to in *phar* stream
wrapper access. This parameter is ignored.

### 返回值

### 错误／异常

Throws <span class="classname">PharException</span> on all method calls

### 参见

-   <span class="function">Phar::setAlias</span>

PharData::setDefaultStub
========================

Dummy function (Phar::setDefaultStub is not valid for PharData)

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::setDefaultStub</span> (\[ <span
class="methodparam"><span class="type">string</span> `$index`</span> \[,
<span class="methodparam"><span class="type">string</span>
`$webindex`</span> \]\] )

Non-executable tar/zip archives cannot have a stub, so this method
simply throws an exception.

### 参数

`index`  
Relative path within the phar archive to run if accessed on the
command-line

`webindex`  
Relative path within the phar archive to run if accessed through a web
browser

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws <span class="classname">PharException</span> on all method calls

### 参见

-   <span class="function">Phar::setDefaultStub</span>

Phar::setMetadata
=================

Sets phar archive meta-data

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setMetadata</span> ( <span
class="methodparam"><span class="type">mixed</span> `$metadata`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

<span class="function">Phar::setMetadata</span> should be used to store
customized data that describes something about the phar archive as a
complete entity. <span class="function">PharFileInfo::setMetadata</span>
should be used for file-specific meta-data. Meta-data can slow down the
performance of loading a phar archive if the data is large.

Some possible uses for meta-data include specifying which file within
the archive should be used to bootstrap the archive, or the location of
a file manifest like
<a href="https://pear.php.net/" class="link external">» PEAR</a>'s
package.xml file. However, any useful data that describes the phar
archive may be stored.

### 参数

`metadata`  
Any PHP variable containing information to store that describes the phar
archive

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">Phar::setMetadata</span> example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.php'] = '<?php echo "hello"';
    $p->setMetadata(array('bootstrap' => 'file.php'));
    var_dump($p->getMetadata());
} catch (Exception $e) {
    echo 'Could not create and/or modify phar:', $e;
}
?>
```

以上例程会输出：

    array(1) {
      ["bootstrap"]=>
      string(8) "file.php"
    }

### 参见

-   <span class="function">Phar::getMetadata</span>
-   <span class="function">Phar::delMetadata</span>
-   <span class="function">Phar::hasMetadata</span>

Phar::setSignatureAlgorithm
===========================

Set the signature algorithm for a phar and apply it

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Phar::setSignatureAlgorithm</span> ( <span
class="methodparam"><span class="type">int</span> `$sigtype`</span> )

> **Note**:
>
> 此方法需要 将 `php.ini` 中的 *phar.readonly* 设为 *0* 以适合 <span
> class="classname">Phar</span> 对象. 否则, 将抛出<span
> class="classname">PharException</span>.

Set the signature algorithm for a phar and apply it. The signature
algorithm must be one of *Phar::MD5*, *Phar::SHA1*, *Phar::SHA256*,
*Phar::SHA512*, or *Phar::PGP* (pgp not yet supported and falls back to
SHA-1).

### 参数

`sigtype`  
One of *Phar::MD5*, *Phar::SHA1*, *Phar::SHA256*, *Phar::SHA512*, or
*Phar::PGP*

### 返回值

没有返回值。

### 错误／异常

Throws <span class="classname">UnexpectedValueException</span> for many
errors, <span class="classname">BadMethodCallException</span> if called
for a zip- or a tar-based phar archive, and a <span
class="classname">PharException</span> if any problems occur flushing
changes to disk.

### 参见

-   <span class="function">Phar::getSupportedSignatures</span>
-   <span class="function">Phar::getSignature</span>

PharData::setStub
=================

Dummy function (Phar::setStub is not valid for PharData)

### 说明

<span class="type">bool</span> <span
class="methodname">PharData::setStub</span> ( <span
class="methodparam"><span class="type">string</span> `$stub`</span> \[,
<span class="methodparam"><span class="type">int</span> `$len`<span
class="initializer"> = -1</span></span> \] )

Non-executable tar/zip archives cannot have a stub, so this method
simply throws an exception.

### 参数

`stub`  
A string or an open stream handle to use as the executable stub for this
phar archive. This parameter is ignored.

`len`  

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws <span class="classname">PharException</span> on all method calls

### 参见

-   <span class="function">Phar::setStub</span>

简介
----

The PharFileInfo class provides a high-level interface to the contents
and attributes of a single file within a phar archive.

类摘要
------

**PharFileInfo**

<span class="ooclass"> class **PharFileInfo** </span> <span
class="ooclass"> <span class="modifier">extends</span> **SplFileInfo**
</span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">chmod</span> ( <span class="methodparam"><span
class="type">int</span> `$permissions`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">compress</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
)

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$entry`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">decompress</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">delMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getCRC32</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getCompressedSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">getContent</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">getMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getPharFlags</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasMetadata</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isCRCChecked</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isCompressed</span> (\[ <span
class="methodparam"><span class="type">int</span>
`$compression_type`<span class="initializer"> = 9021976</span></span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">setMetadata</span> ( <span
class="methodparam"><span class="type">mixed</span> `$metadata`</span> )

/\* 继承的方法 \*/

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getATime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getBasename</span> (\[ <span
class="methodparam"><span class="type">string</span> `$suffix`</span> \]
)

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getCTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getExtension</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">SplFileInfo</span> <span
class="methodname">SplFileInfo::getFileInfo</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$class_name`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getFilename</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getGroup</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getInode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getLinkTarget</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getMTime</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getOwner</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">SplFileInfo</span> <span
class="methodname">SplFileInfo::getPathInfo</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$class_name`</span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getPathname</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getPerms</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getRealPath</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SplFileInfo::getSize</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::getType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SplFileInfo::isDir</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SplFileInfo::isExecutable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SplFileInfo::isFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SplFileInfo::isLink</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SplFileInfo::isReadable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SplFileInfo::isWritable</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">SplFileObject</span> <span
class="methodname">SplFileInfo::openFile</span> (\[ <span
class="methodparam"><span class="type">string</span> `$open_mode`<span
class="initializer"> = "r"</span></span> \[, <span
class="methodparam"><span class="type">bool</span>
`$use_include_path`<span class="initializer"> =
**`false`**</span></span> \[, <span class="methodparam"><span
class="type">resource</span> `$context`<span class="initializer"> =
**`null`**</span></span> \]\]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SplFileInfo::setFileClass</span> (\[ <span
class="methodparam"><span class="type">string</span> `$class_name`<span
class="initializer"> = "SplFileObject"</span></span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">SplFileInfo::setInfoClass</span> (\[ <span
class="methodparam"><span class="type">string</span> `$class_name`<span
class="initializer"> = "SplFileInfo"</span></span> \] )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">SplFileInfo::\_\_toString</span> ( <span
class="methodparam">void</span> )

}

PharFileInfo::chmod
===================

Sets file-specific permission bits

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">PharFileInfo::chmod</span> ( <span
class="methodparam"><span class="type">int</span> `$permissions`</span>
)

<span class="function">PharFileInfo::chmod</span> allows setting of the
executable file permissions bit, as well as read-only bits. Writeable
bits are ignored, and set at runtime based on the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable.
As with all functionality that modifies the contents of a phar, the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
must be off in order to succeed if the file is within a <span
class="classname">Phar</span> archive. Files within <span
class="classname">PharData</span> archives do not have this restriction.

### 参数

`permissions`  
permissions (see <span class="function">chmod</span>)

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">PharFileInfo::chmod</span> example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar('brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.sh'] = '#!/usr/local/lib/php
    <?php echo "hi"; ?>';
    // set executable bit
    $p['file.sh']->chmod(0555);
    var_dump($p['file.sh']->isExecutable());
} catch (Exception $e) {
    echo 'Could not create/modify phar: ', $e;
}
?>
```

以上例程会输出：

    bool(true)

PharFileInfo::compress
======================

Compresses the current Phar entry with either zlib or bzip2 compression

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PharFileInfo::compress</span> ( <span
class="methodparam"><span class="type">int</span> `$compression`</span>
)

This method compresses the file inside the Phar archive using either
bzip2 compression or zlib compression. The
<a href="/ref/bzip2.html" class="link">bzip2</a> or
<a href="/ref/zlib.html" class="link">zlib</a> extension must be enabled
to take advantage of this feature. In addition, if the file is already
compressed, the respective extension must be enabled in order to
decompress the file. As with all functionality that modifies the
contents of a phar, the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
must be off in order to succeed if the file is within a <span
class="classname">Phar</span> archive. Files within <span
class="classname">PharData</span> archives do not have this restriction.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
is on, or if the
<a href="/ref/bzip2.html" class="link">bzip2</a>/<a href="/ref/zlib.html" class="link">zlib</a>
extension is not available.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::compress</span>
example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    var_dump($file->isCompressed(Phar::BZ2));
    $p['myfile.txt']->compress(Phar::BZ2);
    var_dump($file->isCompressed(Phar::BZ2));
} catch (Exception $e) {
    echo 'Create/modify operations on my.phar failed: ', $e;
}
?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::decompressFiles</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::decompress</span>
-   <span class="function">Phar::getSupportedCompression</span>

PharFileInfo::\_\_construct
===========================

Construct a Phar entry object

### 说明

<span class="modifier">public</span> <span
class="methodname">PharFileInfo::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$entry`</span> )

This should not be called directly. Instead, a PharFileInfo object is
initialized by calling <span class="function">Phar::offsetGet</span>
through array access.

### 参数

`entry`  
The full url to retrieve a file. If you wish to retrieve the information
for the file *my/file.php* from the phar *boo.phar*, the entry should be
*phar://boo.phar/my/file.php*.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if
<a href="/language/oop5/decon.html#object.construct" class="link">__construct()</a>
is called twice. Throws <span
class="classname">UnexpectedValueException</span> if the phar URL
requested is malformed, the requested phar cannot be opened, or the file
can't be found within the phar.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::\_\_construct</span>
example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['testfile.txt'] = "hi\nthere\ndude";
    $file = $p['testfile.txt'];
    foreach ($file as $line => $text) {
        echo "line number $line: $text";
    }
    // this also works
    $file = new PharFileInfo('phar:///path/to/my.phar/testfile.txt');
    foreach ($file as $line => $text) {
        echo "line number $line: $text";
    }
} catch (Exception $e) {
    echo 'Phar operations failed: ', $e;
}
?>
```

以上例程会输出：

    line number 1: hi
    line number 2: there
    line number 3: dude
    line number 1: hi
    line number 2: there
    line number 3: dude

PharFileInfo::decompress
========================

Decompresses the current Phar entry within the phar

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PharFileInfo::decompress</span> ( <span
class="methodparam">void</span> )

This method decompresses the file inside the Phar archive. Depending on
how the file is compressed, the
<a href="/ref/bzip2.html" class="link">bzip2</a> or
<a href="/ref/zlib.html" class="link">zlib</a> extensions must be
enabled to take advantage of this feature. As with all functionality
that modifies the contents of a phar, the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
must be off in order to succeed if the file is within a <span
class="classname">Phar</span> archive. Files within <span
class="classname">PharData</span> archives do not have this restriction.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
is on, or if the
<a href="/ref/bzip2.html" class="link">bzip2</a>/<a href="/ref/zlib.html" class="link">zlib</a>
extension is not available.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::decompress</span>
example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    $file->compress(Phar::GZ);
    var_dump($file->isCompressed());
    $p['myfile.txt']->decompress();
    var_dump($file->isCompressed());
} catch (Exception $e) {
    echo 'Create/modify failed for my.phar: ', $e;
}
?>
```

以上例程会输出：

    int(4096)
    bool(false)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::compressFiles</span>
-   <span class="function">Phar::decompressFiles</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::decompress</span>
-   <span class="function">Phar::getSupportedCompression</span>

PharFileInfo::delMetadata
=========================

Deletes the metadata of the entry

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PharFileInfo::delMetadata</span> ( <span
class="methodparam">void</span> )

Deletes the metadata of the entry, if any.

### 参数

No parameters.

### 返回值

Returns **`true`** if successful, **`false`** if the entry had no
metadata. As with all functionality that modifies the contents of a
phar, the <a href="/phar/setup.html#" class="link">phar.readonly</a> INI
variable must be off in order to succeed if the file is within a <span
class="classname">Phar</span> archive. Files within <span
class="classname">PharData</span> archives do not have this restriction.

### 错误／异常

Throws <span class="classname">PharException</span> if errors occurred
while flushing changes to disk, and <span
class="classname">BadMethodCallException</span> if write access is
disabled.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::delMetaData</span>
example**

``` php
<?php
try {
    $a = new Phar('myphar.phar');
    $a['hi'] = 'hi';
    var_dump($a['hi']->delMetadata());
    $a['hi']->setMetadata('there');
    var_dump($a['hi']->delMetadata());
    var_dump($a['hi']->delMetadata());
} catch (Exception $e) {
    // handle errors
}
?>
```

以上例程会输出：

    bool(false)
    bool(true)
    bool(false)

### 参见

-   <span class="function">PharFileInfo::setMetadata</span>
-   <span class="function">PharFileInfo::hasMetadata</span>
-   <span class="function">PharFileInfo::getMetadata</span>
-   <span class="function">Phar::setMetadata</span>
-   <span class="function">Phar::hasMetadata</span>
-   <span class="function">Phar::getMetadata</span>

PharFileInfo::getCRC32
======================

Returns CRC32 code or throws an exception if CRC has not been verified

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">PharFileInfo::getCRC32</span> ( <span
class="methodparam">void</span> )

This returns the <span class="function">crc32</span> checksum of the
file within the Phar archive.

### 返回值

The <span class="function">crc32</span> checksum of the file within the
Phar archive.

### 错误／异常

Throws <span class="classname">BadMethodCallException</span> if the file
has not yet had its CRC32 verified. This should be impossible with
normal use, as the CRC is verified upon opening the file for reading or
writing.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::getCRC32</span>
example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    echo $file->getCRC32();
} catch (Exception $e) {
    echo 'Write operations on my.phar.phar failed: ', $e;
}
?>
```

以上例程会输出：

    3633523372

PharFileInfo::getCompressedSize
===============================

Returns the actual size of the file (with compression) inside the Phar
archive

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">PharFileInfo::getCompressedSize</span> ( <span
class="methodparam">void</span> )

This returns the size of the file within the Phar archive. Uncompressed
files will return the same value for getCompressedSize as they will with
<span class="function">filesize</span>

### 返回值

The size in bytes of the file within the Phar archive on disk.

### 范例

**示例 \#1 A <span
class="function">PharFileInfo::getCompressedSize</span> example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    echo $file->getCompressedSize();
} catch (Exception $e) {
    echo 'Write operations failed on my.phar: ', $e;
}
?>
```

以上例程会输出：

    2

### 参见

-   <span class="function">PharFileInfo::isCompressed</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::decompress</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">Phar::decompressFiles</span>
-   <span class="function">Phar::compressFiles</span>

PharFileInfo::getContent
========================

Get the complete file contents of the entry

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">PharFileInfo::getContent</span> ( <span
class="methodparam">void</span> )

This function behaves like <span
class="function">file\_get\_contents</span> but for Phar.

### 参数

此函数没有参数。

### 返回值

Returns the file contents.

PharFileInfo::getMetadata
=========================

Returns file-specific meta-data saved with a file

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">PharFileInfo::getMetadata</span> ( <span
class="methodparam">void</span> )

Return meta-data that was saved in the Phar archive's manifest for this
file.

### 参数

### 返回值

any PHP variable that can be serialized and is stored as meta-data for
the file, or **`null`** if no meta-data is stored.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::getMetadata</span>
example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.txt'] = 'hello';
    $p['file.txt']->setMetadata(array('user' => 'bill', 'mime-type' => 'text/plain'));
    var_dump($p['file.txt']->getMetadata());
} catch (Exception $e) {
    echo 'Could not create/modify brandnewphar.phar: ', $e;
}
?>
```

以上例程会输出：

    array(2) {
      ["user"]=>
      string(4) "bill"
      ["mime-type"]=>
      string(10) "text/plain"
    }

### 参见

-   <span class="function">PharFileInfo::setMetadata</span>
-   <span class="function">PharFileInfo::hasMetadata</span>
-   <span class="function">PharFileInfo::delMetadata</span>
-   <span class="function">Phar::setMetadata</span>
-   <span class="function">Phar::hasMetadata</span>
-   <span class="function">Phar::getMetadata</span>

PharFileInfo::getPharFlags
==========================

Returns the Phar file entry flags

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">PharFileInfo::getPharFlags</span> ( <span
class="methodparam">void</span> )

This returns the flags set in the manifest for a Phar. This will always
return *0* in the current implementation.

### 返回值

The Phar flags (always *0* in the current implementation)

### 范例

**示例 \#1 A <span class="function">PharFileInfo::getPharFlags</span>
example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    var_dump($file->getPharFlags());
} catch (Exception $e) {
    echo 'Could not create/modify my.phar: ', $e;
}
?>
```

以上例程会输出：

    int(0)

PharFileInfo::hasMetadata
=========================

Returns the metadata of the entry

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PharFileInfo::hasMetadata</span> ( <span
class="methodparam">void</span> )

Returns the metadata of a file within a phar archive.

### 参数

No parameters.

### 返回值

Returns **`false`** if no metadata is set or is **`null`**, **`true`**
if metadata is not **`null`**

### 参见

-   <span class="function">PharFileInfo::setMetadata</span>
-   <span class="function">PharFileInfo::getMetadata</span>
-   <span class="function">PharFileInfo::delMetadata</span>
-   <span class="function">Phar::setMetadata</span>
-   <span class="function">Phar::hasMetadata</span>
-   <span class="function">Phar::getMetadata</span>

PharFileInfo::isCRCChecked
==========================

Returns whether file entry has had its CRC verified

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PharFileInfo::isCRCChecked</span> ( <span
class="methodparam">void</span> )

This returns whether a file within a Phar archive has had its CRC
verified.

### 返回值

**`true`** if the file has had its CRC verified, **`false`** if not.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::isCRCChecked</span>
example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    var_dump($file->isCRCChecked());
} catch (Exception $e) {
    echo 'Create/modify operations failed on my.phar: ', $e;
}
?>
```

以上例程会输出：

    bool(true)

PharFileInfo::isCompressed
==========================

Returns whether the entry is compressed

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">PharFileInfo::isCompressed</span> (\[ <span
class="methodparam"><span class="type">int</span>
`$compression_type`<span class="initializer"> = 9021976</span></span> \]
)

This returns whether a file is compressed within a Phar archive with
either Gzip or Bzip2 compression.

### 参数

`compression_type`  
One of **`Phar::GZ`** or **`Phar::BZ2`**, defaults to any compression.

### 返回值

**`true`** if the file is compressed within the Phar archive,
**`false`** if not.

### 范例

**示例 \#1 A <span class="function">PharFileInfo::isCompressed</span>
example**

``` php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $p['myfile2.txt'] = 'hi';
    $p['myfile2.txt']->setCompressedGZ();
    $file = $p['myfile.txt'];
    $file2 = $p['myfile2.txt'];
    var_dump($file->isCompressed());
    var_dump($file2->isCompressed());
} catch (Exception $e) {
    echo 'Create/modify on phar my.phar failed: ', $e;
}
?>
```

以上例程会输出：

    bool(false)
    bool(true)

### 参见

-   <span class="function">PharFileInfo::getCompressedSize</span>
-   <span class="function">PharFileInfo::decompress</span>
-   <span class="function">PharFileInfo::compress</span>
-   <span class="function">Phar::decompress</span>
-   <span class="function">Phar::compress</span>
-   <span class="function">Phar::canCompress</span>
-   <span class="function">Phar::isCompressed</span>
-   <span class="function">Phar::getSupportedCompression</span>
-   <span class="function">Phar::decompressFiles</span>
-   <span class="function">Phar::compressFiles</span>

PharFileInfo::setMetadata
=========================

Sets file-specific meta-data saved with a file

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">PharFileInfo::setMetadata</span> ( <span
class="methodparam"><span class="type">mixed</span> `$metadata`</span> )

<span class="function">PharFileInfo::setMetadata</span> should only be
used to store customized data in a file that cannot be represented with
existing information stored with a file. Meta-data can significantly
slow down the performance of loading a phar archive if the data is
large, or if there are many files containing meta-data. It is important
to note that file permissions are natively supported inside a phar; it
is possible to set them with the <span
class="function">PharFileInfo::chmod</span> method. As with all
functionality that modifies the contents of a phar, the
<a href="/phar/setup.html#" class="link">phar.readonly</a> INI variable
must be off in order to succeed if the file is within a <span
class="classname">Phar</span> archive. Files within <span
class="classname">PharData</span> archives do not have this restriction.

Some possible uses for meta-data include passing a user/group that
should be set when a file is extracted from the phar to disk. Other uses
could include explicitly specifying a MIME type to return. However, any
useful data that describes a file, but should not be contained inside of
it may be stored.

### 参数

`metadata`  
Any PHP variable containing information to store alongside a file

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">PharFileInfo::setMetadata</span>
example**

``` php
<?php
// make sure it doesn't exist
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.txt'] = 'hello';
    $p['file.txt']->setMetadata(array('user' => 'bill', 'mime-type' => 'text/plain'));
    var_dump($p['file.txt']->getMetaData());
} catch (Exception $e) {
    echo 'Could not create/modify phar: ', $e;
}
?>
```

以上例程会输出：

    array(2) {
      ["user"]=>
      string(4) "bill"
      ["mime-type"]=>
      string(10) "text/plain"
    }

### 参见

-   <span class="function">PharFileInfo::hasMetadata</span>
-   <span class="function">PharFileInfo::getMetadata</span>
-   <span class="function">PharFileInfo::delMetadata</span>
-   <span class="function">Phar::setMetadata</span>
-   <span class="function">Phar::hasMetadata</span>
-   <span class="function">Phar::getMetadata</span>

简介
----

The PharException class provides a phar-specific exception class for
try/catch blocks.

类摘要
------

**PharException**

<span class="ooclass"> class **PharException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

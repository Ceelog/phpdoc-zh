预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

| Constant                                               | Value      | Description                                                                         |
|--------------------------------------------------------|------------|-------------------------------------------------------------------------------------|
| **`Phar::NONE`** (<span class="type">int</span>)       | 0x00000000 | no compression                                                                      |
| **`Phar::COMPRESSED`** (<span class="type">int</span>) | 0x0000F000 | bitmask that can be used with file flags to determine if any compression is present |
| **`Phar::GZ`** (<span class="type">int</span>)         | 0x00001000 | zlib (gzip) compression                                                             |
| **`Phar::BZ2`** (<span class="type">int</span>)        | 0x00002000 | bzip2 compression                                                                   |

| Constant                                         | Value | Description      |
|--------------------------------------------------|-------|------------------|
| **`Phar::PHAR`** (<span class="type">int</span>) | 1     | phar file format |
| **`Phar::TAR`** (<span class="type">int</span>)  | 2     | tar file format  |
| **`Phar::ZIP`** (<span class="type">int</span>)  | 3     | zip file format  |

| Constant                                            | Value  | Description                                                                               |
|-----------------------------------------------------|--------|-------------------------------------------------------------------------------------------|
| **`Phar::MD5`** (<span class="type">int</span>)     | 0x0001 | signature with md5 hash algorithm                                                         |
| **`Phar::SHA1`** (<span class="type">int</span>)    | 0x0002 | signature with sha1 hash algorithm                                                        |
| **`Phar::SHA256`** (<span class="type">int</span>)  | 0x0003 | signature with sha256 hash algorithm (requires hash extension)                            |
| **`Phar::SHA512`** (<span class="type">int</span>)  | 0x0004 | signature with sha512 hash algorithm (requires hash extension)                            |
| **`Phar::OPENSSL`** (<span class="type">int</span>) | 0x0010 | signature with OpenSSL public/private key pair. This is a true, asymmetric key signature. |

| Constant                                         | Value | Description                                                                                                                                                                                                |
|--------------------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`Phar::PHP`** (<span class="type">int</span>)  | 0     | used to instruct the mimeoverrides parameter of <span class="function">Phar::webPhar</span> that the extension should be parsed as a PHP file                                                              |
| **`Phar::PHPS`** (<span class="type">int</span>) | 1     | used to instruct the mimeoverrides parameter of <span class="function">Phar::webPhar</span> that the extension should be parsed as a PHP source file through <span class="function">highlight\_file</span> |

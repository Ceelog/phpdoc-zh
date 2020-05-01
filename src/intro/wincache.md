Windows Cache Extension for PHP is a PHP accelerator that is used to
increase the speed of PHP applications running on Windows and Windows
Server. Once the Windows Cache Extension for PHP is enabled and loaded
by the PHP engine, PHP applications can take advantage of the
functionality without any code modifications.

The Windows Cache Extension includes 5 different types of caches. The
following describes the purpose of each cache type and the benefits it
provides.

-   *PHP Opcode Cache* - PHP is a script processing engine, which reads
    an input stream of data that contains text and/or PHP instructions
    and produces another stream of data, most commonly in the HTML
    format. This means that on a web server the PHP engine reads,
    parses, compiles and executes a PHP script each time that it is
    requested by a Web client. The reading, parsing and compilation
    operations put additional load on the web server's CPU and file
    system and thus affect the overall performance of a PHP web
    application. The PHP bytecode (opcode) cache is used to store the
    compiled script bytecode in shared memory so that it can be re-used
    by PHP engine for subsequent executions of the same script.

    Support for opcode caching was removed in *Wincache 2.0.0*, all
    users who wish to have an opcache should use the
    <a href="/book/opcache.html" class="link">OPcache</a> extension that
    is included with PHP as of PHP 5.5.0.

-   *File Cache* - Even with the PHP opcode cache enabled, the PHP
    engine has to accesses the script files on a file system. When PHP
    scripts are stored on a remote UNC file share, the file operations
    introduce a significant performance overhead. The Windows Cache
    Extension for PHP includes a file cache that is used to store the
    content of the PHP script files in shared memory, which reduces the
    amount of file system operations performed by PHP engine.

-   *Resolve File Path Cache* - PHP scripts very often include or
    operate with files by using relative file paths. Every file path has
    to be normalized to an absolute file path by the PHP engine. When a
    PHP application uses many PHP files and accesses them by relative
    paths, the operation of resolving the paths may negatively impact
    the application's performance. The Windows Cache Extension for PHP
    provides a Resolve File Path cache, which is used to store the
    mappings between relative and absolute file paths, thereby reducing
    the number of path resolutions that the PHP engine has to perform.

-   *User Cache (available since version 1.1.0)* - PHP scripts can take
    advantage of the shared memory cache by using the user cache API's.
    PHP objects and variables can be stored in the user cache and then
    re-used on subsequent requests. This can be used to improve
    performance of PHP scripts and to share the data across multiple PHP
    processes.

-   *Session Handler (available since version 1.1.0)* - The WinCache
    session handler can be used to store the PHP session data in the
    shared memory cache. This avoids file system operations for reading
    and writing session data, which improves performance when large
    amount of data is stored in PHP session.

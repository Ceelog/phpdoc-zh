Preloading
==========

As of PHP 7.4.0, PHP can be configured to preload scripts into the
opcache when the engine starts. Any symbols (functions, classes, etc.)
in those files will then become globally available for all requests
without needing to be explicitly included. That trades convenience and
performance (because the code is always available) for baseline memory
usage. It also requires restarting the PHP process to clear pre-loaded
scripts, meaning this feature is only practical to use in production,
not in a development environment.

Note that the optimal tradeoff between performance and memory may vary
with the application. "Preload everything" may be the easiest strategy,
but not necessarily the best strategy. Additionally, preloading is only
useful when there is a persistent process from one request to another.
That means while it can work in a CLI script if the opcache is enabled,
it's generally pointless. The exception is when using preloading on
<a href="/ffi/examples.html#A%20Complete%20PHP/FFI/preloading%20Example" class="link">FFI libraries</a>.

> **Note**:
>
> Preloading is not supported on Windows.

Configuring preloading involves two steps, and requires that the opcache
be enabled. First, set the
<a href="/opcache/setup.html#" class="link">opcache.preload</a> value in
`php.ini`:

``` ini
opcache.preload=preload.php
```

`preload.php` is an arbitrary file that will run once at server startup
(PHP-FPM, mod\_php, etc.) and load code into persistent memory. If PHP
will be run as root (not recommended), the
<a href="/opcache/setup.html#" class="link">opcache.preload_user</a>
value can specify an alternate system user to run the preloading.
Running preloading as root is not allowed.

In the `preload.php` script, any file referenced by <span
class="function">include</span>, <span
class="function">include\_once</span>, <span
class="function">require</span>, <span
class="function">require\_once</span>, or <span
class="function">opcache\_compile\_file</span> will be parsed into
persistent memory. In the following example, all `.php` files in the
`src` directory will be preloaded, unless they are a *Test* file.

``` php
<?php
$directory = new RecursiveDirectoryIterator(__DIR__ . '/src');
$fullTree = new RecursiveIteratorIterator($directory);
$phpFiles = new RegexIterator($fullTree, '/.+((?<!Test)+\.php$)/i', RecursiveRegexIterator::GET_MATCH);

foreach ($phpFiles as $key => $file) {
    require_once($file[0]);
}
?>
```

Both <span class="function">include</span> and <span
class="function">opcache\_compile\_file</span> will work, but have
different implications for how code gets handled.

-   <span class="simpara"><span class="function">include</span> will
    execute code in the file, while <span
    class="function">opcache\_compile\_file</span> will not. That means
    only the former supports conditional declaration (functions declared
    inside an if-block).</span>
-   <span class="simpara">Because <span class="function">include</span>
    will execute code, nested <span class="function">include</span>d
    files will also be parsed and their declarations preloaded.</span>
-   <span class="simpara"><span
    class="function">opcache\_compile\_file</span> can load files in any
    order. That is, if `a.php` defines class *A* and `b.php` defines
    class *B* that extends *A*, then <span
    class="function">opcache\_compile\_file</span> can load those two
    files in any order. When using <span
    class="function">include</span>, however, `a.php` *must* be included
    first.</span>
-   <span class="simpara">In either case, if a later script includes a
    file that has already been preloaded then its contents will still
    execute, but any symbols it defines will not be re-defined. Using
    <span class="function">include\_once</span> will not prevent the
    file from being included a second time.</span>

Which approach is better therefore depends on the desired behavior. With
code that would otherwise use an autoloader, <span
class="function">opcache\_compile\_file</span> allows for greater
flexibility. With code that would otherwise be loaded manually, <span
class="function">include</span> will be more robust.

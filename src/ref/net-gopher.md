gopher\_parsedir
================

Translate a gopher formatted directory entry into an associative array

### 说明

<span class="type">array</span> <span
class="methodname">gopher\_parsedir</span> ( <span
class="methodparam"><span class="type">string</span> `$dirent`</span> )

<span class="function">gopher\_parsedir</span> parses a gopher formatted
directory entry into an associative array.

While gopher returns *text/plain* documents for actual document
requests. A request to a directory (such as /) will return specially
encoded series of lines with each line being one directory entry or
information line.

### 参数

`dirent`  
The directory entry.

### 返回值

Returns an associative array whose components are:

-   <span class="simpara"> *type* - One of the *GOPHER\_XXX* constants.
    </span>
-   <span class="simpara"> *title* - The name of the resource. </span>
-   <span class="simpara"> *path* - The path of the resource. </span>
-   <span class="simpara"> *host* - The domain name of the host that has
    this document (or directory). </span>
-   <span class="simpara"> *port* - The port at which to connect on
    *host*. </span>

Upon failure, the additional *data* entry of the returned array will
hold the parsed line.

### 范例

**示例 \#1 Hypothetical output from *gopher://gopher.example.com/***

    0All about my gopher site.               /allabout.txt               gopher.example.com    70
    9A picture of my cat.                    /pics/cat.png               gopher.example.com    70
    1A collection of my writings.            /stories                    gopher.example.com    70
    hThe HTTP version of this site.          URL:http://www.example.com  gopher.example.com    70
    1Mirror of this site in Spain.           /                           gopher.ejemplo.co.es  70
    iWelcome to my gopher site.                                          error.host            1
    iPlease select one of the options above                              error.host            1
    iSend complaints to /dev/null                                        error.host            1
    iLong live gopher!                                                   error.host            1

In the example above, the root directory at gopher.example.com knows
about one *DOCUMENT* identified by *0* located at
*gopher://gopher.example.com:70/allabout.txt*. It also knows about two
other directory (which have their own listing files) at
*gopher://gopher.exmaple.com:70/stories* and at
*gopher://gopher.ejemplo.co.es:70/*. In addition there is a binary file,
a link to an HTTP url, and several informative lines.

By passing each line of the directory listing into <span
class="function">gopher\_parsedir</span>, an associative array is formed
containing a parsed out version of the data.

**示例 \#2 Using <span class="function">gopher\_parsedir</span>**

``` php
<?php
$directory = file("gopher://gopher.example.com");

foreach($directory as $dirent) {
    print_r(gopher_parsedir($dirent));
}
?>
```

以上例程会输出：

    Array (
      [type] => 0
      [title] => All about my gopher site.
      [path] => /allabout.txt
      [host] => gopher.example.com
      [port] => 70
    )
    Array (
      [type] => 9
      [title] => A picture of my cat.
      [path] => /pics/cat.png
      [host] => gopher.example.com
      [port] => 70
    )
    Array (
      [type] => 1
      [title] => A collection of my writings.
      [path] => /stories
      [host] => gopher.example.com
      [port] => 70
    )
    Array (
      [type] => 254
      [title] => The HTTP version of this site.
      [path] => URL:http://www.example.com
      [host] => gopher.example.com
      [port] => 70
    )
    Array (
      [type] => 1
      [title] => Mirror of this site in Spain.
      [path] => /
      [host] => gopher.ejemplo.co.es
      [port] => 70
    )
    Array (
      [type] => 255
      [title] => Welcome to my gopher site.
      [path] =>
      [host] => error.host
      [port] => 1
    )
    Array (
      [type] => 255
      [title] => Please select one of the options above.
      [path] =>
      [host] => error.host
      [port] => 1
    )
    Array (
      [type] => 255
      [title] => Send complaints to /dev/null
      [path] =>
      [host] => error.host
      [port] => 1
    )
    Array (
      [type] => 255
      [title] => Long live gopher!
      [path] =>
      [host] => error.host
      [port] => 1
    )

**目录**

-   [gopher\_parsedir](/ref/net-gopher.html#gopher_parsedir) — Translate
    a gopher formatted directory entry into an associative array

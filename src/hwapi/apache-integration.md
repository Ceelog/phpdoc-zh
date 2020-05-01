Integration with Apache
=======================

The Hyperwave extension is best used when PHP is compiled as an Apache
module. In such a case the underlying Hyperwave server can be hidden
from users almost completely if Apache uses its rewriting engine. The
following instructions will explain this.

Since PHP with Hyperwave support built into Apache is intended to
replace the native Hyperwave solution based on Wavemaster, we will
assume that the Apache server will only serve as a Hyperwave web
interface for these examples. This is not necessary but it simplifies
the configuration. The concept is quite simple. First of all you need a
PHP script which evaluates the `$_ENV['PATH_INFO']` variable and treats
its value as the name of a Hyperwave object. Let's call this script
*'Hyperwave'*. The URL *http://your.hostname/Hyperwave/name\_of\_object*
would than return the Hyperwave object with the name
*'name\_of\_object'*. Depending on the type of the object the script has
to react accordingly. If it is a collection, it will probably return a
list of children. If it is a document it will return the mime type and
the content. A slight improvement can be achieved if the Apache
rewriting engine is used. From the users point of view it would be more
straight forward if the URL *http://your.hostname/name\_of\_object*
would return the object. The rewriting rule is quite easy:

``` apache-conf
RewriteRule ^/(.*) /usr/local/apache/htdocs/HyperWave/$1 [L]
```

Now every URL relates to an object in the Hyperwave server. This causes
a simple to solve problem. There is no way to execute a different
script, e.g. for searching, than the 'Hyperwave' script. This can be
fixed with another rewriting rule like the following:

``` apache-conf
RewriteRule ^/hw/(.*) /usr/local/apache/htdocs/hw/$1 [L]
```

This will reserve the directory `/usr/local/apache/htdocs/hw` for
additional scripts and other files. Just make sure this rule is
evaluated before the one above. There is just a little drawback: all
Hyperwave objects whose name starts with *'hw/'* will be shadowed. So,
make sure you don't use such names. If you need more directories, e.g.
for images just add more rules or place them all in one directory.
Before you put those instructions, don't forget to turn on the rewriting
engine with

``` apache-conf
RewriteEngine on
```

You will need scripts:

-   <span class="simpara"> to return the object itself </span>
-   <span class="simpara"> to allow searching </span>
-   <span class="simpara"> to identify yourself </span>
-   <span class="simpara"> to set your profile </span>
-   <span class="simpara"> one for each additional function like to show
    the object attributes, to show information about users, to show the
    status of the server, etc. </span>

As an alternative to the Rewrite Engine, you can also consider using the
Apache *ErrorDocument* directive, but be aware, that *ErrorDocument*
redirected pages cannot receive POST data.

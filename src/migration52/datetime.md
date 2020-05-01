Changes in PHP <a href="/ref/datetime.html" class="link">datetime</a> support
-----------------------------------------------------------------------------

Since PHP 5.1.0, there has been an extension named *date* in the PHP
core. This is the new implementation of PHP's datetime support. Although
it will attempt to guess your system's timezone setting, you should set
the timezone manually. You can do this in any of three ways:

-   <span class="simpara"> in your `php.ini` using the
    <a href="/datetime/setup.html#" class="link">date.timezone</a> INI
    directive </span>
-   <span class="simpara"> on your system using the `TZ` environmental
    variable </span>
-   <span class="simpara"> from your script using the convenience
    function <span class="function">date\_default\_timezone\_set</span>
    </span>

All supported <a href="/timezones.html" class="link">timezones</a> are
listed in the PHP Manual.

With the advent of PHP 5.2.x, there are <span class="type">object</span>
representations of the date and timezone, named *DateTime* and
*DateTimeZone* respectively. The methods map to existing procedural date
functions.

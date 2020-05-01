Date/time support
-----------------

Date/time support has been fully rewritten in PHP 5.1.x, and no longer
uses the system settings to 'know' the timezone in operation. It will
instead utilize, in the following order:

-   The timezone set using the <span
    class="function">date\_default\_timezone\_set</span> function (if
    any)

-   The TZ environment variable (if non empty)

-   "magical" guess (if the operating system supports it)

-   If none of the above options succeeds, UTC

To ensure accuracy (and avoid an **`E_STRICT`** warning), you will need
to define your timezone in your `php.ini` using the following format:

date.timezone = Europe/London

The supported timezones are listed, in this format, in the
<a href="/timezones.html" class="link">timezones appendix</a>.

Also note that <span class="function">strtotime</span> now returns
**`FALSE`** on failure, instead of -1.

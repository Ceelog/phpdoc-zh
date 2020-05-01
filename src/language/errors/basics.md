Basics
------

PHP reports errors in response to a number of internal error conditions.
These may be used to signal a number of different conditions, and can be
displayed and/or logged as required.

Every error that PHP generates includes a type. A
<a href="/errorfunc/constants.html" class="link">list of these types</a>
is available, along with a short description of their behaviour and how
they can be caused.

### Handling errors with PHP

If no error handler is set, then PHP will handle any errors that occur
according to its configuration. Which errors are reported and which are
ignored is controlled by the
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link"><code class="parameter">error_reporting</code></a>
php.ini directive, or at runtime by calling <span
class="function">error\_reporting</span>. It is strongly recommended
that the configuration directive be set, however, as some errors can
occur before execution of your script begins.

In a development environment, you should always set
<a href="/errorfunc/setup.html#PHP外的PHP常量" class="link"><code class="parameter">error_reporting</code></a>
to **`E_ALL`**, as you need to be aware of and fix the issues raised by
PHP. In production, you may wish to set this to a less verbose level
such as `E_ALL & ~E_NOTICE & ~E_STRICT & ~E_DEPRECATED`, but in many
cases **`E_ALL`** is also appropriate, as it may provide early warning
of potential issues.

What PHP does with these errors depends on two further php.ini
directives.
<a href="/errorfunc/setup.html#" class="link"><code class="parameter">display_errors</code></a>
controls whether the error is shown as part of the script's output. This
should always be disabled in a production environment, as it can include
confidential information such as database passwords, but is often useful
to enable in development, as it ensures immediate reporting of issues.

In addition to displaying errors, PHP can log errors when the
<a href="/errorfunc/setup.html#" class="link"><code class="parameter">log_errors</code></a>
directive is enabled. This will log any errors to the file or syslog
defined by
<a href="/errorfunc/setup.html#" class="link"><code class="parameter">error_log</code></a>.
This can be extremely useful in a production environment, as you can log
errors that occur and then generate reports based on those errors.

### User error handlers

If PHP's default error handling is inadequate, you can also handle many
types of error with your own custom error handler by installing it with
<span class="function">set\_error\_handler</span>. While some error
types cannot be handled this way, those that can be handled can then be
handled in the way that your script sees fit: for example, this can be
used to show a custom error page to the user and then report more
directly than via a log, such as by sending an e-mail.

Stream Errors
=============

As with any file or socket related function, an operation on a stream
may fail for a variety of normal reasons (i.e.: Unable to connect to
remote host, file not found, etc...). A stream related call may also
fail because the desired stream is not registered on the running system.
See the array returned by <span
class="function">stream\_get\_wrappers</span> for a list of streams
supported by your installation of PHP. As with most PHP internal
functions if a failure occurs an **`E_WARNING`** message will be
generated describing the nature of the error.

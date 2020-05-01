APD is the Advanced PHP Debugger. It was written to provide profiling
and debugging capabilities for PHP code, as well as to provide the
ability to print out a full stack backtrace. APD supports interactive
debugging, but by default it writes data to trace files. It also offers
event based logging so that varying levels of information (including
function calls, arguments passed, timings, etc.) can be turned on or off
for individual scripts.

**Caution**

APD is a Zend Extension, modifying the way the internals of PHP handle
function calls, and thus may or may not be compatible with other Zend
Extensions (for example Zend Optimizer).

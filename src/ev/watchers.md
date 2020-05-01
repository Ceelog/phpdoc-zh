Watchers
========

A watcher is an object that gets created to record interest in some
event. For instance, the following code waits for **`STDIN`** to become
readable:

``` php
<?php
// Wait until STDIN is readable
$w = new EvIo(STDIN, Ev::READ, function ($watcher, $revents) {
 echo "STDIN is readable\n";
});
Ev::run(Ev::RUN_ONCE);
?>
```

All the watcher constructors automatically start the watchers.
*createStopped* methods create stopped watchers(e.g. <span
class="methodname">EvIo::createStopped</span> )

Note that a watcher will automatically be stopped when the watcher
object is destroyed. Therefore, the watcher objects returned by the
constructors or factory methods should be kept.

Note also that all methods changing some watcher property( *set* ,
`priority` etc.) automatically stop and start it again if it is active,
which means pending events get lost.

See also:
<a href="/ev/watcher-callbacks.html" class="link">Watcher callbacks</a>
.

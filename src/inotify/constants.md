预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

**`IN_ACCESS`** (<span class="type">integer</span>)  
<span class="simpara"> File was accessed (read) (\*) </span>

**`IN_MODIFY`** (<span class="type">integer</span>)  
<span class="simpara"> File was modified (\*) </span>

**`IN_ATTRIB`** (<span class="type">integer</span>)  
<span class="simpara"> Metadata changed (e.g. permissions, mtime, etc.)
(\*) </span>

**`IN_CLOSE_WRITE`** (<span class="type">integer</span>)  
<span class="simpara"> File opened for writing was closed (\*) </span>

**`IN_CLOSE_NOWRITE`** (<span class="type">integer</span>)  
<span class="simpara"> File not opened for writing was closed (\*)
</span>

**`IN_OPEN`** (<span class="type">integer</span>)  
<span class="simpara"> File was opened (\*) </span>

**`IN_MOVED_TO`** (<span class="type">integer</span>)  
<span class="simpara"> File moved into watched directory (\*) </span>

**`IN_MOVED_FROM`** (<span class="type">integer</span>)  
<span class="simpara"> File moved out of watched directory (\*) </span>

**`IN_CREATE`** (<span class="type">integer</span>)  
<span class="simpara"> File or directory created in watched directory
(\*) </span>

**`IN_DELETE`** (<span class="type">integer</span>)  
<span class="simpara"> File or directory deleted in watched directory
(\*) </span>

**`IN_DELETE_SELF`** (<span class="type">integer</span>)  
<span class="simpara"> Watched file or directory was deleted </span>

**`IN_MOVE_SELF`** (<span class="type">integer</span>)  
<span class="simpara"> Watch file or directory was moved </span>

**`IN_CLOSE`** (<span class="type">integer</span>)  
<span class="simpara"> Equals to IN\_CLOSE\_WRITE \| IN\_CLOSE\_NOWRITE
</span>

**`IN_MOVE`** (<span class="type">integer</span>)  
<span class="simpara"> Equals to IN\_MOVED\_FROM \| IN\_MOVED\_TO
</span>

**`IN_ALL_EVENTS`** (<span class="type">integer</span>)  
<span class="simpara"> Bitmask of all the above constants </span>

**`IN_UNMOUNT`** (<span class="type">integer</span>)  
<span class="simpara"> File system containing watched object was
unmounted </span>

**`IN_Q_OVERFLOW`** (<span class="type">integer</span>)  
<span class="simpara"> Event queue overflowed (wd is -1 for this event)
</span>

**`IN_IGNORED`** (<span class="type">integer</span>)  
<span class="simpara"> Watch was removed (explicitly by <span
class="function">inotify\_rm\_watch</span> or because file was removed
or filesystem unmounted </span>

**`IN_ISDIR`** (<span class="type">integer</span>)  
<span class="simpara"> Subject of this event is a directory </span>

**`IN_ONLYDIR`** (<span class="type">integer</span>)  
<span class="simpara"> Only watch pathname if it is a directory (Since
Linux 2.6.15) </span>

**`IN_DONT_FOLLOW`** (<span class="type">integer</span>)  
<span class="simpara"> Do not dereference pathname if it is a symlink
(Since Linux 2.6.15) </span>

**`IN_MASK_ADD`** (<span class="type">integer</span>)  
<span class="simpara"> Add events to watch mask for this pathname if it
already exists (instead of replacing mask). </span>

**`IN_ONESHOT`** (<span class="type">integer</span>)  
<span class="simpara"> Monitor pathname for one event, then remove from
watch list. </span>

> **Note**: <span class="simpara"> The events marked with an asterisk
> (\*) above can occur for files in watched directories. </span>

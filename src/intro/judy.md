PHP Judy is a PECL extension for the
<a href="http://judy.sourceforge.net" class="link external">» Judy C library</a>
implementing dynamic sparse arrays.

A Judy array is a complex but very fast associative array data structure
for storing and looking up values using integer or string keys. Unlike
normal arrays, Judy arrays may be sparse; that is, they may have large
ranges of unassigned indices.

A Judy array consumes memory only when populated yet can grow to take
advantage of all available memory. Judy's key benefits are: scalability,
performance, memory efficiency, and ease of use. Judy arrays are
designed to grow without tuning into the peta-element range, scaling
near O(log-base-256) -- 1 more RAM access at 256 X population.

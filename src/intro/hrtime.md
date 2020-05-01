The HRTime extension implements a high resolution StopWatch class. It
uses the best possible APIs on different platforms which brings
resolution up to nanoseconds. It also makes possible to implement a
custom stopwatch using low level ticks delivered by the underlaying
APIs.

> **Note**: <span class="simpara"> As of PHP 7.3.0 the related function
> <span class="function">hrtime</span> is part of the core. </span>

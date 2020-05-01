范例
====

**目录**

-   [How to use PHP-APD in your
    scripts](/apd/examples.html#How%20to%20use%20PHP-APD%20in%20your%20scripts)

How to use PHP-APD in your scripts
----------------------------------

1.  As the first line of your PHP script, call the
    apd\_set\_pprof\_trace() function to start the trace:

    ``` php
    <?php
    apd_set_pprof_trace();
    ?>
    ```

    You can insert the line anywhere in your script, but if you do not
    start tracing at the beginning of your script you discard profile
    data that might otherwise lead you to a performance bottleneck.

2.  Now run your script. The dump output will be written to
    `apd.dumpdir/pprof_pid.ext`.

    **小贴士**
    If you're running the CGI version of PHP, you will need to add the
    '-e' flag to enable extended information for apd to work properly.
    For example: **`php -e -f script.php`**

3.  To display formatted profile data, issue the **pprofp** command with
    the sort and display options of your choice. The formatted output
    will look something like:

        bash-2.05b$ pprofp -R /tmp/pprof.22141.0

        Trace for /home/dan/testapd.php
        Total Elapsed Time = 0.00
        Total System Time  = 0.00
        Total User Time    = 0.00


        Real         User        System             secs/    cumm
        %Time (excl/cumm)  (excl/cumm)  (excl/cumm) Calls    call    s/call  Memory Usage Name
        --------------------------------------------------------------------------------------
        100.0 0.00 0.00  0.00 0.00  0.00 0.00     1  0.0000   0.0009            0 main
        56.9 0.00 0.00  0.00 0.00  0.00 0.00     1  0.0005   0.0005            0 apd_set_pprof_trace
        28.0 0.00 0.00  0.00 0.00  0.00 0.00    10  0.0000   0.0000            0 preg_replace
        14.3 0.00 0.00  0.00 0.00  0.00 0.00    10  0.0000   0.0000            0 str_replace

    The -R option used in this example sorts the profile table by the
    amount of real time the script spent executing a given function. The
    "cumm call" column reveals how many times each function was called,
    and the "s/call" column reveals how many seconds each call to the
    function required, on average.

4.  To generate a calltree file that you can import into the KCacheGrind
    profile analysis application, issue the **pprof2calltree** comand.

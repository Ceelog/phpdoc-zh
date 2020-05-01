范例
====

**目录**

-   [Win32ps examples](/win32ps/examples.html#Win32ps%20examples)

Win32ps examples
----------------

**示例 \#1 Statistics about the current PHP process**

``` php
<?php
print_r(win32_ps_stat_proc());
/*
    Array
    (
        [pid] => 936
        [exe] => D:\Daten\Source\php-5.1\Debug_TS\php.exe
        [mem] => Array
            (
                [page_fault_count] => 2062
                [peak_working_set_size] => 8396800
                [working_set_size] => 8396800
                [quota_peak_paged_pool_usage] => 32080
                [quota_paged_pool_usage] => 31876
                [quota_peak_non_paged_pool_usage] => 4240
                [quota_non_paged_pool_usage] => 3888
                [pagefile_usage] => 5865472
                [peak_pagefile_usage] => 5865472
            )

        [tms] => Array
            (
                [created] => 0.093
                [kernel] => 0.015
                [user] => 0.062
            )

    )
*/
?>
```

**示例 \#2 Statistics about global memory utilization**

``` php
<?php
print_r(win32_ps_stat_mem());
/*
    Array
    (
        [load] => 37
        [unit] => 1024
        [total_phys] => 1048096
        [avail_phys] => 649960
        [total_pagefile] => 2521368
        [avail_pagefile] => 2237940
        [total_virtual] => 2097024
        [avail_virtual] => 2057848
    )
*/
?>
```

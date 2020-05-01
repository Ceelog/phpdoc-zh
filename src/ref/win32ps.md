win32\_ps\_list\_procs
======================

List running processes

### 说明

<span class="type">array</span> <span
class="methodname">win32\_ps\_list\_procs</span> ( <span
class="methodparam">void</span> )

Retrieves statistics about all running processes.

### 返回值

Returns **`FALSE`** on failure, or an array consisting of process
statistics like <span class="function">win32\_ps\_stat\_proc</span>
returns for all running processes on success.

### 参见

-   <span class="function">win32\_ps\_stat\_proc</span>

win32\_ps\_stat\_mem
====================

Stat memory utilization

### 说明

<span class="type">array</span> <span
class="methodname">win32\_ps\_stat\_mem</span> ( <span
class="methodparam">void</span> )

Retrieves statistics about the global memory utilization.

### 返回值

Returns **`FALSE`** on failure, or an array consisting of the following
information on success:

`load`  
The current memory load in percent of physical memory.

`unit`  
This is always 1024, and indicates that the following values are the
count of 1024 bytes.

`total_phys`  
The amount of total physical memory.

`avail_phys`  
The amount of still available physical memory.

`total_pagefile`  
The amount of total pageable memory (physical memory + paging file).

`avail_pagefile`  
The amount of still available pageable memory (physical memory + paging
file).

`total_virtual`  
The amount of total virtual memory for a process.

`avail_virtual`  
The amount of still available virtual memory for a process.

win32\_ps\_stat\_proc
=====================

Stat process

### 说明

<span class="type">array</span> <span
class="methodname">win32\_ps\_stat\_proc</span> (\[ <span
class="methodparam"><span class="type">int</span> `$pid`<span
class="initializer"> = 0</span></span> \] )

Retrieves statistics about the process with the process id `pid`.

### 参数

`pid`  
The process id of the process to stat. If omitted, the id of the current
process.

### 返回值

Returns **`FALSE`** on failure, or an array consisting of the following
information on success:

`pid`  
The process id.

`exe`  
The path to the executable image.

`mem`  
An array containing information about the following memory utilization
indicators: `page_fault_count`, `peak_working_set_size`,
`working_set_size`, `quota_peak_paged_pool_usage`,
`quota_paged_pool_usage`, `quota_peak_non_paged_pool_usage`,
`quota_non_paged_pool_usage`, `pagefile_usage` and
`peak_pagefile_usage`.

`tms`  
An array containing information about the following CPU time utilization
indicators: `created`, `kernel` and `user`.

### 参见

-   <span class="function">win32\_ps\_list\_procs</span>

**目录**

-   [win32\_ps\_list\_procs](/ref/win32ps.html#win32_ps_list_procs) —
    List running processes
-   [win32\_ps\_stat\_mem](/ref/win32ps.html#win32_ps_stat_mem) — Stat
    memory utilization
-   [win32\_ps\_stat\_proc](/ref/win32ps.html#win32_ps_stat_proc) — Stat
    process

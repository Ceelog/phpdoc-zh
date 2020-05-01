预定义常量
==========

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

| Constant                                                    | Description                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`FAMChanged`** (<span class="type">integer</span>)        | Some value which can be obtained with fstat(1) changed for a file or directory.                                                                                        |
| **`FAMDeleted`** (<span class="type">integer</span>)        | A file or directory was deleted or renamed.                                                                                                                            |
| **`FAMStartExecuting`** (<span class="type">integer</span>) | An executable file started executing.                                                                                                                                  |
| **`FAMStopExecuting`** (<span class="type">integer</span>)  | An executable file that was running finished.                                                                                                                          |
| **`FAMCreated`** (<span class="type">integer</span>)        | A file was created in a directory.                                                                                                                                     |
| **`FAMMoved`** (<span class="type">integer</span>)          | This event never occurs.                                                                                                                                               |
| **`FAMAcknowledge`** (<span class="type">integer</span>)    | An event in response to <span class="function">fam\_cancel\_monitor</span>.                                                                                            |
| **`FAMExists`** (<span class="type">integer</span>)         | An event upon request to monitor a file or directory. When a directory is monitored, an event for that directory and every file contained in that directory is issued. |
| **`FAMEndExist`** (<span class="type">integer</span>)       | Event after the last FAMEExists event.                                                                                                                                 |

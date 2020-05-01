预定义常量
==========

**目录**

-   [Win32Service Service Type
    Bitmasks](/win32service/constants.html#Win32Service%20Service%20Type%20Bitmasks)
-   [Win32Service Service Status
    Constants](/win32service/constants.html#Win32Service%20Service%20Status%20Constants)
-   [Win32Service Service Control Message
    Constants](/win32service/constants.html#Win32Service%20Service%20Control%20Message%20Constants)
-   [Win32Service Service Control Message Accepted
    Bitmasks](/win32service/constants.html#Win32Service%20Service%20Control%20Message%20Accepted%20Bitmasks)
-   [Win32Service Service Start Type
    Constants](/win32service/constants.html#Win32Service%20Service%20Start%20Type%20Constants)
-   [Win32Service Service Error Control
    Constants](/win32service/constants.html#Win32Service%20Service%20Error%20Control%20Constants)
-   [Win32Service Service Flag
    Constants](/win32service/constants.html#Win32Service%20Service%20Flag%20Constants)
-   [Win32 Error
    Codes](/win32service/constants.html#Win32%20Error%20Codes)
-   [Win32 Base Priority
    Classes](/win32service/constants.html#Win32%20Base%20Priority%20Classes)
-   [Win32 Recovery
    action](/win32service/constants.html#Win32%20Recovery%20action)
-   [Win32 Service
    informations](/win32service/constants.html#Win32%20Service%20informations)

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

| Constant                                          | Value      | Description                                                                                                                    |
|---------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------|
| **`WIN32_SERVICE_WIN32_OWN_PROCESS`**             | 0x00000010 | The service runs in its own process.                                                                                           |
| **`WIN32_SERVICE_INTERACTIVE_PROCESS`**           | 0x00000100 | The service can interact with the desktop. This option is not available on Windows Vista or later.                             |
| **`WIN32_SERVICE_WIN32_OWN_PROCESS_INTERACTIVE`** | 0x00000110 | The service runs in its own process and can interact with the desktop. This option is not available on Windows Vista or later. |

| Constant                             | Value      | Description                      |
|--------------------------------------|------------|----------------------------------|
| **`WIN32_SERVICE_CONTINUE_PENDING`** | 0x00000005 | The service continue is pending. |
| **`WIN32_SERVICE_PAUSE_PENDING`**    | 0x00000006 | The service pause is pending.    |
| **`WIN32_SERVICE_PAUSED`**           | 0x00000007 | The service is paused.           |
| **`WIN32_SERVICE_RUNNING`**          | 0x00000004 | The service is running.          |
| **`WIN32_SERVICE_START_PENDING`**    | 0x00000002 | The service is starting.         |
| **`WIN32_SERVICE_STOP_PENDING`**     | 0x00000003 | The service is stopping.         |
| **`WIN32_SERVICE_STOPPED`**          | 0x00000001 | The service is not running.      |

| Constant                                          | Value      | Description                                                                                                                                                                                                                                                                         |
|---------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`WIN32_SERVICE_CONTROL_CONTINUE`**              | 0x00000003 | Notifies a paused service that it should resume.                                                                                                                                                                                                                                    |
| **`WIN32_SERVICE_CONTROL_DEVICEEVENT`**           | 0x0000000B |                                                                                                                                                                                                                                                                                     |
| **`WIN32_SERVICE_CONTROL_HARDWAREPROFILECHANGE`** | 0x0000000C |                                                                                                                                                                                                                                                                                     |
| **`WIN32_SERVICE_CONTROL_INTERROGATE`**           | 0x00000004 | Notifies a service that it should report its current status information to the service control manager.                                                                                                                                                                             |
| **`WIN32_SERVICE_CONTROL_NETBINDADD`**            | 0x00000007 | Notifies a network service that there is a new component for binding.                                                                                                                                                                                                               |
| **`WIN32_SERVICE_CONTROL_NETBINDDISABLE`**        | 0x0000000A | Notifies a network service that one of its bindings has been disabled.                                                                                                                                                                                                              |
| **`WIN32_SERVICE_CONTROL_NETBINDENABLE`**         | 0x00000009 | Notifies a network service that a disabled binding has been enabled.                                                                                                                                                                                                                |
| **`WIN32_SERVICE_CONTROL_NETBINDREMOVE`**         | 0x00000008 | Notifies a network service that a component for binding has been removed.                                                                                                                                                                                                           |
| **`WIN32_SERVICE_CONTROL_PARAMCHANGE`**           | 0x00000006 | Notifies a service that its startup parameters have changed.                                                                                                                                                                                                                        |
| **`WIN32_SERVICE_CONTROL_PAUSE`**                 | 0x00000002 | Notifies a service that it should pause.                                                                                                                                                                                                                                            |
| **`WIN32_SERVICE_CONTROL_POWEREVENT`**            | 0x0000000D |                                                                                                                                                                                                                                                                                     |
| **`WIN32_SERVICE_CONTROL_PRESHUTDOWN`**           | 0x0000000F | Notifies a service that the system will be shutting down. A service that handles this notification blocks system shutdown until the service stops or the preshutdown time-out interval expires. This value is not supported by Windows Server 2003 and Windows XP/2000.             |
| **`WIN32_SERVICE_CONTROL_SESSIONCHANGE`**         | 0x0000000E |                                                                                                                                                                                                                                                                                     |
| **`WIN32_SERVICE_CONTROL_SHUTDOWN`**              | 0x00000005 | Notifies a service that the system is shutting down so the service can perform cleanup tasks. If a service accepts this control code, it must stop after it performs its cleanup tasks. After the SCM sends this control code, it will not send other control codes to the service. |
| **`WIN32_SERVICE_CONTROL_STOP`**                  | 0x00000001 | Notifies a service that it should stop.                                                                                                                                                                                                                                             |

| Constant                                         | Value      | Description                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`WIN32_SERVICE_ACCEPT_HARDWAREPROFILECHANGE`** | 0x00000020 | The service is notified when the computer's hardware profile has changed. This enables the system to send **`WIN32_SERVICE_CONTROL_HARDWAREPROFILECHANGE`** notifications to the service.                                                                                                                                                                  |
| **`WIN32_SERVICE_ACCEPT_NETBINDCHANGE`**         | 0x00000010 | The service is a network component that can accept changes in its binding without being stopped and restarted. This control code allows the service to receive **`WIN32_SERVICE_CONTROL_NETBINDADD`**, **`WIN32_SERVICE_CONTROL_NETBINDREMOVE`**, **`WIN32_SERVICE_CONTROL_NETBINDENABLE`**, and **`WIN32_SERVICE_CONTROL_NETBINDDISABLE`** notifications. |
| **`WIN32_SERVICE_ACCEPT_PARAMCHANGE`**           | 0x00000008 | The service can reread its startup parameters without being stopped and restarted. This control code allows the service to receive **`WIN32_SERVICE_CONTROL_PARAMCHANGE`** notifications.                                                                                                                                                                  |
| **`WIN32_SERVICE_ACCEPT_PAUSE_CONTINUE`**        | 0x00000002 | The service can be paused and continued. This control code allows the service to receive **`WIN32_SERVICE_CONTROL_PAUSE`** and **`WIN32_SERVICE_CONTROL_CONTINUE`** notifications.                                                                                                                                                                         |
| **`WIN32_SERVICE_ACCEPT_POWEREVENT`**            | 0x00000040 | The service is notified when the computer's power status has changed. This enables the system to send **`WIN32_SERVICE_CONTROL_POWEREVENT`** notifications to the service.                                                                                                                                                                                 |
| **`WIN32_SERVICE_ACCEPT_PRESHUTDOWN`**           | 0x00000100 | The service can perform preshutdown tasks. This control code enables the service to receive **`WIN32_SERVICE_CONTROL_PRESHUTDOWN`** notifications. This value is not supported by Windows Server 2003 and Windows XP/2000.                                                                                                                                 |
| **`WIN32_SERVICE_ACCEPT_SESSIONCHANGE`**         | 0x00000080 | The service is notified when the computer's session status has changed. This enables the system to send **`WIN32_SERVICE_CONTROL_SESSIONCHANGE`** notifications to the service. Windows 2000: This value is not supported                                                                                                                                  |
| **`WIN32_SERVICE_ACCEPT_SHUTDOWN`**              | 0x00000004 | The service is notified when system shutdown occurs. This control code allows the service to receive **`WIN32_SERVICE_CONTROL_SHUTDOWN`** notifications.                                                                                                                                                                                                   |
| **`WIN32_SERVICE_ACCEPT_STOP`**                  | 0x00000001 | The service can be stopped. This control code allows the service to receive **`WIN32_SERVICE_CONTROL_STOP`** notifications.                                                                                                                                                                                                                                |
| **`WIN32_SERVICE_ACCEPT_TIMECHANGE`**            | 0x00000200 | The service is notified when the system time has changed. This enables the system to send **`WIN32_SERVICE_CONTROL_TIMECHANGE`** notifications to the service. Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP/2000: This control code is not supported.                                                                           |
| **`WIN32_SERVICE_ACCEPT_TRIGGEREVENT`**          | 0x00000400 | The service is notified when an event for which the service has registered occurs. This enables the system to send **`WIN32_SERVICE_CONTROL_TRIGGEREVENT`** notifications to the service. Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP/2000: This control code is not supported.                                                |

| Constant                         | Value      | Description                                                                                                                  |
|----------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------|
| **`WIN32_SERVICE_BOOT_START`**   | 0x00000000 | A device driver started by the system loader. This value is valid only for driver services.                                  |
| **`WIN32_SERVICE_SYSTEM_START`** | 0x00000001 | A device driver started by the IoInitSystem function. This value is valid only for driver services.                          |
| **`WIN32_SERVICE_AUTO_START`**   | 0x00000002 | A service started automatically by the service control manager during system startup.                                        |
| **`WIN32_SERVICE_DEMAND_START`** | 0x00000003 | A service started by the service control manager when a process calls the StartService function.                             |
| **`WIN32_SERVICE_DISABLED`**     | 0x00000004 | A service that cannot be started. Attempts to start the service result in the error code **`WIN32_ERROR_SERVICE_DISABLED`**. |

| Constant                           | Value      | Description                                                                                                                                                                                                                      |
|------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`WIN32_SERVICE_ERROR_IGNORE`**   | 0x00000000 | The startup program ignores the error and continues the startup operation.                                                                                                                                                       |
| **`WIN32_SERVICE_ERROR_NORMAL`**   | 0x00000001 | The startup program logs the error in the event log but continues the startup operation.                                                                                                                                         |
| **`WIN32_SERVICE_ERROR_SEVERE`**   | 0x00000002 | The startup program logs the error in the event log. If the last-known-good configuration is being started, the startup operation continues. Otherwise, the system is restarted with the last-known-good configuration.          |
| **`WIN32_SERVICE_ERROR_CRITICAL`** | 0x00000003 | The startup program logs the error in the event log, if possible. If the last-known-good configuration is being started, the startup operation fails. Otherwise, the system is restarted with the last-known good configuration. |

| Constant                                   | Value      | Description                                                       |
|--------------------------------------------|------------|-------------------------------------------------------------------|
| **`WIN32_SERVICE_RUNS_IN_SYSTEM_PROCESS`** | 0x00000001 | The service runs in a system process that must always be running. |

| Constant                                            | Value      | Description                                                                                                                                                                                                                                   |
|-----------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`WIN32_ERROR_ACCESS_DENIED`**                     | 0x00000005 | The handle to the SCM database does not have the appropriate access rights.                                                                                                                                                                   |
| **`WIN32_ERROR_CIRCULAR_DEPENDENCY`**               | 0x00000423 | A circular service dependency was specified.                                                                                                                                                                                                  |
| **`WIN32_ERROR_DATABASE_DOES_NOT_EXIST`**           | 0x00000429 | The specified database does not exist.                                                                                                                                                                                                        |
| **`WIN32_ERROR_DEPENDENT_SERVICES_RUNNING`**        | 0x0000041B | The service cannot be stopped because other running services are dependent on it.                                                                                                                                                             |
| **`WIN32_ERROR_DUPLICATE_SERVICE_NAME`**            | 0x00000436 | The display name already exists in the service control manager database either as a service name or as another display name.                                                                                                                  |
| **`WIN32_ERROR_FAILED_SERVICE_CONTROLLER_CONNECT`** | 0x00000427 | This error is returned if the program is being run as a console application rather than as a service. If the program will be run as a console application for debugging purposes, structure it such that service-specific code is not called. |
| **`WIN32_ERROR_INSUFFICIENT_BUFFER`**               | 0x0000007A | The buffer is too small for the service status structure. Nothing was written to the structure.                                                                                                                                               |
| **`WIN32_ERROR_INVALID_DATA`**                      | 0x0000000D | The specified service status structure is invalid.                                                                                                                                                                                            |
| **`WIN32_ERROR_INVALID_HANDLE`**                    | 0x00000006 | The handle to the specified service control manager database is invalid.                                                                                                                                                                      |
| **`WIN32_ERROR_INVALID_LEVEL`**                     | 0x0000007C | The InfoLevel parameter contains an unsupported value.                                                                                                                                                                                        |
| **`WIN32_ERROR_INVALID_NAME`**                      | 0x0000007B | The specified service name is invalid.                                                                                                                                                                                                        |
| **`WIN32_ERROR_INVALID_PARAMETER`**                 | 0x00000057 | A parameter that was specified is invalid.                                                                                                                                                                                                    |
| **`WIN32_ERROR_INVALID_SERVICE_ACCOUNT`**           | 0x00000421 | The user account name specified in the `user` parameter does not exist. See <span class="function">win32\_create\_service</span>.                                                                                                             |
| **`WIN32_ERROR_INVALID_SERVICE_CONTROL`**           | 0x0000041C | The requested control code is not valid, or it is unacceptable to the service.                                                                                                                                                                |
| **`WIN32_ERROR_PATH_NOT_FOUND`**                    | 0x00000003 | The service binary file could not be found.                                                                                                                                                                                                   |
| **`WIN32_ERROR_SERVICE_ALREADY_RUNNING`**           | 0x00000420 | An instance of the service is already running.                                                                                                                                                                                                |
| **`WIN32_ERROR_SERVICE_CANNOT_ACCEPT_CTRL`**        | 0x00000425 | The requested control code cannot be sent to the service because the state of the service is **`WIN32_SERVICE_STOPPED`**, **`WIN32_SERVICE_START_PENDING`**, or **`WIN32_SERVICE_STOP_PENDING`**.                                             |
| **`WIN32_ERROR_SERVICE_DATABASE_LOCKED`**           | 0x0000041F | The database is locked.                                                                                                                                                                                                                       |
| **`WIN32_ERROR_SERVICE_DEPENDENCY_DELETED`**        | 0x00000433 | The service depends on a service that does not exist or has been marked for deletion.                                                                                                                                                         |
| **`WIN32_ERROR_SERVICE_DEPENDENCY_FAIL`**           | 0x0000042C | The service depends on another service that has failed to start.                                                                                                                                                                              |
| **`WIN32_ERROR_SERVICE_DISABLED`**                  | 0x00000422 | The service has been disabled.                                                                                                                                                                                                                |
| **`WIN32_ERROR_SERVICE_DOES_NOT_EXIST`**            | 0x00000424 | The specified service does not exist as an installed service.                                                                                                                                                                                 |
| **`WIN32_ERROR_SERVICE_EXISTS`**                    | 0x00000431 | The specified service already exists in this database.                                                                                                                                                                                        |
| **`WIN32_ERROR_SERVICE_LOGON_FAILED`**              | 0x0000042D | The service did not start due to a logon failure. This error occurs if the service is configured to run under an account that does not have the "Log on as a service" right.                                                                  |
| **`WIN32_ERROR_SERVICE_MARKED_FOR_DELETE`**         | 0x00000430 | The specified service has already been marked for deletion.                                                                                                                                                                                   |
| **`WIN32_ERROR_SERVICE_NO_THREAD`**                 | 0x0000041E | A thread could not be created for the service.                                                                                                                                                                                                |
| **`WIN32_ERROR_SERVICE_NOT_ACTIVE`**                | 0x00000426 | The service has not been started.                                                                                                                                                                                                             |
| **`WIN32_ERROR_SERVICE_REQUEST_TIMEOUT`**           | 0x0000041D | The process for the service was started, but it did not call StartServiceCtrlDispatcher, or the thread that called StartServiceCtrlDispatcher may be blocked in a control handler function.                                                   |
| **`WIN32_ERROR_SHUTDOWN_IN_PROGRESS`**              | 0x0000045B | The system is shutting down; this function cannot be called.                                                                                                                                                                                  |
| **`WIN32_ERROR_SERVICE_SPECIFIC_ERROR`**            | 0x0000042A | The service has returned a service-specific error code.                                                                                                                                                                                       |
| **`WIN32_NO_ERROR`**                                | 0x00000000 | No error.                                                                                                                                                                                                                                     |

| Constant                                | Value      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **`WIN32_ABOVE_NORMAL_PRIORITY_CLASS`** | 0x00008000 | Process that has priority above WIN32\_NORMAL\_PRIORITY\_CLASS but below WIN32\_HIGH\_PRIORITY\_CLASS.                                                                                                                                                                                                                                                                                                                                         |
| **`WIN32_BELOW_NORMAL_PRIORITY_CLASS`** | 0x00004000 | Process that has priority above WIN32\_IDLE\_PRIORITY\_CLASS but below WIN32\_NORMAL\_PRIORITY\_CLASS.                                                                                                                                                                                                                                                                                                                                         |
| **`WIN32_HIGH_PRIORITY_CLASS`**         | 0x00000080 | Process that performs time-critical tasks that must be executed immediately. The threads of the process preempt the threads of normal or idle priority class processes. An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system. Use extreme care when using the high-priority class, because a high-priority class application can use nearly all available CPU time. |
| **`WIN32_IDLE_PRIORITY_CLASS`**         | 0x00000040 | Process whose threads run only when the system is idle. The threads of the process are preempted by the threads of any process running in a higher priority class. An example is a screen saver. The idle-priority class is inherited by child processes.                                                                                                                                                                                      |
| **`WIN32_NORMAL_PRIORITY_CLASS`**       | 0x00000020 | Process with no special scheduling needs.                                                                                                                                                                                                                                                                                                                                                                                                      |
| **`WIN32_REALTIME_PRIORITY_CLASS`**     | 0x00000100 | Process that has the highest possible priority. The threads of the process preempt the threads of all other processes, including operating system processes performing important tasks. For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or cause the mouse to be unresponsive.                                                                                           |

| Constant                          | Value      | Description          |
|-----------------------------------|------------|----------------------|
| **`WIN32_SC_ACTION_NONE`**        | 0x00000000 | No action.           |
| **`WIN32_SC_ACTION_REBOOT`**      | 0x00000001 | Restart the server.  |
| **`WIN32_SC_ACTION_RESTART`**     | 0x00000002 | Restart the service. |
| **`WIN32_SC_ACTION_RUN_COMMAND`** | 0x00000003 | Run a command.       |

| Constant                         | Value                     | Description |
|----------------------------------|---------------------------|-------------|
| **`WIN32_INFO_SERVICE`**         | "service"                 |             |
| **`WIN32_INFO_DISPLAY`**         | "display"                 |             |
| **`WIN32_INFO_USER`**            | "user"                    |             |
| **`WIN32_INFO_PASSWORD`**        | "password"                |             |
| **`WIN32_INFO_PATH`**            | "path"                    |             |
| **`WIN32_INFO_PARAMS`**          | "params"                  |             |
| **`WIN32_INFO_DESCRIPTION`**     | "description"             |             |
| **`WIN32_INFO_START_TYPE`**      | "start\_type"             |             |
| **`INFO_LOAD_ORDER`**            | "load\_order"             |             |
| **`INFO_SVC_TYPE`**              | "svc\_type"               |             |
| **`INFO_ERROR_CONTROL`**         | "error\_control"          |             |
| **`INFO_DELAYED_START`**         | "delayed\_start"          |             |
| **`INFO_BASE_PRIORITY`**         | "base\_priority"          |             |
| **`INFO_DEPENDENCIES`**          | "dependencies"            |             |
| **`INFO_RECOVERY_DELAY`**        | "recovery\_delay"         |             |
| **`INFO_RECOVERY_ACTION_1`**     | "recovery\_action\_1"     |             |
| **`INFO_RECOVERY_ACTION_2`**     | "recovery\_action\_2"     |             |
| **`INFO_RECOVERY_ACTION_3`**     | "recovery\_action\_3"     |             |
| **`INFO_RECOVERY_RESET_PERIOD`** | "recovery\_reset\_period" |             |
| **`INFO_RECOVERY_ENABLED`**      | "recovery\_enabled"       |             |
| **`INFO_RECOVERY_REBOOT_MSG`**   | "recovery\_reboot\_msg"   |             |
| **`INFO_RECOVERY_COMMAND`**      | "recovery\_command"       |             |

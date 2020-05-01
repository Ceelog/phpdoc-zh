win32service
============

**目录**

-   [简介](/intro/win32service.html)
-   [安装／配置](/win32service/setup.html)
    -   [需求](/win32service/setup.html#需求)
    -   [安装](/win32service/setup.html#安装)
    -   [运行时配置](/win32service/setup.html#运行时配置)
    -   [资源类型](/win32service/setup.html#资源类型)
    -   [Security
        consideration](/win32service/setup.html#Security%20consideration)
-   [预定义常量](/win32service/constants.html)
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
-   [范例](/win32service/examples.html)
-   [win32service 函数](/ref/win32service.html)
    -   [win32\_continue\_service](/ref/win32service.html#win32_continue_service)
        — Resumes a paused service
    -   [win32\_create\_service](/ref/win32service.html#win32_create_service)
        — Creates a new service entry in the SCM database
    -   [win32\_delete\_service](/ref/win32service.html#win32_delete_service)
        — Deletes a service entry from the SCM database
    -   [win32\_get\_last\_control\_message](/ref/win32service.html#win32_get_last_control_message)
        — Returns the last control message that was sent to this service
    -   [win32\_pause\_service](/ref/win32service.html#win32_pause_service)
        — Pauses a service
    -   [win32\_query\_service\_status](/ref/win32service.html#win32_query_service_status)
        — Queries the status of a service
    -   [win32\_send\_custom\_control](/ref/win32service.html#win32_send_custom_control)
        — Send a custom control to the service
    -   [win32\_set\_service\_exit\_code](/ref/win32service.html#win32_set_service_exit_code)
        — Define or return the exit code for the current running service
    -   [win32\_set\_service\_exit\_mode](/ref/win32service.html#win32_set_service_exit_mode)
        — Define or return the exit mode for the current running service
    -   [win32\_set\_service\_status](/ref/win32service.html#win32_set_service_status)
        — Update the service status
    -   [win32\_start\_service\_ctrl\_dispatcher](/ref/win32service.html#win32_start_service_ctrl_dispatcher)
        — Registers the script with the SCM, so that it can act as the
        service with the given name
    -   [win32\_start\_service](/ref/win32service.html#win32_start_service)
        — Starts a service
    -   [win32\_stop\_service](/ref/win32service.html#win32_stop_service)
        — Stops a service

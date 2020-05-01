Gupnp
=====

**目录**

-   [简介](/intro/gupnp.html)
-   [安装／配置](/gupnp/setup.html)
    -   [需求](/gupnp/setup.html#需求)
    -   [安装](/gupnp/setup.html#安装)
    -   [运行时配置](/gupnp/setup.html#运行时配置)
    -   [资源类型](/gupnp/setup.html#资源类型)
-   [预定义常量](/gupnp/constants.html)
-   [范例](/gupnp/examples.html)
    -   [Browsing devices and
        services](/gupnp/examples.html#Browsing%20devices%20and%20services)
    -   [Implementing the BinaryLight
        device](/gupnp/examples.html#Implementing%20the%20BinaryLight%20device)
-   [Gupnp 函数](/ref/gupnp.html)
    -   [gupnp\_context\_get\_host\_ip](/ref/gupnp.html#gupnp_context_get_host_ip)
        — Get the IP address
    -   [gupnp\_context\_get\_port](/ref/gupnp.html#gupnp_context_get_port)
        — Get the port
    -   [gupnp\_context\_get\_subscription\_timeout](/ref/gupnp.html#gupnp_context_get_subscription_timeout)
        — Get the event subscription timeout
    -   [gupnp\_context\_host\_path](/ref/gupnp.html#gupnp_context_host_path)
        — Start hosting
    -   [gupnp\_context\_new](/ref/gupnp.html#gupnp_context_new) —
        Create a new context
    -   [gupnp\_context\_set\_subscription\_timeout](/ref/gupnp.html#gupnp_context_set_subscription_timeout)
        — Sets the event subscription timeout
    -   [gupnp\_context\_timeout\_add](/ref/gupnp.html#gupnp_context_timeout_add)
        — Sets a function to be called at regular intervals
    -   [gupnp\_context\_unhost\_path](/ref/gupnp.html#gupnp_context_unhost_path)
        — Stop hosting
    -   [gupnp\_control\_point\_browse\_start](/ref/gupnp.html#gupnp_control_point_browse_start)
        — Start browsing
    -   [gupnp\_control\_point\_browse\_stop](/ref/gupnp.html#gupnp_control_point_browse_stop)
        — Stop browsing
    -   [gupnp\_control\_point\_callback\_set](/ref/gupnp.html#gupnp_control_point_callback_set)
        — Set control point callback
    -   [gupnp\_control\_point\_new](/ref/gupnp.html#gupnp_control_point_new)
        — Create a new control point
    -   [gupnp\_device\_action\_callback\_set](/ref/gupnp.html#gupnp_device_action_callback_set)
        — Set device callback function
    -   [gupnp\_device\_info\_get\_service](/ref/gupnp.html#gupnp_device_info_get_service)
        — Get the service with type
    -   [gupnp\_device\_info\_get](/ref/gupnp.html#gupnp_device_info_get)
        — Get info of root device
    -   [gupnp\_root\_device\_get\_available](/ref/gupnp.html#gupnp_root_device_get_available)
        — Check whether root device is available
    -   [gupnp\_root\_device\_get\_relative\_location](/ref/gupnp.html#gupnp_root_device_get_relative_location)
        — Get the relative location of root device
    -   [gupnp\_root\_device\_new](/ref/gupnp.html#gupnp_root_device_new)
        — Create a new root device
    -   [gupnp\_root\_device\_set\_available](/ref/gupnp.html#gupnp_root_device_set_available)
        — Set whether or not root\_device is available
    -   [gupnp\_root\_device\_start](/ref/gupnp.html#gupnp_root_device_start)
        — Start main loop
    -   [gupnp\_root\_device\_stop](/ref/gupnp.html#gupnp_root_device_stop)
        — Stop main loop
    -   [gupnp\_service\_action\_get](/ref/gupnp.html#gupnp_service_action_get)
        — Retrieves the specified action arguments
    -   [gupnp\_service\_action\_return\_error](/ref/gupnp.html#gupnp_service_action_return_error)
        — Return error code
    -   [gupnp\_service\_action\_return](/ref/gupnp.html#gupnp_service_action_return)
        — Return successfully
    -   [gupnp\_service\_action\_set](/ref/gupnp.html#gupnp_service_action_set)
        — Sets the specified action return values
    -   [gupnp\_service\_freeze\_notify](/ref/gupnp.html#gupnp_service_freeze_notify)
        — Freeze new notifications
    -   [gupnp\_service\_info\_get\_introspection](/ref/gupnp.html#gupnp_service_info_get_introspection)
        — Get resource introspection of service
    -   [gupnp\_service\_info\_get](/ref/gupnp.html#gupnp_service_info_get)
        — Get full info of service
    -   [gupnp\_service\_introspection\_get\_state\_variable](/ref/gupnp.html#gupnp_service_introspection_get_state_variable)
        — Returns the state variable data
    -   [gupnp\_service\_notify](/ref/gupnp.html#gupnp_service_notify) —
        Notifies listening clients
    -   [gupnp\_service\_proxy\_action\_get](/ref/gupnp.html#gupnp_service_proxy_action_get)
        — Send action to the service and get value
    -   [gupnp\_service\_proxy\_action\_set](/ref/gupnp.html#gupnp_service_proxy_action_set)
        — Send action to the service and set value
    -   [gupnp\_service\_proxy\_add\_notify](/ref/gupnp.html#gupnp_service_proxy_add_notify)
        — Sets up callback for variable change notification
    -   [gupnp\_service\_proxy\_callback\_set](/ref/gupnp.html#gupnp_service_proxy_callback_set)
        — Set service proxy callback for signal
    -   [gupnp\_service\_proxy\_get\_subscribed](/ref/gupnp.html#gupnp_service_proxy_get_subscribed)
        — Check whether subscription is valid to the service
    -   [gupnp\_service\_proxy\_remove\_notify](/ref/gupnp.html#gupnp_service_proxy_remove_notify)
        — Cancels the variable change notification
    -   [gupnp\_service\_proxy\_send\_action](/ref/gupnp.html#gupnp_service_proxy_send_action)
        — Send action with multiple parameters synchronously
    -   [gupnp\_service\_proxy\_set\_subscribed](/ref/gupnp.html#gupnp_service_proxy_set_subscribed)
        — (Un)subscribes to the service
    -   [gupnp\_service\_thaw\_notify](/ref/gupnp.html#gupnp_service_thaw_notify)
        — Sends out any pending notifications and stops queuing of new
        ones

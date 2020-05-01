范例
====

**示例 \#1 Registering a PHP script to run as a service**

``` php
<?php
win32_create_service(array(
    'service'     => 'dummyphp',                                           # the name of your service
    'display'     => 'sample dummy PHP service',                           # short description
    'description' => 'This is a dummy Windows service created using PHP.', # long description
    'params'      => '"' . __FILE__ . '"  run',                            # path to the script and parameters
));
?>
```

**示例 \#2 Unregistering a service**

``` php
<?php
win32_delete_service('dummyphp');
?>
```

**示例 \#3 Running as a service**

``` php
<?php
if ($argv[1] == 'run') {
  win32_start_service_ctrl_dispatcher('dummyphp');

  while (WIN32_SERVICE_CONTROL_STOP != win32_get_last_control_message()) {
    # do your work here.
    # try not to take up more than 30 seconds before going around the loop
    # again
  }
}
?>
```

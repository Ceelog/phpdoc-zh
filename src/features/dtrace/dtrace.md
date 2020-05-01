使用 PHP 和 DTrace
------------------

在支持 DTrace 动态跟踪的平台上，可以配置 PHP 打开 DTrace 静态探针。

### PHP DTrace 静态探针配置

请参考操作系统文档获取启用操作系统 DTrace 支持的信息。 例如，在 Oracle
Linux 系统上启动 UEK3 内核，并进行如下操作：

``` php
# modprobe fasttrap
# chmod 666 /dev/dtrace/helper
```

除了 *chmod* 命令，您也可以使用 ACL
包规则来限制特定用户对于设备的访问权限。

使用 *--enable-dtrace* 配置参数构建 PHP：

``` php
# ./configure --enable-dtrace ...
# make
# make install
```

这样就启用了 PHP 核心的静态探针。对于提供了自有探针的 PHP
扩展需要分别构建。

### PHP 核心的 DTrace 静态探针

| 探针名称              | 探针描述                                                                                                                | 探针参数                                                                                        |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| *request-startup*     | 请求开始时触发。                                                                                                        | char \*`file`, char \*`request_uri`, char \*`request_method`                                    |
| *request-shutdown*    | 请求关闭时触发。                                                                                                        | char \*`file`, char \*`request_uri`, char \*`request_method`                                    |
| *compile-file-entry*  | 脚本开始编译时触发。                                                                                                    | char \*`compile_file`, char \*`compile_file_translated`                                         |
| *compile-file-return* | 脚本完成编译时触发。                                                                                                    | char \*`compile_file`, char \*`compile_file_translated`                                         |
| *execute-entry*       | 操作数数组开始执行时触发。例如：函数调用，文件包含以及生成器恢复时会被触发。                                            | char \*`request_file`, int `lineno`                                                             |
| *execute-return*      | 操作数数组执行完毕之后触发。                                                                                            | char \*`request_file`, int `lineno`                                                             |
| *function-entry*      | PHP 引擎进入 PHP 函数或者方法调用时触发。                                                                               | char \*`function_name`, char \*`request_file`, int `lineno`, char \*`classname`, char \*`scope` |
| *function-return*     | PHP 引擎从 PHP 函数或者方法调用返回后触发。.                                                                            | char \*`function_name`, char \*`request_file`, int `lineno`, char \*`classname`, char \*`scope` |
| *exception-thrown*    | 有异常抛出时触发。                                                                                                      | char \*`classname`                                                                              |
| *exception-caught*    | 有异常被捕获时触发。                                                                                                    | char \*`classname`                                                                              |
| *error*               | 无论 <a href="/errorfunc/setup.html#PHP外的PHP常量" class="link">error_reporting</a> 的设定如何，在发生错误时都会触发。 | char \*`errormsg`, char \*`request_file`, int `lineno`                                          |

PHP 扩展可以拥有额外的静态探针。

### 列出 PHP 中可用的静态探针

要列出 PHP 中可用的静态探针，开启一个 PHP 进程，然后运行：

    # dtrace -l

输出信息类似如下所示：

       ID   PROVIDER            MODULE                          FUNCTION NAME
       [ . . . ]
        4   php15271               php               dtrace_compile_file compile-file-entry
        5   php15271               php               dtrace_compile_file compile-file-return
        6   php15271               php                        zend_error error
        7   php15271               php  ZEND_CATCH_SPEC_CONST_CV_HANDLER exception-caught
        8   php15271               php     zend_throw_exception_internal exception-thrown
        9   php15271               php                 dtrace_execute_ex execute-entry
       10   php15271               php           dtrace_execute_internal execute-entry
       11   php15271               php                 dtrace_execute_ex execute-return
       12   php15271               php           dtrace_execute_internal execute-return
       13   php15271               php                 dtrace_execute_ex function-entry
       14   php15271               php                 dtrace_execute_ex function-return
       15   php15271               php              php_request_shutdown request-shutdown
       16   php15271               php               php_request_startup request-startup

Provider 一列由 *php* 和当前进程 id 的组成。

如果运行的是 Apache web 服务器，那么模块名称可能是 `libphp5.so`，
并且可能会出现多块信息，每个运行中的 Apache 进程对应一个输出块。

Function Name 一列表示 Provider 对应的 PHP 内部 C 实现函数名称。

如果没有运行任何 PHP 进程，那么就不会显示任何 PHP 探针。

### PHP DTrace 示例

下例展示了基本的 DTrace D 脚本。

**示例 \#1 `all_probes.d` for tracing all PHP Static Probes with
DTrace**

    #!/usr/sbin/dtrace -Zs

    #pragma D option quiet

    php*:::compile-file-entry
    {
        printf("PHP compile-file-entry\n");
        printf("  compile_file              %s\n", copyinstr(arg0));
        printf("  compile_file_translated   %s\n", copyinstr(arg1));
    }

    php*:::compile-file-return
    {
        printf("PHP compile-file-return\n");
        printf("  compile_file              %s\n", copyinstr(arg0));
        printf("  compile_file_translated   %s\n", copyinstr(arg1));
    }

    php*:::error
    {
        printf("PHP error\n");
        printf("  errormsg                  %s\n", copyinstr(arg0));
        printf("  request_file              %s\n", copyinstr(arg1));
        printf("  lineno                    %d\n", (int)arg2);
    }

    php*:::exception-caught
    {
        printf("PHP exception-caught\n");
        printf("  classname                 %s\n", copyinstr(arg0));
    }

    php*:::exception-thrown
    {
        printf("PHP exception-thrown\n");
        printf("  classname                 %s\n", copyinstr(arg0));
    }

    php*:::execute-entry
    {
        printf("PHP execute-entry\n");
        printf("  request_file              %s\n", copyinstr(arg0));
        printf("  lineno                    %d\n", (int)arg1);
    }

    php*:::execute-return
    {
        printf("PHP execute-return\n");
        printf("  request_file              %s\n", copyinstr(arg0));
        printf("  lineno                    %d\n", (int)arg1);
    }

    php*:::function-entry
    {
        printf("PHP function-entry\n");
        printf("  function_name             %s\n", copyinstr(arg0));
        printf("  request_file              %s\n", copyinstr(arg1));
        printf("  lineno                    %d\n", (int)arg2);
        printf("  classname                 %s\n", copyinstr(arg3));
        printf("  scope                     %s\n", copyinstr(arg4));
    }

    php*:::function-return
    {
        printf("PHP function-return\n");
        printf("  function_name             %s\n", copyinstr(arg0));
        printf("  request_file              %s\n", copyinstr(arg1));
        printf("  lineno                    %d\n", (int)arg2);
        printf("  classname                 %s\n", copyinstr(arg3));
        printf("  scope                     %s\n", copyinstr(arg4));
    }

    php*:::request-shutdown
    {
        printf("PHP request-shutdown\n");
        printf("  file                      %s\n", copyinstr(arg0));
        printf("  request_uri               %s\n", copyinstr(arg1));
        printf("  request_method            %s\n", copyinstr(arg2));
    }

    php*:::request-startup
    {
        printf("PHP request-startup\n");
        printf("  file                      %s\n", copyinstr(arg0));
        printf("  request_uri               %s\n", copyinstr(arg1));
        printf("  request_method            %s\n", copyinstr(arg2));
    }

此脚本在 `dtrace` 命令中使用了 *-Z* 选项。 此选项保证即使在没有任何 PHP
进程运行的时候脚本也能够正确执行。
如果省略了此选项，当没有任何探针可监控的时候，脚本会立即终止执行。

在运行此脚本的过程中，它将监控全部 PHP 核心静态探针。 运行 D 脚本：

    # ./all_probes.d

再运行一个 PHP 脚本或者 PHP 应用，用来进行监控的 D
脚本会输出每个探针被触发时所携带的参数。

监控完成之后，使用 *^C* 来终止 D 脚本的执行。

在多 CPU 的主机上，探针的显示顺序可能不是连续的，这取决于哪颗 CPU
执行探针以及多个 CPU 之间的线程迁移情况。
可以通过显示探针时间戳来减少混淆，例如：

    php*:::function-entry
    {
          printf("%lld: PHP function-entry ", walltimestamp);
          [ . . .]
    }

### 参见

-   <a href="/book/oci8.html#OCI8%20and%20DTrace%20Dynamic%20Tracing" class="link">OCI8 和 DTrace 动态跟踪</a>

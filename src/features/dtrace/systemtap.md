使用 SystemTap 监控 PHP DTrace 静态探针
---------------------------------------

在某些 Linux 发行版上，可以使用 SystemTap 跟踪工具来跟踪 PHP 的静态
DTrace 探针。 此特性在 PHP 5.4.20 和 PHP 5.5 中具备。

### 安装支持 SystemTap 的 PHP

安装 SystemTap SDT 开发包。

``` shell
# yum install systemtap-sdt-devel
```

安装 PHP 并启用 DTrace 探针：

``` shell
# ./configure --enable-dtrace ...
# make
```

### 使用 SystemTap 列出 PHP 静态探针

使用 `stap` 命令列出 PHP 静态探针：

    # stap -l 'process.provider("php").mark("*")' -c 'sapi/cli/php -i'

输出如下：

    process("sapi/cli/php").provider("php").mark("compile__file__entry")
    process("sapi/cli/php").provider("php").mark("compile__file__return")
    process("sapi/cli/php").provider("php").mark("error")
    process("sapi/cli/php").provider("php").mark("exception__caught")
    process("sapi/cli/php").provider("php").mark("exception__thrown")
    process("sapi/cli/php").provider("php").mark("execute__entry")
    process("sapi/cli/php").provider("php").mark("execute__return")
    process("sapi/cli/php").provider("php").mark("function__entry")
    process("sapi/cli/php").provider("php").mark("function__return")
    process("sapi/cli/php").provider("php").mark("request__shutdown")
    process("sapi/cli/php").provider("php").mark("request__startup")

### SystemTap 示例

**示例 \#1 `all_probes.stp` for tracing all PHP Static Probes with
SystemTap**

``` shell
probe process("sapi/cli/php").provider("php").mark("compile__file__entry") {
    printf("Probe compile__file__entry\n");
    printf("  compile_file %s\n", user_string($arg1));
    printf("  compile_file_translated %s\n", user_string($arg2));
}
probe process("sapi/cli/php").provider("php").mark("compile__file__return") {
    printf("Probe compile__file__return\n");
    printf("  compile_file %s\n", user_string($arg1));
    printf("  compile_file_translated %s\n", user_string($arg2));
}
probe process("sapi/cli/php").provider("php").mark("error") {
    printf("Probe error\n");
    printf("  errormsg %s\n", user_string($arg1));
    printf("  request_file %s\n", user_string($arg2));
    printf("  lineno %d\n", $arg3);
}
probe process("sapi/cli/php").provider("php").mark("exception__caught") {
    printf("Probe exception__caught\n");
    printf("  classname %s\n", user_string($arg1));
}
probe process("sapi/cli/php").provider("php").mark("exception__thrown") {
    printf("Probe exception__thrown\n");
    printf("  classname %s\n", user_string($arg1));
}
probe process("sapi/cli/php").provider("php").mark("execute__entry") {
    printf("Probe execute__entry\n");
    printf("  request_file %s\n", user_string($arg1));
    printf("  lineno %d\n", $arg2);
}
probe process("sapi/cli/php").provider("php").mark("execute__return") {
    printf("Probe execute__return\n");
    printf("  request_file %s\n", user_string($arg1));
    printf("  lineno %d\n", $arg2);
}
probe process("sapi/cli/php").provider("php").mark("function__entry") {
    printf("Probe function__entry\n");
    printf("  function_name %s\n", user_string($arg1));
    printf("  request_file %s\n", user_string($arg2));
    printf("  lineno %d\n", $arg3);
    printf("  classname %s\n", user_string($arg4));
    printf("  scope %s\n", user_string($arg5));
}
probe process("sapi/cli/php").provider("php").mark("function__return") {
    printf("Probe function__return: %s\n", user_string($arg1));
    printf(" function_name %s\n", user_string($arg1));
    printf("  request_file %s\n", user_string($arg2));
    printf("  lineno %d\n", $arg3);
    printf("  classname %s\n", user_string($arg4));
    printf("  scope %s\n", user_string($arg5));
}
probe process("sapi/cli/php").provider("php").mark("request__shutdown") {
    printf("Probe request__shutdown\n");
    printf("  file %s\n", user_string($arg1));
    printf("  request_uri %s\n", user_string($arg2));
    printf("  request_method %s\n", user_string($arg3));
}
probe process("sapi/cli/php").provider("php").mark("request__startup") {
    printf("Probe request__startup\n");
    printf("  file %s\n", user_string($arg1));
    printf("  request_uri %s\n", user_string($arg2));
    printf("  request_method %s\n", user_string($arg3));
}
```

在 PHP 脚本的执行过程中，上述脚本会跟踪所有的 PHP 核心静态探针：

    # stap -c 'sapi/cli/php test.php' all_probes.stp

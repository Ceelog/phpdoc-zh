INI 文件处理的变化
------------------

下列 `php.ini` 指令被移除：

-   <span class="simpara">
    <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
    和
    <a href="/ini/core.html#ini.register-long-arrays" class="link">register_long_arrays</a>
    </span>
-   <span class="simpara">
    <a href="/info/setup.html#" class="link">magic_quotes_gpc</a> 、
    <a href="/info/setup.html#" class="link">magic_quotes_runtime</a>
    以及 magic\_quotes\_sybase </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.allow-call-time-pass-reference" class="link">allow_call_time_pass_reference</a>
    </span>
-   <span class="simpara">
    <a href="/network/setup.html#" class="link">define_syslog_variables</a>
    </span>
-   <span class="simpara">
    <a href="/misc/setup.html#" class="link">highlight.bg</a> </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">session.bug_compat_42</a>
    和
    <a href="/session/setup.html#" class="link">session.bug_compat_warn</a>
    </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.y2k-compliance" class="link">y2k_compliance</a>
    </span>
-   <span class="simpara">
    <a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">safe_mode</a>
    、
    <a href="/ini/sect/safe-mode.html#ini.safe-mode-gid" class="link">safe_mode_gid</a>
    、
    <a href="/ini/sect/safe-mode.html#ini.safe-mode-include-dir" class="link">safe_mode_include_dir</a>
    、
    <a href="/ini/sect/safe-mode.html#ini.safe-mode-exec-dir" class="link">safe_mode_exec_dir</a>
    、
    <a href="/ini/sect/safe-mode.html#ini.safe-mode-allowed-env-vars" class="link">safe_mode_allowed_env_vars</a>
    以及
    <a href="/ini/sect/safe-mode.html#ini.safe-mode-protected-env-vars" class="link">safe_mode_protected_env_vars</a>
    </span>

新增下列 `php.ini` 指令：

-   <span class="simpara">
    <a href="/readline/setup.html#" class="link">cli.pager</a> 和
    <a href="/readline/setup.html#" class="link">cli.prompt</a> 对于 CLI
    SAPI 在交互模式中使用 readline </span>
-   <span class="simpara">
    <a href="/features/commandline/ini.html#ini.cli-server.color" class="link">cli_server.color</a>
    使内置用于开发的 web server 能在终端输出使用 ANSI 颜色编码。 </span>
-   <span class="simpara">
    <a href="/info/setup.html#" class="link">max_input_vars</a> - 指定
    GET/POST/COOKIE 输入变量的最大长度。 </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.zend.multibyte" class="link">zend.multibyte</a> -
    控制新的多字节支持。 </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.zend.script-encoding" class="link">zend.script_encoding</a> -
    除非在脚本最前面出现“declare(encoding=...)”指令，否则将使用此值。
    </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.zend.signal-check" class="link">zend.signal_check</a> -
    在关闭时检查是否替代信号处理。 </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">session.upload_progress.enabled</a>
    、
    <a href="/session/setup.html#" class="link">session.upload_progress.cleanup</a>
    、
    <a href="/session/setup.html#" class="link">session.upload_progress.prefix</a>
    、
    <a href="/session/setup.html#" class="link">session.upload_progress.name</a><a href="/session/setup.html#" class="link">session.upload_progress.freq</a>
    、
    <a href="/session/setup.html#" class="link">session.upload_progress.min_freq</a>
    </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.enable-post-data-reading" class="link">enable_post_data_reading</a> -
    禁用时，POST 数据不能读取（和处理）。 </span>
-   <span class="simpara">
    <a href="/ini/core.html#ini.windows-show-crt-warning" class="link">windows_show_crt_warning</a> -
    启用时此指令显示 Windows CRT
    警告。到目前为止这些警告都是默认显示的。 </span>

下列 `php.ini`. 指令被变更：

-   <span class="simpara">
    <a href="/session/setup.html#" class="link">session.entropy_file</a>
    现在默认为 /dev/random 或 /dev/urandom ，取决于在编译时的推测。
    </span>
-   <span class="simpara">
    <a href="/session/setup.html#" class="link">session.entropy_length</a>
    现在默认为 32 。 </span>

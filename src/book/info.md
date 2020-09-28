PHP 选项和信息
==============

**目录**

-   [简介](/intro/info.html)
-   [安装／配置](/info/setup.html)
    -   [需求](/info/setup.html#需求)
    -   [安装](/info/setup.html#安装)
    -   [运行时配置](/info/setup.html#运行时配置)
    -   [资源类型](/info/setup.html#资源类型)
-   [预定义常量](/info/constants.html)
-   [PHP 选项/信息 函数](/ref/info.html)
    -   [assert\_options](/ref/info.html#assert_options) —
        设置/获取断言的各种标志
    -   [assert](/ref/info.html#assert) — 检查一个断言是否为 FALSE
    -   [cli\_get\_process\_title](/ref/info.html#cli_get_process_title)
        — Returns the current process title
    -   [cli\_set\_process\_title](/ref/info.html#cli_set_process_title)
        — Sets the process title
    -   [dl](/ref/info.html#dl) — 运行时载入一个 PHP 扩展
    -   [extension\_loaded](/ref/info.html#extension_loaded) —
        检查一个扩展是否已经加载
    -   [gc\_collect\_cycles](/ref/info.html#gc_collect_cycles) —
        强制收集所有现存的垃圾循环周期
    -   [gc\_disable](/ref/info.html#gc_disable) — 停用循环引用收集器
    -   [gc\_enable](/ref/info.html#gc_enable) — 激活循环引用收集器
    -   [gc\_enabled](/ref/info.html#gc_enabled) —
        返回循环引用计数器的状态
    -   [gc\_mem\_caches](/ref/info.html#gc_mem_caches) — Reclaims
        memory used by the Zend Engine memory manager
    -   [gc\_status](/ref/info.html#gc_status) — Gets information about
        the garbage collector
    -   [get\_cfg\_var](/ref/info.html#get_cfg_var) — 获取 PHP
        配置选项的值
    -   [get\_current\_user](/ref/info.html#get_current_user) — 获取当前
        PHP 脚本所有者名称
    -   [get\_defined\_constants](/ref/info.html#get_defined_constants)
        — 返回所有常量的关联数组，键是常量名，值是常量值
    -   [get\_extension\_funcs](/ref/info.html#get_extension_funcs) —
        返回模块函数名称的数组
    -   [get\_include\_path](/ref/info.html#get_include_path) —
        获取当前的 include\_path 配置选项
    -   [get\_included\_files](/ref/info.html#get_included_files) —
        返回被 include 和 require 文件名的 array
    -   [get\_loaded\_extensions](/ref/info.html#get_loaded_extensions)
        — 返回所有编译并加载模块名的 array
    -   [get\_magic\_quotes\_gpc](/ref/info.html#get_magic_quotes_gpc) —
        获取当前 magic\_quotes\_gpc 的配置选项设置
    -   [get\_magic\_quotes\_runtime](/ref/info.html#get_magic_quotes_runtime)
        — 获取当前 magic\_quotes\_runtime 配置选项的激活状态
    -   [get\_required\_files](/ref/info.html#get_required_files) — 别名
        get\_included\_files
    -   [get\_resources](/ref/info.html#get_resources) — Returns active
        resources
    -   [getenv](/ref/info.html#getenv) — 获取一个环境变量的值
    -   [getlastmod](/ref/info.html#getlastmod) — 获取页面最后修改的时间
    -   [getmygid](/ref/info.html#getmygid) — 获取当前 PHP 脚本拥有者的
        GID
    -   [getmyinode](/ref/info.html#getmyinode) —
        获取当前脚本的索引节点（inode）
    -   [getmypid](/ref/info.html#getmypid) — 获取 PHP 进程的 ID
    -   [getmyuid](/ref/info.html#getmyuid) — 获取 PHP 脚本所有者的 UID
    -   [getopt](/ref/info.html#getopt) — 从命令行参数列表中获取选项
    -   [getrusage](/ref/info.html#getrusage) — 获取当前资源使用状况
    -   [ini\_alter](/ref/info.html#ini_alter) — 别名 ini\_set
    -   [ini\_get\_all](/ref/info.html#ini_get_all) — 获取所有配置选项
    -   [ini\_get](/ref/info.html#ini_get) — 获取一个配置选项的值
    -   [ini\_restore](/ref/info.html#ini_restore) — 恢复配置选项的值
    -   [ini\_set](/ref/info.html#ini_set) — 为一个配置选项设置值
    -   [main](/ref/info.html#main) — 虚拟的main
    -   [memory\_get\_peak\_usage](/ref/info.html#memory_get_peak_usage)
        — 返回分配给 PHP 内存的峰值
    -   [memory\_get\_usage](/ref/info.html#memory_get_usage) —
        返回分配给 PHP 的内存量
    -   [php\_ini\_loaded\_file](/ref/info.html#php_ini_loaded_file) —
        取得已加载的 php.ini 文件的路径
    -   [php\_ini\_scanned\_files](/ref/info.html#php_ini_scanned_files)
        — 返回从额外 ini 目录里解析的 .ini 文件列表
    -   [php\_sapi\_name](/ref/info.html#php_sapi_name) — 返回 web
        服务器和 PHP 之间的接口类型
    -   [php\_uname](/ref/info.html#php_uname) — 返回运行 PHP
        的系统的有关信息
    -   [phpcredits](/ref/info.html#phpcredits) — 打印 PHP 贡献者名单
    -   [phpinfo](/ref/info.html#phpinfo) — 输出关于 PHP 配置的信息
    -   [phpversion](/ref/info.html#phpversion) — 获取当前的PHP版本
    -   [putenv](/ref/info.html#putenv) — 设置环境变量的值
    -   [restore\_include\_path](/ref/info.html#restore_include_path) —
        还原 include\_path 配置选项的值
    -   [set\_include\_path](/ref/info.html#set_include_path) — 设置
        include\_path 配置选项
    -   [set\_time\_limit](/ref/info.html#set_time_limit) —
        设置脚本最大执行时间
    -   [sys\_get\_temp\_dir](/ref/info.html#sys_get_temp_dir) —
        返回用于临时文件的目录
    -   [version\_compare](/ref/info.html#version_compare) —
        对比两个「PHP 规范化」的版本数字字符串
    -   [zend\_thread\_id](/ref/info.html#zend_thread_id) —
        返回当前线程的唯一识别符
    -   [zend\_version](/ref/info.html#zend_version) — 获取当前 Zend
        引擎的版本

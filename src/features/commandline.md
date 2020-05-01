PHP 的命令行模式
================

**目录**

-   [内置Web Server](/features/commandline/webserver.html)
-   [INI 配置](/features/commandline/ini.html)

从版本 4.3.0 开始，PHP 提供了一种新类型的 CLI SAPI（Server Application
Programming Interface，服务端应用编程端口）支持，名为 CLI，意为 *Command
Line Interface*，即命令行接口。顾名思义，该 CLI SAPI 模块主要用作 PHP
的开发外壳应用。*CLI SAPI* 和其它 CLI SAPI
模块相比有很多的不同之处，我们将在本章中详细阐述。值得一提的是，CLI 和
*CGI* 是不同的 SAPI，尽管它们之间有很多共同的行为。

*CLI SAPI* 最先是随 PHP 4.2.0
版本发布的，但仍旧只是一个实验性的版本，并需要在运行 **./configure**
时加上 **--enable-cli** 参数。从 PHP 4.3.0 版本开始，*CLI SAPI*
成为了正式模块，**--enable-cli** 参数会被默认得设置为 on，也可以用参数
**--disable-cli** 来屏蔽。

从 PHP 4.3.0开始，CLI/CGI 二进制执行文件的文件名、位置和是否存在会根据
PHP 在系统上的安装而不同。在默认情况下，当运行 **make** 时，CGI 和 CLI
都会被编译并且分别放置在 PHP 源文件目录的 `sapi/cgi/php` 和
`sapi/cli/php` 下。可以注意到两个文件都被命名为了 php。在 **make
install** 的过程中会发生什么取决于配置行。如果在配置的时候选择了一个
SAPI 模块，如 apxs，或者使用了 **--disable-cgi** 参数，则在 **make
install** 的过程中，CLI 将被拷贝到 `{PREFIX}/bin/php`，除非 CGI
已经被放置在了那个位置。因此，例如，如果在配置行中有
**--with--apxs**，则在 *make install* 的过程中，CLI 将被拷贝到
*{PREFIX}/bin/php*。如果希望撤销 CGI 执行文件的安装，请在 **make
install** 之后运行 **make install-cli**。或者，也可以在配置行中加上
**--disable-cgi** 参数。

> **Note**:
>
> 由于 **--enable-cli** 和 **--enable-cgi**
> 同时默认有效，因此，不必再配置行中加上 **--enable-cli** 来使得 CLI 在
> **make install** 过程中被拷贝到 `{PREFIX}/bin/php`。

在 PHP 4.2.0 到 PHP 4.2.3 之间的 Windows 发行包中，CLI 的文件名为
`php-cli.exe`，相同文件夹下的 `php.exe` 为 CGI。从 PHP 4.3.0
版本开始，Windows 的发行包中 CLI 的执行文件为
`php.exe`，被放置在一个单独的名为 `cli` 的文件夹下，即 `cli/php.exe`。在
PHP 5 中，CLI 存在于主文件夹中，名为 `php.exe`，而 CGI 版本名为
`php-cgi.exe`。

从 PHP 5 起，一个名为 `php-win.exe` 的新文件随包发布。它相当于 CLI
版本，但是 php-win 不输出任何内容，便不提供控制台（不会弹出“DOS
窗口”）。这种方式类似于 php-gtk。需要使用 **--enable-cli-win32**
选项来配置它。

> **Note**: **如何得知自己使用的是哪个 SAPI？**  
>
> 在命令行下，运行 **php -v** 便能得知该 `php` 是 CGI 还是
> CLI。请参考函数 <span class="function">php\_sapi\_name</span> 以及常量
> **`PHP_SAPI`**。

> **Note**:
>
> 在 PHP 4.3.2 中加入了 Unix 的 *man* 页面。可以在命令行中键入 **man
> php** 来查看。

以下为 *CLI SAPI* 和其它 CLI SAPI 模块相比的显著区别：

-   与 *CGI SAPI* 不同，其输出没有任何头信息。

    尽管 *CGI SAPI* 提供了取消 HTTP 头信息的方法，但在 *CLI SAPI*
    中并不存在类似的方法以开启 HTTP 头信息的输出。

    CLI 默认以安静模式开始，但为了保证兼容性，**-q** 和 **--no-header**
    参数为了向后兼容仍然保留，使得可以使用旧的 CGI 脚本。

    在运行时，不会把工作目录改为脚本的当前目录（可以使用 **-C** 和
    **--no-chdir** 参数来兼容 CGI 模式）。

    出错时输出纯文本的错误信息（非 HTML 格式）。

-   *CLI SAPI* 强制覆盖了 `php.ini`
    中的某些设置，因为这些设置在外壳环境下是没有意义的。

    <table>
    <caption><strong>覆盖 <var class="filename">php.ini</var> 设置选项</strong></caption>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>设置选项</th>
    <th><em>CLI SAPI</em> 默认值</th>
    <th>备注</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><a href="/errorfunc/setup.html#" class="link">html_errors</a></td>
    <td><strong><code>FALSE</code></strong></td>
    <td>无意义的 HTML 标记符会使得出错信息很凌乱，所以在外壳下阅读报错信息是十分困难的。因此将该选项的默认值改为 <strong><code>FALSE</code></strong>。</td>
    </tr>
    <tr class="even">
    <td><a href="/outcontrol/setup.html#" class="link">implicit_flush</a></td>
    <td><strong><code>TRUE</code></strong></td>
    <td>在命令行模式下，所有来自 <span class="function">print</span> 和 <span class="function">echo</span> 的输出将被立即写到输出端，而不作任何地缓冲操作。如果希望延缓或控制标准输出，仍然可以使用 <a href="/ref/outcontrol.html" class="link">output buffering</a> 设置项。</td>
    </tr>
    <tr class="odd">
    <td><a href="/info/setup.html#" class="link">max_execution_time</a></td>
    <td>0（无限值）</td>
    <td>鉴于在外壳环境下使用 PHP 的无穷的可能性，最大运行时间被设置为了无限值。为 web 开发的应用程序可能只需运行几秒钟时间，而外壳应用程序的运行时间可能会长的多。</td>
    </tr>
    <tr class="even">
    <td><a href="/ini/core.html#ini.register-argc-argv" class="link">register_argc_argv</a></td>
    <td><strong><code>TRUE</code></strong></td>
    <td><p>由于该设置为 <strong><code>TRUE</code></strong>，将总是可以在 <em>CLI SAPI</em> 中访问到 <em>argc</em>（传送给应用程序参数的个数）和 <em>argv</em>（包含有实际参数的数组）。</p>
    <p>对于 PHP 4.3.0，在使用 <em>CLI SAPI</em> 时，PHP 变量 <em>$argc</em> 和 <em>$argv</em> 已被注册并且设定了对应的值。而在这之前的版本，这两个变量在 <em>CGI</em> 或者 <em>模块</em> 版本中的建立依赖于将 PHP 的设置选项 <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a> 设为 <em>on</em>。除了版本和 <em>register_globals</em> 设定以外，可以随时通过调用 <a href="/reserved/variables/server.html" class="link">$_SERVER</a> 或者 <var class="varname">$HTTP_SERVER_VARS</var> 来访问它们。例如：<var class="varname">$_SERVER['argv']</var></p></td>
    </tr>
    </tbody>
    </table>

    > **Note**:
    >
    > 这些设置无法在设置文件 `php.ini`
    > 或任何指定的其它文件中被初始化为其它值。这些默认值被限制在所有其它的设置文件被解析后改变。不过，它们的值可以在程序运行的过程中被改变（尽管对于该运行过程来说，这些设置项是没有意义的）。

-   为了减轻外壳环境下的工作，我们定义了如下常量：

    <table>
    <caption><strong>CLI 专用常量</strong></caption>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>常量名称</th>
    <th>描 述</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong><code>STDIN</code></strong></td>
    <td>一个已打开的指向 <em>stdin</em> 的流。可以用如下方法来调用：
    <div class="example-contents">
    <div class="phpcode">
    <div class="sourceCode" id="cb1"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb1-1"><a href="#cb1-1"></a><span class="kw">&lt;?php</span></span>
    <span id="cb1-2"><a href="#cb1-2"></a></span>
    <span id="cb1-3"><a href="#cb1-3"></a><span class="kw">$stdin</span> = <span class="fu">fopen</span><span class="ot">(</span><span class="st">&#39;php://stdin&#39;</span><span class="ot">,</span> <span class="st">&#39;r&#39;</span><span class="ot">);</span></span>
    <span id="cb1-4"><a href="#cb1-4"></a></span>
    <span id="cb1-5"><a href="#cb1-5"></a><span class="kw">?&gt;</span></span></code></pre></div>
    </div>
    </div>
    如果想从 <em>stdin</em> 读取一行内容，可以使用
    <div class="example-contents">
    <div class="phpcode">
    <div class="sourceCode" id="cb2"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb2-1"><a href="#cb2-1"></a><span class="kw">&lt;?php</span></span>
    <span id="cb2-2"><a href="#cb2-2"></a><span class="kw">$line</span> = <span class="fu">trim</span><span class="ot">(</span><span class="fu">fgets</span><span class="ot">(</span><span class="kw">STDIN</span><span class="ot">));</span> <span class="co">// 从 STDIN 读取一行</span></span>
    <span id="cb2-3"><a href="#cb2-3"></a><span class="fu">fscanf</span><span class="ot">(</span><span class="kw">STDIN</span><span class="ot">,</span> <span class="st">&quot;%d</span><span class="kw">\n</span><span class="st">&quot;</span><span class="ot">,</span> <span class="kw">$number</span><span class="ot">);</span> <span class="co">// 从 STDIN 读取数字</span></span>
    <span id="cb2-4"><a href="#cb2-4"></a><span class="kw">?&gt;</span></span></code></pre></div>
    </div>
    </div></td>
    </tr>
    <tr class="even">
    <td><strong><code>STDOUT</code></strong></td>
    <td>一个已打开的指向 <em>stdout</em> 的流。可以用如下方式来调用：
    <div class="example-contents">
    <div class="phpcode">
    <div class="sourceCode" id="cb3"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb3-1"><a href="#cb3-1"></a><span class="kw">&lt;?php</span></span>
    <span id="cb3-2"><a href="#cb3-2"></a></span>
    <span id="cb3-3"><a href="#cb3-3"></a><span class="kw">$stdout</span> = <span class="fu">fopen</span><span class="ot">(</span><span class="st">&#39;php://stdout&#39;</span><span class="ot">,</span> <span class="st">&#39;w&#39;</span><span class="ot">);</span></span>
    <span id="cb3-4"><a href="#cb3-4"></a></span>
    <span id="cb3-5"><a href="#cb3-5"></a><span class="kw">?&gt;</span></span></code></pre></div>
    </div>
    </div></td>
    </tr>
    <tr class="odd">
    <td><strong><code>STDERR</code></strong></td>
    <td>一个已打开的指向 <em>stderr</em> 的流。可以用如下方式来调用：
    <div class="example-contents">
    <div class="phpcode">
    <div class="sourceCode" id="cb4"><pre class="sourceCode php"><code class="sourceCode php"><span id="cb4-1"><a href="#cb4-1"></a><span class="kw">&lt;?php</span></span>
    <span id="cb4-2"><a href="#cb4-2"></a></span>
    <span id="cb4-3"><a href="#cb4-3"></a><span class="kw">$stderr</span> = <span class="fu">fopen</span><span class="ot">(</span><span class="st">&#39;php://stderr&#39;</span><span class="ot">,</span> <span class="st">&#39;w&#39;</span><span class="ot">);</span></span>
    <span id="cb4-4"><a href="#cb4-4"></a></span>
    <span id="cb4-5"><a href="#cb4-5"></a><span class="kw">?&gt;</span></span></code></pre></div>
    </div>
    </div></td>
    </tr>
    </tbody>
    </table>

    有了以上常量，就无需自己建立指向诸如 *stderr*
    的流，只需简单的使用这些常量来代替流指向：

    ``` shell
    php -r 'fwrite(STDERR, "stderr\n");'
    ```

    无需自己来关闭这些流，PHP 会自动完成这些操作。

-   *CLI SAPI* *不会*将当前目录改为已运行的脚本所在的目录。

    以下范例显示了本模块与 *CGI SAPI* 模块之间的不同：

    ``` php
    <?php
    // 名为 test.php 的简单测试程序
    echo getcwd(), "\n";
    ?>
    ```

    在使用 *CGI* 版本时，其输出为

        $ pwd
        /tmp

        $ php-cgi -f another_directory/test.php
        /tmp/another_directory

    明显可以看到 PHP 将当前目录改成了刚刚运行过的脚本所在的目录。

    使用 *CLI SAPI* 模式，得到：

        $ pwd
        /tmp

        $ php -q another_directory/test.php
        /tmp

    这使得在利用 PHP 编写外壳工具时获得了很大的便利。

    > **Note**:
    >
    > 可以在命令行运行时给该 *CGI SAPI* 加上 **-C** 参数，使其支持 *CLI
    > SAPI* 的功能。

以下是 PHP 二进制文件（即 `php.exe`
程序）提供的命令行模式的选项参数，随时可以运行带 **-h** 参数的 PHP
命令来查询这些参数。

    Usage: php [options] [-f] <file> [--] [args...]
           php [options] -r <code> [--] [args...]
           php [options] [-B <begin_code>] -R <code> [-E <end_code>] [--] [args...]
           php [options] [-B <begin_code>] -F <file> [-E <end_code>] [--] [args...]
           php [options] -- [args...]
           php [options] -a

      -a               Run interactively
      -c <path>|<file> Look for php.ini file in this directory
      -n               No php.ini file will be used
      -d foo[=bar]     Define INI entry foo with value 'bar'
      -e               Generate extended information for debugger/profiler
      -f <file>        Parse <file>.
      -h               This help
      -i               PHP information
      -l               Syntax check only (lint)
      -m               Show compiled in modules
      -r <code>        Run PHP <code> without using script tags <?..?>
      -B <begin_code>  Run PHP <begin_code> before processing input lines
      -R <code>        Run PHP <code> for every input line
      -F <file>        Parse and execute <file> for every input line
      -E <end_code>    Run PHP <end_code> after processing all input lines
      -H               Hide any passed arguments from external tools.
      -s               Display colour syntax highlighted source.
      -v               Version number
      -w               Display source with stripped comments and whitespace.
      -z <file>        Load Zend extension <file>.

      args...          Arguments passed to script. Use -- args when first argument
                       starts with - or script is read from stdin

*CLI SAPI* 模块有以下三种不同的方法来获取要运行的 PHP 代码：

1.  让 PHP 运行指定文件。

        php my_script.php

        php -f my_script.php

    以上两种方法（使用或不使用 **-f** 参数）都能够运行给定的
    `my_script.php` 文件。可以选择任何文件来运行，指定的 PHP
    脚本并非必须要以 *.php* 为扩展名，它们可以有任意的文件名和扩展名。

2.  在命令行直接运行 PHP 代码。

        php -r 'print_r(get_defined_constants());'

    在使用这种方法时，请注意外壳变量的替代及引号的使用。

    > **Note**:
    >
    > 请仔细阅读以上范例，在运行代码时没有开始和结束的标记符！加上
    > **-r** 参数后，这些标记符是不需要的，加上它们会导致语法错误。

3.  通过标准输入（*stdin*）提供需要运行的 PHP 代码。

    以上用法提供了非常强大的功能，使得可以如下范例所示，动态地生成 PHP
    代码并通过命令行运行这些代码：

        $ some_application | some_filter | php | sort -u >final_output.txt

以上三种运行代码的方法不能同时使用。

和所有的外壳应用程序一样，PHP 的二进制文件（`php.exe` 文件）及其运行的
PHP 脚本能够接受一系列的参数。PHP
没有限制传送给脚本程序的参数的个数（外壳程序对命令行的字符数有限制，但通常都不会超过该限制）。传递给脚本的参数可在全局变量
`$argv` 中获取。该数组中下标为零的成员为脚本的名称（当 PHP
代码来自标准输入获直接用 **-r**
参数以命令行方式运行时，该名称为“*-*”）。另外，全局变量 `$argc` 存有
`$argv` 数组中成员变量的个数（而非传送给脚本程序的参数的个数）。

只要传送给脚本的参数不是以 *-*
符号开头，就无需过多的注意什么。向脚本传送以 *-*
开头的参数会导致错误，因为 PHP
会认为应该由它自身来处理这些参数。可以用参数列表分隔符 *--*
来解决这个问题。在 PHP
解析完参数后，该符号后所有的参数将会被原样传送给脚本程序。

    # 以下命令将不会运行 PHP 代码，而只显示 PHP 命令行模式的使用说明：
    $ php -r 'var_dump($argv);' -h
    Usage: php [options] [-f] <file> [args...]
    [...]

    # 以下命令将会把“-h”参数传送给脚本程序，PHP 不会显示命令行模式的使用说明：
    $ php -r 'var_dump($argv);' -- -h
    array(2) {
      [0]=>
      string(1) "-"
      [1]=>
      string(2) "-h"
    }

除此之外，还有另一个方法将 PHP
用于外壳脚本。可以在写一个脚本，并在第一行以 *\#!/usr/bin/php*
开头，在其后加上以 PHP 开始和结尾标记符包含的正常的 PHP
代码，然后为该文件设置正确的运行属性（例如：**chmod +x
test**）。该方法可以使得该文件能够像外壳脚本或 PERL 脚本一样被直接执行。

``` php
#!/usr/bin/php
<?php
    var_dump($argv);
?>
```

假设改文件名为 `test` 并被放置在当前目录下，可以做如下操作：

    $ chmod +x test
    $ ./test -h -- foo
    array(4) {
      [0]=>
      string(6) "./test"
      [1]=>
      string(2) "-h"
      [2]=>
      string(2) "--"
      [3]=>
      string(3) "foo"
    }

正如所看到的，在向该脚本传送以 *-* 开头的参数时，脚本仍然能够正常运行。

PHP 4.3.3 以来有效的长选项:

<table>
<caption><strong>命令行选项</strong></caption>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>选项名称</th>
<th>长名称</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-a</td>
<td>--interactive</td>
<td><p>交互式运行 PHP。如果编译 PHP 时加入了 <a href="/ref/readline.html" class="link">Readline</a> 扩展（Windows 下不可用），那将会得到一个很好的外壳，包括一个自动完成的功能（例如可以在键入变量名的时候，按下 TAB 键，PHP 会自动完成该变量名）以及命令历史记录，可以用上下键来访问。历史记录存在 <var class="filename">~/.php_history</var> 文件中。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>通过 <a href="/ini/core.html#ini.auto-prepend-file" class="link">auto_prepend_file</a> 和 <a href="/ini/core.html#ini.auto-append-file" class="link">auto_append_file</a> 包含的文件在此模式下会被解析，但有些限制，例如函数必须在被调用之前定义。</p>
</blockquote></td>
</tr>
<tr class="even">
<td>-c</td>
<td>--php-ini</td>
<td><p>用该参数，可以指定一个放置 <var class="filename">php.ini</var> 文件的目录，或者直接指定一个自定义的 <em>INI</em> 文件（其文件名可以不是 <var class="filename">php.ini</var>），例如：</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>$ php -c /custom/directory/ my_script.php

$ php -c /custom/directory/custom-file.ini my_script.php</code></pre>
</div>
</div>
如果不指定此选项，PHP 将在<a href="/configuration/file.html" class="link">默认位置</a>搜索文件。</td>
</tr>
<tr class="odd">
<td>-n</td>
<td>--no-php-ini</td>
<td><p>完全忽略 <var class="filename">php.ini</var>。此参数在 PHP 4.3.0 以后有效。</p></td>
</tr>
<tr class="even">
<td>-d</td>
<td>--define</td>
<td><p>用该参数可以自行设置任何可以在 <var class="filename">php.ini</var> 文件中设置的配置选项的值，其语法为：</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>-d configuration_directive[=value]</code></pre>
</div>
</div>
<p>例子（因版面原因而折行显示）：</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code># 取值部分被省略，将会把配置选项设为 &quot;1&quot;
$ php -d max_execution_time
        -r &#39;$foo = ini_get(&quot;max_execution_time&quot;); var_dump($foo);&#39;
string(1) &quot;1&quot;

# 取值部分为空白，将会把配置选项设为 &quot;&quot;
php -d max_execution_time=
        -r &#39;$foo = ini_get(&quot;max_execution_time&quot;); var_dump($foo);&#39;
string(0) &quot;&quot;

# 配置选项将被设置成为任何 &#39;=&#39; 字符之后的值
$  php -d max_execution_time=20
        -r &#39;$foo = ini_get(&quot;max_execution_time&quot;); var_dump($foo);&#39;
string(2) &quot;20&quot;
$  php
        -d max_execution_time=doesntmakesense
        -r &#39;$foo = ini_get(&quot;max_execution_time&quot;); var_dump($foo);&#39;
string(15) &quot;doesntmakesense&quot;</code></pre>
</div>
</div></td>
</tr>
<tr class="odd">
<td>-e</td>
<td>--profile-info</td>
<td><p>激活扩展信息模式，被用于调试／测试。</p></td>
</tr>
<tr class="even">
<td>-f</td>
<td>--file</td>
<td><p>解析并运行 <strong>-f</strong> 选项给定的文件名。该参数为可选参数，可以省略，仅指明需要运行的文件名即可。</p></td>
</tr>
<tr class="odd">
<td>-h and -?</td>
<td>--help and --usage</td>
<td>使用该参数，可以得到完整的命令行参数的列表及这些参数作用的简单描述。</td>
</tr>
<tr class="even">
<td>-i</td>
<td>--info</td>
<td>该命令行参数会调用 <span class="function">phpinfo</span> 函数并显示出结果。如果 PHP 没有正常工作，建议执行 <strong>php -i</strong> 命令来查看在信息表格之前或者对应的地方是否有任何错误信息输出。请注意当使用 CGI 摸索时，输出的内容为 <em>HTML</em> 格式，因此输出的信息篇幅较大。</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>--syntax-check</td>
<td><p>该参数提供了对指定 PHP 代码进行语法检查的方便的方法。如果成功，则向标准输出写入 <em>No syntax errors detected in &lt;filename&gt;</em> 字符串，并且外壳返回值为 <em>0</em>。如果失败，则输出 <em>Errors parsing &lt;filename&gt;</em> 以及内部解析器错误信息到标准输出，同时外壳返回值将别设置为 <em>255</em>。</p>
<p>该参数将无法检查致命错误（如未定义函数），如果也希望检测致命错误，请使用 <strong>-f</strong> 参数。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>该参数不能和 <strong>-r</strong> 一同使用。</p>
</blockquote></td>
</tr>
<tr class="even">
<td>-m</td>
<td>--modules</td>
<td><p>使用该参数，PHP 将打印出内置以及已加载的 PHP 及 Zend 模块：</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>$ php -m
[PHP Modules]
xml
tokenizer
standard
session
posix
pcre
overload
mysql
mbstring
ctype

[Zend Modules]</code></pre>
</div>
</div></td>
</tr>
<tr class="odd">
<td>-r</td>
<td>--run</td>
<td><p>使用该参数可以在命令行内运行单行 PHP 代码。<em>无需</em>加上 PHP 的起始和结束标识符（<em>&lt;?php</em> 和 <em>?&gt;</em>），否则将会导致语法解析错误。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>使用这种形式的 PHP 时，应注意避免和外壳环境进行的命令行参数替换相冲突。</p>
<p>显示语法解析错误的范例</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>$ php -r &quot;$foo = get_defined_constants();&quot;
Command line code(1) : Parse error - parse error, unexpected &#39;=&#39;</code></pre>
</div>
</div>
<p>这里的问题在于即使使用了双引号 <em>"</em>，sh/bash 仍然实行了参数替换。由于 <var class="varname">$foo</var> 没有被定义，被替换后它所在的位置变成了空字符，因此在运行时，实际被 PHP 读取的代码为：</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>$ php -r &quot; = get_defined_constants();&quot;</code></pre>
</div>
</div>
<p>正确的方法是使用单引号 <em>'</em>。在用单引号引用的字符串中，变量不会被 sh/bash 还原成其原值。</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>$ php -r &#39;$foo = get_defined_constants(); var_dump($foo);&#39;
array(370) {
  [&quot;E_ERROR&quot;]=&gt;
  int(1)
  [&quot;E_WARNING&quot;]=&gt;
  int(2)
  [&quot;E_PARSE&quot;]=&gt;
  int(4)
  [&quot;E_NOTICE&quot;]=&gt;
  int(8)
  [&quot;E_CORE_ERROR&quot;]=&gt;
  [...]</code></pre>
</div>
</div>
<p>如果使用的外壳不是 sh/bash，可能会碰到更多问题。请将碰到的 Bug 向 <a href="https://bugs.php.net/" class="link external">» https://bugs.php.net/</a> 报告。注意，当试图将 shell 变量用到代码中或者使用反斜线时仍然很容易碰到问题。</p>
</blockquote>
<blockquote>
<p><strong>Note</strong>:</p>
<p><strong>-r</strong> 在 <em>CLI</em> SAPI 中有效，在 <em>CGI</em> SAPI 中无效。</p>
</blockquote>
<blockquote>
<p><strong>Note</strong>:</p>
<p>此选项只用于非常基本的用途。因此一些配置指令（例如 <a href="/ini/core.html#ini.auto-prepend-file" class="link">auto_prepend_file</a> 和 <a href="/ini/core.html#ini.auto-append-file" class="link">auto_append_file</a>）在此模式下被忽略。</p>
</blockquote></td>
</tr>
<tr class="even">
<td>-B</td>
<td>--process-begin</td>
<td><p>在处理 stdin 之前先执行 PHP 代码。PHP 5 新加。</p></td>
</tr>
<tr class="odd">
<td>-R</td>
<td>--process-code</td>
<td><p>对每个输入行都执行 PHP 代码。PHP 5 新加。</p>
<p>此模式下有两个特殊变量：<var class="varname">$argn</var> 和 <var class="varname">$argi</var>。<var class="varname">$argn</var> 包含 PHP 当前处理的行内容，而 <var class="varname">$argi</var> 则包含该行号。</p></td>
</tr>
<tr class="even">
<td>-F</td>
<td>--process-file</td>
<td><p>对每个输入行都执行 PHP 文件。PHP 5 新加。</p></td>
</tr>
<tr class="odd">
<td>-E</td>
<td>--process-end</td>
<td><p>在处理完输入后执行的 PHP 代码。PHP 5 新加。</p>
<p>使用 <strong>-B</strong>，<strong>-R</strong> 和 <strong>-E</strong> 选项来计算一个项目总行数的例子。</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>$ find my_proj | php -B &#39;$l=0;&#39; -R &#39;$l += count(@file($argn));&#39; -E &#39;echo &quot;Total Lines: $l\n&quot;;&#39;
Total Lines: 37328</code></pre>
</div>
</div></td>
</tr>
<tr class="even">
<td>-s</td>
<td>--syntax-highlight and --syntax-highlight</td>
<td><p>显示有语法高亮色彩的源代码。</p>
<p>该参数使用内建机制来解析文件并为其生成一个 <em>HTML</em> 高亮版本并将结果写到标准输出。请注意该过程所做的只是生成了一个 <em>&lt;code&gt; [...] &lt;/code&gt;</em> 的 <em>HTML</em> 标记的块，并不包含任何的 <em>HTML</em> 头。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>该选项不能和 <strong>-r</strong> 参数同时使用。</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>-v</td>
<td>--version</td>
<td><p>将 PHP，PHP SAPI 和 Zend 的版本信息写入标准输出。例如：</p>
<div class="example-contents screen">
<div class="cdata">
<pre><code>$ php -v
PHP 4.3.0 (cli), Copyright (c) 1997-2002 The PHP Group
Zend Engine v1.3.0, Copyright (c) 1998-2002 Zend Technologies</code></pre>
</div>
</div></td>
</tr>
<tr class="even">
<td>-w</td>
<td>--strip</td>
<td><p>显示除去了注释和多余空白的源代码。</p>
<blockquote>
<p><strong>Note</strong>:</p>
<p>该选项不能和 <strong>-r</strong> 参数同时使用。</p>
</blockquote></td>
</tr>
<tr class="odd">
<td>-z</td>
<td>--zend-extension</td>
<td><p>加载 Zend 扩展库。如果仅给定一个文件名，PHP 将试图从当前系统扩展库的默认路径（在 Linux 系统下，该路径通常由 <var class="filename">/etc/ld.so.conf</var> 指定）加载该扩展库。如果用一个绝对路径指定文件名，则不会使用系统的扩展库默认路径。如果用相对路径指定的文件名，则 PHP 仅试图在当前目录的相对目录加载扩展库。</p></td>
</tr>
</tbody>
</table>

PHP 的命令行模式能使得 PHP 脚本能完全独立于 web 服务器单独运行。如果使用
Unix 系统，需要在 PHP
脚本的最前面加上一行特殊的代码，使得它能够被执行，这样系统就能知道用哪个程序去运行该脚本。在
Windows 平台下可以将 `php.exe` 和 *.php*
文件的双击属性相关联，也可以编写一个批处理文件来用 PHP 执行脚本。为 Unix
系统增加的第一行代码不会影响该脚本在 Windows
下的运行，因此也可以用该方法编写跨平台的脚本程序。以下是一个简单的 PHP
命令行程序的范例。

**示例 \#1 试图以命令行方式运行的 PHP 脚本（script.php）**

``` php
#!/usr/bin/php
<?php

if ($argc != 2 || in_array($argv[1], array('--help', '-help', '-h', '-?'))) {
?>

This is a command line PHP script with one option.

  Usage:
  <?php echo $argv[0]; ?> <option>

  <option> can be some word you would like
  to print out. With the --help, -help, -h,
  or -? options, you can get this help.

<?php
} else {
    echo $argv[1];
}
?>
```

在以上脚本中，用第一行特殊的代码来指明该文件应该由 PHP
来执行。在这里使用 CLI 的版本，因此不会有 HTTP 头信息输出。在用 PHP
编写命令行应用程序时，可以使用两个参数：`$argc` 和
`$argv`。前面一个的值是比参数个数大 1
的整数（运行的脚本本身的名称也被当作一个参数）。第二个是包含有参数的数组，其第一个元素为脚本的名称，下标为数字
0（`$argv[0]`）。

以上程序中检查了参数的个数是大于 1 个还是小于 1 个。此外如果参数是
**--help**，**-help**，**-h** 或 **-?**
时，打印出帮助信息，并同时动态输出脚本的名称。如果还收到了其它参数，将其显示出来。

如果希望在 Unix 下运行以上脚本，需要使其属性为可执行文件，然后简单的运行
**script.php echothis** 或 **script.php -h**。在 Windows
下，可以为此编写一个批处理文件：

**示例 \#2 运行 PHP 命令行脚本的批处理文件（script.bat）**

``` shell
@C:\php\php.exe script.php %1 %2 %3 %
```

假设将上述程序命名为 `script.php`，且 CLI 版的 `php.exe` 文件放置在
`c:\php\cli\php.exe`，该批处理文件会帮助将附加的参数传给脚本程序：**script.bat
echothis** 或 **script.bat -h**。

请参阅 <a href="/ref/readline.html" class="link">Readline</a>
扩展模块的有关文档，以获取更多的函数的信息。这些函数可以帮助完善 PHP
命令行应用程序。

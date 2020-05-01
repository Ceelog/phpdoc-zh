从 HTML 中分离
--------------

凡是在一对开始和结束标记之外的内容都会被 PHP 解析器忽略，这使得 PHP
文件可以具备混合内容。 可以使 PHP 嵌入到 HTML 文档中去，如下例所示。

``` php
<p>This is going to be ignored by PHP and displayed by the browser.</p>
<?php echo 'While this is going to be parsed.'; ?>
<p>This will also be ignored by PHP and displayed by the browser.</p>
```

这将如预期中的运行，因为当 PHP 解释器碰到 ?\>
结束标记时就简单地将其后内容原样输出（除非马上紧接换行 -
见<a href="/language/basic-syntax/instruction-separation.html" class="link">指令分隔符</a>）直到碰到下一个开始标记；例外是处于条件语句中间时，此时
PHP 解释器会根据条件判断来决定哪些输出，哪些跳过。见下例。

使用条件结构：

**示例 \#1 使用条件的高级分离术**

``` php
<?php if ($expression == true): ?>
  This will show if the expression is true.
<?php else: ?>
  Otherwise this will show.
<?php endif; ?>
```

上例中 PHP 将跳过条件语句未达成的段落，即使该段落位于 PHP
开始和结束标记之外。由于 PHP
解释器会在条件未达成时直接跳过该段条件语句块，因此 PHP
会根据条件来忽略之。

要输出大段文本时，跳出 PHP 解析模式通常比将文本通过 <span
class="function">echo</span> 或 <span class="function">print</span>
输出更有效率。

可以在 PHP 中使用四对不同的开始和结束标记。其中两种，\<?php ?\> 和
\<script language="php"\> \</script\> 总是可用的。另两种是短标记和 <span
class="productname">ASP</span> 风格标记，可以在 `php.ini`
配置文件中打开或关闭。尽管有些人觉得短标记和 <span
class="productname">ASP</span>
风格标记很方便，但移植性较差，通常不推荐使用。

> **Note**:
>
> 此外注意如果将 PHP 嵌入到 XML 或 XHTML 中则需要使用 \<?php ?\>
> 标记以保持符合标准。

**示例 \#2 PHP 开始和结束标记**

``` php
1.  <?php echo 'if you want to serve XHTML or XML documents, do it like this'; ?>

2.  <script language="php">
        echo 'some editors (like FrontPage) don\'t
              like processing instructions';
    </script>

3.  <? echo 'this is the simplest, an SGML processing instruction'; ?>
    <?= expression ?> This is a shortcut for "<? echo expression ?>"

4.  <% echo 'You may optionally use ASP-style tags'; %>
    <%= $variable; # This is a shortcut for "<% echo . . ." %>
```

上例中的 1 和 2 中使用的标记总是可用的，其中示例 1
中是最常用，并建议使用的。

短标记（上例 3）仅在通过 `php.ini` 配置文件中的指令
<a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tag</a>
打开后才可用，或者在 PHP 编译时加入了 **--enable-short-tags** 选项。

<span class="productname">ASP</span> 风格标记（上例 4）仅在通过
`php.ini` 配置文件中的指令
<a href="/ini/core.html#ini.asp-tags" class="link">asp_tags</a>
打开后才可用。

> **Note**:
>
> 在以下情况应避免使用短标记：开发需要再次发布的程序或者库，或者在用户不能控制的服务器上开发。因为目标服务器可能不支持短标记。为了代码的移植及发行，确保不要使用短标记。

> **Note**:
>
> 在 PHP 5.2
> 和之前的版本中，解释器不允许一个文件的全部内容就是一个开始标记
> *\<?php*。自 PHP 5.3
> 起则允许此种文件，但要开始标记后有一个或更多白空格符。

> **Note**:
>
> 自 PHP 5.4 起，短格式的 echo 标记 *\<?=* 总会被识别并且合法，而不管
> <a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tag</a>
> 的设置是什么。

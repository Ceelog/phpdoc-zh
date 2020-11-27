其他变更
--------

### SAPI 模块的变更

#### Apache2Handler

PHP 模块从 *php7\_module* 重命名为 *php\_module*。

### Function 的变更

#### Reflection

可通过新参数 `filter` 来过滤 <span
class="methodname">ReflectionClass::getConstants</span> 和 <span
class="methodname">ReflectionClass::getReflectionConstants</span>
的返回结果。 新增三个常量，搭配使用：

-   **`ReflectionClassConstant::IS_PUBLIC`**
-   **`ReflectionClassConstant::IS_PROTECTED`**
-   **`ReflectionClassConstant::IS_PRIVATE`**

#### Zip

-   <span class="methodname">ZipArchive::addGlob</span> 和 <span
    class="methodname">ZipArchive::addPattern</span> 方法中 `options`
    数组参数可接受更多的值：

    -   *flags*
    -   *comp\_method*
    -   *comp\_flags*
    -   *env\_method*
    -   *enc\_password*

-   <span class="methodname">ZipArchive::addEmptyDir</span>、 <span
    class="methodname">ZipArchive::addFile</span>、 <span
    class="methodname">ZipArchive::addFromString</span> 方法新增 `flags`
    参数。 可用于名称编码 (**`ZipArchive::FL_ENC_*`**)
    与条目（entry）替换 (**`ZipArchive::FL_OVERWRITE`**)。

-   <span class="methodname">ZipArchive::extractTo</span>
    现在会储存文件的修改时间。

### 其他扩展变更

#### CURL

-   现在 CURL 扩展要求 libcurl 版本至少为 7.29.0。

-   移除了 <span class="function">curl\_version</span> 废弃的参数
    `version`。

#### 日期/时间

现在 <span class="classname">DatePeriod</span> 实现（implements）了
<span class="interfacename">IteratorAggregate</span> (之前是 <span
class="interfacename">Traversable</span>)。

#### DOM

现在 <span class="classname">DOMNamedNodeMap</span> 与 <span
class="classname">DOMNodeList</span> 实现（implements）了 <span
class="interfacename">IteratorAggregate</span> (之前是 <span
class="interfacename">Traversable</span>)。

#### 国际化

现在 <span class="classname">IntlBreakIterator</span> 与 <span
class="classname">ResourceBundle</span> 实现（implements）了 <span
class="interfacename">IteratorAggregate</span> (之前是 <span
class="interfacename">Traversable</span>)。

#### Enchant

现在环境允许时，enchant 会默认使用 libenchant-2。 仍然支持 libenchant
1，但已经废弃，并将在未来移除。

#### GD

-   <span class="function">imagepolygon</span>、 <span
    class="function">imageopenpolygon</span>、<span
    class="function">imagefilledpolygon</span> 的参数 `num_points`
    现在为可选参数。 这些函数可用三或四个参数去调用。 省略参数时，会按
    `count($points)/2` 计算。

-   新增函数 <span
    class="function">imagegetinterpolation</span>，可获取当前的插值（interpolation）。

#### JSON

现在无法禁用 JSON 扩展，将是任意 PHP 版本的内置功能，类似 date 扩展。

#### MBString

更新 Unicode 数据表版本到 13.0.0。

#### PDO

现在 <span class="classname">PDOStatement</span> 实现（implements）了
<span class="interfacename">IteratorAggregate</span> (之前是 <span
class="interfacename">Traversable</span>)。

#### LibXML

现在要求 libxml 最小版本为 2.9.0。
这代表着确保了默认情况下禁用了外部实体加载（external entity
loading）的功能。 无需额外步骤即可防范 XML 外部实体注入攻击（XXE
attacks）。

#### MySQLi / PDO MySQL

-   未使用 mysqlnd 时（也是默认且推荐的做法）， 支持的最小
    libmysqlclient 版本为 5.5。

-   现在 <span class="classname">mysqli\_result</span>
    实现（implements）了 <span
    class="interfacename">IteratorAggregate</span> (之前是 <span
    class="interfacename">Traversable</span>)。

#### PGSQL / PDO PGSQL

PGSQL 与 PDO PGSQL 扩展需要 libpq 的版本号至少为 9.1。

#### Readline

在交互提示开始之前调用 <span
class="function">readline\_completion\_function</span> （例如在
<a href="/ini/core.html#ini.auto-prepend-file" class="link">auto_prepend_file</a>
中）， 将重写默认的交互输入补全函数。 之前，只有交互提示（interactive
prompt）开始后， <span
class="function">readline\_completion\_function</span> 才会运行。

#### SimpleXML

现在 <span class="classname">SimpleXMLElement</span>
实现（implements）了 <span
class="interfacename">RecursiveIterator</span> 并吸收了 <span
class="classname">SimpleXMLIterator</span> 的功能。 <span
class="classname">SimpleXMLIterator</span> 是 <span
class="classname">SimpleXMLElement</span> 的一个空扩展。

### INI 文件处理的变更

-   com.dotnet\_version 是一个新的 INI 指令，用于选择 <span
    class="classname">dotnet</span> 对象的 .NET framework 版本。

-   zend.exception\_string\_param\_max\_len 是一个新的 INI
    指令，用于设置字符串化的调用栈（stack strace）的最大字符串长度。

### EBCDIC

不再支持 EBCDIC targets，虽然它不太可能还在当初的地方继续运行。

### 性能

-   opcache 扩展新增了即时编译(JIT) 支持。

-   <span class="function">array\_slice</span> 用于没有空隙的数组时，
    将不会扫描整个数组去查找开始的位移（offset）。 在 offset
    较大、长度较小时，会显著减少函数的运行时间。

-   当本地化 **`LC_CTYPE`** 为 *"C"* 时（也是默认值）， <span
    class="function">strtolower</span> 会使用 SIMD 的实现。

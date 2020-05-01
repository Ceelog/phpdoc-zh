范例
====

**示例 \#1 Xhprof 范例，可选使用图形界面**

本示例启动并结束性能分析器，然后使用捆绑的用户界面来保存和解析结果。
换言之，扩展的代码在调用 <span class="function">xhprof\_disable</span>
函数后结束。

``` php
<?php
xhprof_enable(XHPROF_FLAGS_CPU + XHPROF_FLAGS_MEMORY);

for ($i = 0; $i <= 1000; $i++) {
    $a = $i * $i;
}

$xhprof_data = xhprof_disable();

$XHPROF_ROOT = "/tools/xhprof/";
include_once $XHPROF_ROOT . "/xhprof_lib/utils/xhprof_lib.php";
include_once $XHPROF_ROOT . "/xhprof_lib/utils/xhprof_runs.php";

$xhprof_runs = new XHProfRuns_Default();
$run_id = $xhprof_runs->save_run($xhprof_data, "xhprof_testing");

echo "http://localhost/xhprof/xhprof_html/index.php?run={$run_id}&source=xhprof_testing\n";

?>
```

以上例程的输出类似于：

    http://localhost/xhprof/xhprof_html/index.php?run=t11_4bdf44d21121f&source=xhprof_testing

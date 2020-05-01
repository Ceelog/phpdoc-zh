范例
====

PHP/YAZ keeps track of connections with targets (Z-Associations). A
resource represents a connection to a target.

The script below demonstrates the parallel searching feature of the API.
When invoked with no arguments it prints a query form; else (arguments
are supplied) it searches the targets as given in array *host*.

**示例 \#1 Parallel searching using Yaz**

``` php
<?php
$host=$_REQUEST[host];
$query=$_REQUEST[query];
$num_hosts = count($host);
if (empty($query) || count($host) == 0) {
    echo '<form method="get">
    <input type="checkbox"
    name="host[]" value="bagel.indexdata.dk/gils" />
        GILS test
    <input type="checkbox"
    name="host[]" value="localhost:9999/Default" />
        local test
    <input type="checkbox" checked="checked"
    name="host[]" value="z3950.loc.gov:7090/voyager" />
        Library of Congress
    <br />
    RPN Query:
    <input type="text" size="30" name="query" />
    <input type="submit" name="action" value="Search" />
    </form>
    ';        
} else {
    echo 'You searched for ' . htmlspecialchars($query) . '<br />';
    for ($i = 0; $i < $num_hosts; $i++) {
        $id[] = yaz_connect($host[$i]);
        yaz_syntax($id[$i], "usmarc");
        yaz_range($id[$i], 1, 10);
        yaz_search($id[$i], "rpn", $query);
    }
    yaz_wait();
    for ($i = 0; $i < $num_hosts; $i++) {
        echo '<hr />' . $host[$i] . ':';
        $error = yaz_error($id[$i]);
        if (!empty($error)) {
            echo "Error: $error";
        } else {
            $hits = yaz_hits($id[$i]);
            echo "Result Count $hits";
        }
        echo '<dl>';
        for ($p = 1; $p <= 10; $p++) {
            $rec = yaz_record($id[$i], $p, "string");
            if (empty($rec)) continue;
            echo "<dt><b>$p</b></dt><dd>";
            echo nl2br($rec);
            echo "</dd>";
        }
        echo '</dl>';
    }
}
?>
```

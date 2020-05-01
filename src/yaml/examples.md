范例
====

**示例 \#1 Yaml 范例**

``` php
<?php
$addr = array(
    "given" => "Chris",
    "family"=> "Dumars",
    "address"=> array(
        "lines"=> "458 Walkman Dr.
        Suite #292",
        "city"=> "Royal Oak",
        "state"=> "MI",
        "postal"=> 48046,
      ),
  );
$invoice = array (
    "invoice"=> 34843,
    "date"=> "2001-01-23",
    "bill-to"=> $addr,
    "ship-to"=> $addr,
    "product"=> array(
        array(
            "sku"=> "BL394D",
            "quantity"=> 4,
            "description"=> "Basketball",
            "price"=> 450,
          ),
        array(
            "sku"=> "BL4438H",
            "quantity"=> 1,
            "description"=> "Super Hoop",
            "price"=> 2392,
          ),
      ),
    "tax"=> 251.42,
    "total"=> 4443.52,
    "comments"=> "Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.",
    );

// 把该 invoice 转换生成 YAML 的表示法
$yaml = yaml_emit($invoice);
var_dump($yaml);

// 把 YAML 转换成 PHP 变量
$parsed = yaml_parse($yaml);

// 来回转换，以检查两个结构是否相等效
var_dump($parsed == $invoice);
?>
```

以上例程的输出类似于：

    string(631) "---
    invoice: 34843
    date: "2001-01-23"
    bill-to:
      given: Chris
      family: Dumars
      address:
        lines: |-
          458 Walkman Dr.
                  Suite #292
        city: Royal Oak
        state: MI
        postal: 48046
    ship-to:
      given: Chris
      family: Dumars
      address:
        lines: |-
          458 Walkman Dr.
                  Suite #292
        city: Royal Oak
        state: MI
        postal: 48046
    product:
    - sku: BL394D
      quantity: 4
      description: Basketball
      price: 450
    - sku: BL4438H
      quantity: 1
      description: Super Hoop
      price: 2392
    tax: 251.420000
    total: 4443.520000
    comments: Late afternoon is best. Backup contact is Nancy Billsmer @ 338-4338.
    ...
    "
    bool(true)

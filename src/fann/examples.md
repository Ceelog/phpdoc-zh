范例
====

**目录**

-   [XOR (异或)训练](/fann/examples.html#XOR%20(异或)训练)

XOR (异或)训练
--------------

以下例子展示了怎么训练数据来实现 XOR (异或)功能。

**示例 \#1 xor.data file**

``` txt
4 2 1
-1 -1
-1
-1 1
1
1 -1
1
1 1
-1
```

**示例 \#2 一般训练**

``` php
<?php
$num_input = 2;
$num_output = 1;
$num_layers = 3;
$num_neurons_hidden = 3;
$desired_error = 0.001;
$max_epochs = 500000;
$epochs_between_reports = 1000;

$ann = fann_create_standard($num_layers, $num_input, $num_neurons_hidden, $num_output);

if ($ann) {
    fann_set_activation_function_hidden($ann, FANN_SIGMOID_SYMMETRIC);
    fann_set_activation_function_output($ann, FANN_SIGMOID_SYMMETRIC);

    $filename = dirname(__FILE__) . "/xor.data";
    if (fann_train_on_file($ann, $filename, $max_epochs, $epochs_between_reports, $desired_error))
        fann_save($ann, dirname(__FILE__) . "/xor_float.net");

    fann_destroy($ann);
}
?>
```

这个例子展示怎么读取神经网络并且使用 XOR (异或)功能来运行数据。

**示例 \#3 一般测试**

``` php
<?php
$train_file = (dirname(__FILE__) . "/xor_float.net");
if (!is_file($train_file))
    die("The file xor_float.net has not been created! Please run simple_train.php to generate it");

$ann = fann_create_from_file($train_file);
if (!$ann)
    die("ANN could not be created");

$input = array(-1, 1);
$calc_out = fann_run($ann, $input);
printf("xor test (%f,%f) -> %f\n", $input[0], $input[1], $calc_out[0]);
fann_destroy($ann);
?>
```

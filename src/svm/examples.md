范例
====

The basic process is to define parameters, supply training data to
generate a model on, then make predictions based on the model. There are
a default set of parameters that should get some results with most any
input, so we'll start by looking at the data.

Data is supplied in either a file, a stream, or as an array. If supplied
in a file or a stream, it must contain one line per training example,
which must be formatted as an integer class (usually 1 and -1) followed
by a series of feature/value pairs, in increasing feature order. The
features are integers, the values floats, usually scaled 0-1. For
example:

-1 1:0.43 3:0.12 9284:0.2

In a document classification problem, say a spam checker, each line
would represent a document. There would be two classes, -1 for spam, 1
for ham. Each feature would represent some word, and the value would
represent that importance of that word to the document (perhaps the
frequency count, with the total scaled to unit length). Features that
were 0 (e.g. the word did not appear in the document at all) would
simply not be included.

In array mode, the data must be passed as an array of arrays. Each
sub-array must have the class as the first element, then key =\> value
sets for the feature values pairs.

This data is passed to the SVM class's train function, which will return
an SVM model is successful.

Once a model has been generated, it can be used to make predictions
about previously unseen data. This can be passed as an array to the
model's predict function, in the same format as before, but without the
label. The response will be the class.

Models can be saved and restored as required, using the save and load
functions, which both take a file location.

**示例 \#1 Train from array**

``` php
<?php
$data = array(
    array(-1, 1 => 0.43, 3 => 0.12, 9284 => 0.2),
    array(1, 1 => 0.22, 5 => 0.01, 94 => 0.11),
);

$svm = new SVM();
$model = $svm->train($data);

$data = array(1 => 0.43, 3 => 0.12, 9284 => 0.2);
$result = $model->predict($data);
var_dump($result);
$model->save('model.svm');
?>
```

以上例程的输出类似于：

    int(-1)

**示例 \#2 Train from a file**

``` php
<?php
$svm = new SVM();
$model = $svm->train("traindata.txt");
?>
```

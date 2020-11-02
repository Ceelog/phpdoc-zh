支持向量机
==========

**目录**

-   [简介](/intro/svm.html)
-   [安装／配置](/svm/setup.html)
    -   [需求](/svm/setup.html#需求)
    -   [安装](/svm/setup.html#安装)
    -   [运行时配置](/svm/setup.html#运行时配置)
    -   [资源类型](/svm/setup.html#资源类型)
-   [范例](/svm/examples.html)
-   [SVM](/class/svm.html) — The SVM class
    -   [SVM::\_\_construct](/class/svm.html#SVM::__construct) —
        Construct a new SVM object
    -   [SVM::crossvalidate](/class/svm.html#SVM::crossvalidate) — Test
        training params on subsets of the training data
    -   [SVM::getOptions](/class/svm.html#SVM::getOptions) — Return the
        current training parameters
    -   [SVM::setOptions](/class/svm.html#SVM::setOptions) — Set
        training parameters
    -   [SVM::train](/class/svm.html#SVM::train) — Create a SVMModel
        based on training data
-   [SVMModel](/class/svmmodel.html) — The SVMModel class
    -   [SVMModel::checkProbabilityModel](/class/svmmodel.html#SVMModel::checkProbabilityModel)
        — Returns true if the model has probability information
    -   [SVMModel::\_\_construct](/class/svmmodel.html#SVMModel::__construct)
        — Construct a new SVMModel
    -   [SVMModel::getLabels](/class/svmmodel.html#SVMModel::getLabels)
        — Get the labels the model was trained on
    -   [SVMModel::getNrClass](/class/svmmodel.html#SVMModel::getNrClass)
        — Returns the number of classes the model was trained with
    -   [SVMModel::getSvmType](/class/svmmodel.html#SVMModel::getSvmType)
        — Get the SVM type the model was trained with
    -   [SVMModel::getSvrProbability](/class/svmmodel.html#SVMModel::getSvrProbability)
        — Get the sigma value for regression types
    -   [SVMModel::load](/class/svmmodel.html#SVMModel::load) — Load a
        saved SVM Model
    -   [SVMModel::predict\_probability](/class/svmmodel.html#SVMModel::predict_probability)
        — Return class probabilities for previous unseen data
    -   [SVMModel::predict](/class/svmmodel.html#SVMModel::predict) —
        Predict a value for previously unseen data
    -   [SVMModel::save](/class/svmmodel.html#SVMModel::save) — Save a
        model to a file

简介
----

类摘要
------

**SVM**

<span class="ooclass"> class **SVM** </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`SVM::C_SVC` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::NU_SVC` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::ONE_CLASS` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::EPSILON_SVR` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::NU_SVR` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::KERNEL_LINEAR` <span class="initializer"> = 0</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::KERNEL_POLY` <span class="initializer"> = 1</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::KERNEL_RBF` <span class="initializer"> = 2</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::KERNEL_SIGMOID` <span class="initializer"> = 3</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::KERNEL_PRECOMPUTED` <span class="initializer"> = 4</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_TYPE` <span class="initializer"> = 101</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_KERNEL_TYPE` <span class="initializer"> = 102</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_DEGREE` <span class="initializer"> = 103</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_SHRINKING` <span class="initializer"> = 104</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_PROPABILITY` <span class="initializer"> = 105</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_GAMMA` <span class="initializer"> = 201</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_NU` <span class="initializer"> = 202</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_EPS` <span class="initializer"> = 203</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_P` <span class="initializer"> = 204</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_COEF_ZERO` <span class="initializer"> = 205</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_C` <span class="initializer"> = 206</span> ;

<span class="modifier">const</span> <span class="type">int</span>
`SVM::OPT_CACHE_SIZE` <span class="initializer"> = 207</span> ;

/\* Methods \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">svm::crossvalidate</span> ( <span
class="methodparam"><span class="type">array</span> `$problem`</span> ,
<span class="methodparam"><span class="type">int</span>
`$number_of_folds`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getOptions</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">setOptions</span> ( <span
class="methodparam"><span class="type">array</span> `$params`</span> )

<span class="modifier">public</span> <span class="type">SVMModel</span>
<span class="methodname">svm::train</span> ( <span
class="methodparam"><span class="type">array</span> `$problem`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$weights`</span> \] )

}

预定义常量
----------

SVM Constants
-------------

**`SVM::C_SVC`**  
The basic C\_SVC SVM type. The default, and a good starting point

**`SVM::NU_SVC`**  
The NU\_SVC type uses a different, more flexible, error weighting

**`SVM::ONE_CLASS`**  
One class SVM type. Train just on a single class, using outliers as
negative examples

**`SVM::EPSILON_SVR`**  
A SVM type for regression (predicting a value rather than just a class)

**`SVM::NU_SVR`**  
A NU style SVM regression type

**`SVM::KERNEL_LINEAR`**  
A very simple kernel, can work well on large document classification
problems

**`SVM::KERNEL_POLY`**  
A polynomial kernel

**`SVM::KERNEL_RBF`**  
The common Gaussian RBD kernel. Handles non-linear problems well and is
a good default for classification

**`SVM::KERNEL_SIGMOID`**  
A kernel based on the sigmoid function. Using this makes the SVM very
similar to a two layer sigmoid based neural network

**`SVM::KERNEL_PRECOMPUTED`**  
A precomputed kernel - currently unsupported.

**`SVM::OPT_TYPE`**  
The options key for the SVM type

**`SVM::OPT_KERNEL_TYPE`**  
The options key for the kernel type

**`SVM::OPT_DEGREE`**  

**`SVM::OPT_SHRINKING`**  
Training parameter, boolean, for whether to use the shrinking heuristics

**`SVM::OPT_PROBABILITY`**  
Training parameter, boolean, for whether to collect and use probability
estimates

**`SVM::OPT_GAMMA`**  
Algorithm parameter for Poly, RBF and Sigmoid kernel types.

**`SVM::OPT_NU`**  
The option key for the nu parameter, only used in the NU\_ SVM types

**`SVM::OPT_EPS`**  
The option key for the Epsilon parameter, used in epsilon regression

**`SVM::OPT_P`**  
Training parameter used by Episilon SVR regression

**`SVM::OPT_COEF_ZERO`**  
Algorithm parameter for poly and sigmoid kernels

**`SVM::OPT_C`**  
The option for the cost parameter that controls tradeoff between errors
and generality - effectively the penalty for misclassifying training
examples.

**`SVM::OPT_CACHE_SIZE`**  
Memory cache size, in MB

SVM::\_\_construct
==================

Construct a new SVM object

### 说明

<span class="modifier">public</span> <span
class="methodname">SVM::\_\_construct</span> ( <span
class="methodparam">void</span> )

Constructs a new SVM object ready to accept training data.

### 参数

此函数没有参数。

### 返回值

Throws SVMException if the libsvm library could not be loaded

SVM::crossvalidate
==================

Test training params on subsets of the training data

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">svm::crossvalidate</span> ( <span
class="methodparam"><span class="type">array</span> `$problem`</span> ,
<span class="methodparam"><span class="type">int</span>
`$number_of_folds`</span> )

Crossvalidate can be used to test the effectiveness of the current
parameter set on a subset of the training data. Given a problem set and
a n "folds", it separates the problem set into n subsets, and the
repeatedly trains on one subset and tests on another. While the accuracy
will generally be lower than a SVM trained on the enter data set, the
accuracy score returned should be relatively useful, so it can be used
to test different training parameters.

### 参数

`problem`  
The problem data. This can either be in the form of an array, the URL of
an SVMLight formatted file, or a stream to an opened SVMLight formatted
datasource.

`number_of_folds`  
The number of sets the data should be divided into and cross tested. A
higher number means smaller training sets and less reliability. 5 is a
good number to start with.

### 返回值

The correct percentage, expressed as a floating point number from 0-1.
In the case of NU\_SVC or EPSILON\_SVR kernels the mean squared error
will returned instead.

### 参见

-   <span class="methodname">SVM::train</span>

SVM::getOptions
===============

Return the current training parameters

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SVM::getOptions</span> ( <span
class="methodparam">void</span> )

Retrieve an array containing the training parameters. The parameters
will be keyed on the predefined SVM constants.

### 参数

此函数没有参数。

### 返回值

Returns an array of configuration settings.

SVM::setOptions
===============

Set training parameters

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SVM::setOptions</span> ( <span
class="methodparam"><span class="type">array</span> `$params`</span> )

Set one or more training parameters.

### 参数

`params`  
An array of training parameters, keyed on the SVM constants.

### 返回值

Return true on success, throws SVMException on error.

SVM::train
==========

Create a SVMModel based on training data

### 说明

<span class="modifier">public</span> <span class="type">SVMModel</span>
<span class="methodname">svm::train</span> ( <span
class="methodparam"><span class="type">array</span> `$problem`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$weights`</span> \] )

Train a support vector machine based on the supplied training data.

### 参数

`problem`  
The problem can be provided in three different ways. An array, where the
data should start with the class label (usually 1 or -1) then followed
by a sparse data set of dimension =\> data pairs. A URL to a file
containing a SVM Light formatted problem, with the each line being a new
training example, the start of each line containing the class (1, -1)
then a series of tab separated data values shows as key:value. A opened
stream pointing to a data source formatted as in the file above.

`weights`  
Weights are an optional set of weighting parameters for the different
classes, to help account for unbalanced training sets. For example, if
the classes were 1 and -1, and -1 had significantly more example than
one, the weight for -1 could be 0.5. Weights should be in the range 0-1.

### 返回值

Returns an SVMModel that can be used to classify previously unseen data.
Throws SVMException on error

简介
----

The SVMModel is the end result of the training process. It can be used
to classify previously unseen data.

类摘要
------

**SVMModel**

<span class="ooclass"> class **SVMModel** </span> {

/\* Methods \*/

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">checkProbabilityModel</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">getLabels</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getNrClass</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">getSvmType</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">getSvrProbability</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">load</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">predict\_probability</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">predict</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">save</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

}

SVMModel::checkProbabilityModel
===============================

Returns true if the model has probability information

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SVMModel::checkProbabilityModel</span> ( <span
class="methodparam">void</span> )

Returns true if the model contains probability information.

### 参数

此函数没有参数。

### 返回值

Return a boolean value

SVMModel::\_\_construct
=======================

Construct a new SVMModel

### 说明

<span class="modifier">public</span> <span
class="methodname">SVMModel::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\] )

Build a new SVMModel. Models will usually be created from the SVM::train
function, but then saved models may be restored directly.

### 参数

`filename`  
The filename for the saved model file this model should load.

### 返回值

Throws SVMException on error

### 参见

-   <span class="methodname">SVMModel::load</span>

SVMModel::getLabels
===================

Get the labels the model was trained on

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">SVMModel::getLabels</span> ( <span
class="methodparam">void</span> )

Return an array of labels that the model was trained on. For regression
and one class models an empty array is returned.

### 参数

此函数没有参数。

### 返回值

Return an array of labels

### 参见

-   <span class="methodname">SVMModel::getNrClass</span>

SVMModel::getNrClass
====================

Returns the number of classes the model was trained with

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SVMModel::getNrClass</span> ( <span
class="methodparam">void</span> )

Returns the number of classes the model was trained with, will return 2
for one class and regression models.

### 参数

此函数没有参数。

### 返回值

Return an integer number of classes

SVMModel::getSvmType
====================

Get the SVM type the model was trained with

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">SVMModel::getSvmType</span> ( <span
class="methodparam">void</span> )

Returns an integer value representing the type of the SVM model used,
e.g SVM::C\_SVC.

### 参数

此函数没有参数。

### 返回值

Return an integer SVM type

SVMModel::getSvrProbability
===========================

Get the sigma value for regression types

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">SVMModel::getSvrProbability</span> ( <span
class="methodparam">void</span> )

For regression models, returns a sigma value. If there is no probability
information or the model is not SVR, 0 is returned.

### 参数

此函数没有参数。

### 返回值

Returns a sigma value

SVMModel::load
==============

Load a saved SVM Model

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SVMModel::load</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Load a model file ready for classification or regression.

### 参数

`filename`  
The filename of the model.

### 返回值

Throws SVMException on error. Returns true on success.

### 参见

-   <span class="methodname">SVMModel::save</span>

SVMModel::predict\_probability
==============================

Return class probabilities for previous unseen data

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">SVMModel::predict\_probability</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> )

This function accepts an array of data and attempts to predict the
class, as with the predict function. Additionally, however, this
function returns an array of probabilities, one per class in the model,
which represent the estimated chance of the data supplied being a member
of that class. Requires that the model to be used has been trained with
the probability parameter set to true.

### 参数

`data`  
The array to be classified. This should be a series of key =\> value
pairs in increasing key order, but not necessarily continuous.

`probabilities`  
The supplied value will be filled with the probabilities. This will be
either null, in the case of a model without probability information, or
an array where the index is the class name and the value the predicted
probability.

### 返回值

Float the predicted value. This will be a class label in the case of
classification, a real value in the case of regression. Throws
SVMException on error

### 参见

-   <span class="methodname">SVM::predict</span>

SVMModel::predict
=================

Predict a value for previously unseen data

### 说明

<span class="modifier">public</span> <span class="type">float</span>
<span class="methodname">SVMModel::predict</span> ( <span
class="methodparam"><span class="type">array</span> `$data`</span> )

This function accepts an array of data and attempts to predict the class
or regression value based on the model extracted from previously trained
data.

### 参数

`data`  
The array to be classified. This should be a series of key =\> value
pairs in increasing key order, but not necessarily continuous.

### 返回值

Float the predicted value. This will be a class label in the case of
classification, a real value in the case of regression. Throws
SVMException on error

### 参见

-   <span class="methodname">SVM::train</span>

SVMModel::save
==============

Save a model to a file

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">SVMModel::save</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

Save the model data to a file, for later use.

### 参数

`filename`  
The file to save the model to.

### 返回值

Throws SVMException on error. Returns true on success.

### 参见

-   <span class="methodname">SVMModel::load</span>

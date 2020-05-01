Lapack
======

**目录**

-   [简介](/intro/lapack.html)
-   [安装／配置](/lapack/setup.html)
    -   [需求](/lapack/setup.html#需求)
    -   [安装](/lapack/setup.html#安装)
    -   [运行时配置](/lapack/setup.html#运行时配置)
    -   [资源类型](/lapack/setup.html#资源类型)
-   [预定义常量](/lapack/constants.html)
-   [Lapack](/class/lapack.html) — The Lapack class
    -   [Lapack::eigenValues](/class/lapack.html#Lapack::eigenValues) —
        This function returns the eigenvalues for a given square matrix
    -   [Lapack::identity](/class/lapack.html#Lapack::identity) — Return
        an identity matrix
    -   [Lapack::leastSquaresByFactorisation](/class/lapack.html#Lapack::leastSquaresByFactorisation)
        — Calculate the linear least squares solution of a matrix using
        QR factorisation
    -   [Lapack::leastSquaresBySVD](/class/lapack.html#Lapack::leastSquaresBySVD)
        — Solve the linear least squares problem, using SVD
    -   [Lapack::pseudoInverse](/class/lapack.html#Lapack::pseudoInverse)
        — Calculate the inverse of a matrix
    -   [Lapack::singularValues](/class/lapack.html#Lapack::singularValues)
        — Calculated the singular values of a matrix
    -   [Lapack::solveLinearEquation](/class/lapack.html#Lapack::solveLinearEquation)
        — Solve a system of linear equations
-   [LapackException](/class/lapackexception.html) — The LapackException
    class

简介
----

LAPACK is written in Fortran 90 and provides routines for solving
systems of simultaneous linear equations, least-squares solutions of
linear systems of equations, eigenvalue problems, and singular value
problems. This extension wraps the LAPACKE C bindings to allow access to
several processes exposed by the library. Most functions work with
arrays of arrays, representing rectangular matrices in row major order -
so a two by two matrix \[1 2; 3 4\] would be array(array(1, 2), array(3,
4)).

All of the functions are called statically, for example $eig =
Lapack::eigenvalues($a);

类摘要
------

**Lapack**

<span class="ooclass"> class **Lapack** </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">eigenValues</span> ( <span class="methodparam"><span
class="type">array</span> `$a`</span> \[, <span
class="methodparam"><span class="type">array</span> `$left`</span> \[,
<span class="methodparam"><span class="type">array</span>
`$right`</span> \]\] )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">identity</span> ( <span class="methodparam"><span
class="type">int</span> `$n`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">leastSquaresByFactorisation</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> , <span
class="methodparam"><span class="type">array</span> `$b`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">leastSquaresBySVD</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> , <span
class="methodparam"><span class="type">array</span> `$b`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">pseudoInverse</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">singularValues</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> )

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">solveLinearEquation</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> , <span
class="methodparam"><span class="type">array</span> `$b`</span> )

}

Lapack::eigenValues
===================

This function returns the eigenvalues for a given square matrix

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Lapack::eigenValues</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> \[,
<span class="methodparam"><span class="type">array</span> `$left`</span>
\[, <span class="methodparam"><span class="type">array</span>
`$right`</span> \]\] )

Calculate the eigenvalues for a square matrix, and optionally calculate
the left and right eigenvectors.

### 参数

`a`  
The matrix to calculate the eigenvalues for.

`left`  
Optional parameter - if an array is passed here, it will be filled with
the left eigenvectors

`right`  
Optional parameter - if an array is passed here, it will be filled with
the right eigenvectors

### 返回值

Returns an array of arrays representing the eigenvalues for the array.

### 范例

**示例 \#1 Using <span class="function">Lapack::eigenValues</span>:**

``` php
<?php

 $a = array(
     array(-1.01,   0.86,  -4.60,  3.31,  -4.81  ),
     array( 3.98,   0.53,  -7.04,  5.29,   3.55  ),
     array( 3.30,   8.26,  -3.89,  8.20,  -1.51  ),
     array( 4.43,   4.96,  -7.66, -7.33,   6.18  ),
     array( 7.31,  -6.43,  -6.16,  2.47,   5.58  ),
 );

 $result = Lapack::eigenValues($a);

 ?>
```

Lapack::identity
================

Return an identity matrix

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Lapack::identity</span> ( <span
class="methodparam"><span class="type">int</span> `$n`</span> )

Return a size n identity matrix

### 参数

`n`  
The height and width of the identity matrix.

### 返回值

Will return a an array of n arrays, each containing n entries. The
diagonals of the matrix will be 1s, the other positions 0.

Lapack::leastSquaresByFactorisation
===================================

Calculate the linear least squares solution of a matrix using QR
factorisation

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Lapack::leastSquaresByFactorisation</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> , <span
class="methodparam"><span class="type">array</span> `$b`</span> )

Solve the linear least squares problem, find min x in \|\| B - Ax \|\|
Returns an array representing x. Expects arrays of arrays, and will
return an array of arrays in the dimension B num cols x A num cols. Uses
QR or LQ factorisation on matrix A.

### 参数

`a`  
Matrix A

`b`  
Matrix B

### 返回值

Array of the solution matrix

### 范例

**示例 \#1 Using <span
class="function">Lapack::leastSquaresByFactorisation</span>:**

``` php
<?php

 $a = array(
     array( 1.44,  -7.84,  -4.39,   4.53),
     array(-9.96,  -0.28,  -3.24,   3.83),
     array(-7.55,   3.24,   6.27,  -6.64),
     array( 8.34,   8.09,   5.28,   2.06),
     array( 7.08,   2.52,   0.74,  -2.47),
     array(-5.45,  -5.70,  -1.19,   4.70),
 );

 $b = array(
     array( 8.58,   9.35),
     array( 8.26,  -4.43),
     array( 8.48,  -0.70),
     array(-5.28,  -0.26),
     array( 5.72,  -7.36),
     array( 8.93,  -2.52),           
 );

 $result = Lapack::leastSquaresByFactorisation($a, $b);
 ?>
```

Lapack::leastSquaresBySVD
=========================

Solve the linear least squares problem, using SVD

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Lapack::leastSquaresBySVD</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> , <span
class="methodparam"><span class="type">array</span> `$b`</span> )

Solve the linear least squares problem, find min x in \|\| B - Ax \|\|
Returns an array representing x. Expects arrays of arrays, and will
return an array of arrays in the dimension B num cols x A num cols. Uses
SVD with a divide and conquer algorithm.

### 参数

`a`  
Matrix A

`b`  
Matrix B

### 返回值

Returns the solution as an array of arrays.

### 范例

**示例 \#1 Using <span
class="function">Lapack::leastSquaresBySVD</span>:**

``` php
<?php

  $a = array(
      array( 1.44,  -7.84,  -4.39,   4.53),
      array(-9.96,  -0.28,  -3.24,   3.83),
      array(-7.55,   3.24,   6.27,  -6.64),
      array( 8.34,   8.09,   5.28,   2.06),
      array( 7.08,   2.52,   0.74,  -2.47),
      array(-5.45,  -5.70,  -1.19,   4.70),
  );

  $b = array(
      array( 8.58,   9.35),
      array( 8.26,  -4.43),
      array( 8.48,  -0.70),
      array(-5.28,  -0.26),
      array( 5.72,  -7.36),
      array( 8.93,  -2.52),           
  );

  $result = Lapack::leastSquaresBySVD($a, $b);
  
  ?>
```

Lapack::pseudoInverse
=====================

Calculate the inverse of a matrix

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Lapack::pseudoInverse</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> )

Find the pseudoinverse of a matrix A.

### 参数

`a`  
Matrix to invert

### 返回值

Inverted matrix (array of arrays).

### 范例

**示例 \#1 Using <span class="function">Lapack::pseudoInverse</span>:**

``` php
<?php

   $a = array(
       array( 8, 1, 6 ),
       array( 3, 5, 7 ),
       array( 4, 9, 2 ),
   );

   $result = Lapack::pseudoInverse($a);

   ?>
```

Lapack::singularValues
======================

Calculated the singular values of a matrix

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Lapack::singularValues</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> )

Calculate the singular values of the matrix A.

### 参数

`a`  
The matrix to calculate the singular values for

### 返回值

The singular values

### 范例

**示例 \#1 Using <span class="function">Lapack::singularValues</span>:**

``` php
<?php

    $a = array(
        array( 7.52,  -1.10,  -7.95,  1.08  ),
        array(-0.76,   0.62,   9.34, -7.10  ),
        array( 5.13,   6.62,  -5.66,  0.87  ),
        array(-4.75,   8.52,   5.75,  5.30  ),
        array( 1.33,   4.91,  -5.49, -3.52  ),
        array(-2.40,  -6.77,   2.34,  3.95  ),
    );


    $result = Lapack::singularValues($a);

    ?>
```

Lapack::solveLinearEquation
===========================

Solve a system of linear equations

### 说明

<span class="modifier">public</span> <span
class="modifier">static</span> <span class="type">array</span> <span
class="methodname">Lapack::solveLinearEquation</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> , <span
class="methodparam"><span class="type">array</span> `$b`</span> )

This function computes the solution to the system of linear equations
with a square matrix A and multiple right-hand sides B. Solves A \* X =
B for multiple B.

### 参数

`a`  
Square matrix of linear equations

`b`  
Right hand side to be solved for

### 返回值

Matrix X

### 范例

**示例 \#1 Using <span class="function">Lapack::singularValues</span>:**

``` php
<?php

    $a = array(
        array( 6.80,  -6.05,  -0.45,   8.32,  -9.67   ),
        array(-2.11,  -3.30,   2.58,   2.71,  -5.14   ),
        array( 5.66,   5.36,  -2.70,   4.35,  -7.26   ),
        array( 5.97,  -4.44,   0.27,  -7.17,   6.08   ),
        array( 8.23,   1.08,   9.04,   2.14,  -6.87   ),
    );

    $b = array(
       array(  4.02,  -1.56,   9.81   ),
       array(  6.19,   4.00,  -4.09   ),
       array( -8.22,  -8.67,  -4.57   ),
       array( -7.57,   1.75,  -8.61   ),
       array( -3.03,   2.86,   8.99   ),
    );

    $result = Lapack::solveLinearEquation($a, $b);

    ?>
```

简介
----

Exception thrown when an error is caught in the LAPACK functions

类摘要
------

**lapackexception**

<span class="ooclass"> class **lapackexception** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

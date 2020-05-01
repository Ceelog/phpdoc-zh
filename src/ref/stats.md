stats\_absolute\_deviation
==========================

Returns the absolute deviation of an array of values

### 说明

<span class="type">float</span> <span
class="methodname">stats\_absolute\_deviation</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> )

Returns the absolute deviation of the values in `a`.

### 参数

`a`  
The input array

### 返回值

Returns the absolute deviation of the values in `a`, or **`FALSE`** if
`a` is empty or is not an array.

stats\_cdf\_beta
================

Calculates any one parameter of the beta distribution given values for
the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_beta</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the beta distribution. The kind of the return value and
parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, alpha, and beta denotes cumulative distribution function, the
value of the random variable, and shape parameters of the beta
distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | alpha  | beta   |
| 2       | x            | CDF    | alpha  | beta   |
| 3       | alpha        | x      | CDF    | beta   |
| 4       | beta         | x      | CDF    | alpha  |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, alpha, or beta, determined by `which`.

stats\_cdf\_binomial
====================

Calculates any one parameter of the binomial distribution given values
for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_binomial</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the binomial distribution. The kind of the return value
and parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, n, and p denotes cumulative distribution function, the number of
successes, the number of trials, and the success rate for each trial,
respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | n      | p      |
| 2       | x            | CDF    | n      | p      |
| 3       | n            | x      | CDF    | p      |
| 4       | p            | x      | CDF    | n      |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, n, or p, determined by `which`.

stats\_cdf\_cauchy
==================

Calculates any one parameter of the Cauchy distribution given values for
the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_cauchy</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the Cauchy distribution. The kind of the return value and
parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, x0, and gamma denotes cumulative distribution function, the
value of the random variable, the location and the scale parameter of
the Cauchy distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | x0     | gamma  |
| 2       | x            | CDF    | x0     | gamma  |
| 3       | x0           | x      | CDF    | gamma  |
| 4       | gamma        | x      | CDF    | x0     |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, x0, or gamma, determined by `which`.

stats\_cdf\_chisquare
=====================

Calculates any one parameter of the chi-square distribution given values
for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_chisquare</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the chi-square distribution. The kind of the return value
and parameters (`par1` and `par2`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, and k denotes cumulative distribution function, the value of the
random variable, and the degree of freedom of the chi-square
distribution, respectively.

| `which` | Return value | `par1` | `par2` |
|---------|--------------|--------|--------|
| 1       | CDF          | x      | k      |
| 2       | x            | CDF    | k      |
| 3       | k            | x      | CDF    |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, or k, determined by `which`.

stats\_cdf\_exponential
=======================

Calculates any one parameter of the exponential distribution given
values for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_exponential</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the exponential distribution. The kind of the return
value and parameters (`par1` and `par2`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, and lambda denotes cumulative distribution function, the value
of the random variable, and the rate parameter of the exponential
distribution, respectively.

| `which` | Return value | `par1` | `par2` |
|---------|--------------|--------|--------|
| 1       | CDF          | x      | lambda |
| 2       | x            | CDF    | lambda |
| 3       | lambda       | x      | CDF    |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, or lambda, determined by `which`.

stats\_cdf\_f
=============

Calculates any one parameter of the F distribution given values for the
others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_f</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the F distribution. The kind of the return value and
parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, d1, and d2 denotes cumulative distribution function, the value
of the random variable, and the degree of freedoms of the F
distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | d1     | d2     |
| 2       | x            | CDF    | d1     | d2     |
| 3       | d1           | x      | CDF    | d2     |
| 4       | d2           | x      | CDF    | d1     |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, d1, or d2, determined by `which`.

stats\_cdf\_gamma
=================

Calculates any one parameter of the gamma distribution given values for
the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_gamma</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the gamma distribution. The kind of the return value and
parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, k, and theta denotes cumulative distribution function, the value
of the random variable, and the shape and the scale parameter of the
gamma distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | k      | theta  |
| 2       | x            | CDF    | k      | theta  |
| 3       | k            | x      | CDF    | theta  |
| 4       | theta        | x      | CDF    | k      |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, k, or theta, determined by `which`.

stats\_cdf\_laplace
===================

Calculates any one parameter of the Laplace distribution given values
for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_laplace</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the Laplace distribution. The kind of the return value
and parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, mu, and b denotes cumulative distribution function, the value of
the random variable, and the location and the scale parameter of the
Laplace distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | mu     | b      |
| 2       | x            | CDF    | mu     | b      |
| 3       | mu           | x      | CDF    | b      |
| 4       | b            | x      | CDF    | mu     |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, mu, or b, determined by `which`.

stats\_cdf\_logistic
====================

Calculates any one parameter of the logistic distribution given values
for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_logistic</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the logistic distribution. The kind of the return value
and parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, mu, and s denotes cumulative distribution function, the value of
the random variable, and the location and the scale parameter of the
logistic distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | mu     | s      |
| 2       | x            | CDF    | mu     | s      |
| 3       | mu           | x      | CDF    | s      |
| 4       | s            | x      | CDF    | mu     |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, mu, or s, determined by `which`.

stats\_cdf\_negative\_binomial
==============================

Calculates any one parameter of the negative binomial distribution given
values for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_negative\_binomial</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the negative binomial distribution. The kind of the
return value and parameters (`par1`, `par2`, and `par3`) are determined
by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, r, and p denotes cumulative distribution function, the number of
failure, the number of success, and the success rate for each trial,
respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | r      | p      |
| 2       | x            | CDF    | r      | p      |
| 3       | r            | x      | CDF    | p      |
| 4       | p            | x      | CDF    | r      |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, r, or p, determined by `which`.

stats\_cdf\_noncentral\_chisquare
=================================

Calculates any one parameter of the non-central chi-square distribution
given values for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_noncentral\_chisquare</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the non-central chi-square distribution. The kind of the
return value and parameters (`par1`, `par2`, and `par3`) are determined
by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, k, and lambda denotes cumulative distribution function, the
value of the random variable, the degree of freedom and the
non-centrality parameter of the distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | k      | lambda |
| 2       | x            | CDF    | k      | lambda |
| 3       | k            | x      | CDF    | lambda |
| 4       | lambda       | x      | CDF    | k      |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, k, or lambda, determined by `which`.

stats\_cdf\_noncentral\_f
=========================

Calculates any one parameter of the non-central F distribution given
values for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_noncentral\_f</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span
class="type">float</span> `$par4`</span> , <span
class="methodparam"><span class="type">int</span> `$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the non-central F distribution. The kind of the return
value and parameters (`par1`, `par2`, `par3`, and `par4`) are determined
by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, nu1, nu2, and lambda denotes cumulative distribution function,
the value of the random variable, the degree of freedoms and the
non-centrality parameter of the distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` | `par4` |
|---------|--------------|--------|--------|--------|--------|
| 1       | CDF          | x      | nu1    | nu2    | lambda |
| 2       | x            | CDF    | nu1    | nu2    | lambda |
| 3       | nu1          | x      | CDF    | nu2    | lambda |
| 4       | nu2          | x      | CDF    | nu1    | lambda |
| 5       | lambda       | x      | CDF    | nu1    | nu2    |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`par4`  
The fourth parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, nu1, nu2, or lambda, determined by `which`.

stats\_cdf\_noncentral\_t
=========================

Calculates any one parameter of the non-central t-distribution give
values for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_noncentral\_t</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the non-central t-distribution. The kind of the return
value and parameters (`par1`, `par2`, and `par3`) are determined by
`which`.

The following table lists the return value and parameters by `which`.
CDF, x, nu, and mu denotes cumulative distribution function, the value
of the random variable, the degrees of freedom and the non-centrality
parameter of the distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | nu     | mu     |
| 2       | x            | CDF    | nu     | mu     |
| 3       | nu           | x      | CDF    | mu     |
| 4       | mu           | x      | CDF    | nu     |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, nu, or mu, determined by `which`.

stats\_cdf\_normal
==================

Calculates any one parameter of the normal distribution given values for
the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_normal</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the normal distribution. The kind of the return value and
parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, mu, and sigma denotes cumulative distribution function, the
value of the random variable, the mean and the standard deviation of the
normal distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | mu     | sigma  |
| 2       | x            | CDF    | mu     | sigma  |
| 3       | mu           | x      | CDF    | sigma  |
| 4       | sigma        | x      | CDF    | mu     |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, mu, or sigma, determined by `which`.

stats\_cdf\_poisson
===================

Calculates any one parameter of the Poisson distribution given values
for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_poisson</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the Poisson distribution. The kind of the return value
and parameters (`par1` and `par2`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, and lambda denotes cumulative distribution function, the value
of the random variable, and the parameter of the Poisson distribution,
respectively.

| `which` | Return value | `par1` | `par2` |
|---------|--------------|--------|--------|
| 1       | CDF          | x      | lambda |
| 2       | x            | CDF    | lambda |
| 3       | lambda       | x      | CDF    |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, or lambda, determined by `which`.

stats\_cdf\_t
=============

Calculates any one parameter of the t-distribution given values for the
others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_t</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the t-distribution. The kind of the return value and
parameters (`par1` and `par2`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, and nu denotes cumulative distribution function, the value of
the random variable, and the degrees of freedom of the t-distribution,
respectively.

| `which` | Return value | `par1` | `par2` |
|---------|--------------|--------|--------|
| 1       | CDF          | x      | nu     |
| 2       | x            | CDF    | nu     |
| 3       | nu           | x      | CDF    |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, or nu, determined by `which`.

stats\_cdf\_uniform
===================

Calculates any one parameter of the uniform distribution given values
for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_uniform</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the uniform distribution. The kind of the return value
and parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, a, and b denotes cumulative distribution function, the value of
the random variable, the lower bound and the higher bound of the uniform
distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | a      | b      |
| 2       | x            | CDF    | a      | b      |
| 3       | a            | x      | CDF    | b      |
| 4       | b            | x      | CDF    | a      |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, a, or b, determined by `which`.

stats\_cdf\_weibull
===================

Calculates any one parameter of the Weibull distribution given values
for the others

### 说明

<span class="type">float</span> <span
class="methodname">stats\_cdf\_weibull</span> ( <span
class="methodparam"><span class="type">float</span> `$par1`</span> ,
<span class="methodparam"><span class="type">float</span> `$par2`</span>
, <span class="methodparam"><span class="type">float</span>
`$par3`</span> , <span class="methodparam"><span class="type">int</span>
`$which`</span> )

Returns the cumulative distribution function, its inverse, or one of its
parameters, of the Weibull distribution. The kind of the return value
and parameters (`par1`, `par2`, and `par3`) are determined by `which`.

The following table lists the return value and parameters by `which`.
CDF, x, k, and lambda denotes cumulative distribution function, the
value of the random variable, the shape and the scale parameter of the
Weibull distribution, respectively.

| `which` | Return value | `par1` | `par2` | `par3` |
|---------|--------------|--------|--------|--------|
| 1       | CDF          | x      | k      | lambda |
| 2       | x            | CDF    | k      | lambda |
| 3       | k            | x      | CDF    | lambda |
| 4       | lambda       | x      | CDF    | k      |

### 参数

`par1`  
The first parameter

`par2`  
The second parameter

`par3`  
The third parameter

`which`  
The flag to determine what to be calculated

### 返回值

Returns CDF, x, k, or lambda, determined by `which`.

stats\_covariance
=================

Computes the covariance of two data sets

### 说明

<span class="type">float</span> <span
class="methodname">stats\_covariance</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> , <span
class="methodparam"><span class="type">array</span> `$b`</span> )

Returns the covariance of `a` and `b`.

### 参数

`a`  
The first array

`b`  
The second array

### 返回值

Returns the covariance of `a` and `b`, or **`FALSE`** on failure.

stats\_dens\_beta
=================

Probability density function of the beta distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_beta</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> )

Returns the probability density at `x`, where the random variable
follows the beta distribution of which the shape parameters are `a` and
`b`.

### 参数

`x`  
The value at which the probability density is calculated

`a`  
The shape parameter of the distribution

`b`  
The shape parameter of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_cauchy
===================

Probability density function of the Cauchy distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_cauchy</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$ave`</span> ,
<span class="methodparam"><span class="type">float</span>
`$stdev`</span> )

Returns the probability density at `x`, where the random variable
follows the Cauchy distribution whose location and scale are `ave` and
`stdev`, respectively.

### 参数

`x`  
The value at which the probability density is calculated

`ave`  
The location parameter of the distribution

`stdev`  
The scale parameter of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_chisquare
======================

Probability density function of the chi-square distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_chisquare</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$dfr`</span> )

Returns the probability density at `x`, where the random variable
follows the chi-square distribution of which the degree of freedom is
`dfr`.

### 参数

`x`  
The value at which the probability density is calculated

`dfr`  
The degree of freedom of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_exponential
========================

Probability density function of the exponential distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_exponential</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$scale`</span> )

Returns the probability density at `x`, where the random variable
follows the exponential distribution of which the scale is `scale`.

### 参数

`x`  
The value at which the probability density is calculated

`scale`  
The scale of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_f
==============

Probability density function of the F distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_f</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$dfr1`</span> ,
<span class="methodparam"><span class="type">float</span> `$dfr2`</span>
)

Returns the probability density at `x`, where the random variable
follows the F distribution of which the degree of freedoms are `dfr1`
and `dfr2`.

### 参数

`x`  
The value at which the probability density is calculated

`dfr1`  
The degree of freedom of the distribution

`dfr2`  
The degree of freedom of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_gamma
==================

Probability density function of the gamma distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_gamma</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$shape`</span> ,
<span class="methodparam"><span class="type">float</span>
`$scale`</span> )

Returns the probability density at `x`, where the random variable
follows the gamma distribution of which the shape parameter is `shape`
and the scale parameter is `scale`.

### 参数

`x`  
The value at which the probability density is calculated

`shape`  
The shape parameter of the distribution

`scale`  
The scale parameter of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_laplace
====================

Probability density function of the Laplace distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_laplace</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$ave`</span> ,
<span class="methodparam"><span class="type">float</span>
`$stdev`</span> )

Returns the probability density at `x`, where the random variable
follows the Laplace distribution of which the location parameter is
`ave` and the scale parameter is `stdev`.

### 参数

`x`  
The value at which the probability density is calculated

`ave`  
The location parameter of the distribution

`stdev`  
The shape parameter of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_logistic
=====================

Probability density function of the logistic distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_logistic</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$ave`</span> ,
<span class="methodparam"><span class="type">float</span>
`$stdev`</span> )

Returns the probability density at `x`, where the random variable
follows the logistic distribution of which the location parameter is
`ave` and the scale parameter is `stdev`.

### 参数

`x`  
The value at which the probability density is calculated

`ave`  
The location parameter of the distribution

`stdev`  
The shape parameter of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_normal
===================

Probability density function of the normal distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_normal</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$ave`</span> ,
<span class="methodparam"><span class="type">float</span>
`$stdev`</span> )

Returns the probability density at `x`, where the random variable
follows the normal distribution of which the mean is `ave` and the
standard deviation is `stdev`.

### 参数

`x`  
The value at which the probability density is calculated

`ave`  
The mean of the distribution

`stdev`  
The standard deviation of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_pmf\_binomial
==========================

Probability mass function of the binomial distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_pmf\_binomial</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$n`</span> , <span
class="methodparam"><span class="type">float</span> `$pi`</span> )

Returns the probability mass at `x`, where the random variable follows
the binomial distribution of which the number of trials is `n` and the
success rate is `pi`.

### 参数

`x`  
The value at which the probability mass is calculated

`n`  
The number of trials of the distribution

`pi`  
The success rate of the distribution

### 返回值

The probability mass at `x` or **`FALSE`** for failure.

stats\_dens\_pmf\_hypergeometric
================================

Probability mass function of the hypergeometric distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_pmf\_hypergeometric</span> ( <span
class="methodparam"><span class="type">float</span> `$n1`</span> , <span
class="methodparam"><span class="type">float</span> `$n2`</span> , <span
class="methodparam"><span class="type">float</span> `$N1`</span> , <span
class="methodparam"><span class="type">float</span> `$N2`</span> )

Returns the probability mass at `n1`, where the random variable follows
the hypergeometric distribution of which the number of failure is `n2`,
the number of success samples is `N1`, and the number of failure samples
is `N2`.

### 参数

`n1`  
The number of success, at which the probability mass is calculated

`n2`  
The number of failure of the distribution

`N1`  
The number of success samples of the distribution

`N2`  
The number of failure samples of the distribution

### 返回值

The probability mass at `n1` or **`FALSE`** for failure.

stats\_dens\_pmf\_negative\_binomial
====================================

Probability mass function of the negative binomial distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_pmf\_negative\_binomial</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$n`</span> , <span
class="methodparam"><span class="type">float</span> `$pi`</span> )

Returns the probability mass at `x`, where the random variable follows
the negative binomial distribution of which the number of the success is
`n` and the success rate is `pi`.

### 参数

`x`  
The value at which the probability mass is calculated

`n`  
The number of the success of the distribution

`pi`  
The success rate of the distribution

### 返回值

The probability mass at `x` or **`FALSE`** for failure.

stats\_dens\_pmf\_poisson
=========================

Probability mass function of the Poisson distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_pmf\_poisson</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$lb`</span> )

Returns the probability mass at `x`, where the random variable follows
the Poisson distribution whose parameter is `lb`.

### 参数

`x`  
The value at which the probability mass is calculated

`lb`  
The parameter of the Poisson distribution

### 返回值

The probability mass at `x` or **`FALSE`** for failure.

stats\_dens\_t
==============

Probability density function of the t-distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_t</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$dfr`</span> )

Returns the probability density at `x`, where the random variable
follows the t-distribution of which the degree of freedom is `dfr`.

### 参数

`x`  
The value at which the probability density is calculated

`dfr`  
The degree of freedom of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_uniform
====================

Probability density function of the uniform distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_uniform</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> )

Returns the probability density at `x`, where the random variable
follows the uniform distribution of which the lower bound is `a` and the
upper bound is `b`.

### 参数

`x`  
The value at which the probability density is calculated

`a`  
The lower bound of the distribution

`b`  
The upper bound of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_dens\_weibull
====================

Probability density function of the Weibull distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_dens\_weibull</span> ( <span
class="methodparam"><span class="type">float</span> `$x`</span> , <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> )

Returns the probability density at `x`, where the random variable
follows the Weibull distribution of which the shape parameter is `a` and
the scale parameter is `b`.

### 参数

`x`  
The value at which the probability density is calculated

`a`  
The shape parameter of the distribution

`b`  
The scale parameter of the distribution

### 返回值

The probability density at `x` or **`FALSE`** for failure.

stats\_harmonic\_mean
=====================

Returns the harmonic mean of an array of values

### 说明

<span class="type">number</span> <span
class="methodname">stats\_harmonic\_mean</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> )

Returns the harmonic mean of the values in `a`.

### 参数

`a`  
The input array

### 返回值

Returns the harmonic mean of the values in `a`, or **`FALSE`** if `a` is
empty or is not an array.

stats\_kurtosis
===============

Computes the kurtosis of the data in the array

### 说明

<span class="type">float</span> <span
class="methodname">stats\_kurtosis</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> )

Returns the kurtosis of the values in `a`.

### 参数

`a`  
The input array

### 返回值

Returns the kurtosis of the values in `a`, or **`FALSE`** if `a` is
empty or is not an array.

stats\_rand\_gen\_beta
======================

Generates a random deviate from the beta distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_beta</span> ( <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$b`</span> )

Returns a random deviate from the beta distribution with parameters A
and B. The density of the beta is x^(a-1) \* (1-x)^(b-1) / B(a,b) for 0
\< x \<. Method R. C. H. Cheng.

### 参数

`a`  
The shape parameter of the beta distribution

`b`  
The shape parameter of the beta distribution

### 返回值

A random deviate

stats\_rand\_gen\_chisquare
===========================

Generates a random deviate from the chi-square distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_chisquare</span> ( <span
class="methodparam"><span class="type">float</span> `$df`</span> )

Returns a random deviate from the chi-square distribution where the
degrees of freedom is `df`.

### 参数

`df`  
The degrees of freedom

### 返回值

A random deviate

stats\_rand\_gen\_exponential
=============================

Generates a random deviate from the exponential distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_exponential</span> ( <span
class="methodparam"><span class="type">float</span> `$av`</span> )

Returns a random deviate from the exponential distribution of which the
scale is `av`.

### 参数

`av`  
The scale parameter

### 返回值

A random deviate

stats\_rand\_gen\_f
===================

Generates a random deviate from the F distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_f</span> ( <span
class="methodparam"><span class="type">float</span> `$dfn`</span> ,
<span class="methodparam"><span class="type">float</span> `$dfd`</span>
)

Generates a random deviate from the F (variance ratio) distribution with
"dfn" degrees of freedom in the numerator and "dfd" degrees of freedom
in the denominator. Method : directly generates ratio of chisquare
variates.

### 参数

`dfn`  
The degrees of freedom in the numerator

`dfd`  
The degrees of freedom in the denominator

### 返回值

A random deviate

stats\_rand\_gen\_funiform
==========================

Generates uniform float between low (exclusive) and high (exclusive)

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_funiform</span> ( <span
class="methodparam"><span class="type">float</span> `$low`</span> ,
<span class="methodparam"><span class="type">float</span> `$high`</span>
)

Returns a random deviate from the uniform distribution from `low` to
`high`.

### 参数

`low`  
The lower bound (inclusive)

`high`  
The upper bound (exclusive)

### 返回值

A random deviate

stats\_rand\_gen\_gamma
=======================

Generates a random deviate from the gamma distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_gamma</span> ( <span
class="methodparam"><span class="type">float</span> `$a`</span> , <span
class="methodparam"><span class="type">float</span> `$r`</span> )

Generates a random deviate from the gamma distribution whose density is
(A\*\*R)/Gamma(R) \* X\*\*(R-1) \* Exp(-A\*X).

### 参数

`a`  
location parameter of Gamma distribution (`a` \> 0).

`r`  
shape parameter of Gamma distribution (`r` \> 0).

### 返回值

A random deviate

stats\_rand\_gen\_ibinomial\_negative
=====================================

Generates a random deviate from the negative binomial distribution

### 说明

<span class="type">int</span> <span
class="methodname">stats\_rand\_gen\_ibinomial\_negative</span> ( <span
class="methodparam"><span class="type">int</span> `$n`</span> , <span
class="methodparam"><span class="type">float</span> `$p`</span> )

Returns a random deviate from a negative binomial distribution where the
number of success is `n` and the success rate is `p`.

### 参数

`n`  
The number of success

`p`  
The success rate

### 返回值

A random deviate, which is the number of failure.

stats\_rand\_gen\_ibinomial
===========================

Generates a random deviate from the binomial distribution

### 说明

<span class="type">int</span> <span
class="methodname">stats\_rand\_gen\_ibinomial</span> ( <span
class="methodparam"><span class="type">int</span> `$n`</span> , <span
class="methodparam"><span class="type">float</span> `$pp`</span> )

Returns a random deviate from the binomial distribution whose number of
trials is `n` and whose probability of an event in each trial is `pp`.

### 参数

`n`  
The number of trials

`pp`  
The probability of an event in each trial

### 返回值

A random deviate

stats\_rand\_gen\_int
=====================

Generates random integer between 1 and 2147483562

### 说明

<span class="type">int</span> <span
class="methodname">stats\_rand\_gen\_int</span> ( <span
class="methodparam">void</span> )

Returns a random integer between 1 and 2147483562

### 返回值

A random integer

stats\_rand\_gen\_ipoisson
==========================

Generates a single random deviate from a Poisson distribution

### 说明

<span class="type">int</span> <span
class="methodname">stats\_rand\_gen\_ipoisson</span> ( <span
class="methodparam"><span class="type">float</span> `$mu`</span> )

Returns a random deviate from the Poisson distribution with parameter
`mu`.

### 参数

`mu`  
The parameter of the Poisson distribution

### 返回值

A random deviate

stats\_rand\_gen\_iuniform
==========================

Generates integer uniformly distributed between LOW (inclusive) and HIGH
(inclusive)

### 说明

<span class="type">int</span> <span
class="methodname">stats\_rand\_gen\_iuniform</span> ( <span
class="methodparam"><span class="type">int</span> `$low`</span> , <span
class="methodparam"><span class="type">int</span> `$high`</span> )

Returns a random integer from the discrete uniform distribution between
`low` (inclusive) and `high` (inclusive).

### 参数

`low`  
The lower bound

`high`  
The upper bound

### 返回值

A random integer

stats\_rand\_gen\_noncentral\_chisquare
=======================================

Generates a random deviate from the non-central chi-square distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_noncentral\_chisquare</span> (
<span class="methodparam"><span class="type">float</span> `$df`</span> ,
<span class="methodparam"><span class="type">float</span>
`$xnonc`</span> )

Returns a random deviate from the non-central chi-square distribution
with degrees of freedom, `df`, and non-centrality parameter, `xnonc`.

### 参数

`df`  
The degrees of freedom

`xnonc`  
The non-centrality parameter

### 返回值

A random deviate

stats\_rand\_gen\_noncentral\_f
===============================

Generates a random deviate from the noncentral F distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_noncentral\_f</span> ( <span
class="methodparam"><span class="type">float</span> `$dfn`</span> ,
<span class="methodparam"><span class="type">float</span> `$dfd`</span>
, <span class="methodparam"><span class="type">float</span>
`$xnonc`</span> )

Returns a random deviate from the non-central F distribution where the
degrees of freedoms are `dfn` (numerator) and `dfd` (denominator), and
the non-centrality parameter is `xnonc`.

### 参数

`dfn`  
The degrees of freedom of the numerator

`dfd`  
The degrees of freedom of the denominator

`xnonc`  
The non-centrality parameter

### 返回值

A random deviate

stats\_rand\_gen\_noncentral\_t
===============================

Generates a single random deviate from a non-central t-distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_noncentral\_t</span> ( <span
class="methodparam"><span class="type">float</span> `$df`</span> , <span
class="methodparam"><span class="type">float</span> `$xnonc`</span> )

Returns a random deviate from the non-central t-distribution with the
degrees of freedom, `df`, and the non-centrality parameter, `xnonc`.

### 参数

`df`  
The degrees of freedom

`xnonc`  
The non-centrality parameter

### 返回值

A random deviate

stats\_rand\_gen\_normal
========================

Generates a single random deviate from a normal distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_normal</span> ( <span
class="methodparam"><span class="type">float</span> `$av`</span> , <span
class="methodparam"><span class="type">float</span> `$sd`</span> )

Returns a random deviate from the normal distribution with mean, `av`,
and standard deviation, `sd`.

### 参数

`av`  
The mean of the normal distribution

`sd`  
The standard deviation of the normal distribution

### 返回值

A random deviate

stats\_rand\_gen\_t
===================

Generates a single random deviate from a t-distribution

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_gen\_t</span> ( <span
class="methodparam"><span class="type">float</span> `$df`</span> )

Returns a random deviate from the t-distribution with the degrees of
freedom, `df`.

### 参数

`df`  
The degrees of freedom

### 返回值

A random deviate

stats\_rand\_get\_seeds
=======================

Get the seed values of the random number generator

### 说明

<span class="type">array</span> <span
class="methodname">stats\_rand\_get\_seeds</span> ( <span
class="methodparam">void</span> )

Returns the current seed values of the random number generator

### 返回值

Returns an array of two integers.

stats\_rand\_phrase\_to\_seeds
==============================

Generate two seeds for the RGN random number generator

### 说明

<span class="type">array</span> <span
class="methodname">stats\_rand\_phrase\_to\_seeds</span> ( <span
class="methodparam"><span class="type">string</span> `$phrase`</span> )

Generate two seeds for the random number generator from a `phrase`.

### 参数

`phrase`  
The input phrase

### 返回值

Returns an array of two integers.

stats\_rand\_ranf
=================

Generates a random floating point number between 0 and 1

### 说明

<span class="type">float</span> <span
class="methodname">stats\_rand\_ranf</span> ( <span
class="methodparam">void</span> )

Returns a random floating point number from a uniform distribution
between 0 (exclusive) and 1 (exclusive).

### 返回值

A random floating point number

stats\_rand\_setall
===================

Set seed values to the random generator

### 说明

<span class="type">void</span> <span
class="methodname">stats\_rand\_setall</span> ( <span
class="methodparam"><span class="type">int</span> `$iseed1`</span> ,
<span class="methodparam"><span class="type">int</span> `$iseed2`</span>
)

Set `iseed1` and `iseed2` as seed values to the random generator used in
statistic functions.

### 参数

`iseed1`  
The value which is used as the random seed

`iseed2`  
The value which is used as the random seed

### 返回值

No values are returned.

stats\_skew
===========

Computes the skewness of the data in the array

### 说明

<span class="type">float</span> <span
class="methodname">stats\_skew</span> ( <span class="methodparam"><span
class="type">array</span> `$a`</span> )

Returns the skewness of the values in `a`.

### 参数

`a`  
The input array

### 返回值

Returns the skewness of the values in `a`, or **`FALSE`** if `a` is
empty or is not an array.

stats\_standard\_deviation
==========================

Returns the standard deviation

### 说明

<span class="type">float</span> <span
class="methodname">stats\_standard\_deviation</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$sample`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Returns the standard deviation of the values in `a`.

### 参数

`a`  
The array of data to find the standard deviation for. Note that all
values of the array will be cast to <span class="type">float</span>.

`sample`  
Indicates if `a` represents a sample of the population; defaults to
**`FALSE`**.

### 返回值

Returns the standard deviation on success; **`FALSE`** on failure.

### 错误／异常

Raises an **`E_WARNING`** when there are fewer than 2 values in `a`.

stats\_stat\_binomial\_coef
===========================

Returns a binomial coefficient

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_binomial\_coef</span> ( <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$n`</span> )

Returns the binomial coefficient of `n` choose `x`.

### 参数

`x`  
The number of chooses from the set

`n`  
The number of elements in the set

### 返回值

Returns the binomial coefficient

stats\_stat\_correlation
========================

Returns the Pearson correlation coefficient of two data sets

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_correlation</span> ( <span
class="methodparam"><span class="type">array</span> `$arr1`</span> ,
<span class="methodparam"><span class="type">array</span> `$arr2`</span>
)

Returns the Pearson correlation coefficient between `arr1` and `arr2`.

### 参数

`arr1`  
The first array

`arr2`  
The second array

### 返回值

Returns the Pearson correlation coefficient between `arr1` and `arr2`,
or **`FALSE`** on failure.

stats\_stat\_factorial
======================

Returns the factorial of an integer

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_factorial</span> ( <span
class="methodparam"><span class="type">int</span> `$n`</span> )

Returns the factorial of an integer, `n`.

### 参数

`n`  
An integer

### 返回值

The factorial of `n`.

stats\_stat\_independent\_t
===========================

Returns the t-value from the independent two-sample t-test

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_independent\_t</span> ( <span
class="methodparam"><span class="type">array</span> `$arr1`</span> ,
<span class="methodparam"><span class="type">array</span> `$arr2`</span>
)

Returns the t-value of the independent two-sample t-test between `arr1`
and `arr2`.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`arr1`  
The first set of values

`arr2`  
The second set of values

### 返回值

Returns the t-value, or **`FALSE`** if failure.

stats\_stat\_innerproduct
=========================

Returns the inner product of two vectors

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_innerproduct</span> ( <span
class="methodparam"><span class="type">array</span> `$arr1`</span> ,
<span class="methodparam"><span class="type">array</span> `$arr2`</span>
)

Returns the inner product of `arr1` and `arr2`.

### 参数

`arr1`  
The first array

`arr2`  
The second array

### 返回值

Returns the inner product of `arr1` and `arr2`, or **`FALSE`** on
failure.

stats\_stat\_paired\_t
======================

Returns the t-value of the dependent t-test for paired samples

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_paired\_t</span> ( <span
class="methodparam"><span class="type">array</span> `$arr1`</span> ,
<span class="methodparam"><span class="type">array</span> `$arr2`</span>
)

Returns the t-value of the dependent t-test for paired samples `arr1`
and `arr2`.

### 参数

`arr1`  
The first samples

`arr2`  
The second samples

### 返回值

Returns the t-value, or **`FALSE`** if failure.

stats\_stat\_percentile
=======================

Returns the percentile value

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_percentile</span> ( <span
class="methodparam"><span class="type">array</span> `$arr`</span> ,
<span class="methodparam"><span class="type">float</span> `$perc`</span>
)

Returns the `perc`-th percentile value of the array `arr`.

### 参数

`arr`  
The input array

`perc`  
The percentile

### 返回值

Returns the percentile values of the input array.

stats\_stat\_powersum
=====================

Returns the power sum of a vector

### 说明

<span class="type">float</span> <span
class="methodname">stats\_stat\_powersum</span> ( <span
class="methodparam"><span class="type">array</span> `$arr`</span> ,
<span class="methodparam"><span class="type">float</span>
`$power`</span> )

Returns the sum of the `power`-th power of a vector represented as an
array `arr`.

### 参数

`arr`  
The input array

`power`  
The power

### 返回值

Returns the power sum of the input array.

stats\_variance
===============

Returns the variance

### 说明

<span class="type">float</span> <span
class="methodname">stats\_variance</span> ( <span
class="methodparam"><span class="type">array</span> `$a`</span> \[,
<span class="methodparam"><span class="type">bool</span> `$sample`<span
class="initializer"> = **`FALSE`**</span></span> \] )

Returns the variance of the values in `a`.

### 参数

`a`  
The array of data to find the standard deviation for. Note that all
values of the array will be cast to <span class="type">float</span>.

`sample`  
Indicates if `a` represents a sample of the population; defaults to
**`FALSE`**.

### 返回值

Returns the variance on success; **`FALSE`** on failure.

**目录**

-   [stats\_absolute\_deviation](/ref/stats.html#stats_absolute_deviation)
    — Returns the absolute deviation of an array of values
-   [stats\_cdf\_beta](/ref/stats.html#stats_cdf_beta) — Calculates any
    one parameter of the beta distribution given values for the others
-   [stats\_cdf\_binomial](/ref/stats.html#stats_cdf_binomial) —
    Calculates any one parameter of the binomial distribution given
    values for the others
-   [stats\_cdf\_cauchy](/ref/stats.html#stats_cdf_cauchy) — Calculates
    any one parameter of the Cauchy distribution given values for the
    others
-   [stats\_cdf\_chisquare](/ref/stats.html#stats_cdf_chisquare) —
    Calculates any one parameter of the chi-square distribution given
    values for the others
-   [stats\_cdf\_exponential](/ref/stats.html#stats_cdf_exponential) —
    Calculates any one parameter of the exponential distribution given
    values for the others
-   [stats\_cdf\_f](/ref/stats.html#stats_cdf_f) — Calculates any one
    parameter of the F distribution given values for the others
-   [stats\_cdf\_gamma](/ref/stats.html#stats_cdf_gamma) — Calculates
    any one parameter of the gamma distribution given values for the
    others
-   [stats\_cdf\_laplace](/ref/stats.html#stats_cdf_laplace) —
    Calculates any one parameter of the Laplace distribution given
    values for the others
-   [stats\_cdf\_logistic](/ref/stats.html#stats_cdf_logistic) —
    Calculates any one parameter of the logistic distribution given
    values for the others
-   [stats\_cdf\_negative\_binomial](/ref/stats.html#stats_cdf_negative_binomial)
    — Calculates any one parameter of the negative binomial distribution
    given values for the others
-   [stats\_cdf\_noncentral\_chisquare](/ref/stats.html#stats_cdf_noncentral_chisquare)
    — Calculates any one parameter of the non-central chi-square
    distribution given values for the others
-   [stats\_cdf\_noncentral\_f](/ref/stats.html#stats_cdf_noncentral_f)
    — Calculates any one parameter of the non-central F distribution
    given values for the others
-   [stats\_cdf\_noncentral\_t](/ref/stats.html#stats_cdf_noncentral_t)
    — Calculates any one parameter of the non-central t-distribution
    give values for the others
-   [stats\_cdf\_normal](/ref/stats.html#stats_cdf_normal) — Calculates
    any one parameter of the normal distribution given values for the
    others
-   [stats\_cdf\_poisson](/ref/stats.html#stats_cdf_poisson) —
    Calculates any one parameter of the Poisson distribution given
    values for the others
-   [stats\_cdf\_t](/ref/stats.html#stats_cdf_t) — Calculates any one
    parameter of the t-distribution given values for the others
-   [stats\_cdf\_uniform](/ref/stats.html#stats_cdf_uniform) —
    Calculates any one parameter of the uniform distribution given
    values for the others
-   [stats\_cdf\_weibull](/ref/stats.html#stats_cdf_weibull) —
    Calculates any one parameter of the Weibull distribution given
    values for the others
-   [stats\_covariance](/ref/stats.html#stats_covariance) — Computes the
    covariance of two data sets
-   [stats\_dens\_beta](/ref/stats.html#stats_dens_beta) — Probability
    density function of the beta distribution
-   [stats\_dens\_cauchy](/ref/stats.html#stats_dens_cauchy) —
    Probability density function of the Cauchy distribution
-   [stats\_dens\_chisquare](/ref/stats.html#stats_dens_chisquare) —
    Probability density function of the chi-square distribution
-   [stats\_dens\_exponential](/ref/stats.html#stats_dens_exponential) —
    Probability density function of the exponential distribution
-   [stats\_dens\_f](/ref/stats.html#stats_dens_f) — Probability density
    function of the F distribution
-   [stats\_dens\_gamma](/ref/stats.html#stats_dens_gamma) — Probability
    density function of the gamma distribution
-   [stats\_dens\_laplace](/ref/stats.html#stats_dens_laplace) —
    Probability density function of the Laplace distribution
-   [stats\_dens\_logistic](/ref/stats.html#stats_dens_logistic) —
    Probability density function of the logistic distribution
-   [stats\_dens\_normal](/ref/stats.html#stats_dens_normal) —
    Probability density function of the normal distribution
-   [stats\_dens\_pmf\_binomial](/ref/stats.html#stats_dens_pmf_binomial)
    — Probability mass function of the binomial distribution
-   [stats\_dens\_pmf\_hypergeometric](/ref/stats.html#stats_dens_pmf_hypergeometric)
    — Probability mass function of the hypergeometric distribution
-   [stats\_dens\_pmf\_negative\_binomial](/ref/stats.html#stats_dens_pmf_negative_binomial)
    — Probability mass function of the negative binomial distribution
-   [stats\_dens\_pmf\_poisson](/ref/stats.html#stats_dens_pmf_poisson)
    — Probability mass function of the Poisson distribution
-   [stats\_dens\_t](/ref/stats.html#stats_dens_t) — Probability density
    function of the t-distribution
-   [stats\_dens\_uniform](/ref/stats.html#stats_dens_uniform) —
    Probability density function of the uniform distribution
-   [stats\_dens\_weibull](/ref/stats.html#stats_dens_weibull) —
    Probability density function of the Weibull distribution
-   [stats\_harmonic\_mean](/ref/stats.html#stats_harmonic_mean) —
    Returns the harmonic mean of an array of values
-   [stats\_kurtosis](/ref/stats.html#stats_kurtosis) — Computes the
    kurtosis of the data in the array
-   [stats\_rand\_gen\_beta](/ref/stats.html#stats_rand_gen_beta) —
    Generates a random deviate from the beta distribution
-   [stats\_rand\_gen\_chisquare](/ref/stats.html#stats_rand_gen_chisquare)
    — Generates a random deviate from the chi-square distribution
-   [stats\_rand\_gen\_exponential](/ref/stats.html#stats_rand_gen_exponential)
    — Generates a random deviate from the exponential distribution
-   [stats\_rand\_gen\_f](/ref/stats.html#stats_rand_gen_f) — Generates
    a random deviate from the F distribution
-   [stats\_rand\_gen\_funiform](/ref/stats.html#stats_rand_gen_funiform)
    — Generates uniform float between low (exclusive) and high
    (exclusive)
-   [stats\_rand\_gen\_gamma](/ref/stats.html#stats_rand_gen_gamma) —
    Generates a random deviate from the gamma distribution
-   [stats\_rand\_gen\_ibinomial\_negative](/ref/stats.html#stats_rand_gen_ibinomial_negative)
    — Generates a random deviate from the negative binomial distribution
-   [stats\_rand\_gen\_ibinomial](/ref/stats.html#stats_rand_gen_ibinomial)
    — Generates a random deviate from the binomial distribution
-   [stats\_rand\_gen\_int](/ref/stats.html#stats_rand_gen_int) —
    Generates random integer between 1 and 2147483562
-   [stats\_rand\_gen\_ipoisson](/ref/stats.html#stats_rand_gen_ipoisson)
    — Generates a single random deviate from a Poisson distribution
-   [stats\_rand\_gen\_iuniform](/ref/stats.html#stats_rand_gen_iuniform)
    — Generates integer uniformly distributed between LOW (inclusive)
    and HIGH (inclusive)
-   [stats\_rand\_gen\_noncentral\_chisquare](/ref/stats.html#stats_rand_gen_noncentral_chisquare)
    — Generates a random deviate from the non-central chi-square
    distribution
-   [stats\_rand\_gen\_noncentral\_f](/ref/stats.html#stats_rand_gen_noncentral_f)
    — Generates a random deviate from the noncentral F distribution
-   [stats\_rand\_gen\_noncentral\_t](/ref/stats.html#stats_rand_gen_noncentral_t)
    — Generates a single random deviate from a non-central
    t-distribution
-   [stats\_rand\_gen\_normal](/ref/stats.html#stats_rand_gen_normal) —
    Generates a single random deviate from a normal distribution
-   [stats\_rand\_gen\_t](/ref/stats.html#stats_rand_gen_t) — Generates
    a single random deviate from a t-distribution
-   [stats\_rand\_get\_seeds](/ref/stats.html#stats_rand_get_seeds) —
    Get the seed values of the random number generator
-   [stats\_rand\_phrase\_to\_seeds](/ref/stats.html#stats_rand_phrase_to_seeds)
    — Generate two seeds for the RGN random number generator
-   [stats\_rand\_ranf](/ref/stats.html#stats_rand_ranf) — Generates a
    random floating point number between 0 and 1
-   [stats\_rand\_setall](/ref/stats.html#stats_rand_setall) — Set seed
    values to the random generator
-   [stats\_skew](/ref/stats.html#stats_skew) — Computes the skewness of
    the data in the array
-   [stats\_standard\_deviation](/ref/stats.html#stats_standard_deviation)
    — Returns the standard deviation
-   [stats\_stat\_binomial\_coef](/ref/stats.html#stats_stat_binomial_coef)
    — Returns a binomial coefficient
-   [stats\_stat\_correlation](/ref/stats.html#stats_stat_correlation) —
    Returns the Pearson correlation coefficient of two data sets
-   [stats\_stat\_factorial](/ref/stats.html#stats_stat_factorial) —
    Returns the factorial of an integer
-   [stats\_stat\_independent\_t](/ref/stats.html#stats_stat_independent_t)
    — Returns the t-value from the independent two-sample t-test
-   [stats\_stat\_innerproduct](/ref/stats.html#stats_stat_innerproduct)
    — Returns the inner product of two vectors
-   [stats\_stat\_paired\_t](/ref/stats.html#stats_stat_paired_t) —
    Returns the t-value of the dependent t-test for paired samples
-   [stats\_stat\_percentile](/ref/stats.html#stats_stat_percentile) —
    Returns the percentile value
-   [stats\_stat\_powersum](/ref/stats.html#stats_stat_powersum) —
    Returns the power sum of a vector
-   [stats\_variance](/ref/stats.html#stats_variance) — Returns the
    variance

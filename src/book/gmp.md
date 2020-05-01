GNU Multiple Precision
======================

**目录**

-   [简介](/intro/gmp.html)
-   [安装／配置](/gmp/setup.html)
    -   [需求](/gmp/setup.html#需求)
    -   [安装](/gmp/setup.html#安装)
    -   [运行时配置](/gmp/setup.html#运行时配置)
    -   [资源类型](/gmp/setup.html#资源类型)
-   [预定义常量](/gmp/constants.html)
-   [范例](/gmp/examples.html)
-   [GMP 函数](/ref/gmp.html)
    -   [gmp\_abs](/ref/gmp.html#gmp_abs) — Absolute value
    -   [gmp\_add](/ref/gmp.html#gmp_add) — Add numbers
    -   [gmp\_and](/ref/gmp.html#gmp_and) — Bitwise AND
    -   [gmp\_binomial](/ref/gmp.html#gmp_binomial) — Calculates
        binomial coefficient
    -   [gmp\_clrbit](/ref/gmp.html#gmp_clrbit) — Clear bit
    -   [gmp\_cmp](/ref/gmp.html#gmp_cmp) — Compare numbers
    -   [gmp\_com](/ref/gmp.html#gmp_com) — Calculates one's complement
    -   [gmp\_div\_q](/ref/gmp.html#gmp_div_q) — Divide numbers
    -   [gmp\_div\_qr](/ref/gmp.html#gmp_div_qr) — Divide numbers and
        get quotient and remainder
    -   [gmp\_div\_r](/ref/gmp.html#gmp_div_r) — Remainder of the
        division of numbers
    -   [gmp\_div](/ref/gmp.html#gmp_div) — 别名 gmp\_div\_q
    -   [gmp\_divexact](/ref/gmp.html#gmp_divexact) — Exact division of
        numbers
    -   [gmp\_export](/ref/gmp.html#gmp_export) — Export to a binary
        string
    -   [gmp\_fact](/ref/gmp.html#gmp_fact) — Factorial
    -   [gmp\_gcd](/ref/gmp.html#gmp_gcd) — Calculate GCD
    -   [gmp\_gcdext](/ref/gmp.html#gmp_gcdext) — Calculate GCD and
        multipliers
    -   [gmp\_hamdist](/ref/gmp.html#gmp_hamdist) — Hamming distance
    -   [gmp\_import](/ref/gmp.html#gmp_import) — Import from a binary
        string
    -   [gmp\_init](/ref/gmp.html#gmp_init) — Create GMP number
    -   [gmp\_intval](/ref/gmp.html#gmp_intval) — Convert GMP number to
        integer
    -   [gmp\_invert](/ref/gmp.html#gmp_invert) — Inverse by modulo
    -   [gmp\_jacobi](/ref/gmp.html#gmp_jacobi) — Jacobi symbol
    -   [gmp\_kronecker](/ref/gmp.html#gmp_kronecker) — Kronecker symbol
    -   [gmp\_lcm](/ref/gmp.html#gmp_lcm) — Calculate LCM
    -   [gmp\_legendre](/ref/gmp.html#gmp_legendre) — Legendre symbol
    -   [gmp\_mod](/ref/gmp.html#gmp_mod) — Modulo operation
    -   [gmp\_mul](/ref/gmp.html#gmp_mul) — Multiply numbers
    -   [gmp\_neg](/ref/gmp.html#gmp_neg) — Negate number
    -   [gmp\_nextprime](/ref/gmp.html#gmp_nextprime) — Find next prime
        number
    -   [gmp\_or](/ref/gmp.html#gmp_or) — Bitwise OR
    -   [gmp\_perfect\_power](/ref/gmp.html#gmp_perfect_power) — Perfect
        power check
    -   [gmp\_perfect\_square](/ref/gmp.html#gmp_perfect_square) —
        Perfect square check
    -   [gmp\_popcount](/ref/gmp.html#gmp_popcount) — Population count
    -   [gmp\_pow](/ref/gmp.html#gmp_pow) — Raise number into power
    -   [gmp\_powm](/ref/gmp.html#gmp_powm) — Raise number into power
        with modulo
    -   [gmp\_prob\_prime](/ref/gmp.html#gmp_prob_prime) — Check if
        number is "probably prime"
    -   [gmp\_random\_bits](/ref/gmp.html#gmp_random_bits) — Random
        number
    -   [gmp\_random\_range](/ref/gmp.html#gmp_random_range) — Random
        number
    -   [gmp\_random\_seed](/ref/gmp.html#gmp_random_seed) — Sets the
        RNG seed
    -   [gmp\_random](/ref/gmp.html#gmp_random) — Random number
    -   [gmp\_root](/ref/gmp.html#gmp_root) — Take the integer part of
        nth root
    -   [gmp\_rootrem](/ref/gmp.html#gmp_rootrem) — Take the integer
        part and remainder of nth root
    -   [gmp\_scan0](/ref/gmp.html#gmp_scan0) — Scan for 0
    -   [gmp\_scan1](/ref/gmp.html#gmp_scan1) — Scan for 1
    -   [gmp\_setbit](/ref/gmp.html#gmp_setbit) — Set bit
    -   [gmp\_sign](/ref/gmp.html#gmp_sign) — Sign of number
    -   [gmp\_sqrt](/ref/gmp.html#gmp_sqrt) — Calculate square root
    -   [gmp\_sqrtrem](/ref/gmp.html#gmp_sqrtrem) — Square root with
        remainder
    -   [gmp\_strval](/ref/gmp.html#gmp_strval) — Convert GMP number to
        string
    -   [gmp\_sub](/ref/gmp.html#gmp_sub) — Subtract numbers
    -   [gmp\_testbit](/ref/gmp.html#gmp_testbit) — Tests if a bit is
        set
    -   [gmp\_xor](/ref/gmp.html#gmp_xor) — Bitwise XOR
-   [GMP](/class/gmp.html) — The GMP class

简介
----

A GMP number. These objects support overloaded
<a href="/language/operators/arithmetic.html" class="link">arithmetic</a>,
<a href="/language/operators/bitwise.html" class="link">bitwise</a> and
<a href="/language/operators/comparison.html" class="link">comparison</a>
operators.

> **Note**:
>
> No object oriented interface is provided to manipulate <span
> class="classname">GMP</span> objects. Please use the
> <a href="/book/gmp.html" class="link">procedural GMP API</a>.

**GMP**

<span class="ooclass"> class **GMP** </span> <span
class="oointerface">implements <span
class="interfacename">Serializable</span> </span> {

}

*Yet Another Configurations Container* (Yaconf) is a configurations
container, it parses INI files, and store the result in PHP when PHP is
started, the result lives with the whole PHP lifecycle.

Yaconf stores all configurations as interned string or immutable array,
which means they are not refcounted-able, thus when you retrieving
configurations from yaconf, it could be considered as zero-copy, very
fast.

Yaconf supports sections and sections inheritance in INI files. if PHP
is built as non-ZTS build, Yaconf also supports automatically reloading
after INI files are changed.

Yaconf requires PHP 7.0 or greater.

**示例 \#1 INI example**

``` ini
;simple key val
key=val
;hash
hash.a=val
;array
arr.0=val
;or
arr[]=val
;use PHP constants
version=PHP_VERION
;use enviroment
env=${PATH}
```

**示例 \#2 INI sections example**

``` ini
[SectionA]
key=val
hash.a=val

;SectionB inherits SectionA
[SectionB:SectionA]
;override configuration key in SectionA
key=new_val
```

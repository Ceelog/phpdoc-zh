Comparing generators with <span class="classname">Iterator</span> objects
-------------------------------------------------------------------------

The primary advantage of generators is their simplicity. Much less
boilerplate code has to be written compared to implementing an <span
class="classname">Iterator</span> class, and the code is generally much
more readable. For example, the following function and class are
equivalent:

``` php
<?php
function getLinesFromFile($fileName) {
    if (!$fileHandle = fopen($fileName, 'r')) {
        return;
    }
 
    while (false !== $line = fgets($fileHandle)) {
        yield $line;
    }
 
    fclose($fileHandle);
}

// versus...

class LineIterator implements Iterator {
    protected $fileHandle;
 
    protected $line;
    protected $i;
 
    public function __construct($fileName) {
        if (!$this->fileHandle = fopen($fileName, 'r')) {
            throw new RuntimeException('Couldn\'t open file "' . $fileName . '"');
        }
    }
 
    public function rewind() {
        fseek($this->fileHandle, 0);
        $this->line = fgets($this->fileHandle);
        $this->i = 0;
    }
 
    public function valid() {
        return false !== $this->line;
    }
 
    public function current() {
        return $this->line;
    }
 
    public function key() {
        return $this->i;
    }
 
    public function next() {
        if (false !== $this->line) {
            $this->line = fgets($this->fileHandle);
            $this->i++;
        }
    }
 
    public function __destruct() {
        fclose($this->fileHandle);
    }
}
?>
```

This flexibility does come at a cost, however: generators are
forward-only iterators, and cannot be rewound once iteration has
started. This also means that the same generator can't be iterated over
multiple times: the generator will need to either be rebuilt by calling
the generator function again, or cloned via the
<a href="/language/oop5/cloning.html" class="link">clone</a> keyword.

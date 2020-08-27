Data Structures
===============

**目录**

-   [简介](/intro/ds.html)
-   [安装／配置](/ds/setup.html)
    -   [需求](/ds/setup.html#需求)
    -   [安装](/ds/setup.html#安装)
-   [预定义常量](/ds/constants.html)
-   [范例](/ds/examples.html)
-   [Collection](/class/ds-collection.html) — The Collection interface
    -   [Ds\\Collection::clear](/class/ds-collection.html#Ds\Collection::clear)
        — Removes all values
    -   [Ds\\Collection::copy](/class/ds-collection.html#Ds\Collection::copy)
        — Returns a shallow copy of the collection
    -   [Ds\\Collection::isEmpty](/class/ds-collection.html#Ds\Collection::isEmpty)
        — Returns whether the collection is empty
    -   [Ds\\Collection::toArray](/class/ds-collection.html#Ds\Collection::toArray)
        — Converts the collection to an array
-   [Hashable](/class/ds-hashable.html) — The Hashable interface
    -   [Ds\\Hashable::equals](/class/ds-hashable.html#Ds\Hashable::equals)
        — Determines whether an object is equal to the current instance
    -   [Ds\\Hashable::hash](/class/ds-hashable.html#Ds\Hashable::hash)
        — Returns a scalar value to be used as a hash value
-   [Sequence](/class/ds-sequence.html) — The Sequence interface
    -   [Ds\\Sequence::allocate](/class/ds-sequence.html#Ds\Sequence::allocate)
        — Allocates enough memory for a required capacity
    -   [Ds\\Sequence::apply](/class/ds-sequence.html#Ds\Sequence::apply)
        — Updates all values by applying a callback function to each
        value
    -   [Ds\\Sequence::capacity](/class/ds-sequence.html#Ds\Sequence::capacity)
        — Returns the current capacity
    -   [Ds\\Sequence::contains](/class/ds-sequence.html#Ds\Sequence::contains)
        — Determines if the sequence contains given values
    -   [Ds\\Sequence::filter](/class/ds-sequence.html#Ds\Sequence::filter)
        — Creates a new sequence using a callable to determine which
        values to include
    -   [Ds\\Sequence::find](/class/ds-sequence.html#Ds\Sequence::find)
        — Attempts to find a value's index
    -   [Ds\\Sequence::first](/class/ds-sequence.html#Ds\Sequence::first)
        — Returns the first value in the sequence
    -   [Ds\\Sequence::get](/class/ds-sequence.html#Ds\Sequence::get) —
        Returns the value at a given index
    -   [Ds\\Sequence::insert](/class/ds-sequence.html#Ds\Sequence::insert)
        — Inserts values at a given index
    -   [Ds\\Sequence::join](/class/ds-sequence.html#Ds\Sequence::join)
        — Joins all values together as a string
    -   [Ds\\Sequence::last](/class/ds-sequence.html#Ds\Sequence::last)
        — Returns the last value
    -   [Ds\\Sequence::map](/class/ds-sequence.html#Ds\Sequence::map) —
        Returns the result of applying a callback to each value
    -   [Ds\\Sequence::merge](/class/ds-sequence.html#Ds\Sequence::merge)
        — Returns the result of adding all given values to the sequence
    -   [Ds\\Sequence::pop](/class/ds-sequence.html#Ds\Sequence::pop) —
        Removes and returns the last value
    -   [Ds\\Sequence::push](/class/ds-sequence.html#Ds\Sequence::push)
        — Adds values to the end of the sequence
    -   [Ds\\Sequence::reduce](/class/ds-sequence.html#Ds\Sequence::reduce)
        — Reduces the sequence to a single value using a callback
        function
    -   [Ds\\Sequence::remove](/class/ds-sequence.html#Ds\Sequence::remove)
        — Removes and returns a value by index
    -   [Ds\\Sequence::reverse](/class/ds-sequence.html#Ds\Sequence::reverse)
        — Reverses the sequence in-place
    -   [Ds\\Sequence::reversed](/class/ds-sequence.html#Ds\Sequence::reversed)
        — Returns a reversed copy
    -   [Ds\\Sequence::rotate](/class/ds-sequence.html#Ds\Sequence::rotate)
        — Rotates the sequence by a given number of rotations
    -   [Ds\\Sequence::set](/class/ds-sequence.html#Ds\Sequence::set) —
        Updates a value at a given index
    -   [Ds\\Sequence::shift](/class/ds-sequence.html#Ds\Sequence::shift)
        — Removes and returns the first value
    -   [Ds\\Sequence::slice](/class/ds-sequence.html#Ds\Sequence::slice)
        — Returns a sub-sequence of a given range
    -   [Ds\\Sequence::sort](/class/ds-sequence.html#Ds\Sequence::sort)
        — Sorts the sequence in-place
    -   [Ds\\Sequence::sorted](/class/ds-sequence.html#Ds\Sequence::sorted)
        — Returns a sorted copy
    -   [Ds\\Sequence::sum](/class/ds-sequence.html#Ds\Sequence::sum) —
        Returns the sum of all values in the sequence
    -   [Ds\\Sequence::unshift](/class/ds-sequence.html#Ds\Sequence::unshift)
        — Adds values to the front of the sequence
-   [Vector](/class/ds-vector.html) — The Vector class
    -   [Ds\\Vector::allocate](/class/ds-vector.html#Ds\Vector::allocate)
        — Allocates enough memory for a required capacity
    -   [Ds\\Vector::apply](/class/ds-vector.html#Ds\Vector::apply) —
        Updates all values by applying a callback function to each value
    -   [Ds\\Vector::capacity](/class/ds-vector.html#Ds\Vector::capacity)
        — Returns the current capacity
    -   [Ds\\Vector::clear](/class/ds-vector.html#Ds\Vector::clear) —
        Removes all values
    -   [Ds\\Vector::\_\_construct](/class/ds-vector.html#Ds\Vector::__construct)
        — Creates a new instance
    -   [Ds\\Vector::contains](/class/ds-vector.html#Ds\Vector::contains)
        — Determines if the vector contains given values
    -   [Ds\\Vector::copy](/class/ds-vector.html#Ds\Vector::copy) —
        Returns a shallow copy of the vector
    -   [Ds\\Vector::count](/class/ds-vector.html#Ds\Vector::count) —
        Returns the number of values in the collection
    -   [Ds\\Vector::filter](/class/ds-vector.html#Ds\Vector::filter) —
        Creates a new vector using a callable to determine which values
        to include
    -   [Ds\\Vector::find](/class/ds-vector.html#Ds\Vector::find) —
        Attempts to find a value's index
    -   [Ds\\Vector::first](/class/ds-vector.html#Ds\Vector::first) —
        Returns the first value in the vector
    -   [Ds\\Vector::get](/class/ds-vector.html#Ds\Vector::get) —
        Returns the value at a given index
    -   [Ds\\Vector::insert](/class/ds-vector.html#Ds\Vector::insert) —
        Inserts values at a given index
    -   [Ds\\Vector::isEmpty](/class/ds-vector.html#Ds\Vector::isEmpty)
        — Returns whether the vector is empty
    -   [Ds\\Vector::join](/class/ds-vector.html#Ds\Vector::join) —
        Joins all values together as a string
    -   [Ds\\Vector::jsonSerialize](/class/ds-vector.html#Ds\Vector::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\Vector::last](/class/ds-vector.html#Ds\Vector::last) —
        Returns the last value
    -   [Ds\\Vector::map](/class/ds-vector.html#Ds\Vector::map) —
        Returns the result of applying a callback to each value
    -   [Ds\\Vector::merge](/class/ds-vector.html#Ds\Vector::merge) —
        Returns the result of adding all given values to the vector
    -   [Ds\\Vector::pop](/class/ds-vector.html#Ds\Vector::pop) —
        Removes and returns the last value
    -   [Ds\\Vector::push](/class/ds-vector.html#Ds\Vector::push) — Adds
        values to the end of the vector
    -   [Ds\\Vector::reduce](/class/ds-vector.html#Ds\Vector::reduce) —
        Reduces the vector to a single value using a callback function
    -   [Ds\\Vector::remove](/class/ds-vector.html#Ds\Vector::remove) —
        Removes and returns a value by index
    -   [Ds\\Vector::reverse](/class/ds-vector.html#Ds\Vector::reverse)
        — Reverses the vector in-place
    -   [Ds\\Vector::reversed](/class/ds-vector.html#Ds\Vector::reversed)
        — Returns a reversed copy
    -   [Ds\\Vector::rotate](/class/ds-vector.html#Ds\Vector::rotate) —
        Rotates the vector by a given number of rotations
    -   [Ds\\Vector::set](/class/ds-vector.html#Ds\Vector::set) —
        Updates a value at a given index
    -   [Ds\\Vector::shift](/class/ds-vector.html#Ds\Vector::shift) —
        Removes and returns the first value
    -   [Ds\\Vector::slice](/class/ds-vector.html#Ds\Vector::slice) —
        Returns a sub-vector of a given range
    -   [Ds\\Vector::sort](/class/ds-vector.html#Ds\Vector::sort) —
        Sorts the vector in-place
    -   [Ds\\Vector::sorted](/class/ds-vector.html#Ds\Vector::sorted) —
        Returns a sorted copy
    -   [Ds\\Vector::sum](/class/ds-vector.html#Ds\Vector::sum) —
        Returns the sum of all values in the vector
    -   [Ds\\Vector::toArray](/class/ds-vector.html#Ds\Vector::toArray)
        — Converts the vector to an array
    -   [Ds\\Vector::unshift](/class/ds-vector.html#Ds\Vector::unshift)
        — Adds values to the front of the vector
-   [Deque](/class/ds-deque.html) — The Deque class
    -   [Ds\\Deque::allocate](/class/ds-deque.html#Ds\Deque::allocate) —
        Allocates enough memory for a required capacity
    -   [Ds\\Deque::apply](/class/ds-deque.html#Ds\Deque::apply) —
        Updates all values by applying a callback function to each value
    -   [Ds\\Deque::capacity](/class/ds-deque.html#Ds\Deque::capacity) —
        Returns the current capacity
    -   [Ds\\Deque::clear](/class/ds-deque.html#Ds\Deque::clear) —
        Removes all values from the deque
    -   [Ds\\Deque::\_\_construct](/class/ds-deque.html#Ds\Deque::__construct)
        — Creates a new instance
    -   [Ds\\Deque::contains](/class/ds-deque.html#Ds\Deque::contains) —
        Determines if the deque contains given values
    -   [Ds\\Deque::copy](/class/ds-deque.html#Ds\Deque::copy) — Returns
        a shallow copy of the deque
    -   [Ds\\Deque::count](/class/ds-deque.html#Ds\Deque::count) —
        Returns the number of values in the collection
    -   [Ds\\Deque::filter](/class/ds-deque.html#Ds\Deque::filter) —
        Creates a new deque using a callable to determine which values
        to include
    -   [Ds\\Deque::find](/class/ds-deque.html#Ds\Deque::find) —
        Attempts to find a value's index
    -   [Ds\\Deque::first](/class/ds-deque.html#Ds\Deque::first) —
        Returns the first value in the deque
    -   [Ds\\Deque::get](/class/ds-deque.html#Ds\Deque::get) — Returns
        the value at a given index
    -   [Ds\\Deque::insert](/class/ds-deque.html#Ds\Deque::insert) —
        Inserts values at a given index
    -   [Ds\\Deque::isEmpty](/class/ds-deque.html#Ds\Deque::isEmpty) —
        Returns whether the deque is empty
    -   [Ds\\Deque::join](/class/ds-deque.html#Ds\Deque::join) — Joins
        all values together as a string
    -   [Ds\\Deque::jsonSerialize](/class/ds-deque.html#Ds\Deque::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\Deque::last](/class/ds-deque.html#Ds\Deque::last) — Returns
        the last value
    -   [Ds\\Deque::map](/class/ds-deque.html#Ds\Deque::map) — Returns
        the result of applying a callback to each value
    -   [Ds\\Deque::merge](/class/ds-deque.html#Ds\Deque::merge) —
        Returns the result of adding all given values to the deque
    -   [Ds\\Deque::pop](/class/ds-deque.html#Ds\Deque::pop) — Removes
        and returns the last value
    -   [Ds\\Deque::push](/class/ds-deque.html#Ds\Deque::push) — Adds
        values to the end of the deque
    -   [Ds\\Deque::reduce](/class/ds-deque.html#Ds\Deque::reduce) —
        Reduces the deque to a single value using a callback function
    -   [Ds\\Deque::remove](/class/ds-deque.html#Ds\Deque::remove) —
        Removes and returns a value by index
    -   [Ds\\Deque::reverse](/class/ds-deque.html#Ds\Deque::reverse) —
        Reverses the deque in-place
    -   [Ds\\Deque::reversed](/class/ds-deque.html#Ds\Deque::reversed) —
        Returns a reversed copy
    -   [Ds\\Deque::rotate](/class/ds-deque.html#Ds\Deque::rotate) —
        Rotates the deque by a given number of rotations
    -   [Ds\\Deque::set](/class/ds-deque.html#Ds\Deque::set) — Updates a
        value at a given index
    -   [Ds\\Deque::shift](/class/ds-deque.html#Ds\Deque::shift) —
        Removes and returns the first value
    -   [Ds\\Deque::slice](/class/ds-deque.html#Ds\Deque::slice) —
        Returns a sub-deque of a given range
    -   [Ds\\Deque::sort](/class/ds-deque.html#Ds\Deque::sort) — Sorts
        the deque in-place
    -   [Ds\\Deque::sorted](/class/ds-deque.html#Ds\Deque::sorted) —
        Returns a sorted copy
    -   [Ds\\Deque::sum](/class/ds-deque.html#Ds\Deque::sum) — Returns
        the sum of all values in the deque
    -   [Ds\\Deque::toArray](/class/ds-deque.html#Ds\Deque::toArray) —
        Converts the deque to an array
    -   [Ds\\Deque::unshift](/class/ds-deque.html#Ds\Deque::unshift) —
        Adds values to the front of the deque
-   [Map](/class/ds-map.html) — The Map class
    -   [Ds\\Map::allocate](/class/ds-map.html#Ds\Map::allocate) —
        Allocates enough memory for a required capacity
    -   [Ds\\Map::apply](/class/ds-map.html#Ds\Map::apply) — Updates all
        values by applying a callback function to each value
    -   [Ds\\Map::capacity](/class/ds-map.html#Ds\Map::capacity) —
        Returns the current capacity
    -   [Ds\\Map::clear](/class/ds-map.html#Ds\Map::clear) — Removes all
        values
    -   [Ds\\Map::\_\_construct](/class/ds-map.html#Ds\Map::__construct)
        — Creates a new instance
    -   [Ds\\Map::copy](/class/ds-map.html#Ds\Map::copy) — Returns a
        shallow copy of the map
    -   [Ds\\Map::count](/class/ds-map.html#Ds\Map::count) — Returns the
        number of values in the map
    -   [Ds\\Map::diff](/class/ds-map.html#Ds\Map::diff) — Creates a new
        map using keys that aren't in another map
    -   [Ds\\Map::filter](/class/ds-map.html#Ds\Map::filter) — Creates a
        new map using a callable to determine which pairs to include
    -   [Ds\\Map::first](/class/ds-map.html#Ds\Map::first) — Returns the
        first pair in the map
    -   [Ds\\Map::get](/class/ds-map.html#Ds\Map::get) — Returns the
        value for a given key
    -   [Ds\\Map::hasKey](/class/ds-map.html#Ds\Map::hasKey) —
        Determines whether the map contains a given key
    -   [Ds\\Map::hasValue](/class/ds-map.html#Ds\Map::hasValue) —
        Determines whether the map contains a given value
    -   [Ds\\Map::intersect](/class/ds-map.html#Ds\Map::intersect) —
        Creates a new map by intersecting keys with another map
    -   [Ds\\Map::isEmpty](/class/ds-map.html#Ds\Map::isEmpty) — Returns
        whether the map is empty
    -   [Ds\\Map::jsonSerialize](/class/ds-map.html#Ds\Map::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\Map::keys](/class/ds-map.html#Ds\Map::keys) — Returns a set
        of the map's keys
    -   [Ds\\Map::ksort](/class/ds-map.html#Ds\Map::ksort) — Sorts the
        map in-place by key
    -   [Ds\\Map::ksorted](/class/ds-map.html#Ds\Map::ksorted) — Returns
        a copy, sorted by key
    -   [Ds\\Map::last](/class/ds-map.html#Ds\Map::last) — Returns the
        last pair of the map
    -   [Ds\\Map::map](/class/ds-map.html#Ds\Map::map) — Returns the
        result of applying a callback to each value
    -   [Ds\\Map::merge](/class/ds-map.html#Ds\Map::merge) — Returns the
        result of adding all given associations
    -   [Ds\\Map::pairs](/class/ds-map.html#Ds\Map::pairs) — Returns a
        sequence containing all the pairs of the map
    -   [Ds\\Map::put](/class/ds-map.html#Ds\Map::put) — Associates a
        key with a value
    -   [Ds\\Map::putAll](/class/ds-map.html#Ds\Map::putAll) —
        Associates all key-value pairs of a traversable object or array
    -   [Ds\\Map::reduce](/class/ds-map.html#Ds\Map::reduce) — Reduces
        the map to a single value using a callback function
    -   [Ds\\Map::remove](/class/ds-map.html#Ds\Map::remove) — Removes
        and returns a value by key
    -   [Ds\\Map::reverse](/class/ds-map.html#Ds\Map::reverse) —
        Reverses the map in-place
    -   [Ds\\Map::reversed](/class/ds-map.html#Ds\Map::reversed) —
        Returns a reversed copy
    -   [Ds\\Map::skip](/class/ds-map.html#Ds\Map::skip) — Returns the
        pair at a given positional index
    -   [Ds\\Map::slice](/class/ds-map.html#Ds\Map::slice) — Returns a
        subset of the map defined by a starting index and length
    -   [Ds\\Map::sort](/class/ds-map.html#Ds\Map::sort) — Sorts the map
        in-place by value
    -   [Ds\\Map::sorted](/class/ds-map.html#Ds\Map::sorted) — Returns a
        copy, sorted by value
    -   [Ds\\Map::sum](/class/ds-map.html#Ds\Map::sum) — Returns the sum
        of all values in the map
    -   [Ds\\Map::toArray](/class/ds-map.html#Ds\Map::toArray) —
        Converts the map to an array
    -   [Ds\\Map::union](/class/ds-map.html#Ds\Map::union) — Creates a
        new map using values from the current instance and another map
    -   [Ds\\Map::values](/class/ds-map.html#Ds\Map::values) — Returns a
        sequence of the map's values
    -   [Ds\\Map::xor](/class/ds-map.html#Ds\Map::xor) — Creates a new
        map using keys of either the current instance or of another map,
        but not of both
-   [Pair](/class/ds-pair.html) — The Pair class
    -   [Ds\\Pair::clear](/class/ds-pair.html#Ds\Pair::clear) — Removes
        all values
    -   [Ds\\Pair::\_\_construct](/class/ds-pair.html#Ds\Pair::__construct)
        — Creates a new instance
    -   [Ds\\Pair::copy](/class/ds-pair.html#Ds\Pair::copy) — Returns a
        shallow copy of the pair
    -   [Ds\\Pair::isEmpty](/class/ds-pair.html#Ds\Pair::isEmpty) —
        Returns whether the pair is empty
    -   [Ds\\Pair::jsonSerialize](/class/ds-pair.html#Ds\Pair::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\Pair::toArray](/class/ds-pair.html#Ds\Pair::toArray) —
        Converts the pair to an array
-   [Set](/class/ds-set.html) — The Set class
    -   [Ds\\Set::add](/class/ds-set.html#Ds\Set::add) — Adds values to
        the set
    -   [Ds\\Set::allocate](/class/ds-set.html#Ds\Set::allocate) —
        Allocates enough memory for a required capacity
    -   [Ds\\Set::capacity](/class/ds-set.html#Ds\Set::capacity) —
        Returns the current capacity
    -   [Ds\\Set::clear](/class/ds-set.html#Ds\Set::clear) — Removes all
        values
    -   [Ds\\Set::\_\_construct](/class/ds-set.html#Ds\Set::__construct)
        — Creates a new instance
    -   [Ds\\Set::contains](/class/ds-set.html#Ds\Set::contains) —
        Determines if the set contains all values
    -   [Ds\\Set::copy](/class/ds-set.html#Ds\Set::copy) — Returns a
        shallow copy of the set
    -   [Ds\\Set::count](/class/ds-set.html#Ds\Set::count) — Returns the
        number of values in the set
    -   [Ds\\Set::diff](/class/ds-set.html#Ds\Set::diff) — Creates a new
        set using values that aren't in another set
    -   [Ds\\Set::filter](/class/ds-set.html#Ds\Set::filter) — Creates a
        new set using a callable to determine which values to include
    -   [Ds\\Set::first](/class/ds-set.html#Ds\Set::first) — Returns the
        first value in the set
    -   [Ds\\Set::get](/class/ds-set.html#Ds\Set::get) — Returns the
        value at a given index
    -   [Ds\\Set::intersect](/class/ds-set.html#Ds\Set::intersect) —
        Creates a new set by intersecting values with another set
    -   [Ds\\Set::isEmpty](/class/ds-set.html#Ds\Set::isEmpty) — Returns
        whether the set is empty
    -   [Ds\\Set::join](/class/ds-set.html#Ds\Set::join) — Joins all
        values together as a string
    -   [Ds\\Set::jsonSerialize](/class/ds-set.html#Ds\Set::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\Set::last](/class/ds-set.html#Ds\Set::last) — Returns the
        last value in the set
    -   [Ds\\Set::merge](/class/ds-set.html#Ds\Set::merge) — Returns the
        result of adding all given values to the set
    -   [Ds\\Set::reduce](/class/ds-set.html#Ds\Set::reduce) — Reduces
        the set to a single value using a callback function
    -   [Ds\\Set::remove](/class/ds-set.html#Ds\Set::remove) — Removes
        all given values from the set
    -   [Ds\\Set::reverse](/class/ds-set.html#Ds\Set::reverse) —
        Reverses the set in-place
    -   [Ds\\Set::reversed](/class/ds-set.html#Ds\Set::reversed) —
        Returns a reversed copy
    -   [Ds\\Set::slice](/class/ds-set.html#Ds\Set::slice) — Returns a
        sub-set of a given range
    -   [Ds\\Set::sort](/class/ds-set.html#Ds\Set::sort) — Sorts the set
        in-place
    -   [Ds\\Set::sorted](/class/ds-set.html#Ds\Set::sorted) — Returns a
        sorted copy
    -   [Ds\\Set::sum](/class/ds-set.html#Ds\Set::sum) — Returns the sum
        of all values in the set
    -   [Ds\\Set::toArray](/class/ds-set.html#Ds\Set::toArray) —
        Converts the set to an array
    -   [Ds\\Set::union](/class/ds-set.html#Ds\Set::union) — Creates a
        new set using values from the current instance and another set
    -   [Ds\\Set::xor](/class/ds-set.html#Ds\Set::xor) — Creates a new
        set using values in either the current instance or in another
        set, but not in both
-   [Stack](/class/ds-stack.html) — The Stack class
    -   [Ds\\Stack::allocate](/class/ds-stack.html#Ds\Stack::allocate) —
        Allocates enough memory for a required capacity
    -   [Ds\\Stack::capacity](/class/ds-stack.html#Ds\Stack::capacity) —
        Returns the current capacity
    -   [Ds\\Stack::clear](/class/ds-stack.html#Ds\Stack::clear) —
        Removes all values
    -   [Ds\\Stack::\_\_construct](/class/ds-stack.html#Ds\Stack::__construct)
        — Creates a new instance
    -   [Ds\\Stack::copy](/class/ds-stack.html#Ds\Stack::copy) — Returns
        a shallow copy of the stack
    -   [Ds\\Stack::count](/class/ds-stack.html#Ds\Stack::count) —
        Returns the number of values in the stack
    -   [Ds\\Stack::isEmpty](/class/ds-stack.html#Ds\Stack::isEmpty) —
        Returns whether the stack is empty
    -   [Ds\\Stack::jsonSerialize](/class/ds-stack.html#Ds\Stack::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\Stack::peek](/class/ds-stack.html#Ds\Stack::peek) — Returns
        the value at the top of the stack
    -   [Ds\\Stack::pop](/class/ds-stack.html#Ds\Stack::pop) — Removes
        and returns the value at the top of the stack
    -   [Ds\\Stack::push](/class/ds-stack.html#Ds\Stack::push) — Pushes
        values onto the stack
    -   [Ds\\Stack::toArray](/class/ds-stack.html#Ds\Stack::toArray) —
        Converts the stack to an array
-   [Queue](/class/ds-queue.html) — The Queue class
    -   [Ds\\Queue::allocate](/class/ds-queue.html#Ds\Queue::allocate) —
        Allocates enough memory for a required capacity
    -   [Ds\\Queue::capacity](/class/ds-queue.html#Ds\Queue::capacity) —
        Returns the current capacity
    -   [Ds\\Queue::clear](/class/ds-queue.html#Ds\Queue::clear) —
        Removes all values
    -   [Ds\\Queue::\_\_construct](/class/ds-queue.html#Ds\Queue::__construct)
        — Creates a new instance
    -   [Ds\\Queue::copy](/class/ds-queue.html#Ds\Queue::copy) — Returns
        a shallow copy of the queue
    -   [Ds\\Queue::count](/class/ds-queue.html#Ds\Queue::count) —
        Returns the number of values in the queue
    -   [Ds\\Queue::isEmpty](/class/ds-queue.html#Ds\Queue::isEmpty) —
        Returns whether the queue is empty
    -   [Ds\\Queue::jsonSerialize](/class/ds-queue.html#Ds\Queue::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\Queue::peek](/class/ds-queue.html#Ds\Queue::peek) — Returns
        the value at the front of the queue
    -   [Ds\\Queue::pop](/class/ds-queue.html#Ds\Queue::pop) — Removes
        and returns the value at the front of the queue
    -   [Ds\\Queue::push](/class/ds-queue.html#Ds\Queue::push) — Pushes
        values into the queue
    -   [Ds\\Queue::toArray](/class/ds-queue.html#Ds\Queue::toArray) —
        Converts the queue to an array
-   [PriorityQueue](/class/ds-priorityqueue.html) — The PriorityQueue
    class
    -   [Ds\\PriorityQueue::allocate](/class/ds-priorityqueue.html#Ds\PriorityQueue::allocate)
        — Allocates enough memory for a required capacity
    -   [Ds\\PriorityQueue::capacity](/class/ds-priorityqueue.html#Ds\PriorityQueue::capacity)
        — Returns the current capacity
    -   [Ds\\PriorityQueue::clear](/class/ds-priorityqueue.html#Ds\PriorityQueue::clear)
        — Removes all values
    -   [Ds\\PriorityQueue::\_\_construct](/class/ds-priorityqueue.html#Ds\PriorityQueue::__construct)
        — Creates a new instance
    -   [Ds\\PriorityQueue::copy](/class/ds-priorityqueue.html#Ds\PriorityQueue::copy)
        — Returns a shallow copy of the queue
    -   [Ds\\PriorityQueue::count](/class/ds-priorityqueue.html#Ds\PriorityQueue::count)
        — Returns the number of values in the queue
    -   [Ds\\PriorityQueue::isEmpty](/class/ds-priorityqueue.html#Ds\PriorityQueue::isEmpty)
        — Returns whether the queue is empty
    -   [Ds\\PriorityQueue::jsonSerialize](/class/ds-priorityqueue.html#Ds\PriorityQueue::jsonSerialize)
        — Returns a representation that can be converted to JSON
    -   [Ds\\PriorityQueue::peek](/class/ds-priorityqueue.html#Ds\PriorityQueue::peek)
        — Returns the value at the front of the queue
    -   [Ds\\PriorityQueue::pop](/class/ds-priorityqueue.html#Ds\PriorityQueue::pop)
        — Removes and returns the value with the highest priority
    -   [Ds\\PriorityQueue::push](/class/ds-priorityqueue.html#Ds\PriorityQueue::push)
        — Pushes values into the queue
    -   [Ds\\PriorityQueue::toArray](/class/ds-priorityqueue.html#Ds\PriorityQueue::toArray)
        — Converts the queue to an array

简介
----

<span class="classname">Collection</span> is the base interface which
covers functionality common to all the data structures in this library.
It guarantees that all structures are traversable, countable, and can be
converted to json using <span class="function">json\_encode</span>.

接口摘要
--------

**Ds\\Collection**

<span class="ooclass"> class **Ds\\Collection**</span> <span
class="oointerface">implements <span
class="interfacename">Traversable</span></span> <span
class="oointerface">, <span
class="interfacename">Countable</span></span> <span
class="oointerface">, <span
class="interfacename">JsonSerializable</span></span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">clear</span> ( <span class="methodparam">void</span>
)

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Collection</span>
<span class="methodname">copy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

}

Ds\\Collection::clear
=====================

Removes all values

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Collection::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the collection.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Collection::clear</span> example**

``` php
<?php
$collection = new \Ds\Vector([1, 2, 3]);
print_r($collection);

$collection->clear();
print_r($collection);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Vector Object
    (
    )

Ds\\Collection::copy
====================

Returns a shallow copy of the collection

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Collection</span>
<span class="methodname">Ds\\Collection::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the collection.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the collection.

### 范例

**示例 \#1 <span class="function">Ds\\Collection::copy</span> example**

``` php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = $a->copy();

$b->push(4);

print_r($a);
print_r($b);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
    )

Ds\\Collection::isEmpty
=======================

Returns whether the collection is empty

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Ds\\Collection::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the collection is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the collection is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Collection::isEmpty</span>
example**

``` php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = new \Ds\Vector();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Collection::toArray
=======================

Converts the collection to an <span class="type">array</span>

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">array</span> <span
class="methodname">Ds\\Collection::toArray</span> ( <span
class="methodparam">void</span> )

Converts the collection to an <span class="type">array</span>.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the collection.

### 范例

**示例 \#1 <span class="function">Ds\\Collection::toArray</span>
example**

``` php
<?php
$collection = new \Ds\Vector([1, 2, 3]);

var_dump($collection->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

简介
----

Hashable is an interface which allows objects to be used as keys. It’s
an alternative to <span class="function">spl\_object\_hash</span>, which
determines an object’s hash based on its handle: this means that two
objects that are considered equal by an implicit definition would not
treated as equal because they are not the same instance.

<span class="function">hash</span> is used to return a scalar value to
be used as the object's hash value, which determines where it goes in
the hash table. While this value does not have to be unique, objects
which are equal must have the same hash value.

<span class="function">equals</span> is used to determine if two objects
are equal. It's guaranteed that the comparing object will be an instance
of the same class as the subject.

接口摘要
--------

**Ds\\Hashable**

<span class="ooclass"> class **Ds\\Hashable** </span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">equals</span> ( <span class="methodparam"><span
class="type">object</span> `$obj`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">hash</span> ( <span class="methodparam">void</span> )

}

Ds\\Hashable::equals
====================

Determines whether an object is equal to the current instance

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Ds\\Hashable::equals</span> ( <span
class="methodparam"><span class="type">object</span> `$obj`</span> )

Determines whether another object is equal to the current instance.

This method allows objects to be used as keys in structures such as
<span class="classname">Ds\\Map</span> and <span
class="classname">Ds\\Set</span>, or any other lookup structure that
honors this interface.

> **Note**:
>
> It's guaranteed that `obj` is an instance of the same class.

**Caution**

It's important that objects which are equal also have the same hash
value. See <span class="function">Ds\\Hashable::hash</span>.

### 参数

`obj`  
The object to compare the current instance to, which is always an
instance of the same class.

### 返回值

**`TRUE`** if equal, **`FALSE`** otherwise.

Ds\\Hashable::hash
==================

Returns a scalar value to be used as a hash value

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Hashable::hash</span> ( <span
class="methodparam">void</span> )

Returns a scalar value to be used as the hash value of the objects.

While the hash value does not define equality, all objects that are
equal according to <span class="function">Ds\\Hashable::equals</span>
must have the same hash value. Hash values of equal objects don't have
to be unique, for example you could just return **`TRUE`** for all
objects and nothing would break - the only implication would be that
hash tables then turn into linked lists because all your objects will be
hashed to the same bucket. It's therefore very important that you pick a
good hash value, such as an ID or email address.

This method allows objects to be used as keys in structures such as
<span class="classname">Ds\\Map</span> and <span
class="classname">Ds\\Set</span>, or any other lookup structure that
honors this interface.

**Caution**

Do not pick a value that might change within the object, such as a
public property. Hash table lookups would fail because the hash has
changed.

**Caution**

All objects that are equal must have the same hash value.

### 参数

此函数没有参数。

### 返回值

A scalar value to be used as this object's hash value.

### 范例

**示例 \#1 <span class="function">Ds\\Hashable::hash</span> example**

``` php
<?php
class HashableObject implements \Ds\Hashable
{
    private $name;
    private $email;

    public function __construct($name, $email)
    {
        $this->name  = $name;
        $this->email = $email;
    }

    /**
     * Should return the same value for all equal objects, but doesn't have to
     * be unique. This value will not be used to determine equality.
     */
    public function hash()
    {
        return $this->email;
    }

    /**
     * This determines equality, usually during a hash table lookup to determine
     * if the bucket's key matches the lookup key. The hash has to be equal if
     * the objects are equal, otherwise this determination wouldn't be reached.
     */
    public function equals($obj): bool
    {
        return $this->name  === $obj->name
            && $this->email === $obj->email;
    }
}
?>
```

简介
----

A Sequence describes the behaviour of values arranged in a single,
linear dimension. Some languages refer to this as a "List". It’s similar
to an array that uses incremental integer keys, with the exception of a
few characteristics:

-   Values will always be indexed as \[0, 1, 2, …, size - 1\].
-   Only allowed to access values by index in the range \[0, size - 1\].

Use cases:

-   Wherever you would use an array as a list (not concerned with keys).
-   A more efficient alternative to <span
    class="classname">SplDoublyLinkedList</span> and <span
    class="classname">SplFixedArray</span>.

接口摘要
--------

**Ds\\Sequence**

<span class="ooclass"> class **Ds\\Sequence**</span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Collection</span></span> {

/\* 方法 \*/

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">allocate</span> ( <span class="methodparam"><span
class="type">int</span> `$capacity`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">apply</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">contains</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$...values`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">find</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">first</span> ( <span class="methodparam">void</span>
)

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">get</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">insert</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">join</span> (\[ <span class="methodparam"><span
class="type">string</span> `$glue`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">last</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">map</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">mixed</span> `$values`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">pop</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">push</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$...values`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">reduce</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$initial`</span> \]
)

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">remove</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">reverse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">reversed</span> ( <span
class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">rotate</span> ( <span class="methodparam"><span
class="type">int</span> `$rotations`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">shift</span> ( <span class="methodparam">void</span>
)

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">slice</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">sort</span> (\[ <span class="methodparam"><span
class="type">callable</span> `$comparator`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">number</span> <span
class="methodname">sum</span> ( <span class="methodparam">void</span> )

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">unshift</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$values`</span> \] )

}

Ds\\Sequence::allocate
======================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Ensures that enough memory is allocated for a required capacity. This
removes the need to reallocate the internal as values are added.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::allocate</span>
example**

``` php
<?php
$sequence = new \Ds\Vector();
var_dump($sequence->capacity());

$vector->allocate(100);
var_dump($sequence->capacity());
?>
```

以上例程的输出类似于：

    int(10)
    int(100)

Ds\\Sequence::apply
===================

Updates all values by applying a callback function to each value

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::apply</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Updates all values by applying a `callback` function to each value in
the sequence.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

A <span class="type">callable</span> to apply to each value in the
sequence.

The callback should return what the value should be replaced by.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::apply</span> example**

``` php
<?php
$sequence = new \Ds\Sequence([1, 2, 3]);
$sequence->apply(function($value) { return $value * 2; });

print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 2
        [1] => 4
        [2] => 6
    )

Ds\\Sequence::capacity
======================

Returns the current capacity

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\Sequence::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::capacity</span>
example**

``` php
<?php
$sequence = new \Ds\Vector();
var_dump($sequence->capacity());

$sequence->push(...range(1, 50));
var_dump($sequence->capacity());

$sequence[] = "a";
var_dump($sequence->capacity());
?>
```

以上例程的输出类似于：

    int(10)
    int(50)
    int(75)

Ds\\Sequence::contains
======================

Determines if the sequence contains given values

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Ds\\Sequence::contains</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Determines if the sequence contains all values.

### 参数

`values`  
Values to check.

### 返回值

**`FALSE`** if any of the provided `values` are not in the sequence,
**`TRUE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::contains</span>
example**

``` php
<?php
$sequence = new \Ds\Vector(['a', 'b', 'c', 1, 2, 3]);

var_dump($sequence->contains('a'));                // true
var_dump($sequence->contains('a', 'b'));           // true
var_dump($sequence->contains('c', 'd'));           // false

var_dump($sequence->contains(...['c', 'b', 'a'])); // true

// Always strict
var_dump($sequence->contains(1));                  // true
var_dump($sequence->contains('1'));                // false

var_dump($sequece->contains(...[]));               // true
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(false)
    bool(true)
    bool(true)
    bool(false)
    bool(true)

Ds\\Sequence::filter
====================

Creates a new sequence using a <span class="type">callable</span> to
determine which values to include

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">Ds\\Sequence::filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

Creates a new sequence using a <span class="type">callable</span> to
determine which values to include.

### 参数

`callback`  
<span class="type">bool</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Optional <span class="type">callable</span> which returns **`TRUE`** if
the value should be included, **`FALSE`** otherwise.

If a callback is not provided, only values which are **`TRUE`** (see
<a href="/language/types/boolean.html#language.types.boolean.casting" class="link">converting to boolean</a>)
will be included.

### 返回值

A new sequence containing all the values for which either the `callback`
returned **`TRUE`**, or all values that convert to **`TRUE`** if a
`callback` was not provided.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::filter</span> example
using callback function**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3, 4, 5]);

var_dump($sequence->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#3 (2) {
      [0]=>
      int(2)
      [1]=>
      int(4)
    }

**示例 \#2 <span class="function">Ds\\Sequence::filter</span> example
without a callback function**

``` php
<?php
$sequence = new \Ds\Vector([0, 1, 'a', true, false]);

var_dump($sequence->filter());
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      string(1) "a"
      [2]=>
      bool(true)
    }

Ds\\Sequence::find
==================

Attempts to find a value's index

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::find</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Returns the index of the `value`, or **`FALSE`** if not found.

### 参数

`value`  
The value to find.

### 返回值

The index of the value, or **`FALSE`** if not found.

> **Note**:
>
> Values will be compared by value and by type.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::find</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", 1, true]);

var_dump($sequence->find("a")); // 0
var_dump($sequence->find("b")); // false
var_dump($sequence->find("1")); // false
var_dump($sequence->find(1));   // 1
?>
```

以上例程的输出类似于：

    int(0)
    bool(false)
    bool(false)
    int(1)

Ds\\Sequence::first
===================

Returns the first value in the sequence

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::first</span> ( <span
class="methodparam">void</span> )

Returns the first value in the sequence.

### 参数

此函数没有参数。

### 返回值

The first value in the sequence.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::first</span> example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->first());
?>
```

以上例程的输出类似于：

    int(1)

Ds\\Sequence::get
=================

Returns the value at a given index

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::get</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Returns the value at a given index.

### 参数

`index`  
The index to access, starting at 0.

### 返回值

The value at the requested index.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::get</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->get(0));
var_dump($sequence->get(1));
var_dump($sequence->get(2));
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

**示例 \#2 <span class="function">Ds\\Sequence::get</span> example using
array syntax**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence[0]);
var_dump($sequence[1]);
var_dump($sequence[2]);
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Sequence::insert
====================

Inserts values at a given index

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::insert</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$...values`</span> \] )

Inserts values into the sequence at a given index.

### 参数

`index`  
The index at which to insert. `0 <= index <= count`

> **Note**:
>
> You can insert at the index equal to the number of values.

`values`  
The value or values to insert.

### 返回值

没有返回值。

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::insert</span> example**

``` php
<?php
$sequence = new \Ds\Vector();

$sequence->insert(0, "e");             // [e]
$sequence->insert(1, "f");             // [e, f]
$sequence->insert(2, "g");             // [e, f, g]
$sequence->insert(0, "a", "b");        // [a, b, e, f, g]
$sequence->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($sequence);
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#1 (7) {
      [0]=>
      string(1) "a"
      [1]=>
      string(1) "b"
      [2]=>
      string(1) "c"
      [3]=>
      string(1) "d"
      [4]=>
      string(1) "e"
      [5]=>
      string(1) "f"
      [6]=>
      string(1) "g"
    }

Ds\\Sequence::join
==================

Joins all values together as a string

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">Ds\\Sequence::join</span> (\[ <span
class="methodparam"><span class="type">string</span> `$glue`</span> \] )

Joins all values together as a string using an optional separator
between each value.

### 参数

`glue`  
An optional string to separate each value.

### 返回值

All values of the sequence joined together as a string.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::join</span> example
using a separator string**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join("|"));
?>
```

以上例程的输出类似于：

    string(11) "a|b|c|1|2|3"

**示例 \#2 <span class="function">Ds\\Sequence::join</span> example
without a separator string**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join());
?>
```

以上例程的输出类似于：

    string(11) "abc123"

Ds\\Sequence::last
==================

Returns the last value

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::last</span> ( <span
class="methodparam">void</span> )

Returns the last value in the sequence.

### 参数

此函数没有参数。

### 返回值

The last value in the sequence.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::last</span> example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->last());
?>
```

以上例程的输出类似于：

    int(3)

Ds\\Sequence::map
=================

Returns the result of applying a callback to each value

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">Ds\\Sequence::map</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Returns the result of applying a `callback` function to each value in
the sequence.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

A <span class="type">callable</span> to apply to each value in the
sequence.

The callable should return what the new value will be in the new
sequence.

### 返回值

The result of applying a `callback` to each value in the sequence.

> **Note**:
>
> The values of the current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::map</span> example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

print_r($sequence->map(function($value) { return $value * 2; }));
print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 2
        [1] => 4
        [2] => 6
    )
    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )

Ds\\Sequence::merge
===================

Returns the result of adding all given values to the sequence

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">Ds\\Sequence::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$values`</span> )

Returns the result of adding all given values to the sequence.

### 参数

`values`  
A <span class="classname">traversable</span> object or an <span
class="type">array</span>.

### 返回值

The result of adding all given values to the sequence, effectively the
same as adding the values to a copy, then returning that copy.

> **Note**:
>
> The current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::merge</span> example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->merge([4, 5, 6]));
var_dump($sequence);
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#2 (6) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
      [3]=>
      int(4)
      [4]=>
      int(5)
      [5]=>
      int(6)
    }
    object(Ds\Vector)#1 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Sequence::pop
=================

Removes and returns the last value

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::pop</span> ( <span
class="methodparam">void</span> )

Removes and returns the last value.

### 参数

此函数没有参数。

### 返回值

The removed last value.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::pop</span> example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->pop());
var_dump($sequence->pop());
var_dump($sequence->pop());
?>
```

以上例程的输出类似于：

    int(3)
    int(2)
    int(1)

Ds\\Sequence::push
==================

Adds values to the end of the sequence

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::push</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Adds values to the end of the sequence.

### 参数

`values`  
The values to add.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::push</span> example**

``` php
<?php
$sequence = new \Ds\Vector();

$sequence->push("a");
$sequence->push("b");
$sequence->push("c", "d");
$sequence->push(...["e", "f"]);

print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => a
        [1] => b
        [2] => c
        [3] => d
        [4] => e
        [5] => f
    )

Ds\\Sequence::reduce
====================

Reduces the sequence to a single value using a callback function

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::reduce</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$initial`</span> \] )

Reduces the sequence to a single value using a callback function.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$carry`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

`carry`  
The return value of the previous callback, or `initial` if it's the
first iteration.

`value`  
The value of the current iteration.

`initial`  
The initial value of the carry value. Can be **`NULL`**.

### 返回值

The return value of the final callback.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::reduce</span> with
initial value example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($sequence->reduce($callback, 5));

// Iterations:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

以上例程的输出类似于：

    int(30)

**示例 \#2 <span class="function">Ds\\Sequence::reduce</span> without an
initial value example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->reduce(function($carry, $value) {
    return $carry + $value + 5;
}));

// Iterations:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

以上例程的输出类似于：

    int(21)

Ds\\Sequence::remove
====================

Removes and returns a value by index

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::remove</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Removes and returns a value by index.

### 参数

`index`  
The index of the value to remove.

### 返回值

The value that was removed.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::remove</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->remove(1));
var_dump($sequence->remove(0));
var_dump($sequence->remove(0));
?>
```

以上例程的输出类似于：

    string(1) "b"
    string(1) "a"
    string(1) "c"

Ds\\Sequence::reverse
=====================

Reverses the sequence in-place

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::reverse</span> ( <span
class="methodparam">void</span> )

Reverses the sequence in-place.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::reverse</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);
$sequence->reverse();

print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => c
        [1] => b
        [2] => a
    )

Ds\\Sequence::reversed
======================

Returns a reversed copy

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">Ds\\Sequence::reversed</span> ( <span
class="methodparam">void</span> )

Returns a reversed copy of the sequence.

### 参数

此函数没有参数。

### 返回值

A reversed copy of the sequence.

> **Note**:
>
> The current instance is not affected.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::reversed</span>
example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

print_r($sequence->reversed());
print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => c
        [1] => b
        [2] => a
    )
    Ds\Vector Object
    (
        [0] => a
        [1] => b
        [2] => c
    )

Ds\\Sequence::rotate
====================

Rotates the sequence by a given number of rotations

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::rotate</span> ( <span
class="methodparam"><span class="type">int</span> `$rotations`</span> )

Rotates the sequence by a given number of rotations, which is equivalent
to successively calling `$sequence->push($sequence->shift())` if the
number of rotations is positive, or
`$sequence->unshift($sequence->pop())` if negative.

### 参数

`rotations`  
The number of times the sequence should be rotated.

### 返回值

没有返回值。. The sequence of the current instance will be rotated.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::rotate</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", "d"]);

$sequence->rotate(1);  // "a" is shifted, then pushed.
print_r($sequence);

$sequence->rotate(2);  // "b" and "c" are both shifted, the pushed.
print_r($sequence);
?>
```

以上例程的输出类似于：

    (
        [0] => b
        [1] => c
        [2] => d
        [3] => a
    )
    Ds\Vector Object
    (
        [0] => d
        [1] => a
        [2] => b
        [3] => c
    )

Ds\\Sequence::set
=================

Updates a value at a given index

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::set</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Updates a value at a given index.

### 参数

`index`  
The index of the value to update.

`value`  
The new value.

### 返回值

没有返回值。

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::set</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

$sequence->set(1, "_");
print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => a
        [1] => _
        [2] => c
    )

**示例 \#2 <span class="function">Ds\\Sequence::set</span> example using
array syntax**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

$sequence[1] = "_";
print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => a
        [1] => _
        [2] => c
    )

Ds\\Sequence::shift
===================

Removes and returns the first value

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Ds\\Sequence::shift</span> ( <span
class="methodparam">void</span> )

Removes and returns the first value.

### 参数

此函数没有参数。

### 返回值

The first value, which was removed.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::shift</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->shift());
var_dump($sequence->shift());
var_dump($sequence->shift());
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Sequence::slice
===================

Returns a sub-sequence of a given range

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">Ds\\Sequence::slice</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\] )

Creates a sub-sequence of a given range.

### 参数

`index`  
The index at which the sub-sequence starts.

If positive, the sequence will start at that index in the sequence. If
negative, the sequence will start that far from the end.

`length`  
If a length is given and is positive, the resulting sequence will have
up to that many values in it. If the length results in an overflow, only
values up to the end of the sequence will be included. If a length is
given and is negative, the sequence will stop that many values from the
end. If a length is not provided, the resulting sequence will contain
all values between the index and the end of the sequence.

### 返回值

A sub-sequence of the given range.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::slice</span> example**

``` php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", "d", "e"]);

// Slice from 2 onwards
print_r($sequence->slice(2));

// Slice from 1, for a length of 3
print_r($sequence->slice(1, 3));

// Slice from 1 onwards
print_r($sequence->slice(1));

// Slice from 2 from the end onwards
print_r($sequence->slice(-2));

// Slice from 1 to 1 from the end
print_r($sequence->slice(1, -1));
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => c
        [1] => d
        [2] => e
    )
    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => d
    )
    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => d
        [3] => e
    )
    Ds\Vector Object
    (
        [0] => d
        [1] => e
    )
    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => d
    )

Ds\\Sequence::sort
==================

Sorts the sequence in-place

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::sort</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Sorts the sequence in-place, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::sort</span> example**

``` php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);
$sequence->sort();

print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Sequence::sort</span> example
using a comparator**

``` php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);

$sequence->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Sequence::sorted
====================

Returns a sorted copy

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">Ds\\Sequence</span>
<span class="methodname">Ds\\Sequence::sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Returns a sorted copy, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

Returns a sorted copy of the sequence.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::sorted</span> example**

``` php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);

print_r($sequence->sorted());
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Sequence::sorted</span> example
using a comparator**

``` php
<?php
$sequence = new \Ds\Vector([4, 5, 1, 3, 2]);

$sorted = $sequence->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Sequence::sum
=================

Returns the sum of all values in the sequence

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">number</span> <span
class="methodname">Ds\\Sequence::sum</span> ( <span
class="methodparam">void</span> )

Returns the sum of all values in the sequence.

> **Note**:
>
> Arrays and objects are considered equal to zero when calculating the
> sum.

### 参数

此函数没有参数。

### 返回值

The sum of all the values in the sequence as either a <span
class="type">float</span> or <span class="type">int</span> depending on
the values in the sequence.

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::sum</span> integer
example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->sum());
?>
```

以上例程的输出类似于：

    int(6)

**示例 \#2 <span class="function">Ds\\Sequence::sum</span> float
example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2.5, 3]);
var_dump($sequence->sum());
?>
```

以上例程的输出类似于：

    float(6.5)

Ds\\Sequence::unshift
=====================

Adds values to the front of the sequence

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">Ds\\Sequence::unshift</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

Adds values to the front of the sequence, moving all the current values
forward to make room for the new values.

### 参数

`values`  
The values to add to the front of the sequence.

> **Note**:
>
> Multiple values will be added in the same order that they are passed.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Sequence::unshift</span> example**

``` php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

$sequence->unshift("a");
$sequence->unshift("b", "c");

print_r($sequence);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => a
        [3] => 1
        [4] => 2
        [5] => 3
    )

简介
----

A Vector is a sequence of values in a contiguous buffer that grows and
shrinks automatically. It’s the most efficient sequential structure
because a value’s index is a direct mapping to its index in the buffer,
and the growth factor isn't bound to a specific multiple or exponent.

Strengths
---------

-   Supports array syntax (square brackets).
-   Uses less overall memory than an <span class="type">array</span> for
    the same number of values.
-   Automatically frees allocated memory when its size drops low enough.
-   Capacity does not have to be a power of 2.
-   <span class="function">get</span>, <span
    class="function">set</span>, <span class="function">push</span>,
    <span class="function">pop</span> are all O(1).

Weaknesses
----------

-   <span class="function">shift</span>, <span
    class="function">unshift</span>, <span
    class="function">insert</span> and <span
    class="function">remove</span> are all O(n).

类摘要
------

**Ds\\Vector**

<span class="ooclass"> class **Ds\\Vector**</span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Sequence</span></span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Ds\Vector::MIN_CAPACITY` <span class="initializer"> = 10</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">apply</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">contains</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span class="methodname">copy</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span class="methodname">filter</span>
(\[ <span class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">find</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">first</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">insert</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">join</span> (\[ <span class="methodparam"><span
class="type">string</span> `$glue`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">last</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span class="methodname">map</span> (
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span class="methodname">merge</span> (
<span class="methodparam"><span class="type">mixed</span>
`$values`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$...values`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">reduce</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$initial`</span> \]
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">remove</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">reverse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span class="methodname">reversed</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rotate</span> ( <span class="methodparam"><span
class="type">int</span> `$rotations`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">shift</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span class="methodname">slice</span> (
<span class="methodparam"><span class="type">int</span> `$index`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$length`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sort</span> (\[ <span class="methodparam"><span
class="type">callable</span> `$comparator`</span> \] )

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span class="methodname">sorted</span>
(\[ <span class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">sum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unshift</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

}

预定义常量
----------

**`Ds\Vector::MIN_CAPACITY`**  

Ds\\Vector::allocate
====================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Ensures that enough memory is allocated for a required capacity. This
removes the need to reallocate the internal as values are added.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Vector::allocate</span> example**

``` php
<?php
$vector = new \Ds\Vector();
var_dump($vector->capacity());

$vector->allocate(100);
var_dump($vector->capacity());
?>
```

以上例程的输出类似于：

    int(10)
    int(100)

Ds\\Vector::apply
=================

Updates all values by applying a callback function to each value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::apply</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Updates all values by applying a `callback` function to each value in
the vector.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

A <span class="type">callable</span> to apply to each value in the
vector.

The callback should return what the value should be replaced by.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Vector::apply</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
$vector->apply(function($value) { return $value * 2; });

print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 2
        [1] => 4
        [2] => 6
    )

Ds\\Vector::capacity
====================

Returns the current capacity

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\Vector::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::capacity</span> example**

``` php
<?php
$vector = new \Ds\Vector();
var_dump($vector->capacity());

$vector->push(...range(1, 50));
var_dump($vector->capacity());

$vector[] = "a";
var_dump($vector->capacity());
?>
```

以上例程的输出类似于：

    int(10)
    int(50)
    int(75)

Ds\\Vector::clear
=================

Removes all values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the vector.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Vector::clear</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
print_r($vector);

$vector->clear();
print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Vector Object
    (
    )

Ds\\Vector::\_\_construct
=========================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\Vector::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

Creates a new instance, using either a <span
class="classname">traversable</span> object or an <span
class="type">array</span> for the initial `values`.

### 参数

`values`  
A traversable object or an <span class="type">array</span> to use for
the initial values.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::\_\_construct</span>
example**

``` php
<?php
$vector = new \Ds\Vector();
var_dump($vector);


$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector);
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#2 (0) {
    }
    object(Ds\Vector)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Vector::contains
====================

Determines if the vector contains given values

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Vector::contains</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Determines if the vector contains all values.

### 参数

`values`  
Values to check.

### 返回值

**`FALSE`** if any of the provided `values` are not in the vector,
**`TRUE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::contains</span> example**

``` php
<?php
$vector = new \Ds\Vector(['a', 'b', 'c', 1, 2, 3]);

var_dump($vector->contains('a'));                // true
var_dump($vector->contains('a', 'b'));           // true
var_dump($vector->contains('c', 'd'));           // false

var_dump($vector->contains(...['c', 'b', 'a'])); // true

// Always strict
var_dump($vector->contains(1));                  // true
var_dump($vector->contains('1'));                // false

var_dump($sequece->contains(...[]));               // true
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(false)
    bool(true)
    bool(true)
    bool(false)
    bool(true)

Ds\\Vector::copy
================

Returns a shallow copy of the vector

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span
class="methodname">Ds\\Vector::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the vector.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the vector.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::copy</span> example**

``` php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = $a->copy();

// Updating the copy doesn't affect the original
$b->push(4);

print_r($a);
print_r($b);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
    )

Ds\\Vector::count
=================

Returns the number of values in the collection

See <span class="function">Countable::count</span>

Ds\\Vector::filter
==================

Creates a new vector using a <span class="type">callable</span> to
determine which values to include

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span
class="methodname">Ds\\Vector::filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

Creates a new vector using a <span class="type">callable</span> to
determine which values to include.

### 参数

`callback`  
<span class="type">bool</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Optional <span class="type">callable</span> which returns **`TRUE`** if
the value should be included, **`FALSE`** otherwise.

If a callback is not provided, only values which are **`TRUE`** (see
<a href="/language/types/boolean.html#language.types.boolean.casting" class="link">converting to boolean</a>)
will be included.

### 返回值

A new vector containing all the values for which either the `callback`
returned **`TRUE`**, or all values that convert to **`TRUE`** if a
`callback` was not provided.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::filter</span> example
using callback function**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

var_dump($vector->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#3 (2) {
      [0]=>
      int(2)
      [1]=>
      int(4)
    }

**示例 \#2 <span class="function">Ds\\Vector::filter</span> example
without a callback function**

``` php
<?php
$vector = new \Ds\Vector([0, 1, 'a', true, false]);

var_dump($vector->filter());
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      string(1) "a"
      [2]=>
      bool(true)
    }

Ds\\Vector::find
================

Attempts to find a value's index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::find</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Returns the index of the `value`, or **`FALSE`** if not found.

### 参数

`value`  
The value to find.

### 返回值

The index of the value, or **`FALSE`** if not found.

> **Note**:
>
> Values will be compared by value and by type.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::find</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", 1, true]);

var_dump($vector->find("a")); // 0
var_dump($vector->find("b")); // false
var_dump($vector->find("1")); // false
var_dump($vector->find(1));   // 1
?>
```

以上例程的输出类似于：

    int(0)
    bool(false)
    bool(false)
    int(1)

Ds\\Vector::first
=================

Returns the first value in the vector

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::first</span> ( <span
class="methodparam">void</span> )

Returns the first value in the vector.

### 参数

此函数没有参数。

### 返回值

The first value in the vector.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::first</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->first());
?>
```

以上例程的输出类似于：

    int(1)

Ds\\Vector::get
===============

Returns the value at a given index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::get</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Returns the value at a given index.

### 参数

`index`  
The index to access, starting at 0.

### 返回值

The value at the requested index.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::get</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->get(0));
var_dump($vector->get(1));
var_dump($vector->get(2));
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

**示例 \#2 <span class="function">Ds\\Vector::get</span> example using
array syntax**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector[0]);
var_dump($vector[1]);
var_dump($vector[2]);
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Vector::insert
==================

Inserts values at a given index

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::insert</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$...values`</span> \] )

Inserts values into the vector at a given index.

### 参数

`index`  
The index at which to insert. `0 <= index <= count`

> **Note**:
>
> You can insert at the index equal to the number of values.

`values`  
The value or values to insert.

### 返回值

没有返回值。

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::insert</span> example**

``` php
<?php
$vector = new \Ds\Vector();

$vector->insert(0, "e");             // [e]
$vector->insert(1, "f");             // [e, f]
$vector->insert(2, "g");             // [e, f, g]
$vector->insert(0, "a", "b");        // [a, b, e, f, g]
$vector->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($vector);
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#1 (7) {
      [0]=>
      string(1) "a"
      [1]=>
      string(1) "b"
      [2]=>
      string(1) "c"
      [3]=>
      string(1) "d"
      [4]=>
      string(1) "e"
      [5]=>
      string(1) "f"
      [6]=>
      string(1) "g"
    }

Ds\\Vector::isEmpty
===================

Returns whether the vector is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Vector::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the vector is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the vector is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::isEmpty</span> example**

``` php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = new \Ds\Vector();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Vector::join
================

Joins all values together as a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Ds\\Vector::join</span> (\[ <span
class="methodparam"><span class="type">string</span> `$glue`</span> \] )

Joins all values together as a string using an optional separator
between each value.

### 参数

`glue`  
An optional string to separate each value.

### 返回值

All values of the vector joined together as a string.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::join</span> example using
a separator string**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($vector->join("|"));
?>
```

以上例程的输出类似于：

    string(11) "a|b|c|1|2|3"

**示例 \#2 <span class="function">Ds\\Vector::join</span> example
without a separator string**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($vector->join());
?>
```

以上例程的输出类似于：

    string(11) "abc123"

Ds\\Vector::jsonSerialize
=========================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\Vector::last
================

Returns the last value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::last</span> ( <span
class="methodparam">void</span> )

Returns the last value in the vector.

### 参数

此函数没有参数。

### 返回值

The last value in the vector.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::last</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->last());
?>
```

以上例程的输出类似于：

    int(3)

Ds\\Vector::map
===============

Returns the result of applying a callback to each value

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span
class="methodname">Ds\\Vector::map</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Returns the result of applying a `callback` function to each value in
the vector.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

A <span class="type">callable</span> to apply to each value in the
vector.

The callable should return what the new value will be in the new vector.

### 返回值

The result of applying a `callback` to each value in the vector.

> **Note**:
>
> The values of the current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::map</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

print_r($vector->map(function($value) { return $value * 2; }));
print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 2
        [1] => 4
        [2] => 6
    )
    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )

Ds\\Vector::merge
=================

Returns the result of adding all given values to the vector

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span
class="methodname">Ds\\Vector::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$values`</span> )

Returns the result of adding all given values to the vector.

### 参数

`values`  
A <span class="classname">traversable</span> object or an <span
class="type">array</span>.

### 返回值

The result of adding all given values to the vector, effectively the
same as adding the values to a copy, then returning that copy.

> **Note**:
>
> The current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::merge</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->merge([4, 5, 6]));
var_dump($vector);
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#2 (6) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
      [3]=>
      int(4)
      [4]=>
      int(5)
      [5]=>
      int(6)
    }
    object(Ds\Vector)#1 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Vector::pop
===============

Removes and returns the last value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::pop</span> ( <span
class="methodparam">void</span> )

Removes and returns the last value.

### 参数

此函数没有参数。

### 返回值

The removed last value.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::pop</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->pop());
var_dump($vector->pop());
var_dump($vector->pop());
?>
```

以上例程的输出类似于：

    int(3)
    int(2)
    int(1)

Ds\\Vector::push
================

Adds values to the end of the vector

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::push</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Adds values to the end of the vector.

### 参数

`values`  
The values to add.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Vector::push</span> example**

``` php
<?php
$vector = new \Ds\Vector();

$vector->push("a");
$vector->push("b");
$vector->push("c", "d");
$vector->push(...["e", "f"]);

print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => a
        [1] => b
        [2] => c
        [3] => d
        [4] => e
        [5] => f
    )

Ds\\Vector::reduce
==================

Reduces the vector to a single value using a callback function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::reduce</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$initial`</span> \] )

Reduces the vector to a single value using a callback function.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$carry`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

`carry`  
The return value of the previous callback, or `initial` if it's the
first iteration.

`value`  
The value of the current iteration.

`initial`  
The initial value of the carry value. Can be **`NULL`**.

### 返回值

The return value of the final callback.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::reduce</span> with initial
value example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($vector->reduce($callback, 5));

// Iterations:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

以上例程的输出类似于：

    int(30)

**示例 \#2 <span class="function">Ds\\Vector::reduce</span> without an
initial value example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->reduce(function($carry, $value) {
    return $carry + $value + 5;
}));

// Iterations:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

以上例程的输出类似于：

    int(21)

Ds\\Vector::remove
==================

Removes and returns a value by index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::remove</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Removes and returns a value by index.

### 参数

`index`  
The index of the value to remove.

### 返回值

The value that was removed.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::remove</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->remove(1));
var_dump($vector->remove(0));
var_dump($vector->remove(0));
?>
```

以上例程的输出类似于：

    string(1) "b"
    string(1) "a"
    string(1) "c"

Ds\\Vector::reverse
===================

Reverses the vector in-place

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::reverse</span> ( <span
class="methodparam">void</span> )

Reverses the vector in-place.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Vector::reverse</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);
$vector->reverse();

print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => c
        [1] => b
        [2] => a
    )

Ds\\Vector::reversed
====================

Returns a reversed copy

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span
class="methodname">Ds\\Vector::reversed</span> ( <span
class="methodparam">void</span> )

Returns a reversed copy of the vector.

### 参数

此函数没有参数。

### 返回值

A reversed copy of the vector.

> **Note**:
>
> The current instance is not affected.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::reversed</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

print_r($vector->reversed());
print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => c
        [1] => b
        [2] => a
    )
    Ds\Vector Object
    (
        [0] => a
        [1] => b
        [2] => c
    )

Ds\\Vector::rotate
==================

Rotates the vector by a given number of rotations

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::rotate</span> ( <span
class="methodparam"><span class="type">int</span> `$rotations`</span> )

Rotates the vector by a given number of rotations, which is equivalent
to successively calling `$vector->push($vector->shift())` if the number
of rotations is positive, or `$vector->unshift($vector->pop())` if
negative.

### 参数

`rotations`  
The number of times the vector should be rotated.

### 返回值

没有返回值。. The vector of the current instance will be rotated.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::rotate</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c", "d"]);

$vector->rotate(1);  // "a" is shifted, then pushed.
print_r($vector);

$vector->rotate(2);  // "b" and "c" are both shifted, the pushed.
print_r($vector);
?>
```

以上例程的输出类似于：

    (
        [0] => b
        [1] => c
        [2] => d
        [3] => a
    )
    Ds\Vector Object
    (
        [0] => d
        [1] => a
        [2] => b
        [3] => c
    )

Ds\\Vector::set
===============

Updates a value at a given index

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::set</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Updates a value at a given index.

### 参数

`index`  
The index of the value to update.

`value`  
The new value.

### 返回值

没有返回值。

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::set</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector->set(1, "_");
print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => a
        [1] => _
        [2] => c
    )

**示例 \#2 <span class="function">Ds\\Vector::set</span> example using
array syntax**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector[1] = "_";
print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => a
        [1] => _
        [2] => c
    )

Ds\\Vector::shift
=================

Removes and returns the first value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Vector::shift</span> ( <span
class="methodparam">void</span> )

Removes and returns the first value.

### 参数

此函数没有参数。

### 返回值

The first value, which was removed.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::shift</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->shift());
var_dump($vector->shift());
var_dump($vector->shift());
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Vector::slice
=================

Returns a sub-vector of a given range

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span
class="methodname">Ds\\Vector::slice</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\] )

Creates a sub-vector of a given range.

### 参数

`index`  
The index at which the sub-vector starts.

If positive, the vector will start at that index in the vector. If
negative, the vector will start that far from the end.

`length`  
If a length is given and is positive, the resulting vector will have up
to that many values in it. If the length results in an overflow, only
values up to the end of the vector will be included. If a length is
given and is negative, the vector will stop that many values from the
end. If a length is not provided, the resulting vector will contain all
values between the index and the end of the vector.

### 返回值

A sub-vector of the given range.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::slice</span> example**

``` php
<?php
$vector = new \Ds\Vector(["a", "b", "c", "d", "e"]);

// Slice from 2 onwards
print_r($vector->slice(2));

// Slice from 1, for a length of 3
print_r($vector->slice(1, 3));

// Slice from 1 onwards
print_r($vector->slice(1));

// Slice from 2 from the end onwards
print_r($vector->slice(-2));

// Slice from 1 to 1 from the end
print_r($vector->slice(1, -1));
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => c
        [1] => d
        [2] => e
    )
    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => d
    )
    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => d
        [3] => e
    )
    Ds\Vector Object
    (
        [0] => d
        [1] => e
    )
    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => d
    )

Ds\\Vector::sort
================

Sorts the vector in-place

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::sort</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Sorts the vector in-place, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Vector::sort</span> example**

``` php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);
$vector->sort();

print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Vector::sort</span> example using
a comparator**

``` php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

$vector->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Vector::sorted
==================

Returns a sorted copy

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Vector</span> <span
class="methodname">Ds\\Vector::sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Returns a sorted copy, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

Returns a sorted copy of the vector.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::sorted</span> example**

``` php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

print_r($vector->sorted());
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Vector::sorted</span> example
using a comparator**

``` php
<?php
$vector = new \Ds\Vector([4, 5, 1, 3, 2]);

$sorted = $vector->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Vector::sum
===============

Returns the sum of all values in the vector

### 说明

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">Ds\\Vector::sum</span> ( <span
class="methodparam">void</span> )

Returns the sum of all values in the vector.

> **Note**:
>
> Arrays and objects are considered equal to zero when calculating the
> sum.

### 参数

此函数没有参数。

### 返回值

The sum of all the values in the vector as either a <span
class="type">float</span> or <span class="type">int</span> depending on
the values in the vector.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::sum</span> integer
example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->sum());
?>
```

以上例程的输出类似于：

    int(6)

**示例 \#2 <span class="function">Ds\\Vector::sum</span> float example**

``` php
<?php
$vector = new \Ds\Vector([1, 2.5, 3]);
var_dump($vector->sum());
?>
```

以上例程的输出类似于：

    float(6.5)

Ds\\Vector::toArray
===================

Converts the vector to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\Vector::toArray</span> ( <span
class="methodparam">void</span> )

Converts the vector to an <span class="type">array</span>.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the vector.

### 范例

**示例 \#1 <span class="function">Ds\\Vector::toArray</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Vector::unshift
===================

Adds values to the front of the vector

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Vector::unshift</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

Adds values to the front of the vector, moving all the current values
forward to make room for the new values.

### 参数

`values`  
The values to add to the front of the vector.

> **Note**:
>
> Multiple values will be added in the same order that they are passed.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Vector::unshift</span> example**

``` php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

$vector->unshift("a");
$vector->unshift("b", "c");

print_r($vector);
?>
```

以上例程的输出类似于：

    Ds\Vector Object
    (
        [0] => b
        [1] => c
        [2] => a
        [3] => 1
        [4] => 2
        [5] => 3
    )

简介
----

A Deque (pronounced “deck”) is a sequence of values in a contiguous
buffer that grows and shrinks automatically. The name is a common
abbreviation of “double-ended queue” and is used internally by <span
class="classname">Ds\\Queue</span>.

Two pointers are used to keep track of a head and a tail. The pointers
can “wrap around” the end of the buffer, which avoids the need to move
other values around to make room. This makes shift and unshift very
fast —  something a <span class="classname">Ds\\Vector</span> can’t
compete with.

Accessing a value by index requires a translation between the index and
its corresponding position in the buffer:
`((head + position) % capacity)`.

Strengths
---------

-   Supports array syntax (square brackets).
-   Uses less overall memory than an <span class="type">array</span> for
    the same number of values.
-   Automatically frees allocated memory when its size drops low enough.
-   <span class="function">get</span>, <span
    class="function">set</span>, <span class="function">push</span>,
    <span class="function">pop</span>, <span
    class="function">shift</span>, and <span
    class="function">unshift</span> are all O(1).

Weaknesses
----------

-   Capacity must be a power of 2.
-   <span class="function">insert</span> and <span
    class="function">remove</span> are O(n).

类摘要
------

**Ds\\Deque**

<span class="ooclass"> class **Ds\\Deque** </span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Sequence</span> </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Ds\Deque::MIN_CAPACITY` <span class="initializer"> = 8</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">apply</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">contains</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">copy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">find</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">first</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">insert</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">join</span> (\[ <span class="methodparam"><span
class="type">string</span> `$glue`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">last</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">map</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">mixed</span> `$values`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$...values`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">reduce</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$initial`</span> \]
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">remove</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">reverse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">reversed</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">rotate</span> ( <span class="methodparam"><span
class="type">int</span> `$rotations`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">set</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">shift</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">slice</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sort</span> (\[ <span class="methodparam"><span
class="type">callable</span> `$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">sum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">unshift</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

}

预定义常量
----------

**`Ds\Deque::MIN_CAPACITY`**  

Ds\\Deque::allocate
===================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Ensures that enough memory is allocated for a required capacity. This
removes the need to reallocate the internal as values are added.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

> **Note**:
>
> Capacity will always be rounded up to the nearest power of 2.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Deque::allocate</span> example**

``` php
<?php
$deque = new \Ds\Deque();
var_dump($deque->capacity());

$deque->allocate(100);
var_dump($deque->capacity());
?>
```

以上例程的输出类似于：

    int(8)
    int(128)

Ds\\Deque::apply
================

Updates all values by applying a callback function to each value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::apply</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Updates all values by applying a `callback` function to each value in
the deque.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

A <span class="type">callable</span> to apply to each value in the
deque.

The callback should return what the value should be replaced by.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Deque::apply</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
$deque->apply(function($value) { return $value * 2; });

print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 2
        [1] => 4
        [2] => 6
    )

Ds\\Deque::capacity
===================

Returns the current capacity

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\Deque::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::capacity</span> example**

``` php
<?php
$deque = new \Ds\Deque();
var_dump($deque->capacity());

$deque->push(...range(1, 50));
var_dump($deque->capacity());
?>
```

以上例程的输出类似于：

    int(8)
    int(64)

Ds\\Deque::clear
================

Removes all values from the deque

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the deque.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Deque::clear</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
print_r($deque);

$deque->clear();
print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Deque Object
    (
    )

Ds\\Deque::\_\_construct
========================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\Deque::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

Creates a new instance, using either a <span
class="classname">traversable</span> object or an <span
class="type">array</span> for the initial `values`.

### 参数

`values`  
A traversable object or an <span class="type">array</span> to use for
the initial values.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::\_\_construct</span>
example**

``` php
<?php
$deque = new \Ds\Deque();
var_dump($deque);

$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque);
?>
```

以上例程的输出类似于：

    object(Ds\Deque)#2 (0) {
    }
    object(Ds\Deque)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Deque::contains
===================

Determines if the deque contains given values

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Deque::contains</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Determines if the deque contains all values.

### 参数

`values`  
Values to check.

### 返回值

**`FALSE`** if any of the provided `values` are not in the deque,
**`TRUE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::contains</span> example**

``` php
<?php
$deque = new \Ds\Deque(['a', 'b', 'c', 1, 2, 3]);

var_dump($deque->contains('a'));                // true
var_dump($deque->contains('a', 'b'));           // true
var_dump($deque->contains('c', 'd'));           // false

var_dump($deque->contains(...['c', 'b', 'a'])); // true

// Always strict
var_dump($deque->contains(1));                  // true
var_dump($deque->contains('1'));                // false

var_dump($sequece->contains(...[]));               // true
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(false)
    bool(true)
    bool(true)
    bool(false)
    bool(true)

Ds\\Deque::copy
===============

Returns a shallow copy of the deque

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">Ds\\Deque::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the deque.

### 参数

此函数没有参数。

### 返回值

A shallow copy of the deque.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::copy</span> example**

``` php
<?php
$a = new \Ds\Deque([1, 2, 3]);
$b = $a->copy();

$b->push(4);

print_r($a);
print_r($b);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Deque Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
    )

Ds\\Deque::count
================

Returns the number of values in the collection

See <span class="function">Countable::count</span>

Ds\\Deque::filter
=================

Creates a new deque using a <span class="type">callable</span> to
determine which values to include

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">Ds\\Deque::filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

Creates a new deque using a <span class="type">callable</span> to
determine which values to include.

### 参数

`callback`  
<span class="type">bool</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Optional <span class="type">callable</span> which returns **`TRUE`** if
the value should be included, **`FALSE`** otherwise.

If a callback is not provided, only values which are **`TRUE`** (see
<a href="/language/types/boolean.html#language.types.boolean.casting" class="link">converting to boolean</a>)
will be included.

### 返回值

A new deque containing all the values for which either the `callback`
returned **`TRUE`**, or all values that convert to **`TRUE`** if a
`callback` was not provided.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::filter</span> example using
callback function**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3, 4, 5]);

var_dump($deque->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

以上例程的输出类似于：

    object(Ds\Deque)#3 (2) {
      [0]=>
      int(2)
      [1]=>
      int(4)
    }

**示例 \#2 <span class="function">Ds\\Deque::filter</span> example
without a callback function**

``` php
<?php
$deque = new \Ds\Deque([0, 1, 'a', true, false]);

var_dump($deque->filter());
?>
```

以上例程的输出类似于：

    object(Ds\Deque)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      string(1) "a"
      [2]=>
      bool(true)
    }

Ds\\Deque::find
===============

Attempts to find a value's index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::find</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Returns the index of the `value`, or **`FALSE`** if not found.

### 参数

`value`  
The value to find.

### 返回值

The index of the value, or **`FALSE`** if not found.

> **Note**:
>
> Values will be compared by value and by type.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::find</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", 1, true]);

var_dump($deque->find("a")); // 0
var_dump($deque->find("b")); // false
var_dump($deque->find("1")); // false
var_dump($deque->find(1));   // 1
?>
```

以上例程的输出类似于：

    int(0)
    bool(false)
    bool(false)
    int(1)

Ds\\Deque::first
================

Returns the first value in the deque

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::first</span> ( <span
class="methodparam">void</span> )

Returns the first value in the deque.

### 参数

此函数没有参数。

### 返回值

The first value in the deque.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::first</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->first());
?>
```

以上例程的输出类似于：

    int(1)

Ds\\Deque::get
==============

Returns the value at a given index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::get</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Returns the value at a given index.

### 参数

`index`  
The index to access, starting at 0.

### 返回值

The value at the requested index.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::get</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->get(0));
var_dump($deque->get(1));
var_dump($deque->get(2));
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

**示例 \#2 <span class="function">Ds\\Deque::get</span> example using
array syntax**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque[0]);
var_dump($deque[1]);
var_dump($deque[2]);
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Deque::insert
=================

Inserts values at a given index

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::insert</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$...values`</span> \] )

Inserts values into the deque at a given index.

### 参数

`index`  
The index at which to insert. `0 <= index <= count`

> **Note**:
>
> You can insert at the index equal to the number of values.

`values`  
The value or values to insert.

### 返回值

没有返回值。

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::insert</span> example**

``` php
<?php
$deque = new \Ds\Deque();

$deque->insert(0, "e");             // [e]
$deque->insert(1, "f");             // [e, f]
$deque->insert(2, "g");             // [e, f, g]
$deque->insert(0, "a", "b");        // [a, b, e, f, g]
$deque->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($deque);
?>
```

以上例程的输出类似于：

    object(Ds\Deque)#1 (7) {
      [0]=>
      string(1) "a"
      [1]=>
      string(1) "b"
      [2]=>
      string(1) "c"
      [3]=>
      string(1) "d"
      [4]=>
      string(1) "e"
      [5]=>
      string(1) "f"
      [6]=>
      string(1) "g"
    }

Ds\\Deque::isEmpty
==================

Returns whether the deque is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Deque::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the deque is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the deque is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::isEmpty</span> example**

``` php
<?php
$a = new \Ds\Deque([1, 2, 3]);
$b = new \Ds\Deque();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Deque::join
===============

Joins all values together as a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Ds\\Deque::join</span> (\[ <span
class="methodparam"><span class="type">string</span> `$glue`</span> \] )

Joins all values together as a string using an optional separator
between each value.

### 参数

`glue`  
An optional string to separate each value.

### 返回值

All values of the deque joined together as a string.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::join</span> example using a
separator string**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c", 1, 2, 3]);

var_dump($deque->join("|"));
?>
```

以上例程的输出类似于：

    string(11) "a|b|c|1|2|3"

**示例 \#2 <span class="function">Ds\\Deque::join</span> example without
a separator string**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c", 1, 2, 3]);

var_dump($deque->join());
?>
```

以上例程的输出类似于：

    string(11) "abc123"

Ds\\Deque::jsonSerialize
========================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\Deque::last
===============

Returns the last value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::last</span> ( <span
class="methodparam">void</span> )

Returns the last value in the deque.

### 参数

此函数没有参数。

### 返回值

The last value in the deque.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::last</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->last());
?>
```

以上例程的输出类似于：

    int(3)

Ds\\Deque::map
==============

Returns the result of applying a callback to each value

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">Ds\\Deque::map</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Returns the result of applying a `callback` function to each value in
the deque.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

A <span class="type">callable</span> to apply to each value in the
deque.

The callable should return what the new value will be in the new deque.

### 返回值

The result of applying a `callback` to each value in the deque.

> **Note**:
>
> The values of the current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::map</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

print_r($deque->map(function($value) { return $value * 2; }));
print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 2
        [1] => 4
        [2] => 6
    )
    Ds\Deque Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )

Ds\\Deque::merge
================

Returns the result of adding all given values to the deque

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">Ds\\Deque::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$values`</span> )

Returns the result of adding all given values to the deque.

### 参数

`values`  
A <span class="classname">traversable</span> object or an <span
class="type">array</span>.

### 返回值

The result of adding all given values to the deque, effectively the same
as adding the values to a copy, then returning that copy.

> **Note**:
>
> The current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::merge</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->merge([4, 5, 6]));
var_dump($deque);
?>
```

以上例程的输出类似于：

    object(Ds\Deque)#2 (6) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
      [3]=>
      int(4)
      [4]=>
      int(5)
      [5]=>
      int(6)
    }
    object(Ds\Deque)#1 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Deque::pop
==============

Removes and returns the last value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::pop</span> ( <span
class="methodparam">void</span> )

Removes and returns the last value.

### 参数

此函数没有参数。

### 返回值

The removed last value.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::pop</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->pop());
var_dump($deque->pop());
var_dump($deque->pop());
?>
```

以上例程的输出类似于：

    int(3)
    int(2)
    int(1)

Ds\\Deque::push
===============

Adds values to the end of the deque

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::push</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Adds values to the end of the deque.

### 参数

`values`  
The values to add.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Deque::push</span> example**

``` php
<?php
$deque = new \Ds\Deque();

$deque->push("a");
$deque->push("b");
$deque->push("c", "d");
$deque->push(...["e", "f"]);

print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => a
        [1] => b
        [2] => c
        [3] => d
        [4] => e
        [5] => f
    )

Ds\\Deque::reduce
=================

Reduces the deque to a single value using a callback function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::reduce</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$initial`</span> \] )

Reduces the deque to a single value using a callback function.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$carry`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

`carry`  
The return value of the previous callback, or `initial` if it's the
first iteration.

`value`  
The value of the current iteration.

`initial`  
The initial value of the carry value. Can be **`NULL`**.

### 返回值

The return value of the final callback.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::reduce</span> with initial
value example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($deque->reduce($callback, 5));

// Iterations:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

以上例程的输出类似于：

    int(30)

**示例 \#2 <span class="function">Ds\\Deque::reduce</span> without an
initial value example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->reduce(function($carry, $value) {
    return $carry + $value + 5;
}));

// Iterations:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

以上例程的输出类似于：

    int(21)

Ds\\Deque::remove
=================

Removes and returns a value by index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::remove</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Removes and returns a value by index.

### 参数

`index`  
The index of the value to remove.

### 返回值

The value that was removed.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::remove</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->remove(1));
var_dump($deque->remove(0));
var_dump($deque->remove(0));
?>
```

以上例程的输出类似于：

    string(1) "b"
    string(1) "a"
    string(1) "c"

Ds\\Deque::reverse
==================

Reverses the deque in-place

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::reverse</span> ( <span
class="methodparam">void</span> )

Reverses the deque in-place.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Deque::reverse</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);
$deque->reverse();

print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => c
        [1] => b
        [2] => a
    )

Ds\\Deque::reversed
===================

Returns a reversed copy

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">Ds\\Deque::reversed</span> ( <span
class="methodparam">void</span> )

Returns a reversed copy of the deque.

### 参数

此函数没有参数。

### 返回值

A reversed copy of the deque.

> **Note**:
>
> The current instance is not affected.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::reversed</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

print_r($deque->reversed());
print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => c
        [1] => b
        [2] => a
    )
    Ds\Deque Object
    (
        [0] => a
        [1] => b
        [2] => c
    )

Ds\\Deque::rotate
=================

Rotates the deque by a given number of rotations

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::rotate</span> ( <span
class="methodparam"><span class="type">int</span> `$rotations`</span> )

Rotates the deque by a given number of rotations, which is equivalent to
successively calling `$deque->push($deque->shift())` if the number of
rotations is positive, or `$deque->unshift($deque->pop())` if negative.

### 参数

`rotations`  
The number of times the deque should be rotated.

### 返回值

没有返回值。. The deque of the current instance will be rotated.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::rotate</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c", "d"]);

$deque->rotate(1);  // "a" is shifted, then pushed.
print_r($deque);

$deque->rotate(2);  // "b" and "c" are both shifted, the pushed.
print_r($deque);
?>
```

以上例程的输出类似于：

    (
        [0] => b
        [1] => c
        [2] => d
        [3] => a
    )
    Ds\Deque Object
    (
        [0] => d
        [1] => a
        [2] => b
        [3] => c
    )

Ds\\Deque::set
==============

Updates a value at a given index

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::set</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Updates a value at a given index.

### 参数

`index`  
The index of the value to update.

`value`  
The new value.

### 返回值

没有返回值。

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::set</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

$deque->set(1, "_");
print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => a
        [1] => _
        [2] => c
    )

**示例 \#2 <span class="function">Ds\\Deque::set</span> example using
array syntax**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

$deque[1] = "_";
print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => a
        [1] => _
        [2] => c
    )

Ds\\Deque::shift
================

Removes and returns the first value

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Deque::shift</span> ( <span
class="methodparam">void</span> )

Removes and returns the first value.

### 参数

此函数没有参数。

### 返回值

The first value, which was removed.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::shift</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->shift());
var_dump($deque->shift());
var_dump($deque->shift());
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Deque::slice
================

Returns a sub-deque of a given range

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">Ds\\Deque::slice</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\] )

Creates a sub-deque of a given range.

### 参数

`index`  
The index at which the sub-deque starts.

If positive, the deque will start at that index in the deque. If
negative, the deque will start that far from the end.

`length`  
If a length is given and is positive, the resulting deque will have up
to that many values in it. If the length results in an overflow, only
values up to the end of the deque will be included. If a length is given
and is negative, the deque will stop that many values from the end. If a
length is not provided, the resulting deque will contain all values
between the index and the end of the deque.

### 返回值

A sub-deque of the given range.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::slice</span> example**

``` php
<?php
$deque = new \Ds\Deque(["a", "b", "c", "d", "e"]);

// Slice from 2 onwards
print_r($deque->slice(2));

// Slice from 1, for a length of 3
print_r($deque->slice(1, 3));

// Slice from 1 onwards
print_r($deque->slice(1));

// Slice from 2 from the end onwards
print_r($deque->slice(-2));

// Slice from 1 to 1 from the end
print_r($deque->slice(1, -1));
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => c
        [1] => d
        [2] => e
    )
    Ds\Deque Object
    (
        [0] => b
        [1] => c
        [2] => d
    )
    Ds\Deque Object
    (
        [0] => b
        [1] => c
        [2] => d
        [3] => e
    )
    Ds\Deque Object
    (
        [0] => d
        [1] => e
    )
    Ds\Deque Object
    (
        [0] => b
        [1] => c
        [2] => d
    )

Ds\\Deque::sort
===============

Sorts the deque in-place

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::sort</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Sorts the deque in-place, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Deque::sort</span> example**

``` php
<?php
$deque = new \Ds\Deque([4, 5, 1, 3, 2]);
$deque->sort();

print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Deque::sort</span> example using a
comparator**

``` php
<?php
$deque = new \Ds\Deque([4, 5, 1, 3, 2]);

$deque->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Deque::sorted
=================

Returns a sorted copy

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Deque</span>
<span class="methodname">Ds\\Deque::sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Returns a sorted copy, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

Returns a sorted copy of the deque.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::sorted</span> example**

``` php
<?php
$deque = new \Ds\Deque([4, 5, 1, 3, 2]);

print_r($deque->sorted());
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Deque::sorted</span> example using
a comparator**

``` php
<?php
$deque = new \Ds\Deque([4, 5, 1, 3, 2]);

$sorted = $deque->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Deque::sum
==============

Returns the sum of all values in the deque

### 说明

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">Ds\\Deque::sum</span> ( <span
class="methodparam">void</span> )

Returns the sum of all values in the deque.

> **Note**:
>
> Arrays and objects are considered equal to zero when calculating the
> sum.

### 参数

此函数没有参数。

### 返回值

The sum of all the values in the deque as either a <span
class="type">float</span> or <span class="type">int</span> depending on
the values in the deque.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::sum</span> integer
example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->sum());
?>
```

以上例程的输出类似于：

    int(6)

**示例 \#2 <span class="function">Ds\\Deque::sum</span> float example**

``` php
<?php
$deque = new \Ds\Deque([1, 2.5, 3]);
var_dump($deque->sum());
?>
```

以上例程的输出类似于：

    float(6.5)

Ds\\Deque::toArray
==================

Converts the deque to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\Deque::toArray</span> ( <span
class="methodparam">void</span> )

Converts the deque to an <span class="type">array</span>.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the deque.

### 范例

**示例 \#1 <span class="function">Ds\\Deque::toArray</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Deque::unshift
==================

Adds values to the front of the deque

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Deque::unshift</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

Adds values to the front of the deque, moving all the current values
forward to make room for the new values.

### 参数

`values`  
The values to add to the front of the deque.

> **Note**:
>
> Multiple values will be added in the same order that they are passed.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Deque::unshift</span> example**

``` php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

$deque->unshift("a");
$deque->unshift("b", "c");

print_r($deque);
?>
```

以上例程的输出类似于：

    Ds\Deque Object
    (
        [0] => b
        [1] => c
        [2] => a
        [3] => 1
        [4] => 2
        [5] => 3
    )

简介
----

A Map is a sequential collection of key-value pairs, almost identical to
an <span class="type">array</span> used in a similar context. Keys can
be any type, but must be unique. Values are replaced if added to the map
using the same key.

Strengths
---------

-   Keys and values can be any type, including objects.
-   Supports array syntax (square brackets).
-   Insertion order is preserved.
-   Performance and memory efficiency is very similar to an <span
    class="type">array</span>.
-   Automatically frees allocated memory when its size drops low enough.

Weaknesses
----------

-   Can’t be converted to an array when objects are used as keys.

类摘要
------

**Ds\\Map**

<span class="ooclass"> class **Ds\\Map** </span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Collection</span> </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Ds\Map::MIN_CAPACITY` <span class="initializer"> = 16</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">apply</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">copy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">diff</span> ( <span class="methodparam"><span
class="type">Ds\\Map</span> `$map`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">first</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">mixed</span> `$key`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$default`</span> \]
)

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasKey</span> ( <span class="methodparam"><span
class="type">mixed</span> `$key`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">hasValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">intersect</span> ( <span
class="methodparam"><span class="type">Ds\\Map</span> `$map`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">keys</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">ksort</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">ksorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">last</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">map</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">mixed</span> `$values`</span> )

<span class="modifier">public</span> <span
class="type">Ds\\Sequence</span> <span class="methodname">pairs</span> (
<span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">put</span> ( <span class="methodparam"><span
class="type">mixed</span> `$key`</span> , <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">putAll</span> ( <span class="methodparam"><span
class="type">mixed</span> `$pairs`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">reduce</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$initial`</span> \]
)

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">remove</span> ( <span class="methodparam"><span
class="type">mixed</span> `$key`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$default`</span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">reverse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">reversed</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">skip</span> ( <span class="methodparam"><span
class="type">int</span> `$position`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">slice</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sort</span> (\[ <span class="methodparam"><span
class="type">callable</span> `$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">sum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">union</span> ( <span class="methodparam"><span
class="type">Ds\\Map</span> `$map`</span> )

<span class="modifier">public</span> <span
class="type">Ds\\Sequence</span> <span class="methodname">values</span>
( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">xor</span> ( <span class="methodparam"><span
class="type">Ds\\Map</span> `$map`</span> )

}

预定义常量
----------

**`Ds\Map::MIN_CAPACITY`**  

Ds\\Map::allocate
=================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Allocates enough memory for a required capacity.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

> **Note**:
>
> Capacity will always be rounded up to the nearest power of 2.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::allocate</span> example**

``` php
<?php
$map = new \Ds\Map();
var_dump($map->capacity());

$map->allocate(100);
var_dump($map->capacity());
?>
```

以上例程的输出类似于：

    int(16)
    int(128)

Ds\\Map::apply
==============

Updates all values by applying a callback function to each value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::apply</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Updates all values by applying a `callback` function to each value in
the map.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

A <span class="type">callable</span> to apply to each value in the map.

The callback should return what the value should be replaced by.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::apply</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$map->apply(function($key, $value) { return $value * 2; });

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 2
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 4
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 6
            )

    )

Ds\\Map::capacity
=================

Returns the current capacity

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\Map::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

### 范例

**示例 \#1 <span class="function">Ds\\Map::capacity</span> example**

``` php
<?php
$map = new \Ds\Map();
var_dump($map->capacity());
?>
```

以上例程的输出类似于：

    int(16)

Ds\\Map::clear
==============

Removes all values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the map.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::clear</span> example**

``` php
<?php
$map = new \Ds\Map([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);
print_r($map);

$map->clear();
print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )
    Ds\Map Object
    (
    )

Ds\\Map::\_\_construct
======================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\Map::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Creates a new instance, using either a <span
class="classname">traversable</span> object or an <span
class="type">array</span> for the initial `values`.

### 参数

`values`  
A traversable object or an <span class="type">array</span> to use for
the initial values.

### 范例

**示例 \#1 <span class="function">Ds\\Map::\_\_construct</span>
example**

``` php
<?php
$map = new \Ds\Map();
var_dump($map);

$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map);
?>
```

以上例程的输出类似于：

    object(Ds\Map)#1 (0) {
    }
    object(Ds\Map)#2 (3) {
      [0]=>
      object(Ds\Pair)#1 (2) {
        ["key"]=>
        string(1) "a"
        ["value"]=>
        int(1)
      }
      [1]=>
      object(Ds\Pair)#3 (2) {
        ["key"]=>
        string(1) "b"
        ["value"]=>
        int(2)
      }
      [2]=>
      object(Ds\Pair)#4 (2) {
        ["key"]=>
        string(1) "c"
        ["value"]=>
        int(3)
      }
    }

Ds\\Map::copy
=============

Returns a shallow copy of the map

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the map.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the map.

### 范例

**示例 \#1 <span class="function">Ds\\Map::copy</span> example**

``` php
<?php
$map = new \Ds\Map([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);

print_r($map->copy());
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )

Ds\\Map::count
==============

Returns the number of values in the map

See <span class="function">Countable::count</span>

Ds\\Map::diff
=============

Creates a new map using keys that aren't in another map

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::diff</span> ( <span
class="methodparam"><span class="type">Ds\\Map</span> `$map`</span> )

Returns the result of removing all keys from the current instance that
are present in a given `map`.

`A \ B = {x ∈ A | x ∉ B}`

### 参数

`map`  
The map containing the keys to exclude in the resulting map.

### 返回值

The result of removing all keys from the current instance that are
present in a given `map`.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Complement_(set_theory)" class="link external">» Compliment</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Map::diff</span> example**

``` php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 4, "c" => 5, "d" => 6]);

var_dump($a->diff($b));
?>
```

以上例程的输出类似于：

    object(Ds\Map)#3 (1) {
      [0]=>
      object(Ds\Pair)#4 (2) {
        ["key"]=>
        string(1) "a"
        ["value"]=>
        int(1)
      }
    }

Ds\\Map::filter
===============

Creates a new map using a <span class="type">callable</span> to
determine which pairs to include

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

Creates a new map using a <span class="type">callable</span> to
determine which pairs to include.

### 参数

`callback`  
<span class="type">bool</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Optional <span class="type">callable</span> which returns **`TRUE`** if
the pair should be included, **`FALSE`** otherwise.

If a callback is not provided, only values which are **`TRUE`** (see
<a href="/language/types/boolean.html#language.types.boolean.casting" class="link">converting to boolean</a>)
will be included.

### 返回值

A new map containing all the pairs for which either the `callback`
returned **`TRUE`**, or all values that convert to **`TRUE`** if a
`callback` was not provided.

### 范例

**示例 \#1 <span class="function">Ds\\Map::filter</span> example using
callback function**

``` php
<?php
$map = new \Ds\Map(["a", "b", "c", "d", "e"]);

var_dump($map->filter(function($key, $value) {
    return $key % 2 == 0;
}));
?>
```

以上例程的输出类似于：

    object(Ds\Map)#3 (3) {
      [0]=>
      object(Ds\Pair)#2 (2) {
        ["key"]=>
        int(0)
        ["value"]=>
        string(1) "a"
      }
      [1]=>
      object(Ds\Pair)#4 (2) {
        ["key"]=>
        int(2)
        ["value"]=>
        string(1) "c"
      }
      [2]=>
      object(Ds\Pair)#5 (2) {
        ["key"]=>
        int(4)
        ["value"]=>
        string(1) "e"
      }
    }

**示例 \#2 <span class="function">Ds\\Map::filter</span> example without
a callback function**

``` php
<?php
$map = new \Ds\Map(["a" => 0, "b" => 1, "c" => true, "d" => false]);

var_dump($map->filter());
?>
```

以上例程的输出类似于：

    object(Ds\Map)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      string(1) "a"
      [2]=>
      bool(true)
    }

Ds\\Map::first
==============

Returns the first pair in the map

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">Ds\\Map::first</span> ( <span
class="methodparam">void</span> )

Returns the first pair in the map.

### 参数

此函数没有参数。

### 返回值

The first pair in the map.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Map::first</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->first());
?>
```

以上例程的输出类似于：

    object(Ds\Pair)#2 (2) {
      ["key"]=>
      string(1) "a"
      ["value"]=>
      int(1)
    }

Ds\\Map::get
============

Returns the value for a given key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Map::get</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$default`</span> \] )

Returns the value for a given key, or an optional default value if the
key could not be found.

> **Note**:
>
> Keys of type <span class="type">object</span> are supported. If an
> object implements <span class="classname">Ds\\Hashable</span>,
> equality will be determined by the object's `equals` function. If an
> object does not implement <span class="classname">Ds\\Hashable</span>,
> objects must be references to the same instance to be considered
> equal.

> **Note**:
>
> You can also use array syntax to access values by key, eg.
> `$map["key"]`.

**Caution**

Be careful when using array syntax. Scalar keys will be coerced to
integers by the engine. For example, `$map["1"]` will attempt to access
`int(1)`, while `$map->get("1")` will correctly look up the string key.

See <a href="/language/types/array.html" class="link">Arrays</a>.

### 参数

`key`  
The key to look up.

`default`  
The optional default value, returned if the key could not be found.

### 返回值

The value mapped to the given `key`, or the `default` value if provided
and the key could not be found in the map.

### 错误／异常

<span class="classname">OutOfBoundsException</span> if the key could not
be found and a default value was not provided.

### 范例

**示例 \#1 <span class="function">Ds\\Map::get</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->get("a"));       // 1
var_dump($map->get("d", 10));   // 10 (default used)
?>
```

以上例程的输出类似于：

    int(1)
    int(10)

**示例 \#2 <span class="function">Ds\\Map::get</span> example using
array syntax**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map["a"])); // 1
?>
```

以上例程的输出类似于：

    int(1)

Ds\\Map::hasKey
===============

Determines whether the map contains a given key

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Map::hasKey</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> )

Determines whether the map contains a given key.

### 参数

`key`  
The key to look for.

### 返回值

Returns **`TRUE`** if the key could found, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Map::hasKey</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->hasKey("a")); // true
var_dump($map->hasKey("e")); // false
?>
```

以上例程的输出类似于：

    bool(true)
    bool(false)

Ds\\Map::hasValue
=================

Determines whether the map contains a given value

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Map::hasValue</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Determines whether the map contains a given value.

### 参数

`value`  
The value to look for.

### 返回值

Returns **`TRUE`** if the value could found, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Map::hasValue</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->hasValue(1)); // true
var_dump($map->hasValue(4)); // false
?>
```

以上例程的输出类似于：

    bool(true)
    bool(false)

Ds\\Map::intersect
==================

Creates a new map by intersecting keys with another map

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::intersect</span> ( <span
class="methodparam"><span class="type">Ds\\Map</span> `$map`</span> )

Creates a new map containing the pairs of the current instance whose
keys are also present in the given `map`. In other words, returns a copy
of the current instance with all keys removed that are not also in the
other `map`.

`A ∩ B = {x : x ∈ A ∧ x ∈ B}`

> **Note**:
>
> Values from the current instance will be kept.

### 参数

`map`  
The other map, containing the keys to intersect with.

### 返回值

The key intersection of the current instance and another `map`.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Intersection_(set_theory)" class="link external">» Intersection</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Map::intersect</span> example**

``` php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 4, "c" => 5, "d" => 6]);

var_dump($a->intersect($b));
?>
```

以上例程的输出类似于：

    object(Ds\Map)#3 (2) {
      [0]=>
      object(Ds\Pair)#4 (2) {
        ["key"]=>
        string(1) "b"
        ["value"]=>
        int(2)
      }
      [1]=>
      object(Ds\Pair)#5 (2) {
        ["key"]=>
        string(1) "c"
        ["value"]=>
        int(3)
      }
    }

Ds\\Map::isEmpty
================

Returns whether the map is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Map::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the map is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the map is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Map::isEmpty</span> example**

``` php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Map::jsonSerialize
======================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\Map::keys
=============

Returns a set of the map's keys

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Map::keys</span> ( <span
class="methodparam">void</span> )

Returns a set containing all the keys of the map, in the same order.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">Ds\\Set</span> containing all the keys of the
map.

### 范例

**示例 \#1 <span class="function">Ds\\Map::keys</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->keys());
?>
```

以上例程的输出类似于：

    object(Ds\Set)#2 (3) {
      [0]=>
      string(1) "a"
      [1]=>
      string(1) "b"
      [2]=>
      string(1) "c"
    }

Ds\\Map::ksort
==============

Sorts the map in-place by key

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::ksort</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Sorts the map in-place by key, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::ksort</span> example**

``` php
<?php
$map = new \Ds\Map(["b" => 2, "c" => 3, "a" => 1]);
$map->ksort();

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )

**示例 \#2 <span class="function">Ds\\Map::ksort</span> example using a
comparator**

``` php
<?php
$map = new \Ds\Map([1 => "x", 2 => "y", 0 => "z"]);

// Reverse
$map->ksort(function($a, $b) {
    return $b <=> $a;
});

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => 2
                [value] => y
            )

        [1] => Ds\Pair Object
            (
                [key] => 1
                [value] => x
            )

        [2] => Ds\Pair Object
            (
                [key] => 0
                [value] => z
            )

    )

Ds\\Map::ksorted
================

Returns a copy, sorted by key

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::ksorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Returns a copy sorted by key, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

Returns a copy of the map, sorted by key.

### 范例

**示例 \#1 <span class="function">Ds\\Map::ksorted</span> example**

``` php
<?php
$map = new \Ds\Map(["b" => 2, "c" => 3, "a" => 1]);

print_r($map->ksorted());
?>
```

以上例程的输出类似于：

    Ds\Map Object
    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )

**示例 \#2 <span class="function">Ds\\Map::ksorted</span> example using
a comparator**

``` php
<?php
$map = new \Ds\Map([1 => "x", 2 => "y", 0 => "z"]);

// Reverse
$sorted = $map->ksorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => 2
                [value] => y
            )

        [1] => Ds\Pair Object
            (
                [key] => 1
                [value] => x
            )

        [2] => Ds\Pair Object
            (
                [key] => 0
                [value] => z
            )

    )

Ds\\Map::last
=============

Returns the last pair of the map

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">Ds\\Map::last</span> ( <span
class="methodparam">void</span> )

Returns the last pair of the map.

### 参数

此函数没有参数。

### 返回值

The last pair of the map.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Map::last</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->last());
?>
```

以上例程的输出类似于：

    object(Ds\Pair)#2 (2) {
      ["key"]=>
      string(1) "c"
      ["value"]=>
      int(3)
    }

Ds\\Map::map
============

Returns the result of applying a callback to each value

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::map</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> )

Returns the result of applying a `callback` function to each value of
the map.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

A <span class="type">callable</span> to apply to each value in the map.

The callable should return what the key will be mapped to in the
resulting map.

### 返回值

The result of applying a `callback` to each value in the map.

> **Note**:
>
> The keys and values of the current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Map::map</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->map(function($key, $value) { return $value * 2; }));
print_r($map);
?>
```

以上例程的输出类似于：

    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 2
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 4
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 6
            )

    )
    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )

Ds\\Map::merge
==============

Returns the result of adding all given associations

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$values`</span> )

Returns the result of associating all keys of a given <span
class="classname">traversable</span> object or <span
class="type">array</span> with their corresponding values, combined with
the current instance.

> **Note**:
>
> Values of the current instance will be overwritten by those provided
> where keys are equal.

### 参数

`values`  
A <span class="classname">traversable</span> object or an <span
class="type">array</span>.

### 返回值

The result of associating all keys of a given <span
class="classname">traversable</span> object or <span
class="type">array</span> with their corresponding values, combined with
the current instance.

> **Note**:
>
> The current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Map::merge</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->merge(["a" => 10, "e" => 50]));
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 10
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

        [3] => Ds\Pair Object
            (
                [key] => e
                [value] => 50
            )

    )

Ds\\Map::pairs
==============

Returns a sequence containing all the pairs of the map

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Sequence</span> <span
class="methodname">Ds\\Map::pairs</span> ( <span
class="methodparam">void</span> )

Returns a <span class="classname">Ds\\Sequence</span> containing all the
pairs of the map.

### 参数

此函数没有参数。

### 返回值

<span class="classname">Ds\\Sequence</span> containing all the pairs of
the map.

### 范例

**示例 \#1 <span class="function">Ds\\Map::pairs</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->pairs());
?>
```

以上例程的输出类似于：

    object(Ds\Map)#8 (3) {
      [0]=>
      object(Ds\Pair)#5 (2) {
        ["key"]=>
        string(1) "a"
        ["value"]=>
        int(1)
      }
      [1]=>
      object(Ds\Pair)#6 (2) {
        ["key"]=>
        string(1) "b"
        ["value"]=>
        int(2)
      }
      [2]=>
      object(Ds\Pair)#7 (2) {
        ["key"]=>
        string(1) "c"
        ["value"]=>
        int(3)
      }
    }
    p

Ds\\Map::put
============

Associates a key with a value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::put</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

Associates a `key` with a `value`, overwriting a previous association if
one exists.

> **Note**:
>
> Keys of type <span class="type">object</span> are supported. If an
> object implements <span class="classname">Ds\\Hashable</span>,
> equality will be determined by the object's `equals` function. If an
> object does not implement <span class="classname">Ds\\Hashable</span>,
> objects must be references to the same instance to be considered
> equal.

> **Note**:
>
> You can also use array syntax to associate values by key, eg.
> `$map["key"] = $value`.

**Caution**

Be careful when using array syntax. Scalar keys will be coerced to
integers by the engine. For example, `$map["1"]` will attempt to access
`int(1)`, while `$map->get("1")` will correctly look up the string key.

See <a href="/language/types/array.html" class="link">Arrays</a>.

### 参数

`key`  
The key to associate the value with.

`value`  
The value to be associated with the key.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::put</span> example**

``` php
<?php
$map = new \Ds\Map();

$map->put("a", 1);
$map->put("b", 2);
$map->put("c", 3);

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )

**示例 \#2 <span class="function">Ds\\Map::put</span> example using
objects as keys**

``` php
<?php
class HashableObject implements \Ds\Hashable
{
    /**
     * An arbitrary value to use as the hash value. Does not define equality.
     */
    private $value;

    public function __construct($value)
    {
        $this->value = $value;
    }

    public function hash()
    {
        return $this->value;
    }

    public function equals($obj): bool
    {
        return $this->value === $obj->value;
    }
}

$map = new \Ds\Map();

$obj = new \ArrayIterator([]);

// Using the same instance multiple times will overwrite the previous value.
$map->put($obj, 1);
$map->put($obj, 2);

// Using multiple instances of the same object will create new associations.
$map->put(new \stdClass(), 3);
$map->put(new \stdClass(), 4);

// Using multiple instances of equal hashable objects will overwrite previous values.
$map->put(new \HashableObject(1), 5);
$map->put(new \HashableObject(1), 6);
$map->put(new \HashableObject(2), 7);
$map->put(new \HashableObject(2), 8);

var_dump($map);
?>
```

以上例程的输出类似于：

    object(Ds\Map)#1 (5) {
      [0]=>
      object(Ds\Pair)#7 (2) {
        ["key"]=>
        object(ArrayIterator)#2 (1) {
          ["storage":"ArrayIterator":private]=>
          array(0) {
          }
        }
        ["value"]=>
        int(2)
      }
      [1]=>
      object(Ds\Pair)#8 (2) {
        ["key"]=>
        object(stdClass)#3 (0) {
        }
        ["value"]=>
        int(3)
      }
      [2]=>
      object(Ds\Pair)#9 (2) {
        ["key"]=>
        object(stdClass)#4 (0) {
        }
        ["value"]=>
        int(4)
      }
      [3]=>
      object(Ds\Pair)#10 (2) {
        ["key"]=>
        object(HashableObject)#5 (1) {
          ["value":"HashableObject":private]=>
          int(1)
        }
        ["value"]=>
        int(6)
      }
      [4]=>
      object(Ds\Pair)#11 (2) {
        ["key"]=>
        object(HashableObject)#6 (1) {
          ["value":"HashableObject":private]=>
          int(2)
        }
        ["value"]=>
        int(8)
      }
    }

Ds\\Map::putAll
===============

Associates all key-value pairs of a traversable object or array

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::putAll</span> ( <span
class="methodparam"><span class="type">mixed</span> `$pairs`</span> )

Associates all key-value `pairs` of a <span
class="classname">traversable</span> object or <span
class="type">array</span>.

> **Note**:
>
> Keys of type <span class="type">object</span> are supported. If an
> object implements <span class="classname">Ds\\Hashable</span>,
> equality will be determined by the object's `equals` function. If an
> object does not implement <span class="classname">Ds\\Hashable</span>,
> objects must be references to the same instance to be considered
> equal.

### 参数

`pairs`  
<span class="classname">traversable</span> object or <span
class="type">array</span>.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::putAll</span> example**

``` php
<?php
$map = new \Ds\Map();

$map->putAll([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

    )

Ds\\Map::reduce
===============

Reduces the map to a single value using a callback function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Map::reduce</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$initial`</span> \] )

Reduces the map to a single value using a callback function.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$carry`</span> ,
<span class="methodparam"><span class="type">mixed</span> `$key`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

`carry`  
The return value of the previous callback, or `initial` if it's the
first iteration.

`key`  
The key of the current iteration.

`value`  
The value of the current iteration.

`initial`  
The initial value of the carry value. Can be **`NULL`**.

### 返回值

The return value of the final callback.

### 范例

**示例 \#1 <span class="function">Ds\\Map::reduce</span> with initial
value example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

$callback = function($carry, $key, $value) {
    return $carry * $value;
};

var_dump($map->reduce($callback, 5));

// Iterations:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

以上例程的输出类似于：

    int(30)

**示例 \#2 <span class="function">Ds\\Map::reduce</span> without an
initial value example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->reduce(function($carry, $key, $value) {
    return $carry + $value + 5;
}));

// Iterations:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

以上例程的输出类似于：

    int(21)

Ds\\Map::remove
===============

Removes and returns a value by key

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Map::remove</span> ( <span
class="methodparam"><span class="type">mixed</span> `$key`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$default`</span> \] )

Removes and returns a value by key, or return an optional default value
if the key could not be found.

> **Note**:
>
> Keys of type <span class="type">object</span> are supported. If an
> object implements <span class="classname">Ds\\Hashable</span>,
> equality will be determined by the object's `equals` function. If an
> object does not implement <span class="classname">Ds\\Hashable</span>,
> objects must be references to the same instance to be considered
> equal.

> **Note**:
>
> You can also use array syntax to access values by key, eg.
> `$map["key"]`.

**Caution**

Be careful when using array syntax. Scalar keys will be coerced to
integers by the engine. For example, `$map["1"]` will attempt to access
`int(1)`, while `$map->get("1")` will correctly look up the string key.

See <a href="/language/types/array.html" class="link">Arrays</a>.

### 参数

`key`  
The key to remove.

`default`  
The optional default value, returned if the key could not be found.

### 返回值

The value that was removed, or the `default` value if provided and the
`key` could not be found in the map.

### 错误／异常

<span class="classname">OutOfBoundsException</span> if the key could not
be found and a default value was not provided.

### 范例

**示例 \#1 <span class="function">Ds\\Map::remove</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->remove("a"));      //  1
var_dump($map->remove("e", 10));  // 10 (default used)
?>
```

以上例程的输出类似于：

    int(1)
    int(10)

Ds\\Map::reverse
================

Reverses the map in-place

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::reverse</span> ( <span
class="methodparam">void</span> )

Reverses the map in-place.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::reverse</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$map->reverse();

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

    )

Ds\\Map::reversed
=================

Returns a reversed copy

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::reversed</span> ( <span
class="methodparam">void</span> )

Returns a reversed copy of the map.

### 参数

此函数没有参数。

### 返回值

A reversed copy of the map.

> **Note**:
>
> The current instance is not affected.

### 范例

**示例 \#1 <span class="function">Ds\\Map::reversed</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

print_r($map->reversed());
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => c
                [value] => 3
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

    )

Ds\\Map::skip
=============

Returns the pair at a given positional index

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">Ds\\Map::skip</span> ( <span
class="methodparam"><span class="type">int</span> `$position`</span> )

Returns the pair at a given zero-based `position`.

### 参数

`position`  
The zero-based positional index to return.

### 返回值

Returns the <span class="classname">Ds\\Pair</span> at the given
`position`.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the position is
not valid.

### 范例

**示例 \#1 <span class="function">Ds\\Map::skip</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->skip(1));
?>
```

以上例程的输出类似于：

    object(Ds\Pair)#2 (2) {
      ["key"]=>
      string(1) "b"
      ["value"]=>
      int(2)
    }

Ds\\Map::slice
==============

Returns a subset of the map defined by a starting index and length

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::slice</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\] )

Returns a subset of the map defined by a starting `index` and `length`.

### 参数

`index`  
The index at which the range starts.

If positive, the range will start at that index in the map. If negative,
the range will start that far from the end.

`length`  
If a length is given and is positive, the resulting map will have up to
that many pairs in it. If a length is given and is negative, the range
will stop that many pairs from the end. If the length results in an
overflow, only pairs up to the end of the map will be included. If a
length is not provided, the resulting map will contain all pairs between
the index and the end of the map.

### 返回值

A subset of the map defined by a starting index and length.

### 范例

**示例 \#1 <span class="function">Ds\\Map::slice</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3, "d" => 4, "e" => 5]);

// Slice from 2 onwards
print_r($map->slice(2)->toArray());

// Slice from 1, for a length of 3
print_r($map->slice(1, 3)->toArray());

// Slice from 1 onwards
print_r($map->slice(1)->toArray());

// Slice from 2 from the end onwards
print_r($map->slice(-2)->toArray());

// Slice from 1 to 1 from the end
print_r($map->slice(1, -1)->toArray());
?>
```

以上例程的输出类似于：

    Array
    (
        [c] => 3
        [d] => 4
        [e] => 5
    )
    Array
    (
        [b] => 2
        [c] => 3
        [d] => 4
    )
    Array
    (
        [b] => 2
        [c] => 3
        [d] => 4
        [e] => 5
    )
    Array
    (
        [d] => 4
        [e] => 5
    )
    Array
    (
        [b] => 2
        [c] => 3
        [d] => 4
    )

Ds\\Map::sort
=============

Sorts the map in-place by value

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Map::sort</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Sorts the map in-place by value, using an optional `comparator`
function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Map::sort</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);
$map->sort();

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => c
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => a
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => b
                [value] => 3
            )

    )

**示例 \#2 <span class="function">Ds\\Map::sort</span> example using a
comparator**

``` php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);

$map->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($map);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => b
                [value] => 3
            )

        [1] => Ds\Pair Object
            (
                [key] => a
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 1
            )

    )

Ds\\Map::sorted
===============

Returns a copy, sorted by value

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Returns a copy, sorted by value using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

Returns a copy of the map, sorted by value.

### 范例

**示例 \#1 <span class="function">Ds\\Map::sort</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);

print_r($map->sorted());
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => c
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => a
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => b
                [value] => 3
            )

    )

**示例 \#2 <span class="function">Ds\\Map::sort</span> example using a
comparator**

``` php
<?php
$map = new \Ds\Map(["a" => 2, "b" => 3, "c" => 1]);

// Reverse
$sorted = $map->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => b
                [value] => 3
            )

        [1] => Ds\Pair Object
            (
                [key] => a
                [value] => 2
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 1
            )

    )

Ds\\Map::sum
============

Returns the sum of all values in the map

### 说明

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">Ds\\Map::sum</span> ( <span
class="methodparam">void</span> )

Returns the sum of all values in the map.

> **Note**:
>
> Arrays and objects are considered equal to zero when calculating the
> sum.

### 参数

此函数没有参数。

### 返回值

The sum of all the values in the map as either a <span
class="type">float</span> or <span class="type">int</span> depending on
the values in the map.

### 范例

**示例 \#1 <span class="function">Ds\\Map::sum</span> integer example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->sum());
?>
```

以上例程的输出类似于：

    int(6)

**示例 \#2 <span class="function">Ds\\Map::sum</span> float example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2.5, "c" => 3]);
var_dump($map->sum());
?>
```

以上例程的输出类似于：

    float(6.5)

Ds\\Map::toArray
================

Converts the map to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\Map::toArray</span> ( <span
class="methodparam">void</span> )

Converts the map to an <span class="type">array</span>.

**Caution**

Maps where non-scalar keys are can't be converted to an <span
class="type">array</span>.

**Caution**

An <span class="type">array</span> will treat all numeric keys as
integers, eg. `"1"` and `1` as keys in the map will only result in `1`
being included in the array.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the map.

### 范例

**示例 \#1 <span class="function">Ds\\Map::toArray</span> example**

``` php
<?php
$map = new \Ds\Map([
    "a" => 1,
    "b" => 2,
    "c" => 3,
]);

var_dump($map->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      ["a"]=>
      int(1)
      ["b"]=>
      int(2)
      ["c"]=>
      int(3)
    }

Ds\\Map::union
==============

Creates a new map using values from the current instance and another map

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::union</span> ( <span
class="methodparam"><span class="type">Ds\\Map</span> `$map`</span> )

Creates a new map that contains the pairs of the current instance as
well as the pairs of another `map`.

`A ∪ B = {x: x ∈ A ∨ x ∈ B}`

> **Note**:
>
> Values of the current instance will be overwritten by those provided
> where keys are equal.

### 参数

`map`  
The other map, to combine with the current instance.

### 返回值

A new map containing all the pairs of the current instance as well as
another `map`.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Union_(set_theory)" class="link external">» Union</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Map::union</span> example**

``` php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 3, "c" => 4, "d" => 5]);

print_r($a->union($b));
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => b
                [value] => 3
            )

        [2] => Ds\Pair Object
            (
                [key] => c
                [value] => 4
            )

        [3] => Ds\Pair Object
            (
                [key] => d
                [value] => 5
            )

    )

Ds\\Map::values
===============

Returns a sequence of the map's values

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\Sequence</span> <span
class="methodname">Ds\\Map::values</span> ( <span
class="methodparam">void</span> )

Returns a sequence containing all the values of the map, in the same
order.

### 参数

此函数没有参数。

### 返回值

A <span class="classname">Ds\\Sequence</span> containing all the values
of the map.

### 范例

**示例 \#1 <span class="function">Ds\\Map::values</span> example**

``` php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
var_dump($map->values());
?>
```

以上例程的输出类似于：

    object(Ds\Vector)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Map::xor
============

Creates a new map using keys of either the current instance or of
another map, but not of both

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Map</span>
<span class="methodname">Ds\\Map::xor</span> ( <span
class="methodparam"><span class="type">Ds\\Map</span> `$map`</span> )

Creates a new map containing keys of the current instance as well as
another `map`, but not of both.

`A ⊖ B = {x : x ∈ (A \ B) ∪ (B \ A)}`

### 参数

`map`  
The other map.

### 返回值

A new map containing keys in the current instance as well as another
`map`, but not in both.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Symmetric_difference" class="link external">» Symmetric Difference</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Map::xor</span> example**

``` php
<?php
$a = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);
$b = new \Ds\Map(["b" => 4, "c" => 5, "d" => 6]);

print_r($a->xor($b));
?>
```

以上例程的输出类似于：

    Ds\Map Object
    (
        [0] => Ds\Pair Object
            (
                [key] => a
                [value] => 1
            )

        [1] => Ds\Pair Object
            (
                [key] => d
                [value] => 6
            )

    )

简介
----

A pair is used by <span class="classname">Ds\\Map</span> to pair keys
with values.

类摘要
------

**Ds\\Pair**

<span class="ooclass"> class **Ds\\Pair** </span> <span
class="oointerface">implements <span
class="interfacename">JsonSerializable</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$key`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \]\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">copy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

}

Ds\\Pair::clear
===============

Removes all values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Pair::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the pair.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Pair::clear</span> example**

``` php
<?php
$pair = new \Ds\Pair("a", 1);
print_r($pair);

$pair->clear();
print_r($pair);
?>
```

以上例程的输出类似于：

    Ds\Pair Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Pair Object
    (
    )

Ds\\Pair::\_\_construct
=======================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\Pair::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$key`</span> \[,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> \]\] )

Creates a new instance using a given `key` and `value`.

### 参数

`key`  
The key.

`value`  
The value.

Ds\\Pair::copy
==============

Returns a shallow copy of the pair

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Pair</span>
<span class="methodname">Ds\\Pair::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the pair.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the pair.

### 范例

**示例 \#1 <span class="function">Ds\\Pair::copy</span> example**

``` php
<?php
$a = new \Ds\Pair("a", 1);
$b = $a->copy();

$a->key = "x";

print_r($a);
print_r($b);
?>
```

以上例程的输出类似于：

    Ds\Pair Object
    (
        [key] => x
        [value] => 1
    )
    Ds\Pair Object
    (
        [key] => a
        [value] => 1
    )

Ds\\Pair::isEmpty
=================

Returns whether the pair is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Pair::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the pair is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the pair is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Pair::isEmpty</span> example**

``` php
<?php
$a = new \Ds\Pair("a", 1);
$b = new \Ds\Pair();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Pair::jsonSerialize
=======================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\Pair::toArray
=================

Converts the pair to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\Pair::toArray</span> ( <span
class="methodparam">void</span> )

Converts the pair to an <span class="type">array</span>.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the pair.

### 范例

**示例 \#1 <span class="function">Ds\\Pair::toArray</span> example**

``` php
<?php
$pair = new \Ds\Pair("a", 1);

var_dump($pair->toArray());
?>
```

以上例程的输出类似于：

    array(2) {
      ["key"]=>
      string(1) "a"
      ["value"]=>
      int(1)
    }

简介
----

A Set is a sequence of unique values. This implementation uses the same
hash table as <span class="classname">Ds\\Map</span>, where values are
used as keys and the mapped value is ignored.

Strengths
---------

-   Values can be any type, including objects.
-   Supports array syntax (square brackets).
-   Insertion order is preserved.
-   Automatically frees allocated memory when its size drops low enough.
-   <span class="function">add</span>, <span
    class="function">remove</span> and <span
    class="function">contains</span> are all O(1).

Weaknesses
----------

-   Doesn’t support <span class="function">push</span>, <span
    class="function">pop</span>, <span class="function">insert</span>,
    <span class="function">shift</span>, or <span
    class="function">unshift</span>.
-   <span class="function">get</span> is O(n) if there are deleted
    values in the buffer before the accessed index, O(1) otherwise.

类摘要
------

**Ds\\Set**

<span class="ooclass"> class **Ds\\Set** </span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Collection</span> </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Ds\Set::MIN_CAPACITY` <span class="initializer"> = 16</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">add</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$...values`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">contains</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">copy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">diff</span> ( <span class="methodparam"><span
class="type">Ds\\Set</span> `$set`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">first</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">get</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">intersect</span> ( <span
class="methodparam"><span class="type">Ds\\Set</span> `$set`</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">join</span> (\[ <span class="methodparam"><span
class="type">string</span> `$glue`</span> \] )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">last</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">merge</span> ( <span class="methodparam"><span
class="type">mixed</span> `$values`</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">reduce</span> ( <span class="methodparam"><span
class="type">callable</span> `$callback`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$initial`</span> \]
)

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">remove</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">reverse</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">reversed</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">slice</span> ( <span class="methodparam"><span
class="type">int</span> `$index`</span> \[, <span
class="methodparam"><span class="type">int</span> `$length`</span> \] )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">sort</span> (\[ <span class="methodparam"><span
class="type">callable</span> `$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">sum</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">union</span> ( <span class="methodparam"><span
class="type">Ds\\Set</span> `$set`</span> )

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">xor</span> ( <span class="methodparam"><span
class="type">Ds\\Set</span> `$set`</span> )

}

预定义常量
----------

**`Ds\Set::MIN_CAPACITY`**  

Ds\\Set::add
============

Adds values to the set

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Set::add</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Adds all given values to the set that haven't already been added.

> **Note**:
>
> Values of type <span class="type">object</span> are supported. If an
> object implements <span class="classname">Ds\\Hashable</span>,
> equality will be determined by the object's `equals` function. If an
> object does not implement <span class="classname">Ds\\Hashable</span>,
> objects must be references to the same instance to be considered
> equal.

**Caution**

All comparisons are strict (type and value).

### 参数

`values`  
Values to add to the set.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Set::add</span> example using
integers**

``` php
<?php
$set = new \Ds\Set();

$set->add(1);
$set->add(1);
$set->add(2);
$set->add(3);

// Strict comparison would not treat these the same as int(1)
$set->add("1");
$set->add(true);

var_dump($set);
?>
```

以上例程的输出类似于：

    object(Ds\Set)#1 (5) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
      [3]=>
      string(1) "1"
      [4]=>
      bool(true)
    }

**示例 \#2 <span class="function">Ds\\Set::add</span> example using
objects**

``` php
<?php
class HashableObject implements \Ds\Hashable
{
    /**
     * An arbitrary value to use as the hash value. Does not define equality.
     */
    private $value;

    public function __construct($value)
    {
        $this->value = $value;
    }

    public function hash()
    {
        return $this->value;
    }

    public function equals($obj): bool
    {
        return $this->value === $obj->value;
    }
}

$set = new \Ds\Set();

$obj = new \ArrayIterator([]);

// Adding the same instance multiple times will only add the first.
$set->add($obj);
$set->add($obj);

// Adding multiple instances of the same object will add them all.
$set->add(new \stdClass());
$set->add(new \stdClass());

// Adding multiple instances of equal hashable objects will only add the first.
$set->add(new \HashableObject(1));
$set->add(new \HashableObject(1));
$set->add(new \HashableObject(2));
$set->add(new \HashableObject(2));

var_dump($set);
?>
```

以上例程的输出类似于：

    object(Ds\Set)#1 (5) {
      [0]=>
      object(ArrayIterator)#2 (1) {
        ["storage":"ArrayIterator":private]=>
        array(0) {
        }
      }
      [1]=>
      object(stdClass)#3 (0) {
      }
      [2]=>
      object(stdClass)#4 (0) {
      }
      [3]=>
      object(HashableObject)#5 (1) {
        ["value":"HashableObject":private]=>
        int(1)
      }
      [4]=>
      object(HashableObject)#6 (1) {
        ["value":"HashableObject":private]=>
        int(2)
      }
    }

Ds\\Set::allocate
=================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Set::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Allocates enough memory for a required capacity.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

> **Note**:
>
> Capacity will always be rounded up to the nearest power of 2.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Set::allocate</span> example**

``` php
<?php
$set = new \Ds\Set();
var_dump($set->capacity());

$set->allocate(100);
var_dump($set->capacity());
?>
```

以上例程的输出类似于：

    int(16)
    int(128)

Ds\\Set::capacity
=================

Returns the current capacity

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\Set::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

### 范例

**示例 \#1 <span class="function">Ds\\Set::capacity</span> example**

``` php
<?php
$set = new \Ds\Set();
var_dump($set->capacity());

$set->push(...range(1, 50));
var_dump($set->capacity());
?>
```

以上例程的输出类似于：

    int(16)
    int(64)

Ds\\Set::clear
==============

Removes all values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Set::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the set.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Set::clear</span> example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);
print_r($set);

$set->clear();
print_r($set);
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Set Object
    (
    )

Ds\\Set::\_\_construct
======================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\Set::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Creates a new instance, using either a <span
class="classname">traversable</span> object or an <span
class="type">array</span> for the initial `values`.

### 参数

`values`  
A traversable object or an <span class="type">array</span> to use for
the initial values.

### 范例

**示例 \#1 <span class="function">Ds\\Set::\_\_construct</span>
example**

``` php
<?php
$set = new \Ds\Set();
var_dump($set);

$set = new \Ds\Set([1, 2, 3]);
var_dump($set);
?>
```

以上例程的输出类似于：

    object(Ds\Set)#1 (0) {
    }
    object(Ds\Set)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Set::contains
=================

Determines if the set contains all values

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Set::contains</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Determines if the set contains all values.

> **Note**:
>
> Values of type <span class="type">object</span> are supported. If an
> object implements <span class="classname">Ds\\Hashable</span>,
> equality will be determined by the object's `equals` function. If an
> object does not implement <span class="classname">Ds\\Hashable</span>,
> objects must be references to the same instance to be considered
> equal.

**Caution**

All comparisons are strict (type and value).

### 参数

`values`  
Values to check.

### 返回值

**`FALSE`** if any of the provided `values` are not in the set,
**`TRUE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Set::contains</span> example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->contains(1));                // true
var_dump($set->contains(1, 2));             // true
var_dump($set->contains(...[1, 2]));        // true

var_dump($set->contains("1"));              // false
var_dump($set->contains(...[1, 2, 3, 4]));  // false

var_dump($set->contains(...[]));            // true
?>
```

以上例程的输出类似于：

    bool(true)
    bool(true)
    bool(true)
    bool(false)
    bool(false)
    bool(true)

Ds\\Set::copy
=============

Returns a shallow copy of the set

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the set.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the set.

### 范例

**示例 \#1 <span class="function">Ds\\Set::copy</span> example**

``` php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = $a->copy();

// Updating the copy doesn't affect the original
$b->add(4);

print_r($a);
print_r($b);
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Set Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
    )

Ds\\Set::count
==============

Returns the number of values in the set

See <span class="function">Countable::count</span>

Ds\\Set::diff
=============

Creates a new set using values that aren't in another set

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::diff</span> ( <span
class="methodparam"><span class="type">Ds\\Set</span> `$set`</span> )

Creates a new set using values that aren't in another set.

`A \ B = {x ∈ A | x ∉ B}`

### 参数

`set`  
Set containing the values to exclude.

### 返回值

A new set containing all values that were not in the other `set`.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Complement_(set_theory)" class="link external">» Compliment</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Set::diff</span> example**

``` php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->diff($b));
?>
```

以上例程的输出类似于：

    object(Ds\Set)#3 (2) {
      [0]=>
      int(1)
      [1]=>
      int(2)
    }

Ds\\Set::filter
===============

Creates a new set using a <span class="type">callable</span> to
determine which values to include

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::filter</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \] )

Creates a new set using a <span class="type">callable</span> to
determine which values to include.

### 参数

`callback`  
<span class="type">bool</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> )

Optional <span class="type">callable</span> which returns **`TRUE`** if
the value should be included, **`FALSE`** otherwise.

If a callback is not provided, only values which are **`TRUE`** (see
<a href="/language/types/boolean.html#language.types.boolean.casting" class="link">converting to boolean</a>)
will be included.

### 返回值

A new set containing all the values for which either the `callback`
returned **`TRUE`**, or all values that convert to **`TRUE`** if a
`callback` was not provided.

### 范例

**示例 \#1 <span class="function">Ds\\Set::filter</span> example using
callback function**

``` php
<?php
$set = new \Ds\Set([1, 2, 3, 4, 5]);

var_dump($set->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

以上例程的输出类似于：

    object(Ds\Set)#3 (2) {
      [0]=>
      int(2)
      [1]=>
      int(4)
    }

**示例 \#2 <span class="function">Ds\\Set::filter</span> example without
a callback function**

``` php
<?php
$set = new \Ds\Set([0, 1, 'a', true, false]);

var_dump($set->filter());
?>
```

以上例程的输出类似于：

    object(Ds\Set)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      string(1) "a"
      [2]=>
      bool(true)
    }

Ds\\Set::first
==============

Returns the first value in the set

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Set::first</span> ( <span
class="methodparam">void</span> )

Returns the first value in the set.

### 参数

此函数没有参数。

### 返回值

The first value in the set.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Set::first</span> example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->first());
?>
```

以上例程的输出类似于：

    int(1)

Ds\\Set::get
============

Returns the value at a given index

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Set::get</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> )

Returns the value at a given index.

### 参数

`index`  
The index to access, starting at 0.

### 返回值

The value at the requested index.

### 错误／异常

<span class="classname">OutOfRangeException</span> if the index is not
valid.

### 范例

**示例 \#1 <span class="function">Ds\\Set::get</span> example**

``` php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

var_dump($set->get(0));
var_dump($set->get(1));
var_dump($set->get(2));
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

**示例 \#2 <span class="function">Ds\\Set::get</span> example using
array syntax**

``` php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

var_dump($set[0]);
var_dump($set[1]);
var_dump($set[2]);
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Set::intersect
==================

Creates a new set by intersecting values with another set

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::intersect</span> ( <span
class="methodparam"><span class="type">Ds\\Set</span> `$set`</span> )

Creates a new set using values common to both the current instance and
another `set`. In other words, returns a copy of the current instance
with all values removed that are not in the other `set`.

`A ∩ B = {x : x ∈ A ∧ x ∈ B}`

### 参数

`set`  
The other set.

### 返回值

The intersection of the current instance and another `set`.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Intersection_(set_theory)" class="link external">» Intersection</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Set::intersect</span> example**

``` php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->intersect($b));
?>
```

以上例程的输出类似于：

    object(Ds\Set)#3 (1) {
      [0]=>
      int(3)
    }

Ds\\Set::isEmpty
================

Returns whether the set is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Set::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the set is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the set is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Set::isEmpty</span> example**

``` php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Set::join
=============

Joins all values together as a string

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Ds\\Set::join</span> (\[ <span
class="methodparam"><span class="type">string</span> `$glue`</span> \] )

Joins all values together as a string using an optional separator
between each value.

### 参数

`glue`  
An optional string to separate each value.

### 返回值

All values of the set joined together as a string.

### 范例

**示例 \#1 <span class="function">Ds\\Set::join</span> example using a
separator string**

``` php
<?php
$set = new \Ds\Set(["a", "b", "c", 1, 2, 3]);

var_dump($set->join("|"));
?>
```

以上例程的输出类似于：

    string(11) "a|b|c|1|2|3"

**示例 \#2 <span class="function">Ds\\Set::join</span> example without a
separator string**

``` php
<?php
$set = new \Ds\Set(["a", "b", "c", 1, 2, 3]);

var_dump($set->join());
?>
```

以上例程的输出类似于：

    string(11) "abc123"

Ds\\Set::jsonSerialize
======================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\Set::last
=============

Returns the last value in the set

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Set::last</span> ( <span
class="methodparam">void</span> )

Returns the last value in the set.

### 参数

此函数没有参数。

### 返回值

The last value in the set.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Set::last</span> example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->last());
?>
```

以上例程的输出类似于：

    int(3)

Ds\\Set::merge
==============

Returns the result of adding all given values to the set

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::merge</span> ( <span
class="methodparam"><span class="type">mixed</span> `$values`</span> )

Returns the result of adding all given values to the set.

### 参数

`values`  
A <span class="classname">traversable</span> object or an <span
class="type">array</span>.

### 返回值

The result of adding all given values to the set, effectively the same
as adding the values to a copy, then returning that copy.

> **Note**:
>
> The current instance won't be affected.

### 范例

**示例 \#1 <span class="function">Ds\\Set::merge</span> example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->merge([3, 4, 5]));
var_dump($set);
?>
```

以上例程的输出类似于：

    object(Ds\Set)#2 (6) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
      [3]=>
      int(4)
      [4]=>
      int(5)
    }
    object(Ds\Set)#1 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Set::reduce
===============

Reduces the set to a single value using a callback function

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Set::reduce</span> ( <span
class="methodparam"><span class="type">callable</span>
`$callback`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$initial`</span> \] )

Reduces the set to a single value using a callback function.

### 参数

`callback`  
<span class="type">mixed</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$carry`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

`carry`  
The return value of the previous callback, or `initial` if it's the
first iteration.

`value`  
The value of the current iteration.

`initial`  
The initial value of the carry value. Can be **`NULL`**.

### 返回值

The return value of the final callback.

### 范例

**示例 \#1 <span class="function">Ds\\Set::reduce</span> with initial
value example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);

$callback = function($carry, $value) {
    return $carry * $value;
};

var_dump($set->reduce($callback, 5));

// Iterations:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

以上例程的输出类似于：

    int(30)

**示例 \#2 <span class="function">Ds\\Set::reduce</span> without an
initial value example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->reduce(function($carry, $value) {
    return $carry + $value + 5;
}));

// Iterations:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

以上例程的输出类似于：

    int(21)

Ds\\Set::remove
===============

Removes all given values from the set

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Set::remove</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Removes all given `values` from the set, ignoring any that are not in
the set.

### 参数

`values`  
The values to remove.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Set::remove</span> example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3, 4, 5]);

$set->remove(1);            // Remove 1
$set->remove(1, 2);         // Can't find 1, but remove 2
$set->remove(...[3, 4]);    // Remove 3 and 4

var_dump($set);
?>
```

以上例程的输出类似于：

    object(Ds\Set)#1 (1) {
      [0]=>
      int(5)
    }

Ds\\Set::reverse
================

Reverses the set in-place

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Set::reverse</span> ( <span
class="methodparam">void</span> )

Reverses the set in-place.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Set::reverse</span> example**

``` php
<?php
$set = new \Ds\Set(["a", "b", "c"]);
$set->reverse();

print_r($set);
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => c
        [1] => b
        [2] => a
    )

Ds\\Set::reversed
=================

Returns a reversed copy

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::reversed</span> ( <span
class="methodparam">void</span> )

Returns a reversed copy of the set.

### 参数

此函数没有参数。

### 返回值

A reversed copy of the set.

> **Note**:
>
> The current instance is not affected.

### 范例

**示例 \#1 <span class="function">Ds\\Set::reversed</span> example**

``` php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

print_r($set->reversed());
print_r($set);
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => c
        [1] => b
        [2] => a
    )
    Ds\Set Object
    (
        [0] => a
        [1] => b
        [2] => c
    )

Ds\\Set::slice
==============

Returns a sub-set of a given range

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::slice</span> ( <span
class="methodparam"><span class="type">int</span> `$index`</span> \[,
<span class="methodparam"><span class="type">int</span> `$length`</span>
\] )

Creates a sub-set of a given range.

### 参数

`index`  
The index at which the sub-set starts.

If positive, the set will start at that index in the set. If negative,
the set will start that far from the end.

`length`  
If a length is given and is positive, the resulting set will have up to
that many values in it. If the length results in an overflow, only
values up to the end of the set will be included. If a length is given
and is negative, the set will stop that many values from the end. If a
length is not provided, the resulting set will contain all values
between the index and the end of the set.

### 返回值

A sub-set of the given range.

### 范例

**示例 \#1 <span class="function">Ds\\Set::slice</span> example**

``` php
<?php
$set = new \Ds\Set(["a", "b", "c", "d", "e"]);

// Slice from 2 onwards
print_r($set->slice(2));

// Slice from 1, for a length of 3
print_r($set->slice(1, 3));

// Slice from 1 onwards
print_r($set->slice(1));

// Slice from 2 from the end onwards
print_r($set->slice(-2));

// Slice from 1 to 1 from the end
print_r($set->slice(1, -1));
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => c
        [1] => d
        [2] => e
    )
    Ds\Set Object
    (
        [0] => b
        [1] => c
        [2] => d
    )
    Ds\Set Object
    (
        [0] => b
        [1] => c
        [2] => d
        [3] => e
    )
    Ds\Set Object
    (
        [0] => d
        [1] => e
    )
    Ds\Set Object
    (
        [0] => b
        [1] => c
        [2] => d
    )

Ds\\Set::sort
=============

Sorts the set in-place

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Set::sort</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Sorts the set in-place, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Set::sort</span> example**

``` php
<?php
$set = new \Ds\Set([4, 5, 1, 3, 2]);
$set->sort();

print_r($set);
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Set::sort</span> example using a
comparator**

``` php
<?php
$set = new \Ds\Set([4, 5, 1, 3, 2]);

$set->sort(function($a, $b) {
    return $b <=> $a;
});

print_r($set);
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Set::sorted
===============

Returns a sorted copy

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::sorted</span> (\[ <span
class="methodparam"><span class="type">callable</span>
`$comparator`</span> \] )

Returns a sorted copy, using an optional `comparator` function.

### 参数

`comparator`  
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于
0 的整数。注意：在 PHP 7.0.0 之前的版本中，整数的区间为 -2147483648 to
2147483647。

<span class="type">int</span> <span class="methodname"><span
class="replaceable">callback</span></span> ( <span
class="methodparam"><span class="type">mixed</span> `$a`</span>, <span
class="methodparam"><span class="type">mixed</span> `$b`</span> )

**Caution**
Returning *non-integer* values from the comparison function, such as
<span class="type">float</span>, will result in an internal cast to
<span class="type">integer</span> of the callback's return value. So
values such as 0.99 and 0.1 will both be cast to an integer value of 0,
which will compare such values as equal.

### 返回值

Returns a sorted copy of the set.

### 范例

**示例 \#1 <span class="function">Ds\\Set::sorted</span> example**

``` php
<?php
$set = new \Ds\Set([4, 5, 1, 3, 2]);

print_r($set->sorted());
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
        [4] => 5
    )

**示例 \#2 <span class="function">Ds\\Set::sorted</span> example using a
comparator**

``` php
<?php
$set = new \Ds\Set([4, 5, 1, 3, 2]);

$sorted = $set->sorted(function($a, $b) {
    return $b <=> $a;
});

print_r($sorted);
?>
```

以上例程的输出类似于：

    Ds\Set Object
    (
        [0] => 5
        [1] => 4
        [2] => 3
        [3] => 2
        [4] => 1
    )

Ds\\Set::sum
============

Returns the sum of all values in the set

### 说明

<span class="modifier">public</span> <span class="type">number</span>
<span class="methodname">Ds\\Set::sum</span> ( <span
class="methodparam">void</span> )

Returns the sum of all values in the set.

> **Note**:
>
> Arrays and objects are considered equal to zero when calculating the
> sum.

### 参数

此函数没有参数。

### 返回值

The sum of all the values in the set as either a <span
class="type">float</span> or <span class="type">int</span> depending on
the values in the set.

### 范例

**示例 \#1 <span class="function">Ds\\Set::sum</span> integer example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);
var_dump($set->sum());
?>
```

以上例程的输出类似于：

    int(6)

**示例 \#2 <span class="function">Ds\\Set::sum</span> float example**

``` php
<?php
$set = new \Ds\Set([1, 2.5, 3]);
var_dump($set->sum());
?>
```

以上例程的输出类似于：

    float(6.5)

Ds\\Set::toArray
================

Converts the set to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\Set::toArray</span> ( <span
class="methodparam">void</span> )

Converts the set to an <span class="type">array</span>.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the set.

### 范例

**示例 \#1 <span class="function">Ds\\Set::toArray</span> example**

``` php
<?php
$set = new \Ds\Set([1, 2, 3]);

var_dump($set->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Set::union
==============

Creates a new set using values from the current instance and another set

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::union</span> ( <span
class="methodparam"><span class="type">Ds\\Set</span> `$set`</span> )

Creates a new set that contains the values of the current instance as
well as the values of another `set`.

`A ∪ B = {x: x ∈ A ∨ x ∈ B}`

### 参数

`set`  
The other set, to combine with the current instance.

### 返回值

A new set containing all the values of the current instance as well as
another `set`.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Union_(set_theory)" class="link external">» Union</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Set::union</span> example**

``` php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->union($b));
?>
```

以上例程的输出类似于：

    object(Ds\Set)#3 (5) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
      [3]=>
      int(4)
      [4]=>
      int(5)
    }

Ds\\Set::xor
============

Creates a new set using values in either the current instance or in
another set, but not in both

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Set</span>
<span class="methodname">Ds\\Set::xor</span> ( <span
class="methodparam"><span class="type">Ds\\Set</span> `$set`</span> )

Creates a new set containing values in the current instance as well as
another `set`, but not in both.

`A ⊖ B = {x : x ∈ (A \ B) ∪ (B \ A)}`

### 参数

`set`  
The other set.

### 返回值

A new set containing values in the current instance as well as another
`set`, but not in both.

### See Also

-   <a href="https://en.wikipedia.org/wiki/Symmetric_difference" class="link external">» Symmetric Difference</a>
    on Wikipedia

### 范例

**示例 \#1 <span class="function">Ds\\Set::xor</span> example**

``` php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set([3, 4, 5]);

var_dump($a->xor($b));
?>
```

以上例程的输出类似于：

    object(Ds\Set)#3 (4) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(4)
      [3]=>
      int(5)
    }

简介
----

A Stack is a “last in, first out” or “LIFO” collection that only allows
access to the value at the top of the structure and iterates in that
order, destructively.

Uses a <span class="classname">Ds\\Vector</span> internally.

类摘要
------

**Ds\\Stack**

<span class="ooclass"> class **Ds\\Stack** </span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Collection</span> </span> {

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Stack</span>
<span class="methodname">copy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">peek</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$...values`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

}

Ds\\Stack::allocate
===================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Stack::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Ensures that enough memory is allocated for a required capacity. This
removes the need to reallocate the internal as values are added.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

### 返回值

没有返回值。

Ds\\Stack::capacity
===================

Returns the current capacity

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\Stack::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

Ds\\Stack::clear
================

Removes all values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Stack::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the stack.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Stack::clear</span> example**

``` php
<?php
$stack = new \Ds\Stack([1, 2, 3]);
print_r($stack);

$stack->clear();
print_r($stack);
?>
```

以上例程的输出类似于：

    Ds\Stack Object
    (
        [0] => 3
        [1] => 2
        [2] => 1
    )
    Ds\Stack Object
    (
    )

Ds\\Stack::\_\_construct
========================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\Stack::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

Creates a new instance, using either a <span
class="classname">traversable</span> object or an <span
class="type">array</span> for the initial `values`.

### 参数

`values`  
A traversable object or an <span class="type">array</span> to use for
the initial values.

### 范例

**示例 \#1 <span class="function">Ds\\Stack::\_\_construct</span>
example**

``` php
<?php
$stack = new \Ds\Stack();
print_r($stack);

$stack = new \Ds\Stack([1, 2, 3]);
print_r($stack);
?>
```

以上例程的输出类似于：

    Ds\Stack Object
    (
    )
    Ds\Stack Object
    (
        [0] => 3
        [1] => 2
        [2] => 1
    )

Ds\\Stack::copy
===============

Returns a shallow copy of the stack

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Stack</span>
<span class="methodname">Ds\\Stack::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the stack.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the stack.

### 范例

**示例 \#1 <span class="function">Ds\\Stack::copy</span> example**

``` php
<?php
$a = new \Ds\Stack([1, 2, 3]);
$b = $a->copy();

// Updating the copy doesn't affect the original
$b->push(4);

print_r($a);
print_r($b);
?>
```

以上例程的输出类似于：

    Ds\Stack Object
    (
        [0] => 3
        [1] => 2
        [2] => 1
    )
    Ds\Stack Object
    (
        [0] => 4
        [1] => 3
        [2] => 2
        [3] => 1
    )

Ds\\Stack::count
================

Returns the number of values in the stack

See <span class="function">Countable::count</span>

Ds\\Stack::isEmpty
==================

Returns whether the stack is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Stack::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the stack is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the stack is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Stack::isEmpty</span> example**

``` php
<?php
$a = new \Ds\Stack([1, 2, 3]);
$b = new \Ds\Stack();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Stack::jsonSerialize
========================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\Stack::peek
===============

Returns the value at the top of the stack

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Stack::peek</span> ( <span
class="methodparam">void</span> )

Returns the value at the top of the stack, but does not remove it.

### 参数

此函数没有参数。

### 返回值

The value at the top of the stack.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Stack::peek</span> example**

``` php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c");

var_dump($stack->peek());
?>
```

以上例程的输出类似于：

    string(1) "c"

Ds\\Stack::pop
==============

Removes and returns the value at the top of the stack

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Stack::pop</span> ( <span
class="methodparam">void</span> )

Removes and returns the value at the top of the stack.

### 参数

此函数没有参数。

### 返回值

The removed value which was at the top of the stack.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Stack::pop</span> example**

``` php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c");

var_dump($stack->pop());
var_dump($stack->pop());
var_dump($stack->pop());
?>
```

以上例程的输出类似于：

    string(1) "c"
    string(1) "b"
    string(1) "a"

Ds\\Stack::push
===============

Pushes values onto the stack

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Stack::push</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Pushes `values` onto the stack.

### 参数

`values`  
The values to push onto the stack.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Stack::push</span> example**

``` php
<?php
$stack = new \Ds\Stack();

$stack->push("a");
$stack->push("b");
$stack->push("c", "d");
$stack->push(...["e", "f"]);

print_r($stack);
?>
```

以上例程的输出类似于：

    Ds\Stack Object
    (
        [0] => a
        [1] => b
        [2] => c
        [3] => d
        [4] => e
        [5] => f
    )

Ds\\Stack::toArray
==================

Converts the stack to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\Stack::toArray</span> ( <span
class="methodparam">void</span> )

Converts the stack to an <span class="type">array</span>.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the stack.

### 范例

**示例 \#1 <span class="function">Ds\\Stack::toArray</span> example**

``` php
<?php
$stack = new \Ds\Stack([1, 2, 3]);

var_dump($stack->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      int(3)
      [1]=>
      int(2)
      [2]=>
      int(1)
    }

简介
----

A Queue is a “first in, first out” or “FIFO” collection that only allows
access to the value at the front of the queue and iterates in that
order, destructively.

类摘要
------

**Ds\\Queue**

<span class="ooclass"> class **Ds\\Queue** </span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Collection</span> </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Ds\Queue::MIN_CAPACITY` <span class="initializer"> = 8</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">Ds\\Queue</span>
<span class="methodname">copy</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">peek</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> (\[ <span class="methodparam"><span
class="type">mixed</span> `$...values`</span> \] )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`Ds\Queue::MIN_CAPACITY`**  

Ds\\Queue::allocate
===================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Queue::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Ensures that enough memory is allocated for a required capacity. This
removes the need to reallocate the internal as values are added.

> **Note**:
>
> Capacity will always be rounded up to the nearest power of 2.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

> **Note**:
>
> Capacity will always be rounded up to the nearest power of 2.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Queue::allocate</span> example**

``` php
<?php
$queue = new \Ds\Queue();
var_dump($queue->capacity());

$queue->allocate(100);
var_dump($queue->capacity());
?>
```

以上例程的输出类似于：

    int(8)
    int(128)

Ds\\Queue::capacity
===================

Returns the current capacity

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\Queue::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

### 范例

**示例 \#1 <span class="function">Ds\\Queue::capacity</span> example**

``` php
<?php
$queue = new \Ds\Queue();
var_dump($queue->capacity());

$queue->push(...range(1, 50));
var_dump($queue->capacity());
?>
```

以上例程的输出类似于：

    int(8)
    int(64)

Ds\\Queue::clear
================

Removes all values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Queue::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the queue.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Queue::clear</span> example**

``` php
<?php
$queue = new \Ds\Queue([1, 2, 3]);
print_r($queue);

$queue->clear();
print_r($queue);
?>
```

以上例程的输出类似于：

    Ds\Queue Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Queue Object
    (
    )

Ds\\Queue::\_\_construct
========================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\Queue::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$values`</span> \]
)

Creates a new instance, using either a <span
class="classname">traversable</span> object or an <span
class="type">array</span> for the initial `values`.

### 参数

`values`  
A traversable object or an <span class="type">array</span> to use for
the initial values.

### 范例

**示例 \#1 <span class="function">Ds\\Queue::\_\_construct</span>
example**

``` php
<?php
$queue = new \Ds\Queue();
var_dump($queue);


$queue = new \Ds\Queue([1, 2, 3]);
var_dump($queue);
?>
```

以上例程的输出类似于：

    object(Ds\Queue)#2 (0) {
    }
    object(Ds\Queue)#2 (3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

Ds\\Queue::copy
===============

Returns a shallow copy of the queue

### 说明

<span class="modifier">public</span> <span class="type">Ds\\Queue</span>
<span class="methodname">Ds\\Queue::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the queue.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the queue.

### 范例

**示例 \#1 <span class="function">Ds\\Queue::copy</span> example**

``` php
<?php
$a = new \Ds\Queue([1, 2, 3]);
$b = $a->copy();

// Updating the copy doesn't affect the original
$b->push(4);

print_r($a);
print_r($b);
?>
```

以上例程的输出类似于：

    Ds\Queue Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
    )
    Ds\Queue Object
    (
        [0] => 1
        [1] => 2
        [2] => 3
        [3] => 4
    )

Ds\\Queue::count
================

Returns the number of values in the queue

See <span class="function">Countable::count</span>

Ds\\Queue::isEmpty
==================

Returns whether the queue is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\Queue::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the queue is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the queue is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\Queue::isEmpty</span> example**

``` php
<?php
$a = new \Ds\Queue([1, 2, 3]);
$b = new \Ds\Queue();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\Queue::jsonSerialize
========================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\Queue::peek
===============

Returns the value at the front of the queue

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Queue::peek</span> ( <span
class="methodparam">void</span> )

Returns the value at the front of the queue, but does not remove it.

### 参数

此函数没有参数。

### 返回值

The value at the front of the queue.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Queue::peek</span> example**

``` php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c");

var_dump($queue->peek());
?>
```

以上例程的输出类似于：

    string(1) "a"

Ds\\Queue::pop
==============

Removes and returns the value at the front of the queue

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\Queue::pop</span> ( <span
class="methodparam">void</span> )

Removes and returns the value at the front of the queue.

### 参数

此函数没有参数。

### 返回值

The removed value which was at the front of the queue.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\Queue::pop</span> example**

``` php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c");

var_dump($queue->pop());
var_dump($queue->pop());
var_dump($queue->pop());
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\Queue::push
===============

Pushes values into the queue

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\Queue::push</span> (\[ <span
class="methodparam"><span class="type">mixed</span> `$...values`</span>
\] )

Pushes `values` into the queue.

### 参数

`values`  
The values to push into the queue.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\Queue::push</span> example**

``` php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c", "d");
$queue->push(...["e", "f"]);

print_r($queue);
?>
```

以上例程的输出类似于：

    Ds\Queue Object
    (
        [0] => a
        [1] => b
        [2] => c
        [3] => d
        [4] => e
        [5] => f
    )

Ds\\Queue::toArray
==================

Converts the queue to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\Queue::toArray</span> ( <span
class="methodparam">void</span> )

Converts the queue to an <span class="type">array</span>.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

> **Note**:
>
> This method is not destructive.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the queue.

### 范例

**示例 \#1 <span class="function">Ds\\Queue::toArray</span> example**

``` php
<?php
$queue = new \Ds\Queue([1, 2, 3]);

var_dump($queue->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      int(1)
      [1]=>
      int(2)
      [2]=>
      int(3)
    }

简介
----

A PriorityQueue is very similar to a Queue. Values are pushed into the
queue with an assigned priority, and the value with the highest priority
will always be at the front of the queue.

Implemented using a max heap.

> **Note**:
>
> "First in, first out" ordering is preserved for values with the same
> priority.

> **Note**:
>
> Iterating over a PriorityQueue is destructive, equivalent to
> successive pop operations until the queue is empty.

类摘要
------

**Ds\\PriorityQueue**

<span class="ooclass"> class **Ds\\PriorityQueue** </span> <span
class="oointerface">implements <span
class="interfacename">Ds\\Collection</span> </span> {

/\* Constants \*/

<span class="modifier">const</span> <span class="type">int</span>
`Ds\PriorityQueue::MIN_CAPACITY` <span class="initializer"> = 8</span> ;

/\* 方法 \*/

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">capacity</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">clear</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span
class="type">Ds\\PriorityQueue</span> <span
class="methodname">copy</span> ( <span class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">isEmpty</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">peek</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">pop</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">push</span> ( <span class="methodparam"><span
class="type">mixed</span> `$value`</span> , <span
class="methodparam"><span class="type">int</span> `$priority`</span> )

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">toArray</span> ( <span
class="methodparam">void</span> )

}

预定义常量
----------

**`Ds\PriorityQueue::MIN_CAPACITY`**  

Ds\\PriorityQueue::allocate
===========================

Allocates enough memory for a required capacity

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\PriorityQueue::allocate</span> ( <span
class="methodparam"><span class="type">int</span> `$capacity`</span> )

Ensures that enough memory is allocated for a required capacity. This
removes the need to reallocate the internal as values are added.

### 参数

`capacity`  
The number of values for which capacity should be allocated.

> **Note**:
>
> Capacity will stay the same if this value is less than or equal to the
> current capacity.

> **Note**:
>
> Capacity will always be rounded up to the nearest power of 2.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::allocate</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue->capacity());

$queue->allocate(100);
var_dump($queue->capacity());
?>
```

以上例程的输出类似于：

    int(8)
    int(128)

Ds\\PriorityQueue::capacity
===========================

Returns the current capacity

### 说明

<span class="modifier">public</span> <span class="type">int</span> <span
class="methodname">Ds\\PriorityQueue::capacity</span> ( <span
class="methodparam">void</span> )

Returns the current capacity.

### 参数

此函数没有参数。

### 返回值

The current capacity.

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::capacity</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue->capacity());
?>
```

以上例程的输出类似于：

    int(8)

Ds\\PriorityQueue::clear
========================

Removes all values

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\PriorityQueue::clear</span> ( <span
class="methodparam">void</span> )

Removes all values from the queue.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::clear</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

$queue->clear();
print_r($queue);
?>
```

以上例程的输出类似于：

    Ds\PriorityQueue Object
    (
    )

Ds\\PriorityQueue::\_\_construct
================================

Creates a new instance

### 说明

<span class="modifier">public</span> <span
class="methodname">Ds\\PriorityQueue::\_\_construct</span> ( <span
class="methodparam">void</span> )

Creates a new instance.

### 范例

**示例 \#1 <span
class="function">Ds\\PriorityQueue::\_\_construct</span> example**

``` php
<?php
$queue = new \Ds\PriorityQueue();
var_dump($queue);
?>
```

以上例程的输出类似于：

    object(Ds\PriorityQueue)#1 (0) {
    }

Ds\\PriorityQueue::copy
=======================

Returns a shallow copy of the queue

### 说明

<span class="modifier">public</span> <span
class="type">Ds\\PriorityQueue</span> <span
class="methodname">Ds\\PriorityQueue::copy</span> ( <span
class="methodparam">void</span> )

Returns a shallow copy of the queue.

### 参数

此函数没有参数。

### 返回值

Returns a shallow copy of the queue.

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::copy</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->copy());
?>
```

以上例程的输出类似于：

    Ds\PriorityQueue Object
    (
        [0] => b
        [1] => c
        [2] => a
    )

Ds\\PriorityQueue::count
========================

Returns the number of values in the queue

See <span class="function">Countable::count</span>

Ds\\PriorityQueue::isEmpty
==========================

Returns whether the queue is empty

### 说明

<span class="modifier">public</span> <span class="type">bool</span>
<span class="methodname">Ds\\PriorityQueue::isEmpty</span> ( <span
class="methodparam">void</span> )

Returns whether the queue is empty.

### 参数

此函数没有参数。

### 返回值

Returns **`TRUE`** if the queue is empty, **`FALSE`** otherwise.

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::isEmpty</span>
example**

``` php
<?php
$a = new \Ds\PriorityQueue();
$b = new \Ds\PriorityQueue();

$a->push("a",  5);
$a->push("b", 15);
$a->push("c", 10);

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

以上例程的输出类似于：

    bool(false)
    bool(true)

Ds\\PriorityQueue::jsonSerialize
================================

Returns a representation that can be converted to JSON

See <span class="function">JsonSerializable::jsonSerialize</span>

> **Note**:
>
> You should never need to call this directly.

Ds\\PriorityQueue::peek
=======================

Returns the value at the front of the queue

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\PriorityQueue::peek</span> ( <span
class="methodparam">void</span> )

Returns the value at the front of the queue, but does not remove it.

### 参数

此函数没有参数。

### 返回值

The value at the front of the queue.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::peek</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

var_dump($queue->peek());
?>
```

以上例程的输出类似于：

    string(1) "b"

Ds\\PriorityQueue::pop
======================

Removes and returns the value with the highest priority

### 说明

<span class="modifier">public</span> <span class="type">mixed</span>
<span class="methodname">Ds\\PriorityQueue::pop</span> ( <span
class="methodparam">void</span> )

Removes and returns the value at the front of the queue, ie. the value
with the highest priority.

> **Note**:
>
> Values with equal priority fall back to FIFO (first in first out).

### 参数

此函数没有参数。

### 返回值

The removed value which was at the front of the queue.

### 错误／异常

<span class="classname">UnderflowException</span> if empty.

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::pop</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->pop());
print_r($queue->pop());
print_r($queue->pop());
?>
```

以上例程的输出类似于：

    string(1) "a"
    string(1) "b"
    string(1) "c"

Ds\\PriorityQueue::push
=======================

Pushes values into the queue

### 说明

<span class="modifier">public</span> <span class="type">void</span>
<span class="methodname">Ds\\PriorityQueue::push</span> ( <span
class="methodparam"><span class="type">mixed</span> `$value`</span> ,
<span class="methodparam"><span class="type">int</span>
`$priority`</span> )

Pushes a `value` with a given `priority` into the queue.

### 参数

`value`  
The value to push into the queue.

`priority`  
The priority associated with the value.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::push</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

print_r($queue->pop());
print_r($queue->pop());
print_r($queue->pop());
?>
```

以上例程的输出类似于：

    string(1) "b"
    string(1) "c"
    string(1) "a"

Ds\\PriorityQueue::toArray
==========================

Converts the queue to an <span class="type">array</span>

### 说明

<span class="modifier">public</span> <span class="type">array</span>
<span class="methodname">Ds\\PriorityQueue::toArray</span> ( <span
class="methodparam">void</span> )

Converts the queue to an <span class="type">array</span>.

> **Note**:
>
> This method is not destructive.

> **Note**:
>
> Casting to an <span class="type">array</span> is not supported yet.

### 参数

此函数没有参数。

### 返回值

An <span class="type">array</span> containing all the values in the same
order as the queue.

### 范例

**示例 \#1 <span class="function">Ds\\PriorityQueue::toArray</span>
example**

``` php
<?php
$queue = new \Ds\PriorityQueue();

$queue->push("a",  5);
$queue->push("b", 15);
$queue->push("c", 10);

var_dump($queue->toArray());
?>
```

以上例程的输出类似于：

    array(3) {
      [0]=>
      string(1) "b"
      [1]=>
      string(1) "c"
      [2]=>
      string(1) "a"
    }

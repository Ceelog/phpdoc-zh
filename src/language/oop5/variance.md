Covariance and Contravariance
-----------------------------

In PHP 7.2.0, partial contravariance was introduced by removing type
restrictions on parameters in a child method. As of PHP 7.4.0, full
covariance and contravariance support was added.

Covariance allows a child's method to return a more specific type than
the return type of its parent's method. Whereas, contravariance allows a
parameter type to be less specific in a child method, than that of its
parent.

### Covariance

To illustrate how covariance works, a simple abstract parent class,
`Animal` is created. `Animal` will be extended by children classes,
`Cat`, and `Dog`.

``` php
<?php

abstract class Animal
{
    protected string $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }

    abstract public function speak();
}

class Dog extends Animal
{
    public function speak()
    {
        echo $this->name . " barks";
    }
}

class Cat extends Animal 
{
    public function speak()
    {
        echo $this->name . " meows";
    }
}
```

Note that there aren't any methods which return values in this example.
A few factories will be added which return a new object of class type
`Animal`, `Cat`, or `Dog`.

``` php
<?php

interface AnimalShelter
{
    public function adopt(string $name): Animal;
}

class CatShelter implements AnimalShelter
{
    public function adopt(string $name): Cat // instead of returning class type Animal, it can return class type Cat
    {
        return new Cat($name);
    }
}

class DogShelter implements AnimalShelter
{
    public function adopt(string $name): Dog // instead of returning class type Animal, it can return class type Dog
    {
        return new Dog($name);
    }
}

$kitty = (new CatShelter)->adopt("Ricky");
$kitty->speak();
echo "\n";

$doggy = (new DogShelter)->adopt("Mavrick");
$doggy->speak();
```

以上例程会输出：

    Ricky meows
    Mavrick barks

### Contravariance

Continuing with the previous example with the classes `Animal`, `Cat`,
and `Dog`, a class called `Food` and `AnimalFood` will be included, and
a method `eat(AnimalFood $food)` is added to the `Animal` abstract
class.

``` php
<?php

class Food {}

class AnimalFood extends Food {}

abstract class Animal
{
    protected string $name;

    public function __construct(string $name)
    {
        $this->name = $name;
    }

    public function eat(AnimalFood $food)
    {
        echo $this->name . " eats " . get_class($food);
    }
}
```

In order to see the behavior of contravariance, the `eat` method is
overridden in the `Dog` class to allow any `Food` type object. The `Cat`
class remains unchanged.

``` php
<?php

class Dog extends Animal
{
    public function eat(Food $food) {
        echo $this->name . " eats " . get_class($food);
    }
}
```

The next example will show the behavior of contravariance.

``` php
<?php

$kitty = (new CatShelter)->adopt("Ricky");
$catFood = new AnimalFood();
$kitty->eat($catFood);
echo "\n";

$doggy = (new DogShelter)->adopt("Mavrick");
$banana = new Food();
$doggy->eat($banana);
```

以上例程会输出：

    Ricky eats AnimalFood
    Mavrick eats Food

But what happens if `$kitty` tries to `eat` the `$banana`?

``` php
$kitty->eat($banana);
```

以上例程会输出：

    Fatal error: Uncaught TypeError: Argument 1 passed to Animal::eat() must be an instance of AnimalFood, instance of Food given

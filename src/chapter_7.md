# Object-Oriented Programming

Object-oriented programming (OOP) is a programming paradigm that uses "objects" to design applications and computer programs. Python is an object-oriented programming language by design, making it one of the most popular languages for both beginners and experienced developers.

In this section, we'll cover:
1. Defining Classes
2. Creating Objects
3. Instance Variables
4. Class Variables
5. Methods: Instance Methods, Class Methods, Static Methods
6. Inheritance
7. Polymorphism

## 1. Defining Classes

In Python, a class is defined using the `class` keyword. A class serves as a blueprint for objects.

```python
class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species

    def make_sound(self):
        pass
```

In the example above, `Animal` is a class with an initializer (`__init__`) method that sets the `name` and `species` attributes.

## 2. Creating Objects

To create an instance of a class, you call the class using its name and pass any required arguments.

```python
dog = Animal("Buddy", "Dog")
cat = Animal("Whiskers", "Cat")
```

Here, `dog` and `cat` are objects (instances) of the class `Animal`.

## 3. Instance Variables

Instance variables are variables that are unique to each instance of a class. They are typically defined inside the `__init__` method.

```python
class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species
        self.age = 0   # Instance variable

dog = Animal("Buddy", "Dog")
print(dog.name)  # Output: Buddy
print(dog.age)   # Output: 0
```

## 4. Class Variables

Class variables are shared across all instances of a class. They are defined within the class but outside any methods.

```python
class Animal:
    kingdom = "Animalia"  # Class variable

    def __init__(self, name, species):
        self.name = name
        self.species = species

print(Animal.kingdom)  # Output: Animalia
dog = Animal("Buddy", "Dog")
print(dog.kingdom)     # Output: Animalia
```

## 5. Methods

Methods are functions defined inside a class that operate on instances of that class. There are three types of methods in Python: instance methods, class methods, and static methods.

**Instance Methods:**
These methods take `self` as the first parameter and can modify the object's state.

```python
class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species

    def rename(self, new_name):
        self.name = new_name

dog = Animal("Buddy", "Dog")
dog.rename("Max")
print(dog.name)  # Output: Max
```

**Class Methods:**
These methods take `cls` as the first parameter and can modify the class state. They are decorated with `@classmethod`.

```python
class Animal:
    kingdom = "Animalia"

    def __init__(self, name, species):
        self.name = name
        self.species = species

    @classmethod
    def set_kingdom(cls, new_kingdom):
        cls.kingdom = new_kingdom

Animal.set_kingdom("NewKingdom")
print(Animal.kingdom)  # Output: NewKingdom
```

**Static Methods:**
Static methods do not take `self` or `cls` as the first parameter and cannot modify the object or class state. They are decorated with `@staticmethod`.

```python
class Animal:
    @staticmethod
    def is_animal(name):
        return name.lower() in ['dog', 'cat', 'bird']

print(Animal.is_animal("Dog"))  # Output: True
```

## 6. Inheritance

Inheritance allows a class to inherit attributes and methods from another class.

```python
class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species

    def make_sound(self):
        return "Some sound"

class Dog(Animal):
    def __init__(self, name):
        super().__init__(name, "Dog")

    def make_sound(self):
        return "Bark"

dog = Dog("Buddy")
print(dog.make_sound())  # Output: Bark
```

In the example above, `Dog` inherits from `Animal` and overrides the `make_sound` method.

## 7. Polymorphism

Polymorphism allows objects of different classes to be treated as objects of a common super class. It is typically used with inheritance.

```python
class Animal:
    def make_sound(self):
        pass

class Dog(Animal):
    def make_sound(self):
        return "Bark"

class Cat(Animal):
    def make_sound(self):
        return "Meow"

def make_animal_sound(animal):
    print(animal.make_sound())

dog = Dog()
cat = Cat()
make_animal_sound(dog)  # Output: Bark
make_animal_sound(cat)  # Output: Meow
```

In this example, both `Dog` and `Cat` are treated as `Animal` and can be passed to the `make_animal_sound` function.

## Conclusion

This section has covered the basics of object-oriented programming in Python 3.13, including defining classes, creating objects, instance variables, class variables, methods, inheritance, and polymorphism. Understanding these concepts will enable you to write more organized, reusable, and maintainable code.

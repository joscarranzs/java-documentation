# Inheritance in Java

## Concept of inheritance
Inheritance is a mechanism in Java where one class (subclass) can inherit the properties and behaviors of another class (superclass). It allows for code reuse and establishes a hierarchical relationship between classes.

---

## Types of inheritance

### Single inheritance
A subclass inherits from one superclass.
Example:
```java
class Vehicle {
    String brand;

    public void drive() {
        System.out.println("Driving...");
    }
}

class Car extends Vehicle {
    int speed;
}
```

### Multilevel inheritance
A class is derived from a class, which is also derived from another class.
Example:
```java
class Vehicle {
    String brand;
}

class Car extends Vehicle {
    int speed;
}

class SportsCar extends Car {
    int turboSpeed;
}
```

### Hierarchical inheritance
Multiple subclasses inherit from a single superclass.
Example:
```java
class Vehicle {
    String brand;
}

class Car extends Vehicle {
    int speed;
}

class Bike extends Vehicle {
    boolean hasGear;
}
```

### Hybrid inheritance
A combination of two or more types of inheritance. (Not directly supported in Java due to ambiguity issues with multiple inheritance of classes.)

---

## Super class

### Concept
The superclass is the parent class from which other classes (subclasses) inherit. It provides the common properties and methods that can be reused by subclasses.

### Example
Real-life example:
```java
class Animal {
    String name;

    public void eat() {
        System.out.println(name + " is eating.");
    }
}

class Dog extends Animal {
    public void bark() {
        System.out.println(name + " is barking.");
    }
}
```

---

## Subclass

### Concept
A subclass is a child class that inherits properties and methods from a superclass. It can also have additional properties and methods of its own.

### Example
Real-life example:
```java
class Animal {
    String name;

    public void eat() {
        System.out.println(name + " is eating.");
    }
}

class Cat extends Animal {
    public void meow() {
        System.out.println(name + " is meowing.");
    }
}
```

---

## Super keyword
The `super` keyword is used in Java to refer to the immediate parent class.

### Initializing superclass constructor
Used to call the constructor of the superclass.
Example:
```java
class Animal {
    String name;

    public Animal(String name) {
        this.name = name;
    }
}

class Dog extends Animal {
    public Dog(String name) {
        super(name); // Call to superclass constructor
    }
}
```

### Accessing superclass properties and methods
Used to access parent class’s methods or properties.
Example:
```java
class Animal {
    public void eat() {
        System.out.println("Animal is eating.");
    }
}

class Dog extends Animal {
    public void eat() {
        super.eat(); // Call superclass method
        System.out.println("Dog is eating.");
    }
}
```

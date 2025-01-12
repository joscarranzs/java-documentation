# Abstraction in Java

## Concept of abstraction
Abstraction is the process of hiding unnecessary details from the user and showing only the important parts of an object or system. It helps simplify complex systems by breaking them into smaller, understandable parts.

For example, when you drive a car, you only use the steering wheel, pedals, and buttons. You don’t need to know how the engine works internally.

---

## Abstract class

### Concept
An abstract class in Java is a class that cannot be directly instantiated. It serves as a blueprint for other classes. Abstract classes can have both abstract methods (methods without a body) and regular methods (methods with a body). They are used to define common properties and behavior for related classes.

### Example
```java
abstract class Vehicle {
    int wheels;

    Vehicle(int wheels) {
        this.wheels = wheels;
    }

    // Abstract method
    abstract void start();

    // Regular method
    void showWheels() {
        System.out.println("This vehicle has " + wheels + " wheels.");
    }
}

class Car extends Vehicle {
    Car() {
        super(4);
    }

    @Override
    void start() {
        System.out.println("Car starts with a key.");
    }
}

class Bicycle extends Vehicle {
    Bicycle() {
        super(2);
    }

    @Override
    void start() {
        System.out.println("Bicycle starts by pedaling.");
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle car = new Car();
        Vehicle bicycle = new Bicycle();

        car.showWheels();
        car.start();

        bicycle.showWheels();
        bicycle.start();
    }
}
```
**Output:**
```
This vehicle has 4 wheels.
Car starts with a key.
This vehicle has 2 wheels.
Bicycle starts by pedaling.
```

---

## Interface

### Concept
An interface in Java is a blueprint of a class. It is used to achieve 100% abstraction. Interfaces can only have method declarations (no body) and constants (final variables). Classes that implement an interface must define all its methods.

### Example
```java
interface Animal {
    void eat(); // Abstract method
    void sleep(); // Abstract method
}

class Dog implements Animal {
    @Override
    public void eat() {
        System.out.println("Dog eats bones.");
    }

    @Override
    public void sleep() {
        System.out.println("Dog sleeps in a kennel.");
    }
}

class Bird implements Animal {
    @Override
    public void eat() {
        System.out.println("Bird eats seeds.");
    }

    @Override
    public void sleep() {
        System.out.println("Bird sleeps in a nest.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Dog();
        Animal bird = new Bird();

        dog.eat();
        dog.sleep();

        bird.eat();
        bird.sleep();
    }
}
```
**Output:**
```
Dog eats bones.
Dog sleeps in a kennel.
Bird eats seeds.
Bird sleeps in a nest.
```

---

## Abstract method

### Concept
An abstract method is a method declared in an abstract class or interface without a body. Subclasses or implementing classes must provide a definition for the method.

### Example
```java
abstract class Shape {
    // Abstract method
    abstract void draw();
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a circle.");
    }
}

class Rectangle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a rectangle.");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape circle = new Circle();
        Shape rectangle = new Rectangle();

        circle.draw();
        rectangle.draw();
    }
}
```
**Output:**
```
Drawing a circle.
Drawing a rectangle.
```

---

## Difference between abstract class and interface

| Feature               | Abstract class                          | Interface                            |
|-----------------------|-----------------------------------------|--------------------------------------|
| **Methods**           | Can have abstract and concrete methods | Only abstract methods (Java 7 and earlier) or default methods (Java 8+) |
| **Variables**         | Can have instance variables            | Only static and final variables      |
| **Inheritance**       | Supports single inheritance            | Supports multiple inheritance        |
| **Usage**             | Used when classes share behavior       | Used for unrelated classes to share capabilities |
| **Example**           | `abstract class Vehicle`               | `interface Animal`                   |

### Real-Life Analogy
- **Abstract Class:** Think of a general blueprint for vehicles (cars, bikes, etc.) that share common traits like wheels.
- **Interface:** Imagine a set of rules that all animals (dogs, birds, etc.) must follow, like eating and sleeping.

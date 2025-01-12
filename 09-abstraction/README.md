# Abstraction in Java

## Abstraction
Abstraction is the process of hiding the implementation details of a feature and only showing the essential information to the user. It focuses on what an object does rather than how it does it.
Abstraction is like driving a car. You use the steering wheel, pedals, and gear shift without knowing the complex mechanisms behind the engine or braking system.

---

## Abstract class
An abstract class is a class that cannot be instantiated on its own. It serves as a blueprint for other classes and can include both abstract methods (without implementation) and concrete methods (with implementation).
An abstract class is like a rough draft of a design. It provides the structure but leaves some details to be filled in by subclasses.

```java
abstract class Animal {
    abstract void sound(); // Abstract method

    void eat() { // Concrete method
        System.out.println("This animal eats food.");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("The dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Dog();
        dog.sound(); // Output: The dog barks.
        dog.eat();   // Output: This animal eats food.
    }
}
```

---

## Interface
An interface in Java is a reference type that contains abstract methods (implicitly public and abstract) and constants (implicitly public, static, and final). It defines a contract that classes can implement.
An interface is like a job description. It outlines what a person (or class) must do but doesn’t specify how they should do it.

```java
interface Animal {
    void sound(); // Abstract method
}

class Cat implements Animal {
    @Override
    public void sound() {
        System.out.println("The cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal cat = new Cat();
        cat.sound(); // Output: The cat meows.
    }
}
```

---

## Abstract method
An abstract method is a method that is declared without an implementation. It must be defined in a subclass or implemented by a class implementing an interface.
An abstract method is like a placeholder or a blank form. It specifies that something must be done but leaves the details for someone else to complete.

```java
abstract class Shape {
    abstract void draw(); // Abstract method
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a circle.");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape circle = new Circle();
        circle.draw(); // Output: Drawing a circle.
    }
}
```

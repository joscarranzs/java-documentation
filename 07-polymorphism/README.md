# Polymorphism in Java

## Concept of polymorphism
Polymorphism in Java is the ability of an object to take many forms. It allows a single interface to represent different underlying forms (data types). In Java, polymorphism enables methods to perform different tasks based on the object that invokes them.

---

## Runtime polymorphism

### Concept
Runtime polymorphism, also known as dynamic method dispatch, occurs when a method call is resolved at runtime. This is achieved through method overriding in inheritance. The behavior of the method depends on the actual object being referred to, not the reference type.

### Example
```java
class Animal {
    public void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    public void sound() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal; // Reference of type Animal

        myAnimal = new Dog();
        myAnimal.sound(); // Outputs: Dog barks

        myAnimal = new Cat();
        myAnimal.sound(); // Outputs: Cat meows
    }
}
```

---

## Compile-time polymorphism

### Concept
Compile-time polymorphism, also known as static polymorphism, occurs when a method is resolved at compile time. This is achieved through method overloading, where multiple methods have the same name but different parameter lists.

### Example
```java
class Calculator {
    // Overloaded methods
    public int add(int a, int b) {
        return a + b;
    }

    public double add(double a, double b) {
        return a + b;
    }

    public int add(int a, int b, int c) {
        return a + b + c;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();

        System.out.println(calc.add(5, 10));       // Outputs: 15
        System.out.println(calc.add(5.5, 10.5));   // Outputs: 16.0
        System.out.println(calc.add(1, 2, 3));     // Outputs: 6
    }
}
```

---

## Pros and cons of polymorphism

### Pros
- **Code reusability**: Polymorphism allows writing generic and reusable code.
- **Extensibility**: New functionality can be easily added without altering existing code.
- **Flexibility**: One interface can represent multiple implementations.
- **Readability**: Reduces the need for multiple method names.

### Cons
- **Complexity**: May increase complexity in understanding code due to dynamic behavior.
- **Performance overhead**: Runtime polymorphism introduces a slight performance cost due to method resolution at runtime.
- **Maintenance challenges**: Debugging can be more difficult when methods behave differently at runtime.

---

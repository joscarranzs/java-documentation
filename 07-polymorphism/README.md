# Polymorphism in Java

## Polymorphism
Polymorphism is the ability of an object to take on multiple forms. In Java, it allows methods or objects to behave differently based on the context in which they are used.
Polymorphism is like a person who can play multiple roles: a teacher in the classroom, a parent at home, and a coach on the field. The behavior changes depending on the context.

---

## Runtime polymorphism (dynamic polymorphism)
Runtime polymorphism, also known as dynamic method dispatch, occurs when a method is overridden in a subclass. The decision about which method to call is made at runtime based on the object's actual type.
It’s like hiring someone for a job interview. You know they’re a professional (base class), but the actual skills (overridden methods) they demonstrate depend on their specialization (subclass).

```java
class Animal {
    void sound() {
        System.out.println("Some generic animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("The dog barks");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("The cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal;

        myAnimal = new Dog();
        myAnimal.sound(); // Output: The dog barks

        myAnimal = new Cat();
        myAnimal.sound(); // Output: The cat meows
    }
}
```

---

## Compile-time polymorphism (static polymorphism)
Compile-time polymorphism occurs when a method is overloaded. It is determined at compile time based on the method signature.
It’s like using a Swiss Army knife. The knife can perform multiple functions, like cutting or opening bottles, based on the tool you choose (method signature).

```java
class Calculator {
    // Overloaded methods
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }

    String add(String a, String b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();

        System.out.println("Integer addition: " + calc.add(5, 10)); // Output: 15
        System.out.println("Double addition: " + calc.add(5.5, 4.5)); // Output: 10.0
        System.out.println("String addition: " + calc.add("Hello, ", "World!")); // Output: Hello, World!
    }
}
```

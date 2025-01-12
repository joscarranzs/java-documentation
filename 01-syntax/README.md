### Syntax of Java

#### Comments

**Concept**
Comments are used to explain the code or make notes for programmers. They are ignored by the computer when running the program.

**Single-line comments**
Single-line comments begin with `//`. Anything written after `//` on the same line is a comment.

Example:
```java
// This is a single-line comment
System.out.println("Hello World");
```

**Multi-line comments**
Multi-line comments begin with `/*` and end with `*/`. They can span multiple lines.

Example:
```java
/*
This is a multi-line comment.
It can be used to explain more complex logic.
*/
System.out.println("Hello World");
```

**Documentation comments (Javadoc)**
Documentation comments are written using `/**` and `*/`. They are used to create documentation for classes, methods, or fields and can be processed by the Javadoc tool.

Example:
```java
/**
* This class demonstrates how to use comments.
*/
public class Example {
/**
* Prints a greeting message.
*/
public void greet() {
System.out.println("Hello World");
}
}
```

---

#### Classes

**Concept**
A class is a blueprint to create objects. It defines properties (attributes) and actions (methods) that the object can have.

**Analogy**
A class is like a recipe for a cake. The recipe tells you what ingredients (properties) you need and the steps (methods) to make the cake.

**Example**
```java
// This class represents a car
public class Car {
    // Properties
    String brand;
    int speed;

    // Method
    public void drive() {
        System.out.println("The car is driving");
    }
}
```

---

#### Properties or attributes

**Concept**
Properties are variables inside a class that store information about the object. Each object has its own values for these properties.

**Analogy**
Properties are like the details of a car. For example, the car's color, brand, and maximum speed are its properties.

**Example**
```java
public class Car {
    // Properties
    String color;
    String brand;
    int maxSpeed;

    public static void main(String[] args) {
        // Create a car object
        Car myCar = new Car();
        myCar.color = "Red";
        myCar.brand = "Toyota";
        myCar.maxSpeed = 180;

        System.out.println("Car brand: " + myCar.brand);
    }
}
```

---

#### Methods

**Concept**
Methods are actions or behaviors of a class. They are functions inside a class that describe what the object can do.

**Analogy**
If a car is an object, its methods are actions like "start", "stop", or "drive".

**Example**
```java
public class Car {
    // Method
    public void start() {
        System.out.println("The car has started.");
    }

    public static void main(String[] args) {
        // Create a car object
        Car myCar = new Car();
        myCar.start(); // Call the start method
    }
}
```

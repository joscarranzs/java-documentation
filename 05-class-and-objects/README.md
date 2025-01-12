# Classes and objects in Java

## Classes
A class is a blueprint for creating objects. It defines properties (attributes) and methods (actions) that the objects will have. 
A class is like a recipe for baking a cake. The recipe specifies the ingredients (properties) and the steps (methods) to create the cake.

```java
// This class represents a car
public class Car {
    // Properties
    String brand;
    int speed;

    // Method
    public void drive() {
        System.out.println("The car is driving.");
    }
}
```

---

## Properties
Properties are variables inside a class that hold information about the object. Each object 
has its own unique values for these properties. Properties are like the details of a car: its color, brand, and speed.

```java
public class Car {
    // Properties
    String color;
    String brand;
    int maxSpeed;

    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.color = "Red";
        myCar.brand = "Toyota";
        myCar.maxSpeed = 200;

        System.out.println("Car brand: " + myCar.brand);
    }
}
```

---

## Methods
Methods are actions or behaviors defined in a class. They describe what the object can do. 
If a car is an object, its methods are actions like "start", "stop", or "drive".

```java
public class Car {
    // Method
    public void start() {
        System.out.println("The car has started.");
    }

    public static void main(String[] args) {
        Car myCar = new Car();
        myCar.start(); // Call the start method
    }
}
```

---

## Constructor
A constructor is a special method used to initialize objects. It is called when an object is created. A constructor is like 
assembling a car. When you create a car, you provide the necessary details (e.g., brand and color) to set it up.

```java
public class Car {
    String brand;
    String color;

    // Constructor
    public Car(String brand, String color) {
        this.brand = brand;
        this.color = color;
    }

    public void displayInfo() {
        System.out.println("Brand: " + brand + ", Color: " + color);
    }

    public static void main(String[] args) {
        Car myCar = new Car("Tesla", "Black");
        myCar.displayInfo();
    }
}
```

---

## Object
An object is an instance of a class. It is created based on the blueprint (class) and holds specific values for its properties.
An object is like a specific car built using the recipe (class). For example, a red Toyota Corolla is an object of the car class.

```java
public class Car {
    String brand;
    String color;

    public Car(String brand, String color) {
        this.brand = brand;
        this.color = color;
    }

    public void drive() {
        System.out.println(brand + " is driving.");
    }

    public static void main(String[] args) {
        Car myCar = new Car("Honda", "Blue");
        myCar.drive();
    }
}
```

---

## Instantiation
Instantiation is the process of creating an object from a class. When an object is instantiated, the constructor of the class is called.
Instantiation is like building a specific car using the blueprint (class). Each car is unique because of its properties, but they all follow the same design.

```java
public class Car {
    String brand;

    public Car(String brand) {
        this.brand = brand;
    }

    public static void main(String[] args) {
        // Instantiating an object
        Car myCar = new Car("Ford");
        System.out.println("Car brand: " + myCar.brand);
    }
}
```

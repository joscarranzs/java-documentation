# Classes and objects in Java

## Concept of a class
A class is a blueprint or template for creating objects. It defines properties (attributes) and behaviors (methods) that the objects will have.

### Example
```java
public class Car {
    String brand; // Attribute
    int speed;    // Attribute

    // Constructor
    public Car(String brand, int speed) {
        this.brand = brand;
        this.speed = speed;
    }

    // Method
    public void drive() {
        System.out.println(brand + " is driving at " + speed + " km/h.");
    }
}
```

---

## Concept of an attribute
An attribute (or property) is a variable declared within a class, representing the state or characteristics of the object.

### Example
```java
public class Car {
    String brand; // Attribute
    int speed;   // Attribute
}
```

---

## Concept of a method
A method is a function defined in a class that describes the behavior or actions of the objects.

### Example
```java
public class Car {
    public void drive() {
        System.out.println("The car is driving.");
    }
}
```

---

## Concept of a constructor method
A constructor is a special method used to initialize objects. It is called when an object is created and typically assigns initial values to attributes.

### Example
```java
public class Car {
    String brand;
    int speed;

    // Constructor
    public Car(String brand, int speed) {
        this.brand = brand;
        this.speed = speed;
    }
}
```

---

## Concept of an object
An object is an instance of a class. It is created using the `new` keyword and represents a specific entity with the defined attributes and behaviors of its class.

### Example
```java
public class Main {
    public static void main(String[] args) {
        Car myCar = new Car("Toyota", 120); // Object creation
        myCar.drive(); // Calling a method
    }
}
```

---

## Differences between a class and an object

| **Class**            | **Object**                             |
|----------------------|----------------------------------------|
| A blueprint or template for objects. | A specific instance of a class.           |
| Defines attributes and methods.      | Has actual values for the attributes.     |
| Does not consume memory by itself.   | Consumes memory when instantiated.       |
| Example: `Car` class.                | Example: `Car myCar = new Car("Toyota", 120);`. |

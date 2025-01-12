# Inheritance in Java

## Inheritance
Inheritance is a mechanism in object-oriented programming where one class (the subclass) derives or inherits the properties and behaviors (methods) of another class (the superclass).
Inheritance is like a child inheriting traits (e.g., eye color, height) from their parents. Similarly, a subclass inherits the attributes and methods of its superclass.

---

## Types of inheritance

### Single inheritance
In single inheritance, a class inherits from one superclass.

```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Inherited from Animal
        dog.bark();
    }
}
```

### Hierarchical inheritance
In hierarchical inheritance, multiple classes inherit from a single superclass.

```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

class Cat extends Animal {
    void meow() {
        System.out.println("The cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        Cat cat = new Cat();

        dog.eat(); // Inherited from Animal
        dog.bark();

        cat.eat(); // Inherited from Animal
        cat.meow();
    }
}
```

### Multilevel inheritance
In multilevel inheritance, a class inherits from a class that has already inherited from another class.

```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

class Mammal extends Animal {
    void walk() {
        System.out.println("This mammal walks.");
    }
}

class Dog extends Mammal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Inherited from Animal
        dog.walk(); // Inherited from Mammal
        dog.bark();
    }
}
```

### Multiple inheritance
Java does not support multiple inheritance with classes to avoid the diamond problem. However, it can be achieved using interfaces.

```java
interface Animal {
    void eat();
}

interface Pet {
    void play();
}

class Dog implements Animal, Pet {
    public void eat() {
        System.out.println("The dog eats food.");
    }

    public void play() {
        System.out.println("The dog plays fetch.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();
        dog.play();
    }
}
```

---

## Superclass
A superclass is the parent class from which a subclass inherits.
A superclass is like a parent in a family tree. It passes its traits (methods and attributes) to its children (subclasses).

```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}
```

---

## Subclass
A subclass is the child class that inherits from a superclass. It can add its own properties and methods.
A subclass is like a child who inherits some traits from their parent but also has their own unique characteristics.

```java
class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}
```

---

## The `super` keyword
The `super` keyword is used to refer to the immediate parent class of a subclass. It can be used to:
1. Call the constructor of the superclass.
2. Access properties or methods of the superclass.

The `super` keyword is like a direct line to the parent. It ensures the child class can interact with or call upon the parent's characteristics when needed.

#### Initializing constructor
```java
class Animal {
    String name;

    Animal(String name) {
        this.name = name;
    }
}

class Dog extends Animal {
    Dog(String name) {
        super(name); // Call parent class constructor
    }

    void displayName() {
        System.out.println("Name: " + name);
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog("Buddy");
        dog.displayName();
    }
}
```

#### Accessing properties and methods
```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

class Dog extends Animal {
    void eat() {
        super.eat(); // Call parent class method
        System.out.println("The dog eats kibble.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();
    }
}
```

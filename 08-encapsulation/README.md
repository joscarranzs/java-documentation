# Encapsulation in Java

## Encapsulation
Encapsulation is a fundamental principle of object-oriented programming. It is the practice of bundling data (variables) and methods (functions) that operate on the data into a single unit, typically a class. Access to the data is restricted through access modifiers and controlled using methods like getters and setters.
Encapsulation is like a safe box. The contents (data) inside the box are protected and can only be accessed using a key (methods) provided by the box.

---

## Modifiers
Modifiers in Java control the visibility and behavior of classes, methods, and variables. They ensure the proper level of access to data and enforce constraints.
Modifiers are like access cards in a secure building. Depending on your card level, you can access certain areas (data) while others remain off-limits.

---

## Types of modifiers

### Public modifier
The `public` modifier allows access to the data or method from any other class.

```java
public class Example {
    public String name = "John";

    public void displayName() {
        System.out.println("Name: " + name);
    }
}
```

### Protected modifier
The `protected` modifier allows access to the data or method within the same package and subclasses.

```java
class Parent {
    protected int age = 40;
}

class Child extends Parent {
    public void showAge() {
        System.out.println("Age: " + age);
    }
}
```

### Private modifier
The `private` modifier restricts access to the data or method to the same class only.

```java
public class Example {
    private String secret = "This is private";

    public void revealSecret() {
        System.out.println(secret);
    }
}
```

### Static modifier
The `static` modifier indicates that a variable or method belongs to the class rather than any instance of the class.

```java
public class Example {
    public static String greeting = "Hello, world!";

    public static void displayGreeting() {
        System.out.println(greeting);
    }
}
```

### Final modifier
The `final` modifier prevents a variable, method, or class from being modified or overridden.

```java
public class Example {
    public final int MAX_SPEED = 120;

    public void showMaxSpeed() {
        System.out.println("Max speed: " + MAX_SPEED);
    }
}
```

---

## Getters
Getters are methods used to retrieve the value of a private variable in a controlled manner.
A getter is like a window with a curtain. You can look through the window (access data), but only if the curtain (method) allows it.

```java
public class Example {
    private String name;

    public String getName() {
        return name;
    }

    public Example(String name) {
        this.name = name;
    }

    public static void main(String[] args) {
        Example example = new Example("Alice");
        System.out.println("Name: " + example.getName());
    }
}
```

---

## Setters
Setters are methods used to update the value of a private variable in a controlled way.
A setter is like a secure deposit box. You can add something to the box (update data) but only through a controlled process.

```java
public class Example {
    private int age;

    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        } else {
            System.out.println("Invalid age");
        }
    }

    public int getAge() {
        return age;
    }

    public static void main(String[] args) {
        Example example = new Example();
        example.setAge(25);
        System.out.println("Age: " + example.getAge());
    }
}
```

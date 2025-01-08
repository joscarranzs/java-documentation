# Java syntax basics

## Comments in Java

Comments in Java are used to explain the code and make it more readable. They are ignored by the Java compiler. There are three types of comments:

1. **Single-line comment**: Starts with `//`. Example:

   ```java
   // This is a single-line comment
   int number = 10;
   ```

2. **Multi-line comment**: Enclosed between `/*` and `*/`. Example:

   ```java
   /* This is a 
      multi-line comment */
   int number = 10;
   ```

3. **Documentation comment**: Enclosed between `/**` and `*/` and used to generate documentation using tools like Javadoc. Example:

   ```java
   /**
    * This is a documentation comment.
    * It describes the class or method.
    */
   public class Example {
       // code
   }
   ```

---

## Defining a class

A class in Java is a blueprint for creating objects. It can contain properties (fields) and methods (functions). Example:

```java
public class Person {
    // Properties
    String name;
    int age;

    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method
    public void greet() {
        System.out.println("Hello, my name is " + name + ".");
    }
}
```

---

## Class properties

Properties, also called fields, are variables declared inside a class. They represent the attributes of the objects created from the class.

---

## Class methods

Methods are blocks of code that perform actions or operations. They can accept parameters, perform logic, and return values. Methods define the behavior of the objects created from the class.


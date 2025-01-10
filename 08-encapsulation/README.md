# Encapsulation in Java

## Concept of encapsulation
Encapsulation is the process of wrapping data (fields) and methods that operate on the data into a single unit (class). It helps to restrict direct access to some components of an object and provides controlled access through methods.

---

## Data security with encapsulation
Encapsulation ensures data security by making fields private and exposing them through public getter and setter methods. This prevents unauthorized access and modification of the data and allows validation before updating fields.

---

## Concept of access modifiers
Access modifiers in Java define the scope and visibility of classes, methods, and variables. They control who can access or modify the data.

---

## Types of access modifiers

### public
Allows access from any other class.
Example:
```java
public class Example {
    public int number = 10;
}
```

### protected
Allows access within the same package and to subclasses.
Example:
```java
class Parent {
    protected String name = "Parent";
}

class Child extends Parent {
    public void display() {
        System.out.println(name); // Accessible
    }
}
```

### private
Restricts access to within the same class only.
Example:
```java
class Example {
    private int number = 10;

    public int getNumber() {
        return number; // Controlled access
    }
}
```

### default (no modifier)
Allows access within the same package only.
Example:
```java
class Example {
    int number = 10; // Default access
}
```

---

## Setter methods

### Concept
Setters are public methods used to set or update the value of private fields in a controlled manner. They can include validation logic.

### Example
```java
class Person {
    private String name;

    // Setter method
    public void setName(String name) {
        if (name != null && !name.isEmpty()) {
            this.name = name;
        } else {
            System.out.println("Invalid name");
        }
    }
}
```

---

## Getter methods

### Concept
Getters are public methods used to retrieve the value of private fields. They provide read-only access to the field.

### Example
```java
class Person {
    private String name;

    // Getter method
    public String getName() {
        return name;
    }
}
```

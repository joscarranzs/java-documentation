
# Operators in Java

## Arithmetic operators
Arithmetic operators are used to perform basic mathematical operations:

### Addition (+)
Adds two numbers.
Example:
```java
int sum = 5 + 3; // sum is 8
```

### Subtraction (-)
Subtracts one number from another.
Example:
```java
int difference = 10 - 4; // difference is 6
```

### Multiplication (*)
Multiplies two numbers.
Example:
```java
int product = 7 * 3; // product is 21
```

### Division (/)
Divides one number by another.
Example:
```java
int quotient = 20 / 4; // quotient is 5
```

### Modulo (%)
Finds the remainder of the division of two numbers.
Example:
```java
int remainder = 10 % 3; // remainder is 1
```

---

## Comparison operators
Comparison operators are used to compare two values and return a boolean result:

### Less than (<)
Checks if one value is less than another.
Example:
```java
boolean result = 5 < 10; // result is true
```

### Greater than (>)
Checks if one value is greater than another.
Example:
```java
boolean result = 15 > 8; // result is true
```

### Equal to (==)
Checks if two values are equal.
Example:
```java
boolean result = 5 == 5; // result is true
```

### Less than or equal to (<=)
Checks if one value is less than or equal to another.
Example:
```java
boolean result = 7 <= 7; // result is true
```

### Greater than or equal to (>=)
Checks if one value is greater than or equal to another.
Example:
```java
boolean result = 10 >= 8; // result is true
```

### Not equal to (!=)
Checks if two values are not equal.
Example:
```java
boolean result = 5 != 3; // result is true
```

---

## Logical operators
Logical operators are used to perform logical operations on boolean values:

### OR (||)
Returns `true` if at least one operand is `true`.
Example:
```java
boolean result = true || false; // result is true
```

### AND (&&)
Returns `true` only if both operands are `true`.
Example:
```java
boolean result = true && false; // result is false
```

### NOT (!)
Inverts the boolean value.
Example:
```java
boolean result = !true; // result is false
```

---

## Ternary operator
The ternary operator is a shorthand for an `if-else` statement:

### ? :
Syntax:
```java
condition ? value_if_true : value_if_false;
```
Example:
```java
int number = 5;
String result = (number > 3) ? "Greater" : "Lesser"; // result is "Greater"
```

---

## Method reference operator
The method reference operator `::` is used to refer to methods or constructors in a concise way.
Example:
```java
class Example {
    public static void printMessage() {
        System.out.println("Hello, World!");
    }
}

Runnable r = Example::printMessage;
r.run(); // Outputs: Hello, World!
```

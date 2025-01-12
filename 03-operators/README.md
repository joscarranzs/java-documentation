# Operators in Java

## Arithmetic operators

### Addition (`+`)
Adds two numbers together.

```java
int result = 5 + 3;
System.out.println("Addition: " + result); // Output: 8
```

### Subtraction (`-`)
Subtracts one number from another.

```java
int result = 10 - 4;
System.out.println("Subtraction: " + result); // Output: 6
```

### Multiplication (`*`)
Multiplies two numbers.

```java
int result = 7 * 2;
System.out.println("Multiplication: " + result); // Output: 14
```

### Division (`/`)
Divides one number by another. If both numbers are integers, the result is also an integer (truncated division).

```java
int result = 8 / 2;
System.out.println("Division: " + result); // Output: 4
```

### Modulo (`%`)
Returns the remainder of the division.

```java
int result = 10 % 3;
System.out.println("Modulo: " + result); // Output: 1
```

---

## Comparison operators

### Greater than (`>`)
Checks if the value on the left is greater than the value on the right.

```java
System.out.println(5 > 3); // Output: true
```

### Less than (`<`)
Checks if the value on the left is less than the value on the right.

```java
System.out.println(4 < 6); // Output: true
```

### Greater than or equal to (`>=`)
Checks if the value on the left is greater than or equal to the value on the right.

```java
System.out.println(5 >= 5); // Output: true
```

### Less than or equal to (`<=`)
Checks if the value on the left is less than or equal to the value on the right.

```java
System.out.println(4 <= 7); // Output: true
```

### Equal to (`==`)
Checks if two values are equal.

```java
System.out.println(5 == 5); // Output: true
```

### Not equal to (`!=`)
Checks if two values are not equal.

```java
System.out.println(5 != 3); // Output: true
```

---

## Logical operators

### AND (`&&`)
Returns `true` if both conditions are `true`.

```java
System.out.println(true && false); // Output: false
```

### OR (`||`)
Returns `true` if at least one condition is `true`.

```java
System.out.println(true || false); // Output: true
```

### NOT (`!`)
Reverses the logical state of its operand.

```java
System.out.println(!true); // Output: false
```

---

## Ternary operator

### Conditional (`?:`)
A shorthand for `if-else`. It takes three operands: a condition, a value if true, and a value if false.

```java
int result = (5 > 3) ? 10 : 20;
System.out.println("Ternary result: " + result); // Output: 10
```

---

## Operator precedence

Defines the order in which operators are evaluated in an expression. Operators with higher precedence are evaluated before those with lower precedence.

```java
int result = 5 + 3 * 2; // Multiplication (*) has higher precedence than addition (+)
System.out.println("Result: " + result); // Output: 11
```

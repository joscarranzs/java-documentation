# Data types in Java

## Numeric data types

### short
A `short` is a 16-bit signed integer. It is used to save memory in large arrays where the memory savings are significant.

```java
short number = 10000;
System.out.println("Short number: " + number);
```

### byte
A `byte` is an 8-bit signed integer. It is used to save space in arrays and can also be used in place of `int` where its range is sufficient.

```java
byte smallNumber = 127;
System.out.println("Byte number: " + smallNumber);
```

### int
An `int` is a 32-bit signed integer. It is the most commonly used integer type.

```java
int count = 50000;
System.out.println("Integer count: " + count);
```

### long
A `long` is a 64-bit signed integer. It is used when a wider range than `int` is needed.

```java
long largeNumber = 1000000000L;
System.out.println("Long number: " + largeNumber);
```

### float
A `float` is a 32-bit floating point for representing fractional numbers. It is less precise than `double` and is generally used to save memory in large arrays of floating-point numbers.

```java
float price = 19.99f;
System.out.println("Float price: " + price);
```

### double
A `double` is a 64-bit floating point for representing decimal numbers with more precision than `float`.

```java
double pi = 3.14159;
System.out.println("Double value: " + pi);
```

---

## Character data type

### char
A `char` is a 16-bit data type used to store a single character. It can store any character using Unicode encoding.

```java
char letter = 'A';
System.out.println("Character: " + letter);
```

---

## Boolean data type

### boolean
A `boolean` can only have two possible values: `true` or `false`. It is typically used for conditional checks and logical operations.

```java
boolean isJavaFun = true;
System.out.println("Is Java fun? " + isJavaFun);
```

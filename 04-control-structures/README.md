# Control structures in Java

## Conditional control structures

### if statement
The `if` statement is used to execute a block of code if a specified condition is `true`.

```java
int number = 10;
if (number > 5) {
    System.out.println("The number is greater than 5.");
}
```

### if-else statement
The `if-else` statement allows the execution of one block of code if the condition is `true` and another block if the condition is `false`.

**Example:**
```java
int number = 3;
if (number > 5) {
    System.out.println("The number is greater than 5.");
} else {
    System.out.println("The number is 5 or less.");
}
```

### else-if statement
The `else-if` statement is used to test multiple conditions. It executes the block of code for the first condition that evaluates to `true`.

```java
int number = 8;
if (number > 10) {
    System.out.println("The number is greater than 10.");
} else if (number > 5) {
    System.out.println("The number is greater than 5 but not greater than 10.");
} else {
    System.out.println("The number is 5 or less.");
}
```

### switch-case statement
The `switch-case` statement is used to select one of many blocks of code to be executed based on a matching value.

```java
int day = 3;
switch (day) {
    case 1:
    System.out.println("Monday");
    break;
    case 2:
    System.out.println("Tuesday");
    break;
    case 3:
    System.out.println("Wednesday");
    break;
    default:
    System.out.println("Invalid day");
}
```

---

## Iterative control structures

### for loop
The `for` loop is used to execute a block of code a specific number of times.

```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Iteration: " + i);
}
```

### for-each loop
The `for-each` loop is used to iterate over elements in an array or collection.

```java
int[] numbers = {1, 2, 3, 4, 5};
for (int number : numbers) {
    System.out.println("Number: " + number);
}
```

### while loop
The `while` loop executes a block of code as long as the specified condition is `true`.

```java
int count = 1;
while (count <= 5) {
    System.out.println("Count: " + count);
    count++;
}
```

### do-while loop
The `do-while` loop executes a block of code at least once, and then repeats the execution as long as the specified condition is `true`.

```java
int count = 1;
do {
    System.out.println("Count: " + count);
    count++;
} while (count <= 5);
```

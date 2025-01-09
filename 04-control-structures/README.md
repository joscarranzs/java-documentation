# Control structures in Java

## Conditional control structures
Conditional control structures allow the program to make decisions based on conditions.

### if
Executes a block of code if the condition is `true`.
Example:
```java
int number = 5;
if (number > 3) {
    System.out.println("Number is greater than 3");
}
```

### if-else
Executes one block of code if the condition is `true` and another block if it is `false`.
Example:
```java
int number = 2;
if (number > 3) {
    System.out.println("Number is greater than 3");
} else {
    System.out.println("Number is less than or equal to 3");
}
```

### else-if
Used to test multiple conditions.
Example:
```java
int number = 5;
if (number > 10) {
System.out.println("Number is greater than 10");
} else if (number > 5) {
System.out.println("Number is greater than 5 but less than or equal to 10");
} else {
System.out.println("Number is 5 or less");
}
```

### switch
Used to execute one block of code among multiple options.
Example:
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

## Iteration control structures
Iteration control structures are used to repeat a block of code.

### for
Executes a block of code a specific number of times.
Example:
```java
for (int i = 0; i < 5; i++) {
    System.out.println("Iteration: " + i);
}
```

### for-each
Used to iterate over arrays or collections.
Example:
```java
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    System.out.println(num);
}
```

### while
Repeats a block of code as long as the condition is `true`.
Example:
```java
int i = 0;
while (i < 5) {
    System.out.println("Iteration: " + i);
    i++;
}
```

### do-while
Executes a block of code at least once, then repeats as long as the condition is `true`.
Example:
```java
int i = 0;
do {
    System.out.println("Iteration: " + i);
    i++;
} while (i < 5);
```

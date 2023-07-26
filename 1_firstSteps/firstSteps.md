# First Steps

- Statement: a complete command to be executed. Can include one or more expressions.
- Expression: a coding construct that evaluates to a single value
- Literal: simplest form of expression that cannot be changed. Ex. strings

## Using JShell

### Hello World

---
Type following `statement` in JShell:

```java
System.out.print("Hello World");
```

- Should only be `double` quotes encapsulating the `string literal`, single quotes won't work.

### Variables

---
Variables are used to store information, can be accessed by a given name and are stored in RAM. Memory location of the variable is handled by CPU, we just call it via its name to use it. The type of data that can be stored in a variable are defined using data types.

Define a variable (Declaration Statement) :

```java
int firstNum = 5;
//printing the variable value
System.out.print(firstNum);
```

Note: Cannot redeclare a variable in a program.

Assignment Statement :

```java
int myNum;
myNum = 5;
System.out.print(myNum);

myNum = (6*9);
System.out.print(myNum);
```

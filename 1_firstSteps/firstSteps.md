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

### Expressions

---

```java
int total = myNum1 + myNum2;
System.out.print("Total is = " + total);
```

- `/var` to list all the variables in JShell

### Data Types

---
Primitive Data Types (eight) : (basic data types)

- Whole numbers -- byte, short, int, long ; long (largest) and byte (smallest) ; integer is default for numbers
- Real numbers -- float, double
- Single character -- char
- Boolean value -- boolean

Most data types have specified range of allowed values. Can use built-in (wrapper) class to get these values.

```java
int minIntValue = Integer.MIN_VALUE;
System.out.print("Minimum value of integer data type is " + minIntValue);

//Max int value
System.out.print("Maximum value of integer data type is " + Integer.MAX_VALUE);
```

Note:

- To improve readability of an integer value you can use underscores in numeric literals (commas are not supported): int myNum = 1_25_635_635;

#### Wrapper Classes

The wrapper class in Java provides the mechanism to convert primitive into object and object into primitive. All 8 primitive types in java respective wrapper class.

Can overflow and underflow variables by simply just putting larger value than its max value or smaller value than its minimum value. It will circle back to it's smallest value or vice-versa, as CPU only allocates certain amount of space for a variable based on its data type. These situations are also known as integer wraparounds.

```java
int myNum = Integer.MAX_VALUE + 1
int myNum = 2147483647 + 1
```

Both will result in: `myNum ==> -2147483648`

- If we give a numeric (literal) value instead of an expression, it will simply throw an error for number being too large.

### Size of Data types

Amount of space occupied in memory (in bits) :

- byte = 8
- short = 16
- int = 32
- long = 64

Can use wrapper class to get size. `System.out.print(Long.SIZE)`

Note:

- to create long, need 'L' or 'l' suffix to the value (especially when number is larger than Integer.MAX_VALUE) unless java considers it as integer.

```java
long myLongNum = 1256463 ; // should be fine as value is less than Integer.MAX_VALUE
long myLongNum = 3_214_651_321_654; // will throw an error for integer number too large 
long myLongNum = 3_214_651_321_654L; // will create the long variable
```


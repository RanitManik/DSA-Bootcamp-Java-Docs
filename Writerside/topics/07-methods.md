# Java Methods

## Introduction

In Java, methods are essential building blocks that facilitate code organization and enhance code reusability. This
comprehensive guide covers the fundamental concepts of Java methods, including syntax, parameters, return values, and
various programming examples.

## Problem Statement

Understanding the nuances of Java methods is crucial for developing efficient and modular code. This document aims to
provide detailed insights into the key aspects of methods through extensive examples and explanations.

## Methods

### Syntax of a Method

In Java, a method is defined with a specific syntax, comprising a method signature, return type, method name, and
parameters (if any). The following example illustrates various method types:

```java
public class SyntaxExample {

    // Method without parameters and return value
    public void simpleMethod() {
        System.out.println("Hello from simpleMethod!");
    }

    // Method with parameters and return value
    public int addNumbers(int a, int b) {
        return a + b;
    }

    // Method with parameters and no return value
    public void displayMessage(String message) {
        System.out.println("Message: " + message);
    }

    public static void main(String[] args) {
        SyntaxExample example = new SyntaxExample();

        // Calling methods
        example.simpleMethod();
        int sum = example.addNumbers(5, 7);
        System.out.println("Sum of numbers: " + sum);
        example.displayMessage("Welcome to Java Methods!");
    }
}
```

### 🎯 Program: Sum of Two Numbers

```java
public class SumExample {

    // Method to calculate the sum of two numbers
    public int calculateSum(int num1, int num2) {
        return num1 + num2;
    }

    public static void main(String[] args) {
        SumExample example = new SumExample();

        // Calling the method
        int result = example.calculateSum(10, 15);
        System.out.println("Sum: " + result);
    }
}
```

### 🎯 Program: Greetings

```java
public class GreetingsExample {

    // Method to display personalized greetings
    public void greetUser(String name) {
        System.out.println("Hello, " + name + "! Welcome to Java Methods.");
    }

    public static void main(String[] args) {
        GreetingsExample example = new GreetingsExample();

        // Calling the method
        example.greetUser("John");
    }
}
```

### Returning Values

Methods can return values, allowing for the efficient execution of code. The following example demonstrates a method
returning an integer value:

```java
public class ReturnValueExample {

    // Method with a return value
    public int multiplyNumbers(int num1, int num2) {
        return num1 * num2;
    }

    public static void main(String[] args) {
        ReturnValueExample example = new ReturnValueExample();

        // Calling the method
        int result = example.multiplyNumbers(5, 8);
        System.out.println("Product: " + result);
    }
}
```

### Returning a String

Methods can also return string values. The next example showcases a method returning a personalized greeting:

```java
public class StringReturnExample {

    // Method returning a string
    public String generateGreeting(String name) {
        return "Hello, " + name + "! Have a great day.";
    }

    public static void main(String[] args) {
        StringReturnExample example = new StringReturnExample();

        // Calling the method
        String greeting = example.generateGreeting("Alice");
        System.out.println(greeting);
    }
}
```

### Parameters (Integer Function)

Methods can accept parameters, providing flexibility in handling various data types. The following example focuses on
integer parameters:

```java
public class IntegerParameterExample {

    // Method with integer parameters
    public int calculateSquare(int num) {
        return num * num;
    }

    public static void main(String[] args) {
        IntegerParameterExample example = new IntegerParameterExample();

        // Calling the method
        int result = example.calculateSquare(7);
        System.out.println("Square: " + result);
    }
}
```

### Parameters (String Function)

Extend your understanding of parameters by incorporating string parameters into methods:

```java
public class StringParameterExample {

    // Method with string parameter
    public void printMessage(String message) {
        System.out.println("Message: " + message);
    }

    public static void main(String[] args) {
        StringParameterExample example = new StringParameterExample();

        // Calling the method
        example.printMessage("Welcome to Java Methods!");
    }
}
```

### 🎯 Program: Swap Two Numbers

Practical application of methods can be demonstrated through a program that swaps the values of two numbers:

```java
public class SwapExample {

    // Method to swap two numbers
    public void swapNumbers(int a, int b) {
        System.out.println("Before swapping: a = " + a + ", b = " + b);

        int temp = a;
        a = b;
        b = temp;

        System.out.println("After swapping: a = " + a + ", b = " + b);
    }

    public static void main(String[] args) {
        SwapExample example = new SwapExample();

        // Calling the method
        example.swapNumbers(3, 7);
    }
}
```

### 🎯 Program: Pass Value

Learn how values can be passed between methods and how the original value remains unchanged:

```java
public class PassValueExample {

    // Method to modify and display the passed value
    public void modifyValue(int value) {
        System.out.println("Before modification: value = " + value);
        value = value * 2;
        System.out.println("After modification: value = " + value);
    }

    public static void main(String[] args) {
        PassValueExample example = new PassValueExample();

        int originalValue = 10;

        // Calling the method
        example.modifyValue(originalValue);
        System.out.println("Original value remains unchanged: " + originalValue);
    }
}
```

### Internal Working of Swapping Program

Understanding the internal workings of a swapping program is crucial for a deeper comprehension of method execution.
The `SwapExample` program provided earlier illustrates the mechanics of swapping two numbers.

### 🎯 Program: Change Value

Explore a program that illustrates the ability to modify values within methods:

```java
public class ChangeValueExample {

    // Method to change the value
    public void changeValue(int[] array) {
        System.out.println("Before change: array[0] = " + array[0]);
        array[0] = 100;
        System.out.println("After change: array[0] = " + array[0]);
    }

    public static void main(String[] args) {
        ChangeValueExample example = new ChangeValueExample();

        // Calling the method
        int[] values = { 5, 10, 15 };
        example.changeValue(values);
        System.out.println("Array after method call: values[0] = " + values[0]);
    }
}
```

### Scope

scope is the area of a program where a variable or function is visible and accessible to other code. Scope is a
source-code level concept and is part of the behavior of a compiler or interpreter of a language.

**Method Scope:**

Method scope refers to the visibility and accessibility of variables within a specific method. Variables declared within
a method are only accessible within that method. They have a limited lifespan, existing only for the duration of the
method's execution. Attempting to access these variables outside the method will result in a compilation error.

```java
public class MethodScopeExample {

    public void demonstrateMethodScope() {
        int localVar = 5;
        System.out.println("Local variable within method: " + localVar);
    }

    public static void main(String[] args) {
        MethodScopeExample example = new MethodScopeExample();

        // Cannot access localVar here
        example.demonstrateMethodScope();
    }
}
```

**Block Scope:**

Block scope pertains to the visibility of variables within a specific code block, denoted by curly braces `{}`.
Variables declared inside a block are only accessible within that block. Once the block is exited, these variables go
out of scope and cannot be referenced.

```java
public class BlockScopeExample {

    public void demonstrateBlockScope() {
        int localVar = 5;

        // Block scope
        {
            int blockVar = 10;
            System.out.println("Inside block: localVar = " + localVar + ", blockVar = " + blockVar);
        }

        // Cannot access blockVar here
    }

    public static void main(String[] args) {
        BlockScopeExample example = new BlockScopeExample();
        example.demonstrateBlockScope();
    }
}
```

**Loop Scope:**

Loop scope refers to the visibility of variables declared within a loop structure. Variables defined inside a loop are
confined to that loop and cannot be accessed outside of it.

```java
public class LoopScopeExample {

    public void demonstrateLoopScope() {
        for (int i = 1; i <= 3; i++) {
            System.out.println("Inside loop: i = " + i);
        }

        // Cannot access i here
    }

    public static void main(String[] args) {
        LoopScopeExample example = new LoopScopeExample();
        example.demonstrateLoopScope();
    }
}
```

**Shadowing:**

Shadowing occurs when a local variable within a specific scope has the same name as a variable in an outer scope, such
as a class-level variable. In such cases, the local variable "shadows" or takes precedence over the outer variable
within its scope.

```java
public class ShadowingExample {

    private int x = 5;

    public void demonstrateShadowing(int x) {
        System.out.println("Local variable x: " + x);
        System.out.println("Class-level variable x: " + this.x);
    }

    public static void main(String[] args) {
        ShadowingExample example = new ShadowingExample();
        example.demonstrateShadowing(10);
    }
}
```

**Variable Arguments (Varargs):**

Varargs (variable-length argument lists) allow methods to accept a variable number of parameters. These parameters are
treated as an array within the method, providing flexibility when calling the method with different numbers of
arguments.

```java
public class VarargsExample {

    public void printValues(String... values) {
        for (String value : values) {
            System.out.println(value);
        }
    }

    public static void main(String[] args) {
        VarargsExample example = new VarargsExample();
        example.printValues("One", "Two", "Three");
        example.printValues("Java", "Programming");
    }
}
```

**Method Overloading:**

Method overloading involves defining multiple methods with the same name in a class, but with different parameter types
or counts. This allows for flexibility when calling the method, as the appropriate version is selected based on the
provided arguments.

```java
public class OverloadingExample {

    public int add(int a, int b) {
        return a + b;
    }

    public int add(int a, int b, int c) {
        return a + b + c;
    }

    public double add(double a, double b) {
        return a + b;
    }

    public static void main(String[] args) {
        OverloadingExample example = new OverloadingExample();
        System.out.println("Sum of integers: " + example.add(5, 7));
        System.out.println("Sum of integers: " + example.add(3, 8, 12));
        System.out.println("Sum of doubles: " + example.add(2.5, 3.5));
    }
}
```

## 🎯 Questions

#### Q1: Prime Number

Implement a method to determine whether a given number is prime or not:

```java
public class PrimeNumberExample {

    // Method to check if a number is prime
    public boolean isPrime(int num) {
        if (num <= 1) {
            return false;
        }
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        PrimeNumberExample example = new PrimeNumberExample();

        // Calling the method
        int numberToCheck = 13;
        if (example.isPrime(numberToCheck)) {
            System.out.println(numberToCheck + " is a prime number.");
        } else {
            System.out.println(numberToCheck + " is not a prime number.");
        }
    }
}
```

#### Q2: Check Armstrong Number

Create a method to check if a given number is an Armstrong number:

```java
public class ArmstrongNumberExample {

    // Method to check if a number is Armstrong
    public boolean isArmstrong(int num) {
        int originalNum = num;
        int sum = 0;
        int digits = String.valueOf(num).length();

        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }

        return sum == originalNum;
    }

    public static void main(String[] args) {
        ArmstrongNumberExample example = new ArmstrongNumberExample();

        // Calling the method
        int numberToCheck = 153;
        if (example.isArmstrong(numberToCheck)) {
            System.out.println(numberToCheck + " is an Armstrong number.");
        } else {
            System.out.println(numberToCheck + " is not an Armstrong number.");
        }
    }
}
```

#### Q3: Print All 3-Digit Armstrong Numbers

Develop a method that prints all 3-digit Armstrong numbers within a specified range:

```java
public class ArmstrongNumbersInRangeExample {

    // Method to print Armstrong numbers in a range
    public void printArmstrongNumbersInRange(int start, int end) {
        for (int i = start; i <= end; i++) {
            if (isArmstrong(i, 3)) {
                System.out.println(i);
            }
        }
    }

    // Method to check if a number is Armstrong with a specified number of digits
    private boolean isArmstrong(int num, int digits) {
        int originalNum = num;
        int sum = 0;

        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }

        return sum == originalNum;
    }

    public static void main(String[] args) {
        ArmstrongNumbersInRangeExample example = new ArmstrongNumbersInRangeExample();

        // Calling the method
        System.out.println("3-Digit Armstrong Numbers in the range 100 to 999:");
        example.printArmstrongNumbersInRange(100, 999);
    }
}
```

## Conclusion

In conclusion, understanding methods is fundamental to effective Java programming. They provide a structured way to
organize code, improve code reuse, and make programs more modular. By incorporating the concepts of returning values and
using parameters, you can create powerful and flexible Java applications. Keep practicing and exploring different
scenarios to deepen your understanding of Java methods. Happy coding!
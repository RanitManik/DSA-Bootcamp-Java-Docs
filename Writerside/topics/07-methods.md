# Java Methods

## Introduction

In Java, methods are essential building blocks that facilitate code organization and enhance code reusability. This
comprehensive guide covers the fundamental concepts of Java methods, including syntax, parameters, return values, and
various programming examples.

## Syntax of a Method

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

## Return Statement

In Java, the `return` statement is used to finish the execution of a method and return a value to the calling code. It
is commonly used in methods that have a non-void return type.

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

## Parameter and Argument

In Java, parameters and arguments are key concepts in methods. Let me explain the difference:

1. **Parameter:**
    - A parameter is a variable that is used in a method to receive a value.
    - It acts as a placeholder for the actual value that will be passed to the method.
    - Parameters are defined in the method signature and serve as input placeholders.

   Example:
   ```java
   public void printMessage(String message) {
       System.out.println(message);
   }
   ```
   Here, `message` is a parameter of type String.

2. **Argument:**
    - An argument is the actual value that is passed to the method when it is called.
    - It is the data that is supplied to the parameters of a method during a method call.

   Example:
   ```java
   public static void main(String[] args) {
       MyClass myObject = new MyClass();
       myObject.printMessage("Hello, Ranit!");
   }
   ```
   In this example, "Hello, Ranit!" is the argument passed to the `printMessage` method.

So, in summary, parameters are variables in the method signature, and arguments are the values passed to those
parameters when the method is called.

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

## Scope

scope is the area of a program where a variable or function is visible and accessible to other code. Scope is a
source-code level concept and is part of the behavior of a compiler or interpreter of a language.

### Method Scope:

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

### Block Scope:

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

### Loop Scope:

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

## Shadowing

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

### this keyword in JAVA

In Java, `this` is a keyword that is used to refer to the current instance of the class. It can be used to access
instance variables (class-level variables) and methods of the current object.

Specifically, `this.x` is used to refer to the instance variable `x` of the current object. When you have a local
variable with the same name as an instance variable, using `this` helps to differentiate between the local variable and
the instance variable.

The use of `this` is generally applicable in instance methods and constructors, where you might encounter variable
shadowing (using a local variable with the same name as an instance variable or a parameter).

Here's a brief summary:

- `this` is used to refer to the current instance of the class.
- It can be used to differentiate between instance variables and local variables when they share the same name.
- It is typically used within instance methods and constructors.

> However, there are some cases where `this` is not needed, such as when there is no ambiguity between local variables
> and instance variables or when you are working in a static context (like a static method or a static block) where
> there
> is no instance of the class.

In the provided code, using `this.x` helps in explicitly referencing the instance variable `x` of the class, ensuring
that it is not confused with the local variable `x` within the `demonstrateShadowing` method.

## Variable Arguments (Varargs)

Varargs (variable-length argument lists) allow methods to accept a variable number of parameters. These parameters are
treated as an array within the method, providing flexibility when calling the method with different numbers of
arguments.

```java
public class Variable_length_arguments {
    public static void main(String[] args) {
        fun(5, 6, 8, 9, 58, 95, 51, 48, 59, 263, 498);
        fun(); // This will print an empty array
        multiple(2, 3, "Kunal", "Ranit", "Pushpa");
        // argument's order have to be the same as of parameters
    }

    // "datatype... v" is used to take as many input as you want
    // This is called as "varargs"

    static void fun(int... v) {
        System.out.println(Arrays.toString(v));
    }

    static void multiple(int a, int b, String... v) {
        System.out.println(Arrays.toString(v));
    }
}
```

## Method Overloading

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
# Java Variables

## Introduction

Variables in Java are containers used to store data values. They play a crucial role in programming by allowing
developers to manage and manipulate data. This documentation provides an overview of Java variables, including their
declaration, initialization, data types, naming conventions, scope, and usage.

## Declaration

In Java, variables are declared using the following syntax:

```java
int age; // Declaration of an integer variable named 'age'
```

## Initialization

After declaration, variables must be initialized with a value before use:

```java
age = 25; // Initializing 'age' with the value 25
```

Alternatively, you can declare and initialize in a single line:

```java
int age = 25; // Declaration and initialization in one line
```

## Data Types

Java supports various data types, including primitive types and reference types. Choose a data type based on the kind of
data you want to store:

```java
int count = 10;          // integer
double price = 19.99;    // floating-point number
char grade = 'A';        // character
String name = "John";    // string (reference type)
```

## Naming Conventions

Follow Java's naming conventions when naming variables. Typically, use camelCase:

```java
int studentAge;
double averageScore;
```

## Scope

Variables have a scope, meaning they are accessible only within the block of code where they are declared:

### Local Variables

Local variables are declared within a method, constructor, or block of code. They are only accessible within that
specific scope:

```java
public class Example {
    public static void main(String[] args) {
        int x = 5; 
        // 'x' is a local variable, accessible only within this main method
    }
}
```

### Global Variables

Global variables, also known as instance variables, are declared within a class but outside any method. They are
accessible throughout the entire class:

```java
public class Example {
    int globalVar = 10; 
    // 'globalVar' is a global variable, accessible throughout the class

    public static void main(String[] args) {
        // Access 'globalVar' within the main method 
        // or any other method in the class
        System.out.println(globalVar);
    }
}
```

## Final Keyword

The `final` keyword can be used to make a variable a constant:

```java
final int MAX_VALUE = 100;
```

## Conclusion

Understanding how to declare, initialize, and use variables in Java is fundamental for effective programming. Pay
attention to data types, naming conventions, and scope, including the distinction between local and global variables, to
ensure robust and maintainable code.

For more detailed information, refer to the official [Java Documentation](https://docs.oracle.com/en/java/).

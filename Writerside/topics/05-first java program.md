# first java program

## First Java Program

### Structure of Java File

In Java, source code is saved with the .java extension. Each .java file represents a class, and the class within it must
have the same name as the file. The first alphabet of the class name is conventionally in uppercase, although it is not
mandatory. The class with the same name as the file must be declared as a public class, and it should contain a main
method, which is the entry point of the program.

### Converting .java to .class

The javac compiler is used to convert a .java file to a .class file containing bytecode. The command is as follows:

```java
javac Main.java
```

## Running the Program

### Hello World Program

```java
public class Main{
    public static void main(String[] args){
        System.out.println("Hello World");
    }
}
```

Explanation:

1. `public`: Access modifier allowing access from anywhere.
2. `class`: Keyword representing a group of properties and functions.
3. `Main`: Class name, matching the file name.
4. `public`: Allows the program to use the main function from anywhere.
5. `static`: Keyword allowing the main method to run without using objects.
6. `void`: Keyword indicating no return value from the method.
7. `main`: The name of the method.
8. `String[] args`: Command line arguments of string type array.
9. `System`: A final class in the `java.lang` package.
10. `out`: A variable of `PrintStream` type, a public and static member field of the `System` class.
11. `println`: A method of `PrintStream` class, printing arguments and adding a new line.

### What is a Package?

* A package in Java is a folder containing Java files.
* It provides organizational rules for programs.

## Primitive Data Types

Primitive data types in Java are non-breakable and include `int`, `char`, `float`, `double`, and `long`. These represent
integer, character, floating-point, double-precision, and long integer values, respectively. Boolean stores only `true`
or `false`. `string` is not a primitive data type.

```Java
int i = 26;
char c = 'A';
float f = 98.67f; // Note the 'f' suffix for float
double d = 45676.58975;
long l = 15876954832558315L; // Note the 'L' suffix for long
boolean b = false;

```

### Literals and Identifiers

* **Literals** are fixed values that are used in your program. They are constants that represent specific values.
  For example:

```Java
int number = 42;  // Here, 42 is a literal.
char character = 'A';  // 'A' is a literal character.
double pi = 3.14;  // 3.14 is a literal of type double.
```

* **Identifiers** are names given to program elements such as variables, constants, functions, classes, and more. They
  serve
  as labels for these elements, allowing you to refer to and manipulate them in your code. Some rules for creating valid
  identifiers include:

    * They must start with a letter, underscore (_), or dollar sign ($).
    * Subsequent characters can be letters, digits, underscores, or dollar signs.
    * Java is case-sensitive, so variable and Variable would be different identifiers.
      Examples of identifiers:
  ```Java
  int studentCount;  
  // 'studentCount' is an identifier for a variable.
  final double PI_VALUE = 3.14159; 
  // 'PI_VALUE' is an identifier for a constant.
  void calculateSum() { /* ... */ } 
  // 'calculateSum' is an identifier for a function.

  ```

## Comments in Java

Comments in Java are written in the source code but ignored by the compiler. There are single-line comments (`//`) and
multi-line comments (`/* */`).

## Inputs in Java

The `Scanner` class in `java.util` is used to take input. To use it:

1. Import `java.util.Scanner`.
2. Create a `Scanner` object.
3. Use the object to take input from the keyboard.

```java
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
    }
}
```

### Input Methods

- `nextInt()`: Takes input of type int.
- `nextFloat()`: Takes input of type float.
- `next()`: Takes one word input until a space occurs.
- `nextLine()`: Takes the entire string input, including spaces.

## Sum of Two Numbers

```java
import java.util.Scanner;
public class Sum {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter first number");
        int num1 = input.nextInt();
        System.out.print("Enter second number");
        int num2 = input.nextInt();
        int sum = num1 + num2;
        System.out.println("Sum = " + sum);
    }
}
```

## Conclusion

These topics cover the basics of Java programming, a widely-used language for developing applications. Java is
platform-independent, meaning it can run on any operating system without modifications. Understanding these topics will
lay the foundation for your Java programming journey. The examples provided help you grasp concepts like variables, data
types, control statements, arrays, classes, objects, and methods. Through hands-on practice, you'll gain confidence in
coding and problem-solving with Java. Remember, learning Java is iterative and requires patience and practice. Start now
and enjoy your learning experience!
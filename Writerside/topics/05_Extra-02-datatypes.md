# Data Types in Java

## Introduction

In Java, a data type is a classification of the data that a variable or object can hold. It specifies the size and type
of values that can be stored, and the operations that can be performed on them. Java has two categories of data types:
**primitive** and **reference**.

## Primitive Data Types

Java has eight built-in primitive data types:

| Data Type | Size (in bits) | Range                           | Example                          |
|-----------|----------------|---------------------------------|----------------------------------|
| byte      | 8              | -128 to 127                     | `byte age = 25;`                 |
| short     | 16             | -32,768 to 32,767               | `short temperature = -100;`      |
| int       | 32             | -2^31 to 2^31 - 1               | `int count = 1000;`              |
| long      | 64             | -2^63 to 2^63 - 1               | `long population = 7000000000L;` |
| float     | 32             | Precision: 7 decimal digits     | `float price = 49.99f;`          |
| double    | 64             | Precision: 15 decimal digits    | `double pi = 3.141592653589793;` |
| char      | 16             | Represents Unicode characters   | `char grade = 'A';`              |
| boolean   | -              | Represents true or false values | `boolean isStudent = true;`      |

## Reference Data Types

Reference data types are used to store references to objects. These include:

| Data Type    | Example                             |
|--------------|-------------------------------------|
| Objects      | `String name = new String("John");` |
| Array        | `int[] numbers = {1, 2, 3, 4, 5};`  |
| Enumerations | -                                   |
| Interface    | -                                   |

## Type Conversion & Type casting

### Type Conversion

**Definition:** Type conversion refers to the automatic or implicit conversion of one data type to another by the
programming language itself.

* **Example:** In some programming languages, you can perform operations involving different data types, and the
  language will automatically convert one or more of the operands to a common data type before the operation is
  executed.

* **Type Conversion (Implicit):**
   ```java
   public class TypeConversionExample {
       public static void main(String[] args) {
           // Type Conversion (Implicit)
           int numInt = 10;  // integer
           double numDouble = 5.5;  // double

           double result = numInt + numDouble;  
  // The addition triggers automatic type conversion
           System.out.println(result);  
  // The result will be a double (15.5)
       }
   }
   ```

In this example, type conversion occurs implicitly when adding an `int` and a `double`. The result is automatically
converted to a `double`.

### Type casting

**Definition:** Type casting, on the other hand, is the explicit conversion of a variable from one data type to another
by the programmer.

* **Example:** If you have a variable of type float and you want to use it as an int, you might use explicit type
  casting
  to convert the float to an int.

* **Type Casting (Explicit):**
   ```java
   public class TypeCastingExample {
       public static void main(String[] args) {
           // Type Casting (Explicit)
           double numDouble = 5.5;  // double

           // Explicitly casting the double to an int
           int numInt = (int) numDouble;

           System.out.println(numInt);  // The result will be an integer (5)
       }
   }
   ```

In this example, type casting is done explicitly using `(int)` to cast a `double` to an `int`. Note that this
explicit casting may result in loss of precision, as the decimal part is truncated.

In summary, type conversion is a broader term that includes both implicit (automatic) and explicit (manual) conversion,
while type casting specifically refers to the explicit conversion performed by the programmer. The choice of which term
to use may depend on the context and the level of control the programmer has over the conversion process.

## Automatic Type Promotion in Expressions

In Java, automatic type promotion occurs when evaluating expressions. For example, byte, short, or char operands are
promoted to int, and if one operand is long, float, or double, the entire expression is promoted accordingly.

```java
byte a = 40;
byte b = 50;
byte c = 100;
int d = (a * b) / c;
System.out.println(d);
```

## Conclusion

Understanding data types in Java is fundamental for effective programming. Choose the appropriate data type based on the
requirements of your program to optimize memory usage and ensure proper functionality.

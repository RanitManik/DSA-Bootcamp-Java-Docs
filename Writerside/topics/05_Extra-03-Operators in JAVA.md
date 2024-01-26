# Java Operators: An Overview

## Introduction

Java, being a versatile and object-oriented programming language, employs a variety of operators to perform operations
on variables and values. These operators can be categorized into different types based on their functionality. In this
document, we will explore the essential operators in Java and their usage.

## Arithmetic Operators

Arithmetic operators are used to perform basic mathematical operations.

- **Addition (+):** Adds two operands.
  ```java
  int result = num1 + num2;
  ```

- **Subtraction (-):** Subtracts the right operand from the left operand.
  ```java
  int result = num1 - num2;
  ```

- **Multiplication (*):** Multiplies two operands.
  ```java
  int result = num1 * num2;
  ```

- **Division (/):** Divides the left operand by the right operand.
  ```java
  int result = num1 / num2;
  ```

- **Modulus (%):** Returns the remainder when the left operand is divided by the right operand.
  ```java
  int result = num1 % num2;
  ```

## Relational Operators

Relational operators are used to establish relationships between variables.

- **Equal to (==):** Checks if two operands are equal.
  ```java
  if (num1 == num2) {
      // code block
  }
  ```

- **Not equal to (!=):** Checks if two operands are not equal.
  ```java
  if (num1 != num2) {
      // code block
  }
  ```

- **Greater than (>):** Checks if the left operand is greater than the right operand.
  ```java
  if (num1 > num2) {
      // code block
  }
  ```

- **Less than (<):** Checks if the left operand is less than the right operand.
  ```java
  if (num1 < num2) {
      // code block
  }
  ```

- **Greater than or equal to (>=):** Checks if the left operand is greater than or equal to the right operand.
  ```java
  if (num1 >= num2) {
      // code block
  }
  ```

- **Less than or equal to (<=):** Checks if the left operand is less than or equal to the right operand.
  ```java
  if (num1 <= num2) {
      // code block
  }
  ```

## Logical Operators

Logical operators are used to perform logical operations.

- **Logical AND (&&):** Returns true if both operands are true.
  ```java
  if (condition1 && condition2) {
      // code block
  }
  ```

- **Logical OR (||):** Returns true if at least one of the operands is true.
  ```java
  if (condition1 || condition2) {
      // code block
  }
  ```

- **Logical NOT (!):** Returns true if the operand is false and vice versa.
  ```java
  if (!condition) {
      // code block
  }
  ```

## Ternary Operators

In Java, a ternary operator is a shorthand way of writing an if-else statement. It's also known as the
conditional operator. The syntax is as follows:

```java
variable = (condition) ? expressionIfTrue : expressionIfFalse;
```

Here's a simple example to illustrate how it works:

```java
public class TernaryOperatorExample {
    public static void main(String[] args) {
        int number = 10;
        String result = (number % 2 == 0) ? "Even" : "Odd";
        System.out.println("The number is " + result);
    }
}
```

In this example, if `number` is divisible by 2, the result will be "Even"; otherwise, it will be "Odd". The ternary
operator evaluates the condition (`number % 2 == 0`) and returns the appropriate value based on whether the condition is
true or false.

## Assignment Operators

Assignment operators are used to assign values to variables.

- **Assignment (=):** Assigns the value on the right to the variable on the left.
  ```java
  int result = 10;
  ```

- **Add and Assign (+=):** Adds the right operand to the left operand and assigns the result to the left operand.
  ```java
  result += 5; // equivalent to result = result + 5;
  ```

- **Subtract and Assign (-=):** Subtracts the right operand from the left operand and assigns the result to the left
  operand.
  ```java
  result -= 3; // equivalent to result = result - 3;
  ```

- **Multiply and Assign (*=):** Multiplies the left operand by the right operand and assigns the result to the left
  operand.
  ```java
  result *= 2; // equivalent to result = result * 2;
  ```

- **Divide and Assign (/=):** Divides the left operand by the right operand and assigns the result to the left operand.
  ```java
  result /= 4; // equivalent to result = result / 4;
  ```

- **Modulus and Assign (%=):** Calculates the modulus of the left operand by the right operand and assigns the result to
  the left operand.
  ```java
  result %= 3; // equivalent to result = result % 3;
  ```

## Bitwise Operators

Bitwise operators in Java allow manipulation of individual bits within integer values. They are commonly used in
scenarios involving low-level programming, bitwise flags, and certain optimization techniques. This documentation
provides examples and explanations for each bitwise operator in Java.

- ### Bitwise AND (&)

The bitwise AND operator performs a bitwise AND operation on each pair of corresponding bits. The result is 1 only if
both bits are 1.

**Example:**

```java
int num1 = 5;  // Binary: 0101
int num2 = 3;  // Binary: 0011
int result = num1 & num2;  // Binary: 0001 (1 in decimal)
```

- ### Bitwise OR (|)

The bitwise OR operator performs a bitwise OR operation on each pair of corresponding bits. The result is 1 if at least
one of the bits is 1.

**Example:**

```java
int num1 = 5;  // Binary: 0101
int num2 = 3;  // Binary: 0011
int result = num1 | num2;  // Binary: 0111 (7 in decimal)
```

- ### Bitwise XOR (^)

The bitwise XOR operator performs a bitwise exclusive OR operation on each pair of corresponding bits. The result is 1
if the bits are different.

**Example:**

```java
int num1 = 5;  // Binary: 0101
int num2 = 3;  // Binary: 0011
int result = num1 ^ num2;  // Binary: 0110 (6 in decimal)
```

- ### Bitwise NOT (~)

The bitwise NOT operator inverts each bit of the operand.

**Example:**

```java
int num = 5;  // Binary: 0101
int result = ~num;  // Binary: 1010 (-6 in decimal due to two's complement representation)
```

- ### Left Shift (<<)

The left shift operator shifts the bits of the left operand to the left by a specified number of positions.

**Example:**

```java
int num = 5;  // Binary: 0000 0101
int result = num << 2;  // Binary: 0001 0100 (20 in decimal)
```

- ### Right Shift (>>)

The right shift operator shifts the bits of the left operand to the right by a specified number of positions, filling
the leftmost bits with the sign bit.

**Example:**

```java
int num = -16;  // Binary: 1111 0000
int result = num >> 2;  // Binary: 1111 1100 (-4 in decimal)
```

- ### Unsigned Right Shift (>>>)

The unsigned right shift operator is similar to the right shift operator, but it fills the leftmost bits with zero.

**Example:**

```java
int num = -16;  // Binary: 1111 0000
int result = num >>> 2;  // Binary: 0011 1100 (60 in decimal)
```

## Usage of Bitwise Operators

### 1. Flag Manipulation:

Flags are often used to represent boolean states or options. Each flag can be represented by a single bit. Bitwise
operators are useful for manipulating these flags.

```java
// Example: Setting a flag
int flags = 0;
int FLAG_A = 1; // 0001 in binary
flags |= FLAG_A; // Set Flag A
```

Here, the `|= operator` sets the bits in `flags` that are also set in `FLAG_A`. This is a common way to enable or
disable features by setting or clearing flags.

### 2. Bitwise Masking:

Masking involves using a bitmask to filter out specific bits from an integer.

```java
// Example: Extracting bits 2-4
int value = 0b101011; // Binary: 101011
int mask = 0b000111;  // Binary: 000111

// Step 1: value & mask
int extractedBits = value & mask; // Result: 000011 (Binary)

// Explanation:
// The '&' (bitwise AND) operation compares each corresponding bit of 'value' and 'mask'.
// If both bits are 1, the resulting bit is 1; otherwise, it's 0.

// Breaking down the binary values:
// value   = 101011
// mask    = 000111
// ----------------
// result  = 000011

// The result, after the '&' operation, contains the bits from 'value' where 'mask' has 1s.

// After this step, 'extractedBits' holds the binary value 000011, which is 3 in decimal.
```

In this example, the `& operator` performs a bitwise AND operation, preserving only the bits that are set in
both `value` and `mask`. This is useful for isolating and manipulating specific portions of a binary representation.

### 3. Swapping Values without a Temporary Variable:

Bitwise XOR can be used to swap values without using a temporary variable.

```java
// Example: Swapping values using XOR

int a = 5; // Initial value of a
int b = 8; // Initial value of b

// Step 1: a = a ^ b
a = a ^ b; // a = 5 ^ 8 = 13 (Binary: 1101)

// Step 2: b = a ^ b
b = a ^ b; // b = 13 ^ 8 = 5 (Binary: 0101)

// Step 3: a = a ^ b
a = a ^ b; // a = 13 ^ 5 = 8 (Binary: 1000)

// After these steps, 'a' now holds the value 8, and 'b' holds the value 5

```

The XOR swap works because XORing a value twice with the same value results in the original value. This technique is
often used in situations where memory usage needs to be minimized.

### 4. Checking Even or Odd:

Bitwise AND with 1 can be used to check if a number is even or odd.

```java
// Example: Checking even or odd
int num = 7;
if ((num & 1) == 0) {
    System.out.println("Even");
} else {
    System.out.println("Odd");
}
```

If the least significant bit is 0, the number is even; otherwise, it's odd. This is a more efficient way to check parity
compared to the modulus operator (%).

### 5. Performance Optimization:

Bitwise operations can be more efficient in certain scenarios, especially in low-level programming or
resource-constrained environments. For example, bitwise AND is often faster than traditional boolean AND.

### 6. Bitwise Shifts for Multiplication and Division:

For a given integer `A` and a non-negative integer `B`:

- \[ A  <<  B = A * 2^B \]

This means shifting the bits of `A` to the left by `B` positions is equivalent to multiplying `A` by \(2^B\).

For a given integer `A` and a non-negative integer `B`:

- \[ A  >>  B = A / (2^B) \]

This means shifting the bits of `A` to the right by `B` positions is equivalent to dividing `A` by \(2^B\), and the
result is rounded down to the nearest integer.

Bitwise shifts can be used for multiplication and division by powers of 2.

```java
// Example: Multiplication and division by powers of 2
int x = 10;
int resultMultiply = x << 2; // Equivalent to x * 4
int resultDivide = x >> 1;   // Equivalent to x / 2
```

Left shifts (`<<`) multiply by `2^n`, and right shifts (`>>`) divide by `2^n`. This is often more efficient than using
the `*` and `/` operators.

> While bitwise operators offer performance benefits, it's important to balance optimization with code readability. Use
> comments to explain complex bitwise operations, and prefer readability over micro-optimizations unless performance is
> critical.

## Conclusion

Understanding and utilizing these operators are fundamental to writing efficient and expressive Java programs. Whether
you're performing mathematical calculations, making logical decisions, or manipulating bits, mastering these operators
will enhance your programming skills. As you continue your journey in Java development, keep exploring the nuances of
these operators and their applications in various scenarios.

For more in-depth information, refer to the
official [Java documentation](https://docs.oracle.com/en/java/javase/15/docs/api/index.html).

# Conditional Statements and Loops

### 1. **If-Else Statement:**

- Used to check Boolean conditions (True or False).
- **Syntax:**
  ```java
  if (boolean expression){
      // Body
  } else {
      // Do this
  }
  ```
- **Example:**
  ```java
  public class IfElse {
      public static void main(String[] args) {
          int salary = 25400;
          if (salary > 10000) {
              salary = salary + 2000;
          } else {
              salary = salary + 1000;
          }
          System.out.println(salary);
      }
  }
  ```
- **Output:** 27400

### 2. **Multiple If-Else Statement:**

- Executes one condition from multiple statements.
- **Syntax:**
  ```java
  if (condition1) {
      // Code to be executed if condition1 is true
  } else if (condition2) {
      // Code to be executed if condition2 is true
  } else if (condition3) {
      // Code to be executed if condition3 is true
  } else {
      // Code to be executed if all conditions are false
  }
  ```
- **Example:**
  ```java
  public class MultipleIfElse {
      public static void main(String[] args) {
          int salary = 25400;
          if (salary <= 10000) {
              salary += 1000;
          } else if (salary <= 20000) {
              salary += 2000;
          } else {
              salary += 3000;
          }
          System.out.println(salary);
      }
  }
  ```
- **Output:** 28400

### 3. **Loops:**

- **For Loop:**
    - Used when the number of iterations is known.
    - **Syntax:**
      ```java
      for (initialization; condition; increment/decrement){
          // Body
      }
      ```
    - **Example 1:**
      ```java
      public class ForLoop {
          public static void main(String[] args) {
              for (int num = 1; num <= 5; num += 1){
                  System.out.println(num);
              }
          }
      }
      ```
    - **Output:** 1, 2, 3, 4, 5
    - **Example 2:**
      ```java
      import java.util.Scanner;
      public class ForLoop {
          public static void main(String[] args) {
              Scanner in = new Scanner(System.in);
              int n = in.nextInt();
              for (int num = 1; num <= n; num += 1){
                  System.out.print(num + " ");
              }
          }
      }
      ```
        - **Input:** 6
        - **Output:** 1 2 3 4 5 6

- **While Loop:**
    - Used when the number of iterations is not known.
    - **Syntax:**
      ```java
      while (condition){
          // Code to be executed
          // Increment/Decrement
      }
      ```
    - **Example:**
      ```java
      public class WhileLoop {
          public static void main(String[] args) {
              int num = 1;
              while (num <= 5){
                  System.out.println(num);
                  num += 1;
              }
          }
      }
      ```
    - **Output:** 1, 2, 3, 4, 5

- **Do-While Loop:**
    - Used when the loop needs to execute at least once.
    - Exit-controlled loop.
    - **Syntax:**
      ```java
      do {
          // Code to be executed
          // Update statement (increment/decrement)
      } while (condition);
      ```
    - **Example:**
      ```java
      public class DoWhileLoop {
          public static void main(String[] args) {
              int n = 1;
              do {
                  System.out.println(n);
                  n++;
              } while (n <= 5);
          }
      }
      ```
    - **Output:** 1, 2, 3, 4, 5

- **Comparison between While Loop and Do-While Loop:**

  | While Loop                                              | Do-While Loop                                            |
  |---------------------------------------------------------|----------------------------------------------------------|
  | Used when the number of iterations is not fixed         | Used when we want to execute the statement at least once |
  | Entry-controlled loop                                   | Exit-controlled loop                                     |
  | No semicolon required at the end of `while (condition)` | Semicolon is required at the end of `while (condition)`  |

### 4. **Largest of Three Numbers:**
- **Problem Statement:** "Find largest among three numbers."
- **Approach 1:**
  ```java
  import java.util.Scanner;
  public class LargestOfThree {
      public static void main(String[] args) {
          Scanner in = new Scanner(System.in);
          int a = in.nextInt();
          int b = in.nextInt();
          int c = in.nextInt();
          int max = a;
          if (b > max) {
              max = b;
          }
          if (c > max) {
              max = c;
          }
          System.out.println(max);
      }
  }
  ```
- **Approach 2:**
  ```java
  import java.util.Scanner;
  public class LargestOfThree {
      public static void main(String[] args) {
          Scanner in = new Scanner(System.in);
          int a = in.nextInt();
          int b = in.nextInt();
          int c = in.nextInt();
          int max = 0;
          if (a > b) {
              max = a;
          } else {
              max = b;
          }
          if (c > max) {
              max = c;
          }
          System.out.println(max);
      }
  }
  ```
- **Approach 3 (Using `Math.max`):**
  ```java
  import java.util.Scanner;
  public class LargestOfThree {
      public static void main(String[] args) {
          Scanner in = new Scanner(System.in);
          int a = in.nextInt();
          int b = in.nextInt();
          int c = in.nextInt();
          int max = Math.max(c, Math.max(a, b));
          System.out.println(max);
      }
  }
  ```
- **Input:** 3 6 5
- **Output:** 6

### 5. **Alphabet Case Check:**

- **Problem Statement:**
  "Take an input character from the keyboard and check whether it is an uppercase alphabet or lowercase alphabet."
- Example:
  ```java
  import java.util.Scanner;
  public class AlphabetCaseCheck {
      public static void main(String[] args) {
          Scanner in = new Scanner(System.in);
          char ch = in.next().trim().charAt(0);
          if (ch >= 'a' && ch <= 'z') {
              System.out.println("Lowercase");
          } else {
              System.out.println("Uppercase");
          }
      }
  }
  ```
- **Input:** a
- **Output:** Lowercase
- **Input:** Z
- **Output:** Uppercase

### 6. **Fibonacci Numbers:**

- **Problem Statement:** "Find the nth Fibonacci number."
- **Example:**
  ```java
  import java.util.Scanner;
  public class FibonacciNumbers {
      public static void main(String[] args) {
          Scanner in = new Scanner(System.in);
          int n = in.nextInt();
          int a = 0, b = 1, count = 2;
          while (count <= n) {
              int temp = b;
              b = b + a;
              a = temp;
              count++;
          }
          System.out.println(b);
      }
  }
  ```
- **Input:** 7
- **Output:** 13

### 7. **Counting Occurrence:**

- **Problem Statement:** "Input two numbers, find how many times the second number's digit is present in the first number."
- **Example:**
  ```java
  import java.util.Scanner;
  public class CountingOccurrence {
      public static void main(String[] args) {
          Scanner in = new Scanner(System.in);
          int count = 0;
          int Fn = in.nextInt();
          int Sn = in.nextInt();
          while (Fn > 0) {
              int rem = Fn % 10;
              if (rem == Sn) {
                  count++;
              }
              Fn = Fn / 10;
          }
          System.out.println(count);
      }
  }
  ```
- **Input:** 45535 5
- **Output:** 3

### 8. **Reverse a Number:**

- **Problem Statement:** "Input a number from the keyboard and show the output as the reverse of that number."
- Example:
  ```java
  import java.util.Scanner;
  public class ReverseANumber {
      public static void main(String[] args) {
          Scanner in = new Scanner(System.in);
          int num = in.nextInt();
          int reversedNum = 0;
          while (num > 0) {
              int rem = num % 10;
              num /= 10;
              reversedNum = reversedNum * 10 + rem;
          }
          System.out.println(reversedNum);
      }
  }
  ```
- **Input:** 458792
- **Output:** 297854

### 9. **Calculator Program:**

- Example of a simple calculator program.
- Input and output are managed until the user presses 'X' or 'x'.

   ```java
   import java.util.Scanner;
   public class Calculator {
       public static void main(String[] args) {
           Scanner in = new Scanner(System.in);
           int ans = 0;
           while (true) {
               System.out.print("Enter the operator: ");
               char op = in.next().trim().charAt(0);
               if (op == '+' || op == '-' || op == '*' || op == '/' || op == '%') {
                   System.out.print("Enter two numbers: ");
                   int num1 = in.nextInt();
                   int num2 = in.nextInt();
                   switch (op) {
                       case '+':
                           ans = num1 + num2;
                           break;
                       case '-':
                           ans = num1 - num2;
                           break;
                       case '*':
                           ans = num1 * num2;
                           break;
                       case '/':
                           if (num2 != 0) {
                               ans = num1 / num2;
                           }
                           break;
                       case '%':
                           ans = num1 % num2;
                           break;
                   }
               } else if (op == 'x' || op == 'X') {
                   break;
               } else {
                   System.out.println("Invalid operation!!");
               }
               System.out.println(ans);
           }
       }
   }
   ```

## 10. Conclusion:

To wrap up, diving into Conditional Statements and Loops equips you with essential tools for effective programming. The covered topics, from basic If-Else statements to versatile loops, offer practical solutions for various scenarios. The hands-on examples, like finding the largest number or building a basic calculator, reinforce your skills and prepare you for real-world coding challenges. In a nutshell, this learning journey sets a strong foundation for making informed decisions and handling repetitive tasks in Java programming.
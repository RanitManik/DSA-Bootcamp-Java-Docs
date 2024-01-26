# Arrays and ArrayList in Java

In this section, we will focus on two important concepts: **arrays** and
**ArrayLists**.

Arrays are fixed-size collections that allow you to store and access multiple values using a single variable. They are
useful when dealing with collections of elements of the same type.

ArrayLists, on the other hand, are dynamic collections that can grow or shrink as needed. They provide flexible storage
and manipulation of elements.

By understanding arrays and ArrayLists, you will gain valuable tools for organizing and managing data in your Java
programs.

## Array

At its core, an array is a data structure that houses a fixed-size sequential collection of elements of uniform type.
The array's strength lies in its ability to access elements through indices, providing seamless retrieval, modification,
and iteration capabilities.

* ### Why we need Arrays?

Arrays emerge as indispensable data structures, offering a systematic approach to store and manipulate collections of
elements sharing a common data type. They embody an efficient means of handling multiple values under a single variable,
fostering a streamlined coding paradigm.

* ### Syntax of an Array

Declaring an array entails specifying the data type, followed by the array name and square brackets indicating the size
or dimension.

```java
int[] numbers = new int[5];
```

### Direct hit Program: Store 5 Roll Numbers

```java
public class ArrayExample {
    public static void main(String[] args) {
        int[] rollNumbers = {101, 102, 103, 104, 105};
    }
}
```

* ### How does Array work?

Arrays leverage contiguous memory locations for storing elements, ensuring swift and efficient access. A fundamental
comprehension of their internal workings is crucial for optimizing code and managing memory effectively.

* ### Internal Working of an Array

The internal working of an array involves the way it is stored in memory and how elements are accessed using indices.
Here's an overview of the internal workings of a basic, one-dimensional array:

1. **Memory Allocation:**

    - When you declare an array, the programming language allocates a contiguous block of memory to store all its
      elements.
      The size of this block is determined by the number of elements in the array multiplied by the size of each
      element.

2. **Indexing:**

    - The elements in an array are accessed using indices. The index serves as an offset from the starting memory
      address of
      the array.
    - The formula for accessing the memory location of an element is often as
      follows: `memory_location = base_address + (index * element_size)`.
    - For example, if the base address of an array is 1000, and each element is 4 bytes in size, accessing the element
      at
      index 2 would involve calculating `1000 + (2 * 4) = 1008`.

3. **Contiguous Memory:**

    - Because the elements are stored sequentially in memory, moving from one element to the next involves incrementing
      the
      memory address by the size of each element.
    - This contiguous nature allows for efficient access to elements and supports operations like iteration.

4. **Fixed Size:**

    - The size of the array is fixed at the time of declaration. This fixed size is known to the compiler, and it
      reserves
      the necessary amount of memory accordingly.

5. **Zero-Based Indexing:**

    - In many programming languages, array indices start from 0. This means that the first element of the array is at
      index
      0, the second at index 1, and so on.

6. **Initialization:**

    - When you initialize an array by assigning values to its elements, the programming language takes care of placing
      those
      values in the respective memory locations.

7. **Dynamic Memory Allocation (in some cases):**

    - In certain programming languages, arrays can be dynamically allocated at runtime using constructs like `malloc` (
      in C)
      or `new` (in C++). In such cases, the memory for the array is allocated on the heap, and the array size can be
      determined dynamically.

Understanding the internal workings of arrays is essential for writing efficient and optimized code. It allows
programmers to make informed decisions about data access, manipulation, and memory usage.

* ### Dynamic Memory Allocation

In Java, arrays are static, implying a fixed size upon declaration. To infuse dynamic behavior, alternative data
structures like ArrayLists can be considered.

* ### Application of arrays

Arrays are widely used due to their efficiency and simplicity. They find applications in various algorithms such as
sorting and searching, and they play a key role in data compression techniques.

> It's important to note that while arrays offer fast access to elements, their size is fixed upon declaration, and they
> may not be the most suitable choice if dynamic resizing is required. Other data structures like linked lists or
> dynamic
> arrays may be preferred in such cases.

* ### Continuity of an Array

Array elements are stored in contiguous memory locations. This allows for efficient memory access and retrieval based on
the index.
The contiguous nature of arrays makes it possible to perform arithmetic on indices to access elements directly.

* ### Index of an Array

Array indexing initiates at 0, representing the first element, and spans up to `length - 1`.

* ### String Array

Arrays transcend primitive types and can store objects, such as strings.
for example:

```Java
// Declaring a string array
String[] fruits = {"Apple", "Banana", "Orange", "Mango"};
```

* ### What is null in Java?

In Java, `null` signifies the absence of a value or the default value for object references.

* ### null is used as a default

Upon array initialization without explicit population, elements default to `null`.

* ### Array Input

Arrays can be populated through user input or predefined values.

```java
Scanner scanner = new Scanner(System.in);
int[] userInputArray = new int[5];

for (int i = 0; i < 5; i++) {
    System.out.println("Enter value for index " + i + ": ");
    userInputArray[i] = scanner.nextInt();
}
```

* ### for-each loop

The for-each loop simplifies array iteration, enhancing code readability.

```java
for (int num : numbers) {
    // num represents each element in the array
}
```

* ### toString() Method

The `toString()` method furnishes a string representation of an array, aiding in debugging and logging.

```java
int[] exampleArray = {1, 2, 3, 4, 5};
System.out.println(Arrays.toString(exampleArray));
```

* ### Array of Objects

Arrays transcend primitive types and can store objects, enabling the creation of intricate data structures.

```Java
package L12_Array_Arraylist;

import java.util.Arrays;
import java.util.Scanner;

public class Array_of_objects {
    public static void main(String[] args) {
        System.out.println("Enter the Array inputs: ");
        Scanner in = new Scanner(System.in);

        // array of objects ==>
        String[] str = new String[4];
        for (int i = 0; i < str.length; i++) {
            str[i] = in.next();
        }
        System.out.println(Arrays.toString(str));

        // modify array ==>
        str[0] = "Ranit";
        str[1] = "Manik";
        // the first two elements of array 'str' will be overridden

        // printing the array after modification
        System.out.println(Arrays.toString(str)); 
    }
}
```

* ### Storage of Objects in Heap

Objects within an array find residence in heap memory, with array variables holding references to these objects.

* ### Array Passing in Function

Arrays can be passed as parameters to methods, fostering code modularity and reusability.

```java
void processArray(int[] array) {
    // Perform operations on the array
}
```

- example:

```Java
package L12_Array_Arraylist;

import java.util.Arrays;

public class Passing_in_functions {
public static void main(String[] args) {
int[] nums = {3, 4, 5, 12};
System.out.println(Arrays.toString(nums));
change(nums);
System.out.println(Arrays.toString(nums));
}

    // This behaviour is called 'mutability' ==> Arrays are mutable
    static void change(int[] arr) {
        arr[0] = 99;
    }
}
```

* ### Array Methods

In Java, arrays are a fundamental part of the language, and there are several built-in methods to manipulate
and work with arrays. Here are some commonly used array methods in Java:

1. **`length` property:**
    - Returns the number of elements in the array.
   ```java
   int[] arr = {1, 2, 3, 4, 5};
   int length = arr.length; // length is 5
   ```

2. **`clone` method:**
    - Creates a shallow copy of the array.
   ```java
   int[] arr = {1, 2, 3, 4, 5};
   int[] arrCopy = arr.clone();
   ```

3. **`toString` method:**
    - Converts the array to a string representation.
   ```java
   int[] arr = {1, 2, 3, 4, 5};
   String arrString = Arrays.toString(arr);
   ```

4. **`sort` method:**
    - Sorts the array in ascending order.
   ```java
   int[] arr = {5, 2, 8, 1, 3};
   Arrays.sort(arr); // arr is now [1, 2, 3, 5, 8]
   ```

5. **`binarySearch` method:**
    - Searches for a specified value using a binary search algorithm (requires the array to be sorted).
   ```java
   int[] arr = {1, 2, 3, 5, 8};
   int index = Arrays.binarySearch(arr, 5); // index is 3
   ```

6. **`fill` method:**
    - Fills the array with a specified value.
   ```java
   int[] arr = new int[5];
   Arrays.fill(arr, 42); // arr is now [42, 42, 42, 42, 42]
   ```

7. **`copyOf` method:**
    - Copies the specified range of the array into a new array.
   ```java
   int[] arr = {1, 2, 3, 4, 5};
   int[] newArr = Arrays.copyOf(arr, 3); // newArr is [1, 2, 3]
   ```

These are just a few examples of array methods in Java. There are more methods available in the `Arrays` class for
various array operations. You can explore
the [Java documentation for `java.util.Arrays`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/Arrays.html)
for a comprehensive list and
details.

## Arraylist

An `ArrayList` is a data structure in programming that is part of the Java programming language and some other
languages. It is a dynamic array implementation, meaning it can dynamically resize itself to accommodate a varying
number of elements.

### Syntax

- The syntax involves creating an `ArrayList` object with a specified type, for example:
  ```java
  ArrayList<Integer> list = new ArrayList<>();
  ```

### ArrayList Methods

- `add(element)`: Adds an element to the end of the ArrayList.
- `contains(element)`: Checks if the ArrayList contains a specific element.
- `set(index, element)`: Sets the element at a specified index.
- `remove(index)`: Removes the element at a specified index.

### Input

- Utilize a `Scanner` object to take user input for populating an ArrayList, for example:
  ```java
  Scanner in = new Scanner(System.in);
  ArrayList<Integer> list1 = new ArrayList<>();
  for (int i = 0; i < 5; i++) {
      list1.add(in.nextInt());
  }
  ```

### Output using basic print method

- Simply print the ArrayList using `System.out.println()`. This prints the elements in the ArrayList.

### Output using get() method

- Iterate through the ArrayList using a loop and print each element using the `get(index)` method, for example:
  ```java
  for (int i = 0; i < list1.size(); i++) {
      System.out.print(list1.get(i) + " ");
  }
  ```

### Index of an ArrayList

- Retrieve the element at a specific index using the `get(index)` method, for example:
  ```java
  System.out.println("The element at index 1 is: " + list1.get(1));
  ```

### How is ArrayList capable of storing more than their size?

- Internally, ArrayList has a fixed size. When it reaches its capacity and needs more space:
    - It creates a new ArrayList with double the size.
    - Copies the old elements to the new ArrayList.
    - The old ArrayList is deleted.
    - This process ensures that ArrayLists can dynamically resize and handle more elements than their initial
      capacity.

### Arraylist example

```Java
package L12_Array_Arraylist;

import java.util.ArrayList;
import java.util.Scanner;

public class Array_list_example {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        // syntax ==>
        ArrayList<Integer> list = new ArrayList<>(4); 
        // here 'list' is the reference variable
        // ArrayList is a class that belongs from JAVA collection framework
        // classes are written in Capital letters in JAVA

        // Array list Methods ==>
        list.add(65);
        list.add(66);
        list.add(67);
        list.add(68);
        list.add(69);

        System.out.println(list.contains(67));
        System.out.println(list.contains(695));

        list.set(0, 99); // setting 0th index as '99'
        System.out.println(list);

        list.remove(2); // removes a specific index
        System.out.println(list);

        // input ==>
        System.out.println("Enter the elements of list1: ");
        ArrayList<Integer> list1 = new ArrayList<>(4);
        for (int i = 0; i < 5; i++) {
            list1.add(in.nextInt());
        }
        // output using basic print method ==>
        System.out.println(list1);

        // output using get() method ==>
        for (int i = 0; i < 5; i++) {
            System.out.print(list1.get(i) + " "); 
            // pass index here, list[index] syntax will not work here
        }


        // index of an arraylist ==>
        System.out.println("\nThe 1st index of the arraylist is :"); 
        // '\n'(backslash n) works for every programming language
        
        System.out.println(list1.get(1));

        // how is arraylist capable of storing more than their size?
        // ==>
        /*
        1. size is fixed internally
        2. say arraylist fills by some amount
        ==> it will create a new empty arraylist of double the size
        ==> old elements are copied in the new list
        ==> old one is deleted
        ==> amortized time complexity
         */
    }
}

```

### ArrayList Insertion and Shifting Behavior

In Java, the `ArrayList` class dynamically resizes and shifts elements when inserting at specific positions:

1. **Insertion at Specified Index:**
    - When you use `add(int index, E element)` on an `ArrayList`, it inserts the specified element at the specified
      index.
    - Elements at and to the right of the specified index are shifted to the right.

2. **Dynamic Resizing:**
    - If the internal array is full, `ArrayList` dynamically increases its capacity.
    - Existing elements are copied to the new, larger array.
    - The new element is then inserted at the specified index in the resized array.

### Example:

```java
import java.util.ArrayList;

public class ArrayListInsertionExample {
    public static void main(String[] args) {
        // Create an ArrayList of integers
        ArrayList<Integer> list = new ArrayList<>();

        // Add elements to the ArrayList
        list.add(0, 10);   // ArrayList: [10]
        list.add(1, 20);   // ArrayList: [10, 20]
        list.add(1, 30);   // ArrayList: [10, 30, 20]

        // Print the ArrayList
        System.out.println("ArrayList: " + list);
    }
}
```

In this example, when `list.add(1, 30)` is called, the `ArrayList` shifts the element 20 to the right to make room for
the new element 30 at index 1.

### Behavior Summary:

- **Insertion:** Inserts the specified element at the specified index.
- **Shifting:** Shifts existing elements to the right starting from the specified index.

### Advantages:

- **Dynamic Sizing:** `ArrayList` automatically adjusts its size, making it suitable for scenarios with varying numbers
  of elements.

- **Efficient Insertions:** Efficient for frequent insertions and removals compared to arrays.

### Considerations:

- **Performance:** While efficient for most use-cases, inserting elements in the middle of large lists may have
  performance implications due to the shifting of elements.

> Understanding this behavior is crucial for effectively utilizing ArrayList in scenarios where elements need to be
> inserted at specific positions. This shifting and inserting technique is quite useful for efficiently inserting data at
> a specific position.

## Multidimensional Arrays

Arrays can extend into multiple dimensions, giving rise to matrices or tables of values.

* ### Syntax of a 2D Array

```java
int[][] matrix = new int[3][4];
```

* ### Internal Working of a 2D Array

A 2D array essentially comprises an array of arrays, with each sub-array representing a row.

* ### 2D Array Input

Populating a 2D array involves nested loops for row and column indices.

```java
Scanner scanner = new Scanner(System.in);
int[][] matrix = new int[3][4];

for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 4; j++) {
        System.out.println("Enter value for element at position [" + i + "][" + j + "]: ");
        matrix[i][j] = scanner.nextInt();
    }
}
```

* ### 2D Array Output

Iterating over a 2D array and printing its elements employs nested loops.

```java
for (int[] row : matrix) {
    for (int element : row) {
        System.out.print(element + " ");
    }
    System.out.println();
}
```

* ### Multidimensional Array example

```Java
package L12_Array_Arraylist;

import java.util.Arrays;

public class Multidimensional_array {
    public static void main(String[] args) {
        /*
        2D array structure ==>
        1 2 3
        4 5 6
        7 8 9
         */

        // syntax to declare a 2D array ==>
        int[][] a = new int[3][]; // no of columns is not necessary to specify
        // no of rows is mandatory

        // syntax to store data into a 2D array ==>
        int[][] b = {
                {2, 3, 4}, // 0th index
                {5, 6, 7}, // 1st index
                {7, 8, 9}, // 2nd index
        };
        // 2D array ==> array of internal arrays
        // array 'b' is collection of 3 internal arrays ==>
        // 0th index ==> {2, 3, 4}, 1st index ==> {5, 6, 7} and 2nd index ==> {7, 8, 9}
        // size of the individual rows does not matter ==>
        // each internal array can have variable amount of elements

        // 2D array with variable number of elements in each row ==>
        int[][] arr2D = {
                {2, 3}, // 0th index
                {5, 6, 7}, // 1st index
                {7, 8, 9, 10}, // 2nd index
        };

        // indexing in a 2D array ==>
        /*
        arr2D[0] = {2, 3}
        arr2D[1] = {5, 6, 7}
        arr2D[2] = {7, 8, 9, 10}
         */

        // printing a 2D array ==>
        System.out.println("The array is printing using  'enhanced for' loop: ");
        for (int[] ints : arr2D) {
            System.out.println(Arrays.toString(ints));
        }

        // printing the internal elements of a 2D array ==>
        System.out.println("This are all the indexes of the 2D array: ");
        System.out.println("1st index: " + Arrays.toString(arr2D[0])); // 0th index
        System.out.println("2nd index: " + Arrays.toString(arr2D[1])); // 1st index
        System.out.println("3rd index: " + Arrays.toString(arr2D[2])); // 2nd index

        // length of a 2D array => length of rows ==>
        System.out.println("length of rows is: " + arr2D.length); 
        // this will give us the length of rows
    }
}

```

### Dynamic Arrays

For dynamic resizing, consider the use of ArrayLists or other dynamic data structures.

```java
ArrayList<Integer> dynamicArray = new ArrayList<>();
dynamicArray.add(10);
dynamicArray.add(20);
```

* ### Multidimensional Arraylist example

```Java
package L12_Array_Arraylist;

import java.util.ArrayList;
import java.util.Scanner;

public class Multidimensional_arraylist {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        System.out.println("Enter 9 elements of the arraylist 'list': ");

        // initializing a 2d Arraylist ==>
        ArrayList<ArrayList<Integer>> list = new ArrayList<>();
        for (int i = 0; i < 3; i++) {
            list.add(new ArrayList<>());
        }

        // adding elements ==>
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                list.get(i).add(in.nextInt());
            }
        }

        // printing a 2D arraylist ==>
        System.out.println(list);
    }
}

```

## Programs

### 🎯 Program: Swapping Values in an Array

```java
void swap(int[] array, int index1, int index2) {
    int temp = array[index1];
    array[index1] = array[index2];
    array[index2] = temp;
}
```

### 🎯 Program: Maximum Value of an Array

```java
int findMax(int[] array) {
    int max = array[0];
    for (int num : array) {
        if (num > max) {
            max = num;
        }
    }
    return max;
}
```

### 🎯 Program: Reversing an Array

```java
void reverseArray(int[] array) {
    int start = 0;
    int end = array.length - 1;
    while (start < end) {
        int temp = array[start];
        array[start] = array[end];
        array[end] = temp;
        start++;
        end--;
    }
}
```

### 🎯 Program: Column no not fixed of an 2d array

```java
package A05_arrays.src;

import java.util.Arrays;

public class Column_not_fixed {
    public static void main(String[] args) {
        int[][] arr = {
                {1, 2, 3},
                {5, 4},
                {6, 7, 8, 9},
        };

        // printing a miscellaneous column sized 2D array ==>

        // 1. printing it through the traditional for loop ==>
        for (int row = 0; row < arr.length; row++) {
            for (int col = 0; col < arr[row].length; col++) {
                System.out.print(arr[row][col] + " ");
            }
            System.out.println();
        }

        // 2. printing it  using 'to.string()' method with for-each loop ==>
        System.out.println("The array is printing 
        using 'to.string()' method with enhanced for loop:");
        for (int[] ints : arr) {
            System.out.println(Arrays.toString(ints));
        }
    }
}

```

This comprehensive document serves as a robust reference for Java methods, covering arrays, multidimensional arrays, and
associated functions. Gaining proficiency in these concepts is imperative for crafting efficient and organized Java
code.
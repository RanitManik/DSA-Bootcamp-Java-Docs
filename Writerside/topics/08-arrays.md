# Arrays and ArrayList in Java

In the realm of Java programming, methods serve as pivotal building blocks, orchestrating the organization and structure
of code. They facilitate modularity and reusability, elevating code readability and maintainability. This document
delves into the intricate nuances of Java methods, encompassing a spectrum of topics from fundamental syntax to
sophisticated concepts like multidimensional arrays and ArrayLists.

## Array

* ### Why we need Arrays?

Arrays emerge as indispensable data structures, offering a systematic approach to store and manipulate collections of
elements sharing a common data type. They embody an efficient means of handling multiple values under a single variable,
fostering a streamlined coding paradigm.

* ### What is an Array?

At its core, an array is a data structure that houses a fixed-size sequential collection of elements of uniform type.
The array's strength lies in its ability to access elements through indices, providing seamless retrieval, modification,
and iteration capabilities.

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

Arrays utilize indices to access elements, with each element occupying a specific memory location determined by its
index.

* ### Dynamic Memory Allocation

In Java, arrays are static, implying a fixed size upon declaration. To infuse dynamic behavior, alternative data
structures like ArrayLists can be considered.

* ### Internal Representation of Array

The internal representation delves into how elements are stored in memory and accessed via indices.

* ### Continuity of an Array

Elements reside consecutively in memory, facilitating easy traversal and manipulation.

* ### Index of an Array

Array indexing initiates at 0, representing the first element, and spans up to `length - 1`.

* ### String Array

Arrays transcend primitive types and can store objects, such as strings.

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

```java
Person[] people = new Person[3];
people[0] = new Person("John");
people[1] = new Person("Jane");
people[2] = new Person("Doe");
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

## Arraylist

An `ArrayList` is a data structure in programming that is part of the Java programming language and some other
languages. It is a dynamic array implementation, meaning it can dynamically resize itself to accommodate a varying
number of elements.

### Syntax:

- The syntax involves creating an `ArrayList` object with a specified type, for example:
  ```java
  ArrayList<Integer> list = new ArrayList<>();
  ```

### ArrayList Methods:

- `add(element)`: Adds an element to the end of the ArrayList.
- `contains(element)`: Checks if the ArrayList contains a specific element.
- `set(index, element)`: Sets the element at a specified index.
- `remove(index)`: Removes the element at a specified index.

### Input:

- Utilize a `Scanner` object to take user input for populating an ArrayList, for example:
  ```java
  Scanner in = new Scanner(System.in);
  ArrayList<Integer> list1 = new ArrayList<>();
  for (int i = 0; i < 5; i++) {
      list1.add(in.nextInt());
  }
  ```

### Output using basic print method:

- Simply print the ArrayList using `System.out.println()`. This prints the elements in the ArrayList.

### Output using get() method:

- Iterate through the ArrayList using a loop and print each element using the `get(index)` method, for example:
  ```java
  for (int i = 0; i < list1.size(); i++) {
      System.out.print(list1.get(i) + " ");
  }
  ```

### Index of an ArrayList:

- Retrieve the element at a specific index using the `get(index)` method, for example:
  ```java
  System.out.println("The element at index 1 is: " + list1.get(1));
  ```

### How is ArrayList capable of storing more than their size?:

- Internally, ArrayList has a fixed size. When it reaches its capacity and needs more space:
    - It creates a new ArrayList with double the size.
    - Copies the old elements to the new ArrayList.
    - The old ArrayList is deleted.
    - This process ensures that ArrayLists can dynamically resize and handle more elements than their initial
      capacity.

## Multidimensional Arrays

Arrays can extend into multiple dimensions, giving rise to matrices or tables of values.

### Syntax of a 2D Array

```java
int[][] matrix = new int[3][4];
```

### Internal Working of a 2D Array

A 2D array essentially comprises an array of arrays, with each sub-array representing a row.

### 2D Array Input

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

### 2D Array Output

Iterating over a 2D array and printing its elements employs nested loops.

```java
for (int[] row : matrix) {
    for (int element : row) {
        System.out.print(element + " ");
    }
    System.out.println();
}
```

### Dynamic Arrays

For dynamic resizing, consider the use of ArrayLists or other dynamic data structures.

```java
ArrayList<Integer> dynamicArray = new ArrayList<>();
dynamicArray.add(10);
dynamicArray.add(20);
```

## Array Functions

Java provides a repertoire of utility methods and functions for array manipulation, including sorting and searching.

```java
int[] arrayToSort = {3, 1, 4, 1, 5, 9, 2, 6, 5};
Arrays.sort(arrayToSort);

int indexOfValue = Arrays.binarySearch(arrayToSort, 4);
```

### Internal Working of ArrayList

ArrayLists dynamically resize themselves, affording flexibility in managing collections of elements.

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

This comprehensive document serves as a robust reference for Java methods, covering arrays, multidimensional arrays, and
associated functions. Gaining proficiency in these concepts is imperative for crafting efficient and organized Java
code.
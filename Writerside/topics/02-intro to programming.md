# Introduction to Programming

Programming is the process of providing instructions to a computer to perform various tasks. Computers operate in
binary, using only 0's and 1's. However, instructing computers in binary is extremely challenging for humans. To bridge
this gap, programming languages are employed. These languages serve as a medium for programmers to communicate with
computers, allowing them to write instructions in a more human-readable format.

## Types of Programming Languages

### Procedural Programming

Procedural programming involves specifying a series of well-structured steps and procedures to compose a program. It
relies on a systematic order of statements, functions, and commands to complete a task.

### Functional Programming

Functional programming entails writing a program using pure functions, where variables are never modified but only
create new ones as output. This approach is useful in situations where multiple operations need to be performed on the
same set of data, such as in machine learning.

### Object-Oriented Programming (OOP)

Object-oriented programming revolves around objects, combining both code and data. The fundamental idea is that code and
data are encapsulated into objects, making it easier to develop, debug, reuse, and maintain software.

"One programming language can be of all three types, like Python. Java follows both procedural and object-oriented
paradigms."

## Static vs Dynamic Languages

| Feature                      | Static Languages                      | Dynamic Languages                                           |
|------------------------------|---------------------------------------|-------------------------------------------------------------|
| **Type Checking**            | Performed at compile time             | Performed at runtime                                        |
| **Error Detection**          | Errors detected during compilation    | Errors might not surface until runtime                      |
| **Declaration of Datatypes** | Datatypes must be declared before use | No need to declare datatype of variables                    |
| **Control**                  | More control over the program         | Saves time in writing code, but errors may occur at runtime |
| **Examples**                 | C, C++, Java                          | Python, JavaScript                                          |

## Memory Management

Memory in programming is managed through two types: Stack and Heap.

- **Stack Memory:** Stores reference variables.
- **Heap Memory:** Stores the objects of reference variables.

For example, when declaring a variable "a = 10," "a" is the reference variable stored in stack memory, and "10" is the
object stored in heap memory.

### Stack Memory vs. Heap Memory

When we write code, our computer allocates memory in two main areas: stack memory and heap memory. The stack is used for
storing variables and function calls, while the heap is reserved for the actual objects and their values.

Let's consider a simple statement like `a = 10`. Here, `a` is a reference variable, not the actual value. The value `10`
is the object, stored in the heap memory. The reference variable `a` in the stack memory points to the object in the
heap.

### Reference Variables and Objects

It's crucial to understand that the reference variable (`a`) is not the object itself; it's merely a pointer to the
object. If we change the value via `a`, the original object in the heap memory is altered. In essence, the stack memory
contains variables pointing to objects in the heap memory.

### Objects, Types, and Classes

Objects have types, which are defined by classes. For instance, if we have a person named "Kunal," the object is Kunal,
and the reference variable (`a`) points to that object. Classes help define these types and play a significant role in
object-oriented programming.

### Multiple Pointers to the Same Object

One fascinating aspect is that multiple reference variables can point to the same object. If we have variables `a`
and `b` both pointing to an object, changing the object via one variable reflects that change for all variables pointing
to it. This behavior is crucial in understanding how data modifications affect different parts of your code.

### Garbage Collection

When no reference variable points to an object anymore, it becomes eligible for garbage collection. This process
automatically frees up memory by removing objects without references. It ensures efficient memory usage in your program.

### Dynamic Typing

In dynamically-typed languages like Python, variable types are determined at runtime. This flexibility allows variables
to point to different objects during the program's execution, enhancing adaptability and ease of use.

### Practical Example

Consider a simple Python list: `a = [1, 3, 5, 9]` and `b = a`. Both `a` and `b` point to the same list object. If we
modify the list via `a`, the changes are visible through `b` as well.

### Points to Remember

- Multiple reference variables can point to the same object.
- Changes made to the object of any reference variable are reflected in all other variables pointing to the same object.
- Objects without reference variables are automatically destroyed by the process of "Garbage Collection."

### Conclusion

Understanding memory management and reference variables is foundational to writing robust code. Whether you're dealing
with integers, strings, or complex data structures, grasping these concepts will empower you to write more efficient and
reliable programs.

Remember, coding is not just about syntax; it's about understanding how your code interacts with the computer's memory.
Happy coding!

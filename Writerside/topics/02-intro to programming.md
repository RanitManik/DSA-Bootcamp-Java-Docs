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

### Points to Remember

- Multiple reference variables can point to the same object.
- Changes made to the object of any reference variable are reflected in all other variables pointing to the same object.
- Objects without reference variables are automatically destroyed by the process of "Garbage Collection."
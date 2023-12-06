# Introduction to Java

**Why do we use Programming language?**

- Computers only understand 0’s and 1’s, making it challenging for humans to instruct them directly.
- Programming languages serve as an intermediary, allowing humans to write code in a more readable format.

**Java as a Programming Language:**

- Java code is human-readable and saved with the extension `.java`.
- The code written in Java is known as source code.

**Java Compiler:**

- The Java compiler converts source code into bytecode with the extension `.class`.
- Bytecode doesn't directly run on the system; it requires the Java Virtual Machine (JVM) for execution.
- Java's platform independence is achieved through this compilation to bytecode.

**Java Interpreter:**

- The Java interpreter converts bytecode to machine code (0’s and 1’s).
- It translates the bytecode line by line into machine code during execution.

## More About Platform Independence

- Bytecode can run on all operating systems.
- Source code is converted to machine code through compilation, turning it into executable code.
- In Java, the result is bytecode, and JVM converts this to machine code.
- While Java is platform-independent, JVM is platform-dependent.

## Architecture of Java

### Java Architecture Overview

1. **JDK (Java Development Kit)**
    - **Description:** Comprehensive package for Java development.
    - **Components:**
        - JRE (Java Runtime Environment)
        - Development Tools (Compiler, Debugger, etc.)

2. **JRE (Java Runtime Environment)**
    - **Description:** Provides the runtime environment for Java applications.
    - **Components:**
        - JVM (Java Virtual Machine)
        - Library Classes

3. **JVM (Java Virtual Machine)**
    - **Description:** Executes Java bytecode, providing platform independence.
    - **Functions:**
        - Interprets Java bytecode line by line.
        - Utilizes JIT (Just-In-Time) compilation for performance optimization.

4. **JIT (Just-In-Time Compilation)**
    - **Description:** Dynamic compilation technique used by the JVM.
    - **Functionality:**
        - Translates portions of Java bytecode into native machine code at runtime.
        - Enhances the execution speed of Java applications.

### Relationship Between Components

- **JDK = JRE + Development Tools**
    - The JDK encompasses both the runtime environment (JRE) and essential development tools for creating Java
      applications.

- **JRE = JVM + Library Classes**
    - The JRE consists of the Java Virtual Machine (JVM) responsible for executing bytecode and a set of library classes
      used by Java applications.

### Key Benefits of Java Architecture

- **Platform Independence:**
    - Java bytecode allows "write once, run anywhere" (WORA) capability, enabling Java applications to run on diverse
      devices with compatible JVMs.

- **Dynamic Optimization:**
    - JIT compilation enhances performance by translating bytecode into native machine code during runtime.

This structured overview highlights the interdependence of components in the Java architecture and their roles in
providing a robust and platform-independent environment for Java development and execution.

* Please click on the provided link to view the image and explore the visual representation of the architecture.
  [image link](https://cdn.hashnode.com/res/hashnode/image/upload/v1629049665500/jO3cAZZWn.png?auto=compress,format&format=webp)

## Compile Time

- After obtaining the `.class` file, at runtime:
    1. Class loader loads all classes needed to execute the program.
    2. JVM sends code to the bytecode verifier to check the format of the code.

## Runtime

This visual representation illustrates the flow of components during the runtime of a Java application. The Class Loader
loads classes, the Bytecode Verifier ensures their integrity, the Interpreter executes bytecode, and the Runtime manages
overall program execution. All these components interact with the underlying Hardware.

```
+-----------------------------------+
|            Application            |
|    +------------------------+     |
|    |      Class Loader      |     |
|    +------------------------+     |
|                |                |
|                v                |
|    +------------------------+     |
|    |   Bytecode Verifier    |     |
|    +------------------------+     |
|                |                |
|                v                |
|    +------------------------+     |
|    |       Interpreter      |     |
|    +------------------------+     |
|                |                |
|                v                |
|    +------------------------+     |
|    |        Runtime         |     |
|    +------------------------+     |
|                |                |
|                v                |
|    +------------------------+     |
|    |        Hardware        |     |
|    +------------------------+     |
+-----------------------------------+
```

### Class Loader (How JVM Works)

1. **Loading:**
    - Reads the `.class` file and generates binary data.
    - Creates an object of this class in the heap.

2. **Linking:**
    - JVM verifies the `.class` file.
    - Allocates memory for class variables and default values.
    - Replaces symbolic references with direct references.

3. **Initialization:**
    - All static variables are assigned values defined in the code and static blocks.
    - JVM contains stack and heap memory locations.

### JVM Execution

- **Interpreter:**
    - Line by line execution.
    - When one method is called multiple times, it interprets again and again.

- **JIT (Just-In-Time):**
    - Provides direct machine code for repeated methods, eliminating the need for interpretation.
    - Improves execution speed.

- **Garbage Collector:**
    - Manages memory by reclaiming space occupied by objects no longer in use.

## Working of Java Architecture

This image demonstrates the flow from Java source code to execution on hardware. The Java source code is
compiled
using the Java Development Kit (JDK) to produce bytecode. The Java Runtime Environment (JRE) provides the Java Virtual
Machine (JVM), which interprets the bytecode and, in some cases, uses Just-In-Time Compilation for optimized execution
on the underlying hardware.

<img src="https://www.edureka.co/blog/wp-content/uploads/2019/07/q.png" alt="working of JAVA architecture"/>
## Tools Required to Run Java on a Machine

1. **JDK (Java Development Kit):**
   [Download JDK](https://www.oracle.com/in/java/technologies/javase-downloads.html)

2. **IntelliJ IDEA (Integrated Development Environment):**
    - For Windows: [Download IntelliJ IDEA for Windows](https://www.jetbrains.com/idea/download/#section=windows)
    - For macOS: [Download IntelliJ IDEA for macOS](https://www.jetbrains.com/idea/download/#section=mac)
    - For Linux: [Download IntelliJ IDEA for Linux](https://www.jetbrains.com/idea/download/#section=linux)
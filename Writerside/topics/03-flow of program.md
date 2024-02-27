# Flow of the Program

## Flow Chart

A **flow chart** is a visualization of the thought process or algorithm, represented diagrammatically. It uses various
symbols to depict different elements in the flow of a program:

1. **Start / Stop:** Oval shape indicating the starting and ending points of the flow chart.
2. **Input / Output:** Parallelogram used to represent input and output.
3. **Processing:** Rectangle used to represent processes such as mathematical computations or variable assignments.
4. **Condition:** Diamond shape used to represent conditional statements resulting in true or false (Yes or No).
5. **Flow Direction:** Arrow shape used to represent the flow of the program.

### Examples:

1. **Example 1:**
    - Task: Take a name and output "Hello, name."
    - Flow Chart:
         ```mermaid
      graph TD
      A(Start) --> B(Input name)
      B --> C(Process: Output 'Hello, name')
      C --> D(Stop)
        
      ```

2. **Example 2:**
    - Task: Take input of a salary. If the salary is greater than `10,000`, add a bonus of `2000`; otherwise, add a
      bonus
      of `1000`.
    - Flow Chart:
   ```mermaid
      graph TD
      A(Start) --> B(Input Salary)
      B --> C(Condition: Salary > 10000?)
      C -->|Yes| D(Process: Salary = Salary + 2000)
      C -->|No| E(Process: Salary = Salary + 1000)
      D --> F(Output Salary)
      E --> F
      F --> G(Stop)
        
      ```

3. **Example 3:**
    - Task: Input a number and print whether it is prime or not.
    - Flow Chart: 
   ```mermaid
   graph TD
   A(Start) --> B(Input num)
   B --> C(Condition: num <= 1?)
   C -->|Yes| D(Process: Print Neither prime nor composite)
   C -->|No| E(Condition: Loop through factors)
   E -->|Not Prime| F(Process: Print Not Prime)
   E -->|Prime| G(Process: Print Prime)
   D --> H(Stop)
   F --> H
   G --> H
   ```

## Pseudocode

**Pseudocode** is a rough code representing how the algorithm of a program works. It does not require syntax and
provides a high-level understanding of the logic.

### Example 2 Pseudocode:

```text
Start
Input Salary
if Salary > 10000:
    Salary = Salary + 2000
else:
    Salary = Salary + 1000
Output Salary
Exit
```

### Example 3 Pseudocode:

```text
Start
Input num
if num ≤ 1:
    Print "Neither prime nor composite"
c = 2
while c < num:
    if num % c = 0:
        Print "Not Prime"
        Exit
    c = c + 1
end while
Print "Prime"
Exit.
```

## Optimization of Prime Solution

To optimize the prime solution, we can utilize the fact that we only need to check factors up to the square root of the
number being tested. This significantly reduces the number of iterations required.

### Optimized Pseudocode of Example 3:

```text
Start
Input num
if num ≤ 1:
    Print "Neither prime nor composite"
c = 2
while c * c <= num:
    if num % c = 0:
        Print "Not Prime"
        Exit
    c = c + 1
Print "Prime"
Exit.
```

This optimized approach minimizes the number of iterations needed to determine whether a number is prime.
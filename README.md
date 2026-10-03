
# COA_LAB-04
Computer Organization and Architecture Lab

# Computer Organization & Architecture Lab

## Lab 04 – Use of Venus Simulator for Register Level Execution of RISC-V Arithmetic and Memory Instructions

### Lab Description

The purpose of this lab was to use the Venus RISC-V simulator to execute and verify arithmetic, logical, and memory instructions at the register level. Different RISC-V assembly programs were implemented to understand register operations, bitwise logic, array processing, and memory access.

The tasks performed in this lab were:

1. Basic Arithmetic Operations
2. Arithmetic Operations Using Multiple Registers
3. Bitwise Logical Operations
4. Array Sum Using a Loop
5. Loading Array Elements from Memory

### Task 1 – Basic Arithmetic Operations

Basic arithmetic instructions were executed using two registers, `s0` and `s1`, initialized with the values 5 and 4, respectively. The `add`, `sub`, and `mul` instructions were used to perform addition, subtraction, and multiplication. An additional multiplication operation was performed to calculate the square of 5. The results were verified using the Venus simulator.

**Instructions used:** `li`, `add`, `sub`, `mul`

### Task 2 – Arithmetic Operations Using Multiple Registers

In this task, five registers were initialized with values from 5 to 1. Arithmetic instructions were combined to perform subtraction, addition, and multiplication. The intermediate results were stored in separate registers and then combined to calculate the final result. The program was executed in Venus to verify the register values.

**Instructions used:** `li`, `sub`, `add`, `mul`

### Task 3 – Bitwise Logical Operations

Bitwise logical operations were performed on two values, `0xFFF` and `0xF0F`, stored in registers `s0` and `s1`. The `and`, `or`, and `xor` instructions were used to perform bitwise AND, OR, and exclusive OR operations. The results were checked in the Venus simulator to understand how logical instructions operate on binary data.

**Instructions used:** `li`, `and`, `or`, `xor`

### Task 4 – Array Sum Using a Loop

A RISC-V assembly program was implemented to calculate the sum of all elements in an integer array. The program receives the base address of the array through register `a0` and its size through register `a1`. A loop accesses each element using the `lw` instruction, adds it to the running sum stored in `t0`, and increments the loop counter.

The `slli` instruction was used to calculate the byte offset of each integer, while `bge` and `j` controlled the loop execution. After processing all elements, the final sum was moved into register `a0` before returning from the function.

**Instructions used:** `li`, `bge`, `slli`, `add`, `lw`, `addi`, `j`, `mv`, `ret`

### Task 5 – Loading Array Elements from Memory

In this task, an array containing the even numbers from 2 to 20 was initialized in the data section using the `.data` directive and the `.word` declaration. The `la` instruction was used to load the base address of the array into register `t0`.

The `lw` instruction was then used to load each array element into registers `s0` through `s9`. Different memory offsets were used to access consecutive 32-bit integer values. The program was executed in Venus to verify that the correct values were loaded into the registers.

**Instructions used:** `.data`, `.word`, `la`, `lw`

### Software Used

- Venus RISC-V Simulator

### Topics Covered

- RISC-V Assembly Language
- Register-Level Execution
- Arithmetic Instructions
- Bitwise Logical Instructions
- Memory Access and Load Instructions
- Arrays and Loops
- Branching and Jump Instructions
- Function Calls and Return Instructions

### Conclusion

This lab provided practical experience with RISC-V assembly programming using the Venus simulator. The execution of arithmetic and logical instructions helped develop an understanding of register-level operations, while the array-processing tasks demonstrated memory addressing, data loading, loops, and branching. The results were verified through simulation.

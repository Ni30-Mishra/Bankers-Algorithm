# Bankers-Algorithm
# Bankers-Algorithm
Implemented Banker's Algorithm in C and C++ to find the safe states of processes.

## Overview

This repository contains implementations of the Banker's Algorithm in both C and C++. The Banker's Algorithm is a resource allocation and deadlock avoidance algorithm that tests for the safety of the state when allocating resources to multiple processes. It ensures that the system will not enter a deadlock by simulating the allocation of resources and determining whether it is possible for all processes to complete.

### Features

- **Deadlock Avoidance:** The algorithm checks whether the system is in a safe state by ensuring that all processes can complete without causing a deadlock.
- **User Input:** Accepts the number of processes, the number of resources, the allocation matrix, the maximum requirement matrix, and the available resources as input.
- **Safe Sequence:** If the system is in a safe state, the algorithm outputs a safe sequence of processes.

## C Implementation

The C implementation of the Banker's Algorithm is located in the `C_version` directory. It demonstrates basic memory management and control flow using standard C libraries.

### How to Run the C Program

1. Navigate to the `C_version` directory.
2. Compile the program using a C compiler, e.g., `gcc`:
   ```sh
   gcc banker.c -o banker
   ```
3. Run the executable:
   ```sh
   ./banker
   ```

## C++ Implementation

The C++ implementation of the Banker's Algorithm is located in the `CPP_version` directory. It leverages the C++ Standard Library for input/output operations and includes object-oriented enhancements for better readability.

### How to Run the C++ Program

1. Navigate to the `CPP_version` directory.
2. Compile the program using a C++ compiler, e.g., `g++`:
   ```sh
   g++ banker.cpp -o banker
   ```
3. Run the executable:
   ```sh
   ./banker
   ```

## Sample Input/Output

Both implementations require the following inputs:

- **Number of Processes (`np`)**
- **Number of Resources (`nr`)**
- **Initial Allocation Matrix**
- **Maximum Requirement Matrix**
- **Available Resources**

**Example Input:**

```
Enter the number of processes: 5
Enter the number of resources: 3
Enter the initial allocation matrix:
0 1 0
2 0 0
3 0 2
2 1 1
0 0 2
Enter the max requirement matrix:
7 5 3
3 2 2
9 0 2
2 2 2
4 3 3
Enter the available resources:
3 3 2
```

**Expected Output:**

```
****** Entered Data is ******

Initial allocation:
 P0      0 1 0
 P1      2 0 0
 P2      3 0 2
 P3      2 1 1
 P4      0 0 2

Maximum Requirement:
 P0      7 5 3
 P1      3 2 2
 P2      9 0 2
 P3      2 2 2
 P4      4 3 3

Available resources:
  3 3 2

Need is:
 P0      7 4 3
 P1      1 2 2
 P2      6 0 0
 P3      0 1 1
 P4      4 3 1

The system is in a safe state!
Safe sequence is ==>  P1 P3 P4 P0 P2
```

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please create a pull request or open an issue.

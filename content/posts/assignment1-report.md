---
title: "Assignment 1 Report"
date: 2026-04-24
draft: false
slug: "assignment-1-report"
---
# Remote Development Project Report

**Student Name**: OGUNLADE JOSHUA OLUWASEUN  
**Student ID**: LS2525237  

## Objective

1. Familiarize with Unix/Linux command line operations
2. Develop proficiency in Markdown for technical documentation
3. Implement matrix multiplication with an interpreted language (Python)

---

## Table of Contents
1. [System Configuration](#sys_config)
2. [Implementation Details](#imp_details)
3. [Algorithm Verification](#alg_verify)
4. [Conclusion](#conc)
5. [References](#ref)
6. [Appendix](#appendix)


### System Configuration {#sys_config}

| System Configuration          | Command Used                                      | Output                                                                                   |
|-------------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------|
| **CPU Model**                 | `sysctl -n machdep.cpu.brand_string`              | Apple M1                                                                                 |
| **Memory Size**               | `system_profiler SPHardwareDataType \| grep Memory` | 8 GB                                                                                   |
| **Operating System Version**  | `uname -a`                                        | Darwin Joshs-MacBook-Pro.local 24.5.0 Darwin Kernel Version 24.5.0 RELEASE_ARM64_T8103 |
| **Compiler Version**          | `gcc --version`                                   | Apple clang version 17.0.0                                                               |
| **Python Version**            | `python --version`                                | Python 3.13.1                                                                            |

---

## Implementation Details {#imp_details}

### Python Language Implementation

**Source Code**:

```python
# Define two 3x3 matrices
a = [[2, 5, 6], [9, 4, 5], [6, 3, 2]]
b = [[3, 8, 8], [2, 9, 7], [1, 1, 1]]

def matrix_mult(mat_1, mat_2):
    # Initialize result as a 3x3 matrix of zeros
    result = [[0 for j in range(3)] for k in range(3)]
    
    # Outer loop, iterates over rows of mat_1
    for i in range(len(mat_1)):
        # Middle loop, iterates over columns of mat_2
        for j in range(len(mat_2[i])):
            # Inner loop,  does the actual multiplication
            for k in range(len(mat_2)):
                # Multiply and accumulate into result[i][j]
                result[i][j] += mat_1[i][k] * mat_2[k][j]
    
    return result

print(matrix_mult(a, b))
```

**Execution Command**:

To run the Python script, navigate to the folder where the file is saved and run:

```bash
python matrix_mult.py
```

---

## Algorithm Verification {#alg_verify}

**Correctness**:

To verify the algorithm is correct, I manually calculated the first cell of the 
result matrix `result[0][0]` using row 0 of matrix A and column 0 of matrix B:

| Step | Calculation |
|------|-------------|
| Row 0 of A | `[2, 5, 6]` |
| Column 0 of B | `[3, 2, 1]` |
| Multiply & Sum | `(2×3) + (5×2) + (6×1) = 6 + 10 + 6 = 22` |

The algorithm returned `result[0][0] = 22` which matches the manual 
calculation, confirming the implementation is correct.

The full output of the program was:

[[22, 67, 57], [40, 113, 105], [26, 77, 71]]

## Conclusion {#conc}
This assignment has been a memory refresher for me both in writing Markdown and in 
coding Python. It helped me recall commands I had forgotten and think more carefully 
about how to structure technical documentation. Working with command-line tools to 
retrieve system information was also a good reminder of how much can be done 
directly from the terminal. Overall, it encouraged me to consider how documentation 
is written for an external audience.

---

## References {#ref}

[1] https://stackoverflow.com/questions/11948245/markdown-to-create-pages-and-table-of-contents

[2] https://markdownlivepreview.com/

---

## Appendix {#appendix}

- The system used for this project is a MacBook and not Linux, equivalent commands were used to answer the first question not the ones provided by the Professor. 

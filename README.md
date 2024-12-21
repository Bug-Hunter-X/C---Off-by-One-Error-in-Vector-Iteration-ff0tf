# C++ Off-by-One Error Example

This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The error occurs when the loop condition incorrectly includes the last element's index, which is one past the valid range. This leads to undefined behavior, typically a crash or unexpected results.

## Bug

The `bug.cpp` file contains the erroneous code.  The loop iterates from 0 up to and including `vec.size()`, attempting to access an element that doesn't exist.  

## Solution

The `bugSolution.cpp` file demonstrates the corrected code. The loop condition is changed to `i < vec.size()`, correctly iterating up to, but not including, the last element. 
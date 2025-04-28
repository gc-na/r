<!--
Meta Description: # Understanding `bitwOr` in R: Bitwise OR Operation ## Synopsis The `bitwOr` function in R performs a bitwise OR operation on integer values, allowing...
Meta Keywords: integer, bitwor, bitwise, binary, inputs
-->

# Understanding `bitwOr` in R: Bitwise OR Operation

## Synopsis
The `bitwOr` function in R performs a bitwise OR operation on integer values, allowing users to manipulate binary representations directly.

## Documentation
### Purpose
The `bitwOr` function is designed to compute the bitwise OR of two integer vectors. This operation compares each bit of the integers and returns a new integer where each bit is set to 1 if at least one of the corresponding bits in the operands is 1.

### Usage
```R
bitwOr(x, y)
```

### Arguments
- `x`: An integer vector.
- `y`: An integer vector of the same length as `x` or a single integer.

### Details
- The function is part of the base package in R, meaning it does not require any additional libraries to use.
- The integer inputs are treated in their binary form, and `bitwOr` operates element-wise if `x` and `y` are vectors of the same length.
- The result of `bitwOr` is an integer vector of the same length as the inputs.

## Examples
### Basic Usage
```R
# Example 1: Simple Bitwise OR
result1 <- bitwOr(5, 3)  # 5 in binary is 101, 3 is 011, result is 111 (7 in decimal)
print(result1)  # Output: 7

# Example 2: Element-wise Bitwise OR
x <- c(5, 2, 3)
y <- c(3, 7, 1)
result2 <- bitwOr(x, y)  # Computes bitwise OR for each pair
print(result2)  # Output: 7 7 3
```

## Explanation
When using `bitwOr`, it's important to understand that:
- The inputs are treated as binary numbers, and the operation is performed on each corresponding bit.
- If one of the inputs is negative, it is treated as a two's complement representation, which can lead to unexpected results if the user is not aware of how negative integers are represented in binary.
- The function does not handle non-integer inputs; if you pass non-integer values, R will throw an error.

## One Line Summary
The `bitwOr` function in R computes the bitwise OR of two integer vectors, yielding a new vector based on the binary representation of the inputs.
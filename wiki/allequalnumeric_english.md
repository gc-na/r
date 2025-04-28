<!--
Meta Description: # all.equal.numeric: Comparing Numeric Values in R ## Synopsis The `all.equal.numeric` function in R allows users to compare numeric vectors for near-...
Meta Keywords: numeric, equal, all, tolerance, function
-->

# all.equal.numeric: Comparing Numeric Values in R

## Synopsis
The `all.equal.numeric` function in R allows users to compare numeric vectors for near-equality, providing a flexible and robust way to check if two numbers are "equal enough" considering floating-point precision.

## Documentation
### Purpose
The `all.equal.numeric` method is specifically designed to compare two numeric vectors, returning `TRUE` if they are considered to be approximately equal, or providing a message detailing how they differ if they are not. It is particularly useful when dealing with numerical computations, where precision errors may lead to unexpected results.

### Usage
```R
all.equal(target, current, ...)
```

### Arguments
- `target`: A numeric vector or a single numeric value that you want to compare against.
- `current`: A numeric vector or a single numeric value to compare with the target.
- `...`: Additional arguments for further customization, though typically not needed for basic comparisons.

### Details
The function evaluates the equality of numeric values using a tolerance level to accommodate for minor discrepancies due to floating-point arithmetic. When comparing two numeric values, `all.equal.numeric` checks if the absolute difference between them is within a specified tolerance, which can be adjusted using the `tolerance` parameter. By default, this tolerance is set to a small value to ensure precision.

## Examples
```R
# Basic Comparison
x <- 0.1 + 0.2
y <- 0.3
result <- all.equal(x, y)
print(result)  # TRUE or a message indicating the difference

# Comparing two numeric vectors
vec1 <- c(1.000001, 2.000002, 3.000003)
vec2 <- c(1.000002, 2.000002, 3.000004)
result_vec <- all.equal(vec1, vec2)
print(result_vec)  # A message indicating the differences

# Using a custom tolerance
result_custom <- all.equal(vec1, vec2, tolerance = 1e-5)
print(result_custom)  # TRUE or a message based on custom tolerance
```

## Explanation
When using `all.equal.numeric`, it is important to remember that this function is not intended for strict equality checks. Users should be cautious when interpreting the output, as the function may return a message indicating the nature of the discrepancy. Common pitfalls include:
- Assuming that `all.equal` will always return `TRUE` for almost equal values without considering the specified tolerance.
- Not recognizing that the function provides informative messages for differences, which can be useful for debugging.

In scenarios where precise equality is required, users should utilize the `==` operator instead, while being aware of potential floating-point issues.

## One Line Summary
`all.equal.numeric` is a function in R that compares two numeric values or vectors for approximate equality, accounting for floating-point precision errors.
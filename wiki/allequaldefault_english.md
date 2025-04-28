<!--
Meta Description: # all.equal.default in R: A Comprehensive Guide ## Synopsis The `all.equal.default` function in R is used to test if two R objects are nearly equal, a...
Meta Keywords: equal, all, tolerance, objects, data
-->

# all.equal.default in R: A Comprehensive Guide

## Synopsis
The `all.equal.default` function in R is used to test if two R objects are nearly equal, allowing for a tolerance level that accommodates floating-point comparisons.

## Documentation

### Purpose
`all.equal.default` is specifically designed to compare two R objects for near equality. This function is particularly useful in scenarios where exact equality is not feasible due to floating-point arithmetic issues, such as when comparing numerical values that may differ slightly due to computational precision.

### Usage
```R
all.equal(target, current, tolerance = .Machine$double.eps^0.5, ...)
```

### Parameters
- `target`: The first object to compare.
- `current`: The second object to compare against the first.
- `tolerance`: A numeric value specifying the maximum allowable difference between the two objects. The default is set to the square root of the machine's double precision epsilon.
- `...`: Additional arguments to be passed to methods, if applicable.

### Details
The `all.equal` function returns `TRUE` if the objects are considered equal within the specified tolerance. If not, it returns a character string describing the difference. This function is particularly useful when working with numeric data, where minor discrepancies can arise from calculations.

## Examples

### Basic Usage Example
```R
# Exact equality
x <- 1.0000001
y <- 1.0000002
result <- all.equal(x, y)
print(result)  # Might return a message indicating they are not equal

# Comparing with a specified tolerance
result_with_tolerance <- all.equal(x, y, tolerance = 1e-7)
print(result_with_tolerance)  # Returns TRUE if within tolerance
```

### Comparison of Data Frames
```R
# Creating two data frames with minor differences
df1 <- data.frame(a = c(1.00001, 2.00001), b = c(3, 4))
df2 <- data.frame(a = c(1.00002, 2.00002), b = c(3, 4))

# Comparing data frames
result_df <- all.equal(df1, df2)
print(result_df)  # Will specify differences in the numeric columns if not equal
```

## Explanation
While `all.equal.default` is a powerful tool for comparing R objects, users should be aware of several common pitfalls:

- **Floating-Point Precision**: Due to the way computers handle floating-point numbers, exact comparisons may fail. Always consider using a tolerance level for numerical comparisons.
- **Data Types**: Ensure that the objects being compared are of compatible types. For example, comparing a numeric vector to a character vector will yield inequality.
- **Attributes**: The function may not always compare attributes like names or dimensions unless specified. Be mindful of what aspects of the objects you're interested in comparing.

## One Line Summary
`all.equal.default` is an R function that tests if two objects are nearly equal within a specified tolerance, making it ideal for robust numerical comparisons.
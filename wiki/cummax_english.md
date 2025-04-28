<!--
Meta Description: # cummax in R: Understanding the Cumulative Maximum Function ## Synopsis The `cummax` function in R efficiently calculates the cumulative maximum of a...
Meta Keywords: cummax, maximum, vector, cumulative, values
-->

# cummax in R: Understanding the Cumulative Maximum Function

## Synopsis
The `cummax` function in R efficiently calculates the cumulative maximum of a numeric vector, allowing users to track the highest values encountered as they traverse the data.

## Documentation
### Purpose
`cummax` is used to compute the cumulative maximum of elements in a vector or an array. This helps in scenarios where you need to evaluate and store the highest values sequentially as you process your data, such as in time series analysis or performance tracking.

### Usage
```R
cummax(x)
```

### Arguments
- `x`: A numeric vector or array from which the cumulative maximum will be calculated.

### Details
The `cummax` function returns a vector of the same length as `x`, where each element at position `i` is the maximum value of all elements from the start of `x` to position `i`. The function is vectorized, meaning it can handle operations on large datasets efficiently.

## Examples
Here are some basic usage examples to illustrate how `cummax` works:

### Example 1: Simple Numeric Vector
```R
# Define a numeric vector
numbers <- c(3, 5, 2, 8, 1)

# Calculate the cumulative maximum
result <- cummax(numbers)
print(result)
```
**Output:**
```
[1] 3 5 5 8 8
```

### Example 2: Cumulative Maximum with Negative Values
```R
# Define a vector with negative values
numbers <- c(-1, -3, -2, -5, -4)

# Calculate the cumulative maximum
result <- cummax(numbers)
print(result)
```
**Output:**
```
[1] -1 -1 -1 -1 -1
```

### Example 3: Time Series Data
```R
# Define a time series data vector
time_series <- c(10, 20, 15, 25, 30, 20)

# Calculate the cumulative maximum
cumulative_max <- cummax(time_series)
print(cumulative_max)
```
**Output:**
```
[1] 10 20 20 25 30 30
```

## Explanation
While using `cummax`, be aware of the following common pitfalls:
- **Data Types**: Ensure that the input vector is numeric. Using non-numeric types may lead to unexpected results or errors.
- **Handling NA Values**: The function does not automatically handle `NA` values. If `x` contains `NA`, the result will also include `NA` at the same positions. To ignore `NA` values, use the `na.rm` parameter in conjunction with other functions, as `cummax` itself does not have this option.

## One Line Summary
The `cummax` function in R computes the cumulative maximum of a numeric vector, providing a simple and efficient way to track maximum values sequentially.
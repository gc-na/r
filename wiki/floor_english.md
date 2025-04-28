<!--
Meta Description: # R `floor` Function: Rounding Down to the Nearest Integer ## Synopsis The `floor` function in R rounds numeric values down to the nearest integer, pr...
Meta Keywords: floor, values, function, integer, rounding
-->

# R `floor` Function: Rounding Down to the Nearest Integer

## Synopsis
The `floor` function in R rounds numeric values down to the nearest integer, providing a straightforward way to obtain the largest integer less than or equal to a given number.

## Documentation

### Purpose
The `floor` function is part of base R and is used to round numeric values downwards. This can be particularly useful in data analysis and statistical computations where integer values are required.

### Usage
```R
floor(x)
```

#### Arguments
- `x`: A numeric vector or object for which the floor value needs to be calculated.

### Details
The `floor` function will return the largest integer that is less than or equal to each element of the numeric input. It is vectorized, meaning it can accept a vector and will return a vector of the same length with each element rounded down.

## Examples

### Basic Usage
1. Rounding a single number:
   ```R
   floor(3.7)  # Returns 3
   ```

2. Rounding a vector of numbers:
   ```R
   floor(c(1.1, 2.9, 3.5, 4.0, -1.2))  
   # Returns c(1, 2, 3, 4, -2)
   ```

3. Rounding negative numbers:
   ```R
   floor(-2.3)  # Returns -3
   ```

4. Applying `floor` to a data frame column:
   ```R
   df <- data.frame(values = c(1.9, 2.5, 3.1))
   df$floored_values <- floor(df$values)
   print(df)
   #    values floored_values
   # 1     1.9              1
   # 2     2.5              2
   # 3     3.1              3
   ```

## Explanation
While using the `floor` function, keep the following points in mind:

- **Data Type**: The output of the `floor` function is a numeric vector. If you require integer type output specifically, you may need to convert it using `as.integer()`.
- **Handling NA Values**: If the input vector contains `NA` values, the output will also retain these `NA`s. The `floor` function does not ignore or drop `NA` values.
- **Performance**: The function is vectorized, making it efficient for large datasets.

### Common Pitfalls
- **Confusion with Other Rounding Functions**: Users may confuse `floor` with similar functions like `ceiling` (which rounds up) or `round` (which rounds to the nearest integer). Be sure to choose the appropriate function based on the desired rounding behavior.
- **Negative Values**: Remember that `floor` will always round towards negative infinity. For example, `floor(-1.1)` results in `-2`, which might be counterintuitive for some users.

## One Line Summary
The `floor` function in R efficiently rounds numeric values down to the nearest integer.
<!--
Meta Description: # pmax.int: The R Function for Element-wise Maximum of Integer Vectors ## Synopsis The `pmax.int` function in R computes the parallel maximum of integ...
Meta Keywords: vectors, integer, pmax, values, int
-->

# pmax.int: The R Function for Element-wise Maximum of Integer Vectors

## Synopsis
The `pmax.int` function in R computes the parallel maximum of integer vectors, returning a new integer vector that contains the maximum values at each position across the input vectors.

## Documentation

### Purpose
The `pmax.int` function is designed to facilitate the calculation of the element-wise maximum among multiple integer vectors. It is particularly useful when you need to compare values across multiple datasets or variables and obtain the highest values in a vectorized manner.

### Usage
```R
pmax.int(..., na.rm = FALSE)
```

### Arguments
- `...`: One or more integer vectors. The function accepts multiple arguments, and it will compute the element-wise maximum across these vectors.
- `na.rm`: A logical value indicating whether to remove `NA` values. If set to `TRUE`, any `NA` values in the input vectors will be ignored in the maximum computation.

### Details
- The `pmax.int` function is specifically optimized for integer vectors, making it more efficient than the generic `pmax` for this data type.
- If the input integer vectors have different lengths, they will be recycled to the length of the longest vector. This behavior follows R's recycling rules.
- The function returns an integer vector containing the maximum values at each corresponding position across the input vectors.

## Examples

### Basic Usage
```R
# Define integer vectors
vec1 <- c(1L, 3L, 5L)
vec2 <- c(2L, 1L, 4L)
vec3 <- c(NA, 6L, 2L)

# Compute element-wise maximum
result <- pmax.int(vec1, vec2, vec3, na.rm = TRUE)
print(result)  # Output: [1] 2 6 5
```

### With NA Values
```R
# Including NA values
vec4 <- c(NA, 4L, 7L)

# Compute element-wise maximum while ignoring NA values
result_na <- pmax.int(vec1, vec4, na.rm = TRUE)
print(result_na)  # Output: [1]  1  4  7
```

### Recycling of Vectors
```R
# Vectors of different lengths
vec5 <- c(3L, 5L)
vec6 <- c(1L)

# Recycled computation
result_recycle <- pmax.int(vec5, vec6)
print(result_recycle)  # Output: [1] 3 5
```

## Explanation
When using `pmax.int`, it's important to note that:
- The function is optimized for integer types. Using it with non-integer types may lead to unexpected behavior or slower performance.
- If you set `na.rm` to `FALSE`, any `NA` in the input vectors will result in an `NA` in the output at that position. Always consider whether you want to remove `NA` values based on your specific use case.
- Be cautious about input lengths; ensuring that your vectors are of the same length can prevent unintended results due to recycling.

## One Line Summary
`pmax.int` is an efficient R function that computes the element-wise maximum of multiple integer vectors, with options to handle `NA` values.
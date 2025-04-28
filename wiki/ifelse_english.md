<!--
Meta Description: # The R `ifelse()` Function: Conditional Element Selection Made Easy ## Synopsis The `ifelse()` function in R is a vectorized conditional function tha...
Meta Keywords: ifelse, data, function, test, pass
-->

# The R `ifelse()` Function: Conditional Element Selection Made Easy

## Synopsis
The `ifelse()` function in R is a vectorized conditional function that allows users to evaluate logical conditions and return values based on whether those conditions are true or false. This function is particularly useful for data manipulation and transformation in data frames and vectors.

## Documentation
### Purpose
The `ifelse()` function serves to efficiently apply conditional logic to each element of a vector or data frame column, making it a cornerstone for data analysis and preprocessing in R.

### Usage
```R
ifelse(test, yes, no)
```

### Arguments
- **test**: A logical condition or expression to evaluate. This can be a vector of logical values.
- **yes**: The value(s) to return for each element of `test` that is `TRUE`.
- **no**: The value(s) to return for each element of `test` that is `FALSE`.

### Details
The `ifelse()` function is particularly beneficial because it can handle vectors directly, returning a vector of results that correspond to the evaluation of the `test` condition. It is essential to note that the lengths of `yes` and `no` must be compatible with the length of `test`, or they will be recycled.

## Examples
### Example 1: Basic Conditional Replacement
```R
# Create a numeric vector
numbers <- c(1, 2, 3, 4, 5)

# Use ifelse to categorize numbers
categories <- ifelse(numbers %% 2 == 0, "Even", "Odd")
print(categories)  # Output: "Odd" "Even" "Odd" "Even" "Odd"
```

### Example 2: Conditional Transformation in Data Frames
```R
# Create a data frame
df <- data.frame(id = 1:5, score = c(85, 60, 75, 90, 50))

# Use ifelse to create a new column based on scores
df$result <- ifelse(df$score >= 75, "Pass", "Fail")
print(df)
# Output:
#   id score result
# 1  1    85   Pass
# 2  2    60   Fail
# 3  3    75   Pass
# 4  4    90   Pass
# 5  5    50   Fail
```

### Example 3: Working with NA Values
```R
# Handle NA values
scores <- c(85, NA, 75, NA, 50)

# Replace NA with a default value
results <- ifelse(is.na(scores), "Missing", ifelse(scores >= 75, "Pass", "Fail"))
print(results)  # Output: "Pass" "Missing" "Pass" "Missing" "Fail"
```

## Explanation
While `ifelse()` is powerful and convenient, there are a few common pitfalls to be aware of:
- **Vector Recycling**: If the lengths of `yes` and `no` do not match the length of `test`, R will recycle them, potentially leading to unexpected results.
- **Type Consistency**: Ensure that the values returned in `yes` and `no` are of the same type to avoid coercion issues.
- **Performance**: For large datasets, `ifelse()` can be less efficient compared to other vectorized functions or `dplyr`'s `mutate()` with `case_when()`, especially when dealing with complex conditions.

## One Line Summary
The `ifelse()` function in R provides a simple way to apply conditional logic to vectors and data frames, returning specified values based on logical evaluations.
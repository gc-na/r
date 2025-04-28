<!--
Meta Description: # pmatch: Exact and Partial Matching in R ## Synopsis The `pmatch` function in R is used for partial matching of character strings, allowing users to ...
Meta Keywords: pmatch, matches, vector, match, partial
-->

# pmatch: Exact and Partial Matching in R

## Synopsis
The `pmatch` function in R is used for partial matching of character strings, allowing users to identify the best matches from a vector based on partial input.

## Documentation
### Purpose
`pmatch` is designed to facilitate the matching of character strings in R. It is particularly useful when dealing with user input that may not precisely match the elements in a given vector. The function returns the positions of the matches or `NA` if no matches are found.

### Usage
```R
pmatch(x, table, nomatch = NA_integer_, duplicates.ok = FALSE)
```

#### Arguments
- `x`: A character vector containing the input values to be matched.
- `table`: A character vector of values against which `x` is matched.
- `nomatch`: The value to return for unmatched items. Defaults to `NA_integer_`.
- `duplicates.ok`: A logical value indicating whether duplicate matches are allowed. Defaults to `FALSE`.

### Details
The `pmatch` function performs a case-sensitive match and returns the indices of the best matches found in the `table`. If there are multiple entries that partially match an entry in `x`, the first match is returned unless `duplicates.ok` is set to `TRUE`, in which case all matches will be returned.

## Examples
### Basic Usage Example
```R
# Define a vector of fruits
fruits <- c("apple", "banana", "orange", "grape")

# Use pmatch to find matches
result <- pmatch(c("ap", "gr"), fruits)
print(result)
```
**Output:**
```
[1]  1  4
```

### Handling Unmatched Input
```R
# Attempting to match a non-existent fruit
result <- pmatch(c("pear", "ba"), fruits)
print(result)
```
**Output:**
```
[1] NA  2
```

## Explanation
When using `pmatch`, it's essential to be aware of the following common pitfalls:
- **Case Sensitivity**: `pmatch` is case-sensitive, meaning "Apple" and "apple" would not match. 
- **Partial Matches**: If `x` elements are too generic (like "a"), you may get unexpected matches or multiple results, which may not be useful.
- **Duplicates Handling**: If you are working with a vector that has duplicate entries and you set `duplicates.ok = FALSE`, only the first occurrence will be matched, potentially leading to confusion.

## One Line Summary
`pmatch` in R is a function used for partial matching of character strings, returning the indices of the closest matches from a specified vector.
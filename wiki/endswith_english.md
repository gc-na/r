<!--
Meta Description: # Understanding the `endsWith` Function in R: A Comprehensive Guide ## Synopsis The `endsWith` function in R is used to determine if a character strin...
Meta Keywords: suffix, endswith, function, string, vector
-->

# Understanding the `endsWith` Function in R: A Comprehensive Guide

## Synopsis
The `endsWith` function in R is used to determine if a character string ends with a specified suffix. This function is part of the string manipulation capabilities in R, making it useful for data cleaning, validation, and substring operations.

## Documentation

### Purpose
The `endsWith` function checks whether the provided strings end with a specific substring, returning a logical vector indicating the result for each element.

### Usage
```R
endsWith(x, suffix)
```

### Arguments
- **x**: A character vector or a single character string to be checked.
- **suffix**: A single character string that specifies the suffix to look for.

### Details
The function performs a case-sensitive comparison, meaning that the case of letters matters when checking for the specified suffix. The output is a logical vector of the same length as `x`, where each element is `TRUE` if the corresponding element in `x` ends with `suffix`, and `FALSE` otherwise.

## Examples

### Basic Usage
```R
# Example 1: Basic usage with a single string
string1 <- "HelloWorld"
endsWith(string1, "World")  # Returns TRUE

# Example 2: Working with a character vector
strings_vector <- c("data.csv", "report.pdf", "summary.docx")
endsWith(strings_vector, ".pdf")  # Returns FALSE TRUE FALSE

# Example 3: Case sensitivity
endsWith("example.TXT", ".txt")  # Returns FALSE
```

### Using with Data Frames
```R
# Example 4: Checking suffixes in a data frame
df <- data.frame(file_names = c("image1.png", "document.pdf", "presentation.PPTX"))
df$ends_with_pdf <- endsWith(df$file_names, ".pdf")  # Adds a logical column
```

## Explanation
While using the `endsWith` function, it is essential to remember the following common pitfalls:

- **Case Sensitivity**: The function is case-sensitive. If you need a case-insensitive check, consider converting both the strings and the suffix to the same case (e.g., using `tolower()` or `toupper()`).
- **Empty Strings**: If `x` is an empty string, the function will return `FALSE` regardless of the suffix provided.
- **Vector Recycling**: If `suffix` is a vector longer than one element, R will recycle the suffix values for each element in `x`. This can lead to unexpected results if you aren't aware of this behavior.

## One Line Summary
The `endsWith` function in R is a straightforward tool for checking if a character string or vector ends with a specified suffix, supporting string manipulation and validation tasks.
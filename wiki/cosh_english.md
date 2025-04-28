<!--
Meta Description: # R `cosh`: Compute the Hyperbolic Cosine of Numeric Values ## Synopsis The `cosh` function in R computes the hyperbolic cosine of numeric values, pro...
Meta Keywords: hyperbolic, cosh, cosine, numeric, function
-->

# R `cosh`: Compute the Hyperbolic Cosine of Numeric Values

## Synopsis
The `cosh` function in R computes the hyperbolic cosine of numeric values, providing a mathematical tool for various applications in fields such as engineering, physics, and mathematics.

## Documentation
### Purpose
The `cosh` function calculates the hyperbolic cosine of a given numeric input. The hyperbolic cosine of a number \( x \) is defined mathematically as:

\[
\cosh(x) = \frac{e^x + e^{-x}}{2}
\]

This function is particularly useful in scenarios involving hyperbolic geometry and in solving differential equations.

### Usage
```R
cosh(x)
```

### Arguments
- **x**: A numeric vector, matrix, or array containing the values for which the hyperbolic cosine is to be computed.

### Details
- The `cosh` function is vectorized, meaning it can handle inputs of multiple values at once, returning a vector, matrix, or array of the same dimensions as the input.
- It is part of the base R package, so no additional libraries are needed to use this function.

## Examples
### Basic Usage
```R
# Compute the hyperbolic cosine of a single numeric value
result_single <- cosh(0)  # Returns 1

# Compute the hyperbolic cosine of a vector of numeric values
result_vector <- cosh(c(-1, 0, 1))  # Returns c(1.54308063481524, 1, 1.54308063481524)

# Compute the hyperbolic cosine of a sequence of numbers
result_sequence <- cosh(seq(-2, 2, by = 0.5)) 
# Returns a vector of hyperbolic cosines for the sequence: c(3.76219569108363, 1.35078322768962, 1.0, 1.35078322768962, 3.76219569108363)
```

## Explanation
- **Common Pitfalls**: 
  - Ensure that the input to the `cosh` function is numeric. Non-numeric inputs will result in an error.
  - Be cautious when interpreting the results, especially for large absolute values of \( x \), as the outputs can become very large due to the exponential growth of \( e^x \).
  
- **Gotchas**:
  - The `cosh` function returns values that are always greater than or equal to 1 for real number inputs. This characteristic can be useful when analyzing the behavior of functions involving hyperbolic cosines.
  
- **Additional Notes**:
  - The output of `cosh` is always real-valued, as the hyperbolic cosine is defined for all real numbers.
  - For complex numbers, R will still compute the hyperbolic cosine, but the results will involve complex arithmetic.

## One Line Summary
The `cosh` function in R efficiently calculates the hyperbolic cosine of numeric inputs, making it a valuable tool for mathematical computations.
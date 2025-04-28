<!--
Meta Description: # besselI: Bessel Functions of the First Kind in R ## Synopsis The `besselI` function in R computes the modified Bessel function of the first kind, an...
Meta Keywords: function, bessel, besseli, scaled, first
-->

# besselI: Bessel Functions of the First Kind in R

## Synopsis
The `besselI` function in R computes the modified Bessel function of the first kind, an important mathematical function frequently used in various fields such as physics, engineering, and statistics.

## Documentation

### Purpose
The `besselI` function calculates the modified Bessel function of the first kind, denoted as \( I_v(x) \), for a given order \( v \) and argument \( x \). It is particularly useful in solving differential equations and modeling processes that involve cylindrical symmetry.

### Usage
```R
besselI(x, nu, expon.scaled = FALSE)
```

### Parameters
- `x`: A numeric vector representing the points at which to evaluate the Bessel function.
- `nu`: A numeric value or vector specifying the order(s) of the Bessel function. It can be a non-negative integer or a real number.
- `expon.scaled`: A logical value indicating whether to return the exponentially scaled version of the function. Default is `FALSE`.

### Details
The modified Bessel function of the first kind is defined by the series expansion:
\[
I_v(x) = \sum_{k=0}^{\infty} \frac{(x/2)^{v+2k}}{k! \Gamma(v+k+1)}
\]
where \( \Gamma \) is the gamma function. The function is especially valuable when dealing with problems involving cylindrical coordinates, such as heat conduction in cylindrical objects.

## Examples

### Basic Usage
```R
# Calculate Bessel function of the first kind of order 0 at x = 1
besselI(1, nu = 0)

# Calculate Bessel function of the first kind of order 1 at x = 2
besselI(2, nu = 1)

# Calculate Bessel function for multiple values of nu
besselI(1, nu = c(0, 1, 2))
```

### Exponentially Scaled
```R
# Calculate exponentially scaled Bessel function of the first kind
besselI(1, nu = 0, expon.scaled = TRUE)
```

## Explanation
While using `besselI`, users should be aware that:
- The function can handle both scalar and vector inputs for `x` and `nu`, but the lengths must be compatible for vectorized calculations.
- The order of the Bessel function, `nu`, can be non-integer, but this may lead to complex values for certain inputs.
- When `expon.scaled` is set to `TRUE`, the output represents the Bessel function scaled by an exponential factor, which can be helpful for numerical stability in certain applications.

Common pitfalls include:
- Forgetting to check the compatibility of vector lengths, which can lead to unexpected results or errors.
- Misunderstanding the implications of the `expon.scaled` parameter, which alters the interpretation of the output.

## One Line Summary
The `besselI` function in R computes the modified Bessel function of the first kind, providing essential calculations for various scientific and engineering applications.
<!--
Meta Description: # Kappa in R: Understanding Cohen's Kappa for Inter-Rater Reliability ## Synopsis Cohen's Kappa is a statistical measure used in R to assess the level...
Meta Keywords: kappa, agreement, table, data, cohen
-->

# Kappa in R: Understanding Cohen's Kappa for Inter-Rater Reliability

## Synopsis
Cohen's Kappa is a statistical measure used in R to assess the level of agreement between two raters or classification systems. It accounts for the agreement occurring by chance, providing a more accurate measure of inter-rater reliability than simple percentage agreement.

## Documentation
### Purpose
The `kappa` function in R is primarily used to compute Cohen's Kappa coefficient, which evaluates the degree of agreement between two categorical variables. This is particularly useful in fields such as psychology, medicine, and any domain that involves assessment by multiple observers.

### Usage
The basic syntax for the `kappa` function is as follows:
```R
kappa(table)
```
- **table**: A contingency table (or matrix) that displays the frequency of agreements and disagreements between the two raters.

### Details
Cohen's Kappa values range from -1 to 1, where:
- 1 indicates perfect agreement,
- 0 indicates no agreement beyond chance, and
- negative values indicate less agreement than expected by chance.

The Kappa statistic is calculated using the formula:
\[ \kappa = \frac{p_o - p_e}{1 - p_e} \]
Where:
- \( p_o \) is the observed agreement,
- \( p_e \) is the expected agreement by chance.

In R, you can calculate Kappa using the `irr` package, which provides a convenient implementation.

## Examples
### Example 1: Basic Kappa Calculation
```R
# Load necessary library
install.packages("irr")
library(irr)

# Create a contingency table
ratings <- matrix(c(10, 2, 1, 7), nrow = 2)

# Calculate Kappa
kappa_result <- kappa(ratings)
print(kappa_result)
```

### Example 2: Kappa with Data Frame
```R
# Create a data frame with rater ratings
data <- data.frame(
  rater1 = c("yes", "yes", "no", "yes", "no"),
  rater2 = c("yes", "no", "no", "yes", "yes")
)

# Create a contingency table
table_data <- table(data$rater1, data$rater2)

# Calculate Kappa
kappa_result <- kappa(table_data)
print(kappa_result)
```

## Explanation
When using Cohen's Kappa, it's crucial to ensure that the data is structured correctly as a contingency table. One common pitfall is misinterpreting Kappa values; for instance, a Kappa of 0.6 may seem satisfactory, but it may indicate moderate agreement depending on the context. Additionally, Kappa can be sensitive to the prevalence of categories; rare categories can significantly affect the Kappa statistic.

It's also important to note that Kappa assumes that the ratings are independent and that the categories are mutually exclusive. If these assumptions are violated, the Kappa statistic may not be an appropriate measure of agreement.

## One Line Summary
Cohen's Kappa in R is a statistical measure that quantifies inter-rater agreement while accounting for chance, providing a reliable metric for categorical assessments.
<!--
Meta Description: # R 語言中的 is.infinite 函數：檢查無限值 ## 摘要 `is.infinite` 是 R 語言中的一個內建函數，用於檢查數值是否為無限值。這個函數對於數據分析和數學計算中特別重要，因為無限值可能會影響計算結果。 ## 文件說明 ### 目的 `is.infinite` 函數用來測試...
Meta Keywords: infinite, inf, false, true, result
-->

# R 語言中的 is.infinite 函數：檢查無限值

## 摘要
`is.infinite` 是 R 語言中的一個內建函數，用於檢查數值是否為無限值。這個函數對於數據分析和數學計算中特別重要，因為無限值可能會影響計算結果。

## 文件說明
### 目的
`is.infinite` 函數用來測試一個數值向量中的每個元素是否為正無窮大 (`Inf`) 或負無窮大 (`-Inf`)。

### 使用方法
```R
is.infinite(x)
```

### 參數
- `x`: 一個數值向量，可以是單一數字或多個數字的集合。

### 返回值
此函數返回一個邏輯向量，長度與 `x` 相同。對於每個元素，如果該元素是無窮大，則返回 `TRUE`，否則返回 `FALSE`。

## 範例
以下是使用 `is.infinite` 函數的基本示例：

```R
# 示例 1：檢查單一值
x <- Inf
is.infinite(x)  # 返回 TRUE

# 示例 2：檢查多個值
y <- c(-Inf, 0, 1, 2, Inf, NA)
is.infinite(y)  # 返回 TRUE, FALSE, FALSE, FALSE, TRUE, FALSE

# 示例 3：與其他函數結合使用
z <- c(1, 2, Inf, 3)
result <- z[is.infinite(z)]  # 提取無窮大的值
print(result)  # 返回 Inf
```

## 解釋
使用 `is.infinite` 時，有幾個常見的注意事項：
- 當檢查的向量中包含 `NA` 值時，`is.infinite` 會將 `NA` 對應為 `FALSE`。因此，若要檢查無窮值，需注意向量中的缺失值。
- 此函數只能用於數值型資料，對於字符型或其他類型的資料會報錯。
- 使用 `is.finite` 函數可作為補充，檢查非無窮的有限值。

## 一句總結
`is.infinite` 函數用於檢查 R 中數值是否為無窮大或負無窮大，並返回相應的邏輯值。
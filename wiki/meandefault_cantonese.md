<!--
Meta Description: # mean.default 在 R 語言中的應用 ## 簡介 `mean.default` 是 R 語言中的一個基礎函數，用來計算一組數據的算術平均值。它是 R 語言中計算數據中心趨勢的重要工具。 ## 文檔 ### 目的 `mean.default` 主要用於計算數值向量的均值。它可以處理缺失值...
Meta Keywords: mean, default, trim, false, 預設為
-->

# mean.default 在 R 語言中的應用

## 簡介
`mean.default` 是 R 語言中的一個基礎函數，用來計算一組數據的算術平均值。它是 R 語言中計算數據中心趨勢的重要工具。

## 文檔
### 目的
`mean.default` 主要用於計算數值向量的均值。它可以處理缺失值，並提供靈活的選項來調整計算方式。

### 用法
```R
mean(x, trim = 0, na.rm = FALSE, ...)
```

### 參數
- `x`: 數值向量或數組，需計算均值的數據。
- `trim`: 介於 0 和 0.5 之間的數字，用於修剪數據的比例，預設為 0（不修剪）。
- `na.rm`: 布林值，指示是否在計算均值時排除缺失值。預設為 `FALSE`。
- `...`: 其他額外參數，通常不使用。

## 範例
以下是 `mean.default` 的基本使用示例：

```R
# 計算簡單數值向量的均值
data <- c(1, 2, 3, 4, 5)
result <- mean(data)
print(result)  # 輸出: 3

# 計算包含缺失值的均值
data_with_na <- c(1, 2, NA, 4, 5)
result_na_rm <- mean(data_with_na, na.rm = TRUE)
print(result_na_rm)  # 輸出: 3
```

## 說明
- 一個常見的陷阱是忘記設置 `na.rm` 參數，這會導致結果為 `NA`，如果數據中存在缺失值。
- 當使用 `trim` 參數時，它能有效減少極端值對均值的影響，但必須謹慎選擇修剪比例。
- 此函數僅適用於數值類型的數據，對於字符型或因子型數據應先進行轉換。

## 一行總結
`mean.default` 是 R 語言中計算數值向量均值的基本函數，支持缺失值處理和數據修剪。
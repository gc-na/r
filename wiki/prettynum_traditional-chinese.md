<!--
Meta Description: # R 語言中的 prettyNum 函數：數字格式化的最佳選擇 ## 摘要 `prettyNum` 是 R 語言中用來格式化數字的函數，能夠將數字轉換為更易讀的格式，尤其適用於顯示長數字、貨幣或百分比等情況。 ## 文檔 ### 目的 `prettyNum` 函數的主要目的是改善數字的顯示方式，使...
Meta Keywords: prettynum, mark, numbers, big, decimal
-->

# R 語言中的 prettyNum 函數：數字格式化的最佳選擇

## 摘要
`prettyNum` 是 R 語言中用來格式化數字的函數，能夠將數字轉換為更易讀的格式，尤其適用於顯示長數字、貨幣或百分比等情況。

## 文檔
### 目的
`prettyNum` 函數的主要目的是改善數字的顯示方式，使其更具可讀性。此函數可以自動調整小數點位數、添加千分位分隔符號，並能夠根據用戶的需求格式化數字。

### 用法
```R
prettyNum(x, big.mark = ",", scientific = FALSE, decimal.mark = ".", ...)
```

### 參數
- `x`: 要格式化的數字或數字向量。
- `big.mark`: 指定千分位分隔符，預設為 `","`。
- `scientific`: 邏輯值，是否使用科學記數法。預設為 `FALSE`。
- `decimal.mark`: 指定小數點符號，預設為 `"."`。
- `...`: 其他可選參數，供進一步擴展。

## 範例
以下是 `prettyNum` 的基本使用範例：

```R
# 基本數字格式化
numbers <- c(1234567.89, 9876543.21)
formatted_numbers <- prettyNum(numbers)
print(formatted_numbers)

# 自定義千分位分隔符
formatted_numbers_custom <- prettyNum(numbers, big.mark = " ")
print(formatted_numbers_custom)

# 使用科學記數法
formatted_scientific <- prettyNum(numbers, scientific = TRUE)
print(formatted_scientific)

# 自定義小數點符號
formatted_decimal <- prettyNum(numbers, decimal.mark = ",")
print(formatted_decimal)
```

## 解釋
在使用 `prettyNum` 時，常見的陷阱包括：
- 忘記設置 `big.mark` 和 `decimal.mark` 參數，可能會導致格式不符合預期。
- 對於非常大的數字，可能需要考慮使用科學記數法，以便於閱讀。
- `prettyNum` 不會改變原始數據的類型，返回的仍然是字符型數據，如果需要進行數值計算，需再次轉換。

## 一句總結
`prettyNum` 是 R 語言中一個強大的數字格式化工具，能夠輕鬆提高數字的可讀性。
<!--
Meta Description: # R 語言中的格式化函數 (format) ## 摘要 `format` 函數是 R 語言中的一個核心功能，用於將數值或日期轉換為特定的字符格式，以便於顯示和輸出。它允許用戶自定義數字的顯示方式，包括小數點位數、填充方式等。 ## 文件說明 ### 目的 `format` 函數的主要目的是將數值、...
Meta Keywords: format, mark, nsmall, scientific, big
-->

# R 語言中的格式化函數 (format)

## 摘要
`format` 函數是 R 語言中的一個核心功能，用於將數值或日期轉換為特定的字符格式，以便於顯示和輸出。它允許用戶自定義數字的顯示方式，包括小數點位數、填充方式等。

## 文件說明
### 目的
`format` 函數的主要目的是將數值、日期或時間格式化為可讀性更高的字符型式，這在報告生成和數據可視化中格外重要。

### 使用方法
```R
format(x, ..., digits = NULL, nsmall = 0, scientific = FALSE, big.mark = "", decimal.mark = ".")
```

### 參數說明
- `x`: 要格式化的數值或日期。
- `...`: 其他可選參數，根據需求使用。
- `digits`: 數字的總位數。
- `nsmall`: 最小小數位數。
- `scientific`: 是否以科學記數法顯示，預設為 `FALSE`。
- `big.mark`: 用於千位分隔符的字元。
- `decimal.mark`: 小數點符號，預設為 `.`。

## 示例
### 基本用法
```R
# 格式化數值
num <- 12345.6789
formatted_num <- format(num, nsmall = 2, big.mark = ",")
print(formatted_num)  # 輸出 "12,345.68"

# 格式化日期
date <- as.Date("2023-10-01")
formatted_date <- format(date, "%Y/%m/%d")
print(formatted_date)  # 輸出 "2023/10/01"
```

## 解釋
使用 `format` 函數時，常見的陷阱包括：
- 忘記設置 `nsmall` 參數，可能導致顯示的數字小數位數不足。
- 在處理日期時，使用不正確的格式符號會導致輸出錯誤。
- 當 `scientific` 設置為 `TRUE` 時，數字會以科學記數法顯示，這可能不符合用戶的期望。

## 總結
`format` 函數是 R 語言中一個強大的工具，能夠有效地格式化數字和日期，以提高數據的可讀性和展示效果。
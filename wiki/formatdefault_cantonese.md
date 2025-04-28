<!--
Meta Description: # format.default: R 語言中的格式化基本函數 ## 簡介 `format.default` 是 R 語言中的一個基本函數，用於格式化數據，使其更可讀性。它主要處理數字和字符數據，並能根據用戶的需求自定義格式。 ## 文檔 ### 目的 `format.default` 函數的主要目...
Meta Keywords: format, default, nsmall, width, justify
-->

# format.default: R 語言中的格式化基本函數

## 簡介
`format.default` 是 R 語言中的一個基本函數，用於格式化數據，使其更可讀性。它主要處理數字和字符數據，並能根據用戶的需求自定義格式。

## 文檔
### 目的
`format.default` 函數的主要目的是將數據轉換為字符串格式，以便於展示和輸出。這在數據報告和可視化中非常重要，因為它能夠提高數據的可讀性和理解性。

### 用法
```R
format(x, ...)
```

### 詳細說明
- **x**: 需要格式化的對象，可以是數字、字符或其他數據類型。
- **...**: 其他可選參數，具體取決於需要的格式化需求，比如指定小數位數、填充字符等。

### 主要參數
- `nsmall`: 指定最小小數位數。
- `width`: 指定輸出字符串的寬度。
- `justify`: 指定對齊方式（例如 "left", "right", "centre"）。
- `scientific`: 是否使用科學記數法表示數字。

## 範例
基本用法示例如下：

```R
# 格式化數字
num <- 1234.56789
formatted_num <- format(num, nsmall = 2)
print(formatted_num)  # "1234.57"

# 格式化字符
char <- "Hello, World!"
formatted_char <- format(char, width = 20, justify = "centre")
print(formatted_char)  # "      Hello, World!   "
```

## 解釋
使用 `format.default` 時，常見的誤區包括：
- 忘記指定 `nsmall` 參數，可能導致小數位數不符合預期。
- 使用不正確的對齊方式，可能影響最終輸出的格式效果。
- 在處理大型數據時，過度使用格式化可能影響性能。

## 一句總結
`format.default` 是一個用於格式化數據以提高可讀性的 R 函數，適合數字和字符的自定義展示。
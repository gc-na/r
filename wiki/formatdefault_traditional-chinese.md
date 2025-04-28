<!--
Meta Description: # format.default 在 R 中的用法與範例 ## 簡介 `format.default` 是 R 語言中用於格式化數據的基本函數，它可以幫助用戶將數據轉換為更可讀的字符串表示。這個函數適用於多種數據類型，並且在數據輸出時特別有用。 ## 文檔 ### 目的 `format.defaul...
Meta Keywords: format, default, nsmall, big, mark
-->

# format.default 在 R 中的用法與範例

## 簡介
`format.default` 是 R 語言中用於格式化數據的基本函數，它可以幫助用戶將數據轉換為更可讀的字符串表示。這個函數適用於多種數據類型，並且在數據輸出時特別有用。

## 文檔
### 目的
`format.default` 函數的主要目的是將數據以指定格式轉換為字符串，使其更易於閱讀和理解。這對於打印、顯示和報告數據非常重要。

### 用法
```R
format.default(x, ...)
```

#### 參數
- `x`: 需要格式化的數據，可以是數字、字符、日期等。
- `...`: 其他可選參數，用於指定格式化的詳細選項，如 `nsmall`、`big.mark`、`scientific` 等。

### 詳細說明
`format.default` 函數會根據提供的數據類型自動選擇合適的格式化方式。該函數支持多種格式選項，例如：
- `nsmall`: 控制數字的小數位數。
- `big.mark`: 用於分隔千位的標記。
- `scientific`: 控制是否以科學計數法顯示數字。

使用 `format.default` 時，您可以靈活地調整輸出格式，以滿足不同的需求。

## 範例
```R
# 基本數字格式化
x <- c(12345.67891, 98765.4321)
formatted_x <- format.default(x, nsmall = 2)
print(formatted_x)

# 使用千位分隔符
formatted_x_with_comma <- format.default(x, big.mark = ",")
print(formatted_x_with_comma)

# 日期格式化
date <- as.Date("2023-10-01")
formatted_date <- format.default(date)
print(formatted_date)
```

## 解釋
使用 `format.default` 時，有幾個常見的陷阱和注意事項：
- 當數據中包含 NA 值時，`format.default` 將返回 "NA" 字符串，而不是保留 NA。
- 如果未指定 `nsmall`，則小數位數可能會根據數據自動調整，這可能導致不一致的格式。
- 使用 `big.mark` 時，請注意不同地區的千位分隔符可能不同（例如，某些地區使用句點而不是逗號）。

## 一句總結
`format.default` 是一個強大的 R 函數，用於將數據格式化為易於閱讀的字符串表示，適用於多種數據類型和格式選項。
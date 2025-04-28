<!--
Meta Description: # R 語言中的 `duplicated.default` 函數：檢查重複值的利器 ## 簡介 `duplicated.default` 函數是 R 語言中用來檢查數據中重複值的重要工具。該函數可以幫助用戶快速識別向量或數據框中的重複元素，從而有效地處理數據清理任務。 ## 文檔 ### 目的 `d...
Meta Keywords: duplicated, false, default, true, incomparables
-->

# R 語言中的 `duplicated.default` 函數：檢查重複值的利器

## 簡介
`duplicated.default` 函數是 R 語言中用來檢查數據中重複值的重要工具。該函數可以幫助用戶快速識別向量或數據框中的重複元素，從而有效地處理數據清理任務。

## 文檔
### 目的
`duplicated.default` 函數的主要目的是識別數據中重複的項目。它返回一個邏輯向量，指示每個元素是否在它之前已經出現過。

### 使用方法
```R
duplicated(x, incomparables = FALSE, ...)
```

### 參數
- `x`：要檢查重複的對象，可以是向量、數據框或列表。
- `incomparables`：一個可選的參數，指定哪些值應該被視為不可比較的。
- `...`：其他傳遞給方法的參數。

### 返回值
該函數返回一個邏輯向量，標記每個元素是否是重複的。第一個出現的元素將標記為 `FALSE`，隨後的重複項將標記為 `TRUE`。

## 範例
以下是 `duplicated.default` 函數的基本使用範例：

```R
# 範例 1：檢查向量中的重複值
vec <- c(1, 2, 2, 3, 4, 4, 4)
duplicated(vec)
# 返回: FALSE FALSE TRUE FALSE FALSE TRUE TRUE

# 範例 2：檢查數據框中的重複行
df <- data.frame(a = c(1, 2, 2, 3), b = c("x", "y", "y", "z"))
duplicated(df)
# 返回: FALSE FALSE TRUE FALSE
```

## 說明
使用 `duplicated.default` 時，常見的問題包括：
- 確保輸入對象的類型正確。如果輸入不是向量或數據框，可能會引發錯誤。
- 注意 `incomparables` 參數的使用，這可能會影響重複檢查的結果。
- 該函數僅檢查元素的首次出現，不會顯示所有重複項的索引。如果需要獲得所有重複項，可以結合使用 `which()` 函數。

## 一句總結
`duplicated.default` 是 R 語言中檢查數據重複值的有效函數，能夠幫助用戶快速識別和處理重複數據。
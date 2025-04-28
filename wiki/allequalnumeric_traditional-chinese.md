<!--
Meta Description: # all.equal.numeric：R 語言中數值比較的利器 ## 概述 `all.equal.numeric` 是 R 語言中用於比較兩個數值的函數，常用於檢查數值向量之間的相等性，特別是在數值計算或模擬中，確保結果的準確性至關重要。 ## 文檔 ### 目的 `all.equal.numer...
Meta Keywords: equal, all, numeric, result, tolerance
-->

# all.equal.numeric：R 語言中數值比較的利器

## 概述
`all.equal.numeric` 是 R 語言中用於比較兩個數值的函數，常用於檢查數值向量之間的相等性，特別是在數值計算或模擬中，確保結果的準確性至關重要。

## 文檔
### 目的
`all.equal.numeric` 函數的主要目的是比較兩個數值是否相等，並考慮到浮點運算的精度問題。此函數會返回一個邏輯值，或者在不相等時提供一個描述性的字符串，幫助用戶理解差異。

### 使用方法
```R
all.equal(actual, expected, tolerance = .Machine$double.eps^0.5, ...)
```
- **actual**：要比較的實際數值。
- **expected**：期望的數值。
- **tolerance**：允許的誤差範圍，預設為 `sqrt(.Machine$double.eps)`，此值可根據需求調整。
- **...**：其他可能的參數。

### 詳細說明
- `all.equal.numeric` 會檢查兩個數值是否在指定的容忍範圍內相等。
- 如果兩者相等，則返回 `TRUE`；如果不相等，則返回一個字符串，描述它們之間的差異。
- 此函數非常適合於單元測試或數據驗證的情境中，因為浮點數的比較往往因精度問題而變得複雜。

## 示例
以下是 `all.equal.numeric` 的基本用法範例：

```R
# 基本用法
x <- 0.1 + 0.2
y <- 0.3
result <- all.equal(x, y)
print(result)  # 輸出：TRUE

# 當允許的誤差範圍改變時
x <- 1.000001
y <- 1.000002
result <- all.equal(x, y, tolerance = 1e-5)
print(result)  # 輸出：TRUE

# 不相等的情況
x <- 1
y <- 2
result <- all.equal(x, y)
print(result)  # 輸出： "1 not equal to 2"
```

## 說明
- **常見陷阱**：使用 `all.equal` 時，需注意浮點數的精度問題。在某些情況下，即使兩個數字看似相等，實際上可能因為精度限制導致不相等，因此需要適當設定 `tolerance`。
- **額外註解**：此函數主要用於數值比較，而對於其他類型的對象（如數據框或列表），應使用相應的比較函數。

## 一句總結
`all.equal.numeric` 是 R 中用於精確比較數值的有效工具，特別適合於處理浮點數的相等性檢查。
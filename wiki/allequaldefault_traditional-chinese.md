<!--
Meta Description: # all.equal.default：R 語言中用於比較物件相等性的函數 ## 摘要 `all.equal.default` 是 R 語言中用於比較 R 物件相等性的函數，特別用於檢查兩個物件是否在數值或結構上相等，並容許一定的誤差範圍。 ## 文件說明 ### 目的 `all.equal.def...
Meta Keywords: all, equal, default, true, print
-->

# all.equal.default：R 語言中用於比較物件相等性的函數

## 摘要
`all.equal.default` 是 R 語言中用於比較 R 物件相等性的函數，特別用於檢查兩個物件是否在數值或結構上相等，並容許一定的誤差範圍。

## 文件說明
### 目的
`all.equal.default` 函數的主要目的是比較兩個 R 物件，並判斷它們是否相等。這個函數特別適用於浮點數比較，因為浮點數的表示有時會導致微小的誤差。使用此函數可以避免因為計算誤差而導致的錯誤判斷。

### 用法
```R
all.equal(target, current, ...)
```

### 參數
- `target`：要比較的目標物件。
- `current`：要比較的當前物件。
- `...`：額外的參數，可以用於控制比較的行為。

### 詳細說明
此函數會返回一個邏輯值或描述性文字，用於指示兩個物件是否相等。如果相等，則返回 `TRUE`；如果不相等，則返回一個描述不相等原因的字串。這在進行單元測試或數據檢查時非常有用。

## 範例
### 基本用法範例
```R
# 比較兩個數值
result1 <- all.equal(0.1 + 0.2, 0.3)
print(result1)  # TRUE

# 比較兩個向量
vec1 <- c(1, 2, 3)
vec2 <- c(1, 2, 3)
result2 <- all.equal(vec1, vec2)
print(result2)  # TRUE

# 比較兩個數組（容許誤差）
array1 <- array(c(1.000001, 2.000001), dim = c(1, 2))
array2 <- array(c(1, 2), dim = c(1, 2))
result3 <- all.equal(array1, array2, tolerance = 1e-5)
print(result3)  # TRUE
```

## 解釋
在使用 `all.equal.default` 時，有幾個常見的注意事項：
1. **浮點數的精度問題**：由於浮點數的表示方式，可能會出現微小的差異，這時可以使用 `tolerance` 參數來指定可接受的誤差範圍。
2. **結構比較**：對於複雜結構（如數據框或列表），`all.equal` 將會檢查結構和內容的相等性，這可能會導致誤解。
3. **返回值的解讀**：如果兩個物件不相等，函數會返回一個描述性文字，而不是簡單的 `FALSE`，這有助於調試和理解不相等的原因。

## 一句總結
`all.equal.default` 是 R 中用於比較兩個物件相等性的強大工具，特別適合處理浮點數的相等性檢查。
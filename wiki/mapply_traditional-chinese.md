<!--
Meta Description: # mapply 函數在 R 語言中的應用 ## 簡介 `mapply` 是 R 語言中的一個高效函數，用於對多個向量或列表同時進行函數應用。它是 `sapply` 函數的多重版本，能夠處理多個參數，使得批量數據處理變得更加簡便和靈活。 ## 文件說明 ### 目的 `mapply` 函數的主要目的...
Meta Keywords: mapply, result, fun, moreargs, simplify
-->

# mapply 函數在 R 語言中的應用

## 簡介
`mapply` 是 R 語言中的一個高效函數，用於對多個向量或列表同時進行函數應用。它是 `sapply` 函數的多重版本，能夠處理多個參數，使得批量數據處理變得更加簡便和靈活。

## 文件說明
### 目的
`mapply` 函數的主要目的在於將一個函數應用於多個數據集合，並生成一個統一的輸出。這在需要對多個變量進行相同計算時特別有用，能夠提升代碼的可讀性和執行效率。

### 用法
```R
mapply(FUN, MoreArgs = NULL, SIMPLIFY = TRUE, USE.NAMES = TRUE, ...)
```

### 參數
- `FUN`: 要應用的函數。
- `MoreArgs`: 可選，傳遞給 `FUN` 的其他參數。
- `SIMPLIFY`: 可選，邏輯值，指示是否將結果簡化為向量或矩陣。
- `USE.NAMES`: 可選，邏輯值，指示是否為結果命名。
- `...`: 其他傳遞給函數的參數。

## 範例
以下是 `mapply` 函數的基本用法範例：

### 範例 1: 基本用法
```R
# 定義一個簡單的加法函數
add <- function(x, y) {
  return(x + y)
}

# 使用 mapply 對兩個向量進行加法運算
result <- mapply(add, 1:5, 6:10)
print(result)  # 輸出: 7 9 11 13 15
```

### 範例 2: 使用 MoreArgs
```R
# 定義一個乘法函數，並添加一個額外的參數
multiply <- function(x, y, z) {
  return((x * y) + z)
}

# 使用 mapply，並傳遞額外的參數 z
result <- mapply(multiply, 1:3, 4:6, z = 10)
print(result)  # 輸出: 14 22 32
```

## 解釋
使用 `mapply` 時需要注意以下幾點：
- 當多個輸入向量長度不一致時，`mapply` 會自動重複較短的向量以匹配長度，這可能會導致意外結果。
- 若要避免因數據類型不匹配而產生的錯誤，應確保輸入數據的類型相容。
- 使用 `SIMPLIFY` 參數可以控制結果的格式，通常設置為 `TRUE` 時會返回簡化的數據結構。

## 一句總結
`mapply` 是一個強大的 R 函數，使得對多個向量或列表同時應用函數變得簡單且高效。
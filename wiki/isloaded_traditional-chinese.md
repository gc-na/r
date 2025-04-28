<!--
Meta Description: # R 語言中的 is.loaded 函數：檢查 R 函數是否已加載 ## 簡介 `is.loaded` 是 R 語言中的一個函數，用於檢查一個特定的共享對象（如 C 或 Fortran 函數）是否已經被加載到 R 的內存中。它對於開發 R 擴展包或使用外部庫的用戶特別有用。 ## 文檔 ### 目...
Meta Keywords: loaded, mycfunc, print, mymethod, fortran
-->

# R 語言中的 is.loaded 函數：檢查 R 函數是否已加載

## 簡介
`is.loaded` 是 R 語言中的一個函數，用於檢查一個特定的共享對象（如 C 或 Fortran 函數）是否已經被加載到 R 的內存中。它對於開發 R 擴展包或使用外部庫的用戶特別有用。

## 文檔
### 目的
`is.loaded` 函數的主要目的是判斷某個特定的共享對象（通常為底層語言編寫的函數）是否可用於當前的 R 環境。

### 用法
```R
is.loaded(name)
```

### 參數
- `name`：一個字符向量，指定要檢查的共享對象的名稱。

### 返回值
此函數返回一個布林值：
- `TRUE`：如果指定的共享對象已經加載。
- `FALSE`：如果指定的共享對象尚未加載。

## 範例
### 基本用法
以下是 `is.loaded` 函數的幾個基本使用範例：

```R
# 檢查內置的 C 函數 "mycfunc" 是否已加載
if (is.loaded("mycfunc")) {
  print("mycfunc 已加載")
} else {
  print("mycfunc 尚未加載")
}
```

### 檢查 R 包中的函數
```R
# 假設有一個 R 包 "mypackage"，檢查其中的函數 "mymethod"
if (is.loaded("mypackage::mymethod")) {
  print("mymethod 已加載")
} else {
  print("mymethod 尚未加載")
}
```

## 解釋
在使用 `is.loaded` 時，有幾個常見的陷阱和注意事項：

1. **名稱格式**：確保提供正確的共享對象名稱。通常，這些名稱是 C 或 Fortran 函數的名稱，而不包括包的名稱或其他前綴。

2. **加載順序**：如果在檢查之前沒有調用 `dyn.load()` 來加載共享對象，`is.loaded` 會返回 `FALSE`。因此，檢查加載狀態前，確保已正確加載相關對象。

3. **跨平台差異**：某些共享對象可能在不同的操作系統上有所不同，需特別留意在不同環境中的兼容性。

## 總結
`is.loaded` 是一個用於檢查共享對象是否已加載到 R 環境中的有用函數，適合於 R 擴展開發者和需要使用底層語言功能的用戶。
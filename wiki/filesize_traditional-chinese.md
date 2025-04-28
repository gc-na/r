<!--
Meta Description: # R 語言中的 file.size 函數：檔案大小的查詢工具 ## Synopsis `file.size` 是 R 語言中的一個內建函數，用於返回指定檔案的大小（以位元組為單位）。這個函數對於處理檔案的大小檢查和管理非常有用。 ## Documentation ### 目的 `file.size...
Meta Keywords: file, size, 以位元組為單位, csv, mtcars
-->

# R 語言中的 file.size 函數：檔案大小的查詢工具

## Synopsis
`file.size` 是 R 語言中的一個內建函數，用於返回指定檔案的大小（以位元組為單位）。這個函數對於處理檔案的大小檢查和管理非常有用。

## Documentation
### 目的
`file.size` 函數的主要功能是獲取特定檔案的大小，這在數據分析和檔案管理中有著重要的應用。

### 使用方法
```R
file.size(file)
```
- **參數**：
  - `file`：一個字串，表示檔案的路徑。必須是存在的檔案，否則函數將返回 `NA`。

### 詳細說明
當調用 `file.size` 函數時，它會檢查指定的檔案並返回其大小。如果該檔案不存在，則會返回 `NA`。這個函數的返回值是以位元組為單位，對於進行檔案大小的比較或限制設定非常有幫助。

## Examples
以下是 `file.size` 的基本使用示例：

```R
# 創建一個測試檔案
write.csv(mtcars, "mtcars.csv")

# 獲取檔案大小
size <- file.size("mtcars.csv")
print(size)  # 輸出檔案大小（以位元組為單位）
```

```R
# 檢查不存在的檔案
non_existent_file_size <- file.size("non_existent_file.txt")
print(non_existent_file_size)  # 輸出 NA
```

## Explanation
使用 `file.size` 時常見的陷阱包括：
- 若指定的檔案路徑錯誤或檔案不存在，函數將返回 `NA`，用戶需確認檔案的正確性。
- 返回的大小是以位元組為單位，使用者需根據需求進行單位換算（例如：將位元組轉換為 KB 或 MB）。
- 該函數無法獲取目錄或資料夾的大小，只能用於單個檔案。

## One Line Summary
`file.size` 函數用於返回指定檔案的大小，以位元組為單位，是 R 語言中檔案管理的重要工具。
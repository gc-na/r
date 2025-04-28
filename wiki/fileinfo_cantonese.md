<!--
Meta Description: # R語言中的 file.info 函數詳解 ## 簡介 `file.info` 是 R 語言中的一個函數，用於獲取有關檔案的元數據，包括檔案大小、修改時間、存取權限等。這個函數對於檔案管理和資料處理非常實用。 ## 文件說明 ### 目的 `file.info` 函數的主要目的是提供檔案的詳細資訊...
Meta Keywords: info, file, files, print, example
-->

# R語言中的 file.info 函數詳解

## 簡介
`file.info` 是 R 語言中的一個函數，用於獲取有關檔案的元數據，包括檔案大小、修改時間、存取權限等。這個函數對於檔案管理和資料處理非常實用。

## 文件說明
### 目的
`file.info` 函數的主要目的是提供檔案的詳細資訊，幫助用戶了解檔案的狀態和屬性，特別是在處理大量檔案或進行資料清理時。

### 用法
```R
file.info(files)
```
- **參數**：
  - `files`: 一個字串向量，包含要查詢的檔案路徑。

### 詳細說明
`file.info` 函數返回一個資料框，其中每一行代表一個檔案，每一列則包含該檔案的不同屬性，如下所示：
- `size`: 檔案大小（以字節為單位）
- `mtime`: 最後修改時間
- `ctime`: 檔案狀態改變時間
- `atime`: 最後存取時間
- `isdir`: 是否為目錄（布林值）
- `mode`: 檔案存取模式

## 範例
以下是一些基本的使用範例：

### 範例 1: 獲取單個檔案資訊
```R
info <- file.info("example.txt")
print(info)
```

### 範例 2: 獲取多個檔案資訊
```R
files <- c("example.txt", "data.csv", "script.R")
info <- file.info(files)
print(info)
```

### 範例 3: 檢查目錄的資訊
```R
dir_info <- file.info("my_directory")
print(dir_info)
```

## 解釋
在使用 `file.info` 時，有幾個常見的陷阱和注意事項：
- 確保檔案路徑正確，否則會返回 NA。
- 如果檔案不存在，`file.info` 會顯示該檔案的所有元數據為 NA。
- 使用相對路徑時，請確認當前工作目錄正確，以避免找不到檔案。

## 一句總結
`file.info` 是 R 中一個強大的函數，用於獲取檔案的元數據，幫助用戶進行檔案管理和資料處理。
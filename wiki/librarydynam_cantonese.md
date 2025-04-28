<!--
Meta Description: # library.dynam: R 語言中動態載入共享庫的指令 ## 概述 `library.dynam` 係 R 語言中用於動態載入共享庫嘅一個指令，特別適合用於需要即時加載 C、C++ 或 Fortran 寫嘅擴展功能。 ## 文檔 ### 目的 `library.dynam` 主要用於將已經...
Meta Keywords: library, dynam, mylib, lib, loc
-->

# library.dynam: R 語言中動態載入共享庫的指令

## 概述
`library.dynam` 係 R 語言中用於動態載入共享庫嘅一個指令，特別適合用於需要即時加載 C、C++ 或 Fortran 寫嘅擴展功能。

## 文檔

### 目的
`library.dynam` 主要用於將已經編譯好的共享庫（通常係 .so 或 .dll 文件）載入到 R 環境中，這樣用戶就可以直接使用共享庫提供的函數。

### 用法
```R
library.dynam(package, lib.loc = NULL, verbose = getOption("verbose"), ...)
```

### 參數
- `package`: 要載入的共享庫名稱，通常係一個字符串。
- `lib.loc`: 一個可選參數，指明庫的路徑。如果未提供，R 會使用預設的庫路徑。
- `verbose`: 一個邏輯值，決定是否顯示詳細信息。
- `...`: 其他參數，根據具體情況而定。

### 詳細信息
`library.dynam` 通常用於擴展包中，當包需要調用外部編譯代碼時，會使用此函數來加載相應的共享庫。使用此指令時，確保共享庫已經正確編譯並且可用於指定的路徑。

## 示例

### 基本用法
以下示例說明如何使用 `library.dynam` 載入一個名為 "mylib" 的共享庫：
```R
# 載入名為 mylib 的共享庫
library.dynam("mylib")
```

### 指定路徑
如果共享庫存放在特定路徑，可以這樣指定：
```R
# 指定庫路徑
library.dynam("mylib", lib.loc = "/path/to/library")
```

## 解釋
使用 `library.dynam` 時，常見的陷阱包括：
- 確保共享庫已經正確編譯並可用。
- 檢查庫路徑是否正確，避免因路徑錯誤而導致的載入失敗。
- 注意庫的相依性，確保所需的其他庫也已經載入。

## 一句總結
`library.dynam` 係 R 中一個用於動態載入共享庫的指令，方便用戶調用外部編譯代碼。
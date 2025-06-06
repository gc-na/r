<!--
Meta Description: # R语言中的最小值函数（min） ## 概述 `min` 是 R 编程语言中的一个基本函数，用于计算一组数值中的最小值。它是数据分析和统计计算中常用的工具。 ## 文档 ### 目的 `min` 函数用于返回输入向量中的最小值，可以处理数值、日期和其他可比较的对象。 ### 使用方法 ```R m...
Meta Keywords: min, 数值向量, 最小值, print, false
-->

# R语言中的最小值函数（min）

## 概述
`min` 是 R 编程语言中的一个基本函数，用于计算一组数值中的最小值。它是数据分析和统计计算中常用的工具。

## 文档
### 目的
`min` 函数用于返回输入向量中的最小值，可以处理数值、日期和其他可比较的对象。

### 使用方法
```R
min(..., na.rm = FALSE)
```

#### 参数
- `...`：一个或多个向量、数据框或其他可比较的对象。
- `na.rm`：逻辑值，指示是否在计算最小值时忽略 `NA`（缺失值）。默认为 `FALSE`。

### 详细信息
`min` 函数将返回输入值的最小值。如果输入的所有值均为 `NA`，且 `na.rm` 为 `FALSE`，则返回 `NA`。如果 `na.rm` 为 `TRUE`，则会忽略所有 `NA` 值并计算其余值的最小值。

## 示例
以下是 `min` 函数的一些基本用法示例：

### 示例 1：计算简单向量的最小值
```R
数值向量 <- c(5, 3, 8, 1, 4)
最小值 <- min(数值向量)
print(最小值)  # 输出: 1
```

### 示例 2：处理缺失值
```R
数值向量 <- c(2, NA, 5, 3)
最小值_with_na <- min(数值向量)  # 返回 NA
最小值_ignore_na <- min(数值向量, na.rm = TRUE)  # 返回 2
print(最小值_with_na)  # 输出: NA
print(最小值_ignore_na)  # 输出: 2
```

### 示例 3：多个向量的最小值
```R
向量1 <- c(10, 20, 30)
向量2 <- c(5, 15, 25)
最小值 <- min(向量1, 向量2)
print(最小值)  # 输出: 5
```

## 说明
使用 `min` 函数时，需注意以下几点：
- 确保输入数据是数值型或其他可比较类型。
- 若输入包含 `NA` 值，需根据需要设置 `na.rm` 参数。
- `min` 函数不仅适用于向量，也支持列表和数据框中的列，但返回结果可能需要进一步处理。

## 一句话总结
`min` 函数在 R 中用于计算给定数值集合的最小值，支持处理缺失值选项。
<!--
Meta Description: # Lọc Dữ Liệu Trong R: Cách Sử Dụng Hàm Filter ## Tóm tắt Hàm `filter` trong R thuộc gói `dplyr`, cho phép người dùng lọc các hàng trong một khung dữ ...
Meta Keywords: điều, kiện, liệu, các, filter
-->

# Lọc Dữ Liệu Trong R: Cách Sử Dụng Hàm Filter

## Tóm tắt
Hàm `filter` trong R thuộc gói `dplyr`, cho phép người dùng lọc các hàng trong một khung dữ liệu dựa trên các điều kiện nhất định. Đây là một công cụ mạnh mẽ để làm sạch và phân tích dữ liệu.

## Tài liệu
### Mục đích
Hàm `filter` được sử dụng để chọn lọc các hàng trong một khung dữ liệu theo điều kiện cụ thể. Nó giúp người dùng dễ dàng truy xuất và phân tích các tập con của dữ liệu mà họ quan tâm.

### Cách sử dụng
Cú pháp cơ bản của hàm `filter` như sau:

```R
filter(data, condition1, condition2, ...)
```

- **data**: Khung dữ liệu (data frame) hoặc bảng (tibble) mà bạn muốn lọc.
- **condition**: Điều kiện lọc, có thể có một hoặc nhiều điều kiện.

### Chi tiết
- Hàm `filter` chỉ giữ lại những hàng mà thỏa mãn các điều kiện đã chỉ định.
- Các điều kiện có thể sử dụng các toán tử như `==`, `!=`, `<`, `>`, `<=`, `>=`, cũng như kết hợp các điều kiện bằng `&` (và) và `|` (hoặc).

## Ví dụ
### Ví dụ cơ bản
```R
library(dplyr)

# Tạo một khung dữ liệu mẫu
data <- data.frame(
  id = 1:5,
  score = c(85, 90, 78, 92, 88)
)

# Lọc những hàng có điểm số lớn hơn 85
filtered_data <- filter(data, score > 85)
print(filtered_data)
```

### Ví dụ với nhiều điều kiện
```R
# Lọc những hàng có điểm số lớn hơn 85 và id nhỏ hơn 5
filtered_data_multiple_conditions <- filter(data, score > 85 & id < 5)
print(filtered_data_multiple_conditions)
```

## Giải thích
### Những cạm bẫy thường gặp
- Đảm bảo rằng các biến được sử dụng trong điều kiện đã được xác định trong khung dữ liệu.
- Khi sử dụng nhiều điều kiện, hãy chắc chắn rằng bạn sử dụng đúng toán tử `&` cho "và" và `|` cho "hoặc".
- Nếu không có hàng nào thỏa mãn điều kiện, hàm sẽ trả về một khung dữ liệu rỗng.

## Tóm tắt một dòng
Hàm `filter` trong R cho phép bạn lọc các hàng trong khung dữ liệu dựa trên các điều kiện nhất định một cách nhanh chóng và hiệu quả.
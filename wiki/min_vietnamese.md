<!--
Meta Description: # Hàm min trong R: Cách sử dụng và ví dụ ## Tóm tắt Hàm `min` trong R được sử dụng để tìm giá trị nhỏ nhất trong một tập hợp các số liệu. Đây là một c...
Meta Keywords: giá, trị, hàm, trong, min
-->

# Hàm min trong R: Cách sử dụng và ví dụ

## Tóm tắt
Hàm `min` trong R được sử dụng để tìm giá trị nhỏ nhất trong một tập hợp các số liệu. Đây là một chức năng cơ bản và hữu ích trong phân tích dữ liệu.

## Tài liệu
### Mục đích
Hàm `min` giúp người dùng dễ dàng xác định giá trị nhỏ nhất trong một vector hoặc nhiều vector. Nó thường được sử dụng trong các phân tích thống kê và khi làm việc với dữ liệu lớn.

### Cách sử dụng
Cú pháp chung của hàm `min` như sau:

```R
min(..., na.rm = FALSE)
```

#### Tham số
- `...`: Một hoặc nhiều vector số. Hàm sẽ tìm giá trị nhỏ nhất trong tất cả các vector được cung cấp.
- `na.rm`: (Tùy chọn) Một giá trị logic. Nếu được đặt là `TRUE`, hàm sẽ loại bỏ các giá trị NA (Not Available) trước khi tìm giá trị nhỏ nhất. Mặc định là `FALSE`.

### Chi tiết
Hàm `min` là một phần của ngôn ngữ R nên không cần phải tải thư viện bổ sung. Hàm có thể xử lý nhiều kiểu dữ liệu khác nhau, bao gồm số nguyên, số thực, và các vector. Khi có nhiều vector được đưa vào, hàm sẽ tìm giá trị nhỏ nhất trong tất cả các vector. Nếu tất cả các giá trị đều là NA và `na.rm` không được đặt là `TRUE`, hàm sẽ trả về NA.

## Ví dụ
Dưới đây là một số ví dụ cơ bản về cách sử dụng hàm `min`:

```R
# Ví dụ 1: Tìm giá trị nhỏ nhất trong một vector
vec1 <- c(5, 2, 9, 1, 4)
result1 <- min(vec1)
print(result1)  # Kết quả: 1

# Ví dụ 2: Tìm giá trị nhỏ nhất trong nhiều vector
vec2 <- c(10, 15, 7)
vec3 <- c(8, 12, 20)
result2 <- min(vec2, vec3)
print(result2)  # Kết quả: 7

# Ví dụ 3: Loại bỏ giá trị NA
vec4 <- c(3, NA, 6, 1, NA)
result3 <- min(vec4, na.rm = TRUE)
print(result3)  # Kết quả: 1
```

## Giải thích
Một số điểm cần lưu ý khi sử dụng hàm `min`:
- Nếu tất cả giá trị trong vector là NA và `na.rm` không được đặt là `TRUE`, hàm sẽ trả về NA. Để tránh điều này, hãy chắc chắn rằng bạn đã xử lý các giá trị NA nếu cần thiết.
- Hàm `min` có thể làm việc với các vector có chiều dài khác nhau nhưng sẽ chỉ trả về giá trị nhỏ nhất từ các giá trị đã cho.
- Việc sử dụng `na.rm = TRUE` là rất quan trọng trong các tập dữ liệu thực tế, nơi thường xuất hiện các giá trị thiếu.

## Tóm tắt một dòng
Hàm `min` trong R là một công cụ đơn giản nhưng mạnh mẽ để tìm giá trị nhỏ nhất trong một hoặc nhiều vector, giúp phân tích dữ liệu dễ dàng hơn.
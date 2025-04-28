<!--
Meta Description: # Hàm log trong R: Tính toán logarithm một cách dễ dàng ## Tóm tắt Hàm `log` trong R được sử dụng để tính toán giá trị logarithm tự nhiên (logarit cơ ...
Meta Keywords: tính, logarit, log, một, vector
-->

# Hàm log trong R: Tính toán logarithm một cách dễ dàng

## Tóm tắt
Hàm `log` trong R được sử dụng để tính toán giá trị logarithm tự nhiên (logarit cơ số e) hoặc logarithm với cơ số tùy chọn. Đây là một công cụ hữu ích trong phân tích dữ liệu và các phép toán toán học.

## Tài liệu
### Mục đích
Hàm `log` cho phép người dùng thực hiện các phép tính logarithm trên các số hoặc vector. Nó có thể được sử dụng để tính toán logarit tự nhiên hoặc logarit với cơ số tùy chọn, phục vụ cho nhiều ứng dụng trong thống kê và phân tích dữ liệu.

### Cú pháp
```R
log(x, base = exp(1))
```
- **x**: Một số hoặc vector đầu vào mà bạn muốn tính logarithm.
- **base**: (Tùy chọn) Cơ số của logarithm. Mặc định là `exp(1)` (logarit tự nhiên).

### Chi tiết
Hàm `log` có thể nhận đầu vào là số thực hoặc vector và sẽ trả về một giá trị hoặc vector tương ứng. Khi sử dụng cơ số khác ngoài cơ số tự nhiên, bạn có thể chỉ định bằng cách thay đổi tham số `base`.

## Ví dụ
### Ví dụ 1: Tính logarit tự nhiên
```R
# Tính logarit tự nhiên của 10
log_10 <- log(10)
print(log_10)  # Kết quả sẽ là khoảng 2.302585
```

### Ví dụ 2: Tính logarit với cơ số 10
```R
# Tính logarit cơ số 10 của 100
log_100_base10 <- log(100, base = 10)
print(log_100_base10)  # Kết quả sẽ là 2
```

### Ví dụ 3: Tính logarit cho một vector
```R
# Tính logarit tự nhiên cho một vector
vector <- c(1, 2, 3, 4, 5)
log_vector <- log(vector)
print(log_vector)  # Kết quả sẽ là một vector chứa các giá trị logarit
```

## Giải thích
Một số điều cần lưu ý khi sử dụng hàm `log`:
- Nếu bạn cố gắng tính logarithm của một giá trị âm hoặc bằng 0, hàm sẽ trả về `NaN` (Not a Number). 
- Đảm bảo rằng bạn đã nhập đúng cơ số nếu bạn sử dụng cơ số khác ngoài cơ số tự nhiên, để tránh nhầm lẫn trong kết quả.
- Các giá trị logarithm có thể không phải là số nguyên, vì vậy hãy chuẩn bị cho tình huống này trong phân tích của bạn.

## Tóm tắt một dòng
Hàm `log` trong R cho phép tính toán giá trị logarithm tự nhiên hoặc với cơ số tùy chọn cho các số và vector.
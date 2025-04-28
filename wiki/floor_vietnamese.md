<!--
Meta Description: # Hàm `floor` trong R: Làm tròn số xuống ## Tóm tắt Hàm `floor` trong R được sử dụng để làm tròn các số thực xuống tới số nguyên gần nhất nhỏ hơn hoặc...
Meta Keywords: floor, hàm, trong, các, làm
-->

# Hàm `floor` trong R: Làm tròn số xuống

## Tóm tắt
Hàm `floor` trong R được sử dụng để làm tròn các số thực xuống tới số nguyên gần nhất nhỏ hơn hoặc bằng số đó. Đây là một công cụ hữu ích trong các phép toán số học, phân tích dữ liệu và xử lý số liệu trong R.

## Tài liệu
### Mục đích
Hàm `floor` giúp người dùng làm tròn các số thực xuống, đảm bảo rằng giá trị trả về luôn là số nguyên. Điều này có thể rất cần thiết trong các tình huống yêu cầu kết quả là số nguyên, chẳng hạn như khi tính toán số lượng hoặc khi phân loại dữ liệu.

### Cú pháp
```R
floor(x)
```

### Tham số
- `x`: Một vector số thực (numeric vector) mà bạn muốn làm tròn xuống.

### Chi tiết
Hàm `floor` sẽ trả về một vector mới có cùng độ dài với `x`, trong đó mỗi phần tử là kết quả của việc làm tròn xuống của phần tử tương ứng trong `x`. Nếu `x` chứa các giá trị không phải số (NA), hàm sẽ trả về NA cho các giá trị đó.

## Ví dụ
```R
# Ví dụ 1: Làm tròn số thực
x <- c(2.3, 3.7, 4.0, -1.2, -3.8)
result <- floor(x)
print(result)
# Kết quả: 2, 3, 4, -2, -4

# Ví dụ 2: Sử dụng với vector
y <- c(5.9, 6.1, 7.8, 8.5)
result_y <- floor(y)
print(result_y)
# Kết quả: 5, 6, 7, 8
```

## Giải thích
Khi sử dụng hàm `floor`, người dùng cần lưu ý rằng:
- Kết quả của `floor` luôn là số nguyên và có thể khác với giá trị gốc nếu số thực đó không phải là số nguyên.
- Nếu vector đầu vào chứa giá trị NA, hàm sẽ trả về NA cho các vị trí đó.
- Hàm `floor` có thể là một phần trong chuỗi các phép toán khi xử lý số liệu và phân tích, vì vậy việc hiểu rõ cách sử dụng là rất quan trọng.

## Tóm tắt một câu
Hàm `floor` trong R cho phép người dùng làm tròn các số thực xuống tới số nguyên gần nhất nhỏ hơn hoặc bằng số đó.
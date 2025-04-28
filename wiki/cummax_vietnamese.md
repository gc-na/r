<!--
Meta Description: # cummax trong R: Tính Giá Trị Tối Đa Tích Lũy ## Tóm tắt Hàm `cummax` trong R được sử dụng để tính giá trị tối đa tích lũy của một vector hoặc mảng. ...
Meta Keywords: giá, trị, vector, cummax, một
-->

# cummax trong R: Tính Giá Trị Tối Đa Tích Lũy

## Tóm tắt
Hàm `cummax` trong R được sử dụng để tính giá trị tối đa tích lũy của một vector hoặc mảng. Nó giúp người dùng dễ dàng theo dõi giá trị lớn nhất tính đến từng phần tử trong chuỗi dữ liệu.

## Tài liệu
### Mục đích
Hàm `cummax` giúp người dùng xác định giá trị lớn nhất trong một chuỗi dữ liệu cho đến mỗi phần tử, bằng cách trả về một vector mới có cùng chiều dài với vector đầu vào.

### Cách sử dụng
Cú pháp cơ bản của hàm `cummax` như sau:

```R
cummax(x)
```

- **x**: Một vector số hoặc mảng mà bạn muốn tính giá trị tối đa tích lũy.

### Chi tiết
- Hàm `cummax` sẽ trả về một vector chứa các giá trị tối đa tích lũy tại mỗi vị trí trong vector đầu vào.
- Nếu vector đầu vào là rỗng, hàm sẽ trả về một vector rỗng.
- Hàm này có thể áp dụng cho các vector số thực, số nguyên và các kiểu dữ liệu số khác.

## Ví dụ
Dưới đây là một số ví dụ minh họa cách sử dụng hàm `cummax`:

```R
# Ví dụ 1: Sử dụng với vector số nguyên
vec1 <- c(3, 5, 2, 8, 6)
result1 <- cummax(vec1)
print(result1)
# Kết quả: 3 5 5 8 8

# Ví dụ 2: Sử dụng với vector số thực
vec2 <- c(1.1, 2.3, 1.5, 2.8, 2.7)
result2 <- cummax(vec2)
print(result2)
# Kết quả: 1.1 2.3 2.3 2.8 2.8
```

## Giải thích
- Một số điều cần lưu ý khi sử dụng `cummax`:
  - Nếu vector đầu vào chứa giá trị NA, `cummax` sẽ giữ nguyên giá trị NA cho các vị trí tương ứng trong kết quả.
  - Các giá trị âm sẽ được xử lý giống như các giá trị dương, nghĩa là hàm vẫn hoạt động bình thường và trả về giá trị tối đa tích lũy.

## Tóm tắt một dòng
Hàm `cummax` trong R tính giá trị tối đa tích lũy của một vector, giúp theo dõi giá trị lớn nhất tại mỗi vị trí trong chuỗi dữ liệu.
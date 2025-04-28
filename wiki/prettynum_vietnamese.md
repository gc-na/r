<!--
Meta Description: # Hướng Dẫn Sử Dụng Hàm prettyNum trong R ## Tóm Tắt Hàm `prettyNum` trong R được sử dụng để định dạng số liệu một cách thân thiện và dễ đọc hơn, thườ...
Meta Keywords: định, dạng, cách, phân, prettynum
-->

# Hướng Dẫn Sử Dụng Hàm prettyNum trong R

## Tóm Tắt
Hàm `prettyNum` trong R được sử dụng để định dạng số liệu một cách thân thiện và dễ đọc hơn, thường được sử dụng khi cần hiển thị dữ liệu số trong báo cáo hoặc đồ thị.

## Tài Liệu
### Mục Đích
Hàm `prettyNum` giúp định dạng các số bằng cách thêm các ký tự phân cách hoặc làm tròn số, giúp người dùng dễ dàng đọc và hiểu hơn.

### Cú Pháp
```R
prettyNum(x, ..., big.mark = ",", decimal.mark = ".", scientific = FALSE)
```

### Tham Số
- **x**: Một vector số cần được định dạng.
- **...**: Các tham số bổ sung cho hàm.
- **big.mark**: Ký tự dùng để phân cách hàng triệu (mặc định là ",").
- **decimal.mark**: Ký tự dùng để phân cách phần thập phân (mặc định là ".").
- **scientific**: Nếu TRUE, các số sẽ được hiển thị theo định dạng khoa học.

### Chi Tiết
Hàm `prettyNum` cho phép người dùng tùy chỉnh định dạng của số, bao gồm việc thay đổi ký tự phân cách và định dạng số khoa học. Hàm này rất hữu ích trong việc tạo báo cáo hoặc đồ thị, nơi mà việc hiển thị số liệu rõ ràng là rất quan trọng.

## Ví Dụ
### Ví dụ cơ bản
```R
# Định dạng số đơn giản
numbers <- c(1000, 2500.678, 3000000)
formatted_numbers <- prettyNum(numbers)
print(formatted_numbers)
# Kết quả: "1,000" "2,500.678" "3,000,000"
```

### Ví dụ với tham số tùy chỉnh
```R
# Định dạng với dấu phân cách khác
formatted_numbers_custom <- prettyNum(numbers, big.mark = ".", decimal.mark = ",")
print(formatted_numbers_custom)
# Kết quả: "1.000" "2.500,678" "3.000.000"
```

## Giải Thích
Một số người dùng có thể gặp khó khăn với việc định dạng số lớn hoặc số thập phân, đặc biệt khi sử dụng các ký tự phân cách không phải là mặc định. Điều này có thể dẫn đến việc số liệu không hiển thị đúng cách hoặc không dễ đọc. Hãy chắc chắn rằng bạn đã chỉ định đúng các tham số để đạt được định dạng mong muốn.

## Tóm Tắt Một Dòng
Hàm `prettyNum` trong R giúp định dạng số liệu để làm cho chúng dễ đọc hơn bằng cách tùy chỉnh các ký tự phân cách và định dạng.
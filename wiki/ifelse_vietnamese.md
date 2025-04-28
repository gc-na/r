<!--
Meta Description: # Hàm ifelse trong R: Cách sử dụng và ví dụ ## Tóm tắt Hàm `ifelse` trong R được sử dụng để thực hiện các phép toán điều kiện, cho phép người dùng kiể...
Meta Keywords: ifelse, hàm, các, trong, điều
-->

# Hàm ifelse trong R: Cách sử dụng và ví dụ

## Tóm tắt
Hàm `ifelse` trong R được sử dụng để thực hiện các phép toán điều kiện, cho phép người dùng kiểm tra một điều kiện và trả về các giá trị khác nhau dựa trên kết quả của điều kiện đó.

## Tài liệu
### Mục đích
Hàm `ifelse` là một công cụ mạnh mẽ trong R để thực hiện các quyết định dựa trên điều kiện. Nó cho phép người dùng xử lý dữ liệu một cách linh hoạt, đặc biệt trong các tình huống cần phân loại hoặc thay đổi giá trị trong một vector hoặc dataframe.

### Cú pháp
```R
ifelse(test, yes, no)
```

- **test**: Điều kiện cần kiểm tra. Đây là một biểu thức logic trả về giá trị TRUE hoặc FALSE.
- **yes**: Giá trị trả về nếu điều kiện là TRUE.
- **no**: Giá trị trả về nếu điều kiện là FALSE.

### Chi tiết
Hàm `ifelse` hoạt động bằng cách kiểm tra từng phần tử trong vector `test`. Nếu phần tử đó là TRUE, hàm sẽ trả về giá trị tương ứng từ `yes`, nếu là FALSE, nó sẽ trả về giá trị từ `no`. Hàm này rất hữu ích khi cần thực hiện các thay đổi trong một vector hoặc cột dữ liệu mà không cần phải lập trình nhiều dòng lệnh.

## Ví dụ
### Ví dụ cơ bản
```R
# Ví dụ 1: Sử dụng ifelse để phân loại điểm
diem <- c(85, 70, 90, 60, 55)
xep_loai <- ifelse(diem >= 75, "Đạt", "Không đạt")
print(xep_loai)
# Kết quả: "Đạt" "Đạt" "Đạt" "Không đạt" "Không đạt"

# Ví dụ 2: Sử dụng ifelse để thay thế giá trị trong vector
tuoi <- c(15, 22, 30, 10)
tinh_trang <- ifelse(tuoi < 18, "Trẻ", "Người lớn")
print(tinh_trang)
# Kết quả: "Trẻ" "Người lớn" "Người lớn" "Trẻ"
```

## Giải thích
### Những điều cần lưu ý
- Hàm `ifelse` không phải là một hàm điều kiện đơn giản. Khi sử dụng, cần phải cẩn thận với các vector có độ dài khác nhau vì hàm sẽ tự động lặp lại các giá trị ngắn hơn.
- Một số người dùng có thể gặp khó khăn khi sử dụng `ifelse` với các dữ liệu không phải là logic (như NA), vì nó có thể dẫn đến kết quả không như mong đợi. Đảm bảo kiểm tra và xử lý các giá trị NA trước khi sử dụng hàm này.
- Hàm `ifelse` có thể xử lý các vector lớn nhanh hơn so với sử dụng vòng lặp `for`, do đó, nó thường được ưa chuộng trong việc xử lý dữ liệu lớn.

## Tóm tắt một dòng
Hàm `ifelse` trong R cho phép thực hiện các phép toán điều kiện đơn giản và hiệu quả trên các vector và dataframe.
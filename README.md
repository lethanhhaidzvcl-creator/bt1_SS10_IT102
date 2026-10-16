# bt1_SS10_IT102


# Bài tập 01: Sửa lỗi đặt vé Ticketbox

## 1. Phân tích lỗi

- Lỗi 1: Hàm `datVeConcert()` nhận `soLuong` bằng tham trị. Khi tăng `soLuong` trong hàm, biến trong `main()` không thay đổi.
- Lỗi 2: Chương trình chưa kiểm tra số vé tối đa mỗi đơn hàng là 4.
- Cách sửa: Đổi hàm `datVeConcert()` từ `void` sang `int`, trả về số lượng vé mới và cập nhật lại `soLuong` trong `main()`.
- Bổ sung kiểm tra `MAX_VE` và `MAX_VE_PER_ORDER` trước khi thêm vé.
- Giá vé Early Bird được giảm 15%.

## 2. Test Cases

| Trường hợp kiểm thử | Dữ liệu đầu vào | Kết quả sai thực tế | Kết quả đúng mong đợi |
|---|---|---|---|
| TC01: Kiểm tra cập nhật số lượng | Đặt vé 101 giá 2.000.000đ, Early Bird; vé 102 giá 1.200.000đ | `soLuong` trong `main()` vẫn bằng 0, danh sách báo chưa có vé | Hiển thị 2 vé; vé 101 giá 1.700.000đ, vé 102 giá 1.200.000đ |
| TC02: Kiểm tra giới hạn đơn hàng | Đặt lần lượt 5 vé trong cùng đơn hàng | Có thể thêm quá 4 vé | Chỉ thêm tối đa 4 vé; vé thứ 5 bị từ chối và số lượng vẫn là 4 |

## 3. Kết luận

Đã sửa lỗi truyền tham trị bằng cách trả về số lượng vé mới, bổ sung giới hạn 4 vé mỗi đơn hàng và kiểm tra sức chứa mảng tối đa 100 vé.

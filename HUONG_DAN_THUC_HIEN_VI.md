# Hướng dẫn thực hiện dự án A/B test

## Mục tiêu

So sánh tỷ lệ nhấn nút **구매하기** giữa hai cách diễn đạt cùng một ưu đãi:

- Version A: `2,000원 할인`
- Version B: `10% 할인`

Giá gốc và giá cuối ở cả hai phiên bản đều là 20.000 won và 18.000 won. Chỉ được thay đổi câu giảm giá.

## Các bước cần làm

1. Đổi `username` trong hướng dẫn thành tên tài khoản GitHub của nhóm.
2. Tạo repository `username.github.io` và tải file `index.html` lên.
3. Mở `https://username.github.io` để kiểm tra Version A.
4. Mở `https://username.github.io/?preview=B` để kiểm tra giao diện Version B. Đường dẫn này chỉ dùng để kiểm tra, không gửi cho người tham gia.
5. Tạo A/B Test trong VWO, chia lưu lượng A/B theo tỷ lệ 50:50.
6. Trong VWO, chỉ đổi nội dung của `#discount-label` từ `2,000원 할인` thành `10% 할인`.
7. Tạo mục tiêu Click on element cho `#purchase-button` rồi gửi cùng một đường dẫn gốc cho tất cả người tham gia.
8. Sau tối thiểu 7 ngày và khi đạt mục tiêu khoảng 400 người, nhập số người truy cập và số người đã nhấn nút của từng phiên bản vào các ô màu vàng trong file Excel.

## Quy tắc quan trọng

- Không dừng thí nghiệm chỉ vì thấy kết quả tạm thời có lợi cho một phiên bản.
- Không tự điền hoặc bịa kết quả trước khi có dữ liệu VWO.
- Không thu thập thông tin cá nhân và không thực hiện thanh toán thật.
- Khi viết kết luận, phải báo cáo cả CTR, chênh lệch, khoảng tin cậy 95% và p-value.

## Bộ file sử dụng

- `index.html`: website thí nghiệm.
- `README_KR.md`: hướng dẫn GitHub Pages và VWO bằng tiếng Hàn.
- Báo cáo DOCX/PDF: kế hoạch và nội dung dự án đầy đủ.
- PPTX: bài trình bày chủ đề khoảng 3 phút.
- XLSX: công cụ nhập dữ liệu và tự động phân tích kết quả.

> Trước khi nộp bản kết quả cuối cùng, thay mọi dấu `[ ]` trong báo cáo bằng dữ liệu thực tế từ VWO.

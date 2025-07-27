# 📊 Phân Tích Thị Trường Xe Cũ TP.HCM cho Nhà Đầu Tư Mới

## 🚀 Giới thiệu

Dự án này mô phỏng tình huống một **Chuyên viên Phân tích Dữ liệu** được yêu cầu bởi một nhà đầu tư mới bước chân vào **thị trường xe ô tô cũ tại TP.HCM**. Mục tiêu chính là giúp chị Linh:

- Đánh giá **tiềm năng thị trường** xe cũ.
- **Xác định phân khúc** xe nên đầu tư.
- Đưa ra **chiến lược nhập hàng tối ưu** dựa trên dữ liệu thực tế.

## 📁 Dữ liệu đầu vào

- **File dữ liệu**: `Ad_table.csv`
- **Nguồn**: Tổng hợp từ các trang thương mại điện tử rao bán ô tô cũ.
- **Số lượng mẫu**: Hàng nghìn xe đã được rao bán từ nhiều năm trở lại đây.
- **Thông tin bao gồm**: Nhãn hiệu, dòng xe, năm sản xuất, giá bán, số km đã đi, thời gian đăng tin, địa điểm, loại nhiên liệu, hộp số, tình trạng xe, v.v.

---

## 🧠 Nhiệm vụ của Chuyên viên Phân tích Dữ liệu

### 1. Khám phá và phân tích dữ liệu (80%)

#### a. Mô tả dữ liệu

- **Số cột**: ~20 cột mô tả chi tiết đặc điểm của từng xe.
- **Chất lượng dữ liệu**: Có hiện tượng **thiếu dữ liệu** ở một số cột như `Giá`, `Số km đã đi`, `Loại nhiên liệu`; định dạng không đồng nhất ở một số trường văn bản.

#### b. Làm sạch và chuẩn hóa dữ liệu

- Loại bỏ hoặc xử lý các bản ghi thiếu dữ liệu quan trọng (giá, hãng xe).
- Chuẩn hóa định dạng giá, số km, ngày tháng.
- Chuyển đổi một số cột thành định dạng phân tích được: ngày → `datetime`, giá → `float`, tình trạng → phân loại.

#### c. Xây dựng mô hình dữ liệu

- Gộp các đặc trưng xe theo `hãng xe`, `dòng xe`, `năm`, để tính toán **giá trung bình**, **tỷ lệ giữ giá**, và **độ phổ biến**.
- Thiết lập các chỉ số đánh giá như:
  - Tỷ lệ rao bán theo tháng.
  - Giá trung bình theo dòng xe và khu vực.
  - Biến động giá theo năm sử dụng.

#### d. Trực quan hóa báo cáo

Sử dụng Power BI / Python / Tableau để hiển thị:

- Top 10 hãng xe phổ biến nhất tại TP.HCM.
- Giá trung bình theo dòng xe.
- Biểu đồ xu hướng rao bán theo tháng.
- Phân tích độ giữ giá sau từng năm sử dụng.
- Heatmap về khu vực rao bán sôi động nhất.

---

### 2. Phân tích cơ hội đầu tư (20%)

#### a. Gợi ý 10 dòng xe nên đầu tư ban đầu

Tiêu chí chọn:

- Phổ biến, dễ bán lại.
- Giá hợp lý: 300–800 triệu VNĐ.
- Chi phí bảo trì thấp (ưu tiên xe Nhật, Hàn).
- Giữ giá tốt.
- Phù hợp môi trường đô thị (sedan, hatchback, tiết kiệm nhiên liệu).

✅ **Gợi ý ban đầu (ví dụ)**:

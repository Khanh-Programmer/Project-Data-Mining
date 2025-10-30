# 📊 Dự án: Khai phá & Phân tích Dữ liệu Cổ phiếu FPT

## 🚀 Giới Thiệu Chung

Dự án này tập trung vào việc **khai phá, trực quan hóa và phân tích** các chỉ số tài chính cũng như biến động giá cổ phiếu của **Công ty Cổ phần FPT** qua các giai đoạn.

**Mục tiêu chính:**
* Khám phá **xu hướng tăng trưởng** tổng thể của FPT.
* Phân tích **biến động giá cổ phiếu** theo thời gian.
* Xác định **mối tương quan** giữa các chỉ tiêu tài chính quan trọng (Doanh thu, Lợi nhuận, EPS, ROE) và giá cổ phiếu.

---

## 🗂️ Nguồn Dữ Liệu

| Tiêu chí | Mô tả |
| :--- | :--- |
| **Nguồn** | Thu thập từ các trang tài chính và báo cáo doanh nghiệp chính thức của FPT. |
| **Định dạng** | `.xlsx` |
| **Các Cột Tiêu Biểu** | **`NGÀY`** (Thời điểm), **`GIÁ ĐÓNG CỬA`** (Giá cổ phiếu), **`Doanh thu`**, **`Lợi nhuận sau thuế`**, **`Tổng tài sản`**, **`EPS`**, **`ROE`**, v.v. |

---

## ⚙️ Quy Trình Thực Hiện (Workflow)

### 1️⃣ Tiền Xử Lý Dữ Liệu (Data Preprocessing)

* **Làm sạch dữ liệu:** Xử lý giá trị thiếu (`NaN`), sai định dạng, và loại bỏ các dòng/cột không cần thiết.
* **Chuẩn hóa:** Chuyển đổi cột `NGÀY` về định dạng `datetime` chuẩn.
* **Xử lý thiếu:** Điền giá trị thiếu bằng **0** hoặc **trung bình** (mean/median) tùy theo tính chất của cột.

### 2️⃣ Phân Tích Mô Tả (Descriptive Analysis)

* Tính toán **Trung bình giá đóng cửa** và **Biến động giá** theo ngày/tuần/quý.
* Thống kê mô tả cho các chỉ tiêu tài chính (Min, Max, Quartile, Độ lệch chuẩn).
* So sánh sự thay đổi của các chỉ tiêu tài chính theo từng **Năm** và **Quý**.

### 3️⃣ Trực Quan Hóa Dữ Liệu (Data Visualization)

* **Biểu đồ Tuyến (Line Plot):** Thể hiện **Giá cổ phiếu đóng cửa** theo thời gian để theo dõi xu hướng. 
* **Biểu đồ Tương quan (Heatmap):** Minh họa **mối quan hệ** giữa các chỉ tiêu tài chính và giá cổ phiếu. 

### 4️⃣ Kết Quả & Nhận Xét

* Đưa ra nhận định về **Xu hướng tăng trưởng** của FPT qua các năm.
* Xác định các **Yếu tố tài chính ảnh hưởng mạnh nhất** đến biến động giá cổ phiếu.
* Đề xuất dự đoán xu hướng ngắn hạn dựa trên mô hình thống kê đơn giản.

---

## 🛠️ Công Nghệ & Thư Viện Sử Dụng

| Thư Viện | Chức Năng Chính |
| :--- | :--- |
| **`pandas`** | Xử lý, làm sạch và thao tác dữ liệu. |
| **`numpy`** | Thực hiện các phép tính toán thống kê và ma trận. |
| **`matplotlib`**, **`seaborn`** | Trực quan hóa dữ liệu và tạo biểu đồ chuyên nghiệp. |
| **`datetime`** | Chuẩn hóa và xử lý dữ liệu ngày tháng. |

---

## 💾 Kết Quả Đầu Ra (Deliverables)

| Loại Kết Quả | Mô Tả & Định dạng |
| :--- | :--- |
| **Dữ liệu phân tích** | Tệp Excel (`.xlsx`) chứa dữ liệu đã được làm sạch và các chỉ số thống kê. |
| **Trực quan hóa** | Các tệp hình ảnh (`.PNG`/`.JPG`) chứa các biểu đồ phân tích. |

---

## 💡 Gợi Ý Mở Rộng Tiềm Năng

* **Machine Learningm Deep_Learning:** Áp dụng các thuật toán dự đoán (như ARIMA, Prophet, hoặc mô hình chuỗi thời gian) để dự đoán giá cổ phiếu FPT trong tương lai.
* **Phân tích so sánh:** So sánh FPT với các công ty công nghệ lớn khác (ví dụ: VGI, CMG, ELX) để đánh giá hiệu suất tương đối.
* **Dashboard Động:** Xây dựng một dashboard tương tác để theo dõi và cập nhật dữ liệu tài chính theo thời gian thực.

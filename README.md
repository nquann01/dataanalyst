# ⚡ Data Analysis AI - Hệ Thống Báo Cáo Thông Minh

**Developed by QuanNA**

Đây là một ứng dụng Web (Single-Page Application) chuyên sâu được thiết kế để tự động hóa hoàn toàn quy trình tổng hợp, phân tích và xuất báo cáo kinh doanh, marketing cho các dự án **Gunze, Mỹ phẩm** và **Giày Kosu**. Ứng dụng tích hợp trực tiếp **Google Gemini AI (2.5 Flash)** để đóng vai trò như một CMO ảo: đánh giá số liệu, đưa ra đề xuất chiến lược, dự báo tương lai và hỗ trợ hỏi đáp trực tiếp.

## ✨ Tính Năng Nổi Bật

* **Bảo Mật Nội Bộ:** Tích hợp màn hình xác thực mã truy cập (Auth Token) qua hệ thống Google Apps Script trước khi sử dụng.
* **Xử Lý Dữ Liệu Phức Tạp (Sapo & FB Ads):**
    * Tự động đọc, phân tích và cộng dồn dữ liệu từ các file Excel/CSV.
    * **Dự án Kosu:** Tự động bóc tách doanh thu, chi phí Ads theo từng **Nhân sự** (AnhVV, Trangle, quantm...), chia luồng hiệu quả theo **Từng Kênh** (Page Chính, Page Phụ, LDP, Livestream, Web) và **Vùng Miền** (HN, HCM).
    * Tìm kiếm và thống kê top sản phẩm bán chạy, tỷ lệ hoàn trả theo nhóm sản phẩm.
* **Hệ Thống Báo Cáo Đa Mức Độ:**
    * Báo cáo Tuần / Báo cáo Tháng (đối chiếu KPI).
    * **Dashboard Chuyên Sâu (Kosu):** Trực quan hóa dữ liệu bằng biểu đồ xu hướng ngày, bảng so sánh tăng trưởng (MoM), và phân tích độ hiệu quả chéo giữa các nhân sự.
* **Tích Hợp AI Cố Vấn (Gemini 2.5):**
    * **Tự động đánh giá:** Phân tích điểm sáng/tối trong cơ cấu sản phẩm, tỷ lệ hoàn, hiệu suất Fanpage.
    * **✨ Đề xuất chiến lược:** Đưa ra kế hoạch hành động trọng tâm.
    * **🔮 Dự báo:** Ước tính chu kỳ tiếp theo và cảnh báo rủi ro.
    * **💬 Khung Chat Dữ Liệu:** Hỏi đáp trực tiếp với AI về các chỉ số trong báo cáo vừa tạo.
* **Tiện Ích Nâng Cao:**
    * Lưu trữ lịch sử báo cáo nội bộ (Local Storage).
    * Xuất báo cáo cực nhanh ra **Ảnh (PNG)**, **PDF** hoặc **Sao chép văn bản thô** chuẩn format.

## 🚀 Hướng Dẫn Sử Dụng

Ứng dụng chạy trực tiếp trên trình duyệt, không cần cài đặt backend phức tạp:

1.  **Khởi chạy:** Mở tệp `index.html` trên trình duyệt web (Chrome, Edge, Cốc Cốc...).
2.  **Đăng nhập:** Nhập mã truy cập nội bộ do Admin cấp.
3.  **Cài đặt API Key:** Mở tab cài đặt bên trái, nhập **Google Gemini API Key** (khuyến nghị dùng key trả phí hoặc tier cao để tránh lỗi quá tải 429/503).
4.  **Nhập số liệu:**
    * Chọn tab dự án tương ứng (Gunze & MP hoặc Giày Kosu).
    * Tải lên các tệp số liệu: Dữ liệu Sale (Text), File Ads (CSV), File Sapo (CSV) hoặc Ảnh chụp cửa hàng.
    * *Mẹo: Với Kosu Dashboard, hãy tải đủ cả file Sapo và Ads của Tháng hiện tại & Tháng trước để AI so sánh MoM.*
5.  **Phân tích:** Nhấn **✦ Tạo báo cáo** và chờ AI xử lý.

## 🛠 Công Nghệ Sử Dụng

* **Frontend:** HTML5, CSS3, Vanilla JavaScript (DOM Manipulation).
* **Xử lý Dữ liệu:** `SheetJS (xlsx)` (Đọc/parse CSV, Excel).
* **Xuất File:** `html2canvas` (Render Ảnh), `html2pdf.js` (Render PDF).
* **AI Engine:** Google Generative AI API (Gemini-2.5-flash).

## ⚠️ Lưu Ý Bảo Mật
* **API Key:** API Key được lưu tại vùng nhớ tạm `localStorage` của trình duyệt người dùng cá nhân. KHÔNG hardcode API Key thực tế vào file `index.html` trước khi đẩy code lên mạng.
* **Dữ liệu Kinh doanh:** Các tệp Excel và thông số bạn tải lên sẽ được gửi dạng text/image đến máy chủ Google Gemini để phân tích.

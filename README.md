# IT108 - Session 09 - Bài4: Tối ưu chi phí Token cho hệ thống AI

## 1. Phần 1: Phân tích bài toán tối ưu Token và hiệu suất AI

* **Khái niệm Token là gì?** Token là đơn vị cơ bản mà các mô hình ngôn ngữ lớn (LLM/AI) dùng để đọc và xử lý văn bản (một từ tiếng Anh hoặc một cụm ký tự/âm tiết có thể tương đương với một hoặc nhiều token). Việc hệ thống phải xử lý ít token hơn sẽ giúp giảm tải bộ nhớ và tăng tốc độ phản hồi.
* **Tại sao Markdown giúp AI xử lý tài liệu nhanh hơn và chính xác hơn?**
  - **Dung lượng ký tự tối giản:** Markdown loại bỏ hoàn toàn các thẻ đóng mở rườm rà của HTML (như `<div>`, `<p>`, `<span>`, `<table>`, `<tr>`, `<td>`), chỉ giữ lại các ký tự điều hướng cốt lõi (như `#`, `-`, `|`, `**`).
  - **Giảm thiểu lãng phí Token:** Do cấu trúc văn bản thô cực kỳ gọn nhẹ, số lượng token tiêu tốn cho cùng một nội dung tài liệu giảm đi đáng kể (thường tiết kiệm từ 30% đến 50% token so với HTML).
  - **Tăng độ chính xác (Context Window):** Khi số lượng token giảm, AI dễ dàng tập trung vào phần nội dung cốt lõi của tài liệu bên trong giới hạn cửa sổ ngữ cảnh (Context Window) mà không bị "nhiễu" bởi các thẻ mã nguồn định dạng giao diện.

---

## 2. Phần 2: So sánh Markdown và HTML & Lựa chọn của lập trình viên

### 1. Bảng so sánh chi tiết

| Tiêu chí | Markdown (`.md`) | HTML (`.html`) |
| :--- | :--- | :--- |
| **Số lượng ký tự / Cấu trúc** | Cực kỳ ngắn gọn, dùng ký tự đại diện thô (Plain Text). | Dài dòng, lặp lại các thẻ mở và thẻ đóng phức tạp. |
| **Mức độ tiêu thụ Token** | **Thấp** (Tiết kiệm chi phí gọi API AI tối đa). | **Cao** (Làm lãng phí token vào các thẻ định dạng). |
| **Tính "Human-readable" (Độ dễ đọc)** | Trực quan, dễ đọc ngay cả dưới dạng văn bản thô trên mọi trình soạn thảo. | Khó đọc hơn do bị bao phủ bởi quá nhiều thẻ mã nguồn kỹ thuật. |
| **Tốc độ xử lý của AI** | Nhanh hơn, tiết kiệm tài nguyên tính toán của mô hình. | Chậm hơn và dễ gây quá tải ngữ cảnh với văn bản lớn. |

### 2. Lựa chọn cuối cùng và lý luận
* **Lựa chọn:** Lập trình viên **luôn ưu tiên sử dụng Markdown** khi thiết kế hệ thống truyền tải tài liệu cho AI (như viết file `README.md`, prompt hướng dẫn hệ thống, tài liệu kỹ thuật).
* **Lý luận:** Trong phát triển phần mềm và ứng dụng AI hiện đại, tối ưu chi phí API và tối ưu tốc độ phản hồi là ưu tiên hàng đầu. Markdown vừa đảm bảo con người dễ đọc - dễ viết, vừa giúp các hệ thống tự động hóa tiết kiệm chi phí vận hành đáng kể nhờ lượng token tiêu thụ thấp hơn nhiều lần so với HTML.

---

## 3. Phần 3: Hướng dẫn nộp bài
1. Tạo thư mục trên máy tính theo đúng cú pháp yêu cầu của môn học: `RE26446_IT108_Session08_Ex04` (lấy theo thông tin lớp và mã sinh viên của bạn từ [LMS Portal](https://lms-student.rikkei.edu.vn/courses/6a88fb77a493e63f11a75432)).
2. Lưu toàn bộ nội dung phân tích và bảng so sánh trên vào tệp `README.md` trong thư mục vừa tạo.
3. Đẩy (push) thư mục này lên một **Public Repository** trên [GitHub](https://github.com).
4. Copy đường dẫn URL của repository đó dán vào ô nộp bài trên hệ thống [LMS Portal](https://lms-student.rikkei.edu.vn/courses/6a88fb77a493e63f11a75432) rồi ấn nút **Nộp bài tập**.
# AI Support Log — Nhật Ký Sử Dụng AI
**Học viên:** Hồ Lương An  
**Mã học viên (MHV):** 2A202601332  

---

### 1. AI đã giúp tôi ở đâu?
- Hỗ trợ xây dựng khung cấu trúc hoàn chỉnh cho **Product Metrics Pack** theo chuẩn 5 phase của bài lab, làm rõ sự khác biệt giữa 4 khái niệm cốt lõi: *Core job, Core action, Core value, Core value event*.
- Gợi ý đặt tên sự kiện tracking chuẩn hóa theo định dạng `object_action` (ví dụ: `test_drive_booking_confirmed`, `test_drive_session_completed`) và viết 2 tiêu chí nghiệm thu kỹ thuật (Acceptance Criteria) về chống ghi đúp dữ liệu (Idempotency) và bắt trạng thái phản hồi từ backend.
- Brainstorm các góc nhìn về Leading Indicator (*Slot Selection Rate, Reminder Confirmation Rate*) và Counter-Metric (*No-Show Rate, Human Escalation Rate*) để hoàn thiện bộ chỉ số.

---

### 2. AI sai, hời hợt hoặc đề xuất metric sai nature ở đâu?
- Ban đầu, AI có xu hướng máy móc đề xuất nhịp đo lường *Daily/Weekly (DAU/WAU)* và nhầm lẫn Core Action là hành vi bề mặt như "Chat hỏi đáp thông tin xe với AI".
- AI từng đề xuất North Star Metric chỉ đếm số lượng tin nhắn trao đổi hoặc số lượt mở ứng dụng — đây là các chỉ số vanity metrics, không có ngưỡng chất lượng (Quality Threshold) và rất dễ bị làm giả/game số.

---

### 3. Tôi đã tự sửa hoặc quyết định lại điều gì?
- **Chốt lại Core Action thực chất:** Quyết định Core Action phải là hành vi **"Khách hàng hoàn tất và nhận mã xác nhận đặt lịch lái thử (`test_drive_booking_confirmed`)"**, phản ánh đúng cam kết nhận giá trị trải nghiệm xe thật tại showroom.
- **Quyết định Cadence theo bản chất (Nature):** Chọn nhịp đo là **Monthly (hoặc 30-day Window)** dựa trên hành trình mua sắm cân nhắc xe ô tô (High-involvement product), kiên quyết không áp đặt nhịp Daily/Weekly vô nghĩa.
- **Bổ sung bộ Counter-metric thực tế:** Đưa vào chỉ số **No-Show Rate** và **Human Escalation Rate** để kiểm soát chất lượng vận hành showroom và đảm bảo AI Agent hoạt động hiệu quả, không gây lãng phí nguồn lực xe demo.

# Bài nộp LAB5 — t1-healthcare · Nhóm CCD

**Lớp:** L3B · **Bàn / zone:** 7 · **Track:** t1-healthcare

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Nguyễn Tấn Châu | 2A202603846 | Phân tích lát cắt & phạm vi (§1), thiết kế UX khi AI sai & ánh xạ HAX/PAIR (§3), demo ca lạ |
| Nguyễn Phan Tấn Đức | 2A202603818 | Xây dựng bảng 10 kịch bản rủi ro & phân tích 2 ca đắt nhất (§2), chốt tiêu chí đánh giá (§6) |
| Huỳnh Văn Cường | 2A202603866 | Thiết kế mức tự chủ 5 tool theo cost-of-error (§4), dựng prototype HTML & chụp ảnh đánh số (§5) |

---

## §1. Lát cắt & phạm vi

### 1.1. Lát cắt của track
* **Sản phẩm:** Kênh chat Hỏi dược sĩ của Pharmacity
* **Một người dùng:** Khách hàng
* **Một việc:** Nhắn hỏi *"tôi (hoặc người nhà) bị X, có thuốc gì không"*
* **Một quyết định của AI:** Tự trả lời và gợi ý sản phẩm, hỏi thêm câu sàng lọc, hay chuyển dược sĩ, khuyên đi khám ngay
* **Một kết quả:** Người dùng thuốc không nhận sai sản phẩm và ca nguy hiểm không nằm trong hàng chờ

### 1.2. Ba việc tính năng KHÔNG làm
1. **Không kê đơn, gợi ý thuốc kê đơn (kháng sinh, thuốc tim mạch, huyết áp...) hoặc đề xuất "thuốc OTC thay thế" cho thuốc kê đơn:** Vì trái quy định pháp luật về dược phẩm và vượt quá thẩm quyền của AI; sai hoạt chất hoặc dùng sai thuốc kê đơn gây nguy hiểm tính mạng và kháng kháng sinh.
2. **Không tự tính toán hoặc chỉ định liều lượng uống cụ thể (số viên/lần, mg/kg):** Vì AI không nắm được cân nặng, chức năng gan/thận và bệnh nền đầy đủ của người dùng thuốc; AI chỉ dẫn chiếu thông tin in trên nhãn hoặc chuyển dược sĩ tư vấn liều.
3. **Không tự động lưu trữ thông tin sức khỏe nhạy cảm vào hồ sơ khách hàng khi chưa có sự đồng ý rõ ràng:** Vì dữ liệu bệnh lý là dữ liệu cá nhân nhạy cảm; tự ý gọi `luu_ghi_chu_suc_khoe` vi phạm quyền riêng tư và dễ lưu nhầm bệnh lý của người nhà (con, cha mẹ) vào hồ sơ người nhắn.

---
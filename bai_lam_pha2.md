# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ CHẠY AFFILIATE)

- **Họ tên:** Phạm Nhật Anh
- **Lớp:** HNKS26CNTT3
- **Link repository Pha2:** https://github.com/NkatAnh/HNKS26CNTT3_PromptAI_H04.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói Affiliate ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "TT",
    "ngay_bat_dau": "2026-12-20",
    "creator_chinh": 2,
    "thuc_tap_sinh": 1,
    "hang_tai_khoan": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "SP",
    "ngay_bat_dau": "2027-01-08",
    "creator_chinh": 3,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": null,
    "ghi_chu": "ngồi bàn gần cửa ra vào (có một bạn đang bó bột chân)"
  },
  {
    "ma_goi": "PRO",
    "ngay_bat_dau": null,
    "creator_chinh": 4,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "vip",
    "ghi_chu": "mượn thêm đèn trợ sáng và phông xanh để quay mẫu"
  }
]

```

**Link trò chuyện:** https://share.gemini.google/VKEtudtFmS56

## 4.3. Báo giá gói Affiliate bằng Chain-of-Thought

**KET QUA AI**

```text
1. **Tiền Creator chính:**
* Gói đăng ký: TT – Gói TikTok Affiliate (đơn giá: 1.500.000 đồng/Creator chính).
* Số lượng Creator chính: 4 người.
* Thành tiền: $4 \times 1.500.000 = 6.000.000\text{ đồng}$.


2. **Tiền thực tập sinh:**
* Thực tập sinh từ 15 đến dưới 18 tuổi tính 60% giá Creator chính: $60\% \times 1.500.000 = 900.000\text{ đồng/người}$.
* Số lượng thực tập sinh: 2 người (16 tuổi và 17 tuổi đều thuộc độ tuổi 15 đến dưới 18 tuổi).
* Bé 7 tuổi đi cùng ngồi khu chờ (dưới 15 tuổi): miễn phí ($0\text{ đồng}$).
* Thành tiền: $(2 \times 900.000) + 0 = 1.800.000\text{ đồng}$.


3. **Tổng tiền gói:**
* $\text{Tổng tiền gói} = \text{Tiền Creator chính} + \text{Tiền thực tập sinh} = 6.000.000 + 1.800.000 = 7.800.000\text{ đồng}$.


4. **Giảm giá team:**
* Team có 4 Creator chính (đạt điều kiện từ 4 Creator chính trở lên) nên được giảm 10% trên tổng tiền gói.
* Số tiền giảm: $10\% \times 7.800.000 = 780.000\text{ đồng}$.
* Tiền gói sau giảm: $7.800.000 - 780.000 = 7.020.000\text{ đồng}$.


5. **Phụ thu thuê mic:**
* Đơn giá thuê bộ mic thu âm không dây: 250.000 đồng/bộ (không áp dụng giảm giá).
* Số lượng thuê: 2 bộ.
* Thành tiền phụ thu: $2 \times 250.000 = 500.000\text{ đồng}$.


6. **Tổng tiền:**
* $\text{Tổng tiền} = \text{Tiền gói sau giảm} + \text{Phụ thu thuê mic} = 7.020.000 + 500.000 = 7.520.000\text{ đồng}$.



[RESULT: 7.520.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/7xbEb1jJCqL6

### b) Kiểm tra kết quả AI

AI tính đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_phong",
  "so_khach": 3,
  "so_ca_bi_anh_huong": 2,
  "tom_tat": "Team 3 người bị xếp phòng thường thiếu đèn livestream và bị ồn trong 2 ca thực hành đầu."
}
```

**Link trò chuyện:** https://share.gemini.google/NsQMOzaiBhbC

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 3.0 / 5.0 | **- Câu bị lỗi:** *"Gói TikTok Affiliate bên mình giá chỉ 1.200.000đ/người thôi... Bạn báo huỷ trước 5 ngày thì được hoàn lại đủ 100% tiền nha"*<br>

<br>**- Lý do sai:** Đã cung cấp thông tin về giá gói (1.200.000đ) và chính sách hoàn tiền (trước 5 ngày hoàn 100%), nhưng hiện thiếu dữ liệu chuẩn của trung tâm để đối chiếu xác thực tính chính xác tuyệt đối của hai con số này. | Cần đối chiếu lại bảng giá và quy định hoàn hủy hiện hành của trung tâm trước khi tư vấn (ví dụ: *"Gói TikTok Affiliate hiện có mức phí là [Giá chuẩn]đ/người. Trong trường hợp báo hủy trước [Số ngày chuẩn] ngày, bạn sẽ được hoàn lại [Tỷ lệ chuẩn]% học phí."*). |
| **Đầy đủ (30%)** | 1.5 / 3.0 | **- Câu bị lỗi:** Toàn bộ đoạn văn thiếu phần khai thác thông tin đăng ký ở cuối câu trả lời.<br>

<br>**- Lý do sai:** Mới chỉ trả lời 2 ý (giá gói và chính sách hoàn tiền), hoàn toàn thiếu bước mời khách hàng cung cấp ngày đợt thực chiến và số lượng suất muốn đăng ký. | Bổ sung câu kêu gọi hành động ở cuối: *"Để bên mình kiểm tra suất trống và giữ chỗ, bạn vui lòng cho biết ngày đợt thực chiến dự kiến tham gia cùng số lượng suất muốn đăng ký nhé!"* |
| **Giọng điệu (20%)** | 0.0 / 2.0 | **- Câu bị lỗi 1:** *"Dạ hello bạn nha!"*, *"cứ chốt lẹ kẻo hết slot nè!"*<br>

<br>**- Lý do sai:** Dùng từ ngữ suồng sã, thiếu chuyên nghiệp (*hello, nha, chốt lẹ, nè*).<br>

<br>**- Câu bị lỗi 2:** *"đăng ký xong gắn link là nổ đơn hoa hồng trăm triệu luôn ạ."*<br>

<br>**- Lý do sai:** Cam kết doanh thu, hoa hồng ảo, thổi phồng kết quả sai quy định tư vấn. | **- Sửa lỗi 1:** *"Xin chào bạn, cảm ơn bạn đã quan tâm đến khóa học bên mình."* và *"Bạn vui lòng phản hồi sớm để bên mình hỗ trợ giữ suất nhé."*<br>

<br>**- Sửa lỗi 2:** *"Sau khi đăng ký, bạn sẽ được hướng dẫn chi tiết quy trình triển khai và tối ưu kênh để đạt hiệu quả hoa hồng tốt nhất."* |
| **Tổng điểm** | **4.5 / 10** |  |  |
```

**Link trò chuyện:** https://share.gemini.google/yYHENxpDK8J7

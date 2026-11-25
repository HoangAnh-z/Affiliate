# BÀI LÀM PHA 2 

- **Họ tên:** Bùi Hoàng Anh
- **Lớp:** CNTT3
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Claude

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```JSON
[
  {"ma_goi": "SVT", "ngay_su_kien": "2026-12-20", "nguoi_lon": 2, "tre_em": 1, "loai_ve": "thuong", "ghi_chu": null},
  {"ma_goi": "FZ", "ngay_su_kien": "2027-01-05", "nguoi_lon": 3, "tre_em": 0, "loai_ve": "thuong", "ghi_chu": "một người cần hỗ trợ xe lăn"},
  {"ma_goi": "VIP", "ngay_su_kien": null, "nguoi_lon": 4, "tre_em": 0, "loai_ve": "vip", "ghi_chu": "một người khiếm thị cần hỗ trợ tìm chỗ"}
]
```

**Link trò chuyện:** https://claude.ai/share/4b62588c-65f0-42a9-8bf5-1285aa81fa1d


## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền người lớn: 5 × 1.200.000 = 6.000.000
Tiền trẻ em:
    Giá mỗi trẻ 5-11 tuổi: 1.200.000 × 70% = 840.000
    2 trẻ (8 và 10 tuổi): 2 × 840.000 = 1.680.000
    Bé 3 tuổi miễn phí: 0
Tiền vé: 6.000.000 + 1.680.000 = 7.680.000
Giảm giá nhóm: có 5 người lớn nên được giảm 5%.
Số tiền giảm: 7.680.000 × 5% = 384.000
Tiền vé sau giảm: 7.680.000 − 384.000 = 7.296.000
Phụ thu: 1 × 300.000 = 300.000 (không giảm)
Tổng tiền: 7.296.000 + 300.000 = 7.596.000
[RESULT: 7.596.000 đồng]
```

**Link trò chuyện:** https://claude.ai/share/3b3d0c2f-b727-46cb-9b79-eb051799d2bb
### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```JSON
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "Khách mua vé khán đài có mái che nhưng bị xếp khu không mái, mưa ướt ghế suốt hai hiệp đầu."
}
```

**Link trò chuyện:** https://claude.ai/share/76b00b64-6edf-4f38-acb4-43d9e37367a3

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
|---|---|---|---|
| Đúng thông tin (5,0) | 5,0/5,0 (tạm tính) | Nhân viên nêu giá "1.000.000đ/người" và chính sách "huỷ trước 3 ngày thì được hoàn tiền đầy đủ". Tôi chưa có bảng giá và chính sách chuẩn để đối chiếu, nên tạm coi hai thông tin này đúng. | Không có. Nếu số liệu chuẩn khác, tôi sẽ chấm lại. |
| Đầy đủ (3,0) | 1,5/3,0 | Câu bị lỗi: "Anh cần gì cứ nhắn em nhé!"<br>Lý do sai: Đã trả lời cả hai nội dung (giá và huỷ vé) nhưng chưa mời khán giả cung cấp ngày trận đấu và số lượng vé để đặt, nên thiếu một nửa yêu cầu của tiêu chí. | "Anh vui lòng cho em biết ngày trận đấu và số lượng vé anh muốn đặt để em hỗ trợ giữ vé cho anh ạ." |
| Giọng điệu (2,0) | 1,0/2,0 | Câu bị lỗi 1: "xem rất đã luôn ạ"<br>Lý do sai: Từ "đã luôn" mang tính khẩu ngữ, suồng sã, trái yêu cầu giao tiếp chuyên nghiệp.<br><br>Câu bị lỗi 2: "Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh."<br>Lý do sai: Từ "nha" quá thân mật, không phù hợp với văn phong chăm sóc khách hàng. | Câu 1: "Đây là trận đấu được nhiều khán giả quan tâm ạ."<br>Câu 2: "Nếu anh huỷ vé trước 3 ngày, anh sẽ được hoàn tiền đầy đủ ạ." |
| **Tổng điểm** | **7,5/10** | Đạt khá: thông tin rõ ràng, nhưng thiếu lời mời đặt vé và dùng từ ngữ chưa chuyên nghiệp. | Ưu tiên sửa hai lỗi trên. |

**Link trò chuyện:** https://claude.ai/share/dafa16f3-833b-452c-918e-94ffe431609c

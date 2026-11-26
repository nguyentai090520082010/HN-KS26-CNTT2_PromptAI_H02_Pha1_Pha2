# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 06
- **Họ tên:** Nguyễn Đức Tài
- **Lớp:** CNTT 2
- **Link repository Pha2:** https://github.com/nguyentai090520082010/HN-KS26-CNTT2_PromptAI_H02_Pha1_Pha2.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt bàn ra JSON

**KET QUA AI**

```text
[{"ma_buffet": "NUONG", "ngay_dat": "2026-12-19", "nguoi_lon": 2, "tre_em": 1, "khu_vuc": "trong_nha", "ghi_chu": null}, {"ma_buffet": "HAISAN", "ngay_dat": "2027-01-03", "nguoi_lon": 3, "tre_em": 0, "khu_vuc": null, "ghi_chu": "Một người dị ứng sữa"}, {"ma_buffet": "LAU", "ngay_dat": null, "nguoi_lon": 4, "tre_em": 0, "khu_vuc": "san_vuon", "ghi_chu": "ông ngoại đi xe lăn"}]
```

**Link trò chuyện:** https://share.gemini.google/3RNevxqpbnyE

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
1. **Tiền người lớn:**
$10 \times 399.000 = 3.990.000\text{ đồng}$
2. **Tiền trẻ em:**
* 3 trẻ cao $1,1\text{ m}$, $1,2\text{ m}$ và $1,35\text{ m}$ (từ $1\text{ m}$ đến $1,4\text{ m}$, tính $50\%$ giá người lớn): $3 \times (50\% \times 399.000) = 3 \times 199.500 = 598.500\text{ đồng}$
* 1 bé cao $0,8\text{ m}$ (dưới $1\text{ m}$, miễn phí): $1 \times 0 = 0\text{ đồng}$
* Tổng tiền trẻ em: $598.500 + 0 = 598.500\text{ đồng}$


3. **Tiền buffet (tiền người lớn + tiền trẻ em):**
$3.990.000 + 598.500 = 4.588.500\text{ đồng}$
4. **Giảm giá đoàn:**
* Đoàn có $10$ người lớn (từ $10$ người lớn trở lên, giảm $5\%$ trên tiền buffet):
* Số tiền giảm: $5\% \times 4.588.500 = 229.425\text{ đồng}$
* Tiền buffet sau giảm: $4.588.500 - 229.425 = 4.359.075\text{ đồng}$


5. **Phụ thu:**
* Thuê $1$ phòng riêng: $1 \times 500.000 = 500.000\text{ đồng}$


6. **Tổng tiền:**
$4.359.075 + 500.000 = 4.859.075\text{ đồng}$

[RESULT: 4.859.075 đồng]
```

**Link trò chuyện:** https://share.gemini.google/rwlaT9cxZmqn

### b) Kiểm tra kết quả AI

Kết luận: AI tính đúng toàn bộ các bước và khớp với tổng tiền 4.859.075 đồng theo bảng giá và quy tắc tính giá

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{"loai_su_co": "thieu_mon", "so_khach": 5, "so_mon_bi_thieu": 2, "tom_tat": "Gia đình 5 người đi buffet hải sản tối 08/11/2026 nhưng không có tôm hùm và cua."}
```

**Link trò chuyện:** https://share.gemini.google/LnKQNGSLDRl8

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
### 1. Danh sách các lỗi trừ điểm

* **Lỗi 1: Giá buffet lẩu không đúng thông tin chuẩn**
* Câu bị lỗi (trích nguyên văn): `Buffet lẩu bên em 279k/người lớn thôi, ngon bá cháy luôn.`
* Lý do sai: Giá chuẩn của buffet lẩu là 299.000 đồng/người lớn, không phải 279k/người lớn. Ngoài ra, cụm "ngon bá cháy luôn" mang tính suồng sã, thiếu chuyên nghiệp.
* Câu sửa đề xuất: `Giá buffet lẩu hiện tại của nhà hàng là 299.000 đồng/người lớn ạ.`


* **Lỗi 2: Chính sách giữ bàn khi đến trễ sai quy định**
* Câu bị lỗi (trích nguyên văn): `Chị trễ 40 phút em vẫn giữ bàn cho chị nha.`
* Lý do sai: Theo quy định chuẩn, khách đến trễ trên 30 phút sẽ bị huỷ bàn; trễ 40 phút không được giữ bàn.
* Câu sửa đề xuất: `Theo quy định giữ bàn, nếu quý khách đến trễ trên 30 phút (như trường hợp trễ 40 phút), nhà hàng xin phép huỷ bàn ạ.`


* **Lỗi 3: Thiếu lời mời cung cấp thông tin đặt bàn**
* Câu bị lỗi (trích nguyên văn): `Có gì nhắn em nhé!`
* Lý do sai: Bài tư vấn chưa mời khách cung cấp thông tin đặt bàn, đồng thời dùng từ ngữ suồng sã ("nhắn em nhé").
* Câu sửa đề xuất: `Quý khách vui lòng cho nhà hàng biết ngày giờ dự kiến và số lượng khách để bên em hỗ trợ đặt bàn trước nhé ạ.`


* **Lỗi 4: Giọng điệu suồng sã, thiếu chuyên nghiệp**
* Câu bị lỗi (trích nguyên văn): `Dạ chào chị nha! Buffet lẩu bên em 279k/người lớn thôi, ngon bá cháy luôn. Chị trễ 40 phút em vẫn giữ bàn cho chị nha. Có gì nhắn em nhé!`
* Lý do sai: Sử dụng các từ ngữ suồng sã, không phù hợp tư vấn dịch vụ chuyên nghiệp như "nha", "bên em", "ngon bá cháy luôn", "nhé".
* Câu sửa đề xuất: `Dạ chào quý khách! Giá buffet lẩu là 299.000 đồng/người lớn ạ. Theo quy định, khách đến trễ trên 30 phút sẽ bị huỷ bàn. Quý khách vui lòng cung cấp ngày giờ và số lượng khách để nhà hàng hỗ trợ đặt bàn ạ.`



---

### 2. Bảng tổng hợp chấm điểm

| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| Đúng thông tin | 0/5 | Nêu giá `Buffet lẩu bên em 279k/người lớn thôi` (sai so với 299.000 đồng/người lớn) và `Chị trễ 40 phút em vẫn giữ bàn cho chị nha` (sai quy định trễ trên 30 phút huỷ bàn). | Nêu đúng giá `299.000 đồng/người lớn` và quy định `đến trễ trên 30 phút sẽ huỷ bàn`. |
| Đầy đủ | 1/3 | Có trả lời 2 câu hỏi về giá và đến trễ 40 phút, nhưng thiếu lời mời khách cung cấp thông tin để đặt bàn (`Có gì nhắn em nhé!`). | Thêm lời mời cụ thể cung cấp ngày giờ, số lượng khách để hỗ trợ đặt bàn. |
| Giọng điệu | 0/2 | Dùng nhiều từ suồng sã, thiếu chuyên nghiệp: `nha`, `bên em`, `ngon bá cháy luôn`, `nhé`. | Dùng xưng hô và ngôn ngữ lịch sự, chuẩn mực của nhân viên tư vấn nhà hàng. |

Tổng điểm: 1/10
```

**Link trò chuyện:** https://share.gemini.google/DiAG0uwliQMs

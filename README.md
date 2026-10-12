# CS9 · Kinh tế sản phẩm AI — Nhóm 3CE

**AI in Action · Track 1 · Ngày 24**
Bài thực hành: chi phí, định giá và hiệu quả đầu tư cho một sản phẩm AI.

- Học viên: Hà Thị Mỹ Linh — 2A202602619
- Nhóm: 3CE
- File nộp: [`3CE_CS9.xlsx`](3CE_CS9.xlsx)

## Sản phẩm phân tích: ChấmNhanh (Đề bài 2)

ChấmNhanh bán cho các trung tâm ngoại ngữ. AI nhận một bài viết tiếng Anh 250–300 từ, chấm theo 4 tiêu chí và viết nhận xét. Khoảng 10% bài (sát ngưỡng hoặc bị khiếu nại) cần giáo viên kiểm tra lại.

Nhóm chưa có dự án chung nên dùng số liệu của tình huống giả định ChấmNhanh. Không có đầu vào thật nào từ các buổi trước.

## Cấu trúc file Excel

| Sheet | Nội dung |
|---|---|
| `0_Hướng dẫn` | Luật điền ô, đơn vị, ngưỡng tham khảo |
| `0_Đầu vào` | Đầu vào lấy từ các buổi trước và đề bài đã chọn |
| `A_Tài chính căn bản` | Lập 3 báo cáo tài chính cho công ty Trợ Lý Xanh (kết quả kinh doanh, cân đối kế toán, lưu chuyển tiền tệ) và trả lời câu hỏi 1–4 |
| `1_Chi phí mỗi việc` | Chi phí phục vụ một bài chấm: gọi AI, giáo viên kiểm tra, hạ tầng |
| `2_Định giá` | Gói giá, hai nhóm khách và các phép thử giá |
| `3_Giả định` | Ba kịch bản lạc quan / cơ sở / xấu |
| `4_Chỉ số mỗi khách` | Biên gộp, LTV, CAC, LTV/CAC, thời gian hoàn vốn CAC |
| `5_Dòng tiền & hiệu quả` | Dòng tiền 24 tháng, NPV, IRR, tháng hết tiền, bảng độ nhạy, mức hòa vốn |
| `6_Hiệu quả nội bộ` | Không áp dụng (ChấmNhanh bán cho khách bên ngoài) |
| `7_Quyết định` | Quyết định, luật xử lý và mức cảnh báo |
| `8_Thang điểm` | Thang điểm của giảng viên |
| `9_Số tham khảo` | Giá token, tỷ giá, lương tối thiểu kèm nguồn |

## Giả định chính

| Hạng mục | Giá trị |
|---|---|
| Mô hình AI | Claude Sonnet 5.5 — 2 USD / 10 USD mỗi triệu token vào / ra |
| Gọi mô hình mỗi bài | 2 lần × (3.000 token vào + 800 token ra), gọi lại 5% |
| Tỷ giá | 26.170 VND/USD (Vietcombank, 04/10/2026) |
| Giáo viên kiểm tra | 10% số bài × 3 phút × 120.000 đ/giờ |
| Gói giá | 3.900.000 đ/tháng gồm 600 bài, vượt hạn mức 5.500 đ/bài |
| Nhóm khách | 75% trung tâm nhỏ (500 bài/tháng) · 25% trung tâm lớn (2.500 bài/tháng) |
| Chia đối tác | 20% doanh thu |
| Kịch bản cơ sở | 10 khách mới tháng đầu, tăng 5%/tháng, rời bỏ 4,5%/tháng, CAC 7 triệu đ |
| Chi phí | Cố định 160 triệu đ/tháng, xây dựng 600 triệu đ, tiền mặt 3 tỷ đ, chiết khấu 15%/năm |

## Kết quả chính

**Chi phí mỗi bài: 1.619 đ** (gọi AI 769 đ, giáo viên 600 đ, phần còn lại 250 đ). Phần ngoài tiền AI bằng 110% chi phí gọi AI. Giá sàn (3 × chi phí) là 4.858 đ/bài.

| Chỉ số | Lạc quan | Cơ sở | Xấu | Ngưỡng |
|---|---|---|---|---|
| Biên lợi nhuận gộp | 74,6% | 68,9% | 53,4% | ≥ 60% |
| LTV ÷ CAC | 28,3 | 11,4 | 2,9 | > 3 |
| Hoàn vốn CAC (tháng) | 1,3 | 1,9 | 4,7 | < 12 |
| NPV 24 tháng | 15,03 tỷ đ | 3,51 tỷ đ | −3,23 tỷ đ | > 0 |
| Tháng hết tiền | Không | Không | Tháng 17 | Không hết trong 12 tháng |
| Hoàn vốn dự án | Tháng 10 | Tháng 15 | Chưa hoàn vốn | < 24 tháng |

- Biên gộp bình quân trước khi chia đối tác là 75,1%, sau khi chia 20% còn 55,1%.
- Trung tâm lớn đem lại 55% doanh thu. Nếu bán gói không giới hạn, tiền AI của nhóm này vượt doanh thu (biên −3,8%), nên nhóm giữ gói có phí vượt hạn mức.
- **Biến nguy hiểm nhất:** doanh thu bình quân giảm 20% làm NPV giảm khoảng 2,91 tỷ đ. Nếu trung tâm lớn rời đi và được thay bằng trung tâm nhỏ, NPV còn khoảng −58 triệu đ.

## Quyết định

**Thử nghiệm nhỏ với 10 trung tâm trong 3 tháng.** Chỉ mở rộng khi giữ được doanh thu bình quân 5,21 triệu đ/trung tâm/tháng và biên sau chia từ 55% trở lên.

**Luật xử lý:** NẾU doanh thu bình quân dưới 3.950.400 đ/trung tâm/tháng hoặc biên gộp dưới 44,7% trong 2 tuần liên tiếp, trên ít nhất 10 trung tâm, THÌ dừng mở rộng và thiết kế lại gói, tỷ lệ chia và cơ cấu khách. Không giảm phí vượt xuống dưới 4.858 đ/bài và không tăng chi quảng cáo để che cảnh báo.

**Mức cảnh báo tự tính (NPV 24 tháng = 0), đưa vào bảng theo dõi Ngày 23:**

| Chỉ số | Mức hòa vốn |
|---|---|
| Doanh thu bình quân tối thiểu | 3.950.400 đ/trung tâm/tháng |
| Biên gộp tối thiểu | 44,7% |
| CAC tối đa | 16.453.008 đ (LTV/CAC 4,8) |
| Khách mới tháng đầu tối thiểu | 6 |
| Chi phí cố định tối đa | 330.340.409 đ/tháng |
| Chia đối tác tối đa | 39,3% |

Gắn nhãn **NGUY** khi vượt ngưỡng hòa vốn và **ĐÁNG LO** khi còn cách ngưỡng không quá 10%. Phụ trách tài chính cập nhật hằng tuần.

## Cách xem file

Mở `3CE_CS9.xlsx` bằng Excel hoặc Google Sheets. Ô vàng là giả định nhập tay, ô xanh lá nhạt là công thức đã khóa. Sheet A tính bằng triệu đồng; từ sheet 1 trở đi tính bằng đồng.

## Lưu ý

- Tỷ lệ rời bỏ, CAC và tỷ lệ giáo viên kiểm tra 10% là giả định của tình huống, chưa đo thực tế.
- Giá token và tỷ giá tra ngày 04/10/2026. Nên tra lại trước khi dùng.

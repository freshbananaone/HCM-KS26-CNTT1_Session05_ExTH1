# Bài thực hành 1: Lập kế hoạch tài chính cá nhân bằng Chain-of-Thought

## 1. Mục tiêu

Sử dụng kỹ thuật Chain-of-Thought (CoT) để hướng dẫn AI lập kế hoạch chi tiêu hàng tháng. AI sẽ tính từng bước để tránh sai số và giúp biết nên dành bao nhiêu tiền cho chi tiêu, trả nợ và tiết kiệm.

## 2. Dữ liệu giả định
Lấy ví dụ một người có tình hình tài chính như sau:

- Thu nhập mỗi tháng: 20.000.000 đồng.
- Thuế phải nộp: 2.000.000 đồng.
- Chi phí cố định (tiền nhà, điện nước...): 7.000.000 đồng.
- Tiền trả nợ tối thiểu mỗi tháng: 3.000.000 đồng.
- Mục tiêu tiết kiệm: ít nhất 20% thu nhập sau thuế.

## 3. Prompt mẫu
Bạn là một trợ lý tài chính thông minh. Hãy lập kế hoạch tài chính cá nhân hàng tháng cho tôi dựa trên dữ liệu đầu vào sau:
- Thu nhập mỗi tháng: 20.000.000 đồng.
- Thuế phải nộp: 2.000.000 đồng.
- Chi phí cố định (tiền nhà, điện nước...): 7.000.000 đồng.
- Tiền trả nợ tối thiểu mỗi tháng: 3.000.000 đồng.
- Mục tiêu tiết kiệm: ít nhất 20% thu nhập sau thuế.

YÊU CẦU QUAN TRỌNG:
Hãy suy nghĩ từng bước một và tính toán chi tiết trước khi đưa ra quyết định. Bắt buộc hiển thị đầy đủ phép tính cộng trừ nhân chia trung gian, không nhảy cóc ra kết quả. Tuân thủ chính xác các bước sau:
- Bước 1: Tính toán tổng thu nhập khả dụng sau khi trừ thuế và chi phí cố định bắt buộc.
- Bước 2: Phân bổ khoản tiền trả nợ tối thiểu.
- Bước 3: Trích lập quỹ tiết kiệm theo tỷ lệ cam kết.
- Bước 4: Chia phần còn lại cho chi tiêu linh hoạt theo quy tắc 50/30/20 cải tiến.

ĐẦU RA CẦN TRÌNH BÀY THÀNH HAI PHẦN:
- Phần 1: Nhật ký suy luận logic (Reasoning Steps) chỉ ra công thức tính toán và số liệu trung gian rõ ràng.
- Phần 2: Bảng phân bổ ngân sách cuối cùng bằng Markdown Table với các cột: Hạng mục, Số tiền, Tỷ lệ %, Ghi chú (đảm bảo tổng tỷ lệ phần trăm chính xác 100%, không dùng code Python).

## 4. Kết quả chạy thử


# Phần 1: Nhật ký suy luận logic (Reasoning Steps)

## Bước 1: Tính toán thu nhập khả dụng

**Thu nhập ban đầu:** 20.000.000 VNĐ

- Thuế phải nộp: 2.000.000 VNĐ
- Thu nhập sau thuế:
  `20.000.000 - 2.000.000 = 18.000.000 VNĐ`
- Chi phí cố định bắt buộc (tiền nhà, điện nước...): 7.000.000 VNĐ
- Thu nhập còn lại:
  `18.000.000 - 7.000.000 = 11.000.000 VNĐ`

**Kết quả:** Thu nhập khả dụng là **11.000.000 VNĐ**.

## Bước 2: Phân bổ khoản trả nợ tối thiểu

- Thu nhập khả dụng: 11.000.000 VNĐ
- Khoản trả nợ tối thiểu: 3.000.000 VNĐ
- Số tiền còn lại:
  `11.000.000 - 3.000.000 = 8.000.000 VNĐ`

**Kết quả:** Trả nợ **3.000.000 VNĐ**, còn lại **8.000.000 VNĐ**.

## Bước 3: Trích lập quỹ tiết kiệm

Mục tiêu tiết kiệm tối thiểu là **20% thu nhập sau thuế**.

- Thu nhập sau thuế: 18.000.000 VNĐ
- Tiền tiết kiệm:
  `18.000.000 × 20% = 3.600.000 VNĐ`
- Số tiền còn lại:
  `8.000.000 - 3.600.000 = 4.400.000 VNĐ`

**Kết quả:** Tiết kiệm **3.600.000 VNĐ**, còn lại **4.400.000 VNĐ**.

## Bước 4: Phân bổ chi tiêu linh hoạt

Số tiền còn lại để chi tiêu là **4.400.000 VNĐ**.

Áp dụng tỷ lệ phân bổ 60/40:

- **60% cho nhu cầu thiết yếu** (ăn uống, đi lại):
  `4.400.000 × 60% = 2.640.000 VNĐ`
- **40% cho chi tiêu cá nhân** (giải trí, phát triển bản thân):
  `4.400.000 × 40% = 1.760.000 VNĐ`

## Bảng tổng kết ngân sách hàng tháng

| Khoản mục | Số tiền (VNĐ) |
|---|---:|
| Tổng thu nhập | 20.000.000 |
| Thuế | 2.000.000 |
| Chi phí cố định | 7.000.000 |
| Trả nợ tối thiểu | 3.000.000 |
| Tiết kiệm (20% sau thuế) | 3.600.000 |
| Chi tiêu thiết yếu hằng ngày | 2.640.000 |
| Chi tiêu cá nhân, giải trí | 1.760.000 |
| **Tổng phân bổ** | **20.000.000** |

## Kết luận

Kế hoạch phân bổ ngân sách đảm bảo:

1. Thanh toán đầy đủ các khoản thuế và chi phí cố định.
2. Trả nợ tối thiểu 3.000.000 VNĐ mỗi tháng.
3. Tiết kiệm đúng 20% thu nhập sau thuế.
4. Phân bổ hợp lý số tiền còn lại cho sinh hoạt và nhu cầu cá nhân.
5. Tổng chi tiêu, trả nợ và tiết kiệm không vượt quá thu nhập.

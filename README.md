# Ứng Dụng Blockchain Trong Thương Mại Điện Tử

Dự án này là bài báo cáo kết thúc học phần "Blockchain và Ứng dụng" tại Trường Đại học Ngoại ngữ - Tin học Thành phố Hồ Chí Minh (HUFLIT)[cite: 8]. Mục tiêu của dự án là xây dựng một hệ thống demo ứng dụng công nghệ Blockchain nhằm giải quyết vấn đề gian lận, thiếu tin cậy trong các giao dịch thương mại điện tử[cite: 8].

## 👥 Nhóm Thực Hiện (Nhóm 27)
*   Phan Hoàng Ân (23DH110177)
*   Huỳnh Thục Quyên (23DH114554)
*   Nguyễn Thị Trà Mi (23DH112041)

**Giảng viên hướng dẫn:** Th.S Trần Minh Thái

## 🎯 Mục Tiêu Dự Án
*   Xây dựng hệ thống demo ghi nhận lịch sử đơn hàng và thanh toán lên Blockchain phi tập trung
*   Tạo sổ cái minh bạch, bất biến làm bằng chứng xác thực cho hoạt động mua bán
*   Đánh giá tính khả thi và lợi ích của Blockchain trong thương mại điện tử (chống gian lận, bảo vệ quyền lợi người mua và người bán)

## 🏗️ Kiến Trúc Hệ Thống
Hệ thống demo được xây dựng với kiến trúc 3 thành phần:
1.  **Ứng dụng Web (Frontend):** Giao diện người dùng (React/Vue.js hoặc HTML/CSS/JS) để người mua tạo đơn hàng, thanh toán và theo dõi lịch sử giao dịch.
2.  **Máy chủ Backend:** Xử lý logic nghiệp vụ và đóng vai trò trung gian tương tác với Blockchain thông qua thư viện Web3 (như Web3.py).
3.  **Nền tảng Blockchain:** Sử dụng Ethereum/BSC Testnet để triển khai Smart Contract, lưu trữ dữ liệu đơn hàng và mô phỏng giao dịch thanh toán.

## 🛠️ Công Nghệ Sử Dụng
*   **Nền tảng Blockchain:** Ethereum/BSC Testnet
*   **Smart Contract:** Solidity
*   **Thư viện Web3:** Web3.py / Ethers.js / Web3.js
*   **Công cụ hỗ trợ:** Google Colab, Truffle/Hardhat

## ⚙️ Các Chức Năng Cốt Lõi (Smart Contract)
*   `createOrder()`: Người mua ghi nhận thông tin đơn hàng lên Blockchain với trạng thái "Pending".
*   `confirmPayment()`: Người bán (hoặc Backend) xác nhận đã nhận thanh toán, cập nhật trạng thái đơn hàng thành "Paid" và lưu mã hash giao dịch.
*   `resolveDispute()`: Hàm phân quyền dành riêng cho Trọng tài (Arbiter) để xử lý tranh chấp và cập nhật trạng thái đơn hàng cuối cùng.

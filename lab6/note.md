# 📘 Lab 06 – ATM Class & Package Diagram

## 1. Class Diagram
- **ATM**: đối tượng chính, xử lý các giao dịch (rút tiền, nạp tiền, chuyển khoản).  
- **Card**: mô tả thẻ ATM (số thẻ, mã PIN hash, trạng thái).  
- **Account**: tài khoản ngân hàng, có số dư và các thao tác debit/credit.  
- **Transaction**: lưu thông tin giao dịch (id, loại, số tiền, thời gian, trạng thái).  
- Quan hệ:
  - ATM sử dụng Card để xác thực.
  - ATM tạo Transaction khi có giao dịch.
  - Card liên kết với Account.
  - Account phát sinh Transaction khi có thay đổi số dư.

## 2. Package Diagram
- **UI**: giao diện người dùng (form đăng nhập, form rút tiền).  
- **Controller**: trung gian xử lý giữa UI và dịch vụ ngân hàng.  
- **BankService**: các nghiệp vụ ngân hàng (quản lý tài khoản, xử lý giao dịch).  
- **Hardware**: phần cứng ATM (đầu đọc thẻ, máy nhả tiền, máy in biên lai).  
- Luồng:
  - Người dùng thao tác ở UI → Controller nhận lệnh → gọi BankService → tương tác với Hardware khi cần.  

## 3. Kết luận
- Class Diagram mô tả chi tiết lớp và quan hệ.  
- Package Diagram thể hiện kiến trúc tổng quan.  
- Đây là nền tảng để bước sang Lab 07 (lập trình module Withdraw).

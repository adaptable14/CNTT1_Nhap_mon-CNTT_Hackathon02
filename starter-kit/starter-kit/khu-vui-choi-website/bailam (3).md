# BÀI LÀM – HACKATHON 02

  

-  **Mã đề:** 04

-  **Họ tên:** Hà Duy Mạnh 

-  **Lớp:** K26-HN-CNTT1

-  **Link repository:**[https://github.com/adaptable14/CNTT1_Nhap_mon-CNTT_Hackathon02](https://github.com/adaptable14/CNTT1_Nhap_mon-CNTT_Hackathon02)

-  **Hệ điều hành (Windows/macOS):** Windows

  

## 4.2. Thao tác máy tính cơ bản bằng CLI

  

### Các lệnh đã chạy

  

```

Get-Location
Get-ChildItem -Force
Move-Item .\noi_quy_khu_choi.txt .\docs\
Copy-Item .\data\ve_vao_cong_thang_4.xlsx .\backup\
 Set-Location .\logs
 Get-ChildItem
 Set-Location .
 Get-ChildItem -Force -Recurse | Select-Object FullName

  

```

  

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

  

```

FullName
--------
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\backup
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\data
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\docs
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\evidence
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\logs
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\web
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\.env
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\bai_lam.md
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\temp_404.tmp
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\backup\ve_vao_cong_thang_4.xlsx
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\data\ve_vao_cong_thang_4.xlsx
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\docs\noi_quy_khu_choi.txt
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\logs\entry.log
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\web\images
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\web\app.js
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\web\index.html
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\web\style.css
C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website\web\images\logo-kidland.png


PS C:\Users\ASUS\Downloads\starter-kit\starter-kit\khu-vui-choi-website>
  

```

  

## 4.3. Lọc log truy cập website

  

### a) Lệnh lọc các dòng status=500

  

```
 Get-Content .\logs\entry.log | Select-String "ERROR" | Set-Content .\logs\loi_500.txt
  

```

  

### 2 dòng đầu tiên trong logs/loi_500.txt

  

```text

(Dán kết quả vào đây – xoá dòng này)

  

```

  

### b) Lệnh đếm số dòng status=404 và kết quả

  

```shell

# Ghi lệnh vào đây (xoá dòng này)

  

```

  

```text

(Dán kết quả đếm vào đây – xoá dòng này)

  

```

  

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

  

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

  

```

notepad .\tong_hop.ps1
 .\tong_hop.ps1
  Get-Content .\logs\tong_hop.txt

```

  

### Nội dung file logs/tong_hop.txt

  

```
# Script: tong_hop.ps1
# Tac gia: Hà Duy Mạnh
# Ngay tao: 2026-11-11

Write-Host "Dang tao bao cao..."

"=== BAO CAO SU CO WEBSITE ===" | Set-Content .\logs\tong_hop.txt

Get-Content .\logs\entry.log | Select-String "WARNING" | Add-Content .\logs\tong_hop.txt

$errorCount = @(Get-Content .\logs\entry.log | Select-String "ERROR").Count

Add-Content .\logs\tong_hop.txt $errorCount

Write-Host "Hoan thanh!"

  

```

  

## 4.5. README.md và bảo vệ thông tin bí mật

  

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

  

- [x] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote

- [x] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)

- [x] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

  

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

  

### Bảng lỗi

  

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
|1 | Network| file cũ  | đổi lại tên đường dẫn bị lỗi thành :images/logo-kidland.png |
| 2 | Consol  | hienThiGoi(); |hienThiGoiChoi(); |

  

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

  

### Báo cáo lỗi gửi trưởng nhóm

  

-  **Context:** em đang kiểm tra website kidland trên gg bg f12

-  **Expected:** web hiển thị đầy đủ logo và bảng giá 

-  **Actual:** em nhận ra bg dữ liệu ko đúng yêu cầu em cần tìm 

-  **Log:**

  

### Câu tìm kiếm Google

  

```text



  

```

  

## 4.7. Excel

  

> Phần Excel được chấm trực tiếp trên file `data/ve_vao_cong_thang_4.xlsx`, không cần ghi vào đây.

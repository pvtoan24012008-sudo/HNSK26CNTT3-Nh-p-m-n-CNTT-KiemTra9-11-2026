# BÀI LÀM – (ĐỀ LUYỆN TẬP SỐ 02)

- **Mã đề:** 02
- **Họ tên:**Phạm Viết Toàn 
- **Lớp:** CNTT3
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\bien_ban_ban_giao.txt .\docs
mkdir backup
cp .\data\ban_ve_thang_11.xlsx .\backup
rm .\cache_991.tmp
cd .\logs
ls
cd..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         11/9/2026   9:44 PM                backup
d-----         11/9/2026   9:00 PM                data
d-----         11/9/2026   9:41 PM                docs
d-----         11/9/2026   3:15 PM                evidence
d-----         11/9/2026   8:49 PM                logs
d-----         11/9/2026   3:08 PM                web
-a----         11/9/2026   3:07 PM             82 .env
-a----         11/9/2026   3:07 PM           2611 bai_lam.md
-a----         11/9/2026   9:04 PM          11203 ban_ve_thang_11.xlsx


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/9/2026   3:07 PM           5693 ban_ve_thang_11.xlsx


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/9/2026   3:07 PM           5693 ban_ve_thang_11.xlsx


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/9/2026   3:07 PM            172 bien_ban_ban_giao.txt


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website\evidence


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/9/2026   3:11 PM         204023 Screenshot 2026-11-09 151145.png
-a----         11/9/2026   3:15 PM         194438 Screenshot 2026-11-09 151514.png


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/9/2026   3:07 PM            893 server.log


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         11/9/2026   3:08 PM                images
-a----         11/9/2026   3:07 PM            618 app.js
-a----         11/9/2026   3:08 PM            545 index.html
-a----         11/9/2026   3:08 PM            460 style.css


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap_11_9\starter-k
    it\rap-phim-website\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/9/2026   3:08 PM            342 logo-cinebox.png

```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng ERROR

```shell
Select-string "ERROR" .\logs\server.log >> .\logs\loi_error.txt
Get-Content .\logs\loi_error.txt -Head 3
```

### 2 dòng đầu tiên trong logs/loi_error.txt

```text
logs\server.log:8:2026-11-01 09:25:40 ERROR POST /api/mua-ve
logs\server.log:9:2026-11-01 09:29:11 ERROR POST /api/thanh-toan-qr
```

### b) Lệnh đếm số dòng WARNING và kết quả

```shell
(Select-String "WARNING" .\logs\server.log). Count

```

```text
5
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO SU CO WEBSITE ===

2026-11-01 09:08:10 WARNING GET /phim-sap-chieu-cu
2026-11-01 09:15:30 WARNING GET /uu-dai-thang-9
2026-11-01 09:36:50 WARNING GET /images/phong-imax.jpg
2026-11-01 10:01:20 WARNING GET /voucher-het-han
2026-11-01 10:12:55 WARNING GET /combo-bap-nuoc




Count    : 6
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property : 



```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và _in nghiêng_, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | :---: | :---: | :---: |
| 1   | network|  Tên file ảnh sai | Sửa tên ảnh theo đúng folder lưu trữ|
| 2   | console  | app.js:18 Uncaught ReferenceError: hienThiBangGia is not defined | Đổi tên ở dòng 18 thành hienThiBangGiaVe|

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- ****Context:**** Tôi là sinh viên năm nhất chưa fix lỗi hiển thị dữ liệu của web bao giờ 
- ****Expected:**** Bây giờ trang web xem phim của tôi muốn có đủ dữ liệu ở bảng hiển thị giao diện 
- ****Actual:**** Dữ liệu trên trang web không có gì và tôi vào tab console thấy thông báo lỗi app.js:18 Uncaught ReferenceError: hienThiBangGia is not 
- ****Log:**** app.js:18 Uncaught ReferenceError: hienThiBangGia is not 

### Câu tìm kiếm Google

```text
site:[https://stackoverflow.com](https://stackoverflow.com/) "Uncaught ReferenceError"
```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_ve_thang_11.xlsx`, không cần ghi vào đây.

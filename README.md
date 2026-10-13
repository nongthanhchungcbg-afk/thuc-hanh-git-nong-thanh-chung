# Thực hành tạo dự án mới trên GitHub

**Học viên: NÔNG THÀNH CHUNG**

## Mục tiêu

Tạo một Git repository trên máy tính, kết nối tới GitHub và đồng bộ README bằng các lệnh Git cơ bản.

## Ý nghĩa các lệnh

| Lệnh | Ý nghĩa |
| --- | --- |
| `git init` | Khởi tạo một repository Git cục bộ trong thư mục hiện tại. Git tạo thư mục ẩn `.git` để theo dõi lịch sử dự án. |
| `git remote add origin <URL>` | Thêm địa chỉ repository từ xa và đặt bí danh `origin` cho địa chỉ đó. |
| `git add README.md` | Đưa README vào staging area, chuẩn bị nội dung file cho commit tiếp theo. |
| `git commit -m "Add README.md file"` | Tạo một commit lưu lại các thay đổi đã stage; `-m` ghi thông điệp mô tả commit. |
| `git push -u origin main` | Đẩy commit trên nhánh `main` lên remote `origin`; `-u` thiết lập nhánh upstream để những lần push sau ngắn gọn hơn. |
| `git status` | Xem trạng thái file trong working tree, staging area và nhánh hiện tại. |
| `git log --oneline` | Xem lịch sử commit dạng ngắn. |

## Quy trình thực hiện

1. Tạo repository mới trên GitHub, đặt tên `thuc-hanh-git-nong-thanh-chung`. Chọn **Public** và không tạo README tự động.
2. Cài Git for Windows nếu máy chưa có Git.
3. Mở PowerShell hoặc Git Bash trong thư mục dự án và chạy các lệnh dưới đây. Thay `<URL-repository-cua-ban>` bằng URL HTTPS repository bạn vừa tạo trên GitHub:

```powershell
cd "$HOME\Downloads\NONGTHANHCHUNG\GitPractice"
git init
git branch -M main
git remote add origin <URL-repository-cua-ban>
git add README.md
git commit -m "Add README.md file"
git push -u origin main
```

4. Khi Git hỏi danh tính commit lần đầu, cấu hình tên và email của bạn (dùng email đã xác minh trên GitHub nếu muốn commit được gắn với hồ sơ):

```powershell
git config user.name "NÔNG THÀNH CHUNG"
git config user.email "địa-chỉ-email-của-bạn"
```

5. Mở repository trên GitHub để xác nhận `README.md` đã xuất hiện. Nộp link repository cho giảng viên.

## Lưu ý

Trong bài thực hành này, Git for Windows đã được cài đặt; repository local được khởi tạo trên nhánh `main`, README được stage và commit, sau đó đẩy lên repository GitHub. Khi Git yêu cầu xác thực lúc push, hoàn tất xác thực trong trình duyệt GitHub. Không chia sẻ mật khẩu hoặc mã xác thực với người khác.
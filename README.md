# devops-lab1-portfolio
Lab 1 — DevOps Course
Dưới đây là bảng so sánh chi tiết giữa phương pháp triển khai thủ công (Traditional) và phương pháp tự động hóa bằng DevOps (CI/CD Pipeline) dựa trên trải nghiệm thực hành lab:

| Tiêu chí | Cách THỦ CÔNG (Traditional) | Cách DEVOPS (CI/CD Pipeline) |
| :--- | :--- | :--- |
| **Làm sao để deploy?** | Copy/Upload file thủ công qua FTP, SSH, SCP hoặc remote vào server chạy lệnh | Push code lên GitHub $\rightarrow$ pipeline tự chạy |
| **Mất bao lâu?** | Vài phút đến vài giờ (tùy thuộc vào quy mô dự án và các bước thao tác) | ~10 giây |
| **Ai làm deploy?** | Con người (Developer / System Admin) thực hiện thủ công | GitHub Actions (máy tự làm) |
| **Có bị sai sót không?** | Dễ mắc lỗi human error (quên file, nhầm môi trường, thiếu cấu hình) | Không — pipeline nhất quán 100% |
| **Rollback nếu lỗi?** | Phải tìm lại phiên bản cũ, khôi phục DB/code thủ công, mất nhiều thời gian | `git revert` + push $\rightarrow$ tự động rollback |
| **Làm sao biết deploy thành công?** | Phải kiểm tra log trên server hoặc tự truy cập website để kiểm tra thủ công | GitHub Actions gửi notification :white_check_mark:/:x: |
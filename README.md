# notes-api-2324802010254

Báo cáo thực hành học phần **Điện toán Đám mây** — TDMU 2026–2027

**MSSV:** 2324802010254
**Họ tên:** Huỳnh Đăng Khoa

---

## Liên kết

| Hạng mục | Đường dẫn |
|---|---|
| Báo cáo GitHub Pages (Bài 1, 2, 3) | https://imkhoaformrbys.github.io/notes-api-2324802010254/ |
| Báo cáo — Bài 1 | https://imkhoaformrbys.github.io/notes-api-2324802010254/#lab1 |
| Báo cáo — Bài 2 | https://imkhoaformrbys.github.io/notes-api-2324802010254/#lab2 |
| Báo cáo — Bài 3 | https://imkhoaformrbys.github.io/notes-api-2324802010254/#lab3 |
| Container image (GHCR) | https://github.com/users/imkhoaformrbys/packages/container/package/notes-api |
| Kho mã nguồn | https://github.com/imkhoaformrbys/notes-api-2324802010254 |

---

## Mô tả các bài thực hành

### Bài 1 — Lập trình trên Máy ảo Đám mây Đầu tiên
Khởi tạo môi trường phát triển trên GitHub Codespaces, xây dựng API "Hello Cloud" trả về thông tin hệ thống dạng JSON, so sánh với máy tính cá nhân và nhận diện 5 đặc tính NIST qua thực nghiệm.

### Bài 2 — Ảo hóa, Container và Mô phỏng Trung tâm Dữ liệu
Đóng gói API thành Docker container, giới hạn tài nguyên bằng cgroups, phát hành image lên GHCR, và mô phỏng lập lịch trung tâm dữ liệu bằng CloudSim Plus với 4 kịch bản (Time-Shared và Space-Shared).

### Bài 3 — Lưu trữ Phân tán: NoSQL và Lưu trữ Đối tượng
Tích hợp MongoDB Atlas (Replica Set 3 nút, AWS Singapore) làm cơ sở dữ liệu NoSQL và Supabase Storage làm kho lưu trữ đối tượng. Xây dựng API CRUD đầy đủ có hỗ trợ tải tệp đính kèm. Đo hiệu quả chỉ mục B-tree trên bộ sưu tập 2.000 tài liệu: giảm số tài liệu duyệt từ 2.001 xuống 571 (hệ số 3,5×).

---

## Khởi chạy cục bộ

```bash
npm install
npm start
```

Yêu cầu tệp `.env` với các biến:

```
MONGODB_URI=mongodb+srv://<user>:<password>@<cluster>.mongodb.net/notes?retryWrites=true&w=majority
SUPABASE_URL=https://<project-ref>.supabase.co
SUPABASE_SERVICE_KEY=<secret-key>
```

API khởi động tại `http://localhost:3000`

---

## Container

```bash
docker pull ghcr.io/imkhoaformrbys/notes-api:1.0
docker run -p 3000:3000 ghcr.io/imkhoaformrbys/notes-api:1.0
```


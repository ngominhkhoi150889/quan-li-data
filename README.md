# Dữ liệu sổ chi tiêu chung

Kho này chỉ chứa dữ liệu cho ứng dụng [Sổ chi tiêu](https://ngominhkhoi150889.github.io/quan-li-chi-tieu/) — ai có link cũng xem được.

## File dữ liệu

Toàn bộ khoản chi nằm trong một file duy nhất: [`ledger.json`](ledger.json).

```json
{
  "v": 1,
  "updatedAt": "2026-11-15T08:00:00.000Z",
  "entries": [
    { "id": "…", "name": "Cà phê", "description": "Hai ly", "qty": 2, "price": 35000, "createdAt": "…" }
  ]
}
```

- `entries` là mảng chỉ-thêm; mỗi phần tử có `id` duy nhất.
- Ứng dụng chỉ đọc và thêm phần tử mới; không có endpoint sửa/xoá. Muốn sửa thì sửa file bằng tay trên GitHub.
- Hai người ghi cùng lúc không ghi đè nhau: ứng dụng dùng `sha` của file và thử lại khi GitHub báo xung đột.

## Thêm khoản chi

Trang đọc file công khai, không cần token. Để ghi, mỗi người dán một **fine-grained token** có quyền `Contents: Read and write` trên kho này vào ứng dụng một lần; token chỉ lưu trên trình duyệt của họ. Token không được nhúng vào trang công khai.

## Ghi chú

Các issue cũ (nếu còn) không còn được ứng dụng đọc; dữ liệu hiện tại lấy từ `ledger.json`.

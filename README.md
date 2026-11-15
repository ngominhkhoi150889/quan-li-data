# Dữ liệu sổ chi tiêu chung

Kho này chỉ chứa dữ liệu cho ứng dụng [Sổ chi tiêu](https://ngominhkhoi150889.github.io/quan-li-chi-tieu/) — ai có link cũng xem được.

## Cấu trúc dữ liệu

- Mỗi khoản chi là một **issue đang mở**. Tiêu đề issue là tên khoản chi.
- Phần mô tả nằm ở đầu nội dung issue; khối `<!--ledger:...-->` là dữ liệu số lượng và đơn giá do ứng dụng đọc.
- Hạn mức: ứng dụng đọc tối đa 300 issue mới nhất.
- Đóng issue sẽ ẩn khoản chi khỏi sổ (dữ liệu vẫn còn trong lịch sử issue).

## Thêm khoản chi

Trang web đọc dữ liệu công khai, không cần token. Để thêm khoản mới, điền form trên trang rồi bấm **Thêm qua GitHub**: trang mở sẵn form issue ở kho này, bạn chỉ cần đăng nhập GitHub và bấm **Submit new issue**.

Muốn thêm trực tiếp trong trang (không mở tab khác), bạn cần một fine-grained token có quyền `Issues: Read and write` trên kho này và dán vào banner của trang. Token chỉ lưu trên trình duyệt của bạn.

## Quyền

Sổ chỉ ghi thêm: không ai sửa hay xoá được khoản của người khác trong ứng dụng. Mọi issue đều công khai theo kho.

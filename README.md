# Drama Hot Hôm Nay

Trang cập nhật những tin tức drama hot nhất trong ngày, nguồn từ Facebook và TikTok.
Tin hiển thị dạng danh sách, xem lại được tối đa 7 ngày gần nhất.

## Cách chạy

Mở file `index.html` trực tiếp, hoặc bật GitHub Pages:
Settings → Pages → Deploy from a branch → Branch: `main`, thư mục `/ (root)` → Save.
Trang sẽ chạy tại `https://diepvu203.github.io/Test/`.

## Cách cập nhật dữ liệu

Toàn bộ tin nằm trong `news.json`, theo cấu trúc:

```json
{
  "updated_at": "04/11/2026 02:15",
  "days": [
    { "date": "2026-11-04", "items": [
      { "title": "...", "summary": "...", "source": "Facebook",
        "url": "https://...", "heat": 5, "tag": "Scandal" }
    ]}
  ]
}
```

- `source` chỉ nhận: `Facebook`, `TikTok`, `Báo`.
- `heat` từ 1 đến 5, càng cao càng hot, danh sách tự xếp theo độ hot.
- Mỗi lần cập nhật: thêm 1 ngày mới vào `days`, xóa các ngày cũ hơn 7 ngày.

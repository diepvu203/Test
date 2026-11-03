# Drama Hot Hôm Nay

Trang cập nhật những tin tức drama hot nhất trong ngày, chỉ lấy từ Facebook và TikTok.
Tin hiển thị dạng danh sách, chia rõ 2 mục Facebook và TikTok. Bấm vào tin là bay
thẳng qua bài gốc trên Facebook hoặc TikTok — không link qua trang báo hay trang khác.
Xem lại được tối đa 7 ngày gần nhất.

## Cách chạy

Mở file `index.html` trực tiếp, hoặc bật GitHub Pages:
Settings → Pages → Deploy from a branch → Branch: `main`, thư mục `/ (root)` → Save.
Trang sẽ chạy tại `https://diepvu203.github.io/Test/`.

## Cách cập nhật dữ liệu

Toàn bộ tin nằm trong `news.json`, theo cấu trúc:

```json
{
  "updated_at": "04/11/2026 02:30",
  "days": [
    { "date": "2026-11-04", "items": [
      { "title": "...", "summary": "...", "source": "Facebook",
        "url": "https://www.facebook.com/...", "heat": 5, "tag": "Scandal" }
    ]}
  ]
}
```

Quy tắc bắt buộc:

- `source` chỉ nhận: `Facebook`, `TikTok`.
- `url` chỉ được là link `https://www.facebook.com/...` hoặc
  `https://www.tiktok.com/...`. Không dùng link báo, YouTube hay trang tổng hợp.
- `heat` từ 1 đến 5, càng cao càng hot, danh sách tự xếp theo độ hot.
- Mỗi lần cập nhật: thêm 1 ngày mới vào `days`, xóa các ngày cũ hơn 7 ngày.

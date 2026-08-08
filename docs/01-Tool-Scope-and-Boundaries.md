# 01 — Tool Scope and Boundaries

## Tool làm gì

Product DNA Engine nhận asset đã được kiểm tra từ Asset Cleaner và tạo mô hình dữ liệu mô tả sản phẩm: category, silhouette, construction, neckline, sleeve, closure, color, pattern, material appearance, hardware, accessories, logos, text, dimensions tương đối, critical identity features, uncertainty và consistency locks.

## Tool tuyệt đối không làm

- Không generate hoặc edit ảnh.
- Không quyết định Luxury/Commercial/Editorial.
- Không quyết định lens, camera motion, framing.
- Không biên đạo tay/chân/người mẫu.
- Không thay background.
- Không áp lighting/color grade.
- Không tạo video.
- Không “hoàn thiện” chi tiết bị che bằng suy đoán.
- Không đổi `unknown` thành fact để JSON “đẹp hơn”.
- Không tự gộp hai sản phẩm thành một sản phẩm.
- Không tự coi phụ kiện thật là hallucination.

## Single Responsibility

T02 trả lời: **“Sản phẩm hiện có đặc điểm gì, chúng ta biết điều đó chắc đến đâu, và những đặc điểm nào phải được khóa?”**

T03+ mới trả lời các câu hỏi sáng tạo.

## Priority

1. User-confirmed truth.
2. Clear multi-view visual evidence.
3. Clear single-view evidence.
4. Structured metadata from T01.
5. Conservative inference.
6. Unknown.

Không được đảo priority vì “thường quần áo kiểu này sẽ…”.

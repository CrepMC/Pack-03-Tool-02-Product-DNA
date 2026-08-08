# 02 — User Workflow

## Flow chuẩn

1. Import `AssetReport`.
2. Validate schema, readiness, lineage.
3. Hiển thị asset đã chọn theo role.
4. Chạy Product Scan.
5. Tạo danh sách sản phẩm/đối tượng.
6. Người dùng xác nhận `main product` và `companion items` khi mơ hồ.
7. Chạy extraction theo category.
8. Hiển thị Product DNA Review.
9. Flag field confidence thấp.
10. Người dùng sửa/xác nhận field nếu cần.
11. Khóa DNA.
12. Xuất artifact và handoff T03.

## Các trạng thái UI

`WAITING_INPUT → VALIDATING → SCANNING → NEEDS_REVIEW | READY_FOR_REVIEW → USER_REVIEW → LOCKED → EXPORTED`

Từ mọi state có lỗi schema có thể chuyển `BLOCKED`. `LOCKED` không được chỉnh trực tiếp; thay đổi phải tạo revision mới.

## UX principle

Không ép người dùng duyệt 100 field. Chỉ surface:
- conflict;
- low confidence;
- critical identity field;
- potentially destructive misclassification;
- missing view quan trọng.

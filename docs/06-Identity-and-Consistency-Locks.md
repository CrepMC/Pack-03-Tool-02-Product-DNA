# 06 — Identity and Consistency Locks

`ConsistencyLockSpec` là output quan trọng thứ hai sau ProductDNA.

## Hard locks

Dùng cho:
- category;
- silhouette;
- neckline/collar;
- sleeve shape;
- closure;
- exact visible accessory presence;
- dominant color;
- major pattern;
- major logo/graphic;
- unique trim/hardware.

Hard lock chỉ tạo khi field observed/user_confirmed đủ confidence.

## Soft locks

Dùng cho:
- material appearance;
- minor texture;
- subtle drape;
- tiny stitching;
- uncertain color nuance.

## Prohibited mutations

Ví dụ:
- V-neck → shirt collar;
- no collar → added lapel;
- plain hem → ruffle;
- drawstring removed/added;
- hat in reference bị xóa;
- bag tự sinh;
- polka-dot size/pattern thay đổi đáng kể;
- color family drift.

## Unknown handling

Không tạo lock “must be X” nếu value unknown. Thay vào đó tạo guard: `do_not_invent`.

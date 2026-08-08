# 05 — Attribute Extraction Rules

## Field extraction

Mỗi field có:
- `value`
- `status`
- `confidence`
- `evidence_refs`
- `criticality`
- `notes`

## Color

Tách:
- observed base color;
- secondary colors;
- pattern colors;
- uncertainty do lighting;
- user-confirmed canonical color nếu có.

Không lấy màu cinematic grade làm màu sản phẩm.

## Material

Dùng `material_appearance` khi chỉ có ảnh: matte woven, smooth knit, denim-like, satin-like. Chỉ khẳng định “cotton”, “silk”, “linen” khi có metadata hoặc user-confirmed evidence.

## Construction

Các yếu tố như neckline/collar/closure/pocket/hardware thường là high-criticality vì video AI hay làm biến dạng.

## Text/logo

Không tự OCR nếu chữ không đủ rõ. Ghi `partially_legible` hoặc `unknown`; không bịa spelling.

## Countable details

Số nút, túi, dây, khoen chỉ được ghi số khi vùng đó đầy đủ và không bị occlusion.

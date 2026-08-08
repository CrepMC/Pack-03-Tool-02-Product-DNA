# 03 — Evidence Model

Mỗi thuộc tính quan trọng phải có evidence record.

## Evidence record

- `evidence_id`
- `asset_id`
- `region`
- `observation`
- `visibility`
- `quality`
- `view_angle`
- `supports`
- `contradicts`
- `confidence_contribution`

## Bốn trạng thái tri thức

### observed
Nhìn trực tiếp thấy từ asset đủ rõ.

### inferred
Suy ra hợp lý nhưng không nhìn trực tiếp. Không được dùng cho critical locks trừ khi user xác nhận.

### user_confirmed
Người dùng xác nhận rõ; có priority cao nhất.

### unknown
Không đủ dữ liệu. Đây là kết quả hợp lệ.

## Evidence aggregation

Không cộng confidence cơ học. Multi-view độc lập làm tăng confidence; nhiều crop của cùng một ảnh không được tính là evidence độc lập.

## Contradiction

Nếu asset A cho thấy V-neck nhưng asset B có vẻ crew neck:
- không chọn ngẫu nhiên;
- tạo conflict;
- xác định asset role/lineage;
- yêu cầu human review nếu đều là reference hợp lệ.

# 07 — Confidence Scoring

## Mục tiêu

Confidence là tín hiệu review, không phải giả vờ xác suất khoa học.

## Recommended bands

- 0.90–1.00: clear/confirmed
- 0.75–0.89: good evidence
- 0.55–0.74: uncertain; review nếu critical
- 0.30–0.54: weak; không hard-lock
- 0.00–0.29: unknown

## Factors

- visibility;
- resolution/sharpness;
- occlusion;
- angle suitability;
- cross-view agreement;
- user confirmation;
- contradictory evidence;
- lighting distortion.

## Criticality override

Neckline confidence 0.72 vẫn cần review; một texture phụ 0.72 có thể chấp nhận soft lock.

## Không làm

- Không hiển thị 99.9% nếu không có basis.
- Không tăng confidence chỉ vì model “biết thời trang”.
- Không coi metadata do model tự sinh là independent evidence.

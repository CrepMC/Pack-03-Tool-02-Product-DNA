# 01 — Inbound from Asset Cleaner

Envelope:
- `source_tool = T01_ASSET_CLEANER`
- `target_tool = T02_PRODUCT_DNA`
- `artifact_type = AssetReport`
- payload schema `AssetReport` v1.x
- SHA-256 canonical JSON

T02 chỉ ACCEPT nếu:
- schema hợp lệ;
- status APPROVED;
- readiness READY;
- selected assets tồn tại;
- lineage không đứt.

Nếu critical visibility không đủ: tạo `RevisionRequest` về T01.

# 10 — State Machine

## States

- WAITING_INPUT
- VALIDATING_INPUT
- INPUT_REJECTED
- SCANNING_PRODUCTS
- EXTRACTING
- RESOLVING_CONFLICTS
- NEEDS_HUMAN_REVIEW
- READY_FOR_REVIEW
- USER_REVIEW
- LOCKING
- LOCKED
- EXPORTING
- EXPORTED
- BLOCKED

## Guards

- Không EXTRACTING nếu AssetReport chưa READY/APPROVED.
- Không LOCKED nếu unresolved critical conflict còn tồn tại.
- Không EXPORT nếu schema invalid.
- LOCKED artifact immutable.
- Revision tạo artifact version mới.

## Idempotency

Re-run cùng asset + cùng config + cùng user confirmations phải không làm thay đổi identity fields vô cớ.

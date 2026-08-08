# 02 — Outbound to Creative Director

Envelope:
- `source_tool = T02_PRODUCT_DNA`
- `target_tool = T03_CREATIVE_DIRECTOR`
- `artifact_type = ProductDNA`
- payload ProductDNA v1.0.0
- lock artifact `ConsistencyLockSpec`
- integrity hash.

T03 acknowledge:
`ACCEPTED | REJECTED | NEEDS_MIGRATION | NEEDS_HUMAN_REVIEW`.

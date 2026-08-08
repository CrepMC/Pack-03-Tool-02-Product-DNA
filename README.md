# Pack 03 — Tool 02: Product DNA Engine

**Version:** 1.0.0  
**Target:** Google Flow Tool Maker / AI Studio-style custom tool workflow  
**Upstream:** T01 Asset Cleaner  
**Downstream:** T03 Creative Director  
**Primary artifact:** `ProductDNA`

## Mục tiêu

Tool 02 biến các asset đã được T01 kiểm tra thành một bản mô tả sản phẩm có cấu trúc, có bằng chứng và có mức độ tin cậy. `ProductDNA` là **source of truth về sản phẩm** cho toàn pipeline quảng cáo video. Tool này không được tự sáng tạo đặc điểm sản phẩm, không được tự sửa ảnh, không được quyết định phong cách quảng cáo, camera, chuyển động hay cinematic look.

## Nguyên tắc lõi

1. **Evidence before attribute** — không có bằng chứng hình ảnh đủ rõ thì không khẳng định.
2. **Unknown is valid** — `unknown` tốt hơn một thuộc tính bịa.
3. **Visible ≠ inferred** — luôn tách cái nhìn thấy khỏi cái suy đoán.
4. **Product identity is immutable downstream** — chi tiết được khóa ở T02 không được tool sau tự ý đổi.
5. **Asset lineage is preserved** — mọi kết luận phải chỉ ra asset/evidence tương ứng.
6. **No hidden correction** — nếu T01 chưa đủ chất lượng thì tạo revision request, không âm thầm “tưởng tượng cho đủ”.
7. **No creative direction** — Product DNA mô tả *sản phẩm là gì*, không quyết định *quảng cáo nó như thế nào*.

## Ba prompt chính

- [prompts/Prompt-01-Foundation-UI-and-Inbound-Contract.md](prompts/Prompt-01-Foundation-UI-and-Inbound-Contract.md)
- [prompts/Prompt-02-Vision-Extraction-Evidence-and-Taxonomy.md](prompts/Prompt-02-Vision-Extraction-Evidence-and-Taxonomy.md)
- [prompts/Prompt-03-Production-Hardening-Locks-and-Handoff.md](prompts/Prompt-03-Production-Hardening-Locks-and-Handoff.md)

Chạy ba prompt theo đúng thứ tự. Prompt 2 và Prompt 3 giả định Tool Maker đã hoàn thành và bảo toàn thay đổi của prompt trước.

## Cấu trúc

- `docs/`: thiết kế sản phẩm và quy tắc vận hành.
- `schemas/`: JSON Schema cho artifact/handoff.
- `taxonomies/`: taxonomy chuẩn để giảm vocabulary drift.
- `protocol/`: handoff T01→T02 và T02→T03.
- `examples/`: tình huống chuẩn và mơ hồ.
- `tests/`: acceptance, regression, adversarial và contract tests.
- `checklists/`: checklist triển khai và review.
- `diagrams/`: sơ đồ Mermaid.
- `templates/`: mẫu issue, revision request, evidence record.
- `references/`: baseline của dự án và phạm vi claim.

## Definition of Done

Tool được coi là đạt khi:

- nhận `AssetReport` hợp lệ từ T01;
- không sửa asset;
- trích xuất Product DNA có evidence;
- phân biệt `observed`, `inferred`, `unknown`, `user_confirmed`;
- tạo immutable lock specification;
- không tự thêm phụ kiện hoặc chi tiết trang phục;
- không đẩy thuộc tính confidence thấp thành fact;
- có cơ chế human review;
- output validate với schema;
- handoff sang T03 không kèm conversation thừa;
- vượt acceptance + adversarial tests của pack.

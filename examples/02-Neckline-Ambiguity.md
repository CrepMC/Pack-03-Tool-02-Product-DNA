# Example 02 — Neckline ambiguity

Ảnh tóc che một phần cổ. Model thấy khả năng V-neck nhưng không chắc.

Expected:
- `neckline.status = inferred|unknown`;
- confidence dưới hard-lock threshold;
- UI hỏi người dùng hoặc request view rõ;
- tuyệt đối không hard-lock “shirt collar”.

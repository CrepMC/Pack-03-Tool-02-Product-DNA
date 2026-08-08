# Example 03 — Real accessory vs hallucination

Ảnh reference có mũ thật. Không được dùng negative rule chung kiểu “no hats”.

Expected:
- mũ được tách thành product/accessory candidate;
- nếu confirmed, presence trở thành lock;
- downstream chỉ cấm *extra accessory absent from reference*.

# 13 — Performance and Storage

- Cache analysis theo asset content hash + config version.
- Evidence crop chỉ lưu reference/coordinate nếu platform hỗ trợ, tránh duplicate binary.
- Lazy-load evidence inspector.
- Không serialize image bytes vào ProductDNA.
- ProductDNA phải nhỏ, deterministic, portable.
- Dùng canonical JSON trước khi hash.
- Giới hạn số candidate product để tránh UI overload; overflow vào secondary list.

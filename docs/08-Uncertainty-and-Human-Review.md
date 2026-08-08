# 08 — Uncertainty and Human Review

## Trigger review

- critical field dưới threshold;
- asset conflict;
- main product ambiguous;
- accessory may belong to background;
- front/back orientation uncertain;
- neckline partially occluded;
- logo/text partially legible;
- product boundary overlap;
- color heavily affected by lighting;
- outfit includes multiple similar products.

## Review interaction

UI phải hỏi cụ thể:
- “Cổ áo là V-neck không cổ hay có cổ bẻ?”
- “Dây ở eo là chi tiết của quần hay vật phía sau?”

Không hỏi chung chung “Bạn muốn sửa gì?”.

## User correction

User edit tạo evidence type `user_confirmed`, không xóa model evidence cũ. Audit trail ghi old/new/reason/timestamp.

## No forced completion

Người dùng có thể chấp nhận `unknown` và tiếp tục. Downstream phải tôn trọng guard `do_not_invent`.

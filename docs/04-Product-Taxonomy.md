# 04 — Product Taxonomy

Taxonomy dùng vocabulary ổn định để giảm prompt drift.

## Top-level

- upper_garment
- lower_garment
- dress_or_skirt
- footwear
- bag
- headwear
- eyewear
- jewelry
- belt
- watch
- accessory_other

## Category-specific attribute packs

### Upper garment
neckline, collar, sleeve, closure, placket, hem, fit, length, pocket, yoke, cuff, shoulder, pattern, trim.

### Lower garment
waistband, rise, leg_shape, length, closure, pocket, pleat, crease, hem, drawstring, belt_loop.

### Dress/skirt
neckline, sleeve, waist, bodice, skirt_shape, slit, length, layer, drape.

### Footwear
toe, heel, sole, upper, closure, strap, shaft, hardware.

### Bag
body_shape, handle, strap, closure, compartment, hardware, logo placement.

### Accessories
category-specific field pack, không ép garment fields lên phụ kiện.

## Rule

Nếu category chưa chắc: giữ `category_candidates[]`, không ép taxonomy sâu.

# Acceptance Tests

## A01 — Valid upstream
Given AssetReport APPROVED/READY, Tool scan và tạo ProductDNA schema-valid.

## A02 — No image mutation
Không action nào generate/edit/replace asset.

## A03 — V-neck no collar
Input rõ V-neck collarless → `neckline=v_neck`, `collar=none`, hard lock khi confidence đủ.

## A04 — Occluded neckline
Không đủ evidence → unknown/inferred + review, không tự tạo collar.

## A05 — Real accessory
Mũ thật trong reference → không bị negative rule xoá.

## A06 — Extra accessory prevention
Không có bag trong reference → guard downstream “do not invent bag” khi appropriate.

## A07 — Material caution
Ảnh giống cotton nhưng thiếu metadata → không ghi cotton fact.

## A08 — User confirmation
User sửa collar → user_confirmed, audit preserved.

## A09 — Conflicting assets
Hai view conflict critical → block locking.

## A10 — Multiple products
Áo/quần/túi tách product ID.

## A11 — Unknown valid
Artifact có unknown vẫn export được nếu non-blocking.

## A12 — No creative leakage
ProductDNA không chứa luxury, camera lens, motion choreography.

## A13 — Lock evidence
Mọi hard lock có evidence refs.

## A14 — Immutable locked artifact
Edit sau LOCKED → tạo revision version mới.

## A15 — T03 handoff
Envelope validate và chỉ truyền artifact cần thiết.

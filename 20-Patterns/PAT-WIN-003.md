---
type: pattern
pattern_id: PAT-WIN-003
domain: Windows
topic: Lifecycle
---
# Section / mapping / cache lifetime

## Problem Pattern
mapping 存在时 cache 可能提前删除。

## Detection
区分 object/view/handle/driver owner，使用 refcount/rundown。

## General Rule
mapping 存在不等于 cache ownership。

## Related Cases
- [[CASE-WIN-20260921-001]]

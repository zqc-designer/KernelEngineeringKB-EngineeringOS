---
type: pattern
pattern_id: PAT-LNX-001
domain: Linux
topic: I/O
---
# cloned BIO 生命周期与引用计数

## Problem Pattern
clone BIO 的 submit/end_io/bio_put/free ownership 不一致。

## Detection
记录 identity、owner、parent/clone、submit、end_io、put、free；检查 bi_private/bi_end_io。

## General Rule
任何 clone 必须明确 owner 与引用责任。

## Related Cases
- [[CASE-LNX-20261001-001]]
- [[CASE-LNX-20260923-001]]

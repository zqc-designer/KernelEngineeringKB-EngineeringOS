---
type: pattern
pattern_id: PAT-LNX-003
domain: Linux
topic: Lifecycle
---
# BIO completion callback context 所有权

## Problem Pattern
bi_private/bi_end_io 恢复顺序错误可能导致 UAF 或错误 callback。

## Detection
建立 original→clone context table。

## General Rule
callback ownership 必须与 BIO ownership 同步。

## Related Cases
- [[CASE-LNX-20260923-001]]

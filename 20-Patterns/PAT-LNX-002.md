---
type: pattern
pattern_id: PAT-LNX-002
domain: Linux
topic: Concurrency
---
# outstanding 计数与 queue drain

## Problem Pattern
worker 退出不仅取决于队列为空，还取决于所有 submitted I/O 完成。

## Detection
记录 enqueue→submit→complete→dequeue，并验证 outstanding=0。

## General Rule
计数器是 lifecycle invariant。

## Related Cases
- [[CASE-LNX-20261001-001]]
- [[CASE-LNX-20260928-001]]

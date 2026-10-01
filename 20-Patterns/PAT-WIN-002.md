---
type: pattern
pattern_id: PAT-WIN-002
domain: Windows
topic: Concurrency
---
# async worker/completion 与 cleanup/stop 竞态

## Problem Pattern
cleanup/stop 与 async completion 同时修改 context。

## Detection
completion 前 acquire rundown，cleanup 等待 rundown。

## General Rule
callback 期间 context 必须保持有效。

## Related Cases
- [[CASE-WIN-20261001-001]]

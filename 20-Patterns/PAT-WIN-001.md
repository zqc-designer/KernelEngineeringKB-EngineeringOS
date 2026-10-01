---
type: pattern
pattern_id: PAT-WIN-001
domain: Windows
topic: Lifecycle
---
# Driver unload 的 rundown barrier

## Problem Pattern
unload pending 时 worker、IRP、mapping、DeviceObject 仍可能存活。

## Detection
stop new work→worker drain→IRP drain→mapping drain→cleanup→unload。

## General Rule
unload 是状态机终点。

## Related Cases
- [[CASE-WIN-20261001-001]]
- [[CASE-WIN-20260920-001]]

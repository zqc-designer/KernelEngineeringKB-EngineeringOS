---
type: pattern
pattern_id: PAT-WIN-004
domain: Windows
topic: Crash Analysis
---
# 0x50/0xD1/0x7E 按代码位置聚类

## Problem Pattern
多个 bugcheck 可能共享生命周期边界。

## Detection
按函数、结构体、资源、IRQL、线程角色聚类。

## General Rule
不要只按 bugcheck code 分类。

## Related Cases
- [[CASE-WIN-20261001-001]]

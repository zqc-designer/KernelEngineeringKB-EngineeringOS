---
type: pattern
pattern_id: PAT-LNX-004
domain: Linux
topic: Crash Analysis
---
# 高压 I/O 下先证明内存破坏再归因

## Problem Pattern
virtqueue/skb 等底层 crash 可能只是上游内存破坏结果。

## Detection
寻找 slab corruption、UAF、DMA/BIO 越界、callback 指针异常等直接证据。

## General Rule
没有直接证据时不要仅凭底层栈归因 disk_filter。

## Related Cases
- [[CASE-LNX-20261001-001]]

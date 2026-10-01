---
type: playbook
playbook_id: PB-LNX-001
domain: Linux
version: v1.0
---
# Linux Block Driver BIO 生命周期排查

## Trigger
高压 I/O、UAF、double free、virtqueue/skb 异常

## Procedure
给 BIO 建唯一 ID；画 original/clone ownership；记录 alloc/clone/submit/end_io/put/free；核对 bi_private/bi_end_io；核对 outstanding；注入 completion 延迟；再判断归因。

## Exit Criteria
每个 BIO 生命周期闭合；无 UAF/double put；submitted==received；stop 后 outstanding==0。

## Source Patterns
- [[PAT-LNX-001]]
- [[PAT-LNX-002]]
- [[PAT-LNX-003]]
- [[PAT-LNX-004]]

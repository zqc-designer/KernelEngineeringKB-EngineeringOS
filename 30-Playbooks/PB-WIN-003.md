# PB-WIN-003 — Async I/O cancel / pending IRP 排查

1. 建 request ID
2. SUBMITTED/PENDING
3. cancel → CANCELING
4. 等 completion
5. 唯一 owner 释放 context
6. 压测 cancel/complete race

**Exit:** 每个 request 恰好一个终态和一次资源释放。

[[PAT-WIN-005]] [[PAT-WIN-002]]

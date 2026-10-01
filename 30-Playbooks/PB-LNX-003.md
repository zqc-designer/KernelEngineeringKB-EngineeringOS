# PB-LNX-003 — Block I/O 内存破坏归因排查

1. 锁定 crash 时间线
2. 给 BIO 建 ID
3. 记录 clone/submit/end_io/put/free
4. 检查 callback/context
5. 检查 slab poison/redzone
6. 对齐异常地址
7. 只在有直接证据时归因

**Exit:** BIO lifecycle 闭合或获得明确 memory corruption 证据链。

[[PAT-LNX-005]] [[PAT-LNX-001]] [[PAT-LNX-003]]

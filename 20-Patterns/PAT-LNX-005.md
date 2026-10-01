# PAT-LNX-005 — Block I/O attribution requires lifecycle evidence

下层 block/net 崩溃不等于上游 filter 直接损坏。先对齐 BIO lifecycle、memory corruption 证据和 crash 时间线。

**Detection:** BIO ID、submit/end_io、poison/redzone、异常地址、UAF/越界/double free。

**Rule:** 先证明生命周期违规，再做组件归因。

[[CASE-LNX-20260928-002]] [[PB-LNX-003]]

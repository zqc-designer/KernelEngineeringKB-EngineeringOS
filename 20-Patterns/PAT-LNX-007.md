# PAT-LNX-007 — mmap cache requires capacity/mapping invariants

`vmalloc_user` + `remap_pfn_range` 必须同时满足 allocation、mapping length、capacity、boundary 一致性。

**Detection:** PAGE_ALIGN、PFN 数、mapping length、capacity/boundary、释放顺序。

[[CASE-LNX-20260921-002]] [[PB-LNX-005]]

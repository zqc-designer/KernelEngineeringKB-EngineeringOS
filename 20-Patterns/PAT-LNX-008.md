# PAT-LNX-008 — Kernel file I/O must have operation ownership

file_io 在 stop、completion、metadata update 期间必须能回答“谁在等谁”和“谁负责完成”。

**Detection:** operation ID、file ref、submit、complete、metadata、close。

[[CASE-LNX-20260928-003]] [[PB-LNX-004]]

# PAT-LNX-006 — Stop condition must separate queue drain and I/O drain

队列为空不代表所有异步 I/O 已完成。stop 必须区分 STOPPING、QUEUE_DRAIN、IO_DRAIN、TERMINATED 和 outstanding。

**Rule:** 用状态机表达终止条件。

[[CASE-LNX-20260929-002]] [[PB-LNX-004]]

# PAT-WIN-005 — Async I/O cancellation is a state machine

异步 WriteFile 的 cancel 必须统一建模 pending IRP、cancel race 和 completion ownership。取消与正常完成汇聚到同一释放路径。

[[CASE-WIN-20260922-002]] [[PB-WIN-003]]

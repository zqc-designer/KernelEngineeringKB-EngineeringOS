# PB-LNX-004 — soft lockup / hung task 状态机排查

1. 找 worker
2. 展开等待链
3. 拆分 STOPPING/QUEUE_DRAIN/IO_DRAIN
4. 检查 completion
5. 注入 delay/timeout
6. 验证 terminal state

**Exit:** queue empty 且 outstanding==0，或明确 timeout/error terminal state。

[[PAT-LNX-006]] [[PAT-LNX-008]]

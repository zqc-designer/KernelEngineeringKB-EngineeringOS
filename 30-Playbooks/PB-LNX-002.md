---
type: playbook
playbook_id: PB-LNX-002
domain: Linux
version: v1.0
---
# Linux 高压 I/O soft lockup / hung task 排查

## Trigger
soft lockup、hung task、kthread 长时间运行

## Procedure
找线程；展开等待链；检查 while 条件；分离 stop/queue/outstanding；检查 completion；注入 timeout/stop；验证 drain。

## Exit Criteria
stop && queue_empty && outstanding==0，或明确 error terminal state。

## Source Patterns
- [[PAT-LNX-002]]

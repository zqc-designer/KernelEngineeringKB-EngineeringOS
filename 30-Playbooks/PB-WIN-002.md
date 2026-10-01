---
type: playbook
playbook_id: PB-WIN-002
domain: Windows
version: v1.0
---
# Windows Section / mapping / cache 生命周期排查

## Trigger
cache 删除、进程退出、thread sleep/unmap、mapping UAF

## Procedure
列 owner；区分 object/view/handle；建立 ref/rundown；stop new access；等 mapping users；unmap；删除 cache。

## Exit Criteria
最后一个访问者退出后才释放 backing storage。

## Source Patterns
- [[PAT-WIN-003]]

---
type: playbook
playbook_id: PB-WIN-001
domain: Windows
version: v1.0
---
# Windows Driver Verifier + KD 生命周期排查

## Trigger
0x50/0xD1/0x7E 或 DOE_UNLOAD_PENDING

## Procedure
按代码位置聚类；开启 Verifier；记录 DriverObject/DeviceObject；跟踪 worker；跟踪 IRP completion；验证 rundown；stop 后确认 ownership 归零。

## Exit Criteria
stop/unload/concurrent I/O 回归无 UAF/IRQL violation，DriverUnload 前 ownership 全归零。

## Source Patterns
- [[PAT-WIN-001]]
- [[PAT-WIN-002]]
- [[PAT-WIN-004]]

# PAT-WIN-008 — Virtual disk bring-up needs protocol compliance before filesystem mount

NTFS mount 之前先验证 virtual disk 的设备枚举和 SCSI 基础命令：INQUIRY 0x83、READ CAPACITY(16)、MODE SENSE(10)、REQUEST SENSE、REPORT LUNS、split read。

[[CASE-WIN-20260901-001]] [[PB-WIN-005]]

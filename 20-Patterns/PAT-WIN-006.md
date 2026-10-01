# PAT-WIN-006 — Section/View/Backing Storage are different lifetimes

section object、view、client handle、backing cache 是不同生命周期实体；handle/view 存在不等于 backing storage 安全。

[[CASE-WIN-20260923-001]] [[PB-WIN-004]]

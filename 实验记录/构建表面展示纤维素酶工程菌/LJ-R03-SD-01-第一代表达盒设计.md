# SD-01 第一代表达盒设计实验结果

## Objectives

确定可由组成型启动子驱动、并可实现表面锚定的融合表达结构，形成三个标准化的表达盒（2026.4.18–5.13）。

## Methods

在 SnapGene 中完成表达盒设计与序列核对：**J23116（Anderson 组成型启动子）– B0034（RBS）– TorA SP（信号肽）– INPNC（BBa_K1933011，已删终止密码子，含 His-tag）– (EAAAK)+(GGGGS) 混合 linker – Δdockerin 密码子优化 Cel48S/Cel9K/Cel5L – B0015（终止子）**；载体为 pCDF-based 质粒（CloDF13 复制子，SmR），宿主 MG1655。

## Result

确定三个表达盒 **INPNC–Cel48S / INPNC–Cel9K / INPNC–Cel5L**，共用调控、锚定与融合策略，差异仅在 cargo。选择 J23116 的原因：组成型表达无需诱导、操作简单，且希望工程菌在接触固体纤维素底物前预先积累一定数量的表面展示酶。两个事后发现值得记录：TorA 与 INPNC 定位机制的兼容性始终未获实验验证；SmR 筛选标记后来被证明无法抑制 WT（SD-07~09），导致第一代体系整体重建为 pACYC / CmR。

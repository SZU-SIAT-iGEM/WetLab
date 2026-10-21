# SDX-09 Ptac-lacO / GFP 报告系列实验结果

## Objectives

验证“组成型 J23116 持续表达造成宿主毒性”的假设：更换为可诱导 Ptac-lacO，并以 GFP 作为小分子量报告 cargo，先独立验证组装方案本身是否可靠，再回到大型纤维素酶（2026.9.29–10.6）。

## Methods

在 pACYCDuet-1 骨架上构建两个 Ptac-lacO 架构的 construct：Ptac-GFP（两条分支、四轮 PCR 获得 GFP 表达盒与线性化载体片段，两片段 Gibson 组装）与 Ptac-INPNC-Cel9K（三片段一步组装）。多轮 PCR 获得各片段条带后完成 Gibson assembly，转化 MG1655（未诱导条件下筛选）。

## Result

GFP 片段多轮 PCR 获得预期条带。转化后 Ptac-GFP 平板获得单个候选克隆，而 Ptac-INPNC-Cel9K 平板未得到克隆；对 GFP 候选克隆的 colony PCR 确认其携带正确的重组 construct。结论：当前 pACYC 骨架、氯霉素筛选与 Gibson 组装流程本身可以正确组装、转化并稳定保留目标质粒；而仅将 J23116 更换为 Ptac-lacO 并不足以解决 INPNC-cellulase 构建失败的问题，限制因素更可能与 surface-display fusion architecture 本身有关（后续转入 Lpp-OmpA 路线，见 SD-13 / DBTL B5）。

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/pacycd-gfp-gibson-assembly.avif)

*Construction strategy of pACYC–Ptac–GFP (Gibson assembly).*

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/pacycduet-1-cel9k-gibson-assembly.avif)

*Construction strategy of pACYCDuet-1–Ptac–INPNC–Cel9K (Gibson assembly).*

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/1002-gfp-r1.avif)

*GFP PCR round 1.*

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/1003-gfp-r2.avif)

*pACYCDuet round 1 and GFP round 2 PCR.*

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/1003-gfp-pacycd-r2.avif)

*pACYCD round 2 PCR.*

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/pacyc-gfp-colony.avif)

*pACYC–Ptac–GFP plate: one candidate colony obtained.*

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/b5-ptac-cel9k.avif)

*pACYC–Ptac–INPNC–Cel9K plate: no colonies obtained.*

![](https://static.igem.wiki/teams/6100/wiki/images-of-wetlab-dbtl/dbtl-b/1006-gfp-colony-1792499672081-2.avif)

*Colony PCR of the Ptac-GFP candidate colony.*

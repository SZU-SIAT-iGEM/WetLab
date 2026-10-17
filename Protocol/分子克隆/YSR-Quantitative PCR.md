# 荧光定量PCR

## 耗材

- cDNA (From reverse transcription PCR)

- 目的基因正向引物 (10 μM)

- 目的基因反向引物 (10 μM)

- 内参基因正向引物 (10 μM)

- 内参基因正向引物 (10 μM)

- 2× SYBR Green qPCR Master Mix

- ddH₂O

- 96孔板

## 仪器

- 荧光定量 PCR 仪

## 实验流程

1. **配制 qPCR 预混液**  
   分别配制目的基因组和内参基因组的 Master Mix，以减少加样误差。

| 组分                            | 目的基因 Master Mix (每反应) | 内参基因 Master Mix (每反应) |
| ----------------------------- | --------------------- | --------------------- |
| cDNA 模板                       | 适量（10-200ng）          | 适量（10-200ng）          |
| 目的基因正向引物 (10 μM)              | 0.4 μl                | -                     |
| 目的基因反向引物 (10 μM)              | 0.4 μl                | -                     |
| 内参基因正向引物 (10 μM)              | -                     | 0.4 μl                |
| 内参基因反向引物 (10 μM)              | -                     | 0.4 μl                |
| 2× SYBR Green qPCR Master Mix | 10 μl                 | 10 μl                 |
| ddH₂O                         | 补至 20 μl              | 补至 20 μl              |

2. **加样**
- 将 20 μl 目的基因反应液加入对应的孔中。

- 将 20 μl 内参基因反应液加入对应的孔中。

- 用光学封板膜密封
3. **设置 qPCR 程序（两步法）**
- 预变性：95℃ 30 sec

- 循环（40 次）：95℃ 5 sec → 60℃ 15–30 sec
4. **熔解曲线分析（Dissociation Stage）**
- 按仪器默认程序运行。

- 关键点： 必须确认目的基因和内参基因的熔解曲线均为单一且尖锐的峰，以确保扩增特异性。
5. **数据分析（2^-ΔΔCt 法）**
- 计算每个样本技术重复中，目的基因与内参基因的平均 Ct 值。

- 计算 ΔCt：ΔCt = 目的基因平均 Ct - 内参基因平均 Ct

- 计算 ΔΔCt：ΔΔCt = 实验组 ΔCt - 对照组 ΔCt

- 计算相对表达量（Fold Change）：相对表达量 = 2^-ΔΔCt

# Quantitative PCR

## Materials

- cDNA (From reverse transcription PCR)

- Target gene forward primer (10 μM)

- Target gene reverse primer (10 μM)

- Reference gene forward primer (10 μM)

- Reference gene reverse primer (10 μM)

- 2× SYBR Green qPCR Master Mix

- ddH₂O

- 96-well plate

## Equipment

- Real-Time PCR System

## Procedure

1. **Prepare qPCR Master Mixes**  
   Prepare the target gene and reference gene Master Mixes separately to minimize pipetting errors.

| Component                             | Target Gene Master Mix (per rxn) | Reference Gene Master Mix (per rxn) |
| ------------------------------------- | -------------------------------- | ----------------------------------- |
| cDNA Template                         | Appropriate amount (10-200 ng)   | Appropriate amount (10-200 ng)      |
| Target gene forward primer (10 μM)    | 0.4 μl                           | -                                   |
| Target gene reverse primer (10 μM)    | 0.4 μl                           | -                                   |
| Reference gene forward primer (10 μM) | -                                | 0.4 μl                              |
| Reference gene reverse primer (10 μM) | -                                | 0.4 μl                              |
| 2× SYBR Green qPCR Master Mix         | 10 μl                            | 10 μl                               |
| ddH₂O                                 | up to 20 μl                      | up to 20 μl                         |

2. **Loading**
- Add 20 μl of the target gene reaction mix to the corresponding wells.

- Add 20 μl of the reference gene reaction mix to the corresponding wells.

- Seal with an optical adhesive film.
3. **Set Up the qPCR Program (Two-step method)**
- Initial denaturation: 95°C for 30 sec

- Cycles (40x): 95°C for 5 sec → 60°C for 15–30 sec
4. **Melt Curve Analysis (Dissociation Stage)**
- Run according to the instrument's default program.

- *Crucial:* Ensure both the target and reference genes show a single, sharp peak to confirm amplification specificity.
5. **Data Analysis (2^-ΔΔCt Method)**
- Calculate the average Ct value of the target gene and reference gene across technical replicates for each sample.

- Calculate ΔCt: ΔCt = Average Ct (Target) - Average Ct (Reference)

- Calculate ΔΔCt: ΔΔCt = ΔCt (Experimental Group) - ΔCt (Control Group)

- Calculate relative expression (Fold Change): Fold Change = 2^-ΔΔCt

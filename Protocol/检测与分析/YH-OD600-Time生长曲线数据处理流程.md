# OD₆₀₀–Time 生长曲线数据处理

## 材料

原始 OD₆₀₀–Time 数据、对应培养条件的无细胞培养基空白（Blank）数据、样品分组及重复孔信息。

## 工具

Excel、Python、R 或 GraphPad Prism。

## Protocol

### 1. 原始数据整理

保留原始数据文件，建立用于后续处理的数据副本。

按照培养时间、菌株、培养条件及重复编号整理 OD₆₀₀ 数据。将时间统一转换为小时（h），优先使用仪器记录的实际测量时间。

区分生物学重复（biological replicates）与技术重复（technical replicates），并明确各样品对应的培养基空白组。

### 2. 培养基空白校正

对于每种培养条件，使用培养基组成和测量条件相匹配的无细胞空白孔进行校正。

若同一培养条件设置多个空白孔，在每个时间点计算其 OD₆₀₀ 中位数：

\[
OD_{\mathrm{blank,median}}(t)
=\operatorname{median}\left\{OD_{\mathrm{blank},1}(t),\ldots,OD_{\mathrm{blank},m}(t)\right\}
\]

其中，\(m\) 为对应培养条件下的空白孔数量。

将每个样品孔的原始 OD₆₀₀ 减去相同时间点的空白中位数：

\[
OD_{\mathrm{corrected},i}(t)=OD_{\mathrm{raw},i}(t)-OD_{\mathrm{blank,median}}(t)
\]

不同培养条件分别使用对应的空白组校正，不混用不同培养基的空白数据。中位数可降低单个异常空白孔对基线估计的影响，但不能消除所有系统误差。每份数据只进行一次空白校正。

保留校正后的负值及异常值并进行检查，不直接删除、截断为零或进行平滑处理。

### 3. 重复数据汇总

对于同一生物学重复内的多个技术重复孔，在每个时间点计算校正后 OD₆₀₀ 的算术平均值：

\[
\overline{OD}_{b}(t)=\frac{1}{n_b}\sum_{i=1}^{n_b}OD_{\mathrm{corrected},b,i}(t)
\]

其中，\(n_b\) 为第 \(b\) 个生物学重复中有效技术孔的数量。

若存在多个独立生物学重复，则以各生物学重复的均值作为独立观测，计算总体均值：

\[
\overline{OD}(t)=\frac{1}{B}\sum_{b=1}^{B}\overline{OD}_b(t)
\]

以及生物学重复间的样本标准差（SD）：

\[
SD(t)=\sqrt{\frac{\sum_{b=1}^{B}[\overline{OD}_b(t)-\overline{OD}(t)]^2}{B-1}}
\]

其中，\(B\) 为独立生物学重复数（计算上述 SD 时 \(B\geq2\)）。

若仅有技术重复、没有多个独立生物学重复，可报告技术孔的 Mean ± SD，但须注明该 SD 表征的是技术孔间变异，不能视为生物学重复间的变异，也不能据此将技术孔作为独立生物学重复进行统计推断。

### 4. 生长曲线绘制

以培养时间（h）为 X 轴，以空白校正后的 OD₆₀₀ 为 Y 轴绘制生长曲线。

- **X-axis:** Time (h)
- **Y-axis:** Blank-corrected OD₆₀₀
- **数据展示:** Mean ± SD（按实验实际重复层级计算并标注）

可使用误差棒或阴影误差带表示 SD。图注注明培养条件、生物学重复数、技术重复数，以及误差棒或阴影所代表的变异层级。

---

# OD₆₀₀–Time Growth Curve Data Processing Protocol

## Materials

Raw OD₆₀₀–time measurements, cell-free medium blank measurements matched to each culture condition, and sample grouping and replicate-well information.

## Tools

Excel, Python, R, or GraphPad Prism.

## Protocol

### 1. Organize the raw data

Preserve the original data file and create a separate copy for processing.

Organize OD₆₀₀ values by cultivation time, strain, culture condition, and replicate identifier. Express time in hours (h), preferably using the actual measurement timestamps recorded by the instrument.

Distinguish biological replicates from technical replicates, and identify the matching cell-free medium blank group for each sample.

### 2. Correct for the medium blank

For each culture condition, use cell-free blank wells with matching medium composition and measurement conditions.

If multiple blank wells are available, calculate the median blank OD₆₀₀ separately at every time point:

\[
OD_{\mathrm{blank,median}}(t)
=\operatorname{median}\left\{OD_{\mathrm{blank},1}(t),\ldots,OD_{\mathrm{blank},m}(t)\right\}
\]

Here, \(m\) denotes the number of blank wells for that culture condition.

Subtract the corresponding time-matched blank median from each individual sample-well reading:

\[
OD_{\mathrm{corrected},i}(t)=OD_{\mathrm{raw},i}(t)-OD_{\mathrm{blank,median}}(t)
\]

Process each medium condition using its own matching blank wells; do not pool blanks from different media. The median reduces the influence of a single anomalous blank reading but does not eliminate systematic measurement errors. Apply blank correction only once.

Preserve and inspect negative or anomalous corrected values; do not automatically discard them, clamp them to zero, or smooth them.

### 3. Summarize replicates

For technical replicate wells derived from the same biological replicate, calculate the arithmetic mean corrected OD₆₀₀ at each time point:

\[
\overline{OD}_{b}(t)=\frac{1}{n_b}\sum_{i=1}^{n_b}OD_{\mathrm{corrected},b,i}(t)
\]

Here, \(n_b\) is the number of valid technical replicate wells for biological replicate \(b\).

If multiple independent biological replicates are available, treat the mean of each biological replicate as one independent observation and calculate the overall mean:

\[
\overline{OD}(t)=\frac{1}{B}\sum_{b=1}^{B}\overline{OD}_b(t)
\]

Calculate the sample standard deviation (SD) across biological replicates:

\[
SD(t)=\sqrt{\frac{\sum_{b=1}^{B}[\overline{OD}_b(t)-\overline{OD}(t)]^2}{B-1}}
\]

Here, \(B\) is the number of independent biological replicates (\(B\geq2\) is required for this SD).

When only technical replicates are available, technical-well Mean ± SD may be reported, but the SD must be explicitly identified as technical variation. Technical wells must not be treated as independent biological replicates for statistical inference.

### 4. Plot growth curves

Plot cultivation time (h) on the X-axis and blank-corrected OD₆₀₀ on the Y-axis.

- **X-axis:** Time (h)
- **Y-axis:** Blank-corrected OD₆₀₀
- **Data presentation:** Mean ± SD, calculated and labeled at the appropriate replicate level

SD may be displayed using error bars or shaded error bands. State the culture conditions, the number of biological and technical replicates, and the level of variation represented by the error bars or bands in the figure legend.

# OD₆₀₀ 生长曲线表观比生长速率分析

## **材料**

24 h 酶标仪原始 OD₆₀₀ 数据（含时间及孔位信息）、对应培养条件下的无细胞培养基空白孔数据、菌株及技术重复孔位信息。

## **工具**

Python 数据分析环境（pandas、NumPy、SciPy）、Excel 或 GraphPad Prism 绘图软件。

## **流程**

1、**整理数据。** 将各孔数据按照培养时间（h）、培养条件、菌株、孔位及技术重复编号进行整理。

2、**校正空白。** 对每种培养条件，在每个采样时间点计算各培养基无细胞空白孔 OD₆₀₀ 的中位数，并从对应培养基实验组下每个技术孔的原始读数中扣除：

\[
OD_{\mathrm{corr},i}(t)=OD_{\mathrm{raw},i}(t)-\operatorname{median}\{OD_{\mathrm{blank},1}(t),OD_{\mathrm{blank},2}(t),OD_{\mathrm{blank},3}(t)\}
\]

空白校正只执行一次。采用中位数能够降低单个空白孔异常读数的影响，但不能完全消除不同孔位之间的背景差异。背景校正对生长速率估计具有重要影响（Atolia et al., 2020）。保留原始数据及校正后的数据以便追溯。

3、**转换数据。** 对校正后大于 0 的 OD₆₀₀ 数据进行自然对数转换：

\[
Y(t)=\ln[OD_{\mathrm{corr}}(t)]
\]

对数转换使指数增长阶段的 OD₆₀₀–时间关系近似呈线性，从而能够通过拟合斜率估计比生长速率（Hall et al., 2014）。校正后小于或等于 0 的数据不参与对数转换，也不添加伪计数代替。

4、**建立滑动窗口。** 对每个技术孔分别遍历连续 6 h 的完整时间窗口，包括 0–6 h、0.25–6.25 h，直至 18–24 h。每个窗口包含 25 个时间点，每条完整曲线共有 73 个候选窗口。仅对具有完整有效数据的窗口进行拟合。

本次采用 6 h 作为探索性窗口长度，以减少短期测量波动对斜率的影响，同时避免使用过长时间范围拟合可能存在的非线性生长过程。该窗口长度为本次分析的预设参数，并非统一的文献标准。

5、**逐窗口拟合。** 以培养时间 \(t\) 为自变量，以 \(\ln OD_{\mathrm{corr}}\) 为因变量，对每个窗口进行含自由截距的普通最小二乘线性回归：

\[
\ln OD_{\mathrm{corr}}(t)=a+\mu_{\mathrm{app},w}t
\]

其中，\(a\) 为回归截距，\(\mu_{\mathrm{app},w}\) 为该窗口的表观比生长速率，单位为 h⁻¹。

记录每个窗口的起止时间、回归斜率、决定系数 \(R^2\)、最低校正 OD₆₀₀、净 OD₆₀₀ 增量及倍数变化。拟合时不强制直线经过原点。利用生长曲线估计增长参数具有成熟的方法学基础，但不同拟合方法及模型可能得到不同的增长参数（Hall et al., 2014; Sprouffske & Wagner, 2016）。

6、**执行质量控制（QC）。** 对每个候选窗口分别检查以下条件：

- **最低校正 OD₆₀₀ ≥ 0.02：** 排除过低 OD 信号，以降低对数转换对测量噪声的放大效应。该阈值属于探索性设定，尚未根据本实验酶标仪的实际检测限进行独立验证。低 OD 数据的可靠性取决于具体仪器和测量条件（Atolia et al., 2020）。
- **线性回归 \(R^2\) ≥ 0.80：** 排除与对数线性关系吻合较差的窗口。该阈值用于评价局部拟合质量，但不能单凭 \(R^2\) 确认细菌处于指数生长期。
- **6 h 净 OD₆₀₀ 增量 ≥ 0.03：** 要求窗口内存在一定的绝对增长幅度，降低微小测量波动对速率估计的影响。该条件可能排除真实但缓慢的增长。
- **6 h 倍数变化 ≥ 1.15：** 要求窗口终点与起点的校正 OD₆₀₀ 比值不低于 1.15，以排除相对增长幅度过小的窗口。
- **最大单步正增量占比 ≤ 0.50：** 将窗口内相邻时间点的正向 OD₆₀₀ 增量相加，计算其中最大单步正增量占全部正增量之和的比例。要求该比例不超过 0.50，以减少单个异常上升点对速率估计的影响。
- **24 h 净 OD₆₀₀ 增量 ≥ 0.03：** 要求该技术孔在整个培养周期内表现出一定的净增长，避免仅凭短期波动报告正向增长速率。

此外，仅保留回归斜率大于 0 的窗口。上述数值阈值均为本次分析采用的探索性筛选条件，其目的在于降低低 OD 噪声、局部异常波动及非线性变化对表观生长速率估计的影响。

7、**筛选并确定表观比生长速率。** 首先保留通过全部质量控制条件的窗口，然后从合格窗口中选择正斜率最大的窗口，将该斜率定义为该技术孔的最大 6 h 表观比生长速率：

\[
\mu_{\mathrm{app,6h,max}}=\max_{w\in W_{\mathrm{QC}}}(\mu_{\mathrm{app},w})
\]

其中 \(W_{\mathrm{QC}}\) 为通过质量筛选的窗口集合。若某个技术孔不存在合格窗口，则其速率标记为 NA，而不赋值为 0。NA 表示未获得满足当前质量标准的可靠速率估计，并不一定代表没有生长。

8、**汇总技术重复并作图。** 对每株菌在每种碳源条件下的合格技术孔分别计算最大 6 h 表观比生长速率，再计算算术平均值及样本标准差（Mean ± SD），同时记录有效技术孔数量 \(n_{\mathrm{tech}}\)。

柱状图以合格技术孔的速率均值作为柱高，误差棒表示技术孔间 SD，散点表示各技术孔的独立计算结果。如果只有一个技术孔通过 QC，则只报告该孔的速率，不计算 SD。未获得合格速率估计的菌株标记为 NA。

---

# Apparent Specific Growth Rate Analysis of OD₆₀₀ Growth Curves

## **Materials**

Raw OD₆₀₀ measurements from a 24 h microplate-reader assay (including time points and well positions), cell-free medium blank measurements for each culture condition, and strain and technical-replicate well information.

## **Tools**

Python data analysis environment (pandas, NumPy, SciPy), and Excel or GraphPad Prism for plotting.

## **Protocol**

1. **Organize the data.** Organize the measurements from each well by cultivation time (h), culture condition, strain, well position, and technical replicate number.

2. **Perform blank correction.** At each sampling time point, calculate the median OD₆₀₀ of the cell-free medium blank wells for each culture condition. Subtract this median from the raw reading of each corresponding experimental well:

\[
OD_{\mathrm{corr},i}(t)=OD_{\mathrm{raw},i}(t)-\operatorname{median}\{OD_{\mathrm{blank},1}(t),OD_{\mathrm{blank},2}(t),OD_{\mathrm{blank},3}(t)\}
\]

Perform blank correction only once. Using the median reduces the influence of anomalous readings from individual blank wells, but does not completely remove background differences among well positions. Background correction can substantially affect growth-rate estimates (Atolia et al., 2020). Retain both raw and blank-corrected data for traceability.

3. **Transform the data.** Apply the natural logarithm to blank-corrected OD₆₀₀ values greater than zero:

\[
Y(t)=\ln[OD_{\mathrm{corr}}(t)]
\]

Log transformation makes the relationship between OD₆₀₀ and time approximately linear during exponential growth, allowing the specific growth rate to be estimated from the fitted slope (Hall et al., 2014). Do not log-transform values equal to or below zero or replace them with arbitrary pseudocounts.

4. **Construct sliding windows.** For each technical replicate well, examine all complete, consecutive 6 h windows, from 0–6 h and 0.25–6.25 h through 18–24 h. Each window contains 25 time points, resulting in 73 candidate windows per complete growth curve. Fit only windows with a complete set of valid observations.

A 6 h window was selected as an exploratory analysis parameter to reduce the influence of short-term measurement fluctuations while avoiding potentially nonlinear behavior over excessively long periods. This window length is specific to the present analysis and is not a universally prescribed literature standard.

5. **Fit each window.** For each window, perform ordinary least-squares linear regression with cultivation time \(t\) as the independent variable and \(\ln OD_{\mathrm{corr}}\) as the dependent variable, allowing the intercept to vary freely:

\[
\ln OD_{\mathrm{corr}}(t)=a+\mu_{\mathrm{app},w}t
\]

Here, \(a\) is the regression intercept and \(\mu_{\mathrm{app},w}\) is the apparent specific growth rate for the window, expressed in h⁻¹.

Record the start and end times, fitted slope, coefficient of determination \(R^2\), minimum blank-corrected OD₆₀₀, net OD₆₀₀ increase, and fold change for each window. Do not force the fitted line through the origin. Extracting growth parameters from growth curves is well established, although different fitting methods and models may produce different estimates (Hall et al., 2014; Sprouffske & Wagner, 2016).

6. **Apply quality control (QC).** Evaluate each candidate window against the following criteria:

- **Minimum blank-corrected OD₆₀₀ ≥ 0.02:** Exclude very low OD signals to reduce amplification of measurement noise after log transformation. This exploratory threshold has not been independently validated against the detection limit of the microplate reader used. Reliability at low OD depends on the instrument and measurement conditions (Atolia et al., 2020).
- **Linear regression \(R^2\) ≥ 0.80:** Exclude windows with poor agreement with a log-linear trend. This criterion evaluates local fit quality, but \(R^2\) alone cannot establish the presence of exponential growth.
- **Net OD₆₀₀ increase over 6 h ≥ 0.03:** Require a minimum absolute increase within the window to reduce the influence of small measurement fluctuations. This criterion may exclude genuine but slow growth.
- **6 h fold change ≥ 1.15:** Require the ratio of the final to initial blank-corrected OD₆₀₀ in the window to be at least 1.15, excluding windows with negligible relative growth.
- **Largest positive single-step increment fraction ≤ 0.50:** Sum all positive OD₆₀₀ increments between adjacent time points in the window and divide the largest positive increment by that sum. Require the resulting fraction to be no greater than 0.50 to reduce the influence of a single anomalous upward jump.
- **Net OD₆₀₀ increase over 24 h ≥ 0.03:** Require a minimum net increase over the full culture period to avoid reporting a positive growth rate based only on short-term fluctuations.

Additionally, retain only windows with positive regression slopes. All numerical QC thresholds are exploratory criteria adopted for the present analysis. They are intended to reduce the effects of low-OD noise, local anomalous fluctuations, and nonlinear growth on apparent growth-rate estimates.

7. **Select the apparent specific growth rate.** First retain all windows that pass every QC criterion. Then select the largest positive slope among those windows as the maximum 6 h apparent specific growth rate for the technical replicate well:

\[
\mu_{\mathrm{app,6h,max}}=\max_{w\in W_{\mathrm{QC}}}(\mu_{\mathrm{app},w})
\]

Here, \(W_{\mathrm{QC}}\) denotes the set of windows passing QC. If no window qualifies for a technical replicate, record its rate as NA rather than zero. NA indicates that no rate estimate met the current QC criteria; it does not necessarily mean that growth was absent.

8. **Summarize technical replicates and plot the results.** For each strain under each carbon-source condition, obtain the maximum 6 h apparent specific growth rate separately for every qualified technical replicate well. Calculate the arithmetic mean and sample standard deviation (Mean ± SD), and record the number of valid technical replicates \(n_{\mathrm{tech}}\).

In bar plots, use the mean of the qualified technical-well rate estimates as the bar height, the between-well SD as the error bar, and individual points to represent the independently calculated rates for each technical well. If only one technical well passes QC, report its rate without calculating SD. Mark strains without a qualified rate estimate as NA.

## Reference

Atolia, E., Cesar, S., Arjes, H. A., Rajendram, M., Shi, H., Knapp, B. D., Khare, S., Aranda-Díaz, A., Lenski, R. E., & Huang, K. C. (2020). Environmental and physiological factors affecting high-throughput measurements of bacterial growth. *mBio, 11*(5), e01378-20. https://doi.org/10.1128/mBio.01378-20

Hall, B. G., Acar, H., Nandipati, A., & Barlow, M. (2014). Growth rates made easy. *Molecular Biology and Evolution, 31*(1), 232–238. https://doi.org/10.1093/molbev/mst187

Sprouffske, K., & Wagner, A. (2016). Growthcurver: An R package for obtaining interpretable metrics from microbial growth curves. *BMC Bioinformatics, 17*, Article 172. https://doi.org/10.1186/s12859-016-1016-7

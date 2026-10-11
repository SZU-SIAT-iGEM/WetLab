

> 依据文献整理（原始出处见文末引用），2026-10-02
> 方法名称：Soft agar (swim plate) chemotaxis assay / 半固体琼脂趋化环实验

---

## 1. 实验原理

将趋化野生型 E. coli 点种于含**可代谢糖类吸引剂**的低浓度琼脂（0.25–0.35% w/v）平板中心。细菌生长消耗中心区域的糖，形成由内向外的浓度梯度；细菌沿梯度趋糖游动，形成向外扩张的**趋化环（ring）**。非趋化突变体（如 ΔcheA、ΔcheY）只能随机扩散，形成弥散菌斑、无清晰环。

- 糖类通过 9 种化学感受器被识别（半乳糖、葡萄糖、麦芽糖、核糖、甘露醇、山梨醇、海藻糖、果糖、N-乙酰葡萄糖胺感受器）
- **关键**：除葡萄糖感受器外，其余糖感受器均**可诱导**——接种前培养必须含同种糖作诱导物，否则平板上不出环（Adler 1973 JGM; Adler/Hazelbauer/Dahl 1973 JB）
- 乳糖本身不吸引，需先被 β-半乳糖苷酶水解为葡萄糖+半乳糖后才表现出趋化

---

## 2. 试剂配方（明确成分）

### 2.1 体系 A：限定盐培养基软琼脂板（推荐用于糖类趋化，经典 Adler 体系）

富培养基（LB/胰蛋白胨）本身含丝氨酸/天冬氨酸等强吸引剂，会掩盖糖信号，**测糖趋化必须用限定培养基**。

**盐溶液（Kaiser & Hogness 1960 salts，per L 蒸馏水）**

| 成分 | 用量 |
|---|---|
| K₂HPO₄ | 11.2 g |
| KH₂PO₄ | 4.8 g |
| (NH₄)₂SO₄ | 2.0 g |
| MgSO₄·7H₂O | 0.25 g |
| Fe₂(SO₄)₃ | 0.5 mg |

**磷酸钾缓冲液替代法**（手头有 0.2 M potassium phosphate buffer 母液时，两种磷酸盐可整组替换）：

| 成分 | 每升培养基用量 |
|---|---|
| 0.2 M 磷酸钾缓冲液母液（**pH 7.4**，即 K₂HPO₄/KH₂PO₄ 缓冲对） | **500 mL**（终浓度：总磷酸盐 100 mM，K⁺ ~161 mM，与原配方等价） |
| (NH₄)₂SO₄ | 2.0 g |
| MgSO₄·7H₂O | 0.25 g |
| Fe₂(SO₄)₃ | 0.5 mg |
| 蒸馏水 | 补至 1 L |

- 母液若为 pH 7.0（常见商品规格），建议先用 K₂HPO₄ 调至 7.4：原配方两种盐摩尔比 1.82:1 对应 pH 7.46，起始 pH 偏低会影响趋化表型（pH 本身是趋化信号）
- 母液标签须只含 K₂HPO₄ + KH₂PO₄（或 KH₂PO₄ + KOH）；若含 NaCl 则为 PBS，**不可用**（P 少 8.4 倍、K⁺ 少 36 倍）

**铺板培养基（per L）**

| 成分 | 用量 | 处理 |
|---|---|---|
| 上述盐溶液 | 1× | 与琼脂同锅高压 |
| Bacto agar（或 Noble agar） | **3.0 g（0.3%）**，可用范围 2.5–3.5 g | 高压 121 °C 20 min |
| 目标糖（D-半乳糖 / D-核糖 / 麦芽糖 / D-葡萄糖 / D-果糖等） | **5 g（0.5%）**，建议试 0.2–0.5% | **过滤除菌（0.22 µm）**，灭菌后待培养基冷至 ~50 °C 时无菌加入 |

- 糖不随培养基高压（避免焦糖化/降解），过滤除菌后加入
- 倒板前培养基 pH 应为 ~7.0–7.3（Croze 2011 报告终 pH 7.3±0.1）
- 每 100 mm 培养皿倒 **20–25 mL**（Croze 用 58 mL 铺 10 mm 厚，一般实验室 20–25 mL 即 ~3–4 mm 厚已足够）
- 现配现用最好；swim 板可室温避光存放数天（JoVE 61364 建议 16 h 内使用，最长 1–2 天）

### 2.2 体系 B：胰蛋白胨软琼脂板 + 外加糖（supplemented soft agar assay，Sanders 2013）

用于比较"加糖 vs 不加糖"对迁移速度的影响（吸引剂使整体迁移**变慢**，因梯度形成需要更长时间）：

| 成分              | 用量（per L）                            |
| --------------- | ------------------------------------ |
| Bacto tryptone  | 10 g（1%）                             |
| NaCl            | 5 g（0.5%）                            |
| Bacto agar (BD) | **3.5 g（0.35%）**                     |
| 待测糖（过滤除菌）       | 高压冷却至 ~50 °C 后无菌加入，浓度建议 0.1–10 mM 起试 |

（Wolfe & Berg 1989 原配方为 0.35% agar + 1% tryptone + 0.5% NaCl；Sanders 2013 按此对 E. coli 做 supplemented assay，丝氨酸呈剂量依赖性减慢迁移）

### 2.3 细菌培养

| 项目 | 条件 |
|---|---|
| 菌株 | 趋化野生型 E. coli K-12：**RP437**（经典趋化 WT）或 MG1655/Motile 株；阴性对照用 ΔcheY 或 ΔcheA 等渗突变体（如 RP8611 Δtsr Δtar-tap Δtrg 或 cheY::kan） |
| 培养基 | 体系 A 用：同一盐培养基 + **同种糖 0.4–0.5%**（诱导感受器）；体系 B 用：LB 或 1% tryptone broth |
| 温度 | **30 °C**（37 °C 鞭毛合成差，趋化表型弱） |
| 摇床 | 200 rpm |
| 接种流程 | 单克隆 → 过夜培养 → 1:100 转接 → 培养至**晚对数期 OD₆₀₀ = 0.8–1.3**（Croze 2011）或 OD₆₀₀ ≈ 0.6（JoVE 61364） |
| 点种前稀释 | 用同种新鲜培养基稀释至 OD₆₀₀ ≈ 0.1（≈10⁸ CFU/mL） |

---

## 3. 操作步骤

1. **铺板**：糖过滤除菌；含盐+琼脂的基础培养基高压后冷至 ~50 °C，无菌加糖混匀，每 100 mm 皿倒 20–25 mL，水平静置凝固 ≥1 h（盖子盖好）。
2. **接种**：用 2–10 µL 移液器吸取 **≤2–6 µL** 稀释菌液（OD₆₀₀≈0.1），将枪头轻插入板中心琼脂内约 2–3 mm，缓缓打出菌液（Croze 2011 用 ≤1 µL 液滴；JoVE 61364 用 6 µL 轻插入琼脂打出）。
3. **吸收**：室温静置 ~30–60 min 让菌液被琼脂吸收（可选：Croze 做法是在菌点吸收后加 ~1.5 mm 无菌矿物油层防蒸发，长时程拍摄用）。
4. **培养**：平板**正置**（勿倒置，防止冷凝水滴落破坏环），**30–32 °C** 培养。
5. **观察与测量**：
   - 体系 A（限定盐+糖板）：**8–24 h** 内出现清晰趋化环；野生型 8–10 h 可扩至大半个板
   - 体系 B（tryptone 板）：~8 h（30 °C）可见外环（丝氨酸 taxis）+ 内环（天冬氨酸 taxis）的双环经典图案；外加糖板按 Sanders 2013 培养 **20 h** 后测迁移直径
   - 用直尺/卡尺测**环直径**（mm），每个处理 ≥3 个平行板；也可定时拍照用 ImageJ 定量环半径随时间变化
6. **判读**：
   - WT + 糖板 → 清晰同心环（趋化阳性）
   - che 突变体 → 接种点周围均匀弥散云，无环（验证体系特异性）
   - 无糖盐板 → 无环或极弱（阴性对照）
   - 体系 B 逻辑：外加吸引剂浓度越高、迁移速度越慢（剂量-速度曲线可半定量）

---

## 4. 关键参数与陷阱（文献依据）

| 参数 | 要点 | 出处 |
|---|---|---|
| 琼脂浓度 | **≤0.35%** 才有清晰趋化环；0.35% 时环变宽为生长/扩散带；0.4–0.5% 前沿失稳、不贯穿胶深；<0.25% 时前沿速度对琼脂浓度不敏感。推荐 0.25–0.3% | Croze et al. 2011 Biophys J |
| 培养温度 | 30 °C（±0.5），不要 37 °C | Adler 系列; JoVE 61364; Croze 2011 |
| 感受器诱导 | 半乳糖/麦芽糖/核糖 taxis 是诱导型的，**接种前培养液中必须含同种糖** | Adler 1973 JGM |
| 糖的灭菌 | 糖过滤除菌、勿高压 | Adler 1973 JGM（甘油单独高压的处理逻辑同理） |
| 琼脂品牌 | 不同品牌琼脂杂质/硬度不同会影响 swarm 与趋化（Eiken vs Difco）；尽量固定同一品牌同一货号 | JoVE 61364 |
| 湿度 | 环境湿度影响平板表面状态，培养箱内放湿盒或尽快使用新鲜板 | JoVE 61364 |
| 平板正置 | 倒置培养冷凝水会破坏环 | 常规微生物操作 |
| 测量时间窗 | 环会融合/弥散，需在固定时间点测量并拍照存档 | Sanders 2013 (20 h); JoVE 61364 (8–10 h WT 铺满板) |

---

## 5. 常用糖类吸引剂一览（阈值，饱和浓度量级）

来自 Adler 1973/1975（阈值 = 引发趋化反应的最低浓度）：

| 糖 | 感受器 | 阈值（~M） |
|---|---|---|
| D-半乳糖 | 半乳糖感受器（GalBP 为识别组分） | 1×10⁻⁶ |
| D-葡萄糖 | 葡萄糖感受器（PTS 相关，组成型）/半乳糖感受器亦识别 | 3×10⁻⁶（葡萄糖感受器）；1×10⁻⁶（半乳糖感受器交叉） |
| 麦芽糖 | 麦芽糖感受器（MBP 为识别组分） | 3×10⁻⁶ |
| D-核糖 | 核糖感受器（RBP 为识别组分） | 7×10⁻⁶ |
| D-甘露醇 | 甘露醇感受器 | 7×10⁻⁶ |
| D-山梨醇 | 山梨醇感受器 | 1×10⁻⁵ |
| 海藻糖 | 海藻糖感受器 | 6×10⁻⁶ |
| D-果糖、D-岩藻糖、6-脱氧葡萄糖、N-乙酰葡萄糖胺、半乳糖醇、葡萄糖胺、乳糖（需水解）、α-D-葡萄糖-1-磷酸、甲基-β-D-半乳糖苷、甲基-β-D-葡萄糖苷 | 各自对应感受器 | ≤10⁻⁵（均为有效吸引剂） |

> 提示：平板中糖是能量源，浓度（mM–% 级）远高于感受阈值（µM 级）；梯度由细菌代谢消耗动态形成，不需按阈值配板。

---

## 6. 试剂采购清单（示例）

| 试剂 | 规格建议 |
|---|---|
| K₂HPO₄、KH₂PO₄、(NH₄)₂SO₄、MgSO₄·7H₂O、Fe₂(SO₄)₃（或 FeSO₄·7H₂O 替代） | 分析纯，Sigma/国药 |
| Bacto Agar（BD 214010）或 Noble Agar（Difco） | 微生物级 |
| D-半乳糖、D-核糖、麦芽糖、D-葡萄糖、D-果糖等 | ≥99%，Sigma |
| Bacto Tryptone（BD 211705）、NaCl | 体系 B 用 |
| 0.22 µm 滤器 | 糖液除菌 |
| 100×15 mm 培养皿 | — |

---

## 7. 参考文献

1. **Adler J.** Chemotaxis in bacteria. *Science* 1966;153:708–716. PMID: 4957395 —— 平板法（plate method）原始文献，半固体琼脂中趋化环概念
2. **Adler J.** A method for measuring chemotaxis and use of the method to determine optimum conditions for chemotaxis by *Escherichia coli*. *J Gen Microbiol* 1973;74:77–91. PMID: 4632978 —— 限定盐培养基确切配方（Kaiser-Hogness salts + 甘油 5 g/L；半乳糖替换甘油）、诱导性 taxis 需诱导物
3. **Adler J, Hazelbauer GL, Dahl MM.** Chemotaxis toward sugars in *Escherichia coli*. *J Bacteriol* 1973;115:824–847. PMID: 4580570, PMC246327 —— 糖类吸引剂全谱系、9 种糖感受器、阈值
4. **Adler J.** Chemotaxis in bacteria. *Annu Rev Microbiol* 1975;29:627–656. PMID: 772314 —— 平板法/毛细管法综述，感受器-配体阈值表
5. **Wolfe AJ, Berg HC.** Migration of bacteria in semisolid agar. *Proc Natl Acad Sci USA* 1989;86:6973–6977 —— tryptone 软琼脂板经典配方（1% tryptone + 0.5% NaCl + 0.35% agar）
6. **Sanders LM, Andermann TM, Ottemann KM.** A supplemented soft agar chemotaxis assay demonstrates the *Helicobacter pylori* chemotactic response to zinc and nickel. *Microbiology* 2013;159:46–57. PMID: 23139399, **PMC3542728（开放获取）** —— supplemented soft agar assay：E. coli 板配方、外加吸引剂减慢迁移的剂量效应、20 h 测量
7. **Croze OA, Ferguson GP, Cates ME, Poon WCK.** Migration of chemotactic bacteria in soft agar: role of gel concentration. *Biophys J* 2011;101:525–534. PMID: 21806920, **PMC3145277（开放获取）** —— 琼脂浓度 0.15–0.5% 系统研究、点种/矿物油/拍摄定量细节
8. **Nandakumar R, et al. (JoVE)** Investigating flagella-driven motility in *E. coli*. *J Vis Exp* 2020, e61364. doi:10.3791/61364 —— 软琼脂板操作流程（0.3% agar，25 mL/板，6 µL 接种，30 °C）
9. University of Utah Parkinson Lab, *E. coli chemotaxis* 项目页（chemotaxis.biology.utah.edu）—— 软琼脂板双环（丝氨酸环+天冬氨酸环）图解

---

*注：Adler 1966 Science 与 Adler 1975 综述为付费/扫描件，其平板细节经由 PubMed 摘要、PMC 开放全文（PMC3542728、PMC3145277、PMC246327）及 Adler 1973 JGM 摘要交叉核实；Fe₂(SO₄)₃ 0.5 mg/L 按 Adler 1973 JGM 摘要原文照录，若缺货可用等摩尔 FeSO₄·7H₂O 替代并自行验证生长。*

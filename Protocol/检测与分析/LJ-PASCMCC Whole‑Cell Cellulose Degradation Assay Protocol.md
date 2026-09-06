## PASC/MCC 整细胞纤维素降解实验 Protocol

本方案用于评价**表达或表面展示纤维素酶的大肠杆菌整细胞**对两类纤维素底物的降解能力。实验分为有氮源的菌体培养/诱导，以及洗涤后的短时无生长酶解反应两部分。

- **PASC（phosphoric acid-swollen cellulose，磷酸膨润纤维素）**：经磷酸处理后结晶度降低、可及性高，更适合检测内切葡聚糖酶等对无定形纤维素的初步降解能力。
- **MCC（microcrystalline cellulose，微晶纤维素）**：本实验以 MCC 作为结晶纤维素底物；若使用 Avicel，将其视为 MCC 的商品来源，并记录具体型号，不将二者作为不同底物比较。
------

## 一、实验目的

1. 将购买的微晶纤维素制备为 PASC，建立可重复的无定形/低结晶度纤维素底物。
2. 比较工程化大肠杆菌整细胞对 PASC 与 MCC 的降解能力。
3. 采用 **DNS 还原糖法**定量反应上清中的还原糖，以葡萄糖当量表示纤维素降解产物。
4. 通过“无细胞底物对照、无底物细胞对照、失活细胞对照”等，排除培养基残留、菌体背景和底物自身背景造成的假阳性。

------

## 二、实验原理

纤维素酶作用于纤维素后，可释放葡萄糖、纤维二糖及可溶性寡糖等具有还原性的产物。BC0235 为 Solarbio 还原糖含量检测试剂盒（微量法）；按盒内说明书显色后在 540 nm 测定吸光度，并用盒内葡萄糖标准品标准曲线换算为还原糖浓度（葡萄糖当量）。[3][4]

PASC 是将 MCC 在浓磷酸中膨润、再经水洗制得的纤维素底物。该过程会降低有序结构并提高酶可及性，因此 PASC 通常比 MCC 更易被纤维素酶降解。[1][2]

------

## 三、实验耗材与仪器

### 1. 试剂与耗材

| 类别       | 名称                                            | 规格/建议                                                    | 用途                                   |
| ---------- | ----------------------------------------------- | ------------------------------------------------------------ | -------------------------------------- |
| 底物       | 微晶纤维素（MCC；Avicel 仅作为商品名记录）       | 记录供应商、货号和型号                                       | 制备 PASC；作为结晶纤维素底物          |
| PASC 制备  | 磷酸                                            | 85%（w/w）浓磷酸                                             | 使微晶纤维素膨润                       |
| 反应缓冲液 | Sodium acetate buffer                           | 50 mM，pH 5.0；可按目标酶最适 pH 调整                        | 整细胞降解反应缓冲液                   |
| 反应缓冲液 | 冰醋酸、无水乙酸钠                              | 分析纯                                                       | 配制乙酸钠缓冲液                       |
| 洗涤液     | 无菌去离子水/超纯水                             | —                                                            | PASC 洗涤、菌体洗涤                    |
| 菌体       | 待测工程化大肠杆菌整细胞                        | 诱导表达完成后的菌液                                         | 纤维素酶来源                           |
| DNS 定量   | Solarbio BC0235 还原糖含量检测试剂盒（微量法）  | 按试剂盒批次说明书配制和操作                                 | 还原糖检测                             |
| 标准品     | 葡萄糖标准品                                    | 试剂盒自带或分析纯 D-glucose                                 | 建立标准曲线                           |
| 对照菌     | 阴性对照菌                                      | 空载体菌株、未诱导菌株或不表达纤维素酶菌株                   | 排除宿主和载体背景                     |
| 离心耗材   | 1.5/2.0 mL EP 管、15/50 mL 离心管               | 耐离心                                                       | 反应和样品处理                         |
| 其他       | 移液器吸头、封口膜、一次性手套、pH 试纸或 pH 计 | —                                                            | 常规操作                               |
| 可选       | 葡萄糖氧化酶/己糖激酶法试剂                     | —                                                            | 若需区分葡萄糖与总还原糖，可作补充检测 |

### 2. 仪器

| 仪器               | 用途                           |
| ------------------ | ------------------------------ |
| 台式高速冷冻离心机 | 菌体收集、反应液澄清           |
| 恒温振荡器         | 整细胞-底物反应                |
| 分光光度计或酶标仪 | 测定菌液 OD600、DNS 显色 OD 值 |
| 水浴锅或金属浴     | DNS 显色反应                   |
| 涡旋振荡器         | 重悬底物及菌体                 |
| 分析天平           | 称取微晶纤维素                 |
| 磁力搅拌器         | PASC 制备过程中的混匀          |
| 通风橱             | 操作 85% 磷酸时必须使用        |
| 烘箱               | 测定 PASC 悬液的实际干物质浓度 |

------

## 四、溶液配制

### 1. 50 mM Sodium acetate buffer，pH 5.0

建议作为首次整细胞纤维素酶检测的默认反应缓冲液。若你的纤维素酶来源已知，或前期结果显示最适 pH 不在 5.0 附近，应以该酶的最适 pH 为准重新优化。

- 配制 50 mM 乙酸钠溶液；
- 用冰醋酸调节至 pH 5.0；
- 高压灭菌或 0.22 μm 过滤除菌；
- 4°C 保存。

> **不建议用 PBS 作为默认反应液。**PBS 的 pH 通常接近中性，而多数真菌来源或常用工程化纤维素酶在弱酸性条件下活性更高；更重要的是，定量反应前必须将菌体从培养基中洗净，以避免培养基中的蛋白胨、酵母粉、糖类或其他还原性组分干扰 DNS 检测。

------

# 五、PASC 自制步骤

## 1. PASC 制备条件

以下配方以 **1.0 g 微晶纤维素**为例，最终可获得足量 PASC 悬液用于多个平行实验。

| 项目              | 推荐条件                           |
| ----------------- | ---------------------------------- |
| 起始底物          | 微晶纤维素 1.0 g                   |
| 磷酸浓度          | 85%（w/w）                         |
| 磷酸用量          | 10 mL                              |
| 反应温度          | 0–4°C                              |
| 膨润时间          | 45–60 min                          |
| 沉淀/洗涤离心条件 | 8,000–10,000 × g，10 min，4°C      |
| 最终底物储备液    | 建议配成 2.0%（w/v，以干重计）PASC |
| 保存条件          | 4°C，建议 1 周内使用；尽量现制现用 |

------

## 2. PASC 制备

### Step 1：预冷与安全准备

1. 提前将 85% 磷酸、去离子水、玻璃烧杯、搅拌子和离心管置于冰上或 4°C 环境预冷。
2. 在**通风橱**内完成浓磷酸相关操作。
3. 穿戴实验服、护目镜/面屏和耐酸手套。

> 85% 磷酸具有强腐蚀性。若发生皮肤接触，应立即用大量流动清水冲洗；如有眼部暴露或持续不适，应按实验室化学品安全规范处理并就医。

### Step 2：微晶纤维素磷酸膨润

1. 在冰浴中的玻璃烧杯内加入 **10 mL 85% 磷酸**。
2. 将 **1.0 g 微晶纤维素**分多次、缓慢加入磷酸中，同时持续磁力搅拌。
3. 在 **0–4°C** 下持续搅拌 **45–60 min**，直至形成均一、黏稠的乳白色至半透明悬液/凝胶。

**注意：**

- 纤维素必须分批加入，避免形成无法分散的大团块。
- 不建议在室温下长时间处理，也不建议超过约 1 h；过度酸处理会导致纤维素发生明显酸水解，改变底物性质。
- 不同批次 MCC 的粒径和晶型不同，最终 PASC 的状态可能略有差异；应记录原料型号和处理时间。

### Step 3：终止反应并沉淀 PASC

1. 预先在较大烧杯中加入 **100 mL 冰冷去离子水**，并进行搅拌。
2. 将磷酸-纤维素悬液**缓慢倒入冰冷水中**，边倒边剧烈搅拌。
3. 混匀后，转移至离心管中。
4. 以 **8,000–10,000 × g，4°C，离心 10 min**，弃去上清液。

> 应将“含有纤维素的酸性悬液”缓慢加入大量水中，而不是将水直接倒入浓酸体系中；操作时全程在通风橱内进行。

### Step 4：反复洗涤至近中性

1. 向沉淀中加入足量去离子水，充分涡旋或温和吹打重悬。
2. 再次以 **8,000–10,000 × g，4°C，离心 10 min**。
3. 重复洗涤 **4–6 次**，每次弃上清后记录上清液 pH。
4. 当最终上清液 pH 达到 **5.5–7.0**，即可认为残余磷酸已基本去除。

**关键注意事项：**

- **不要直接用 NaOH 中和。**直接加碱会产生盐分并改变底物体系，后续可能影响酶反应和 DNS 检测；采用反复水洗更适合制备酶学实验用 PASC。
- 洗涤不充分时，残留酸会降低反应体系 pH，造成菌体失活、酶活偏低或不同批次之间不可比。
- PASC 容易形成凝胶状团块，应每次彻底重悬，保证洗涤充分。

### Step 5：测定 PASC 干物质浓度并配制储备液

由于洗涤后的 PASC 为悬液，不能仅按总体积估算其实际浓度；建议通过干重法校准。

1. 取一个预先称重的铝盒或耐热称量皿，记录空皿质量 M0M_0M0。
2. 充分混匀 PASC 悬液后，取 **1.0 mL** 加入称量皿，记录湿重。
3. 置于 **105°C 烘箱**中干燥至恒重，记录干燥后总质量 M1M_1M1。
4. PASC 干物质浓度计算：

PASC 浓度（mg/mL） = (M1 - M0) × 1000 / 取样体积（mL）

1. 用去离子水或反应缓冲液将 PASC 调整为 **2.0%（w/v，即 20 mg/mL）**储备液。

例如，若 PASC 总干物质量为 0.80 g，则将其最终补足至：

0.80 g ÷ 0.02 g/mL = 40 mL

即可获得 2.0% PASC 储备液。

### Step 6：PASC 保存

- 建议将 PASC 保存于 4°C，使用前充分涡旋或匀浆。
- 最好在 **1 周内使用**；如果发现浑浊异常、异味或污染迹象，应重新制备。
- 若必须长期保存，建议先验证保存方式不会显著影响其可及性和酶解性能。
- 不建议未经验证就对最终 PASC 悬液高压灭菌，因为高温处理可能改变底物分散状态和结晶结构，从而影响批间可比性。

------

# 六、整细胞纤维素降解实验

## 1. 实验设计

建议至少设置下列组别，每组做 **3 个生物学重复**；每个生物学重复可做 2–3 个技术复孔。

| 组别             | 菌体                         | 底物           | 用途                            |
| ---------------- | ---------------------------- | -------------- | ------------------------------- |
| PASC-实验组      | 表达纤维素酶的整细胞         | PASC           | 检测对无定形/膨润纤维素的降解   |
| MCC-实验组       | 表达纤维素酶的整细胞         | 微晶纤维素/MCC | 检测对结晶纤维素的降解          |
| 底物空白         | 无菌缓冲液                   | PASC 或 MCC    | 扣除底物自身或试剂背景          |
| 细胞空白         | 表达纤维素酶的整细胞         | 不加底物       | 扣除菌体释放物及菌体残留背景    |
| 阴性菌对照       | 空载体/未诱导/不表达酶的菌体 | PASC 或 MCC    | 排除宿主菌非特异背景            |
| 失活细胞对照     | 热失活待测菌体               | PASC 或 MCC    | 排除非酶学吸附或背景释放        |
| BC0235 方法学对照 | 葡萄糖标准品                 | 不加底物       | 验证 BC0235 显色和标准曲线是否正常 |

------

## 2. 菌体制备

### Step 1：培养与诱导

按你的表达载体、诱导剂及目标蛋白表达体系，在含氮培养基中培养和诱导。推荐使用 LB；若需定义培养基，则使用含 NH4Cl 或其他经验证氮源的 M9。MCC/PASC 不是合适的氮源，不能替代培养基中的氮源。

培养基只用于菌体扩增和诱导，不得直接带入后续酶解反应。建议记录：

- 宿主菌株；
- 质粒名称；
- 诱导剂及其浓度；
- 诱导时 OD600；
- 诱导温度和时长；
- 是否为胞内表达、周质表达、分泌表达或细胞表面展示。

> 关于无氮源条件：洗涤后的菌体在 1 mL 体系中进行 0–120 min 的短时酶解时，实验目的不是培养细胞，因此不需要额外补氮源；但不能据此判断细胞能在无氮源条件下生长。若要测试 MCC/PASC 是否能支持生长，必须另设生长实验，在无碳源的无机盐基础上补充 NH4Cl 等氮源，并以 MCC/PASC 作为待测碳源；同时设置葡萄糖阳性对照和无碳源阴性对照。

> 若纤维素酶位于胞内，完整大肠杆菌通常难以直接接触底物，整细胞活性可能很低；本方案尤其适合**表面展示型、分泌型或外膜定位型纤维素酶系统**。

### Step 2：收集并洗涤菌体

1. 取诱导结束的菌液，记录 OD600。
2. 以 **4,000–6,000 × g，4°C，离心 8–10 min** 收集菌体。
3. 弃去上清。
4. 用预冷的 **50 mM sodium acetate buffer，pH 5.0**重悬菌体。
5. 再次离心并重悬，重复洗涤 **2 次**。
6. 最终将菌体重悬于同一反应缓冲液中，调节至 **OD600统一** 的菌悬液备用。

### 为什么必须洗菌？

培养基中的蛋白胨、酵母粉、糖类及代谢产物可能带来 DNS 反应背景；同时，培养基残余会使各实验组的 pH、离子强度和底物状态不一致。

------

## 3. 底物工作液制备

### PASC 工作液

将 2.0% PASC 储备液用反应缓冲液稀释为 **0.625%（w/v）**工作液。

### MCC 工作液

称取 MCC，以反应缓冲液配制为 **0.625%（w/v）**工作液。使用前及每次取样前均需充分涡旋，避免颗粒沉降造成底物浓度不一致。

> 后续反应体系中，底物工作液占 80%，故最终底物浓度为 **0.5%（w/v）**。

------

## 4. 整细胞降解反应体系

### 单管反应体系：总体积 1.0 mL

| 成分                      |     体积 | 最终条件                   |
| ------------------------- | -------: | -------------------------- |
| 0.625% PASC 或 MCC 工作液 |   800 μL | 终浓度 0.5%（w/v）         |
| 洗涤并标准化后的菌悬液    |   200 μL | 以实际加入的 OD 单位归一化 |
| 总体积                    | 1,000 μL | —                          |

例如：若菌悬液 OD600 = 10，则加入 200 μL 后，每管菌体输入量为：

10 × 0.2 mL = 2.0 OD600·mL

所有样品应保持相同的菌体输入量。

### 反应条件

| 参数       | 初始推荐条件                 | 说明                                  |
| ---------- | ---------------------------- | ------------------------------------- |
| 温度       | 37°C                         | 可根据目标酶活性优化为 30、37 或 40°C |
| 振荡速度   | 180–220 rpm                  | 保持底物悬浮、改善传质                |
| 反应时间   | 0、15、30、60、120 min       | 建议先做时间梯度，确定线性区间        |
| 底物浓度   | 0.5%（w/v）                  | PASC 与 MCC 必须保持相同干重浓度      |
| 缓冲液     | 50 mM sodium acetate，pH 5.0 | 可依目标酶最适 pH 调整                |
| 生物学重复 | ≥3                           | 用于统计分析                          |

> 对于时间梯度实验，建议每个时间点使用独立反应管，而不是从同一反应管反复取样。这样可以避免因多次取样、底物沉降和体系体积变化带来的误差。

------

## 5. 终止反应及样品澄清

1. 达到设定反应时间后，立即将反应管置于冰上。
2. 以 **12,000–14,000 × g，4°C，离心 5 min**。
3. 小心吸取上清液，避免带入菌体或 PASC/MCC 颗粒。
4. 取上清进行 DNS 还原糖检测；若不能立即检测，可短暂置于冰上，建议当天完成。

> 对于 MCC 组，离心尤其重要。若有悬浮颗粒进入 DNS 显色体系，会造成散射、吸光度偏高及批间变异。

------

# 七、DNS 还原糖检测

## 1. BC0235 微量法

BC0235 是 Solarbio 还原糖含量检测试剂盒（微量法），检测波长为 **540 nm**。试剂盒的标准品、试剂配制、样品体积、显色温度和显色时间均以随盒说明书的当前批次为准；不得把其他 DNS 方法的加样体积或沸水浴时间直接套用到 BC0235。

1. 反应结束后，立即冰浴并高速离心；取澄清、无菌体和无纤维素颗粒的上清。
2. 用与样品相同的反应缓冲液稀释葡萄糖标准品和样品；每个稀释倍数至少做技术复孔。
3. 按 BC0235 说明书同时加入标准品、样品、空白和试剂；所有孔使用相同的加样顺序、反应时间和温度。
4. 按说明书完成显色，在 **540 nm** 读取吸光度；使用试剂盒空白校正，并以标准曲线换算还原糖浓度。
5. 样品吸光度超出标准曲线线性范围时，重新稀释后测定；记录稀释倍数。

> BC0235 测得的是还原糖总量，结果应报告为“还原糖浓度（mg/mL，葡萄糖当量）”，不能直接称为葡萄糖浓度。

### 样本前处理流程

整细胞 + 底物反应 → 冰浴/高速离心 → 取澄清上清 → 按 BC0235 显色 → 540 nm 读数 → 标准曲线换算

------

## 2. 结果计算

### （1）背景扣除

优先使用同底物、同菌体输入量的阴性菌对照扣除背景：

Cnet = C工程菌+底物 - C阴性菌+同一底物

若未设置阴性菌，则使用底物空白和细胞空白：

Cnet = C实验组 - C底物空白 - C细胞空白

其中，Cnet 的单位为 mg/mL 葡萄糖当量。

### （2）计算总还原糖释放量

还原糖释放量（mg） = Cnet × Vreaction × DF

其中：

- Cnet：背景扣除后的还原糖浓度，mg/mL；
- Vreaction：反应总体积，本方案为 1.0 mL；
- DF：样品在 BC0235 检测前的稀释倍数。

### （3）计算整细胞表观活性

若将 1 U 定义为每分钟释放 1 μmol 葡萄糖当量，则：

Activity (U) = Cnet × Vreaction × DF × 1000 / (180.16 × t)

其中，t 为反应时间（min）；180.16 为葡萄糖的相对分子质量（mg/mmol）。

Specific activity = Activity (U) / [Input OD600 × mL]

单位：μmol glucose equivalents·min^-1·(OD600·mL)^-1

------

## 八、注意事项

### 1. PASC 与 MCC 结果不能简单横向等同

PASC 经磷酸膨润后更容易被酶接近，因此通常会得到高于 MCC 的还原糖释放量。该差异反映的是底物可及性、结晶度及酶作用模式的综合结果，而不只是“酶量”的差异。[1][2]

### 2. 必须控制菌体代谢对结果的影响

活的大肠杆菌可能消耗反应中生成的葡萄糖或其他可溶性寡糖，导致 DNS 检测到的还原糖低于实际释放量。因此：

- 首次实验建议优先使用较短时间梯度，如 0–60 min；
- 选取还原糖释放量与时间呈线性关系的时间段计算活性；
- 必须设置阴性菌和失活菌对照；
- 如果目标是严格衡量酶促释放，而非“整细胞体系净积累的糖”，可进一步考虑检测纤维二糖、葡萄糖及寡糖组成，例如 HPLC 或离子色谱。

### 3. DNS 测到的是“还原糖总量”

DNS 法会对葡萄糖、纤维二糖和多种可溶性寡糖产生响应。

- “还原糖浓度（以葡萄糖当量计）”
- “reducing sugar released, expressed as glucose equivalents”

而不是直接写作“葡萄糖浓度”或者“纤维二糖浓度”。

### 4. PASC 和 MCC 都会沉降

- 每次取 PASC/MCC 工作液前必须充分涡旋；
- 建议使用宽口吸头或剪短吸头前端，避免纤维素团块堵塞；
- 配制反应体系时尽量快速、顺序一致；
- 反应期间需保持振荡；
- 若悬浮不均匀，重复之间的差异会非常大。

### 5. DNS 测定前必须彻底去除菌体和纤维素颗粒

菌体、PASC 或 MCC 颗粒会造成光散射，也可能在显色过程中带来不稳定背景。每个样品均应在反应后高速离心，取清亮上清检测。

### 6. 优先使用反应缓冲液洗菌，而不是直接用培养基或 PBS 进入反应

若用含有蛋白胨、酵母粉或糖类的培养基直接做 DNS，背景往往偏高。对于以弱酸性为最适条件的纤维素酶，推荐用同一反应缓冲液洗涤菌体并重悬，以保证体系一致。

### 7. PASC 的批次标准化很重要

每批 PASC 应至少记录：

- 微晶纤维素供应商、货号、型号；
- 初始纤维素质量；
- 磷酸浓度、用量；
- 膨润温度与时间；
- 洗涤次数、最终上清 pH；
- 最终 PASC 干重浓度；
- 保存时间。

------

## 九、数据呈现方式

### 1. 结果表格模板

| 菌株/样品            | 底物 | 反应时间（min） | 还原糖浓度（mg/mL，葡萄糖当量） | 背景校正后浓度（mg/mL） | 归一化活性［U/(OD600·mL)］ |
| -------------------- | ---- | --------------: | ------------------------------: | ----------------------: | -------------------------: |
| 阴性对照菌           | PASC |              60 |                                 |                         |                            |
| 工程菌               | PASC |              60 |                                 |                         |                            |
| 阴性对照菌           | MCC  |              60 |                                 |                         |                            |
| 工程菌               | MCC  |              60 |                                 |                         |                            |
| BC0235 方法学对照 | 葡萄糖标准品 |              — |                                 |                         |                            |

### 2. 作图

- **柱状图：**不同菌株在 PASC 和 MCC 上的归一化还原糖释放量；
- **时间曲线：**0–120 min 内还原糖释放量随时间的变化；
- **PASC/MCC 活性比值：**

PASC/MCC activity ratio = PASC 上的归一化活性 / MCC 上的归一化活性

该比值可作为整细胞体系对低结晶度与高结晶度纤维素相对偏好的辅助指标，但不能单独代表“纤维素酶性能优劣”。

------

## 十、培养条件

1. **LB 或含氮 M9 只用于培养和诱导。**LB 含有蛋白胨和酵母粉，适合大肠杆菌扩增，但其中的还原性组分会干扰 DNS，因此诱导结束后必须洗菌。若使用 M9，基础盐中应包含氮源，例如 NH4Cl；同时补充 Mg2+、Ca2+、碳源和必要的抗生素。
2. **MCC/PASC 不能单独支持大肠杆菌生长。**它们主要提供碳源，而且大肠杆菌通常不具备直接利用结晶纤维素的能力；即使工程菌能利用水解产物，仍需氮源合成蛋白质和核酸。无氮源体系可用于短时酶解，但不能作为生长培养基。
3. **建议的培养流程：**单菌落接种含相应抗生素的 LB，37°C、180–220 rpm 培养过夜；按 1:50–1:100 转接新鲜 LB，培养至目标 OD600 后按载体和目标蛋白要求诱导。诱导温度、时间和诱导剂浓度应以目标蛋白的表达条件为准，并记录实际 OD600。
4. **若要验证底物能否作为碳源，需另做生长实验：**含氮 M9 + MCC/PASC 为实验组；含氮 M9 + 葡萄糖为阳性对照；含氮 M9 不加碳源为阴性对照。用 OD600 和 CFU 双重判断，不能用一次短时 DNS 结果代替生长证据。
5. **目标酶条件参考：**Cel5L 和 Cel9K 的文献统一测定条件约为 60°C、pH 5.8；Cel48S 的纯化酶最适约为 70°C、pH 5.7。[7][8] 由于本实验使用大肠杆菌整细胞，首轮仍建议 37°C、pH 5.0–5.5；如需优化，可增加 50–60°C、pH 5.5–6.0 条件，但不宜直接套用 Cel48S 的 70°C。

------

## 十一、首轮摸底条件

如果目前尚不清楚表达体系的最适条件，可先采用以下组合完成初筛：

| 项目             | 建议初始条件                                 |
| ---------------- | -------------------------------------------- |
| 整细胞反应缓冲液 | 50 mM sodium acetate，pH 5.0                 |
| 底物             | 0.5% PASC 或 0.5% MCC                        |
| 菌体输入量       | 2.0 OD600·mL/反应管                          |
| 总反应体积       | 1.0 mL                                       |
| 温度             | 37°C                                         |
| 振荡             | 200 rpm                                      |
| 时间点           | 0、15、30、60 min                            |
| 检测             | 反应后离心取上清，按 BC0235 微量法检测        |
| 判定原则         | 选择还原糖释放量随时间线性增加的区间计算活性 |

------

## 十二、参考文献

[1] Wood TM. Preparation of crystalline, amorphous, and dyed cellulase substrates. Methods in Enzymology. 1988;160:19–25. doi: 10.1016/0076-6879(88)60103-0.

[2] Zhang Y-HP, Himmel ME, Mielenz JR. Outlook for cellulase improvement: screening and selection strategies. Biotechnology Advances. 2006;24(5):452–481. doi: 10.1016/j.biotechadv.2006.03.003.

[3] Zhang Y-HP, Lynd LR. Toward an aggregated understanding of enzymatic hydrolysis of cellulose: noncomplexed cellulase systems. Biotechnology and Bioengineering. 2004;88(7):797–824. doi: 10.1002/bit.20282.

[4] Miller GL. Use of dinitrosalicylic acid reagent for determination of reducing sugar. Analytical Chemistry. 1959;31(3):426–428. doi: 10.1021/ac60147a030.

[5] Ghose TK. Measurement of cellulase activities. Pure and Applied Chemistry. 1987;59(2):257–268. doi: 10.1351/pac198759020257.

[6] Neidhardt FC, Bloch PL, Smith DF. Culture medium for enterobacteria. Journal of Bacteriology. 1974;119(3):736–747. doi: 10.1128/jb.119.3.736-747.1974.

[7] Leis B, Held C, Bergkemper F, et al. Comparative characterization of all cellulosomal cellulases from Clostridium thermocellum reveals high diversity in endoglucanase product formation essential for complex activity. Biotechnology for Biofuels. 2017;10:240. doi: 10.1186/s13068-017-0928-4.

[8] Liu YJ, Liu S, Dong S, et al. Determination of the native features of the exoglucanase Cel48S from Clostridium thermocellum. Biotechnology for Biofuels. 2018;11:6. doi: 10.1186/s13068-017-1009-4.





# PASC/MCC Whole‑Cell Cellulose Degradation Assay Protocol

This protocol is used to evaluate the cellulose‑degrading capability of *Escherichia coli* whole‑cells that express or surface‑display cellulases against two types of cellulose substrates. The assay consists of two parts: cell culture‑induction in nitrogen‑containing medium, followed by short‑term growth‑free enzymatic hydrolysis using washed cells.

- **PASC (phosphoric acid‑swollen cellulose)**: Phosphoric‑acid‑treated cellulose with reduced crystallinity and high accessibility. It is suitable for assessing the initial degradation capacity of endoglucanases toward amorphous cellulose.
- **MCC (microcrystalline cellulose)**: Used herein as the crystalline cellulose substrate. Avicel is regarded as a commercial source of MCC; record its exact model number, and do not treat Avicel as a distinct substrate for comparison.

## 1. Assay Objectives
1. Prepare PASC from commercial microcrystalline cellulose to generate a reproducible amorphous/low‑crystallinity cellulose substrate.
2. Compare the cellulose‑degrading performance of engineered *E. coli* whole‑cells toward PASC and MCC.
3. Quantify reducing sugars in reaction supernatants via the **DNS reducing‑sugar assay**, expressed as glucose equivalents for cellulose‑degradation products.
4. Eliminate false‑positive signals derived from medium residues, cellular backgrounds and substrate backgrounds by setting up no‑cell substrate controls, no‑substrate cell controls and inactivated‑cell controls.

## 2. Assay Principle
Upon cellulase‑catalyzed hydrolysis of cellulose, reducing products including glucose, cellobiose and soluble oligosaccharides are released. BC0235 refers to the Solarbio Reducing Sugar Content Assay Kit (micro‑volume method). After color development following the kit manual, absorbance is measured at 540 nm, and reducing‑sugar concentration is calculated against the kit‑supplied glucose standard curve, reported as glucose equivalents.

PASC is produced by swelling MCC in concentrated phosphoric acid followed by extensive water washing. This treatment disrupts ordered cellulose structures and improves enzyme accessibility; consequently, PASC is generally more susceptible to enzymatic hydrolysis than MCC.

## 3. Consumables and Instruments
### 3.1 Reagents and Consumables
| Category | Name | Specification / Recommendation | Purpose |
|---|---|---|---|
| Substrates | Microcrystalline cellulose (MCC; Avicel recorded only as commercial name) | Record supplier, catalog number and model | PASC preparation; crystalline cellulose substrate |
| PASC preparation | Phosphoric acid | 85 % (w/w) concentrated phosphoric acid | Swelling of microcrystalline cellulose |
| Reaction buffer | Sodium acetate buffer | 50 mM, pH 5.0; adjust pH according to the enzyme’s known optimum | Buffer for whole‑cell degradation reactions |
| Reaction buffer | Glacial acetic acid, anhydrous sodium acetate | Analytical grade | Prepare sodium acetate buffer |
| Washing solution | Sterile deionized / ultrapure water | — | PASC washing; cell washing |
| Cells | Tested engineered *E. coli* whole‑cells | Post‑induction bacterial culture | Source of cellulase |
| DNS quantification | Solarbio BC0235 Reducing Sugar Content Assay Kit (micro‑volume method) | Prepare and operate strictly according to batch‑specific kit instructions | Reducing‑sugar quantification |
| Standards | Glucose standard | Kit‑supplied or analytical‑grade D‑glucose | Generate standard curve |
| Control strains | Negative‑control strain | Empty‑vector strain, uninduced strain, or cellulase‑negative strain | Rule out host and vector‑derived background signals |
| Centrifuge consumables | 1.5/2.0 mL EP tubes, 15/50 mL centrifuge tubes | Centrifuge‑resistant | Reactions and sample processing |
| Miscellaneous | Pipette tips, sealing film, disposable gloves, pH test strips or pH meter | — | General laboratory operations |
| Optional | Reagents for glucose‑oxidase / hexokinase assay | — | Supplementary test to discriminate glucose from total reducing sugars |

### 3.2 Instruments
| Instrument | Purpose |
|---|---|
| Benchtop high‑speed refrigerated centrifuge | Cell harvesting; clarification of reaction mixtures |
| Thermostatted shaker | Whole‑cell‑substrate incubation |
| Spectrophotometer or microplate reader | Measure OD₆₀₀ of cell suspensions; read DNS‑colorimetric absorbance |
| Water bath or heat block | DNS color‑development reaction |
| Vortex mixer | Resuspend substrates and cell pellets |
| Analytical balance | Weigh microcrystalline cellulose |
| Magnetic stirrer | Mixing during PASC preparation |
| Fume hood | Mandatory for handling 85 % phosphoric acid |
| Oven | Determine actual dry‑matter concentration of PASC suspension |

## 4. Solution Preparation
### 4.1 50 mM Sodium acetate buffer, pH 5.0
Use this as the default reaction buffer for initial whole‑cell cellulase activity assays. If the enzyme’s optimum pH is known and deviates from pH 5.0, optimize pH accordingly.
1. Prepare 50 mM sodium‑acetate solution.
2. Adjust pH to 5.0 with glacial acetic acid.
3. Sterilize by autoclaving or 0.22 μm filtration.
4. Store at 4 °C.

> **PBS is not recommended as the default reaction buffer.** PBS is usually near neutral pH, while most fungal‑derived or engineered cellulases exhibit higher activity under weak‑acidic conditions. Critically, cells must be thoroughly washed before quantification to avoid interference from peptone, yeast extract, sugars and other reducing components carried over from culture medium.

## 5. In‑house PASC Preparation Protocol
### 5.1 PASC Preparation Conditions
The following recipe starts from **1.0 g microcrystalline cellulose**, yielding sufficient PASC suspension for multiple parallel experiments.

| Item | Recommended Condition |
|---|---|
| Starting substrate | 1.0 g microcrystalline cellulose |
| Phosphoric‑acid concentration | 85 % (w/w) |
| Phosphoric‑acid volume | 10 mL |
| Incubation temperature | 0–4 °C |
| Swelling time | 45–60 min |
| Precipitation / washing centrifugation | 8 000–10 000 × g, 10 min, 4 °C |
| Final stock suspension | 2.0 % (w/v, dry‑weight basis) PASC |
| Storage condition | 4 °C; use within 1 week; prepare fresh whenever possible |

### 5.2 PASC Preparation Steps
#### Step 1 Pre‑cooling and safety precautions
1. Pre‑chill 85 % phosphoric acid, deionized water, glass beakers, stir bars and centrifuge tubes on ice or at 4 °C.
2. Perform all concentrated‑phosphoric‑acid operations inside a **fume hood**.
3. Wear lab coat, goggles / face shield and acid‑resistant gloves.

> 85 % phosphoric acid is highly corrosive. In case of skin contact, flush immediately with large volumes of running tap water. For eye exposure or persistent injury, follow institutional chemical‑safety protocols and seek medical attention.

#### Step 2 Phosphoric‑acid swelling of microcrystalline cellulose
1. Add **10 mL of 85 % phosphoric acid** into an ice‑cooled glass beaker under magnetic stirring.
2. Slowly add **1.0 g microcrystalline cellulose** in small portions while continuous magnetic stirring.
3. Maintain incubation at **0–4 °C with stirring for 45–60 min**, until a homogeneous, milky‑white to translucent viscous suspension/gel is formed.

**Notes**
- Add cellulose portion‑wise to avoid large non‑dispersible clumps.
- Avoid prolonged room‑temperature treatment; do not exceed ~1 h incubation. Excessive acid hydrolysis will alter substrate properties.
- Particle size and crystal form vary between MCC batches; record raw‑material model and incubation duration.

#### Step 3 Quench reaction and precipitate PASC
1. Prepare a larger beaker containing **100 mL ice‑cold deionized water**, keep stirring.
2. Slowly pour the phosphoric‑acid‑cellulose suspension into the ice‑cold water with vigorous stirring.
3. Transfer mixture into centrifuge tubes.
4. Centrifuge at **8 000–10 000 × g, 4 °C, 10 min**, discard supernatant.

> Pour acidic cellulose suspension into excess cold water — **do not add water directly into concentrated acid**. Keep all steps inside the fume hood.

#### Step 4 Repeated washing until near‑neutral pH
1. Resuspend pellet thoroughly with sufficient deionized water by vortexing or gentle pipetting.
2. Centrifuge again at **8 000–10 000 × g, 4 °C, 10 min**.
3. Repeat washing **4–6 times**. Record supernatant pH after each decantation.
4. Stop washing when supernatant pH reaches **5.5–7.0**, indicating adequate removal of residual phosphoric acid.

**Critical notes**
- **Do NOT neutralize directly with NaOH**. Direct alkali addition introduces salts that may interfere with enzymatic reactions and DNS quantification. Repeated water washing is preferred for enzyme‑assay‑grade PASC.
- Insufficient acid carry‑over lowers system pH, causes cell inactivation, reduced enzyme activity and poor batch‑to‑batch reproducibility.
- PASC readily forms gel‑like aggregates; ensure complete resuspension in each washing cycle.

#### Step 5 Determine PASC dry‑matter concentration and prepare stock suspension
Since washed PASC exists as suspension, concentration cannot be estimated from volume alone. Calibrate gravimetrically.
1. Pre‑weigh an aluminum dish or heat‑resistant weighing boat, record empty‑dish mass M₀.
2. Thoroughly homogenize PASC suspension; withdraw **1.0 mL suspension into the dish**, record wet mass.
3. Dry at **105 °C oven to constant weight**, record final mass M₁.
4. Calculate PASC dry‑matter concentration:

PASC concentration (mg/mL) = (M₁ − M₀) × 1000 / sampling volume (mL)

Dilute PASC with deionized water or reaction buffer to prepare **2.0 % (w/v, i.e. 20 mg/mL) stock suspension**.

Example: If total dry PASC mass = 0.80 g, final volume = 0.80 g ÷ 0.02 g/mL = 40 mL to obtain 2.0 % PASC stock.

#### Step 6 PASC storage
- Store PASC at 4 °C; vortex thoroughly before every use.
- Preferably use within **1 week**. Discard if abnormal turbidity, off‑odors or contamination appears.
- If long‑term storage is required, validate that storage conditions do not alter substrate accessibility and hydrolyzability.
- Autoclaving of final PASC suspension is not recommended without validation; high temperature may change dispersion and crystal structure, compromising batch comparability.

## 6. Whole‑Cell Cellulose Degradation Assay
### 6.1 Experimental Design
Set up the following groups. Run **at least 3 biological replicates per group**, with 2‑3 technical replicates for each biological replicate.

| Group | Cells | Substrate | Purpose |
|---|---|---|---|
| PASC experimental group | Cellulase‑expressing whole‑cells | PASC | Evaluate degradation toward amorphous/swollen cellulose |
| MCC experimental group | Cellulase‑expressing whole‑cells | MCC | Evaluate degradation toward crystalline cellulose |
| Substrate blank | Sterile buffer | PASC or MCC | Subtract substrate‑derived and reagent background |
| Cell blank | Cellulase‑expressing whole‑cells | No substrate | Subtract background from cell‑released components |
| Negative‑strain control | Empty‑vector / uninduced / cellulase‑negative cells | PASC or MCC | Rule out non‑specific host‑strain background |
| Inactivated‑cell control | Heat‑inactivated test cells | PASC or MCC | Exclude non‑enzymatic adsorption and background release |
| BC0235 method‑control | Glucose standards | No substrate | Validate BC0235 color‑development and standard‑curve performance |

### 6.2 Cell Preparation
#### Step 1 Culture and induction
Grow and induce cells in nitrogen‑supplemented medium according to your expression vector, inducer and target‑protein system. LB is recommended; for defined medium, use nitrogen‑supplemented M9 (e.g. NH₄Cl). MCC/PASC cannot serve as nitrogen sources and cannot replace medium nitrogen.

Culture medium is used solely for cell growth and induction and must not be carried over into downstream hydrolysis reactions. Record:
‑ Host strain
‑ Plasmid construct
‑ Inducer and concentration
‑ OD₆₀₀ at induction onset
‑ Induction temperature and duration
‑ Expression mode: intracellular / periplasmic / secreted / cell‑surface display

> Notes on nitrogen‑free conditions: After washing, cells are assayed in short‑term (0–120 min) hydrolysis reactions. These reactions are not intended for cell growth and do not require additional nitrogen. Do not interpret these setups as evidence that cells can grow in nitrogen‑free environments. To test whether MCC/PASC supports cell growth, perform independent growth assays using nitrogen‑supplemented minimal medium with MCC/PASC as sole carbon source, alongside glucose positive control and no‑carbon‑source negative control.

> For intracellular‑expressed cellulases: intact *E. coli* cells have limited physical access to substrates, resulting in low apparent whole‑cell activity. This protocol is best suited for surface‑displayed, secreted or outer‑membrane‑targeted cellulase systems.

#### Step 2 Harvest and wash cells
1. Record OD₆₀₀ of post‑induction culture.
2. Harvest cells by centrifugation: **4 000–6 000 × g, 4 °C, 8–10 min**. Discard supernatant.
3. Resuspend pellet in pre‑chilled **50 mM sodium‑acetate buffer, pH 5.0**.
4. Repeat centrifugation‑resuspension washing cycle **twice**.
5. Finally resuspend cells in identical reaction buffer and normalize suspensions to uniform OD₆₀₀ before use.

> Rationale for thorough washing: Peptone, yeast extract, sugars and metabolites from culture medium contribute interfering signals in DNS assays. Carry‑over also perturbs pH, ionic strength and substrate behavior across reaction tubes.

### 6.3 Prepare substrate working suspensions
- **PASC working suspension**: Dilute 2.0 % PASC stock with reaction buffer to **0.625 % (w/v)**.
- **MCC working suspension**: Weigh MCC powder and prepare **0.625 % (w/v)** suspension in reaction buffer. Vortex vigorously immediately before pipetting and between sampling steps to prevent particle sedimentation.

> Working suspensions occupy 80 % of final reaction volume, giving final substrate concentration of **0.5 % (w/v)**.

### 6.4 Whole‑cell degradation reaction setup
#### Single‑tube reaction system (total volume = 1.0 mL)

| Component | Volume | Final Condition |
|---|---:|---|
| 0.625 % PASC or MCC working suspension | 800 μL | Final substrate 0.5 % (w/v) |
| Washed, OD‑normalized cell suspension | 200 μL | Normalized by input OD₆₀₀ · mL units |
| Total volume | 1 000 μL | — |

Example: If cell suspension OD₆₀₀ = 10, adding 200 μL gives cell input = 10 × 0.2 mL = 2.0 OD₆₀₀·mL. Maintain identical cell input across all reactions.

#### Reaction parameters
| Parameter | Initial recommended setting | Remarks |
|---|---|---|
| Temperature | 37 °C | Optimize to 30 °C / 37 °C / 40 °C according to enzyme properties |
| Shaking speed | 180–220 rpm | Maintain substrate suspension and improve mass transfer |
| Time‑points | 0, 15, 30, 60, 120 min | Run time‑course to identify linear‑activity window |
| Final substrate concentration | 0.5 % (w/v) | Match dry‑mass concentration between PASC and MCC |
| Buffer | 50 mM sodium acetate, pH 5.0 | Adjust pH for enzyme optimum |
| Biological replicates | ≥3 | For statistical analysis |

> For time‑course experiments, prepare independent reaction tubes for each time‑point. Avoid repeated sampling from one single tube, which causes volume change, substrate sedimentation and measurement bias.

### 6.5 Terminate reaction and clarify samples
1. Immediately transfer tubes onto ice once target incubation time is reached.
2. Centrifuge: **12 000–14 000 × g, 4 °C, 5 min**.
3. Carefully collect supernatant; avoid carry‑over of cells or cellulose particles.
4. Use supernatant for DNS reducing‑sugar measurement. Keep samples on ice if measurement cannot be performed immediately; complete detection within the same day.

> Efficient centrifugation is especially critical for MCC groups. Resuspended particles in color‑development mixtures produce light scattering, artificially elevated absorbance and large inter‑sample variation.

## 7. DNS Reducing‑Sugar Quantification
### 7.1 BC0235 micro‑volume assay
BC0235 is the Solarbio Reducing Sugar Content Assay Kit (micro‑volume format), read at **540 nm**. Follow batch‑specific kit instructions for reagent preparation, sample volume, incubation temperature and incubation time. Do not directly apply incubation parameters from other DNS protocols to BC0235.

1. Stop reactions on ice, high‑speed centrifuge, harvest particle‑free clear supernatant.
2. Dilute glucose standards and samples using the identical reaction buffer. Include technical replicates for every dilution factor.
3. Load standards, samples and blanks together with assay reagents following BC0235 instructions. Maintain identical pipetting order, incubation time and temperature across all wells.
4. Complete color‑development, read absorbance at **540 nm**. Correct against kit blank and calculate reducing‑sugar concentration via standard curve.
5. If sample absorbance falls outside linear range of standard curve, dilute sample and re‑measure; record dilution factor.

> BC0235 measures total reducing sugars. Report results as “reducing‑sugar concentration (mg/mL, glucose equivalents)”, **do not report as glucose concentration**.

Sample workflow: Whole‑cell + substrate reaction → ice bath / high‑speed centrifugation → collect clear supernatant → BC0235 color‑development → 540 nm absorbance reading → convert via standard curve.

### 7.2 Calculations

#### (1) Background subtraction

Preferentially subtract background using negative‑control strain with identical substrate and identical cell input:

\(C_{net}=C_{engineered\,cell+substrate}-C_{negative\,control+same\,substrate}\)

If negative‑strain control is unavailable, use substrate blank and cell blank:

\(C_{net}=C_{experimental}-C_{substrate\,blank}-C_{cell\,blank}\)

\(C_{net}\): background‑corrected reducing‑sugar concentration (mg/mL, glucose equivalents).

#### (2) Total released reducing‑sugar mass

\(Released\,reducing\,sugar\,(mg)=C_{net} \times V_{reaction} \times DF\)

- \(C_{net}\): background‑corrected reducing‑sugar concentration, mg/mL
- \(V_{reaction}\): total reaction volume (1.0 mL in this protocol)
- DF: dilution factor applied before DNS measurement

#### (3) Apparent whole‑cell activity

Define 1 U as the amount of whole‑cells releasing 1 μmol glucose equivalents per minute.

\(Activity\,(U)=\frac{C_{net} \times V_{reaction} \times DF \times 1000}{180.16 \times t}\)

- t = reaction time (min)
- 180.16 = molar mass of glucose (mg/mmol)

Specific activity:

\(Specific\;activity=\frac{Activity\,(U)}{Input\,OD_{600} \times mL}\) Unit: μmol glucose equivalents·min⁻¹·(OD₆₀₀·mL)⁻¹

## 8. Important Notes
1. Do not directly compare absolute numerical values obtained from PASC and MCC. PASC is more enzymatically accessible after phosphoric‑acid swelling and usually yields higher reducing‑sugar release. Observed differences reflect combined effects of substrate crystallinity, accessibility and enzyme mode‑of‑action, and are not merely a read‑out of enzyme quantity.

2. Control for metabolic consumption by living *E. coli*. Viable bacterial cells may consume newly‑formed glucose and soluble oligosaccharides, lowering detected reducing‑sugar values below true enzymatic release.
‑ For initial assays, prioritize short‑time windows (0–60 min).
‑ Calculate activity only within time intervals where reducing‑sugar accumulation increases linearly with incubation time.
‑ Always include negative‑strain and heat‑inactivated‑cell controls.
‑ If you aim to strictly quantify enzymatic release (rather than net sugar accumulation in whole‑cell mixtures), supplementary analysis such as HPLC or ion chromatography can characterize profiles of glucose, cellobiose and oligosaccharides.

3. DNS detects total reducing sugars. DNS responds to glucose, cellobiose and diverse soluble oligosaccharides. Report data as “reducing sugar released, expressed as glucose equivalents”, not “glucose concentration” or “cellobiose concentration”.

4. Both PASC and MCC sediment rapidly.
‑ Vortex working suspensions thoroughly before every pipetting step.
‑ Use wide‑orifice tips or cut‑tip ends to avoid clogging by cellulose aggregates.
‑ Prepare reaction tubes quickly and maintain consistent pipetting sequence.
‑ Keep shaking during incubation.
‑ Poor suspension homogeneity leads to large inter‑replicate variation.

5. Rigorously remove cells and cellulose particles before DNS measurement. Cells, PASC or MCC particles cause light scattering and unstable background signals. Always high‑speed‑centrifuge reaction mixtures and assay only clear supernatants.

6. Wash cells using reaction buffer rather than raw culture medium or PBS. Media containing peptone, yeast extract or sugars produce high background in DNS. For cellulases with weak‑acidic optima, wash and resuspend cells in the identical assay buffer to guarantee system consistency.

7. Standardize every batch of PASC. Record for each batch:
‑ MCC supplier, catalog number, model
‑ Initial cellulose mass
‑ Phosphoric‑acid concentration and volume
‑ Swelling temperature and duration
‑ Washing cycles and final supernatant pH
‑ Final gravimetric PASC concentration
‑ Storage age before use

## 9. Data Presentation
### 9.1 Result Table Template
| Strain / Sample | Substrate | Incubation time (min) | Reducing‑sugar concentration (mg/mL, glucose equivalents) | Background‑corrected concentration (mg/mL) | Normalized activity [U/(OD₆₀₀·mL)] |
|---|---|---:|---:|---:|---|
| Negative‑control strain | PASC | 60 | | | |
| Engineered strain | PASC | 60 | | | |
| Negative‑control strain | MCC | 60 | | | |
| Engineered strain | MCC | 60 | | | |
| BC0235 method control | Glucose standard | — | | | |

### 9.2 Plotting suggestions
‑ **Bar chart**: Normalized reducing‑sugar release of different strains on PASC versus MCC.
‑ **Time‑course curve**: Reducing‑sugar accumulation over 0–120 min incubation.
‑ **PASC/MCC activity ratio**:

$$PASC/MCC\;activity\;ratio=\frac{normalized\;activity\;on\;PASC}{normalized\;activity\;on\;MCC}$$

This ratio assists evaluation of relative preference toward low‑ versus high‑crystallinity substrates, but cannot independently represent overall cellulase performance.

## 10. Culture‑Condition
1. **LB or nitrogen‑supplemented M9 are only for cell growth and induction.** LB contains peptone and yeast extract, good for *E. coli* propagation, yet its reducing components interfere with DNS; cells must be thoroughly washed after induction. For M9 minimal medium, supply nitrogen e.g. NH₄Cl together with Mg²⁺, Ca²⁺, carbon source and required antibiotics.
2. **MCC/PASC alone cannot support *E. coli* growth.** They serve only as carbon sources. Even engineered strains capable of hydrolyzing cellulose still require nitrogen for biosynthesis. Nitrogen‑free buffers are for short‑term hydrolysis, not growth media.
3. **Recommended culture workflow:** Inoculate single colony into antibiotic‑supplemented LB, grow overnight at 37 °C, 180‑220 rpm. Sub‑culture 1:50‑1:100 into fresh LB, grow to target OD₆₀₀ and induce according to vector‑specific protocols. Record actual OD₆₀₀, induction temperature, duration and inducer concentration.
4. **To test whether MCC/PASC functions as carbon source, perform independent growth assays.** Setup: nitrogen‑supplemented M9 + MCC/PASC (test group); nitrogen‑supplemented M9 + glucose (positive control); nitrogen‑supplemented M9 without carbon source (negative control). Evaluate growth by both OD₆₀₀ and CFU counts. Short‑term DNS hydrolysis results cannot substitute growth evidence.
5. **Reference enzyme properties reported in literature:** Cel5L and Cel9K are commonly assayed at ~60 °C, pH 5.8; purified Cel48S exhibits optimum near 70 °C, pH 5.7. For *E. coli* whole‑cell assays, start with 37 °C, pH 5.0‑5.5. Subsequent optimization may include 50‑60 °C and pH 5.5‑6.0; do not directly adopt the 70 °C optimum of purified Cel48S for whole‑cell reactions.

## 11. Initial Screening Conditions
If optimum reaction parameters for your construct are unknown, start with the following baseline setup:

| Item | Initial screening condition |
|---|---|
| Whole‑cell reaction buffer | 50 mM sodium acetate, pH 5.0 |
| Substrates | 0.5 % PASC or 0.5 % MCC |
| Cell input | 2.0 OD₆₀₀·mL per reaction tube |
| Total reaction volume | 1.0 mL |
| Incubation temperature | 37 °C |
| Shaking speed | 200 rpm |
| Time‑points | 0, 15, 30, 60 min |
| Detection | Post‑reaction centrifugation, supernatant assayed via BC0235 micro‑volume kit |
| Criterion for activity calculation | Select time range where reducing‑sugar release increases linearly over time |

## References
[1] Wood TM. Preparation of crystalline, amorphous, and dyed cellulase substrates. *Methods in Enzymology*. 1988;160:19‑25. doi: 10.1016/0076‑6879(88)60103‑0.
[2] Zhang Y‑HP, Himmel ME, Mielenz JR. Outlook for cellulase improvement: screening and selection strategies. *Biotechnology Advances*. 2006;24(5):452‑481. doi: 10.1016/j.biotechadv.2006.03.003.
[3] Zhang Y‑HP, Lynd LR. Toward an aggregated understanding of enzymatic hydrolysis of cellulose: noncomplexed cellulase systems. *Biotechnology and Bioengineering*. 2004;88(7):797‑824. doi: 10.1002/bit.20282.
[4] Miller GL. Use of dinitrosalicylic acid reagent for determination of reducing sugar. *Analytical Chemistry*. 1959;31(3):426‑428. doi: 10.1021/ac60147a030.
[5] Ghose TK. Measurement of cellulase activities. *Pure and Applied Chemistry*. 1987;59(2):257‑268. doi: 10.1351/pac198759020257.
[6] Neidhardt FC, Bloch PL, Smith DF. Culture medium for enterobacteria. *Journal of Bacteriology*. 1974;119(3):736‑747. doi: 10.1128/jb.119.3.736‑747.1974.
[7] Leis B, Held C, Bergkemper F, et al. Comparative characterization of all cellulosomal cellulases from *Clostridium thermocellum* reveals high diversity in endoglucanase product formation essential for complex activity. *Biotechnology for Biofuels*. 2017;10:240. doi: 10.1186/s13068‑017‑0928‑4.
[8] Liu YJ, Liu S, Dong S, et al. Determination of the native features of the exoglucanase Cel48S from *Clostridium thermocellum*. *Biotechnology for Biofuels*. 2018;11:6. doi: 10.1186/s13068‑017‑1009‑4.
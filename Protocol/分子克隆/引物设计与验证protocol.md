# 巢式PCR引物设计与验证

## **耗材**

- **引物：** 引物干粉、无菌 ddH₂O。
- **PCR 试剂：** 高保真酶 PCR Mix、Taq 酶 PCR Mix、10 mM 正反向引物、模板 DNA。
- **电泳试剂：** 琼脂糖、1× TAE 缓冲液、核酸染料、DNA Marker、Loading Buffer。
- **回收试剂：** 胶回收试剂盒、异丙醇。
- **耗材：** 0.2 mL PCR 管、1.5 mL/2 mL 离心管、移液器及枪头、一次性塑料手套、手术刀片、平头镊子。

## **仪器**

- PCR 仪
- 微波炉
- 核酸电泳仪及电泳槽
- 小型凝胶电泳紫外观测仪
- 凝胶成像系统
- 离心机
- 恒温水浴锅或金属浴
- NanoDrop 分光光度计

## **实验流程**

1. **NCBI 引物设计**
   2. 打开 NCBI Primer-BLAST 网页。
   3. 在序列输入框中粘贴目标序列或导入 FASTA 格式文件。
   4. 设定引物设计范围及预期产物长度。
   5. 设定引物退火温度。
   6. **取消勾选** "Specificity check"，勾选 "Show results in a new window"。
   7. 点击 "Get Primers" 获取结果，挑选合适的引物对，记录其序列、起止位置及产物大小。
   8. 依照上述方法，在第一对引物的预期产物内部设计第二对引物，以此类推设计第三对、第四对引物。

9. **引物合成与溶解**
   10. 汇总所有设计的引物序列，交由生物公司合成。
   11. 收到引物干粉后，仔细阅读说明书；加水溶解前先进行简略离心。
   12. 按照说明书加入适量无菌 ddH₂O 溶解至 100 μM 母液，使用时稀释至 10 mM，于 -20°C 保存。

13. **巢式PCR扩增**
   14. **第一轮 PCR 体系：** 高保真酶 Mix 22 μL + 10 mM F1 引物 1 μL + 10 mM R1 引物 1 μL + 模板 DNA 1 μL。震荡混匀并简略离心。
   15. **Touchdown PCR 程序：**
      - 95°C 5 min
      - 20 个循环：90°C 5s，95°C 20s，70°C 30s，72°C 25s
      - 15 个循环：95°C 20s，60°C 30s，72°C 25s
      - 72°C 5 min，4°C 持续。
   16. **后续轮次 PCR：** 将上一轮 PCR 产物用无菌水稀释 100 倍作为新模板。使用内部引物配制相同体系，沿用 Touchdown PCR 程序。
   17. **注意：** 若后续计划进行 TA 克隆，**最后一轮 PCR** 需将高保真酶更换为 Taq 酶。

18. **TAE 电泳验证**
   19. 配制 1% 琼脂糖凝胶：0.25 g 琼脂糖加入 25 mL 1× TAE，微波炉中高火加热至完全融化，冷却至 50–60°C 后加入核酸染料。
   20. 取 5 μL PCR 产物点样，加入 5 μL Marker，120V 电泳 30 min。
   21. 使用凝胶成像仪观察。

22. **切胶回收**
   23. 更换新鲜 1× TAE 电泳缓冲液，配制 0.7% 大孔回收胶，尽量多上样，电压低于 100V 电泳约 30 min。
   24. 在小型紫外灯下用手术刀切下目的条带，尽量切除多余凝胶，放入 2 mL 离心管。
   25. 使用胶回收试剂盒提取纯化 DNA，最后用预热至 50°C 的 ddH₂O 洗脱。
   26. 使用 NanoDrop 测定回收 DNA 浓度，保存于 -20°C。

27. **测序验证与数据分析**
   28. 将纯化后的 PCR 产物送生物公司进行一代测序。
   29. 使用 MEGA 软件打开测序结果中的 `.ab1` 峰值图文件，观察首尾峰图质量，记录不可信区域。
   30. 使用记事本打开 `.seq` 文件，根据峰值图剔除首尾不可信碱基，在序列开头添加 `>` 及文件名，保存为 FASTA 格式。
   31. 在 MEGA 中使用 "Align" 功能导入双向测序的两条序列。
   32. 对反向互补的序列右键选择 "Reverse component"。
   33. 点击 "Align DNA" 进行比对，根据两条序列的重叠区域拼接出完整的全长核酸序列。

---

# Nested PCR Primer Design and Verification

## **Materials and Consumables**

- **Primers:** Lyophilized primer powder, sterile ddH₂O.
- **PCR Reagents:** High-fidelity polymerase PCR Mix, Taq polymerase PCR Mix, 10 mM forward and reverse primers, template DNA.
- **Electrophoresis Reagents:** Agarose, 1× TAE buffer, nucleic acid dye, DNA Marker, Loading Buffer.
- **Recovery Reagents:** Gel extraction kit, isopropanol.
- **Consumables:** 0.2 mL PCR tubes, 1.5 mL/2 mL centrifuge tubes, pipettes and tips, disposable plastic gloves, scalpel blades, flat-tipped forceps.

## **Instruments**

- PCR instrument
- Microwave oven
- Nucleic acid electrophoresis apparatus and tank
- Small UV gel observation device
- Gel imaging system
- Centrifuge
- Constant-temperature water bath or metal bath
- NanoDrop spectrophotometer

## **Experimental Procedure**

1. **NCBI Primer Design**
   2. Open the NCBI Primer-BLAST webpage.
   3. Paste the target sequence into the sequence input box or upload a FASTA file.
   4. Set the primer design range and the expected product length.
   5. Set the primer annealing temperature.
   6. **Uncheck** "Specificity check", and check "Show results in a new window".
   7. Click "Get Primers" to obtain results, select suitable primer pairs, and record their sequences, start/end positions, and product sizes.
   8. Following the above method, design the second pair of primers within the expected product of the first pair, and design the third, fourth pairs, and so on.

9. **Primer Synthesis and Dissolution**
   10. Compile all designed primer sequences and submit them to a biological company for synthesis.
   11. After receiving the lyophilized primers, read the instructions carefully; briefly centrifuge before adding water.
   12. Dissolve with appropriate amount of sterile ddH₂O according to the instructions to a 100 μM stock solution, dilute to 10 mM for use, and store at -20°C.

13. **Nested PCR Amplification**
   14. **First-round PCR system:** High-fidelity polymerase Mix 22 μL + 10 mM F1 primer 1 μL + 10 mM R1 primer 1 μL + template DNA 1 μL. Vortex to mix and briefly centrifuge.
   15. **Touchdown PCR program:**
      - 95°C 5 min
      - 20 cycles: 90°C 5s, 95°C 20s, 70°C 30s, 72°C 25s
      - 15 cycles: 95°C 20s, 60°C 30s, 72°C 25s
      - 72°C 5 min, 4°C hold.
   16. **Subsequent PCR rounds:** Dilute the previous round's PCR product 100-fold with sterile water as the new template. Prepare the same system using inner primers and follow the Touchdown PCR program.
   17. **Note:** If TA cloning is planned, **the final round of PCR** must replace the high-fidelity polymerase with Taq polymerase.

18. **TAE Electrophoresis Verification**
   19. Prepare a 1% agarose gel: add 0.25 g agarose to 25 mL 1× TAE, heat in a microwave on medium-high until completely melted, cool to 50–60°C, and add nucleic acid dye.
   20. Load 5 μL of PCR product, load 5 μL Marker, and run at 120V for 30 min.
   21. Observe using a gel imaging system.

22. **Gel Extraction**
   23. Replace with fresh 1× TAE running buffer, prepare a 0.7% large-well recovery gel, load as much sample as possible, and run at a voltage below 100V for about 30 min.
   24. Under a small UV lamp, excise the target band with a scalpel, remove excess gel as much as possible, and place it into a 2 mL centrifuge tube.
   25. Use a gel extraction kit to extract and purify the DNA, finally eluting with ddH₂O preheated to 50°C.
   26. Measure the concentration of the recovered DNA using a NanoDrop and store at -20°C.

27. **Sequencing Verification and Data Analysis**
   28. Submit the purified PCR product to a biological company for Sanger sequencing.
   29. Open the `.ab1` chromatogram file from the sequencing results using MEGA software, observe the peak quality at the beginning and end, and record unreliable regions.
   30. Open the `.seq` file with Notepad, remove the unreliable bases at the beginning and end based on the chromatogram, add `>` and the file name at the beginning of the sequence, and save in FASTA format.
   31. Use the "Align" function in MEGA to import the two sequences from bidirectional sequencing.
   32. For the reverse complementary sequence, right-click and select "Reverse component".
   33. Click "Align DNA" to perform the alignment and assemble the complete full-length nucleic acid sequence based on the overlapping regions of the two sequences.
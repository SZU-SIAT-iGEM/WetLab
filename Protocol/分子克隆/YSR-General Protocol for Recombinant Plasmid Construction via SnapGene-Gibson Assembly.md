# 使用 SnapGene-Gibson Assembly 构建重组质粒通用 Protocol

## **序列与软件**

- 载体序列：从 SnapGene 官网下载或由实验室提供

- 基因 CDS 序列：从 NCBI 获取的目标基因编码序列

- 标准化元件：启动子、RBS 和终止子序列（从 iGEM 官网或文献中获取）

- SnapGene：已在计算机上安装并激活

## 仪器

- 计算机

## **实验流程**

1. **序列获取与准备**
- 获取基因 CDS： 进入 NCBI 官网搜索目标基因（如 ascF），选择正确的物种（如大肠杆菌 MG1655 菌株）。点击下载 FASTA 格式的 Coding Sequences (CDS) 序列。

- 获取标准元件： 在 iGEM 官网 Parts 部分获取启动子、RBS 和终止子的序列。

- 获取载体： 在 SnapGene 官网搜索载体名称并下载源文件。
2. **片段划分与文件创建**
- 在 SnapGene 界面中，将获取的所有序列分别创建为独立的 DNA 文件。

- 根据表达盒设计将序列划分为多个片段。例如，分为 5 个文件：载体、启动子-RBS-间隔序列、基因1-RBS-间隔序列、基因2、终止子。

- 注意： SnapGene 进行 Gibson 组装的片段长度至少需要 50 bp。如果某一片段（如 RBS-Spacer）过短，可在软件模拟时将其与相邻基因序列合并。但在湿实验前，必须人工重新设计并修改该区域的重叠引物和同源臂。
3. **SnapGene 虚拟 Gibson 组装**
- 打开载体文件页面，点击左上角 Actions（行动） -> Gibson Assembly（插入多个片段）。

- 线性化载体： 在右上角选择用限制酶线性化载体。按住 Shift 键同时选择两个合适的限制性内切酶。关键点： 在右侧确认要替换的区域，确保选择的是两个酶之间的目标区域，以免破坏载体元件。建议利用软件左下角的搜索功能，确保所选酶的识别序列不在待插入的基因序列内。

- 插入片段： 点击上方“片段”选项，在右侧依次选择并插入准备好的片段文件，确保顺序正确。

- 设计同源臂： 点击上方“产物”页面，点击右上角 Overlap PCR Primers（重叠 PCR 引物），SnapGene 将自动设计同源臂。确认参数（重叠区域 15–25 bp，Tm 值 50℃）。

- 点击 Assemble（组装），命名并保存生成的质粒文件。
4. **结果核验与湿实验准备**
- 检查生成的质粒图谱，确认各元件位置、方向和序列均无误。

- 人工修改引物： 若在 Step 2 中因长度限制合并了片段，需人工设计并修改真实实验所需的同源臂序列。

- 导出引物序列并合成，用于后续的 PCR 扩增和体外 Gibson 组装实验。

# General Protocol for Recombinant Plasmid Construction via SnapGene-Gibson Assembly

## **Sequences and Software**

- Vector sequence: Downloaded from the SnapGene official website or provided by the laboratory

- Gene CDS sequence: The target gene coding sequence retrieved from NCBI

- Standardized parts: Promoter, RBS, and terminator sequences (obtained from the iGEM official website or literature)

- SnapGene: Installed and activated on the computer

## **Equipment**

- Computer

## **Procedure**

1. **Sequence Retrieval and Preparation**
- Obtain Gene CDS: Go to the NCBI official website, search for the target gene (e.g., *ascF*), and select the correct species (e.g., *E. coli* MG1655 strain). Click to download the Coding Sequences (CDS) in FASTA format.

- Obtain Standard Parts: Retrieve the promoter, RBS, and terminator sequences from the Parts section of the iGEM official website.

- Obtain Vector: Search for the vector name on the SnapGene official website and download the source file.
2. **Fragment Division and File Creation**
- In the SnapGene interface, create independent DNA files for all retrieved sequences.

- Divide the sequences into multiple fragments based on the expression cassette design. For example, divide them into 5 files: Vector, Promoter-RBS-Spacer, Gene1-RBS-Spacer, Gene2, and Terminator.

- *Note:* The fragment length for Gibson assembly in SnapGene must be at least 50 bp. If a fragment (e.g., RBS-Spacer) is too short, it can be merged with the adjacent gene sequence during software simulation. However, before wet-lab experiments, the overlap primers and homology arms for this region must be manually redesigned and modified.
3. **Virtual Gibson Assembly in SnapGene**
- Open the vector file page and click Actions -> Gibson Assembly in the top left corner.

- Linearize the Vector: Select "Linearize vector with restriction enzymes" in the top right corner. Hold the `Shift` key to select two suitable restriction enzymes simultaneously. *Crucial:* Confirm the region to be replaced on the right side, ensuring that the target region between the two enzymes is selected to avoid destroying vector elements. It is recommended to use the search function in the bottom left corner of the software to ensure that the recognition sequences of the selected enzymes are not present within the gene sequences to be inserted.

- Insert Fragments: Click on the "Fragments" tab at the top, and select and insert the prepared fragment files in the correct order on the right side.

- Design Homology Arms: Click on the "Product" tab at the top, and click Overlap PCR Primers in the top right corner. SnapGene will automatically design the homology arms. Confirm the parameters (overlap region 15–25 bp, Tm value 50°C).

- Click Assemble, name, and save the generated plasmid file.
4. **Verification and Wet-Lab Preparation**
- Check the generated plasmid map to confirm that the positions, orientations, and sequences of all elements are correct.

- Manually Modify Primers: If fragments were merged due to length limitations in Step 2, manually design and modify the homology arm sequences required for the actual experiment.

- Export the primer sequences and synthesize them for subsequent PCR amplification and *in vitro* Gibson assembly experiments.

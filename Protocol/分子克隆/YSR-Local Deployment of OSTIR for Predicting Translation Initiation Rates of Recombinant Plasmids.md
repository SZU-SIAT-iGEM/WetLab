# 本地部署 OSTIR 预测重组质粒翻译起始效率

## 数据

- 重组质粒 DNA 序列

## 仪器

- 计算机

## 实验流程

1. 本地部署 OSTIR并验证安装

2. 准备直接复制的序列
   将重组质粒序列复制为连续字符串，去除 FASTA 标题行、空格、换行和数字。如有 RNA 序列，将 `U` 转换为 `T`，并统一为大写字母。确保序列包含完整的 5′ UTR、RBS、起始密码子以及起始密码子下游至少 30–50 nt。

3. 通过命令行直接运行 OSTIR

4. 解读结果
   打开 ostir_results.csv，读取目标基因起始密码子（通常为 ATG）处的预测翻译起始速率。检查是否存在预测速率高于目标位点的隐蔽起始密码子，这可能提示翻译起始旁路或框外翻译风险。若比较多个 RBS 变体，可按预测速率进行相对排序。

# Local Deployment of OSTIR for Predicting Translation Initiation Rates of Recombinant Plasmids

## **Data**

- Recombinant plasmid DNA sequence

## **Equipment**

- Computer

## **Procedure**

1. Locally deploy OSTIR and verify the installation.

2. Prepare the directly copied sequence.  
   Copy the recombinant plasmid sequence as a continuous string, removing FASTA header lines, spaces, line breaks, and numbers. If it is an RNA sequence, convert `U` to `T` and use uppercase letters uniformly. Ensure the sequence contains the complete 5′ UTR, RBS, start codon, and at least 30–50 nt downstream of the start codon.

3. Run OSTIR directly via the command line.

4. Interpret the results.  
   Open `ostir_results.csv` and read the predicted translation initiation rate at the start codon of the target gene (usually ATG). Check whether there are cryptic start codons with a predicted rate higher than the target site, which may indicate a risk of translation initiation bypass or out-of-frame translation. If comparing multiple RBS variants, they can be ranked relatively based on their predicted rates.

## References

1. barricklab/ostir GitHub repository: https://github.com/barricklab/ostir

2. OSTIR Wiki — Command Line Usage: https://github.com/barricklab/ostir/wiki/Command-Line-Usage

3. OSTIR Wiki — Installation: https://github.com/barricklab/ostir/wiki/Installation

4. OSTIR Wiki — Python Module Usage: https://github.com/barricklab/ostir/wiki/Python-Module-Usage

5. Bioconda ostir package metadata (Python ≥ 3.8, ViennaRNA ≥ 2.4.18)

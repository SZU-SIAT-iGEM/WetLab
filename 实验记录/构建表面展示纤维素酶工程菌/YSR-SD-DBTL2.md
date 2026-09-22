# DBTL 2: Re-evaluating the antibiotic selection system

## Overview

上一轮实验暴露出了一个此前被我们忽略的 assumption：

> 能够在 antibiotic plate 上生长的 colony，并不一定就是目标 transformant。

因此，我们决定重新测试整个 SmR-based selection system，并加入未经 transformation 的 DH5α 和 MG1655 WT 作为 negative control。

这一轮我们同时比较不同 antibiotic condition 下：

- 工程菌，即尝试转入 pCDF-based SmR plasmid 的 DH5α 和 MG1655；

- 野生型 DH5α 和 MG1655 WT，未转入任何 plasmid。

我们设置了三种 selection condition：

1. **链霉素平板**：观察工程菌是否能够形成 colonies；

2. **壮观霉素平板**：同时涂布工程菌和 WT，判断壮观霉素能否抑制 WT；

3. **链霉素 + 壮观霉素平板**：同时涂布工程菌和 WT，判断双抗生素组合是否能提高筛选严谨性。

如果 selection system 工作正常，那么：

- 工程菌应当能够生长；

- WT 应当无法生长。

如果 WT 同样能够生长，那么此前根据“selection plate 上有 colony”判断 transformation 成功的逻辑就不再成立。

我们重新制备 MG1655 competent cells，并进行 pCDF-based SmR plasmid transformation。

同时保留未经任何 plasmid transformation 的 DH5α 和 MG1655 WT。

随后将各组细胞分别涂布于以下平板：

- 链霉素平板：工程菌；

- 壮观霉素平板：工程菌、WT；

- 链霉素 + 壮观霉素平板：工程菌、WT。

所有平板在相同条件下过夜培养。

## DBTL Cycle 2.1

## What does the streptomycin plate alone tell us?

### Design

链霉素平板是最初 DBTL 1 中使用的 selection condition。

我们首先保留这一条件，观察工程菌是否能够形成 colonies。

但需要注意的是，这一轮链霉素平板只测试了工程菌，没有同时设置 WT negative control。

因此，即使工程菌能够生长，也不能单独证明 streptomycin selection 具有区分 WT 与 transformants 的能力。

### Build

将转入 pCDF-based SmR plasmid 的工程菌涂布于链霉素平板，并在 37℃ 下过夜培养。

### Test

结果显示，链霉素平板上的工程菌能够形成单菌落。

这一结果与 DBTL 1 中观察到的现象一致。

<img width="2476" height="2476" alt="SD链霉素工程菌" src="https://github.com/user-attachments/assets/3cadb4e6-14e9-4ba4-bad1-6bf3cfe65e27" />

图2.1-1 划线接种工程菌的链霉素平板

### Learn

链霉素平板上工程菌能够生长，只能说明，在链霉素筛选条件下，工程菌组能够形成 colonies，但并不能证明这些 colonies 一定是携带目标质粒的 transformants。

原因如下：

- 该条件没有同时设置 WT negative control；

- 仅凭工程菌生长，无法排除 background growth；

- 也无法判断 streptomycin 是否真正抑制了没有 resistance plasmid 的细胞。

因此，链霉素平板上的 colony formation 仍然不能作为可靠的 transformation evidence。

## DBTL Cycle 2.2

## Can spectinomycin provide a more reliable selection condition?

### Design

为了进一步验证问题是否仅仅来源于第一批 streptomycin plates 或 antibiotic condition，我们重新购买了 spectinomycin，并重新制备 selection plates。

这一轮实验我们设置了 WT negative control。

我们的目标是测试：更换 antibiotic condition 后，是否能够真正建立 WT 与 transformants 之间清晰的生长差异？

### Build

我们重新进行 transformation，并将：

- 工程菌

- 未经 transformation 的 DH5α 和 MG1655 WT

分别涂布于新的 spectinomycin-containing plates，所有组在 37℃ 培养条件下过夜培养。

### Test

结果显示，壮观霉素平板上，工程菌能够形成 colonies；同时，DH5α 和 MG1655 WT 也能够在壮观霉素平板上形成 colonies。

也就是说，WT 没有被壮观霉素有效抑制。

<img width="2476" height="2476" alt="SD壮观霉素工程菌" src="https://github.com/user-attachments/assets/81025138-f89b-450c-9bfc-56c532f44dc2" />

图2.2-1 涂布接种工程菌的壮观霉素平板

<img width="2476" height="1270" alt="SD壮观霉素WT" src="https://github.com/user-attachments/assets/1752c108-7c4f-4055-9fc2-412f412968ca" />

图2.2-2 涂布接种野生型菌株的壮观霉素

### Learn

这一结果与我们的预期明显不符。如果 spectinomycin selection 工作正常，那么，工程菌应当生长，WT 应当无法生长，但实际结果是 WT 同样能够生长。

这说明，spectinomycin 单抗生素条件在我们的实验体系中无法可靠区分 WT 与 plasmid-containing cells。

因此，我们观察到的“工程菌在 antibiotic plate 上形成 colony”也并不能证明 plasmid transformation 成功。

## DBTL Cycle 2.3

## Does combined streptomycin + spectinomycin selection improve stringency?

### Design

由于壮观霉素单药不能抑制 WT，我们进一步测试双抗生素组合是否能够提高 selection stringency。

我们使用链霉素 + 壮观霉素双抗生素平板同时涂布：

- 工程菌

- 未经 transformation 的 DH5α 和 MG1655 WT

如果双药组合能够抑制 WT，而工程菌仍然生长，则说明双药 selection 可能比单药更可靠。

如果 WT 仍然生长，则说明 SmR-based selection system 整体无法承担筛选 transformants 的功能。

### Build

我们重新制备链霉素 + 壮观霉素双药平板。

随后将工程菌、DH5α 和 MG1655 WT 分别涂布于双药平板上，所有组在 37℃ 培养条件下过夜培养。

### Test

结果显示，链霉素 + 壮观霉素双抗平板上，工程菌能够形成 colonies；同时，DH5α 和 MG1655 WT也能够在链霉素 + 壮观霉素双抗平板上形成 colonies。

也就是说，即使联合使用两种 antibiotic，WT 仍然没有被抑制。

<img width="2476" height="2476" alt="SD双抗工程菌" src="https://github.com/user-attachments/assets/b2ab51cc-a46e-4bb1-bba5-175cdebf3b72" />

<img width="2476" height="1210" alt="SD双抗WT" src="https://github.com/user-attachments/assets/9d4f1770-6924-4724-9719-8c8c22138b7c" />

### Learn

连续三种 selection condition 的结果可以总结为：

| Selection condition | 工程菌        | WT         |
| ------------------- | ---------- | ---------- |
| 链霉素平板               | 有 colonies | 未设置        |
| 壮观霉素平板              | 有 colonies | 有 colonies |
| 链霉素 + 壮观霉素平板        | 有 colonies | 有 colonies |

我们能够从中提取的关键信息是：WT 在壮观霉素单药和链霉素 + 壮观霉素双药条件下都能够生长。

这说明问题并不是简单地由某一种 antibiotic 或某一个浓度条件造成。

至少在本实验体系中：

spectinomycin 单药不能抑制 WT；

streptomycin + spectinomycin 双药也不能抑制 WT；

因此 SmR-based selection 无法可靠地区分 WT 与 transformants。

在这里，我们不需要立即证明 WT 生长的具体分子机制。

对于工程迭代来说，更关键的是：

这个 selection system 已经无法继续承担“识别 transformant”的功能。

因此，即使继续优化 Gibson assembly，只要 selection 本身不能可靠工作，我们仍然无法判断获得的 colony 究竟是不是目标工程菌，所以在下一轮中，我们需要重新设置 selection condition，丢弃 SmR-based selection。

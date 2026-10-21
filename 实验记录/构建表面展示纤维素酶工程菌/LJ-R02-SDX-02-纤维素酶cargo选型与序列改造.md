# SDX-02 纤维素酶 cargo 选型与序列改造实验结果

## Objectives

确定三种目标纤维素酶，并完成适合融合表达的序列改造，使其能够作为 INP 展示系统的 cargo（2025.12.11–2026.4.24）。

## Methods

1. 酶选型：选择 *Clostridium thermocellum* 来源的 Cel48S（GH48，外切型）、Cel9K（GH9，外切型）与 Cel5L（GH5，过程性内切型），以 endo–exo 组合覆盖纤维素降解所需的协同作用；
2. 序列改造：删除三种酶中不再需要的 dockerin 结构域（本系统依赖 INP 锚定，不依赖 scaffoldin–dockerin 组装）；对合成序列进行大肠杆菌密码子优化。

## Result

确定“三种酶分株表达、后续以 microbial cocktail 组合使用”的方案，以降低单株的质粒负担与表达压力。三个 construct 共用调控元件、锚定模块与融合策略，仅在 cargo 上不同——这一设计后来成为 SD-11 失败归因的结构基础：三者共同失败更可能指向共享架构，而非三个独立的克隆事件同时出错。

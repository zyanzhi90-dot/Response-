# 证据、Claim、术语与引用

本文件包含 supporting discipline SD-01 至 SD-03。它们负责让 TIE-native response 正确、可追踪和一致，不改变 `01`–`03` 中的写作节奏。

## SD-01 concern—evidence—claim 对齐

### 1. 先确定判断标准

对每个 concern 写出 reviewer 实际要判断的对象。若 comment 混合不同概念、指标或尺度，只建立理解所需的最小框架，并为每一维配置直接 evidence。

检查链：

> concern → 判断标准 → 动作 → 直接 evidence → evidence 覆盖范围 → response conclusion

相邻证据、代理指标或另一方法的属性不自动等价。可以使用多种 evidence，但必须说明每种 evidence 分别回答什么。

**Evidence identity 与 scope label：** 内部分析每项 evidence 时，依据当前项目 primary evidence 准确判断其归属、适用范围、成立条件和可支持的 claim boundary；内部可细分到保证判断正确所需的粒度。分析与分类结果不自动进入最终 Response。只有 reviewer 为理解回答、判断 evidence 或 claim、消除真实歧义确实需要的信息，才以最小充分形式外显。本检查只负责 evidence identity、scope label 与 claim boundary，不规定段落顺序、block 数量或英文句型。

### 2. Claim boundary

- 理论 claim 写明成立条件。
- 实验 claim 限于实际测试的对象、条件、平台和评价量。
- 单一指标改善不推出总体优势。
- 部分支持不能写成完全支持。
- 与当前 conclusion 有实质关系的不利 evidence 必须保留，并用于收紧 claim。
- 缺少直接 evidence 时，显式标记未验证、降低 claim 或保留 limitation，不用更多文字掩盖缺口。

TIE R2-2 的有条件证明提供正面组织；R4-4 用外扰实验覆盖量化、延迟和速度估计等多个独立问题，是代理 evidence 的反例。

### 3. 对新 response 的最低检查

每个结论都能回指一项足够直接的 evidence；每项 reviewer 要求都能定位到已完成、部分完成、未完成或有理据不同意中的一种状态。写出 response 不能证明实验或修改已经完成。

### 4. 独立 mathematical-correctness gate

若 response 回答定义、公式、推导或证明，须回到当前项目的原始数学材料逐项核验：矩阵/向量维度、定义域与时间区间、量词和完整成立条件；每个等式及不等式的中间步骤，尤其 `>` 与 `≥` 的严格关系；假设是否足以推出所写 conclusion；新旧 equation number、符号和稿件版本是否一致。**写出了推导不等于推导数学上成立。**B3 只给局部推导的组织，C1 的完整 proof 仅为单例参考；此 gate 是新 response 的正确性检查，不是江 TIE 作者稳定做到的表达。TIE R2-2 的严格不等号/矩阵表述和 R2-3 的 SVD 维度/符号均提示必须独立核查。

**Provenance:** CK-003、CK-004、CK-011、CK-012；Nature/ARS concern—action—evidence 与 claim–source alignment 只作 supporting。

## SD-02 source、provenance 与 citation

### 1. 来源职责

| 来源 | 可以决定 | 不可以决定 |
|---|---|---|
| reviewer 原 comment | concern 与措辞边界 | 实验是否已完成 |
| 当前稿件/作者确认 | 定义、术语、符号、已有论述与真实修改 | TIE 风格 |
| 正式实验输出/图表 | 数值、曲线关系、测得结果 | 变量定义或普遍 claim |
| TIE PDF | 组织、推进、图文位置和表达习惯 | 新项目事实 |
| 阶段裁决/派生总结 | 定位、边界和历史 provenance | 覆盖 primary source |
| 外部方法原文/可靠文献 | 方法身份与外部 claim | 替当前实验提供结果 |
| Nature/ARS | 完整性、事实性、claim/source/consistency 纪律 | 覆盖 TIE 的文风与组织 |

### 2. Citation

外部方法、前作或文献在首次承担识别、比较或 evidence role 时建立可追踪来源。是否需要新 citation、首次位置、编号和 caption 是否重复，取决于稿件、来源性质、期刊规范和上下文。

- 不猜 DOI、作者、编号或 revised-manuscript citation。
- 方法名出现不自动意味着每次都要重复 citation。
- response citation 与 manuscript citation 若属于不同体系，应保持各自可解析，不能互相推断编号。
- 派生总结中的 citation 线索必须回到可核验来源。

### 3. Benchmark 迁移

从 TIE 迁移段落动作、证据位置、图组推进、信息密度和收束功能；不复制其拼写/语法错误、过强 claim、具体平台、参数或偶然短语。单一范例的观察只有在 PDF 原文、阶段裁决和适用边界共同支持时才进入核心。

**Provenance:** CK-013、CK-017、CK-018；阶段 1 来源索引与 TIE PDF；Nature/ARS 只补足 provenance 与不可编造原则。

## SD-03 术语、符号与交叉引用一致性

### 1. 首次定义与后续稳定

reviewer 首次需要理解关键指标、术语或符号时，同时给出清楚含义和正式符号。后文稳定使用，不要求每次重复完整定义。正式名称与符号必须来自当前稿件或实验 primary source，不能从 TIE、文件名或脚本创造。

**符号一致不等于 reviewer 可读性充分。** 后文可在紧邻重复或局部式链中只用符号；进入新的段落/证据块，或陈述关键 criterion、主要结果、比较及结论时，若裸符号会迫使 reviewer 回查定义，应就近重现技术含义与符号的对应。这里要求读者能连续判断对象，不设每次重写全称的格式规则；具体表达由 `02` 的 SL-04/SL-05 实现。

### 2. 指代与对象

当多个方法、指标、任务、figures 或 panels 并列时，显化必要对象。实际无歧义时允许代词、简称和局部 panel 引用。目标是唯一可解析，不是机械重复全称。

逐句核对关键限定短语的**科学附着**：它实际修饰的实验对象、操作、条件、baseline、metric 和范围，须与当前项目 primary evidence 的真实关系一致。不能因介词、量词或副词在语法上成立，就把某项 parameter/setting 改称另一实验层级，或把部分 evidence 扩成总体 claim；范围与结论强度仍由 SD-01 判定，`02`/`06` 在 phrase level 调用该判定。

### 3. 修改同步

术语、符号、单位、数值、comparison label、figure/panel、caption、正文、response citation 和修改位置必须指向同一最新版本。每次实质修改只重开受影响链条，但该链条必须同步到底。

### 4. 位置真实性

只有在 artifact 中可验证时才写“已加入”“已修改”“见 Fig./Table/Section/Page/Line”。页码或行号不稳定时，可用 section、paragraph、figure 或显式 placeholder，不能编造精确位置。

TIE 自身的 Figs. 2–5/实际涉及 Fig. 6、Table II/Table III/排版 Table 2，以及 reviewer 编号重复均为一致性负例，不可迁移。

**Provenance:** CK-002、CK-010、CK-014、CK-019 的一致性部分；TIE R1-2 与 R4-6 的编号错误为负例；Nature package consistency 只作 supporting。

## 4. 支持层停止线

完成本文件的检查后，不得因“一般学术英语更规范”“另一期刊常这样写”或外部 Skill 的固定 phrase 再改写已经满足 TIE-native 逻辑的段落。支持层发现事实、覆盖、claim、source 或 consistency 缺陷时，回到受影响的核心单元定点修正；没有缺陷就停止。

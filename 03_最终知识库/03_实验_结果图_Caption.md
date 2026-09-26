# 实验、结果图与 Caption

本文件实现 TN-03、TN-04 和 TN-05。核心目标是让 reviewer 沿正文阅读路径知道：新增实验怎样进入具体设置和证据，图中比较了什么，以及哪些可观察现象回答 concern。若新 response 需要结论，其范围另由 `04` 审计。

## TN-03 实验或比较如何进入

### 1. 按任务进入实验或比较

新增实验的可验证推进是 **action → concrete setup → evidence locator → observation**（B4/A5）。可先报告已做测试，再给通道、强度、公平参数或平台、任务；若目的尚不清楚，再说明它回答哪个 concern 或 criterion。purpose 不是所有实验的固定首句。比较场景先让 baseline 的已有作用贴近真正区分维度（B5），再按需要进入图表或技术解释；完整多控制器图表路径仍仅是 C3 参考。

实验动作后给理解证据所需的具体设置：

- 比较方法或对象；
- 评价量；
- 会改变解释的实验条件；
- 公平比较所需的共同条件；
- reviewer 判断所需的参考线或阈值。

不在此处复述完整 Methods。若某实现细节正是 reviewer concern，才把它提升为 evidence。

### 2. 建立 evidence block

对服务同一子问题的多项实验：

1. 集中说明实际需要的共同目的和公共设置；
2. 连续呈现相关图组或表格；
3. 保留各实验不可替代的条件、数值、结果和实质不利比较；
4. 集中读出与 concern 有关的关键 observation；若确需结论，再由 `04` 核查其 evidence boundary。

不要让每张图各自重启完整 mini-response。若两组实验回答不同判断标准，应分成两个 block，而不是为了形式合并。

### 3. TIE 原文校准

- R1-2：目的与公共噪声模型集中说明，再按三个强度组织成图组；图组前集中读出扰动幅值与参数估计表现。
- R3-2：先解释比较对象的意义，再宣布新增 PID/MBAC 比较；多幅 tracking figures 与参数表连续进入，随后集中读图。完整多控制器图表链仅作 C3 参考。
- R4-3：真实机器人实验较短，动作、平台、轨迹、结果图和 observation 形成单一紧凑 block；随后的一般 robustness 结论属 source defect。
- R4-6：原文表格进入前说明表中列和比较对象；完整 Table 请求仅作 C5 参考，R3-2 中复用同表不算独立复例。原文 Table II/Table III/Table 2 不一致是负例。

这些例子说明 block 可以在图前读结果，也可以在图后集中读取。硬规则不是“结果句必须位于图后”，而是 evidence 与其解释保持低跳转、可唯一定位。

## TN-04 figure、caption 与 body 的功能分工

### 1. Figure

Figure 承担可视 evidence。它必须保留与 concern 有关的曲线、方法、条件、单位、panel 对应和必要参考线。不能用文件名、脚本标签或代码图注替代正式 figure 的含义。

### 2. Caption

Caption 负责让读者识别图：对象、方法、条件、指标、panel 和必要参考线。它不承担完整 response 论证，也不必机械重复正文中的每个结果或 citation。

“自足”是功能目标：即使 reviewer 先看图和 caption，也不应把方法、条件或 panel 对错。所需密度由图复杂度与期刊规范决定。TIE 原文的 captions 通常简短，只写图的识别信息；当前知识库在不改变这种简洁性的前提下，要求消除实际歧义。

### 3. Body

正文负责：

- 在需要显化目的时说明图回答哪个 concern；
- 读出与 concern 有关的关键现象；
- 解释现象如何回答判断标准；
- 报告会改变结论的实质不利结果；
- 在确需 conclusion 时说明 evidence 支持到哪里，并由 `04` 核查其范围。

正文不逐字重述 caption，caption 也不替正文完成推论。

### 4. 邻近和定位

claim 与 evidence 的“相邻”是低跳转成本，不是像素规则。可通过紧邻排版、明确 cross-reference 或稳定 location mapping 实现。多图并列时，结果句必须让 reviewer 唯一识别具体 figure/panel；唯一先行项时可以自然使用局部 panel 或代词。

**Provenance:** CK-007、CK-009、CK-010；TIE R1-2、R3-2、R4-3、R4-6；supporting 只补足 traceability 与 caption ambiguity 边界。

## TN-05 结果读取

### 1. 结果句的构成

结果读取句至少使下列观察关系可恢复：

> 哪个方法/对象 + 哪个指标 + 哪个条件/任务 + 观察到什么

不要求所有元素堆在一个句子里；若 concern 需要解释该现象的意义，可在相邻句说明与 criterion 的关系。定性 observation 也可以成立，不要求每组结果都有数字。

### 2. 读图顺序

按 reviewer 判断顺序读取，而非按画图或文件生成顺序读取：

1. 先读决定 concern 的主指标；
2. 再读必要的对照或边界；
3. 需要进一步解释时，才进入 comparison 或 inference；结论不属于固定读图末步。

多个 panels 共同完成一个判断时，集中说明它们的分工；不同 panels 回答不同 concern 时分开解释。

### 3. 不利结果

与当前 concern、比较或 claim 有实质关系的不利结果必须报告。正确处理是：

1. 如实说出不利关系；
2. 说明它是否影响目标 criterion；
3. 据此缩小或校准 conclusion。

不得删除不利比较，只保留另一项有利指标来暗示全面优势。也不需要罗列与该 concern 无关的所有负面观察。

### 4. 从结果到 conclusion

TIE 可验证的子链是 **evidence locator → observation**。是否另写 conclusion 由 reviewer concern 和新稿 evidence 决定；若写，结论不得超过测试对象、条件、平台和指标，这属于 `04` 的 evidence→claim gate，不是江 TIE 作者稳定做到的实验末块。多图可以集中读取，避免逐图重复同一判断。

**Provenance:** CK-006、CK-011、CK-012、CK-015；TIE R1-2/R3-2 的集中读图与 R4-3 的有限实验链；阶段 1 正式图中的不利比较只作为机制验证，不迁移其变量和数值。

## 4. 多图/多实验写作决策表

| 当前状态 | 下一步 |
|---|---|
| 多项实验回答同一子问题且共享设置 | 建一个 evidence block，公共设置集中说明 |
| 实验共享目的但有独有条件或不利结果 | 保留独有 evidence，不因压缩删除 |
| 图多但只需一个综合判断 | 连续放置图组，集中读取一次 |
| 图分别回答不同判断标准 | 分开 block 或明确分段，不强行汇总 |
| 多个 figures/panels 可能混淆 | 显式写 figure/panel 对应 |
| caption 已能识别图，正文需解释 | 正文只写现象、关系和边界 |
| 正文开始逐字复述 caption | 删除重复，保留 reviewer 判断信息 |
| 发现实质不利比较 | 报告它并收紧 claim |

## 5. 图文验收

1. 从实验动作及必要的 purpose，能否知道这组 evidence 回答什么？
2. 只看 figure 与 caption，能否识别方法、条件、指标和 panel？
3. 只看图旁正文，能否知道 reviewer 应观察什么？若有结论，其边界能否由 `04` 核验？
4. 是否存在悬空图号、模糊 panel、旧编号或 caption/body 冲突？
5. 是否把每幅图写成重复 mini-response？
6. 是否隐藏了会改变当前 claim 的不利 evidence？
7. 是否把可选结论误当成每组 evidence 的必需末句，或重复同一判断？

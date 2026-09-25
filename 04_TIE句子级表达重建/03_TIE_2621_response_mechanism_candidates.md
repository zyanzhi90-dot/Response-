# TIE_2621 候选 scene-level response mechanisms 与 language fingerprint

## 0. 证据边界与判级方法

主证据是已验收的 `02_TIE_2621_scene_response_corpus.md`（S01–S16）；`Response_TIE_江_No.17-TIE-2621.pdf` 仅用于必要的原文回查。下文 `PDF p.` 均指 PDF 物理页。`00_TIE_2621_sentence_realization基准.md` 只读，不参与决定分类。本文件只建**候选机制**，不构造固定回复格式，不推断 TIE_2621 以外的规范。

判级单位是**独立 reviewer situation 与独立证据块**，不是句子出现次数。S10/R3-C2（PDF pp.12–17）和 S16/R4-C6（pp.20–21）几乎复用同一参数表说明，表格材料只算一份；S14/R4-C4（pp.19–20）复述 S01/R1-C2 的外扰测试，也不算第二套独立鲁棒性实验。一个 scene 可同时支持某个跨场景机制，并让其独有组织方式停留在单例级。

- **LEVEL A — CORE / CROSS-SCENE**：多个独立 scene 的语义推进重复；仅迁移该推进关系，不迁移原文缺陷或全部句序。
- **LEVEL B — SCENARIO-SPECIFIC**：同类 situation 有重复证据，或任务本身要求这种功能承接；只在触发条件满足时启用。存在共用材料时从严降级。
- **LEVEL C — SINGLE / REFERENCE ONLY**：一条独立 scene 才展示完整路径；只能提示要核查哪些状态，不能作为生成规则。
- **SOURCE DEFECT**：不进入 A/B/C 的可生成部分；高频错误也不能升级。

本轮候选编号固定为 **A1–A6（6 条）、B1–B6（6 条）、C1–C6（6 条）**。分类不是让新 comment 必须只选一个标签；先拆其真实 concerns，再为每个 concern 判断证据强度。

## 1. Reviewer-situation taxonomy

| Situation 与判别触发 | 证据 scenes（Referee / Comment；PDF 页） | 证据强度 | 是否足以形成 reusable mechanism |
|---|---|---|---|
| **A. 局部 typo / wording / Figure clarification**：审稿人给出可定位、可替换的错词、句子或图示不清；修订对象明确 | S02/R1-C3 p.4；S03/R2-C1 p.7；S11/R4-C2a p.18；S12/R4-C2b p.18 | 四个独立 scene；Figure clarification 仅一例 | **是，B1**，限“对象明确、无未答技术争点”；图示本身如何改进仍无复例 |
| **B. 局部 equation / definition 不清**：某式、符号关系或极限局部有疑点，需替换定义并解释 | S05/R2-C3 pp.8–9；S07/R2-C5 pp.9–10；S03/R2-C1 p.7 有 wording + 公式边缘证据 | 同类两例，具体 SVD/极限各单例 | **是，B2** 的“修订对象 → 局部解释/新式 → 可查摘录”；不推出固定数学论证 |
| **C. 要求详细 derivation**：审稿人指出等号/不等式之间缺步骤 | S06/R2-C4 p.9；S08/R2-C6 p.10 | 两个独立推导请求 | **是，B3**，限把前提、代数链和使用的事实接起来 |
| **D. 理论条件或证明受到核心质疑**：某前提若不成立会使 theorem/proof 整体开放 | S04/R2-C2 pp.7–8 | 单例，且严格不等式有待核验 | **否，C1**；保留“condition → derivation → implication”的参考路径，不作稳定完整机制 |
| **E. 新增 experiment / robustness test**：审稿人指出证据缺口，需交代新增操作、设置和结果 | S01/R1-C2 pp.3–6；S13/R4-C3 pp.18–19；S14/R4-C4 pp.19–20 仅复用 S01 的扰动证据 | S01、S13 是两种独立实验场景；鲁棒性专门测试只有 S01 | **是，B4** 的条件型实验推进；不把“外扰”当所有 robustness concern 的答案 |
| **F. comparison + Figure/Table evidence**：要求新增基线，展示差异及相应图表 | S10/R3-C2 pp.12–17；S16/R4-C6 pp.20–21 复用参数表；S09/R3-C1 pp.11–12 有概念比较而非同类图表 | 图像+表的完整综合比较只有 S10 一例 | **部分**：基线→差异读取为 **B5**；完整 PID/MBAC/参数表链仅 **C3** |
| **G. novelty / prior-work difference**：审稿人认为前作已做核心方法 | S09/R3-C1 pp.11–12；S15/R4-C5 p.20 只重合部分 method rationale | 完整 novelty defense 仅一例 | **否，C2**；三贡献维度和篇幅不能泛化 |
| **H. method motivation / why this method**：问已有方法可用时为何选所提方案 | S15/R4-C5 p.20；S10/R3-C2 pp.12–13 有部分 rationale | 完整“为何用”独立 scene 仅 S15 | **否，C4**；背景→局限→方案可参考，具体证明强度另核 |
| **I. 明确 Table/data presentation**：要求列出参数、算法和真值供直接查阅 | S16/R4-C6 pp.20–21；S10/R3-C2 p.17 复用同表 | 一份独立表格材料 | **否，C5**；列说明和读表动作可观察，但没有第二个独立 table task |
| **J. 单个 comment 含多个独立 concern**：同条中有 typo + 技术说明，或多 baselines + experiment，或文献 + 现实干扰 | S05/R2-C3 pp.8–9；S10/R3-C2 pp.12–17；S14/R4-C4 pp.19–20 | 三个独立多 concern scenes；S14 有未覆盖子问 | **是，B6**，限不同 concern 引出不同 action/explanation/evidence 功能块；覆盖充分性另审 |

分类时先问：审稿人的要求是否只是改一个可定位对象，还是需要新增推导/证据？如果一条评论同时涉及多个动作，就同时标 J 和对应的 A–I。R4-C4 的 quantization、delay、dirty derivative 不能因为作者只做外扰测试就改标为“普通外扰请求”；taxonomy 按 reviewer 的真实问题定，答复覆盖情况另记。

## 2. Scene-level response organization：有条件触发的状态序列

以下 `Entry / Block / Transition / Stop` 是功能状态，不规定句数、连接词或固定标题。礼貌开场可存在，但它本身不完成实质答复。

### 2.1 局部 correction（B1；taxonomy A）

- **Trigger**：错误对象与目标改动可直接定位，且没有独立的证明或实验要求。
- **Entry**：从被指出的 `typos / statement / Figure 1` 进入，而不是先回顾领域背景。
- **Blocks**：对象及已完成修改 → 必要时给替换句/新图说明 → Section/Page 或蓝色标记。只有当 reviewer 的质疑仍涉及“为何正确”时，才进入技术解释。
- **Transition**：对象已明确且动作可核对，才给 location 或摘录；若摘录本身已展示修订，继续辩论没有原文支持。
- **Stop**：改动对象、核对方式与位置已交代即停。S02 p.4 在校对/蓝色标记后停；S12 p.18 在 Figure 1 修改和位置后停；S03 p.7 则在位置之后还给修订句与公式，因此位置不是终点标志。
- **Variation / boundary**：S11 p.18 因涉及全稿校对，多一个外部语言协助动作；S12 未说明图的具体输入输出，显示这种短答可以留下 coverage gap，不能把“短”当充分性的证明。

### 2.2 局部 equation / definition（B2；taxonomy B）

- **Trigger**：审稿人问定义、符号关系或极限；问题范围局限在某式前后。
- **Entry**：先报准确的修订对象：Eq. (18) typo + 前文叙述（S05 pp.8–9），或 F(t) 定义 + 零/非零特征值说法（S07 pp.9–10）。
- **Blocks**：已改动作 → 使新式成立所需的局部 technical fact/definition → 修订式或短摘录 → location（可先于摘录）。
- **Transition**：只有对象被修订后，才需要解释其数学含义；解释足以回应局部问题后，不扩为 Theorem 1 级证明。
- **Stop**：新定义/条件和相应结果均可在 excerpt 中找到即停。S05 以 SVD 对象关系结束，S07 以 F(t) 与极限摘录结束。
- **Boundary**：S05 的维数/正交表述和 S07 的参数条件需独立检查，不能从“作者贴出公式”推断公式已正确。

### 2.3 缺失 derivation（B3；taxonomy C）

- **Trigger**：审稿人指出某个等号或不等式的中间运算缺失。
- **Entry**：先映射旧式号到修订式号并报告已补推导（S06 p.9；S08 p.10）。
- **Blocks**：先列等式链实际使用的前提/恒等式 → 展开中间式 → 指认末步所用事实或新增符号 → 需要时回到论文位置。
- **Transition**：前提必须可见才进入代数链；公式已经连通 reviewer 指出的跳步时，才允许给推论。S06 用 `VcᵀVc=I` 开始，S08 用 `(22), FΦr=..., Bc=...` 开始。
- **Stop**：所问的“从哪一步到哪一步”已能沿公式逐行追踪；S08 更进一步定义 `μd,ρd` 与紧集结论，因为它们属于所贴推导末行。
- **Variation**：S06 的自然语言短、式链较短；S08 的不等式长。长度由缺失步骤决定，不由“derivation”标签统一规定。

### 2.4 核心理论条件/证明（C1；taxonomy D，参考实例）

- **Trigger**：审稿人指出关键性质可能不成立，且该性质支撑 theorem/proof。
- **Reference path**：先界定命题成立的**条件**（S04/R2-C2，PDF pp.7–8 的 PE）→ 从定义取得窗口积分下界 → 对权重建立下界 → 连接窗口与 D 的积分 → 在同一条件范围内读出 implication → 报 Remark 的位置及摘录。
- **Transition/stop**：一个条件尚未进入 proof 时，不能跳到无条件结论；所有用于下界的条件和时间范围均交代后才可停止。
- **Evidence limit**：仅 S04 一例，而且严格 `>`、`D(t)>σ` 写法有问题。可用它提醒新评论需要明确数学责任；不能生成“所有理论质疑都先写 PE 背景再贴整段 Remark”的规则。

### 2.5 新增 experiment / robustness evidence（B4；taxonomy E）

- **Trigger**：reviewer 指明现有证据缺少现实条件或真实平台，需要实际新增测试。
- **Entry**：承接缺口或直接报测试动作。S01/R1-C2 p.3 先同意测量噪声的关联；S13/R4-C3 p.18 直接报 Baxter 实验。两条路径都进入“做了什么”的可核对状态。
- **Blocks**：test action → concrete setup（扰动通道/强度/公平条件，或平台/任务）→ evidence locator → 观察测得内容；manuscript location 可在摘录前或结果后。S01 p.3–4 的“测量位置噪声、σ、Figs.1–6、最大偏差/估计表现”；S13 pp.18–19 的“Baxter 左臂、轨迹、估计图、nominal 对比”。
- **Transition**：purpose 若出现，只解释为何开展；有了具体操作和 setting，才可指图；图后读取 observation。原文在 observation 后还给过较宽的 robustness claim，但其范围不属于已验证的 B4 mechanism。
- **Stop / evidence-quality gate**：B4 可预测到 observation；原文有时再写 claim/location 并结束。是否继续 conclusion、claim 是否与测试范围相称，须另做 evidence-quality audit。S14/R4-C4 pp.19–20 用一般外扰答量化/延迟/脏微分，不能视为这些因素的独立实验依据。
- **Variation**：S01 的 purpose-fronting 是单场景措辞；S13 用 `In addition`。真实机器人 setup 和噪声强度 setup 所需字段不同。

### 2.6 比较中的 baseline → 差异读取（B5；taxonomy F 的可复用子机制）

- **Trigger**：必须说明所提方法相对已有方法/控制器的区别，且 comparison 维度可明确。
- **Blocks**：指出 baseline 的真实功能或可取表现 → 明确本文比较维度 → 同一维度下读差异 → 必要时用 Figure/Table 支持。S09/R3-C1 pp.11–12 先承认 [20] 已估动力学参数，再给本文运动学范围/NE/降阶差异；S10/R3-C2 pp.12–13、17 先承认 PID 已广用且三者能稳定跟踪，再读 tracking 和 transient 差异。
- **Transition**：承认 baseline 不等于接受 reviewer 的总体否定；只有比较维度、测试条件相同时才能走向优劣判断。技术对象、baseline 与其比较谓语保持相邻。
- **Stop**：reviewer 所要求的维度已有对应 evidence/解释即停；无需在每条比较后重做整个领域背景。
- **Boundary**：S09 是 prior-work 概念比较，S10 是实验控制器比较；共同机制仅是“先定位 baseline，再读特定差异”。S10 的完整图表组织仍是 C3，不能由两场景推出固定综合比较结构。

### 2.7 多 concern 分块（B6；taxonomy J）

- **Trigger**：同一 comment 内存在可分别判定完成与否的要求。
- **Entry**：一个 comment 触发不同动作时，作者以不同对象/动作进入相继功能块。S05：typo 改正与 SVD 解释；S10：PID/MBAC tracking、动态参数比较与实验宣告；S14：相关文献与外扰测试。原文不一定显式列出完整 concern inventory。
- **Blocks/transition**：一个 block 报告某项 action、explanation 或 evidence 后，转入另一项实质内容；`Additionally/Moreover` 只是 S05/S10/S14 的表面连接，不能单靠连接词构成新 block。
- **Stop / completeness audit**：原文可在已写出的功能块后结束，并不保证每个 concern 获得充分 evidence。S14 未覆盖量化/延迟/脏微分，S10 的真实实验只被宣布。逐项充分回答属于独立 completeness audit criterion。
- **Variation**：concern 可以合并在同一段（S05），也可成多段（S10）；不必强行编号 1)/2)/3)。

### 2.8 其余单例组织：只供对照

- **Novelty（C2；S09/R3-C1，pp.11–12）**：前作已做什么 → 本文新增范围 → 为什么该范围有意义 → 另两个技术贡献维度 → location。三个维度是此文自身事实，非通用数量；原文长且含过强 claim。
- **完整多控制器/图表比较（C3；S10/R3-C2，pp.12–17）**：rationale → PID/MBAC action → 七关节图与 RMSE → 逐 baseline 读图 → 参数 Table → 综合判断 → location。与 S16 的参数表段重用，不能据重复表述提升证据级。
- **Why this method（C4；S15/R4-C5，p.20）**：既有 adaptive control 的用途 → gradient law 的耦合问题 → 所提 finite-time/leakage 方案 → 概括性优势，直接结束；无图表或 location。最后优势 claim 在本 response 内缺证据。
- **明确参数表（C5；S16/R4-C6，pp.20–21）**：报已比较 → 表中三组数据 → location/摘录 → 总体读表。它与 S10 用同一份表，不能算第二种 table task。

## 3. Block-level semantic state transitions

| 当前状态 → 下一状态 | 下一状态出现的条件与认知任务 | 连续句证据与级别 | 可停止处 |
|---|---|---|---|
| **concern uptake → concrete action/object** | 承接已指明的缺口之后，下一句让 reader 知道作者改了什么或测了什么；否则仍停留在礼貌 | S01 p.3 `We agree...` → tests；S02 p.4 typo → corrected；S05 pp.8–9 typo/statement 双动作。A1 | 动作与核对对象明确，局部问题可进入 location/摘录 |
| **technical fact → condition → derivation → implication** | reviewer 挑战成立性，先限定命题，再展示条件如何作用于式链，最后才推论 | S04 pp.7–8 PE → 窗口 → 权重 → D；仅 C1，不能推广其具体 PE 顺序 | 被挑战性质在同一条件域内已证明；若关键不等号未成立，则不可停在“已证明” |
| **revision action → needed local explanation → revised expression** | 若错处并非纯 typo，动作句后还需说明新定义/关系为何对应问题 | S05 pp.8–9 SVD；S07 pp.9–10 F(t)/极限；B2 | 新表达可核查且原疑问被回答 |
| **purpose/deficit → test operation → setup → evidence locator** | purpose 本身不交代实验；需给扰动/平台/任务/比较条件后，图号才有解释对象 | S01 p.3 噪声强度与公平参数 → Figs.1–6；S13 p.18 Baxter/轨迹 → Figs.14–15；B4 | setup 足够使 Figure 指向具体测试 |
| **locator → observation → comparison/inference** | 图表只是证据地址；下一状态要读出测量值、方向或与 baseline 的关系 | S01 pp.3–4 图 → ±2/4/6 cm 与收敛；S10 pp.13/17 图 → PID/MBAC/FT，表 → 接近真值；S13 pp.18–19 图 → nominal 对照。A5 | 已给可见 observation；若没有比较请求，不必强行比较 |
| **observation → optional claim（独立质量门槛）** | 原文有时在 observation 后继续给结论；是否继续、范围是否由证据支持，不是已验证的 B4 实现 | S01 p.4、S10 p.17、S13 p.19 都有“观察 → 广泛 effectiveness/robustness”跃迁，其强度是 SOURCE DEFECT；A5 只保留 locator→observation，不保留该强 claim | evidence-quality audit 核对 claim 与已测变量、平台、条件；原文并未稳定做到 |
| **baseline value → discriminating difference** | reviewer 要的是差异，先让 baseline 的真实能力成立，再说明同一维度的局限或本文新增 | S09 pp.11–12 [20] 已有动态估计 → 本文范围/模型；S10 pp.12–13/17 PID/MBAC 有稳态 → 暂态差异；B5 | 特定差异和证据已明，停止扩展其他维度 |
| **reported block → another substantive block** | 前一块报告了 action、explanation 或 evidence，下一块带入不同实质内容；连接词不能代替内容 | S05 pp.8–9 `Additionally` 换到 SVD；S10 p.13 `Additionally/Moreover` 换参数/实验；S14 pp.19–20 `Additionally` 换外扰，但未覆盖原三项；B6 | 原文可在部分 block 后结束；遗漏项另作 completeness audit |
| **revision/evidence → manuscript location or excerpt** | location 提供可追溯性，可先于摘录、附在 action 后，也可最终收束 | S03 p.7 location→替换句；S06/S08 pp.9–10 location→公式；S01 p.4、S10 p.17 evidence→location；A6 | reviewer 能找到改动；重复 location 不增加证据 |

这些是**语义状态**，不是“句 1/2/3”的句法配方。`However` 只有在真实的旧法可取处与局限之间才承担转折；`Therefore/This implies` 只有在前面的证据支持相应推论时才有作用。

## 4. Language fingerprint：稳定选择与偶然措辞分离

### 4.1 Semantic subject 与 core verb：谁对哪个动作负责

| 本句语义责任 | 原文常用 subject → core verb | 证据与状态 | 推断边界 |
|---|---|---|---|
| 作者承认 concern、设计或实际开展工作 | `we/the authors → agree, developed, design, conduct, have proof-read, have invited` | S01 p.3、S09 p.11、S11 p.18、S15 p.20；`A3` | `we` 并不限于寒暄；也不要求每句都用 `we`。`“The authors thank...”` 高频只表示礼貌，不是一条内容机制 |
| 稿件中的可定位对象被修改 | `typos/statement/derivation/Figure → have/has been corrected, rewritten, added, modified` | S02 p.4、S03 p.7、S05 pp.8–9、S06 p.9、S12 p.18；`A3` | 主语应是实际改动对象；`corrected and updated`、`modified and updated` 的重复动词不迁移 |
| 数学命题或比较事实被陈述 | `matrix D/PE condition/interval/NE model/parameters → is introduced, satisfies, holds, is based on, converges` | S04 pp.7–8、S09 pp.11–12、S15 p.20；`A3` | 条件应约束该技术对象的 claim；不能凭该句形式推断命题已正确 |
| 测试设置与任务被说明 | `tests/experiments/disturbance/robot/parameters → are conducted, have been performed, is chosen, is commanded, are chosen` | S01 p.3、S13 p.18；`A3` 的语义责任，具体 “robot is commanded” 只见一次 | `we conduct` 和 `tests are conducted` 在 S01 同在；语态/主语不构成硬限制 |
| 证据进入、结果被读出 | `results/disturbances/performance/details → are shown/depicted`；`maximum deviations/estimated parameters/tracking errors → are, are close, are relatively large`；亦用 `we can see` | S01 pp.3–4、S10 pp.13/17、S13 p.18、S16 pp.20–21；`A3/A5` | Figure/Table 多在 `in/from` 后作 locator；不是一律充当语法主语 |

核心动词由**对象的实际状态变化或可观察关系**选出，不由“学术英语动词清单”选出。完成 manuscript 修改通常用完成动作；数学证明用 `hold/derive/imply` 类关系；图表读取用 `show/depict/observe`。这只是本 PDF 的分布，不替任何新稿决定时态或真值。

### 4.2 Information order 与 condition/baseline 的邻接

- **条件贴近 claim（A4）**：S04/R2-C2 p.7 把 `if Rf ... is PE, then D ...` 放在一个技术命题里，随后才证明；S08/R2-C6 p.10 在式链前列 `According to (22)` 与恒等式；S07/R2-C5 pp.9–10 分开说明 nonzero/zero eigenvalue。不是“条件总在句首”，而是 reviewer 能找到该 claim 在何条件下成立。
- **baseline 贴近比较谓语（A4/B5）**：S09/R3-C1 pp.11–12 的 `[20]/Lagrange` 与新方法差异相邻；S10/R3-C2 pp.13/17 的 PID/MBAC 贴近 tracking、transient、RMSE 或参数精度读取。只有 baseline、metric/维度和 observation 对齐后才能形成比较。
- **purpose（若有）→ setup → metric/evidence → observation（B4/A5）**：S01 p.3 的 “To further show...” 后是白噪声通道/强度及图；S13 p.18 直接从 Baxter 实验进入轨迹与估计图。purpose 不承担 setup，图号不承担 observation。是否继续 conclusion 及其证据范围另作 evidence-quality audit。
- **manuscript location（A6）**：既可在修改句后、修订 excerpt 前（S03 p.7、S06 p.9、S13 p.18），也可在读完证据后（S01 p.4、S10 p.17）。原文重复 location 的做法仅是可观察冗余，不是机制。

### 4.3 Terminology behavior 与句子密度

- **术语连续性**：S01 pp.3–4 重复 `end-effector position / disturbances / parameters`；S04 pp.7–8 重复 `PE condition / D / Rf`；S09 pp.11–12 重复 `kinematic parameters / NE model / PE condition`；S10 pp.12–17 重复 PID/MBAC/FT 和 `tracking error`。有跨 scene 证据支持“同一对象继续用同一术语以维持指代”；**没有**证据支持为避免重复而主动换同义词，也不能把原文机械重复或赘句当优点。
- **局部问题短**：S02 p.4、S03 p.7、S11–S12 p.18 为 3–5 个功能句或更短；“完成动作—位置/摘录”后不铺背景。S05–S08 pp.8–10 的自然语言也短，但公式/摘录可很长。S04/S09/S10 pp.7–17 长，是因为 theorem、novelty、多 baseline 需要更多功能块；**不支持统一句长阈值**。
- **单句责任**：S01 p.3 将噪声操作、σ 定义、公平条件、图号分给相邻句；S13 p.18 将平台、轨迹、估计图、观察分句；S04 p.7 条件命题在一句里，随后独立进入证明。可观察的是相邻句接力，不是每句只能有一个判断。S09、S10 中超长复句与语法失误应隔离。

### 4.4 Connectors 只按真实功能解释

| 原文 connector | 实际逻辑工作与出处 | 非规则化边界 |
|---|---|---|
| `As suggested / According to your suggestion` | 把 reviewer 请求接到已完成修改或新增比较；S02 p.4、S03 p.7、S06 p.9、S10 p.13 | 不能替代说明具体对象/动作，也不能假称已完成 |
| `For your convenience` | 引入修订摘录/结果和查找位置；S03 p.7、S06 p.9、S13 p.18 | 只是导航，非内容证据；重复使用可冗长 |
| `However` | 从已有方法作用/共同表现转到限制；S09 p.11、S10 pp.12–13、S15 p.20 | 只有前后事实真有反差才成立 |
| `Additionally / Moreover` | 移到第二个 concern、另一组 evidence 或新贡献；S05 pp.8–9、S10 p.13、S14 pp.19–20 | S14 的转换不解决原三项技术要求，连接词不能修补 coverage gap |
| `On the other hand` | S09 p.11 将 novelty 的第一维换到 NE 计算维度 | 单一 novelty response 的段落标记，`SINGLE INSTANCE`；不能要求所有 response 用它 |
| `Therefore / Thus / This implies` | 承担前文事实/式链到结论的推论；S04 p.8、S09 pp.11–12、S15 p.20 | 论证强度必须由前文支持；原文多处强推论是 `SOURCE DEFECT` |

### 4.5 Figure/Table/result 的可见链

`evidence object → locator → observation → [comparison/inference in some scenes] → [claim in some scenes]`。已验证的 TIE 推进止于 locator→observation；后续 claim 的有无及范围另属 evidence-quality gate。

S01/R1-C2 pp.3–4 用 `disturbances/performance → shown in Fig.1/3/5 与 Fig.2/4/6 → 最大偏差/收敛`；S13/R4-C3 pp.18–19 用 `estimation results → Fig.15 → 与 nominal/dashed line 的接近`；S10/R3-C2 pp.13/17 用 `comparison results → Figs.7–14 → PID/MBAC/FT 读图 → RMSE`，再用 `estimated parameters → Table III → 与真值的总体比较`。S16/R4-C6 pp.20–21 的 Table 链与 S10 复用，不能增加独立 evidence count。

链上的方括号表示**非必需环节**：若 reviewer 只要修 typo，根本没有 Figure/Table；若图只展示某项结果，不必硬加方法优劣。原文可在 observation 后给出较宽 claim；是否应停在 observation、claim 是否充分受证据支持，均由独立质量审查判断。S01 的数字强度读取是 `C6` 单例，不能说所有结果都必须有数字。

## 5. LEVEL A/B/C 候选 evidence table

每行是一条**可审查的候选**。`A/B` 也仅在所列触发和证据范围内可用于下一轮规则验证；此处不宣称已经普遍有效。

| ID / Level | 候选机制（功能关系） | 独立证据、页码与限制 |
|---|---|---|
| **A1 / CORE** | 礼貌承接后尽快进入**可回答的 concern、技术命题或已完成对象/动作**，避免 response 长时间停留在 meta 感谢 | S01/R1-C2 p.3；S03/R2-C1 p.7；S04/R2-C2 p.7；S11/R4-C2a p.18；进入点各异，不规定第二句固定写法 |
| **A2 / CORE** | **问题越局部，response 通常越短；独立技术/证据任务越多，往往出现更多功能块与更长篇幅**。原文停止点不保证充分覆盖 | S02/R1-C3 p.4 与 S12/R4-C2b p.18 对比 S04/R2-C2 pp.7–8、S09/R3-C1 pp.11–12、S10/R3-C2 pp.12–17；停止充分性另作 audit |
| **A3 / CORE** | 语义责任选择主语和动作：作者行为用 we/authors，稿件修改用具体对象，技术关系用技术对象，证据定位/读取用结果对象 | S01 p.3–4、S03 p.7、S04 pp.7–8、S09 pp.11–12、S13 pp.18–19；允许同 scene 交替主语 |
| **A4 / CORE** | **条件或 baseline 与受其约束的 claim/比较维度相邻**，然后再解释或证明 | S04/R2-C2 p.7、S07/R2-C5 pp.9–10、S09/R3-C1 pp.11–12、S10/R3-C2 pp.13/17；不规定条件必须句首 |
| **A5 / CORE** | 有图表时从 **evidence locator 进入具体 observation**；只有请求或证据需要才继续 comparison/conclusion | S01/R1-C2 pp.3–4、S10/R3-C2 pp.13/17、S13/R4-C3 pp.18–19；S16 共用表仅为旁证；强结论隔离 |
| **A6 / CORE** | **稿件位置或修订摘录提供可追溯性**，可置于动作后、摘录前或结果后；它服务于核查，不决定整条 response 的尾句 | S03/R2-C1 p.7、S06/R2-C4 p.9、S08/R2-C6 p.10、S01/R1-C2 p.4、S10/R3-C2 p.17 |
| **B1 / SCENARIO** | 局部明确错误：**对象 → 完成修正 → 必要的替换内容/位置 → 停止** | S02/R1-C3 p.4、S03/R2-C1 p.7、S11/R4-C2a p.18、S12/R4-C2b p.18；仅限局部纠正 |
| **B2 / SCENARIO** | 局部 equation/definition：**改动对象 → 最小技术关系 → 新式/摘录 → 停止** | S05/R2-C3 pp.8–9、S07/R2-C5 pp.9–10；具体 SVD 与极限各是单例 |
| **B3 / SCENARIO** | 缺推导：**引用已有关系/前提 → 展开中间式 → 指认使用的事实/符号** | S06/R2-C4 p.9、S08/R2-C6 p.10；公式长度随缺口变化 |
| **B4 / SCENARIO** | 新增测试：**action → concrete setup → evidence locator → observation**；其后有无 conclusion、claim 范围是否恰当，另作 evidence-quality gate | S01/R1-C2 pp.3–4、S13/R4-C3 pp.18–19；二者较宽的 robustness claim 是 SOURCE DEFECT；S14 不算独立实验 |
| **B5 / SCENARIO** | 比较：**baseline 已有作用/表现 → 明确本文不同维度 → 同维度差异及其证据** | S09/R3-C1 pp.11–12 与 S10/R3-C2 pp.12–13/17；概念比较与实验比较只共享这一子机制 |
| **B6 / SCENARIO** | 多 concern：**不同 concern → 不同 action/explanation/evidence 功能块**；块间转换须带来新实质内容。逐项充分覆盖另作 completeness audit | S05/R2-C3 pp.8–9；S10/R3-C2 pp.12–17；S14/R4-C4 pp.19–20 显示原文可遗漏子问；不强制编号 |
| **C1 / REFERENCE** | 核心证明争议：**技术条件 → 窗口/权重推导 → bounded implication → 修订位置** | S04/R2-C2 pp.7–8 唯一完整例，原文严格式和矩阵/标量写法待核；不得直接生成 |
| **C2 / REFERENCE** | novelty：**承认前作 → 本文多个真实技术差异维度 → 贡献归位** | S09/R3-C1 pp.11–12 唯一完整例；“三个维度/三段长度”均不可泛化 |
| **C3 / REFERENCE** | 综合控制器比较：**rationale → PID/MBAC action → tracking 图 → RMSE → 参数表 → location** | S10/R3-C2 pp.12–17 唯一完整例；S16 复用参数表，不提供第二独立支撑 |
| **C4 / REFERENCE** | method motivation：**已有方法功能 → 限制机制 → 本文方案 → 优势主张** | S15/R4-C5 p.20 唯一完整 scene；最后优势在此 response 中缺直接 evidence |
| **C5 / REFERENCE** | 明确 Table 请求：**比较已做 → 表列说明 → 表后总体 observation** | S16/R4-C6 pp.20–21 唯一独立 table task；S10 p.17 同表同文，不升级 |
| **C6 / REFERENCE** | 噪声强度图：**三个 σ → 三个图 → 三个最大偏差数字 → 对应估计图** | S01/R1-C2 pp.3–6 单例；其 `Figs.2-5` 总述编号错误已隔离 |

## 6. Anti-overgeneralization：看似规律、不能升级的判断

| 容易误升级的说法 | PDF/scene 反证或证据边界 | 本轮判定 |
|---|---|---|
| “实验必须以 `To further...` 开始” | S01/R1-C2 p.3 有 `To further show...`；S13/R4-C3 p.18 的真实实验摘录从 `In addition, experiments...` 开始；S10/R3-C2 p.13 也先从 `According to your suggestion` 报行动 | **不成立**。可保留 B4 的 action/setup/evidence 顺序，不固定入口词 |
| “manuscript location 一定是最后一行” | S03/R2-C1 p.7 先 location 后替换句；S06/R2-C4 p.9、S08/R2-C6 p.10 先 location 后公式；S01/R1-C2 p.4 和 S10/R3-C2 p.17 才在末尾给 location | **不成立**。A6 是可追溯性机制，非尾句位置规则 |
| “reviewer 前提错误时必须先写 negative claim，指出其误解” | S04/R2-C2 p.7 直接界定 PE→D 的条件命题再证明；S09/R3-C1 p.11 先承认 [20] 已做的工作再列真实差异，均未以 `reviewer misunderstood` 进入 | **无证据**。若需澄清，核心是正面的技术对象/条件/比较；负句可否使用本 PDF 不建立禁令 |
| “Figure/Table 必须作 grammatical subject” | S01/R1-C2 pp.3–4 是 `disturbances/performance are shown in Fig...`；S10/R3-C2 p.13 是 `comparison results are depicted in Figs...`；S16/R4-C6 p.20 是 `details ... are shown in Table...`；S10 p.17 有 `Fig.14 show` 但非唯一模式 | **不成立**。Figure/Table 常是 locator，subject 依语义责任选 |
| “所有结果必须给数字” | S01/R1-C2 p.3 读 ±2/4/6 cm；S13/R4-C3 p.18–19 读 “most ... close to nominal values”；S10/R3-C2 p.17 主要定性读 tracking 与表的 closeness | **不成立**。直接数字读取是 C6 单例；也不能以此许可空泛结果 |
| “novelty response 应照 R3-C1 写三大段” | S09/R3-C1 pp.11–12 只有一条完整 novelty scene，且段内反复铺陈、强 claim 与语法问题；S15 p.20 的动机答复更短且另有目标 | **不成立**。C2 只说明该文真实差异维度，不提供长度或贡献数量规则 |
| “实验结果都可写 `robustness/effectiveness verified`” | S01/R1-C2 p.4 只测试特定白噪声；S13/R4-C3 p.19 只展示 nominal convergence；S14/R4-C4 pp.19–20 未测所问的量化/延迟/脏微分 | **SOURCE DEFECT**。结论不能超出所示条件；A5 的推论环节可在 observation 后停止 |
| “`we` 应限制为感谢或完全避免” | S01/R1-C2 p.3 有 `we agree`、`we conduct`；S09/R3-C1 p.11 有 `we developed`；S15/R4-C5 p.20 有 `we design`；同时也有对象主语 | **不成立**。A3 按行为责任选择，不按禁词选择 |
| “每条 response 都拆成编号 1)/2)/3)” | S05/R2-C3 pp.8–9 一条含 typo 与定义但按连续段展开；S10/R3-C2 pp.12–17 多 concern 用段落、图、表；S14/R4-C4 pp.19–20 两块靠 `Additionally` 转换 | **无证据**。B6 只描述不同功能块，不要求版式编号或保证逐项覆盖 |
| “同一表格在两个 comment 中出现就证明 Table 组织稳定” | S10/R3-C2 p.17 与 S16/R4-C6 pp.20–21 近乎同文、同一 43 行参数表，且表号互不一致 | **不成立**。一份独立表材料，C5 保持单例 |
| “reviewer 要量化、延迟或 dirty derivative，可用一般外扰测试替代” | S14/R4-C4 pp.19–20 原请求列三类具体非理想因素；作者只讨论文献并引用 S01 外扰测试 | **不成立**。这是未覆盖 concern 的 source defect，而非 B4 的变体成功例 |
| “出现 `This implies/Therefore` 就已完成证明” | S04/R2-C2 p.8 的严格 `>` 与矩阵-标量结论仍有核验问题；S09/R3-C1 p.12 的 PE/降阶推论过强；S15/R4-C5 p.20 的 advantage claim 缺证据 | **不成立**。推论依赖前提与数据，不依赖连接词 |

## 7. SOURCE DEFECT 隔离清单

这里记录应从候选机制中剥离的部分；保留 scene 与页码，使后续规则验证能回查。**缺陷出现多次也不得进入可生成机制。**

| 缺陷类型 | 原文位置及问题 | 隔离边界 |
|---|---|---|
| 过强实验结论 | S01/R1-C2 p.4 从三种加噪仿真说 “verified robustness”；S13/R4-C3 p.19 从 nominal convergence 说 robustness verified；S10/R3-C2 p.17 从图/表推出总体 effectiveness/accuracy | 只保留 locator→observation 的推进；结论应受实际 tested condition 约束，不能复制 `verified` 的范围 |
| concern 未覆盖 | S14/R4-C4 pp.19–20 未逐项回应 quantization、delay、dirty derivative；S10/R3-C2 p.13 宣布真实实验但本 scene 中未展开 setup/数据 | 不能把“额外相关测试”或“已做”当作完成全部子问；逐项覆盖属于独立 completeness audit |
| 数学条件或推导跳跃 | S04/R2-C2 pp.7–8 的严格 `>`、`D(t)>σ` 维度写法；S09/R3-C1 p.12 把 SVD 降阶直接连到 PE 可保证；S05/R2-C3 pp.8–9 的 SVD 维数/正交条件及符号变化 | A4/B2/B3/C1 只能转移“先展示条件与步骤”的组织，不能转移这些具体命题的真值 |
| Figure/Table/location/引用编号错配 | S01/R1-C2 p.3 “Figs.2-5” 对后续 Figs.1–6；S10/R3-C2 pp.13–17 `Table III` 对 PDF `Table 1`、Fig.14 图例 `MARC` 对正文 `MBAC`、[20] 对 [27]；S13/R4-C3 pp.18–19 轨迹/估计图号不一致；S16/R4-C6 pp.20–21 `Table II/III/Table 2` 与 Section V/IV 不一 | A6 是核查位置，不许可复制编号；具体编号须逐一对 PDF/稿件证实 |
| 表内反例与总体精度 claim | S10/R3-C2 p.17、S16/R4-C6 pp.20–21 共用的 43 行表中第 1、10、14、21 等行所提估计未必更接近真值，却说总体更准确 | 只能描述有证据支持的比较范围；不能从“作者说更好”建立比较规则 |
| 语法、搭配和冗余 | S01 p.3 `sensors data may subject to`、`depicted as shown`；S05 pp.8–9 定义段冗长；S06 p.9 `detailed formulated`；S09 pp.11–12 `fast and accurate convenience`、过长段；S10 p.13 `gradient decent`、`verity`、`conducted and performed`；S11 p.18 `help us polishing`；S15 p.20 `exiting reference/effected`；S16 p.20 `The detailed of...` | 只记录其语义功能和出现位置；错误句法不因来源为 TIE 而变成可模仿 fingerprint |
| 重复动作或整段复贴 | S01/R1-C2 p.3 先后两次报 robustness tests、两次位置；S04/R2-C2 pp.7–8 先证明后复贴几乎同文 Remark；S10/R3-C2 p.13 比较 action 重复；S10/S16 同表段复用 | A2 只描述任务复杂度与功能块/篇幅的关系；不能把重复当完整组织所必需 |

## 8. 目前 TIE_2621 尚不能建立的规则区域

1. **核心理论反驳的可复用形式**：只有 S04/R2-C2（pp.7–8），且本身存在严格式/记号边界；不能推到所有证明争议、所有 theorem rebuttal。
2. **novelty response 的稳定维度、长度与文献比较标准**：仅 S09/R3-C1（pp.11–12）完整对应 originality；S15 是 method motivation 而非第二个 novelty 复例。
3. **独立的完整多控制器 comparison + experiment 机制**：只有 S10/R3-C2（pp.12–17）展示 PID/MBAC/FT 图和参数表；S16 复用表，S13 是另一项真实实验，不构成第二套综合比较。
4. **不同类型 robustness 条件的分别回应**：白噪声 S01 有详细 setup；S14 提到量化、延迟、脏微分但未测试。不能建立这些因素的组织或结果读取规则。
5. **参数表的独立重复证据**：S10 与 S16 同一材料。无法据此确定表格应有几列、是否必须列真值、怎样逐行解读或该怎样做整体统计比较。
6. **不利、混合或失败结果如何诚实呈现**：本 PDF 的结果多做有利概括，且表中反例没有被正文认真分析；无法建立处理不利结果的 scene mechanism。
7. **数值证据的普遍密度**：S01 有三个偏差数字；多数图表段为定性读取。不能定“每图必须有数值”或“定性足够”的规则。
8. **`we` 与对象主语的硬比例、固定时态或连接词频率**：只能观察语义责任及局部用法，不能推生成配额。
9. **reviewer 明确不接受作者解释时的后续轮次/升级回复**：本 PDF 是一轮逐点 response，没有反复交涉或决定函二次修回的独立场景。
10. **编号子项、统一句长、统一收尾位置**：原文没有支持这些版式硬约束；不能在下一轮把它们补成所谓 TIE fingerprint。

**候选模型使用边界**：面对新 comment，可先按 §1 判断真实 situation 与子问，再用 §2/§3 找可用的 A/B 状态推进；若只落到 C，返回原 scene 作为参考并保持证据不足的标记。任何进入结论的内容必须重新核对新稿自己的事实与数据。本文件未据其他稿件需求倒推，也未更新既有基准或最终知识库。

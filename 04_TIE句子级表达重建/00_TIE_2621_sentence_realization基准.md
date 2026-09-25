# 江 TIE_2621 response realization 基准：scene → block → 连续句 → 单句

## 0. 使用边界、证据等级与读取顺序

- 唯一语料：`Response_TIE_江_No.17-TIE-2621.pdf`，共 21 个 PDF 页面；完整覆盖 Associate Editor 1 条、Referee 1 3 条、Referee 2 6 条、Referee 3 2 条、Referee 4 7 条 response。Referee 4 原文把语法问题和 Figure 1 问题都编号为 Comment 2，本文分别记为 `R4-C2a`、`R4-C2b`。
- 引文均来自作者 response 或其中粘贴的 revised text。只合并 PDF 换行造成的断词；原有用词、时态、单复数和标点问题不代为修正。
- `REPEATED/STABLE` 只表示该实现机制在 **2621 这一封 response 内跨多个 comment 重复**，不等于 IEEE TIE 的普遍规范。
- `SINGLE-INSTANCE` 表示只有一个可核对实例，不能上升为稳定规律。
- `SOURCE DEFECT / DO NOT TRANSFER` 表示原句可用于观察信息组织，但其语法、搭配、claim 强度或冗余不可迁移。

旧表中的 `REPEATED/STABLE`、`SINGLE-INSTANCE` 仅记录原始出现范围；**正式可用级别以本页经验证的 A/B/C 为准**，不得把同表复贴或同实验复述算独立复例。

本基准以 **PDF 原文 → `02_TIE_2621_scene_response_corpus.md` → 定点修订的 `03_TIE_2621_response_mechanism_candidates.md` → `04_TIE_2621_mechanism_validation.md`** 为证据链；旧版 00 的正确句子证据保留在附录。页码均为 PDF 阅读器显示的物理页，不是各 referee 章节自行重起的页码。16 个有实质内容的 reviewer-response scenes 构成分析集；R1-C1、R4-C1 仅致谢认可，AE-C1 是编辑层总答复，见 02 的完整清点。S10/R3-C2 与 S16/R4-C6 复用同一参数表，S14/R4-C4 复用 S01/R1-C2 的外扰测试；**重复文字不等于独立证据**。

| 等级 | 可用方式 | 不能做什么 |
|---|---|---|
| **VALIDATED CORE / A1–A6** | 跨独立 scene 的语义责任、信息邻接、证据读取和可追溯性。A2 只描述任务复杂度与功能块/篇幅的关系 | 不能据此设固定句数、统一结束位置或“作者总会充分答完”的行为 |
| **VALIDATED SCENARIO-SPECIFIC / B1–B6** | reviewer situation 符合触发条件时，选择对应功能块。B4 止于 action→setup→locator→observation；B6 止于多 concern 引出不同实质块 | 不能把 bounded conclusion 或逐项完整覆盖伪称为 TIE 原文稳定做到的事 |
| **REFERENCE ONLY / C1–C6** | 回看唯一 scene 的真实组织、条件和局限，辅助判断未知情形 | 不能生成固定 proof、novelty、PID 比较、method motivation、Table 或数字测试路径 |
| **SOURCE DEFECT / DO NOT TRANSFER** | 标出原句有用的信息位置，同时隔离其缺陷 | 不能复制过强结论、未答子问、数学/编号/语法错误、冗余 |

**使用次序**：读 reviewer 原 comment → 判断 situation 与各独立 concern → 选可用 A/B；遇 C 只查看参考 scene → 决定 response blocks → 再做连续句的主语、动词、条件、baseline、图表与 location 实现 → 最后用 §7 的独立质量门槛核查。这是江 TIE_2621 一封 response 的实证基准，**不是 IEEE TIE 通行规范，也不是万能模板**。

## 1. Reviewer situation → mechanism routing

| 从 reviewer comment 识别的 situation | 可调用机制 | 实际来源与边界 |
|---|---|---|
| 可定位的 typo、措辞、Figure clarification | A1–A3、A6 + **B1** | S02/R1-C3 p.4、S03/R2-C1 p.7、S11/R4-C2a p.18、S12/R4-C2b p.18。Figure 具体怎样变清楚只有 S12 一例，短答不等于充分答复 |
| 局部 equation、definition 或极限表达不清 | A1、A3、A4、A6 + **B2** | S05/R2-C3 pp.8–9、S07/R2-C5 pp.9–10；只支持局部动作→关系→修订式，不验证 SVD/极限公式的数学正确性 |
| 某等号或不等式缺中间推导 | A1、A3、A4、A6 + **B3** | S06/R2-C4 p.9、S08/R2-C6 p.10；实际缺哪一步决定公式长度 |
| theorem 所赖条件/证明遭核心质疑 | A1、A3、A4；**C1 仅参考** | S04/R2-C2 pp.7–8 唯一完整 scene；其 PE→D 窗口证明不可成为通用路径，严格不等号还需独立数学核对 |
| 要新增 noise/robustness test 或真实 experiment | A1–A3、A5、A6 + **B4** | S01/R1-C2 pp.3–6、S13/R4-C3 pp.18–19 是独立测试；S14/R4-C4 pp.19–20 复用 S01，不算第三套实验 |
| 需要 prior-work / controller comparison | A1、A3–A5 + **B5** | S09/R3-C1 pp.11–12 的技术范围比较与 S10/R3-C2 pp.12–17 的控制器比较，仅共享 baseline capability→discriminating difference；完整多图/表路径仍为 C3 |
| novelty/originality 被否定 | B5 可用于具体差异；**C2 仅参考** | S09/R3-C1 pp.11–12；三贡献维度、长篇幅及强 claim 不作规则 |
| 问“why this method” | A1、A3、A4，必要时 B5；**C4 仅参考** | S15/R4-C5 p.20 唯一完整动机场景；不要求图表或固定 location |
| 明确要求参数 Table / data presentation | A3、A5、A6；**C5 仅参考** | S16/R4-C6 pp.20–21；S10 p.17 是同表同文，不是独立验证 |
| 一个 comment 有多个可分别回答的 concern | 相应类型并行识别 + **B6** | S05/R2-C3 pp.8–9、S10/R3-C2 pp.12–17、S14/R4-C4 pp.19–20；可见不同功能块，**不保证**每项都已充分覆盖 |

先按 reviewer 所问分类，不能按作者后来选择做的实验倒改类型。S14 所问的 quantization、delay、dirty derivative 仍是三个具体非理想因素，即使作者只给一般外扰测试。一个 comment 可同时属于“局部公式”与“多 concern”，路由不要求互斥。

## 2. Response-level organization：触发、块序与实际停止

**跨 scene 核心（A1–A6）**：礼貌句之后尽快出现可回答的 concern、技术命题或已完成动作（A1）；局部问题通常短，独立技术/证据任务越多，往往有更多功能块和更长篇幅（**修订后 A2**）；一个 block 内按语义责任选主语/动词（A3），让条件或 baseline 靠近受约束的 claim/比较维度（A4）；有图表时 locator 后读出 observation（A5）；用 Section/Page 或摘录提供可追溯性，位置可以在结果前或后（A6）。这些只是可预测的关系，不能推出统一的完整 response 形状。

| 条件触发 | 真实 response 的必要功能块及为何按此顺序 | 可能增加的块与作者实际结束点 | 证据等级 |
|---|---|---|---|
| **B1 局部 correction**：错误对象明确 | 被指出对象/已改动作 → 可核对的替换句或位置；先指出改了什么，位置才有指向 | S02 p.4 多一次全稿校对；S03 p.7 先给 location 再贴新句/公式；S12 p.18 在 Figure 改动+位置后结束，却未具体解释输入输出，属 coverage gap | B1：S02/S03/S11/S12；只对局部问题复用 |
| **B2 local equation/definition**：符号关系或极限局部不明 | 修订对象 → 使新式成立的局部事实/定义 → 修订式或摘录；解释从改动本身的技术缺口生出 | S05 pp.8–9 先改 typo/statement，再解释 SVD；S07 pp.9–10 给 F(t) 与零/非零极限；location 可先于摘录；数学正确性另审 | B2：S05/S07 |
| **B3 missing derivation**：具体等号/不等式跳步 | 已补推导及式号对应 → 使用的前提/恒等式 → 连续中间式 → 末步所用事实/新符号；没有前提就无法读后面的式链 | S06 p.9 以 Ac 对角性结束；S08 p.10 还定义 μd、ρd 并延至紧集/负导数。说明句短，公式可长 | B3：S06/S08 |
| **B4 added experiment**：需要实际新增测试 | action → concrete setup（通道/强度/公平参数或平台/任务）→ evidence locator → observation；setup 让图号有实验含义，图之后必须读出可见结果 | S01 pp.3–4 先同意 concern，位置一度早报，随后噪声设置与配对图；S13 pp.18–19 先报 Baxter 实验/位置，再进平台、轨迹、估计图。两者随后都给较宽 robustness claim，属于源缺陷；**bounded conclusion 不是 B4** | B4：S01/S13，修订后验证；S14 不算独立实验 |
| **B5 comparison**：需要明确与旧法的差异 | baseline 已有功能/可取处 → 同一比较维度上的本文差异 → 必要的图/表或技术解释；先定位 baseline，差异才不是空称 | S09 pp.11–12 属前作/技术范围，S10 pp.12–13/17 属 PID/MBAC tracking；第二个维度可以先写本文 NE 再回到 Lagrange，不固定逐句顺序；多图多表全链仍是 C3 | B5：S09/S10 的共同子机制 |
| **B6 multi-concern**：一条 comment 触发多个动作 | 一个 action/explanation/evidence block → 另一个有新实质内容的 block；块间转换由新对象或新证据承担，不由 `Additionally` 本身承担 | S05 pp.8–9 的 typo+SVD，S10 pp.12–17 的控制器/参数/实验宣告，S14 pp.19–20 的文献+一般外扰；作者可能在部分子问未获证据时结束，**逐项完整覆盖不是 B6** | B6：S05/S10/S14，修订后验证 |

**停止点的描述边界**：B1/B2 的局部 response 常在动作、摘录或位置后结束；长技术答复可重复 rationale、动作或整段摘录。A2 只预测局部性与块数/篇幅的关系，**不预测“充分答完才停”**。B4 可预测到 observation，后续 claim 是否出现由原场景而变；B6 可预测到不同实质块，不预测所有子问都已回答。充分性与结论范围统一由 §7 的独立审计判断。

## 3. Block-level semantic transitions：连续句的认知需求

| 前一状态留下的问题 → 下一状态 | 为什么下一步自然出现 | 代表证据与语义责任 | 等级/停止边界 |
|---|---|---|---|
| concern uptake → **concrete action/object** | 接受 concern 本身不说明作者做了什么 | S01/R1-C2 p.3 `We agree...` 后由 `tests` 承担 conducted；S03/R2-C1 p.7 由 `statement` 承担 corrected | A1；进入可核查动作，不规定感谢后的第几句 |
| revision action → **needed local explanation → revised expression** | 改公式/定义的动作仍留“为什么这样写” | S05/R2-C3 pp.8–9 从 `typos/statement` 转 `formula/Vc/Yc/Ac`；S07/R2-C5 pp.9–10 从新 F(t) 转零/非零极限 | B2；解释只延至所问局部关系 |
| known relation/condition → **intermediate derivation → used fact/new symbol** | reviewer 无法从原式跳到目标等号/不等式 | S06/R2-C4 p.9 以 `VcᵀVc=I` 起步，后用 Ac 对角性；S08/R2-C6 p.10 先列 `(22), FΦr=..., Bc=...` | B3；式链连通才有该块的内容终点；数学真值另审 |
| technical object → **condition → derivation → implication** | 关键性质要先限定何时成立，再给支撑 | S04/R2-C2 pp.7–8 的 PE→D 仅 **C1 单例**；A4 支持“条件贴 claim”，不支持整套 PE 窗口证明变成规则 | C1 仅参考，推导有效性由 §7 核查 |
| purpose/deficit（若写）→ **test action → setup → locator** | 目的不是实验操作，图号也不能替代测量条件 | S01/R1-C2 p.3 噪声通道、σ、公平条件后进入图；S13/R4-C3 p.18 直接由 Baxter 平台与任务进入图，无 purpose-fronting | B4；purpose 可无，setup 依场景变化 |
| evidence object → **Figure/Table locator → observation** | `shown in Fig./Table` 只告诉读者看哪里，下一句必须读出结果 | S01 p.3–4 奇数图扰动、偶数图估计；S10/R3-C2 pp.13/17 tracking/RMSE/参数表；S13 p.18–19 nominal 对照 | A5；comparison/claim 只有确有需要与支持才另进入 |
| baseline capability → **discriminating difference** | 先承认对照方法实际能做什么，差异才有具体维度 | S09/R3-C1 p.11 [20] 的动态估计→本文还含运动学；S10/R3-C2 pp.12–13/17 PID/MBAC 的作用→tracking/暂态差异 | B5；不是必须写 `However` 或固定两句 |
| reported block → **another substantive block** | 一个 comment 内有另一独立动作/证据 | S05 p.8 typo→SVD；S10 p.13 tracking→参数表/实验宣告；S14 p.19–20 文献→外扰（后者没有覆盖原三项） | B6；换 connector 本身不算新块，遗漏另审 |
| revision/evidence → **manuscript location or excerpt** | 具体 Section/Page 或修订摘录使动作可查 | S03 p.7 先 location 后新句；S06/S08 pp.9–10 位置后给式；S01 p.4/S10 p.17 结果后报位置 | A6；location 不是固定尾句 |

这里的箭头是 **semantic state transition**，不是“一句必须用哪个连接词”的模板，也不隐含固定句数。`observation → conclusion` 在原文确有出现，但 S01、S13 的广义 robustness 结论是 SOURCE DEFECT；因此本基准的 B4 稳定链止于 observation，结论的有无与范围进入 §7 的 evidence→claim gate。

## 4. Continuous realization anchors：保留连续上下文

以下保留 PDF 原文的连续英文句群，只合并排版断词；方括号 `[1]` 等是本基准的句序索引，`[equation follows]` 和式中的 `…` 明示省略的展示公式，完整数学式须回 PDF 所指页核对。错词、过强结论与编号问题保留为 **SOURCE DEFECT**，不作为推荐措辞。完整 comment、跨页图/表和逐句分析见 02 的对应 S 卡。

### 4.1 小范围修订：对象先承担动作（B1；S03/R2-C1，PDF p.7）

> [1] Thanks for your constructive comments to improve our paper. [2] As suggested by the reviewer, the statement of robot Jacobian matrix has been corrected and updated in the revised manuscript. [3] For your convenience, the revised text is listed as below. [4] Please see Section II, Page 2 of the revised manuscript for details. [5] Then, the relationship between the joint velocity q̇ and end-effector velocity ẋ can be obtained by taking the partial differentiation of f_kine(q) as [equation follows].

[1] 只承接。[2] 把 reviewer 的措辞问题变成 `statement → has been corrected` 的 manuscript 动作；读者随后需要看改成什么。[3] `revised text` 引摘录，[4] location 先于摘录而非收尾。[5] 主语转为 `relationship`，动词 `can be obtained`，以修订句/公式回答原措辞错误。局部问题只需这些块；`corrected and updated` 为重复搭配缺陷。

### 4.2 局部定义兼多 concern：从改字到关系（B2+B6；S05/R2-C3，PDF pp.8–9）

> [1] According to your suggestions, the typos in equation (18) have been corrected. [2] Additionally, the statement above (18) has been carefully rewritten and the presentation has been improved. [3] Generally, the formula Uc = Vc Ac YcT can be obtained by using the singular-value-decomposition (SVD) method, which is widely employed in matrix operations. [4] The Vc is an orthogonal matrix whose columns are eigenvectors of Uc UcT, Yc is an orthogonal matrix whose columns are eigenvectors of UcT Uc, and Ac is a diagonal matrix of the form Ac = diag{σ1, · · ·, σr}, with r = rank(Uc). [5] Note that the matrix Vc and Yc are unitary matrices such that the relationships Vc VcT = I and Yc YcT = I hold.

[1] 的 `typos → corrected` 只完成表面错误；[2] 的 `statement → rewritten` 切到独立解释任务，`Additionally` 不是转换本身。[3] 的 `formula → can be obtained` 正式进入技术理由；[4]、[5] 用 Vc/Yc/Ac 作为连续主语而不换同义词，补关系后才能贴修订文本。SVD 维数、`σ1...σr` 与摘录的 `a1...an` 不一致，属数学/版本源缺陷；此段仅证明“动作→局部关系→表达”的句间组织。

### 4.3 补推导：位置后把解释交给连续式链（B3；S06/R2-C4，PDF p.9）

> [1] According to your suggestion, the derivation of equation (19) ((20) in the revised version) has been detailed formulated in the revised manuscript. [2] For your convenience, the added text is listed as below, please refer to Section III, Page 5 for more details. [3] Since Vc satisfies that VcT Vc = I, multiplying VcT on both sides of Uc = Vc Ac YcT, we can obtain that VcT Uc = Ac YcT. [4] Then, multiplying Uc on both side of (19), we have [QUc = Yc(Ac+e^(−δt)ηI)^(−1)VcᵀUc = Yc(Ac+e^(−δt)ηI)^(−1)AcYcᵀ = …]. [5] Note that in above derivations, the fact Ac is a diagonal matrix is used.

[1] `derivation → has been ... formulated` 对应旧/新式号，[2] 先给可查位置。[3] `Since` 中的已知正交关系为 [4] 代入式链提供前提；[4] 的 `we have` 把前句产物继续用于 `QUc`；[5] 回指最后一步的 Ac 对角性。省略号只节省本基准的公式排版，完整等式在 PDF p.9；`detailed formulated/on both side` 为原文语法缺陷。S08/R2-C6 p.10 以已知关系→不等式链→新符号作独立同类支持。

### 4.4 新增噪声测试：setup 的句间接力（B4；S01/R1-C2，PDF p.3）

> [1] In some practical applications, uncertainties may inevitably exist in the measurement of end-effector position, e.g., the visual tracking system may be effected by environmental noises. [2] Without loss of generality, in the comparative studies, we conduct the tests by adding white noises with different intensity to the measured end-effector position. [3] The external disturbance is chosen to be d(t) = σw(t), where σ is the degree of intensity, and w(t) is the white Gaussian noise with the power of 1 dBW. [4] For fair comparisons, the parameters in the adaptive estimation are chosen to be the same. [5] The simulation results are depicted as shown in Figs. 2-5.

[1] 把“噪声是否考虑”落到末端位置测量。[2] `we → conduct` 承担加噪操作，测量通道在句尾；[3] `disturbance → is chosen` 接着定义 σ 和 w(t)，[4] `parameters → are chosen` 单独承担公平设置。[5] `results → are depicted` 才从 setup 进入 locator；随后 PDF p.3–4 又按奇数图扰动→偏差数值、偶数图估计→收敛读取。`effected`、`Without loss of generality` 用于经验设置、`depicted as shown` 和 Figs.2–5 对实际 Figs.1–6 的错配均不迁移。

### 4.5 真实机器人：platform → task → Figure → observation（B4；S13/R4-C3，PDF pp.18–19）

> [1] In addition, experiments have been further performed based on the left robotic arm of a real Baxter robot, as shown in Fig.3. [2] In the experiment, the robot is commanded to track a set of sinusoidal and cosine trajectories depicted in Fig.14. [3] The estimation results are shown in Fig.15. [4] We can see from the figure that, most of the estimated parameters are close to the nominal values (dashed line) with satisfactory convergence performance. [5] In terms of the above test results, the robustness of the proposed estimation algorithm can be verified.

[1] `experiments → have been performed` 报平台，[2] 换 `robot → is commanded to track` 承担任务；[3] `results → are shown` 引入图；[4] `we → can see` 读 nominal baseline 与“most parameters”这一有限观察。**B4 的可验证链到 [4] 为止**。[5] 是真实的原文末句，却从 nominal convergence 跳到一般 robustness，属 SOURCE DEFECT；摘录的 Fig.14/15 与随附图编号亦需核对。这一独立 scene 同时反证“实验必须以 `To further...` 开始”。

### 4.6 比较：先定位 baseline 的作用，再读差异（B5；S10/R3-C2，PDF pp.12–13）

> [1] In this paper, we proposed a finite time parameters estimation scheme to identify the kinematic and dynamic parameters of the robots with enhanced convergence rate and accuracy. [2] The conventional PID control methods have achieved great success in robot manipulators control. [3] However, satisfactory control performance may not be obtained using the PID control because the unknown robot dynamics act as a prominent external disturbance and may lead to degradation of the control performance or even incur instability. [4] Model based adaptive control (MBAC) has been thus introduced to handle the effect of the uncertain robot dynamics. [5] For most of MBAC based robot systems, however, gradient decent based adaptive laws were designed to minimize the tracking errors and parameters prediction errors.

[1] `we → proposed` 界定本方法目标；[2] `PID methods → have achieved` 承认 baseline 的已有作用；[3] `performance → may not be obtained` 把真正差异收紧到未知动力学下的控制表现；[4] 因这个限制引入 MBAC，故 [5] 自然再谈 MBAC 的 adaptive law。`However` 仅标事实上的转折，不是必用词。后面的 Figs.7–14 和 Table（PDF pp.13–17）再给 evidence locator/reading；原文中的 `gradient decent`、过强性能 claim 不作为同作者写法。

### 4.7 多 concern 的失败边界：有新块，不等于逐项答完（B6；S14/R4-C4，PDF pp.19–20）

> [1] According to your suggestion, the above mentioned state-of-the-art studies of robot identifications have been discussed and cited in the introduction part of the revised manuscript. [2] Please refer to Section I, Page 1 for more details. [3] Additionally, to further show the effectiveness of our proposed estimation algorithm, robustness tests are conducted by adding unknown external disturbances to the robot system model. [4] The test results show that the estimated parameters are observed with satisfactory convergence rate and accuracy, even in the presence of external disturbances. [5] The details about robustness tests could be found in Section IV, Page 7 in the revised manuscript.

[1] `studies → have been discussed and cited` 与 [2] 的位置构成文献块；[3] `tests → are conducted` 才进入第二块，[4] `results → show` 给一般外扰下观察，[5] 给第二处位置。第二块确有新动作，但原 comment 指定的 quantization、delay、dirty derivative 均未逐项测试。**B6 只能预测分块；完整覆盖是 §7 的独立门槛。**

### 4.8 核心证明仅作参考（C1；S04/R2-C2，PDF p.7）

> [1] In the adaptive parameter estimation, the verification of persistence excitation (PE) condition is important, since the PE condition needs to be fulfilled to guarantee the error convergence. [2] However, the online verification of PE condition is a non-trivial issue, especially for the nonlinear robot system. [3] In this paper, the matrix D is introduced for the verification of PE condition, i.e., if the regressor vector Rf in equation (11) is PE, then the matrix D is positive definite, with λmin(D) > σ > 0. [4] The proof is detailed as follows.

[1]、[2] 给必要背景；[3] 用 `matrix D → is introduced` 和 `if Rf...then D...` 陈述条件命题；[4] 才从 explanation 进入 proof。它展示 A4 的“条件靠近 claim”，但 **PE 窗口证明的整条 response 仅此一例**；PDF p.8 的严格不等号与 `D(t)>σ` 写法仍需数学核查，不能从这个例子推出 C1 可生成。

## 5. Sentence realization / language fingerprint：句子如何承担前后状态

### 5.1 Semantic subject 与 core verb 的责任对应（A3）

| 句子实际负责什么 | 原文可观察的 subject → core verb | 为什么接在前句之后；证据等级 |
|---|---|---|
| 作者接受 concern、设计或开展工作 | `we/the authors → agree, developed, design, conduct, proof-read` | concern 尚需作者态度或动作时由作者承担；S01 p.3、S09 p.11、S11 p.18、S15 p.20。`we agree` 明写只见 S01 一处，不生成固定同意句 |
| 可定位稿件对象发生修改 | `typos/statement/derivation/Figure → have/has been corrected, rewritten, added, modified` | reviewer 点到具体对象后，主语直接对应该对象；S02 p.4、S03 p.7、S05 pp.8–9、S06 p.9、S12 p.18。动作完成态跨 scene 重复，但 `corrected and updated` 的重复不转移 |
| 技术条件或关系进入论证 | `matrix D/PE condition/relationship/NE model → is introduced, satisfies, holds, is based on`；作者亦用 `we can obtain/derive` | 从“已改/有问题”转到“为何成立”时换技术对象与关系动词；S04 pp.7–8、S06 p.9、S09 pp.11–12。数学真值另核 |
| 测试设置与任务 | `tests/experiments → are conducted/have been performed`；`disturbance/parameters → is/are chosen`；`robot → is commanded to track` | 操作、设置、公平条件、任务由各自语义对象承担；S01 p.3、S13 p.18。`robot is commanded`、`disturbance is chosen` 各为单例措辞，不固定被动语态 |
| evidence 进入与被读出 | `results/disturbances/performance/details → are shown/depicted in Fig./Table`；观察可用 `maximum deviations/estimated parameters/tracking errors → are/are close to/are relatively large`，或 `we can see` | setup 后先给 locator，下一句读量值或方向；S01 pp.3–4、S10 pp.13/17、S13 pp.18–19。Figure/Table 常是介词后的地址，并非必须作 grammatical subject |

核心动词不是可随意替换的“高级词汇表”：`corrected` 指修错，`rewritten` 指重写叙述，`added` 指补推导，`conducted/performed` 指实际开展，`shown/depicted` 指证据定位，`obtain/derive/hold` 指数学关系。**谁做了什么、哪一对象改变了什么**决定主语与动词。`we` 可做设计、测试、比较等作者动作，不能被限制为感谢；但证据对象也不必强行换成 `we`。

### 5.2 条件、baseline、信息密度与术语延续（A4/B5）

- **条件邻接**：S04 p.7 把 PE 放入 `if Rf is PE, then D...` 的命题里，S07 pp.9–10 分开 nonzero/zero eigenvalue，S08 p.10 把 `(22)` 与恒等式放在式链前。可复用的是“受条件约束的主张让人就近找到条件”，不是所有条件句都要以 `If` 开头或都要与 claim 同一句。
- **baseline 邻接**：S09 pp.11–12 的 `[20]/Lagrange` 与其已有估计范围/计算比较同块；S10 pp.12–13/17 的 PID/MBAC 与 tracking/暂态/RMSE 的观察相连。baseline 的名字不能漂到另一指标旁。S10 的参数表后转 [27]，不能把 [16]/[20]/[27] 混称。
- **一句的信息责任**：S01 p.3 将加噪操作、σ 定义、公平参数与图号分到相邻句；S13 p.18 将平台、任务、结果图、观察分句；S04 p.7 可在一句里容纳技术对象与 if-condition。局部修正多为短 action/location/摘录，S04/S09/S10 因技术或多个证据块较长。PDF 没有支持“每句必须一个信息”“统一 20–30 words”的硬阈值。
- **术语连续**：`end-effector position/disturbance/parameters`（S01 pp.3–4）、`PE condition/D/Rf`（S04 pp.7–8）、`kinematic parameters/NE model`（S09 pp.11–12）、`PID/MBAC/FT/tracking error`（S10 pp.12–17）在相邻句反复复现。没有证据支持为避免重复而主动换同义词；但原文冗余段也不因此变成优点。

### 5.3 Figure/Table/result 与 manuscript location（A5/A6）

`evidence object → Figure/Table locator → observed value/direction/visual baseline` 是稳定子链。S01 p.3–4 先定位奇数扰动图、读 ±2/4/6 cm，再定位偶数估计图、读收敛；S13 pp.18–19 定位估计图后读 `most ... close to nominal values (dashed line)`；S10 pp.13/17 先给 tracking 图与 RMSE，再读 PID/MBAC/FT，参数表则说明真值和两种估计列后作总体读取。S10/S16 的同表复贴不能算两份独立证据。**数字是 S01 的直接量化单例；不是所有结果必备数字。**

location 只提供核查路径：S03 p.7、S06 p.9、S13 p.18 先给 Section/Page 再贴修订句/式/实验段；S01 p.4、S10 p.17 在观察或讨论后给 location。`For your convenience` 常把正文转向摘录，`As suggested/According to...` 常把 comment 转向已做动作；位置可以是句尾、下一句或摘录前，**不固定最后一行**。同一 response 反复给相同位置是源冗余。

### 5.4 Connectors 只代表已发生的关系

`However` 在 S09/S10/S15 中从既有方法作用切到局限；`Additionally/Moreover` 在 S05/S10/S14 中换到另一动作，但 S14 证明连接词不能弥补漏答；`On the other hand` 在 S09 p.11 切到 NE 计算维度，仅 novelty 单例；`Therefore/Thus/This implies` 标推论，不能替代数学或实验支持；`For your convenience` 引入 excerpt/location，不能替代实质答复。它们是 **realization evidence**，不是必须依次使用的连接词清单。



## 6. Anti-overgeneralization：已被原文或 validation 否定的捷径

| 看似可写成规律 | 为什么不能升级；可保留的事实 |
|---|---|
| 实验必须用 `To further...` 开头 | S01/R1-C2 p.3 有该目的句，S13/R4-C3 p.18 真实实验以 `In addition, experiments...` 起；B4 稳定的是 action→concrete setup→locator→observation，不是入口词 |
| location 必须是整条 response 最后一行 | S03/R2-C1 p.7、S06/R2-C4 p.9、S13/R4-C3 p.18 均先报位置再贴内容；A6 只要求可追溯，不规定位置 |
| reviewer 前提有错就先写 negative claim 或“reviewer misunderstood” | S04/R2-C2 p.7 直接界定 PE 条件下的 D 命题；S09/R3-C1 p.11 先承认 [20] 已做工作再给区别。原文没有把负面否定句当默认入口；也不能据其缺席立“永禁负句” |
| Figure/Table 必须作 grammatical subject | S01 p.3 `disturbances/performance are shown in Fig...`、S10 p.13 `results are depicted in Figs...`；Figure/Table 多是 locator，主语依本句语义责任选 |
| 所有结果都必须给数字 | S01/R1-C2 p.3 给三组 ±cm；S13/R4-C3 p.18–19 定性读与 nominal 接近，S10/R3-C2 p.17 也多定性。数字化直接读取只有 C6 的特定场景 |
| novelty 回应应照 S09 写三个长段 | S09/R3-C1 pp.11–12 是 C2 单例且过长、含强 claim；多个贡献维度是该文事实，不是固定数量或长度 |
| 有了实验就能写 `robustness/effectiveness verified` | S01 p.4 的三个白噪声强度与 S13 p.19 的 nominal 收敛均不足支持泛化 robustness；两处原文这样写属 SOURCE DEFECT，不是 fingerprint |
| `we` 应只用于感谢或完全避免 | S01 p.3 有 `we agree/we conduct`，S09 p.11 有 `we developed`，S15 p.20 有 `we design`；A3 按动作责任选主语 |
| 每个 multi-concern response 都要编号 1)/2)/3) | S05 pp.8–9 按连续段展开，S10 pp.12–17 按段/图/表，S14 pp.19–20 用两个 action 块；B6 不给版式编号规则 |
| S10 和 S16 的相同参数表证明 Table 机制跨两份独立数据稳定 | S10/R3-C2 p.17 与 S16/R4-C6 pp.20–21 几乎复用同一 43 行表与说明，只是一份材料；C5 仍为 reference only |
| 原文在 concern 充分覆盖时才结束 | S12/R4-C2b p.18 未写清输入输出，S14/R4-C4 pp.19–20 未测三种指定非理想因素，S10/R3-C2 p.13 实验只被宣布；A2/B6 不包含该停止行为 |
| 原文结论总与 evidence 严格同范围 | S01/S13 的宽 robustness claim 直接反证；B4 在 observation 之后不再给稳定 conclusion 步骤，结论范围属于 §7 的审计门槛 |

## 7. Independent quality gates：新 response 的审计要求，不是 TIE fingerprint

下表的“应检查”是为了避免把 PDF 的不足复制到新回复，**不声称江 TIE_2621 作者稳定做到**。它可以决定新稿某块是否足以结束，但不能用于回写 A2/B4/B6 的 descriptive 定义。

| Gate | 新 response 应检查什么 | PDF 反例与隔离结果 |
|---|---|---|
| **Concern completeness** | 将 reviewer comment 拆成可分别回答的事项；逐项查有无具体 action、explanation 或 evidence，若没有就明确边界。B6 只预测不同功能块，不保证全覆盖 | S14/R4-C4 pp.19–20 以一般外扰替代量化/延迟/脏微分；S10/R3-C2 p.13 真实实验仅宣告；S12/R4-C2b p.18 未说明 Figure 1 的具体输入输出。**SOURCE DEFECT** |
| **Evidence → claim boundary** | 对每个 observation 记录被测平台、变量、强度、baseline 与 metric；结论不得越过这些条件。B4 止于 observation，不把谨慎结论冒充原文稳定末块 | S01/R1-C2 p.4 的白噪声结果与 S13/R4-C3 p.19 的 nominal 接近被写成一般 robustness verified；S10/R3-C2 p.17 的总体精度/效果说法还受表内反例限制。**SOURCE DEFECT** |
| **Mathematical correctness** | 核对式号、维度、量词、时间区间、`≥`/`>`、正交矩阵条件和从假设到推论的每一步；“贴出推导”不等于成立 | S04/R2-C2 pp.7–8 的严格不等号及 `D(t)>σ` 矩阵/标量混写；S05/R2-C3 pp.8–9 的 SVD 尺寸/符号变化；S09/R3-C1 p.12 从模型降阶到 PE 成立的跳跃。**SOURCE DEFECT/需独立核验** |
| **Terminology / version / Figure / Table consistency** | 同一术语、baseline 引文、旧新式号、图表编号、修订 section/page 在 response、附图和稿件间逐项一致；A6 的“有 location”不自动保证 location 正确 | S01/R1-C2 p.3 `Figs.2-5` 对实际 Figs.1–6；S10/R3-C2 pp.13–17 `[20]/[27]`、`MBAC/MARC`、`Table III/Table 1`；S13/R4-C3 pp.18–19 轨迹/估计图号错配；S16/R4-C6 pp.20–21 `Table II/III/Table 2` 与 Section V/IV 不一。**SOURCE DEFECT** |
| **Language and redundancy** | 在保留原文信息顺序的前提下核对主谓一致、搭配和重复；不能把错误句法“修好以后”伪称作者原句 | S01 `sensors data may subject to/depicted as shown`，S06 `detailed formulated`，S09 冗长和 `fast and accurate convenience`，S10 `verity/gradient decent/conducted and performed`，S11 `help us polishing`，S16 `The detailed of...`；S04 证明/Remark 复贴。**SOURCE DEFECT** |

质量 gate 与机制的关系是单向的：**先**用已验证 A/B 描述 PDF 里可靠的组织与表达，**再**用 gate 审查新稿的事实和完成度。gate 不反向制造“江 TIE 作者一向充分覆盖、谨慎收束、编号正确”的假规律。

## 8. C1–C6：单例参考，不是生成路径

| C / reviewer situation | 唯一 scene 的可观察组织 | 为什么只能 reference only |
|---|---|---|
| **C1 proof challenge** | S04/R2-C2 pp.7–8：PE 条件命题→窗口积分/权重→D 下界→Remark/location | 只有一次核心 theorem 挑战；严格 `>`、矩阵/标量记号有缺陷。B3 的局部推导不是第二例 |
| **C2 novelty** | S09/R3-C1 pp.11–12：[20] 已做内容→本文运动学范围→NE/Lagrange 计算差异→SVD/PE 降阶维度→Section I/Page 2 | 完整 originality defense 只此一次；三段长度、绝对 novelty/PE claim 不可生成 |
| **C3 full multi-controller comparison** | S10/R3-C2 pp.12–17：PID/MBAC rationale→Figs.7–14 tracking/RMSE→参数 Table→总体读取→location | 综合图+表链只此一次，S16 是同表复用；实验子问在该 scene 未展开 setup |
| **C4 why-this-method** | S15/R4-C5 p.20：既有 adaptive control→gradient coupling 限制→finite-time/leakage 方案→优势主张 | 独立 method-motivation comment 仅一例；最后优势在此 response 中缺直接 evidence |
| **C5 explicit Table request** | S16/R4-C6 pp.20–21：已比较→真值/两方法列→location/摘录→总体读表 | S10 p.17 是同一参数表，不构成独立复例；总体精度还受表内反例限制 |
| **C6 quantitative noise** | S01/R1-C2 pp.3–6：三个 σ→三组扰动图→±2/4/6 cm→对应估计图 | 只有一组强度/数字链；S14 复用外扰测试，不能升级为普遍量化要求 |

如果新 comment 只匹配 C 类型，先回 PDF 和 02 的原 scene 看具体边界，再根据新稿证据自行决定组织；本基准不会把 C 的完整路径当已验证模式。

## 附录 A. 旧版句子级证据索引（保留正确原句，按新边界使用）

以下保留旧 00 的真实引句、主语—动词配对和若干核查记录，供“整条 response → block → 连续句 → 单句 → 词”时下钻。它们不得覆盖上文 A/B/C 分级；旧版中的冲突判定已在下列对应行直接修正。固定 realization skeletons 已由 §§2–5 的状态推进取代。

### A.1 功能分类表：真实原句与出处

| # | Response function | 2621 真实实现（1–3 个代表例） | 证据等级 |
|---|---|---|---|
| 1 | 感谢 reviewer 后很快进入实质 | “The authors sincerely thank the reviewer for the constructive comments. **We agree that it is important to consider the measurement noises in the estimation**, since the sensors data may subject to sensor noise in real applications.” (`R1-C2`)<br>“Thanks for your constructive comments to improve our paper. **As suggested by the reviewer, the statement of robot Jacobian matrix has been corrected and updated** in the revised manuscript.” (`R2-C1`)<br>“The authors sincerely thank the reviewer for the constructive comment. **According to your suggestions, the typos in equation (18) have been corrected. Additionally, the statement above (18) has been carefully rewritten**...” (`R2-C3`) | `A1`：礼貌之后尽快进入可回答的 concern、技术对象或已完成动作；这些实例恰在下一句出现，但不生成固定“第二句”规则。冗长感谢模板非核心机制。 |
| 2 | 直接回答或界定核心技术问题 | “In this paper, **the matrix D is introduced for the verification of PE condition**, i.e., **if** the regressor vector \(R_f\) in equation (11) is PE, **then** the matrix D is positive definite, with \(\lambda_{\min}(D)>\sigma>0\).” (`R2-C2`)<br>“Very different from the previous work, in this paper, **we developed an adaptive parameter estimation algorithm for both the robot dynamic parameters and kinematic parameters**.” (`R3-C1`)<br>“In the literature [20], **the estimation algorithm is based on a conventional Lagrange dynamics model**... In comparison to the Lagrange model, **the NE model is of more computational efficiency**.” (`R3-C1`) | `A4/B5` 可复用的是条件或 baseline 靠近其受约束命题/差异；R2-C2 的整条证明为 `C1`、R3-C1 的整条 novelty defense 为 `C2`，均只供参考。原文没有默认先写 `reviewer misunderstood`。`Very different from...` 及 `is of more computational efficiency` 为 `SOURCE DEFECT / DO NOT TRANSFER`。 |
| 3 | 承接 reviewer 合理的 concern | “**We agree that it is important to consider the measurement noises in the estimation**, since the sensors data may subject to sensor noise in real applications.” (`R1-C2`)<br>“**As the reviewer pointed out, the adaptive estimation technique is important** for robot manipulators to achieve better control performance and has been widely investigated...” (`R3-C1`)<br>“The conventional PID control methods have achieved great success in robot manipulators control. **However**, satisfactory control performance may not be obtained...” (`R3-C2`) | 可观察到短承接后转入作者自己的技术范围；不设“只占一句”硬规则。`As the reviewer pointed out` 接受合理前提，不接受否定性总评。`sensors data may subject to` 为语法缺陷。 |
| 4 | 澄清误解或区分两个概念，不过度防御 | “Very different from the previous work... we developed an adaptive parameter estimation algorithm for **both the robot dynamic parameters and kinematic parameters**.” (`R3-C1`)<br>“In the literature [20], the estimation algorithm is based on a conventional **Lagrange dynamics model**... On the other hand... the **Newton-Euler (NE) dynamic model** has been employed...” (`R3-C1`)<br>“In this paper, the matrix D is introduced... **if** the regressor vector \(R_f\) ... is PE, **then** the matrix D is positive definite...” (`R2-C2`) | 已验证的子机制是具体条件贴近 D 命题（`A4`）、前作能力贴近技术差异（`B5`）；不能把这两个单例合成一条固定的“误解纠正流程”。这两处未以 `the reviewer misunderstood` 等负面判断开头，但不构成禁令。`R3-C1` 三段篇幅不可迁移。 |
| 5 | 报告 manuscript 中已完成的修改 | “the statement of robot Jacobian matrix **has been corrected and updated** in the revised manuscript.” (`R2-C1`)<br>“the typos in equation (18) **have been corrected**. Additionally, the statement above (18) **has been carefully rewritten**...” (`R2-C3`)<br>“more details about the derivation of equation (34) ((35) in the revised version) **have been added** in the revised manuscript.” (`R2-C6`) | `REPEATED/STABLE`：具体 manuscript object 作主语，`has/have been + past participle` 报告完成态；动词与对象绑定，而不是只写笼统程度。 |
| 6 | 引入新增 experiment / comparison | “**To further show the effectiveness** of our proposed estimation algorithm, **robustness tests are conducted by adding unknown external disturbances** to the system model.” (`R1-C2`)<br>“**To further verity the effectiveness** of proposed algorithm, **comparison studies have been carried out based on a PID controller and a model based adaptive controller (MBAC) [16]**.” (`R3-C2`)<br>“In addition, **experiments have been further performed based on the left robotic arm of a real Baxter robot**...” (`R4-C3`) | `B4` 经验证的是 **action → concrete setup → evidence locator → observation**；purpose-fronting 仅是 S01/S10 的入口实例，S13 用 `In addition`。`verity`、`experiment results are performed`、`conducted and performed` 为 `SOURCE DEFECT / DO NOT TRANSFER`。 |
| 7 | 交代 platform、task、setting、baseline、metric | “experiments have been further performed **based on the left robotic arm of a real Baxter robot**... **the robot is commanded to track a set of sinusoidal and cosine trajectories**...” (`R4-C3`)<br>“comparison studies have been carried out **based on a PID controller and a model based adaptive controller (MBAC) [16]**. The comparison results are depicted in Figs.7-14.” (`R3-C2`)<br>“Fig. 14 show the profile of the **root mean square error (RMSE) of tracking error of the 7 joint**.” (`R3-C2`) | `MIXED`：platform→task 和 baseline→metric 分别出现并可迁移；但 2621 没有一处用一个紧凑句群完整串起 platform/task/setting/baseline/metric，故“完整五要素模板”为 `SINGLE-INSTANCE/NOT ESTABLISHED`。 |
| 8 | 自然定义符号、条件和评价标准 | “The external disturbance is chosen to be \(d(t)=\sigma w(t)\), **where** \(\sigma\) is the degree of intensity, and \(w(t)\) is the white Gaussian noise with the power of 1 dBW.” (`R1-C2`)<br>“For fair comparisons, **the parameters in the adaptive estimation are chosen to be the same**.” (`R1-C2`)<br>“if the regressor vector \(R_f\) in equation (11) is PE, then the matrix D is positive definite, with \(\lambda_{\min}(D)>\sigma>0\).” (`R2-C2`) | 具体条件紧邻所限定的 claim、符号在公式附近释义，是可迁移机制；`where`、独立公平条件句和 `if...then...` 是各自语境中的实现实例，不是固定句型。2621 没有把数学符号机械当“缩写”塞进括号。 |
| 9 | 引入 Figure / Table | “**The disturbances** added on the measured end-effector position **are shown in Fig. 1, Fig. 3 and Fig. 5**, with \(\sigma\) chosen to be...” (`R1-C2`)<br>“**The comparison results are depicted in Figs.7-14**.” (`R3-C2`)<br>“**The detailed of the estimated parameters are shown in Table III, where** the real value..., the parameters estimated by... [two methods] have been presented, respectively.” (`R3-C2`; 同型句又见 `R4-C6`) | `A5`：evidence object→Figure/Table locator→observation 跨独立 scene 成立；Table 后用 `where` 释列的两处几乎复用同一材料，只算一个实例。`The detailed of...`、`depicted as shown` 为源语法/冗余缺陷。 |
| 10 | 直接读取实验结果和数字 | “the maximum deviations added on the measured positions are **about ±2 cm, ±4 cm and ±6 cm, respectively**.” (`R1-C2`)<br>“most of the estimated parameters are **close to the nominal values (dashed line)** with satisfactory convergence performance.” (`R4-C3`)<br>“the tracking errors of the PID control... are **relatively large**... The MBAC controller has achieved... steady-state tracking performance... **but** the performance of transient state is much lower than the proposed FT method.” (`R3-C2`) | 直接数字句为 `SINGLE-INSTANCE`；图中定性读取为 `REPEATED/STABLE`。数字直接放在 observation 谓语补足语中，没有先加多层 meta 包装。2621 的大表未逐行复述数值，只给总体判断。 |
| 11 | 表达有利比较、不利比较以及转折 | “**although** the stable tracking can be obtained by using all three types of controller, the tracking errors of the PID control... are relatively large...” (`R3-C2`)<br>“The MBAC controller has achieved... steady-state tracking performance... **but** the performance of transient state is much lower than the proposed FT method.” (`R3-C2`)<br>“**In comparison to the Lagrange model**, the NE model is of more computational efficiency... **Therefore**, ... [it] is computationally more efficient and more suitable...” (`R3-C1`) | `REPEATED/STABLE`：先承认共同/有利部分，`although/however/but` 后放真正区分点；baseline 紧贴比较级。没有“本方法在某指标更差”的诚实不利结果实例，因此该用途不能由 2621 建立规则。比较级语法多处有缺陷。 |
| 12 | 从 evidence 进入 conclusion 的原文与边界 | “**This implies that** D is positive definite and its minimum eigenvalue satisfies \(D(t)>\sigma\) with \(\sigma=e^{-\vartheta T}\varepsilon\).” (`R2-C2`；结论受前文 PE 条件约束)<br>“The test results show that the estimated parameters are observed with satisfactory convergence rate and accuracy, **even in the presence of external disturbances**.” (`R4-C4`)<br>“In terms of the above test results, **the robustness of the proposed estimation algorithm can be verified**.” (`R4-C3`) | `A5/B4` 已验证的是 locator→observation，**不是**稳定的 bounded conclusion。R2-C2 为 `C1` 单例且式子需核；R4-C4 只复用 S01 的外扰测试；R4-C3 的广义 robustness 属 `SOURCE DEFECT / DO NOT TRANSFER`。claim 范围另由 §7 gate 审查。 |
| 13 | 说明修改后的 manuscript location | “Please see **Section II, Page 2** of the revised manuscript for details.” (`R2-C1`)<br>“The above discussions have been summarized as a remark and presented in **Section III, Page 4** of the revised manuscript...” (`R2-C2`)<br>“As suggested, the above robustness tests have been presented in **Section IV, Page 7** of the revised manuscript.” (`R1-C2`) | `A6`：具体 Section/Page 使修订可查；S03/S06/S08/S13 的 location 在摘录前，S01/S10 可在结果后。**不是**固定独立尾句；位置与编号正确性另审。 |
| 14 | 局部 response 的短篇幅与实际停止 | “As suggested by the reviewer, Figure 1 has been modified and updated in the revised manuscript. **Please refer to Section II, Page 3 for more details.**” (`R4-C2b`)<br>“According to your suggestion, these typos have been all corrected... **The modifications are highlighted in blue color and please refer to Section I, Page 1 for more details.**” (`R1-C3`) | `A2/B1`：局部问题通常在动作、location 或摘录后较快结束；但 R4-C2b 没具体解释输入输出，故短篇幅与“充分覆盖”不能等同。技术问题也可能复贴或重复；停止充分性只在 §7 审计。 |

### A.2 句子实现观察：主语、动词、顺序、限定和衔接

| 功能组 | 常见 grammatical subject 与核心动词 | 典型信息顺序与句长 | condition / baseline / limitation 的位置 | 前后句衔接 | 可迁移机制 | 不可迁移部分 |
|---|---|---|---|---|---|---|
| 感谢后进入实质（#1、#3） | 感谢句用 `the authors/we + thank`；实质句可换成 `we + agree`，或 `statement/typos + has/have been corrected/rewritten`。 | 通常很快由礼貌转到可回答的 concern、对象或动作；无固定词数或“必须第二句”规则。 | concern 的现实条件可后接 `since...`；不在感谢句里堆限定。 | `According to your suggestion`、`As suggested by the reviewer` 可标从感谢转动作，但连接词不是动作本身。 | `A1`：尽快出现具体 concern/对象/动作，不固定句数。 | `which are appreciated` 等二次感谢是冗余套话；`Thanks for ... to improve our paper` 搭配生硬。 |
| 核心问题的回答/澄清（#2、#4） | 主语服从语义责任：`the matrix D is introduced`、`the estimation algorithm is based on...`、`the NE model...` 陈述技术事实；`we developed/design` 陈述作者的设计动作。 | R2-C2 的 PE 条件→D 命题→证明、R3-C1 的前作范围→本文差异均为完整 response **单例**；跨场景只验证条件/baseline 邻接。不能规定统一句长。 | 数学条件嵌入核心 claim：`if..., then...`；比较 baseline 放在 `from/in comparison to [20]/the Lagrange model` 中，紧邻比较谓语。 | `However` 可引出 gap；`On the other hand` 在 R3-C1 切换第二维；`Therefore/This implies` 仅表面标记推论。 | `A4/B5`：技术事实及比较维度清楚、条件/baseline 邻接；不能复制 C1/C2 的全链。 | `Very different from...`、`It should be emphasized that, this is not a trivial issue` 带防御色彩；三段式 novelty 辩护过长且含若干绝对 claim。 |
| 已完成修改（#5、#13、#14） | manuscript object 作主语反复出现：`statement/equation/derivation/Figure/discussion + has/have been + corrected/rewritten/added/modified/presented`。 | 对象→完成动作→具体 location/摘录；S03、S06 在 location 后仍贴文本或公式，故无固定尾句与词数。 | 版本变化可紧跟对象：`equation (19) ((20) in the revised version)`；位置可在句末、下一句或摘录前。 | `Additionally` 并列第二动作；`For your convenience` 引摘录；`As suggested` 可标动作来源。 | `A3/A6`：对象绑定实际完成动作，位置服务核查；局部问题通常短。 | `minor revisions` 并未出现；`corrected and updated`、`modified and updated` 有语义重叠，不必照搬。 |
| 新增 experiment/comparison 与 setup（#6、#7、#8） | 主语服从语义责任：`we` 可承担测试/比较动作；`tests/comparison studies/experiments` 承担操作；robot 承担 task；disturbance/parameters 承担 setting。后两种具体句型各只见一例。 | 已验证的实验句群为 **action → concrete setup → evidence locator → observation**；purpose 可在前，S13 直接从 `In addition, experiments...` 进入 action；不设句长。 | setup 可用 `by adding...` / `based on...`；baseline 紧邻比较动作；符号在公式旁解释；fairness 可独立成句。 | `To further show...` 只见于某些入口；`In addition` 也可引实验；设置完成后结果才进入图。 | `B4/A3`：从操作与设置到 evidence/observation；结论范围属于独立 gate。 | `experiment results are performed` 搭配错误；`conducted and performed` 重复；`Without loss of generality` 对经验设置的适用性可疑。 |
| Figure/Table 与结果读取（#9、#10） | `results/disturbances/performance/details` 可作主语，`shown/depicted`；读取时也用 `maximum deviations are...`、`most parameters are close...` 或 `we can see/it can be observed`。 | `A5` 验证 locator→direct observation；随后是否 comparison/claim 依实际请求和证据，非固定第三句或统一词数。 | 参数值可在 Figure locator 句末 `with σ chosen to be...`；数字列表后置 `respectively`；视觉 baseline 可写 `(dashed line)`，均为具体场景实例。 | `As seen from the figures` 与 `We can see from the figure/Table` 把证据地址转观察；不要求下一句给总体 claim。 | evidence/result 常作主语，但 Figure/Table 多是介词后的 locator；数字读取只在 S01 清楚出现。 | `depicted as shown` 重复；`The detailed of...`、主谓一致、比较级和图表编号有缺陷，不能复制。 |
| 比较与结论边界（#11、#12） | 比较对象可作主语：`tracking errors... are relatively large`、`MBAC controller has achieved...`、`NE model...`；推论可见 `This implies...` 或 `test results show...`。 | `B5` 的共同状态是 baseline 已有作用→具体差异；复句或相邻句皆见，无统一长度。 | baseline 应紧贴比较维度；数学条件在命题附近；实验中的 `even in...` 只是一个原文限定实例。 | `although/but/however` 可标真实转折；`therefore/this implies` 不自动证明推论。 | 可迁移 baseline 与差异邻接；实验结论范围并非原文稳定做对，须经 §7 gate。 | `improved than`、`more estimation accuracy`、比较对象不对称和 `verified robustness/effectiveness` 均为源缺陷。 |

### A.3 Subject–verb 配对的句子级证据

| 要表达的意思 | 2621 实际偏好的 subject | 2621 实际核心动词 | 判定 |
|---|---|---|---|
| 作者接受 concern | `we` | `agree` | `SINGLE-INSTANCE` 的显式 `we agree`，但“感谢后立刻承接”的机制跨 comment 重复。 |
| 作者做出设计、修改、测试、比较或报告 | `we/the authors` | `developed`, `design`, `conduct`, `have ... addressed`, `have ... proof-read` 等与动作相符的动词 | `REPEATED/STABLE` 的是作者可为自身动作负责；不限制 `we` 只能用于设计，也不要求每个实验句都用 `we`。 |
| manuscript 改动 | `statement`, `typos`, `derivation`, `Figure`, `discussion/tests` | `has/have been corrected`, `rewritten`, `added`, `modified`, `presented` | `REPEATED/STABLE`。 |
| 实验动作 | `tests`, `comparison studies`, `experiments` | `are conducted`, `have been carried out`, `have been performed` | `REPEATED/STABLE`，但应去掉错误/重复搭配。 |
| task | `the robot` | `is commanded to track` | `SINGLE-INSTANCE`：只说明该句由 robot 承担 task；不推出 Case 不能作其他句子的主语。 |
| setting/公平性 | `the disturbance`, `parameters` | `is chosen`, `are chosen to be the same` | 各为 `SINGLE-INSTANCE`：只说明这些句子的设置对象与动词匹配；不规定 setting 句必须采用被动语态。 |
| evidence locator | `results`, `disturbances`, `performance/details` | `are shown`, `are depicted` | `REPEATED/STABLE`。 |
| evidence reading | `maximum deviations`, `estimated parameters`, `tracking errors` | `are`, `are close to`, `are relatively large` | `REPEATED/STABLE` 的 object-led observation；实际原文也频繁使用较弱的 `we can see`。 |
| 数学结论 | `matrix D`, `minimum eigenvalue`, `term/relationship` | `is positive definite`, `satisfies`, `converge/hold` | 具体 PE→D 正定全链仅 S04/C1 单例；可复用的是 `A3/A4` 的技术对象承担关系动词、条件贴近 claim。数学真值另审。 |

### A.4 原句核查记录

| 核查项 | 2621 实际证据 | 结论 |
|---|---|---|
| 是否写 `minor revisions` 等模糊修改程度 | 全文无 `minor revision` / `minor revisions`。封面和 AE response 有 “the paper has been duly revised”, “significantly improved”，但逐条回复主要落到具体对象和动作。 | 不把 `minor revisions` 当作 2621 句式。可迁移的是对象级完成动作；封面式程度副词不能替代证据。 |
| 修改动作怎样落到对象 | `typos/equation/statement` → `corrected`; `statement` → `rewritten`; `derivation/details/analysis` → `added`; `tests/comparisons` → `conducted/carried out`; `discussion/tests` → `presented`; `Figure` → `modified and updated`。 | `REPEATED/STABLE` 的核心是“对象选择动词”，不是统一写 `revised`。避免 `conducted and performed`、`modified and updated` 等重复。 |
| 数学符号是否被当作缩写放括号 | 缩写定义见 `persistence excitation (PE)`, `singular-value-decomposition (SVD)`, `model based adaptive controller (MBAC)`, `root mean square error (RMSE)`；数学符号则用公式后 `where σ is... and w(t) is...` 释义。 | 2621 区分 acronym 与 symbol；没有把 `σ` 等机械写成括号缩写。 |
| 是否有 `the values cited in the comment` 式 meta-response | 全文未出现 `the values cited in the comment` 或同型表达。数字句直接写 “maximum deviations... are about ±2 cm, ±4 cm and ±6 cm”。 | 直接陈述被测量对象和数值，不把 reviewer comment 当数据载体。 |
| experiment/comparison 如何从操作进入 setup | S01/R1-C2 用 `To further show...`，随后 `tests ... conducted by adding...`、定义 disturbance/intensity 与公平条件；S13/R4-C3 用 `In addition, experiments...`，随后 Baxter arm→tracking task→Figures。 | `B4` 验证 **action→concrete setup→locator→observation**；purpose-fronting 可有可无，不能称稳定入口。`verity` 是原文错误。 |
| robot / task / setting 的主语责任 | `R4-C3` 中 `the robot` 作 task 主语；`R1-C2` 中 `tests`、`the external disturbance`、`the parameters` 分别承担测试、设置和公平比较动作；`R3-C2` 中 `comparison studies` 承担比较动作。`R1-C2` 还写 “we conduct the tests”。 | `A3`：主语按本句语义责任选择；`we/the authors` 也可以承担作者主动的设计、测试、比较和报告。`the robot is commanded` 等具体措辞只有单例，不设禁词/必用主语。 |
| 数字是否直接陈述 | 唯一清晰的直接数字读取是 “maximum deviations... are about ±2 cm, ±4 cm and ±6 cm, respectively.”；表格虽含大量数字，正文仅概括 closeness/accuracy。 | 直接数字句为 `SINGLE-INSTANCE`，但可确认没有先加解释性包装；不能据此宣称 2621 总是量化。 |
| Figure/Table 如何承担 evidence 主语 | 2621 常让 `results/disturbances/performance/details` 作语法主语，Figure/Table 位于 `shown/depicted in` 介词短语；随后才用 `the figures/Table` 作为观察来源。 | `A5`：evidence object→locator→observation 跨 S01/S10/S13 独立成立；S10/S16 的同表材料不二计。不是每句都以 Fig./Table 起句。`SOURCE DEFECT`：S01 Figs.2–5 对 Figs.1–6，S13 正文/附图编号，以及 S10/S16 的 Table/引文编号错配。 |

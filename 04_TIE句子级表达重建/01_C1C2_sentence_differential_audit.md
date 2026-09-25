# TCYB Referee 4 Comment 1/2：top-down differential audit

## 0. 范围、依据与判定口径

- 审计对象为当前 `Response-TCYB.tex` 与其编译 PDF 中 Referee No. 4 的 Comment 1、Comment 2；PDF 物理页分别为 pp.6–11、pp.11–13。科学意图以 `00_project/response思路_作者原文.txt` 锁定。表达金标准是江 TIE_2621 PDF；正式机制以已验收的 realization `00` 及最终知识库 00–08 为准。旧 `01` 只作历史核对，本表重新判定。
- 顺序为科学主线 → situation/整条组织 → 功能块 → 连续句状态 → 逐句主语、核心动词、句法、限定与 baseline、术语、连接和用词 → 独立质量门槛 → 连续通读。**A1–A6 是跨 scene 核心，B1–B6 仅按场景触发；C1–C6 仅供回查。** B4 的已验证链止于 observation；B6 的分块不保证原作者逐项答全。充分性与 claim 边界由独立 gate 判定。
- 句子编号按阅读顺序。C1 的正文 30 句与四幅图的 caption 20 个句子/并列标签共 50 项；C2 正文 25 句。四个图 caption 中的名词标签虽无谓语，也逐项检查映射、术语与信息位置。两条编号小标题另作结构项，不混入句数。公式和引文编号按 TeX 原貌识别；表中为可定位的原句或唯一识别片段，未提供替换英文。
- `KEEP` 表示当前实现已达要求；`REWRITE` 是实质表达缺陷；`MOVE` 是句子可用而位置妨碍认知推进；`DELETE` 是无新任务的重复；`MERGE` 是拆句造成实质重复。本次没有因“还有别的写法”作非 KEEP。非 KEEP 的任务、缺陷、目标 realization 与词层问题见逐句表及紧随的定点说明。

### 金标准定位

| 已验证机制 | TIE 原文锚点（物理页） | 本轮可用边界 |
|---|---|---|
| A1/A2/A3/A4 | R1-C2 pp.3–6；R2-C3–C6 pp.8–10；R3-C2 pp.12–17 | 尽快进入可核查的技术事实/动作；篇幅随任务数变；主语和动词承担实际语义；条件与 baseline 就近。A2 **不**预测“充分答完才停止”。 |
| A5/A6、B4 | R1-C2 pp.3–6；R4-C3 pp.18–19；R3-C2 pp.13–17 | action → concrete setup → Figure locator → observation；稿件位置用于追溯、没有固定末尾；不强制 `To further` 或 conclusion。 |
| B5/B6 | R3-C1 pp.11–12；R3-C2 pp.12–17；R2-C3 pp.8–9；R4-C4 pp.19–20 | 同一维度内锁定 baseline 再读差异；多 concern 带来不同实质块。R3-C1 的完整 novelty 和 R3-C2 的完整多控制器路径仍为 C-only。 |
| Source defect 隔离 | R1-C2 p.4；R4-C3 p.19；R4-C4 pp.19–20 | TIE 原文的过强 robustness、未答全、语法或编号瑕疵不转移到当前 Response。 |

## 1. Comment 1

### A. Scientific-intent lock 与 response-level verdict

**作者主线**：先纠正“声称 sparse GP 中最低计算成本”的前提；用最小框架区分 ILC 跨轮任务代价收敛与控制步内 `t_comp^max < Δt`；解释原稿 computational-burden 讨论中 fast-AGP/standard GP 与 CRBFNN/lattice RBFNN 各自的 baseline；承认只变刚度并看 `J_j` 不足以回答跨任务计算效率；补不同任务及权重/刚度设置的逐步运行时间比较；正文只作已确认且可核查的局部澄清。评论真正要求的是**计算效率结论的适用范围**，不是一般收敛稳健性。

**核对结果**：现稿已经区分两个评价层级，并给出 Cases 1/2、`W_x` 与 `S_e(t)` 的 setup、Figure、`J_j` 和 `t_comp^max` 读取；明确保留了 proposed method 在线时间高于 IL-SOGP 的不利结果（S23、S39）。末句只限于已测场景满足各自控制周期，未把这些图说成“最低计算成本”。这符合主线。当前“已作 minor revisions”的具体修改及稿件位置未给出，无法从这两份 Response 文件核实；这是可追溯性缺口，不推定稿件未修改。

**Response-level：NEEDS REVISION。** Situation 为错误最低成本前提 + 评价量混淆 + 旧证据不足 + 新跨任务/设置比较，调用 A1–A6、B4、B5、B6；证明挑战/novelty 的 C-only 路径不适用。当前顺序遵循作者锁定的主线：claim 澄清 → 最小认知框架 → 原稿 computational-burden 的两组 baseline 解释 → S12 进入第二核心点 → 新证据。实质证据链大体顺；修订重点是把抽象意图句改成具体 claim 边界，并把“稿件改了什么”写成可追溯动作，而非移动 S12 或重写图表结果。

### B. 当前 block map（按现有顺序）

| 现有块 | 当前内容及其必要性 | 判定与目标位置/边界 |
|---|---|---|
| C1-B0，S01–S03 | 致谢、最低成本前提、两种评价层级入口。reviewer 需要先知道真实 claim 边界。 | **REWRITE** S02 的“作者意图”入口；S01/S03 保留。实际评价对象/范围应在前面可抓取。 |
| C1-B1，S04–S08 | ILC iteration → `J_j` → 跨轮收敛；control step → `t_comp^max < Δt`。这是纠正计算量混用所需的最小技术关系。 | **KEEP**；不因比 TIE 局部 correction 长而机械压缩。 |
| C1-B2，S09–S11 | 承认原稿描述不清、区分两组 computational-burden baseline、宣称修改。 | **REWRITE** S09/S11 的具体对象和动作；baseline 句 S10 保持。需在实际稿件核对后给可识别位置/改动，A6 不要求置于末尾。 |
| C1-B3，S12 | 承认“只变刚度 + 只看任务代价”未答计算效率普适性，正式进入第二核心点/新增实验块。 | **KEEP**：位于 claim 澄清、最小认知框架和原稿两组 baseline 解释之后，紧接新 evidence，符合作者锁定的顺序。 |
| C1-B4，S13–S23 + Fig.1/2 captions | 新任务 action → robot/task/control-period/baselines/metric setup → Figs.1/2 → Case 1/2 `J_10`、逐步时间与 IL-SOGP 不利对照。 | **KEEP**。B4/A5 的核心推进已实现；不要求 purpose-first，但现有 purpose 句有实际任务。 |
| C1-B5，S34–S39 + Fig.3/4 captions | 原两自由度任务的权重/刚度变体 action → 具体设置 → locator → task cost 与运行时间读取。 | **KEEP**。这是第二个独立设置块，不因再次使用 `To further` 就判错；后者不是生成规则。 |
| C1-B6，S50 | 在已测 Cases/变体及各自控制周期内归纳实时性。 | **KEEP**。结论是条件型且范围相称，不将 conclusion 当成 B4 必备末块。 |

两个编号标题分别预告“评价框架”和“新增比较”，有实际导航功能，**KEEP**；不因 TIE 不强制编号而删除。现稿没有给出可定位的 manuscript excerpt/location；此缺口由 C1-B2 定点处理，不能虚构页码。

### C. 连续句与状态推进

| 连续句群 | 上句留下的认知需求 → 下句实际承担 | 判定 |
|---|---|---|
| S02→S03→S04–S08 | S02 的“并非最低”只陈述意图；S03 引出两层评价，S04–S08 按作者主线落到 `J_j` 与 `t_comp^max < Δt`。 | **S02 REWRITE；S03–S08 KEEP**。先给具体 claim 边界，再按原序保留最小认知框架；否定 reviewer 前提不需要评判其理解。 |
| S08→S09–S11→S12 | 判据建立后，S09–S11 解释原稿 computational-burden 的 fast-AGP/GP 与 CRBFNN/RBFNN baseline；S12 随后承认旧 stiffness/`J_j` 证据不足，进入第二核心点。 | **S09/S11 REWRITE；S12 KEEP**。此处的块转换由新的证据缺口承担，现有顺序符合作者主线。 |
| S13–S19→S20–S23 | 新任务目的与完成动作之后，robot/contact/`Δt`、baselines、输出矩阵、两项 metric 逐项设定；Figs.1/2 定位后先读 `J_10`，再读逐步时间和不利 IL-SOGP 对照。 | **KEEP**。B4/A5 已兑现；S23 的 `but` 有真实“耗时更高/仍小于周期”的转折。 |
| Fig.1/2→S34–S39→Fig.3/4→S50 | 第一组“不同任务”之后，第二组带来新的 `W_x`/`S_e(t)` 操作与 20 ms 条件；locator 后读 `J_10` 与时间；末句归纳两组测试。 | **KEEP**。不同周期 10/20 ms 始终贴近各自结果，未把 20 ms 外推到 Cases 1/2。 |

### D. 逐句审计（C1-S01–S50）

表中“核查”逐项覆盖语义主语/核心动词、主从关系和信息序、条件/baseline/术语、连接词与实际词语；caption 标签按“无谓语映射”检查。

| ID | 当前原句/唯一片段 | 句内核查与句间责任 | 判定 |
|---|---|---|---|
| C1-S01 | The authors sincerely thank the reviewer for the constructive comment. | authors→thank 承接 concern；礼貌词不过量，下一句应进入实质。 | **KEEP** |
| C1-S02 | The evaluation is not intended to identify the sparse GP method with the lowest computational cost. | evaluation→is not intended 只述意图；`the evaluation` 无具体对象，真正 claim 边界延迟。 | **REWRITE** |
| C1-S03 | This study distinguishes ILC learning convergence from control-step real-time computation. | study→distinguishes 作两层评价的入口；下一组用正式量具体化，不把两个名词当同义词。 | **KEEP** |
| C1-S04 | In iterative learning control (ILC), the same task is executed over successive iterations. | task→is executed；ILC 条件前置，给 S05 的 iteration 单位。 | **KEEP** |
| C1-S05 | Each iteration `j` contains a sequence of control steps and yields the task cost `J_j` accumulated over the complete iteration. | iteration→contains/yields；单一层级内两动作，`J_j` 定义就近，无换名。 | **KEEP** |
| C1-S06 | Accelerated convergence therefore means reaching a prescribed level of `J_j` in fewer iterations. | convergence→means；`therefore` 由 S04–S05 的 iteration 单位推出评价量。 | **KEEP** |
| C1-S07 | Online computation is evaluated at each control step, where the calculation must be completed before the next control update. | computation→is evaluated；`where` 贴控制步条件，与跨轮量分开。 | **KEEP** |
| C1-S08 | Real-time feasibility requires `t_comp^max < Δt`. | feasibility→requires；判据紧贴受限定的 claim，短句收束 S07。 | **KEEP** |
| C1-S09 | We agree that the related descriptions in the manuscript were not sufficiently clear. | we→agree 承认表达问题，但 `related descriptions` 无可定位对象，后句才点 baseline。 | **REWRITE** |
| C1-S10 | In the discussion of computational burden, fast-AGP is compared with a standard GP, whereas CRBFNN is compared with a lattice-distributed RBFNN [30]. | 两个方法→is compared；各 baseline 紧邻对象，`whereas` 是真实并列区别；引文位置可辨。 | **KEEP** |
| C1-S11 | We have made minor revisions to the relevant manuscript text to avoid possible misunderstanding. | we→have made 只述笼统动作；`minor`、`relevant text` 和目的状语均不能定位具体修改。 | **REWRITE** |
| C1-S12 | We agree that varying only `S_e(t)` and reporting `J_j` did not directly address the computational-efficiency concern under different tasks and settings. | we→agree；变量、metric 和缺口同句；在两组 baseline 解释后承接第二核心点，并自然引出新实验。 | **KEEP** |
| C1-S13 | To further evaluate real-time feasibility under interaction tasks that differ from the original two-DOF task, comparison studies have been conducted using Cases 1 and 2 in [10]. | studies→have been conducted；目的限定不同任务，动作与 Case 来源明确；`To further` 有真实作用，非强制入口。 | **KEEP** |
| C1-S14 | Both the task cost `J_j` and `t_comp^max` are reported. | 两个 metric→are reported；承接两个评价层级，不把代价当时间。 | **KEEP** |
| C1-S15 | These two cases use a simulated seven-DOF Franka Emika Panda robot that approaches an uneven surface and slides along the surface after contact. | cases→use，robot→approaches/slides；setup 先平台后接触任务，具体且自然。 | **KEEP** |
| C1-S16 | The robot, trajectory, and contact environment differ from those used in the original two-DOF task, and the outer-loop control period is `Δt=10` ms. | setup 对象→differ，period→is；旧任务 baseline 与新任务差异、时间条件同块可追。 | **KEEP** |
| C1-S17 | The compared methods are classical IL [18], IL-SOGP [10], and the proposed method. | methods→are；三组 baseline/target 明列，为后面结果比较定参照。 | **KEEP** |
| C1-S18 | Case 1 evaluates accurate tracking with `C=[25,0,1]`, whereas Case 2 evaluates compliant interaction with `C=[100,0,0.1]`. | Case→evaluates；两个目的及其矩阵紧贴；`whereas` 有实际对照维度。 | **KEEP** |
| C1-S19 | The comparison results are depicted in Figs. 1 and 2. | results→are depicted；Figure 作 locator，下一句实际读取。 | **KEEP** |
| C1-S20 | As shown in Fig. 1(c), the proposed method yields `J_10=80.40` in Case 1, compared with 86.01 for IL-SOGP and 88.61 for classical IL. | method→yields；locator、metric、Case、两 baseline 同句贴合。 | **KEEP** |
| C1-S21 | Fig. 2(c) shows that the proposed method yields `J_10=64.83` in Case 2, compared with 66.86 for IL-SOGP and 72.06 for classical IL. | Figure→shows 是允许的证据主语；Case/metric/baseline 顺序可读，不要求所有图都作主语。 | **KEEP** |
| C1-S22 | Figs. 1(d) and 2(d) show that the proposed method yields `t_comp^max=4.75` ms and 4.65 ms in Cases 1 and 2, respectively. | Figures→show；两个 panel、数值、Case 由 respectively 一一对应。 | **KEEP** |
| C1-S23 | Both values are higher than those of IL-SOGP but satisfy `t_comp^max < Δt` with `Δt=10` ms. | values→are/satisfy；先保留不利 baseline，再给 10 ms 条件；`but` 不是装饰性转折。 | **KEEP** |
| C1-S24 | Fig. 1 caption: Comparison results for classical IL, IL-SOGP, and the proposed method for Case 1 in [10]. | 无谓语范围标签；方法、Case、来源齐全，指向本图而非性能 claim。 | **KEEP** |
| C1-S25 | Fig. 1 caption: (a) Damping parameter `B_d(t)` and (b) stiffness parameter `S_d(t)` at iteration 10. | 无谓语 panel 映射；对象与 iteration 条件贴合。 | **KEEP** |
| C1-S26 | Fig. 1 caption: (c) Task cost `J_j`. | 无谓语 panel 映射；与正文 S20 同一 metric。 | **KEEP** |
| C1-S27 | Fig. 1 caption: (d) Maximum online computation time per control step `t_comp^max`. | 无谓语 panel 映射；逐步时间名称稳定。 | **KEEP** |
| C1-S28 | Fig. 1 caption: The dashed line in (d) denotes the control period `Δt=10` ms. | line→denotes；视觉基线与 10 ms 条件可核查。 | **KEEP** |
| C1-S29 | Fig. 2 caption: Comparison results for classical IL, IL-SOGP, and the proposed method for Case 2 in [10]. | 无谓语范围标签；Case 2 与三种方法明确。 | **KEEP** |
| C1-S30 | Fig. 2 caption: (a) `B_d(t)` and (b) `S_d(t)` at iteration 10. | 无谓语 panel 映射；沿用 Fig.1 的术语和条件。 | **KEEP** |
| C1-S31 | Fig. 2 caption: (c) Task cost `J_j`. | 无谓语 panel 映射；与正文 S21 一致。 | **KEEP** |
| C1-S32 | Fig. 2 caption: (d) Maximum online computation time per control step `t_comp^max`. | 无谓语 panel 映射；与正文 S22 一致。 | **KEEP** |
| C1-S33 | Fig. 2 caption: The dashed line in (d) denotes `Δt=10` ms. | line→denotes；图内阈值清楚。 | **KEEP** |
| C1-S34 | To further examine `J_j` and `t_comp^max` under different task objectives and environment conditions in the original two-DOF simulation task, additional comparisons have been conducted. | comparisons→have been conducted；切换到新设置块，metric 与原任务范围先给；重复 purpose 不替代新动作。 | **KEEP** |
| C1-S35 | The position-error weight `W_x` is set to `20I`, `50I`, and `200I`, while `W_f=I` is kept fixed. | `W_x`→is set，`W_f`→is kept；变化量/固定量同句，`while` 真实区分。 | **KEEP** |
| C1-S36 | Separately, `S_e(t)` is set to `10(sin πt)^2I`, `30(sin πt)^2I`, and `50(sin πt)^2I`. | stiffness→is set；`Separately` 准确标识另一组实验，不暗示同时改变两个变量。 | **KEEP** |
| C1-S37 | The comparison results are depicted in Figs. 3 and 4. | results→are depicted；再次从 setup 进入 locator，后两句读取。 | **KEEP** |
| C1-S38 | As seen from the figures, the proposed method achieves a lower `J_10` than IL-SOGP for all reported `W_x` values and `S_e(t)` settings. | method→achieves；baseline/metric 与已报告条件相邻，`all reported` 限定测试集合。 | **KEEP** |
| C1-S39 | Although proposed `t_comp^max` is generally higher than IL-SOGP, `t_comp^max < Δt` with `Δt=20` ms in all comparisons. | 让步从不利时间差转到 20 ms 判据；术语稳定，范围是当前图的设置。 | **KEEP** |
| C1-S40 | Fig. 3 caption: Comparison between the proposed method and IL-SOGP under different `W_x` values. | 无谓语范围标签；target/baseline/变化量同处。 | **KEEP** |
| C1-S41 | Fig. 3 caption: Top row: task cost `J_j`. | 无谓语 row 映射；与上排曲线一致。 | **KEEP** |
| C1-S42 | Fig. 3 caption: Bottom row: maximum online computation time per control step `t_comp^max`. | 无谓语 row 映射；与下排曲线一致。 | **KEEP** |
| C1-S43 | Fig. 3 caption: `W_x` is `20I`, `50I`, and `200I` from left to right, with `W_f=I`. | weight→is；panel 次序和固定条件紧邻，避免读图歧义。 | **KEEP** |
| C1-S44 | Fig. 3 caption: The dashed lines in the bottom row denote `Δt=20` ms. | lines→denote；视觉阈值与当前图条件一致。 | **KEEP** |
| C1-S45 | Fig. 4 caption: Comparison between the proposed method and IL-SOGP under different `S_e(t)` settings. | 无谓语范围标签；baseline 与环境变量同处。 | **KEEP** |
| C1-S46 | Fig. 4 caption: Top row: task cost `J_j`. | 无谓语 row 映射；不把代价当计算时间。 | **KEEP** |
| C1-S47 | Fig. 4 caption: Bottom row: maximum online computation time per control step `t_comp^max`. | 无谓语 row 映射；与正文 S39 同一时间量。 | **KEEP** |
| C1-S48 | Fig. 4 caption: `S_e(t)` is `10(sin πt)^2I`, `30(sin πt)^2I`, and `50(sin πt)^2I` from left to right. | stiffness→is；panel 次序与数值逐一对应。 | **KEEP** |
| C1-S49 | Fig. 4 caption: The dashed lines in the bottom row denote `Δt=20` ms. | lines→denote；与 S39 的判据条件一致。 | **KEEP** |
| C1-S50 | These results show that the proposed method satisfies `t_comp^max < Δt` in Cases 1/2 and the tested `W_x`/`S_e(t)` variations under their respective control periods. | results→show；Case/变量/各自周期把推论限定在实测范围，未声称最低成本。 | **KEEP** |

**C1 非 KEEP 定点说明**

| ID | 原句功能 | 真实 blocker 与具体词层问题 | 下一步应实现的语义（不写替换句） |
|---|---|---|---|
| S02 REWRITE | 纠正最低成本前提。 | `The evaluation` 语义对象虚，`is not intended to identify` 把可核查的 claim 状态变成主观意图；读者到 S08 才知道评价什么。不是因否定句本身错误。 | 用真实评估对象、baseline/判据直接给 claim 边界，保留“不声称 sparse GP 最低成本”的科学意思；不要扩张成全面计算优势。 |
| S09 REWRITE | 承认稿件表述引起误解。 | `related descriptions` 泛指，主句虽有 we→agree 却未指出到底哪一处 comparison 关系不清；与下一句 S10 的精确 baseline 脱节。 | 让被澄清的 computational-burden statement 或两组 comparison 对象承担明确语义责任，再自然接 S10。 |
| S11 REWRITE | 报告 manuscript revision。 | `made minor revisions` 的程度词、`relevant manuscript text` 的泛指和 `to avoid possible misunderstanding` 的目的语均不告诉 reviewer 改了什么；无可核位置。 | 在核对实际修订稿后报告具体 statement/句子发生的动作，并给可核查的 section/page 或短摘录；A6 不规定必须放最后。不得编造未确认的改动。 |

### E. C1 独立质量门槛与同作者感

- **Concern completeness**：不同任务（Cases 1/2）与不同设置（`W_x`、`S_e(t)`）均有独立证据；旧刚度/任务代价不足被承认。需补“原稿何处已限定 computational-burden claim”的可查说明，不能仅凭 S11 的宣告判完成。
- **Evidence→claim**：Figs.1–4 支持各已测 `t_comp^max < Δt`；不能推出所有 sparse GP 中最低计算成本，也不能推出未测任务都实时。S23/S39 的不利比较应原样保留。S50 当前有 Cases/变体/各自周期限定，可保留。
- **数学/版本一致性**：C1 文本中 `4.75, 4.65 < 10`、当前参数变体的 20 ms 条件与可见图/图注一致；`J_10` 读数与图方向一致。稿件修订文本及精确页码未随两份 Response 提供，只能标记待原稿核对。
- **连续通读**：证据主体的 action→setup→locator→observation、主语与量词很接近 TIE R1-C2/R3-C2；S12 在原稿 baseline 解释之后进入第二核心点，位置成立。“一眼不像”的主要来源是开头 `evaluation/intended` 的抽象意图表达，以及 S09/S11 的空泛 revision 语言。修复这三句即可，不需要移动 S12 或对其余 47 项进行无意义润色。

## 2. Comment 2

### A. Scientific-intent lock 与 response-level verdict

**作者主线**：纠正最低成本前提；简短重申跨轮学习收敛与逐控制步实时性；直接解释 `8.7617×7`、`2.4688×10`，承认 fast-AGP 每轮与估计累计仿真时间均比 SOGP 长而迭代数少；区分仿真运行时间与逐控制步实时性；承认旧 Table I 的呈现易混淆，说明新列改成每步最大在线计算时间；再给不同任务/设置的逐步时间证据。Reviewer 原文提到 `O(L^3)` 与 `O(L^2)`；作者已锁定的回应主线不要求为此单设复杂度讨论块。

**核对结果**：S04–S11 的层级与算术、S16–S24 的逐步时间证据和不利 IL-SOGP 对照，基本遵循作者主线；未把迭代数少说成总运行时间低。`8.7617×7=61.3319`、`2.4688×10=24.6880` 算术正确，并恰当地称 estimated。现稿宣告了 Table I 列与“accompanying text”改动，但修订稿正文未在本轮材料中提供，相关 claim 的实际修改范围与位置仍须核稿；不把未单独讨论渐近复杂度判作当前缺口。

**Response-level：NEEDS REVISION。** Situation 为最低成本 claim 澄清 + Table/metric 解释 + 多任务实时性实验 + 多 concern（A1–A6、B4、B5、B6；Table request 的 C5 仅参考）。现稿的计量区分与数值解释顺序符合作者主线；S02 的 claim 边界表达、S14 的修订位置及 S15 的证据来历仍需定点处理。B4 evidence 本体不需推倒重做。

### B. 当前 block map（按现有顺序）

| 现有块 | 当前内容及其必要性 | 判定与目标位置/边界 |
|---|---|---|
| C2-B0，S01–S03 | 致谢；否认“最低成本”意图；说明两种评价量。 | **REWRITE** S02，改为可核的 claim/baseline/criterion 边界；S01/S03 保留。S01 的三分法可由本 comment 中复杂度、Table 乘法与实时性争点推知，不判误引 reviewer。 |
| C2-B1，S04–S06 | 迭代→控制步→`J_j<1.5` 的轮数与 `t_comp^max < Δt`。 | **KEEP**；比 C1 更短，符合本 comment 的重申任务。 |
| C2-B2，S07–S11 | Table I 两个原运行时间的性质→乘法→不利结论→与逐步时间区分。 | **REWRITE** S10 的比较对象；S07–S09/S11 的数值与判据功能保留。S11 是对数值解释的局部闭合，不能只因 S06 已定义判据而删除。 |
| C2-B3，S12–S14 | 承认表呈现问题，宣告列替换及正文修改。 | **REWRITE** S12/S14；S13 的对象与动作具体。相关全文 claim 的实际修改和位置仍需核稿，不可凭“accompanying text”视为已答。 |
| C2-B4，S15–S19 | 汇总原 robot experiment 与 Cases 1/2 的逐步时间；Fig.1/2 定位并读出 10 ms 判据。 | **REWRITE** S15 的证据来历/动作分工；S16–S19 保留。S16 的 standard GP 比较只支持原平台实时性背景，不代表与 SOGP 的成本排序。 |
| C2-B5，S20–S23 | 两个设置的具体数值→20 ms 判据→Fig.3/4 所有设置→与 IL-SOGP 的不利时间比较。 | **KEEP**；先选值，再读全图，最后承认较慢；baseline、metric、condition 不混用。 |
| C2-B6，S24–S25 | 已测场景实时性归纳 + “未证明最低计算成本”的 claim 边界。 | **KEEP**；两句功能不同，结论有测试范围，末句限制证据解释。稿件 claim 修订的真实性仍须另行核对。 |

三个编号标题分别承载 Table 解释、Table 修订、不同任务/设置 timing 证据，**KEEP**；编号是本稿导航选择，非 TIE 必需句型。C2 没有附 Table I 修订表格或 manuscript excerpt；S13 的列名可读，但修改真实性与全稿一致性须回查修订稿，不能虚构 Table 内容。

### C. 连续句与状态推进

| 连续句群 | 上句留下的认知需求 → 下句实际承担 | 判定 |
|---|---|---|
| S02→S03→S04–S06 | S02 只说比较“无意”找最低；S03–S06 按作者主线给 iteration/step 的实际量。 | **S02 REWRITE；S03–S06 KEEP**。先澄清真实 claim 边界，再简短展开两个评价量；不另加复杂度块。 |
| S07→S08→S09→S10–S11 | 每轮平均时间 → 与轮数相乘 → fast-AGP 在两种仿真运行时间上较慢、迭代数较少 → 解释不能拿这些量直接判断逐步实时性。 | **核心链 KEEP；S10 REWRITE**。`simulation runtimes` 对 `online computation` 是时间量与过程的跨类比较；改成同类 metric 的区分，S11 的判据自然接上。 |
| S12→S13→S14 | 旧表混淆 → 具体更换列 → 宣告 accompanying text 修订。 | **S12/S14 REWRITE**：先沿用已定义的量，再报告可核的稿件动作；不能把“已有修订宣告”当成“相关 claim 已全稿处理”。 |
| S15→S16→S17→S18→S19 | 总括证据 → 原平台 GP 时值 → 另两任务 setup → Fig.1/2 panel locator/读数 → 10 ms 观察。 | **S15 REWRITE；其余 KEEP**。先区别原有实验与新增 cross-task evidence，再由不同条件引出各自图；Figure 不是必须作主语。 |
| S20→S21→S22→S23→S24→S25 | 选定参数值与 IL-SOGP 对照 → 20 ms 条件 → 全部设置图的观察 → 不利的逐步时间排序 → 限定已测场景归纳 → 明确无最低成本证据。 | **KEEP**。S20 较长但只承担“两项示例读数”一种任务；`respectively`、分号和条件使映射可恢复。S24/S25 属本 comment 确有需要的结束功能，不从 B4 推出通用 conclusion 规则。 |

### D. 逐句审计（C2-S01–S25）

| ID | 当前原句/唯一片段 | 句内核查与句间责任 | 判定 |
|---|---|---|---|
| C2-S01 | We sincerely thank the reviewer for pointing out the need to distinguish computational cost, learning convergence, and real-time feasibility. | we→thank；三层对象与此 comment 的复杂度、Table 轮数、实时性相符；长但只有承接任务。 | **KEEP** |
| C2-S02 | The comparison is not intended to identify the sparse GP method with the lowest computational cost. | comparison→is not intended；真实 claim/baseline 未入主句，仍是作者意图而非技术界定。 | **REWRITE** |
| C2-S03 | In this study, learning convergence and control-step online computation are evaluated separately. | 两对象→are evaluated；给后面两量的入口，下一句具体定义，术语未漂移。 | **KEEP** |
| C2-S04 | An ILC task proceeds through multiple iterations, and each iteration contains control steps and produces one `J_j`. | task/iteration→proceeds/contains/produces；层级关系同句可恢复，为 S05 轮数作前提。 | **KEEP** |
| C2-S05 | The 7 and 10 iterations required by fast-AGP and SOGP to reach `J_j<1.5` characterize learning convergence. | iteration numbers→characterize；threshold、方法、metric 与轮数紧邻，`Accordingly` 有真实承接。 | **KEEP** |
| C2-S06 | Real-time feasibility is instead evaluated by `t_comp^max`, with `t_comp^max<Δt` as the criterion. | feasibility→is evaluated；`instead` 转入另一层量；metric 全称、符号和判据同句。 | **KEEP** |
| C2-S07 | The 8.7617 s and 2.4688 s values cited in the comment are average runtimes of one complete 5-s simulation iteration. | values→are；两个数字的单位与每轮 5 s 条件明确；`cited in the comment` 只是定位来源，未扭曲量，非实质 blocker。 | **KEEP** |
| C2-S08 | Using per-iteration runtimes and iteration numbers gives estimated cumulative times 61.3319 s (`8.7617×7`) and 24.6880 s (`2.4688×10`). | calculation→gives；“estimated”限定乘法结果，方法与阈值前条件同句；信息密度服务单一计算。 | **KEEP** |
| C2-S09 | Under this setting, fast-AGP has longer per-iteration and estimated cumulative simulation runtimes than SOGP, although it reaches the threshold in fewer ILC iterations. | fast-AGP→has/reaches；不利 baseline 先报，`although` 标真实轮数差，条件前置。 | **KEEP** |
| C2-S10 | These simulation runtimes are different from per-control-step online computation. | runtimes→are different from computation；前者是测得时间，后者是过程，比较对象不平行。 | **REWRITE** |
| C2-S11 | Real-time feasibility is assessed by whether `t_comp^max<Δt`. | feasibility→is assessed；在 S07–S10 数值解释后回扣逐步判据，承担局部闭合。 | **KEEP** |
| C2-S12 | We agree that original Table I could conflate per-iteration simulation runtime, iteration-domain convergence, and per-step online computation. | we→agree；`iteration-domain convergence` 与 `per-step online computation` 是新的抽象标签且量/过程不平行。 | **REWRITE** |
| C2-S13 | We have replaced Table I's per-iteration runtime column with maximum online computation time per control step `t_comp^max` (ms). | we→have replaced；Table、原列、新列、单位明确；动作本身可读，真实性待 manuscript 核对。 | **KEEP** |
| C2-S14 | We have also revised the accompanying text to distinguish iteration-domain convergence from control-step online timing. | we→have revised；`accompanying text` 无位置、`iteration-domain`/`online timing` 漂移，未说明实际 claim 修订。 | **REWRITE** |
| C2-S15 | To evaluate the control-step criterion under different tasks and settings, comparisons have been conducted using the original robot experiment, Cases 1/2, and `W_x`/`S_e(t)` variations. | comparisons→have been conducted；一个动作合并原有平台与新增测试，读者难辨新旧证据职责。 | **REWRITE** |
| C2-S16 | In the original robot experiment, proposed `t_comp^max=9.90` ms at `Δt=20` ms, whereas standard GP gives 679.53 ms under the same conditions. | methods→give；原平台、GP baseline、metric/20 ms 条件同句；只支持此对照。 | **KEEP** |
| C2-S17 | Cases 1/2 use a simulated seven-DOF robot, different trajectories/contact environments, and outer-loop `Δt=10` ms. | Cases→use；不同任务条件与周期紧贴，承接原平台后的新场景。 | **KEEP** |
| C2-S18 | Figs. 1(d) and 2(d) give proposed `t_comp^max=4.75` and 4.65 ms, respectively. | Figures→give；panel、metric、Case 顺序清楚，locator 即实际数值读取。 | **KEEP** |
| C2-S19 | Both values satisfy `t_comp^max<Δt` in these benchmarks. | values→satisfy；`these benchmarks` 回指 S17 的 10 ms 条件，范围局部。 | **KEEP** |
| C2-S20 | At `W_x=200I`, Fig.3(f) gives 9.73/3.16 ms; at `S_e(t)=30(sin πt)^2I`, Fig.4(e) gives 6.85/2.50 ms for proposed/IL-SOGP. | 两条件各贴一图与两方法读数；分号分开独立示例，`respectively` 映射可恢复。 | **KEEP** |
| C2-S21 | The proposed method satisfies `t_comp^max<Δt` with `Δt=20` ms. | method→satisfies；接 S20 的两个设置，判据/周期就近，不外推。 | **KEEP** |
| C2-S22 | Complete comparisons in Figs.3/4 show the criterion also holds for all tested `W_x` and `S_e(t)` variations. | comparisons→show；由选值转向全部已测设置，`all tested` 有范围限定。 | **KEEP** |
| C2-S23 | Across Cases 1/2 and selected `W_x`/`S_e(t)` comparisons, the proposed method generally requires more per-step time than IL-SOGP. | method→requires；不利 baseline 结论保留，`generally` 不冒充所有场景逐点严格排序。 | **KEEP** |
| C2-S24 | Taken together, the results show `t_comp^max<Δt` in original robot experiment, Cases 1/2, and tested settings under respective periods. | results→show；仅合并已述证据，周期限定保留；connector 负责汇总。 | **KEEP** |
| C2-S25 | This evidence does not establish the lowest computational cost among sparse GP methods. | evidence→does not establish；限定能证明什么，回应 reviewer 的最低成本疑虑；不是从实验结果推出全面优势。 | **KEEP** |

**C2 非 KEEP 定点说明**

| ID | 原句功能 | 真实 blocker 与具体词层问题 | 下一步应实现的语义（不写替换句） |
|---|---|---|---|
| S02 REWRITE | 纠正最低成本前提。 | `The comparison` 指向不明，`is not intended to identify` 只表达意图，未直接陈述实际 claim 边界。 | 让实际 claim 范围及成本/实时性两个不同判断可核；保留“不声称 sparse GP 最低成本”的作者意图，不增设复杂度论证。 |
| S10 REWRITE | 从每轮/累计仿真运行时间切换到控制步实时性。 | `simulation runtimes` 与 `online computation` 不同类；这是量与过程的词义错配，非单纯同义词选择。 | 比较可同类识别的“每轮/累计仿真运行时间”和“每控制步最大在线计算时间”，再由 S11 给判据。 |
| S12 REWRITE | 承认 Table I 原呈现易混淆。 | `iteration-domain convergence`、`per-step online computation` 与前文正式 metric 的称谓不连续，且与 runtime 不是同类并列项。 | 用前文的迭代数/每轮仿真运行时间/每步最大在线时间及其角色说明表的具体混淆；不创造抽象中间标签。 |
| S14 REWRITE | 报告 accompanying manuscript text 修订。 | `accompanying text` 不可定位；`control-step online timing` 与 `t_comp^max` 换名；仍看不出被质疑的计算优势 claim 在何处受限。 | 核对修订稿后报告具体句子或段落的动作及位置/短摘录；只陈述实际已改的范围，全稿 claim 检查另列 gate。 |
| S15 REWRITE | 引入原平台与跨任务、跨设置时间证据。 | `comparisons have been conducted using` 将原有 robot experiment 和新增 Cases/设置并列成同一次新增动作，证据来历/任务分工不清；泛化的 `comparisons` 主语遮住具体对象。 | 区分已有原平台测量与新增跨任务/设置测试，各自携带对应 control period；自然进入 S16 原平台、S17–S19 新任务，再入 S20–S23 设置。 |

**范围记录**：reviewer 提到了 `O(L^3)` fast-AGP 与 `O(L^2)` SOGP；本轮不将“未单独讨论这两个复杂度”升级为必补 block 或 expression/scientific blocker。仍需用修订稿核对已宣告的 Table I 与相关 computational-cost/efficiency claim 的实际修订。

### E. C2 独立质量门槛与同作者感

- **Concern completeness**：按作者锁定的 C2 主线，Table 乘法、不利运行时间、控制步实时性、多任务/设置均已处理；不要求新增复杂度块。相关稿件 claim 修订的可查证据仍待核对，S25 的证据边界不能代替实际稿件动作；这属于独立核稿门槛。
- **Evidence→claim**：原平台 GP 的 `9.90/679.53` 只比较 proposed/standard GP；Cases/参数图的 IL-SOGP 数据只比较相应 scenario；不可把不同 baseline 拼成“普遍比 SOGP 便宜”。S09/S23 对 fast-AGP 较慢的结果必须保留。S24 只说已测场景满足各自控制周期，范围合适。
- **数学/版本一致性**：乘法与所报结果一致；`9.90<20`、`4.75,4.65<10`、`9.73,6.85<20` 均成立。当前 Response PDF 的 Fig.1–4 图号、panel 和可见图注与文中引用对应。原稿 Table I、新稿 Table I 与全文 claim 的实际版本未提供，因此 S13/S14 的“已修改”只能核对叙述清楚性，不能在本轮确证稿件事实。
- **语言与冗余**：S07 的 “values cited in the comment” 虽可更直接，但可唯一定位两数且不破坏推进，**KEEP**；S11 在数值解释后重述判据承担局部闭合，**KEEP**。S20 长而保持两组条件/数值的映射，不因句长单独判错。真正词层问题集中在 S02/S10/S12/S14/S15。
- **连续通读**：算术链与 Fig. locator→observation 很接近 TIE 的具体对象驱动写法；“一眼不像”的系统来源是入口仍以作者意图取代技术边界、Table 修订的抽象标签/泛称、以及证据来历被一句总括动词抹平。修这些点即可，后段的实测与不利比较不应为追求同作者感而删改。

## 3. Cross-response same-author verdict 与修改入口

| 层次 | Comment 1 | Comment 2 |
|---|---|---|
| 组织/节奏 | S12 在最小认知框架与原稿 baseline 解释后进入第二核心点，顺序成立；两组实验按 B4/A5 推进。 | Table 数值→不利结论→逐步证据的主体顺序符合作者主线。 |
| 主语/动词 | 证据部分由 cases、methods、results、figures、values 承担实际动作；入口的 `evaluation→is not intended` 与修订句 `we→have made` 太空。 | 时间链的 quantity→gives/has/satisfies 成立；入口、Table 修订与证据引入仍用模糊 intention/revised/conducted。 |
| 条件/baseline/术语 | 10/20 ms、`J_j`/`t_comp^max`、IL-SOGP/GP 区分总体稳定；不利时间结果保留。 | S12/S14 换抽象标签；GP 与 SOGP 的证据用途须保持分开。reviewer 提到的 `O(L^3)`/`O(L^2)` 不触发独立必补块。 |
| Figure/结论/location | Fig.1–4 均有 locator 后观察；S50 范围相称；revision location 缺。 | Fig.1–4 引用后有观测；S24/S25 各有功能；Table/claim revision location 缺。 |

**最终同作者感**：C1/C2 的实验与数值读取已使用 TIE 可验证的 action→setup→locator→observation、技术对象主语和连续术语；整体仍有 expression blocker，主要在两条入口的抽象意图表述及修订动作的不可核查表达。C1 的 S12 位置成立；C2 仍需明确原有与新增证据的来历。没有证据要求删编号、限制 `we`、让 Figure 必作主语、每图加数字、每段加 conclusion 或把 location 固定末尾。

**定点修改的输入已明确**：C1 为 3 REWRITE、无 MOVE；C2 为 5 REWRITE、无必补复杂度功能块。修改 Response 时须另外核对实际修订稿的 Table I、相关 claim 与可引用位置；本轮未获得这些稿件内容，不得把未核信息写成已完成事实。本轮没有改动 Response PDF/TeX 或任何知识库文件。

### 统计（仅计当前现有句子/ caption 标签）

| Comment | KEEP | REWRITE | MOVE | DELETE | MERGE | 合计 |
|---|---:|---:|---:|---:|---:|---:|
| C1 | 47 | 3 | 0 | 0 | 0 | 50 |
| C2 | 20 | 5 | 0 | 0 | 0 | 25 |

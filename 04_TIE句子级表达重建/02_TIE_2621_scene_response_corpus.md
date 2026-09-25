# 江 TIE_2621：场景级完整 response 原始证据库

## 0. 来源、计数与读法

- **唯一金标准**：`Response_TIE_江_No.17-TIE-2621.pdf`，21 个 PDF 页面。下文“PDF p.”指阅读器显示的物理页序；PDF 正文各 referee 分节另行从 1 编页，不能混同。英文引文只接合 PDF 换行断词，保留原有语法、编号和 claim。数学式必要时转写为等价的行内记号；精确符号以所指 PDF 页为准。
- **逐条清点**：Associate Editor 1 条（PDF p.2，编辑层总答复）；Referee 1 三条（p.3–4，图续 p.5–6）；Referee 2 六条（p.7–10）；Referee 3 两条（p.11–17）；Referee 4 七条（p.18–21）。R4 原文把 proofreading 和 Figure 1 两项都标作 `2.`，此处分别记 `R4-C2a`、`R4-C2b`。其中 R1-C1、R4-C1 只有认可及单句致谢，无实质论证；下面保留清点记录。**有实质分析价值的 reviewer-response scenes 共 16 个。**
- **证据等级**：`REPEATED/STABLE` = 跨多个独立 response 重复；`SAME-SCENE REPEATED` = 只在同类 scene 中重复；`SINGLE INSTANCE` = 当前只见一例；`SOURCE DEFECT` = 原文可观察但存在语法、论证强度、数字/图表或逻辑问题，不作可模仿表达。等级只对本 PDF 内证据有效。
- **分析单位**：每卡按原答复的先后顺序列功能链。引文旁的 S1/S2 等是**连续句**，后文逐句说明主语、核心动词、限定/基线、承接与下句动因；长篇 response 分段取连续句群，并完整交代其间未引句段的功能。所引 revised-manuscript 摘录仍属于该 response 的实际组成部分。

### 全量索引

| 原文条目 | PDF 页 | reviewer 的 concern / 答复状态 | 本库 |
|---|---:|---|---|
| AE-C1 | 2 | 要逐项回应审稿意见；编辑层概览，不计 reviewer scene | §1 |
| R1-C1 | 3 | 总体认可；仅 “Thanks for your recognition of our work.” | 清点，不计有效 scene |
| R1-C2 | 3–6 | 噪声/外扰未进入仿真评估 | S01 |
| R1-C3 | 4 | 摘要和 Eq. (1) 前错词 | S02 |
| R2-C1 | 7 | Jacobian 描述错误 | S03 |
| R2-C2 | 7–8 | D 的正定性和 Theorem 1 证明条件 | S04 |
| R2-C3 | 8–9 | Eq. (18) 错误、SVD 表示不明 | S05 |
| R2-C4 | 9 | Eq. (19) 首个等号缺推导 | S06 |
| R2-C5 | 9–10 | 零特征值时极限表达 | S07 |
| R2-C6 | 10 | Eq. (34) 后两步不等式缺推导 | S08 |
| R3-C1 | 11–12 | 对照 [20]，原创性不足 | S09 |
| R3-C2 | 12–17 | PID/自适应比较、优势证据和实验 | S10 |
| R4-C1 | 18 | 总体描述/认可；仅 “Thanks for your recognition of our work.” | 清点，不计有效 scene |
| R4-C2a | 18 | 语法和拼写校对 | S11 |
| R4-C2b | 18 | Figure 1 子系统输入/输出不明 | S12 |
| R4-C3 | 18–19 | 要真实装置实验 | S13 |
| R4-C4 | 19–20 | 编码器量化、测量延迟、脏微分的比较 | S14 |
| R4-C5 | 20 | 为何用所提自适应控制律 | S15 |
| R4-C6 | 20–21 | 不同识别算法的参数表 | S16 |

## 1. 编辑层边界：AE-C1（PDF p.2）

编辑要求准确逐项回复。作者先称已处理全部意见并标蓝，再依次概述比较/鲁棒性、理论推导、文献/novelty、真实机器人实验、英文校对，最后指向后面的逐点答复。这是全稿导航，不是某一 reviewer concern 的 evidence chain。其 “experiments have also been carried out and performed to shown” 与 “help us polishing” 均为 `SOURCE DEFECT`。该项已核对但不混入 16 个 reviewer scene 的重复次数。

## 2. Scene cards

### S01｜R1-C2：补 measurement noise / disturbance test（PDF pp.3–6）

**Reviewer situation / concern**：审稿人说原仿真未说明测量噪声和扰动，要求补入以便正确评价。作者把担忧落实为末端位置测量扰动对运动学参数估计的测试。

**完整组织**：致谢 → 承认测量噪声的实际关联（实质从 “We agree...” 开始）→ 宣布补外扰/噪声测试和 manuscript location → 再以测试目的开辟具体结果块 → 实际测量背景 → 白噪声设置、三个强度和公平参数 → Figs. 1–6：先展示扰动，再展示估计 → 读最大位置偏差与估计收敛 → “robustness” 结论 → 再报 Section IV, Page 7；附图在 PDF pp.4–6，文字答复在 p.4 结束。前一块给审稿人“已补”，后一块给可复核的 setup 与图证据；重复 location 是原文冗余。

**连续句 A（PDF p.3，回应到 setup）**：

> [S1] We agree that it is important to consider the measurement noises in the estimation, since the sensors data may subject to sensor noise in real applications. [S2] According to your suggestion, tests with external disturbances and noises are conducted and presented to substantiate the robustness of the proposed finite-time estimation algorithm in the revised manuscript. [S3] For your convenience, the detailed test results are given as follows, please refer to Section IV, Page 7 for more details. [S4] To further show the effectiveness of our proposed estimation algorithm, robustness tests are conducted by adding unknown external disturbances to the system model.

- S1：`We / agree` 直接承接担忧；`since` 后给真实传感器背景，尚无测试证据。S2 因此转到动作，`tests / are conducted and presented`，方法/条件放 `with external disturbances and noises`；此处由 concern 转向已做工作。
- S3：`test results / are given`，加 manuscript 位置；它为后面的详细结果开门，但 “are given ... please refer” 拼接了两个独立句。S4：`robustness tests / are conducted`，`by adding...` 给实际操作；和 S2 重复动作，下一句才解释为何对末端位置加扰动。

**连续句 B（PDF p.3，setup 到图）**：

> [S1] In some practical applications, uncertainties may inevitably exist in the measurement of end-effector position, e.g., the visual tracking system may be effected by environmental noises. [S2] Without loss of generality, in the comparative studies, we conduct the tests by adding white noises with different intensity to the measured end-effector position. [S3] The external disturbance is chosen to be d(t) = σw(t), where σ is the degree of intensity, and w(t) is the white Gaussian noise with the power of 1 dBW. [S4] For fair comparisons, the parameters in the adaptive estimation are chosen to be the same. [S5] The simulation results are depicted as shown in Figs. 2-5.

- S1：`uncertainties / may ... exist`，限定在末端位置测量；视觉系统例子把一般 concern 落到测试变量。S2：`we / conduct`，`by adding...` 交代操作，`to the measured end-effector position` 定测量通道。S3：`disturbance / is chosen`，紧随公式用 `where` 定义 σ 与 w(t)，延续 S2 的白噪声。S4：`parameters / are chosen`，独立说明比较公平条件。S5：`results / are depicted`，由 explanation/setup 转入 evidence locator；其 “Figs. 2-5” 与下文及附图 Figs. 1–6 不一致，属 `SOURCE DEFECT`。

**连续句 C（PDF pp.3–4，读图到结论）**：

> [S1] The disturbances added on the measured end-effector position are shown in Fig. 1, Fig. 3 and Fig. 5, with σ chosen to be σ = 0.005, σ = 0.01 and σ = 0.02. [S2] It can be observed from the figures that the maximum deviations added on the measured positions are about ±2 cm, ±4 cm and ±6 cm, respectively. [S3] The parameters estimation performance are shown in Fig.2, Fig.4 and Fig.6. [S4] We can see from the figures that, the parameters of three groups are observed with satisfactory convergence rate and accuracy, even in the presence of external disturbances. [S5] This has verified the robustness of the proposed estimation algorithm.

- S1：`disturbances / are shown`；σ 置于 `with` 尾部，对应奇数图。S2：形式主语 `It / can be observed`，真正观察是三个最大偏差，`respectively` 将数字回连三个 σ。S3：`performance / are shown`，切到偶数估计图，保持 “disturbance → estimation” 成对次序。S4：`We / can see`，从图读收敛表现，`even in...` 后置测试条件。S5：`This / has verified` 把观察升级为总体鲁棒性结论；仅凭有限噪声仿真过强。最后原文再用 “As suggested...” 交代 Section IV, Page 7。

**Language fingerprint / status**：技术对象 `tests/disturbance/parameters/results` 与 `we` 交替作主语；`conducted/chosen/shown/observed/verified` 推进。术语 `end-effector position`、`external disturbances`、`parameters` 连续重复，无同义词替换。`purpose → 操作 → 三强度 → 图 → 数字 → 收敛 → claim` 是此场景完整路径，属 `SINGLE INSTANCE`；图先定位再读值的链还见 S10、S13，属 `REPEATED/STABLE`。`sensors data may subject to`、`effected by`、`different intensity`、`parameters estimation performance are`、错误图号与笼统 “verified” 均为 `SOURCE DEFECT`。

### S02｜R1-C3：两个局部错词（PDF p.4）

**Reviewer situation / concern**：摘要 “existed” 用词和 Eq. (1) 前 “from/form” 错误。

**完整组织**：致谢 → 实质从 “these typos have been all corrected” 起，报告改正 → 扩至全文校对 → 蓝色标记与 Section I, Page 1 位置 → 停止；没有技术解释或图证据。

**原文连续全段**：

> [S1] Thanks for your helpful comments to improve our paper. [S2] According to your suggestion, these typos have been all corrected. [S3] We have carefully proof-read the paper and tried our best to correct similar typos in the manuscript. [S4] The modifications are highlighted in blue color and please refer to Section I, Page 1 for more details.

- S1：`[implicit we] / Thanks`，仅承接。S2：`typos / have been ... corrected`，指向 reviewer 所列对象；S3：`We / have proof-read, tried`，从两处修正扩到全稿；S4：`modifications / are highlighted`，随后主语隐含转为对 reviewer 的 `please refer`，以位置结束。S2–S4 都围绕完成动作，不需要实验链。

**Language fingerprint / status**：短答复、对象被动完成时、location 收尾；与 S03/S11/S12 同类重复，`SAME-SCENE REPEATED`。`have been all corrected`、`tried our best` 和 S4 连句不作风格范例，`SOURCE DEFECT`。

### S03｜R2-C1：Jacobian 描述不准确（PDF p.7）

**Reviewer situation / concern**：审稿人指出 Eq. (1) 后 “Taking the partial defferentation of (1) with respect to” 的说法不正确。

**完整组织**：致谢 → 实质从具体 “statement ... has been corrected and updated” 开始 → location → 给修订后的单句及公式 `ẋ = (∂f_kine(q)/∂q)q̇ = J(q,θ)q̇` → 在摘录处结束。答复文字短，证据就是替换句而非额外论证。

**连续句**：

> [S1] Thanks for your constructive comments to improve our paper. [S2] As suggested by the reviewer, the statement of robot Jacobian matrix has been corrected and updated in the revised manuscript. [S3] For your convenience, the revised text is listed as below. [S4] Please see Section II, Page 2 of the revised manuscript for details. [S5] Then, the relationship between the joint velocity q̇ and end-effector velocity ẋ can be obtained by taking the partial differentiation of f_kine(q) as [equation follows].

- S1：致谢。S2：`statement / has been corrected and updated`，把 reviewer 指出的措辞变成明确改动。S3：`text / is listed`，引出可直接核查的修订。S4：`[you] / Please see`，给位置。S5：`relationship / can be obtained`，并用 `by taking... of f_kine(q)` 替换被质疑的 “of (1)”；`as` 紧接公式。S3/S4 在修订句前，故 response 真正结束于公式，而不是 location。

**Language fingerprint / status**：`object + has been corrected` 与 S02/S05/S12 重复，`REPEATED/STABLE`；针对措辞错处直接给替换文本，在 S05、S07 也见，`SAME-SCENE REPEATED`。`corrected and updated` 重复、`listed as below` 生硬，`SOURCE DEFECT`。

### S04｜R2-C2：D 正定性和证明前提（PDF pp.7–8）

**Reviewer situation / concern**：审稿人质疑指数衰减积分不能确保 D 长时间正定，进而质疑 Theorem 1 中 `D > εI`；这属于**技术条件/证明有效性**，不能用改字句处理。

**完整组织**：致谢 → 先说明 PE 对误差收敛为何重要、在线核验为何难 → 实质命题从 “if the regressor vector Rf ... is PE, then ... D is positive definite” 开始 → 宣告 proof → 将 PE 的长度 T 窗口移到 `[t−T,t]` → 在窗口上给指数权重下界 → 将局部积分并入 `[0,t]` 的 D → 正定下界与 σ 结论 → 声明纳入 Section III, Page 4 → 粘贴 Remark 2 全文，结束。证明块不是礼貌回应的延长，而是逐步回答 reviewer 对全时积分的反例担忧。

**连续句 A（PDF p.7，条件进入证明）**：

> [S1] In the adaptive parameter estimation, the verification of persistence excitation (PE) condition is important, since the PE condition needs to be fulfilled to guarantee the error convergence. [S2] However, the online verification of PE condition is a non-trivial issue, especially for the nonlinear robot system. [S3] In this paper, the matrix D is introduced for the verification of PE condition, i.e., if the regressor vector Rf in equation (11) is PE, then the matrix D is positive definite, with λmin(D) > σ > 0. [S4] The proof is detailed as follows.

- S1：`verification / is important`，`since` 放收敛所需条件；S2：`verification / is` 重复 PE 一词并转到在线难点；S3：`matrix D / is introduced`，条件嵌入 `if Rf ... is PE, then D...`，正式答技术核心；S4：`proof / is detailed`，从 explanation 进入可检验的 deduction。这里没有讨论 reviewer 是否“误解”。

**连续推导 B（PDF pp.7–8；原文数学式按顺序摘记）**：

> [S1] From the definition of PE condition, we can obtain that ∫(t to t+T) Rfᵀ(τ)Rf(τ)dτ ≥ εI, which also can be expressed as ∫(t−T to t) Rfᵀ(τ)Rf(τ)dτ ≥ εI, for t > T > 0. [S2] Thus we can obtain that, if Rf satisfies the PE condition, the relationship ∫(t−T to t) Rfᵀ(τ)Rf(τ)dτ ≥ εI will hold for t > T > 0. [S3] Then, let us consider the integration interval τ ∈ [t − T, t]. [S4] Since t − τ ≤ T, we can obtain that e^(−ϑ(t−τ)) ≥ e^(−ϑT) > 0 according to the monotonicity of the exponential function. [S5] Then the following inequality can be derived: ∫(t−T to t) e^(−ϑ(t−τ))RfᵀRf dτ ≥ e^(−ϑT)∫(t−T to t) RfᵀRf dτ ≥ e^(−ϑT)εI.

- S1：`we / can obtain`，从 PE 定义给移动窗口；`for t>T>0` 后置适用范围。S2：`relationship / will hold`，重述 S1 的窗口下界；原文重复而非新增步骤。S3：`we / consider`，把下一步所需的 τ 区间提到句首。S4：`we / can obtain`，`Since t−τ≤T` 先给条件，再给权重下界。S5：`inequality / can be derived`，用刚得到的权重下界乘接 PE 窗口下界；由文字解释转入公式证明。

**收束（PDF p.8）**：原文接着写 `[0,t]` 的正权积分大于 `[t−T,t]` 部分，再给 `D > e^(−ϑT)εI`，然后：“This implies that D is positive definite and its minimum eigenvalue satisfies D(t) > σ with σ = e^(−ϑT)ε.” 随后报 “summarized as a remark ... Section III, Page 4” 并复贴 Remark 2。`This implies` 是从不等式到结论的转折；后面的长摘录仅重复正文论证。

**Language fingerprint / status**：技术对象 `PE condition / matrix D / integration interval / inequality` 主导；动词 `satisfies/hold/obtain/derive/implies`；同一符号持续使用。此类证明链在本 PDF 只有一例，`SINGLE INSTANCE`。与 S08 同属技术补推导，但 S08 直接贴式而无长篇条件铺垫，故不能把 S04 当通用长度。**数学/表述缺陷**：原文把 `λmin(D)>σ` 与 `D(t)>σ` 混写（后者矩阵与标量维度不清）；从左边包含右边到严格 `>` 需额外非零积分条件，单靠非负性通常只得 `≥`；证明要把 PE 作为前提，不能声称无条件正定；窗口重述及整段 Remark 重复；这些均为 `SOURCE DEFECT` 或至少需独立核验，不能迁移结论强度。

### S05｜R2-C3：Eq. (18) typo 与 SVD 表示条件（PDF pp.8–9）

**Reviewer situation / concern**：Eq. (18) 有 typo；审稿人追问为何可写 `Uc = Vc Ac Ycᵀ`，涉及 Vc/Yc 的关系。一个 comment 含“修字”和“补定义”两个工作。

**完整组织**：致谢 → 两个完成动作（改 typo；重写 Eq. (18) 前的叙述）→ 从 SVD 方法回答表示成立的来源 → 定义 Vc、Yc、Ac 和正交关系 → Section III, Page 5 → 贴修订正文，结束。实质在两个具体动作开始；技术解释紧接动作，因 reviewer 不只要求校对。

**连续句 A（PDF pp.8–9）**：

> [S1] According to your suggestions, the typos in equation (18) have been corrected. [S2] Additionally, the statement above (18) has been carefully rewritten and the presentation has been improved. [S3] Generally, the formula Uc = Vc Ac YcT can be obtained by using the singular-value-decomposition (SVD) method, which is widely employed in matrix operations. [S4] The Vc is an orthogonal matrix whose columns are eigenvectors of Uc UcT, Yc is an orthogonal matrix whose columns are eigenvectors of UcT Uc, and Ac is a diagonal matrix of the form Ac = diag{σ1, · · ·, σr}, with r = rank(Uc). [S5] Note that the matrix Vc and Yc are unitary matrices such that the relationships Vc VcT = I and Yc YcT = I hold.

- S1：`typos / have been corrected`，处理表面错误。S2：`statement / has been rewritten`，`Additionally` 转到真正的解释缺口。S3：`formula / can be obtained`，`by using SVD` 是理由，正式由 action 进入 technical explanation。S4：`Vc/Yc/Ac / is/are`，连续给三对象各自属性，`with r=...` 贴近对角矩阵定义。S5：`matrices / are`，补正交关系，因下一步贴正文需要这些条件。

**结束段（PDF p.9）**：原文再写 “the above analysis ... has been added in Section III, Page 5” 并贴 “Then, let us employ the SVD...” 的修订段。贴文与前段内容高度重复，但构成 response 的实际收尾。

**Language fingerprint / status**：改动句用 `typos/statement` 作主语；解释句用 `formula/Vc/Yc/Ac` 作主语，术语直接重复。`action → technical definition → location/excerpt` 与 S06/S07 同类，`SAME-SCENE REPEATED`；SVD 内容为 `SINGLE INSTANCE`。`the Vc`、`can be obtained by using` 的冗长、前段 Ac 的 `σ1...σr` 与贴文的 `a1...an` 不一致；`unitary` 与实矩阵的 `orthogonal` 混用、`VcVcᵀ=I` 是否适用于缩减 SVD 取决于矩阵尺寸，均标 `SOURCE DEFECT`，不能把数学定义视为已独立验证。

### S06｜R2-C4：补 Eq. (19) 首个等号推导（PDF p.9）

**Reviewer situation / concern**：审稿人要求把 Eq. (19) 第一个等号的来源写清。

**完整组织**：致谢 → 实质从宣布补推导及旧/新式号对应开始 → 给 Section III, Page 5 → 贴代数过程：`VcᵀVc=I`、左乘 `Vcᵀ`、得到 `VcᵀUc=AcYcᵀ`、把它带入 `QUc`、利用 Ac 对角性结束。这里正文短，主要空间留给公式。

**连续句与式链**：

> [S1] According to your suggestion, the derivation of equation (19) ((20) in the revised version) has been detailed formulated in the revised manuscript. [S2] For your convenience, the added text is listed as below, please refer to Section III, Page 5 for more details. [S3] Since Vc satisfies that VcT Vc = I, multiplying VcT on both sides of Uc = Vc Ac YcT, we can obtain that VcT Uc = Ac YcT. [S4] Then, multiplying Uc on both side of (19), we have [QUc = Yc(Ac+e^(−δt)ηI)^(−1)VcᵀUc = Yc(Ac+e^(−δt)ηI)^(−1)AcYcᵀ = Yc diag(a1/(a1+e^(−δt)η), …, an/(an+e^(−δt)η))Ycᵀ]. [S5] Note that in above derivations, the fact Ac is a diagonal matrix is used.

- S1：`derivation / has been ... formulated`，式号对应紧贴对象。S2：`text / is listed`，location 同句尾，下一句即贴推导。S3：`we / can obtain`，`Since` 先放正交条件，随后报告左乘结果。S4：`we / have`，`Then` 接 S3 的结果进入 `QUc`，式链使“为什么等号成立”可逐步跟踪。S5：`fact / is used`，指认末步对角化理由，在此结束。

**Language fingerprint / status**：`Since → Then → Note` 是本场景的推导串联；类似“补推导后直接贴公式”亦见 S08，`SAME-SCENE REPEATED`，具体代数过程 `SINGLE INSTANCE`。`has been detailed formulated`、`on both side`、逗号拼句为 `SOURCE DEFECT`；数学式需以 PDF 核对，不能从文字判定证明无误。

### S07｜R2-C5：零特征值的极限与 F(t) 定义（PDF pp.9–10）

**Reviewer situation / concern**：审稿人质疑 Eq. (22) 上方对零特征值 `aj` 的极限陈述。

**完整组织**：致谢 → 实质从“equation updated/typo corrected”开始 → 说明修改的不是单字，而是 F(t) 的定义及相应的零/非零特征值说法 → 给 Section III, Page 5 → 粘贴新 F(t)、`Q(t)Uc(t)=I−F(t)`、两个极限句，结束。答复比 R2-C2 短，因为争点是明确的局部公式和局部极限。

**连续句（PDF pp.9–10）**：

> [S1] According to your suggestion, the above mentioned equation has been updated and the typo has been corrected. [S2] In the revised version, the definition of F(t) is modified to [displayed diagonal formula] and the corresponding formulation is modified to “for the nonzero eigenvalue ai, the term e^(−δt)η/(ai+e^(−δt)η) would converge to zero when t → ∞, and for zero eigenvalue aj, lim e^(−δt)η/(aj+e^(−δt)η) = 1”. [S3] For your convenience, the modified text is listed below, and more details could be found in Section III, Page 5 of the revised manuscript.

- S1：`equation/typo / has been updated/corrected`，先报告动作。S2：`definition/formulation / is modified`，用同一动词并列两个互相关联对象，条件 `nonzero` 与 `zero` 紧贴对应特征值；这才直接回答“等于 1？”的疑问。S3：`text / is listed`，引出粘贴；摘录先定义 F(t)，再写 `Q(t)Uc(t)=I−F(t)`，最后写两类极限。动作、解释和位置都在这三句里，结尾是摘录内容。

**Language fingerprint / status**：术语 `F(t)/eigenvalue` 重复，未改称。局部修正 + 新公式 + 两类条件结果，为 `SINGLE INSTANCE`；短式答复模式与 S05/S06 属 `SAME-SCENE REPEATED`。原文 S2 数学排版交叠、`above mentioned` 生硬；极限适用还需 `η,δ` 等参数条件，不能脱离上下文迁移，`SOURCE DEFECT`/边界风险。

### S08｜R2-C6：Eq. (34) 后两项不等式（PDF p.10）

**Reviewer situation / concern**：审稿人明确要求最后两步不等式的详细推导。

**完整组织**：致谢 → 实质从宣布已补 derivation 及旧/新式号开始 → 给 revised text 和 Page 8 左栏位置 → 摘录先写 `FΦr=Φr−QBc`、`Bc=UcΦr`，再逐行展示 `L̇d` 的界，最后定义 `μd,ρd` 并连接紧集 Ω 与 `L̇d<0`；response 在长公式后结束。与 S06 一样，说明句短，因为 reviewer 要的是代数链本身。

**连续句与式链**：

> [S1] According to your suggestion, more details about the derivation of equation (34) ((35) in the revised version) have been added in the revised manuscript. [S2] For your convenience, the revised text is listed below, and please refer to Page 8, left column for more details. [S3] According to (22) and considering that FΦr = Φr − QBc, Bc = UcΦr, (34) can be rewritten as [displayed chain for L̇d: original expression → −||Φ̂r−QBc|| + ||FΦr|| − K2||es|| → −||Φ̃r|| − K2||es|| + 2||FΦr|| → −μd√Ld + ρd]. [S4] where μd = ... , ρd = 2||F||||Φr||. [S5] Since F and Φr are bounded and lim F = 0, there exists a compact set Ω ... such that ... L̇d < 0 ... .

- S1：`details / have been added`，式号括注给版本映射。S2：`text / is listed`，位置在公式前。S3：`(34) / can be rewritten`，`According to (22)` 和两个恒等式作前置依据；接下来主要由连续不等式承担论证，而非自然语言句。S4：`μd/ρd / [are defined]`，回填最后一行的新符号。S5：`there / exists`，在 `Since` 的有界及极限条件下，从式界过渡到紧集/负导数结论，在此收尾。

**Language fingerprint / status**：`action → location → premise → equation chain → symbol definitions → conclusion`，只在这个不等式场景完整出现，`SINGLE INSTANCE`；“补推导简短导语 + 公式承担主体”与 S06 为 `SAME-SCENE REPEATED`。S3 的多个 `≤` 步和 S5 引用 [32] 的适用条件，不能只凭 response 文本认作严谨证明；“last two inequality” 语法不佳、旧式号与修订式号交错，为 `SOURCE DEFECT`/核验点。

### S09｜R3-C1：originality 被 [20] 质疑（PDF pp.11–12）

**Reviewer situation / concern**：审稿人认为控制律已有 [20]，本文只加辅助滤波矩阵，原创性不足。作者回答实际贡献范围，而不是评判审稿人的理解。

**完整组织**：致谢 → 承认 [20] 已有自适应参数估计（实质从这句开始）→ 第一维：本文同时估计动力学和运动学参数；解释运动学不确定性、有限时间估计的需求，引用仿真/实验观察 → 第二维：Newton–Euler 对照 [20] 的 Lagrange，谈计算开销及高 DOF 适用 → 第三维：模型降阶/SVD 处理回归矩阵相关及 PE 问题、宣称估计精度 → 再致谢并交代 Section I, Page 2，结束。每一维先给与前作的具体区分，再补为什么重要；三段扩展很长。

**连续句 A（PDF p.11，previous work 到本文范围）**：

> [S1] As the reviewer pointed out, the adaptive estimation technique is important for robot manipulators to achieve better control performance and has been widely investigated in previous literatures, e.g., in [20], an adaptive parameters estimation method was designed to estimate the unknown robot dynamics by using the information of the estimation errors. [S2] Very different from the previous work, in this paper, we developed an adaptive parameter estimation algorithm for both the robot dynamic parameters and kinematic parameters. [S3] The kinematic uncertainties widely exist in robot control, for example, when a robot is equipped with different types of end-effectors or to grasp a tool with unknown length, these kinematic parameters will alter and lead to the unknown manipulator Jacobian matrix. [S4] Thus, it is desirable to achieve fast and accurate estimation of robot kinematic parameters. [S5] However, among the literatures about adaptive robot control, few studies have concerned with the estimation of robot kinematic parameters with finite-time (FT) convergence.

- S1：`technique / is ... investigated`，以 [20] 的已做工作作为 baseline；不否定已有估计。S2：`we / developed`，直接给本文差别，`both ... and ...` 把新范围放在句尾。S3：`uncertainties / exist`，用端执行器/工具长度解释为何运动学参数值得估。S4：`it / is desirable`，从场景推到快且准的需要。S5：`few studies / have concerned`，从需要转向 literature gap。之后原文写 FT 算法与仿真/实验表现，结束第一维。

**连续句 B（PDF pp.11–12，第二维）**：

> [S1] On the other hand, in this paper, the Newton-Euler (NE) dynamic model has been employed in dynamic parameters identification to improve the computational efficiency. [S2] In the literature [20], the estimation algorithm is based on a conventional Lagrange dynamics model, which requires explicit mathematical form of the dynamics and is cost expensive in calculation. [S3] In addition, the amount of calculation of Lagrange model will increase significantly with the increase of the DOFs and this may lead to the problem called ‘curse of dimensionality’. [S4] Hence, Lagrange model has been merely used for identification of a high DOF robot, such as Baxter with 7 DOFs of each arm. [S5] In comparison to the Lagrange model, the NE model is of more computational efficiency.

- S1：`NE model / has been employed`，`On the other hand` 开第二贡献维度。S2：`algorithm [20] / is based`，紧邻 Lagrange baseline；S3：`amount of calculation / will increase`，解释 baseline 的代价；S4：`Lagrange model / has been ... used`，试图举高 DOF 例子，但 `merely used` 与论点可能相反；S5：`NE model / is`，回到比较主张。下一句以 O(N) 作支持，再以 `Therefore` 收束效率与实时性。

**连续句 C（PDF p.12，第三维）**：

> [S1] Another contribution to be highlighted is the improved accuracy of the estimated parameters by using the model reduction method. [S2] It is well known that, persistence excitation (PE) condition should be satisfied to fulfill the convergence of the estimated parameters. [S3] However, the conventional NE dynamic model may not be able to guarantee the PE condition, due to the restriction of the robot mechanism and lack of sensors information. [S4] For example, in the NE regressor of Baxter robot, some columns of the matrix may be linear dependent of others, and thus the matrix RfT Rf in the PE condition may not be full rank. [S5] As a result, the PE condition would not be satisfied and the estimated parameters may not converge to their real values.

- S1：`contribution / is`，明确第三维。S2：`PE condition / should be satisfied`，先给理论要求；S3：`NE model / may not ... guarantee`，由要求切回本文模型的障碍；S4：`columns / may be ... dependent`，给 Baxter regressor 具体例子；S5：`PE condition / would not ... be satisfied`，说明这种相关性的后果。下一句 “To remedy...” 引出 SVD 降阶，后接估计结果和 Section I, Page 2。`PE condition` 与 `estimated parameters` 持续复现，不改称。

**Language fingerprint / status**：三段分别用 `Very different... / On the other hand / Another contribution` 起头；`previous work → 本文范围 → 动机/障碍 → 贡献` 的顺序只在本 novelty 争议出现，`SINGLE INSTANCE`。与 S15 共享“既有自适应法 → 本文有限时间方案”的部分内容，相关内容重复但不能据此称通用 novelty 写法，最多 `SAME-SCENE REPEATED` 于方法动机类。**SOURCE DEFECT**：开头及多处超长句；`Very different` 生硬；`few studies`、计算复杂度及 “PE condition can be fulfilled” 缺充分比较/条件；`curse of dimensionality` 与 `Lagrange ... merely used` 强/疑似反向；`fast and accurate convenience`、`effect` 等语法搭配；第三维把降阶直接推到 PE 成立属逻辑跳跃。不得将三段长度或 claim 强度提升成风格规则。

### S10｜R3-C2：PID / MBAC 比较、参数表与实验要求（PDF pp.12–17）

**Reviewer situation / concern**：原稿仅对 PD 比较；审稿人要 PID、[20] 自适应控制器的 tracking 对照、明确优势，并指出实验会提高质量。这是多子任务的综合 evidence request。

**完整组织**：致谢 → **先给 rationale**：所提有限时间估计的目标，承认 PID 应用，再解释未知动力学和传统 MBAC 的暂态局限 → 概述本文 estimation law 的目的和有限时间 claim → **第二段** NE/Lagrange 的计算比较与 SVD 降阶/PE 解释 → **第三段才报已新增** PID 与 MBAC [16] 比较、与 [20] 动态参数对比表及实验（实质证据动作明确出现于此）→ 引出 revised text → **图证据**：Figs. 7–13 七关节轨迹，Fig. 14 RMSE；先承认三者稳定跟踪，接着读 PID 偏差、MBAC 稳态/暂态，再读 FT RMSE → **表证据**：参数真值、所提估计、adaptive [27]，概括估计精度 → Section IV, Page 8 结束。原文只有一句声称实验也已做，实际随后详写的是仿真比较和参数表；真实机器人实验的细节由 S13 给出。

**连续句 A（PDF pp.12–13，rationale）**：

> [S1] In this paper, we proposed a finite time parameters estimation scheme to identify the kinematic and dynamic parameters of the robots with enhanced convergence rate and accuracy. [S2] The conventional PID control methods have achieved great success in robot manipulators control. [S3] However, satisfactory control performance may not be obtained using the PID control because the unknown robot dynamics act as a prominent external disturbance and may lead to degradation of the control performance or even incur instability. [S4] Model based adaptive control (MBAC) has been thus introduced to handle the effect of the uncertain robot dynamics. [S5] For most of MBAC based robot systems, however, gradient decent based adaptive laws were designed to minimize the tracking errors and parameters prediction errors.

- S1：`we / proposed`，先放本文目标。S2：`PID methods / have achieved`，给 reviewer 要求的 baseline 合理地位；S3：`performance / may not be obtained`，`because` 指明未知动力学造成的限制；S4：`MBAC / has been introduced`，顺着这个限制引入第二 baseline；S5：`adaptive laws / were designed`，开始解释 MBAC 的误差驱动方式。下一句从稳态成功转到暂态问题，再引出本文 leakage term。

**连续句 B（PDF p.13，从 rationale 转到新增 evidence）**：

> [S1] According to your suggestion, comparisons have been conducted based on the PID control and a MBAC [16] in the revised manuscript. [S2] Additionally, the dynamic parameters estimated using the proposed algorithm and adaptive method in [20] have also been detailed performed in Table III, to show the performance of the proposed estimation algorithm. [S3] Moreover, experiment results of the estimation have also been conducted and performed in Section IV, Page 7 of the revised version. [S4] For your convenience, the comparisons results are depicted as below. [S5] To further verity the effectiveness of proposed algorithm, comparison studies have been carried out based on a PID controller and a model based adaptive controller (MBAC) [16].

- S1：`comparisons / have been conducted`，正式答 PID/MBAC 的 action，baseline 紧跟 `based on`。S2：`parameters / have ... performed`，用 `Additionally` 转向表格识别对照，实为不自然主谓搭配；S3：`results / have ... conducted`，`Moreover` 报实验但不提供该实验 setup。S4：`results / are depicted`，准备进入图表。S5：`comparison studies / have been carried out`，重新起 revised-text 段，重复 S1；下一句才给 Figs. 7–14。

**连续句 C（PDF pp.13, 17，图的读取跨图页继续）**：

> [S1] The comparison results are depicted in Figs.7-14. [S2] As seen from the figures, although the stable tracking can be obtained by using all three types of controller, the tracking errors of the PID control (dashed-dotted line ‘−.’) are relatively large, since the PID controller is seriously effected by the robot dynamics such as inertial and Coriolis torque. [S3] The MBAC controller has achieved well steady-state tracking performance (dashed line ‘−−’) after a period time of adaptation, but the performance of transient state is much lower than the proposed FT method. [S4] Fig. 14 show the profile of the root mean square error (RMSE) of tracking error of the 7 joint. [S5] We can see clearly from the figure that, both steady state and transient errors are improved than the other twos, which have show the effectiveness of the proposed controller.

- S1：`results / are depicted`，由 setup 进入 Figure locator。S2：`tracking/errors / can be obtained/are`，`although` 先承认三者可稳定跟踪，转而读 PID 与模型动力学相关的误差；线型括注贴近 PID。S3：`MBAC controller / has achieved`，先给稳态可取处，`but` 转暂态，与 FT 比较；`steady-state/transient` 延续 S2 的 tracking 维度。S4：`Fig.14 / show`，从轨迹切换 RMSE 指标。S5：`We / can see`，由 observation 升到 effectiveness 结论；主张强于图上直接可见内容。

**连续句 D（PDF p.17，表的读取）**：

> [S1] Comparisons of the parameters estimation performance have also been carried out based on our proposed FT estimated algorithm and the adaptive estimation method in [27]. [S2] The detailed of the estimated parameters are shown in Table III, where the real value of the dynamic parameters, the parameters estimated by using our proposed finite-time algorithm and adaptive estimation method in [27] have been presented, respectively. [S3] We can see from the Table III that, the parameters estimated by using our proposed method is close to the real dynamic parameters, and has more estimation accuracy than conventional adaptive estimation method. [S4] As suggested, the above discussions have been presented in Section IV, Page 8 of the revised manuscript.

- S1：`Comparisons / have been carried out`，从 tracking 图切到 parameter estimation baseline [27]。S2：`details / are shown`，`where` 解释表的三组列；S3：`We / can see`，从表列到“接近真值”观察，再到精度比较，未逐行量化；S4：`discussions / have been presented`，用具体 location 结束。`parameters estimation`、`estimated parameters` 被反复使用。

**Language fingerprint / status**：本 scene 罕见地含多个 baseline 与两个 evidence 形态；`rationale → comparison action → figures → contrastive reading → Table → summary → location` 仅此一例，`SINGLE INSTANCE`。图表定位后读取结果在 S01/S13/S16 重复，`REPEATED/STABLE`；表的 `where` 解释列在 S16 几乎重复，`SAME-SCENE REPEATED`。**SOURCE DEFECT**：`verity`、`gradient decent`、`detailed performed`、`conducted and performed`、`effected`、`improved than` 等；[20] 在 action 句变成 [27] 于表段，MBAC 是 [16]，三者不能混称；正文 `Table III`、本 response 附表 `Table 1` 不一致；Fig. 14 图例有 `MARC` 而正文称 `MBAC`；声称更高精度但附表第 1、10、14、21 等行并非所提方法更接近真值，故总体比较不得无条件搬用。正文没有在本 scene 内展开新实验的 platform、task、测量条件，这是 coverage gap，不能把 “experiment results ... conducted” 当充分实验证据。

### S11｜R4-C2a：proofreading（PDF p.18；原文第一个 C2）

**Reviewer situation / concern**：全文多处语法错误和 typo，需要校对。

**完整组织**：致谢 → 实质从“已通读校对并修正”开始 → 邀请英语母语者协助 → 蓝色标记供查，结束；无单个段落 excerpt 或技术论证。

**连续全段**：

> [S1] The authors sincerely thank the reviewer for the helpful comment. [S2] According to your suggestion, we have carefully proof-read the paper and tried our best to correct typos and grammar errors in the manuscript. [S3] In addition, we have also invited a native English-speaker to help us polishing this paper. [S4] For your convenience, the modifications are highlighted in blue color in the revised manuscript.

- S1：`authors / thank`。S2：`we / have proof-read, tried`，把校对要求变成完成动作；S3：`we / have invited`，`In addition` 给第二种实施方式；S4：`modifications / are highlighted`，以定位方式结束。短答无 evidence-reading，因为 reviewer 只要求校对。

**Language fingerprint / status**：行动 + 可查标记，与 S02 proofreading `SAME-SCENE REPEATED`。`tried our best`、`help us polishing` 及 PDF 本身尚存错误，为 `SOURCE DEFECT`；这张卡只记录作者怎么答，不证明校对质量。

### S12｜R4-C2b：Figure 1 输入输出不清（PDF p.18；原文第二个 C2）

**Reviewer situation / concern**：Figure 1 没交代各子系统输入与输出。

**完整组织**：致谢 → 实质从 Figure 1 已修改开始 → Section II, Page 3 → 结束。它比 S03 更短：原 response 不给修改后的图、也未逐一写输入输出，所以证据只到“报告动作”的层级。

**连续全段**：

> [S1] Thanks for your constructive comments to improve our paper. [S2] As suggested by the reviewer, Figure 1 has been modified and updated in the revised manuscript. [S3] Please refer to Section II, Page 3 for more details.

- S1：致谢。S2：`Figure 1 / has been modified and updated`，直接答图改动；S3：`[you] / refer`，位置收尾。没有下一句解释图中如何清晰化，不能替作者补造。

**Language fingerprint / status**：小范围对象 + 完成动作 + location，与 S02/S03 同类，`SAME-SCENE REPEATED`；具体输入/输出说明缺席为此 scene 的 `SINGLE INSTANCE` 边界。`modified and updated` 重复，`SOURCE DEFECT`。

### S13｜R4-C3：真实 Baxter 实验（PDF pp.18–19）

**Reviewer situation / concern**：审稿人认为仿真不足，希望真实机构的实时实验；作者使用 Baxter 左臂，而非审稿人举的二自由度机构。

**完整组织**：致谢 → 实质从“实验已在 Baxter 进行”开始 → 先报 Section IV, Page 7 并引入摘录 → 真实左臂平台与 Fig.3 → 正弦/余弦跟踪任务与 Fig.14 → Fig.15 估计结果 → 与 nominal/dashed line 比较 → robustness 结论；随后附 Figure 15、Figure 16（PDF p.19），response 结束。实验段较短，因只展示一个平台、一个任务和一幅估计图，没有 S10 的多 baseline 对比。

**连续句（PDF pp.18–19）**：

> [S1] In addition, experiments have been further performed based on the left robotic arm of a real Baxter robot, as shown in Fig.3. [S2] In the experiment, the robot is commanded to track a set of sinusoidal and cosine trajectories depicted in Fig.14. [S3] The estimation results are shown in Fig.15. [S4] We can see from the figure that, most of the estimated parameters are close to the nominal values (dashed line) with satisfactory convergence performance. [S5] In terms of the above test results, the robustness of the proposed estimation algorithm can be verified.

- S1：`experiments / have been performed`，`based on...left robotic arm` 给平台，Fig.3 指机器人。S2：`robot / is commanded to track`，任务自然跟在平台后；`depicted in Fig.14` 给轨迹定位。S3：`results / are shown`，转入 evidence。S4：`We / can see`，读 Fig.15，并在 `nominal values (dashed line)` 处放视觉 baseline；“most” 保留部分非一致结果。S5：`robustness / can be verified`，由观察转 conclusion，但一组机器人实验并不足以一般验证鲁棒性。

**Language fingerprint / status**：`platform → task → result figure → observation → claim` 为 `SINGLE INSTANCE`；图后读值的顺序跨 S01/S10 重复，`REPEATED/STABLE`。**SOURCE DEFECT**：原摘录的 Fig.14/15 与随附图标 Figure 16/15 的轨迹/估计对应关系不一致，且正文的机器人 Fig.3 未随附；`experiments ... performed` 冗余；“robustness verified” 超出这里仅对 nominal convergence 的观察。原文未给采样率、延迟或可复核误差数字，不能替它补充。

### S14｜R4-C4：量化、延迟与 dirty derivative 的 robustness concern（PDF pp.19–20）

**Reviewer situation / concern**：审稿人要求考虑 encoder/camera 量化、输出测量延迟、脏微分速度估计，并提供相关文献。作者答的是文献讨论 + 外扰鲁棒性测试，**没有逐项直接测试量化/延迟/脏微分**。

**完整组织**：致谢 → 实质从“相关识别研究已在引言讨论引用”开始 → Section I, Page 1 → `Additionally` 切至系统模型外扰测试 → 一句概括收敛观察 → Section IV, Page 7 结束。与 S01 相关但此处不重复其 setup/图；因此这是“引用回应 + 相关替代性鲁棒性证据”，不是完整满足三项技术要求的实验。

**连续句（PDF pp.19–20）**：

> [S1] According to your suggestion, the above mentioned state-of-the-art studies of robot identifications have been discussed and cited in the introduction part of the revised manuscript. [S2] Please refer to Section I, Page 1 for more details. [S3] Additionally, to further show the effectiveness of our proposed estimation algorithm, robustness tests are conducted by adding unknown external disturbances to the robot system model. [S4] The test results show that the estimated parameters are observed with satisfactory convergence rate and accuracy, even in the presence of external disturbances. [S5] The details about robustness tests could be found in Section IV, Page 7 in the revised manuscript.

- S1：`studies / have been discussed and cited`，先回应给定文献；S2：`[you] / refer`，为这个子任务给位置。S3：`tests / are conducted`，`Additionally` 切第二块，`by adding...` 指实际测试扰动；S4：`results / show`，`even in...` 仅限定一般外扰条件；S5：`details / could be found`，给另一个位置并结束。三项指定非理想因素没有任何句子直接承担。

**Language fingerprint / status**：一个 comment 拆成两个 action/location 块，`SINGLE INSTANCE`；外扰句几乎重复 S01，属 `SAME-SCENE REPEATED` 的内容复用。**SOURCE DEFECT**：外扰和 sensor quantization、delay、dirty derivatives 不是等价测试，故 response 存在 concern-coverage gap；`state-of-the-art`、`robot identifications` 搭配不佳；概括 “robustness” 也不能覆盖审稿人列的因素。

### S15｜R4-C5：为何选此自适应控制律（PDF p.20）

**Reviewer situation / concern**：已有许多表现可接受的 adaptive controller；审稿人要求选择本文控制律的理由。这是方法动机/相对优势询问，未要求新增数据。

**完整组织**：致谢 → 实质从“adaptive control 的在线学习能力”背景开始 → 现有 gradient-descent law 及 tracking/observer error 耦合 → 这种耦合可能拖慢参数收敛 → 本文 leakage-term、由估计误差驱动的有限时间方案 → 与传统 gradient law 的概括比较 → 在比较性结论处直接结束；**无 manuscript location、Figure、Table**。它与 S09/S10 的部分 rationale 重复，但没有重贴实验。

**连续句（PDF p.20）**：

> [S1] In the past decades, adaptive control has been well investigated because of its online learning ability to update control parameters and to handle model uncertainties, e.g., in the model based control, it has been successfully employed to estimate the unknown parameters. [S2] In most exiting reference, however, the adaptive laws are designed to minimize the error of tracking control based on the gradient descent method. [S3] From this point of view, the parameter estimation convergence speed of gradient based adaptive laws could be regarded a function of the observer error and control error, which create strong couplings. [S4] This implies that the convergence of the estimated parameters may be effected by the system tracking errors. [S5] To improve the estimation performance, in this paper, we design a finite time adaptive estimation scheme with a leakage term driven by parameter estimation errors, such that precise and fast estimation of robotic parameters can be retained by using the information estimation error.

- S1：`adaptive control / has been investigated`，`because` 给广泛采用的原因，不急于否定其他方法。S2：`adaptive laws / are designed`，`however` 转到本文要解决的现有做法。S3：`convergence speed / could be regarded`，把 gradient law 与两种 error 耦合；S4：`This / implies`，将耦合解释为跟踪误差可能影响参数收敛。S5：`we / design`，`To improve...` 用 S4 的限制引出本文方案，`with a leakage term...` 紧贴方案构成。原文最后一句以 “Comparing with traditional gradient descent based adaptive method...” 直接宣称 finite-time identification 和 better control performance，没有再给证据或 location。

**Language fingerprint / status**：背景 → 现有法作用/限制 → 本文设计 → 概括优势，`SINGLE INSTANCE` 的完整 motivation chain；前作/gradient 的事实与 S09/S10 部分重复，属 `SAME-SCENE REPEATED`。`adaptive laws / estimated parameters / tracking errors` 反复出现。**SOURCE DEFECT**：`exiting reference`、`effected`、`can be retained`、`information estimation error` 等错误/含混；`can guarantee ... better control performance` 未由本 response 内证据支持，且控制律和估计律在答复中时有混称。

### S16｜R4-C6：不同识别算法的参数表（PDF pp.20–21）

**Reviewer situation / concern**：要求以表格列出不同 identification algorithms 估得的参数。这是明确的 table/data presentation request，不是重新论证完整控制方案。

**完整组织**：致谢 → 实质从“比较研究已做并呈现”开始 → 说明表含真值、所提 FT 和 adaptive 三列 → 给 Section V, Page 8 → 粘贴比较段：方法、Table III、按表作总体观察 → 附 Table 2（43 行参数数值）→ 最后一条比较句跨页续完，在 PDF p.21 结束。表是 response 的主要证据对象，答复未逐行解读 43 个值。

**连续句 A（PDF p.20，action/location）**：

> [S1] According to your suggestion, comparative studies by using different estimation methods have been carried out and presented in the revised manuscript. [S2] The detailed of the estimated parameters are shown in Table II, where the real values of the dynamic parameters, the parameters estimated by using our proposed finite-time algorithm and the adaptive estimation method have been presented, respectively. [S3] For your convenience, the added text is listed as below, please refer to Section V, Page 8 for details.

- S1：`studies / have been carried out and presented`，由要求转成完成动作。S2：`details / are shown`，`where` 说明三组比较列，正面回答表的内容；S3：`text / is listed`，给位置并引入摘录。S2 的 `Table II`、S3 的 `Section V` 与其后摘录并不一致。

**连续句 B（PDF pp.20–21，表进入 observation）**：

> [S1] Comparisons of the parameters estimation performance have also been carried out based on our proposed FT estimated algorithm and the adaptive estimation method in [27]. [S2] The detailed of the estimated parameters are shown in Table III, where the real value of the dynamic parameters, the parameters estimated by using our proposed finite-time algorithm and adaptive estimation method in [27] have been presented, respectively. [S3] We can see from the Table III that, the parameters estimated by using our proposed method are close to the real dynamic parameters, and has more estimation accuracy than conventional adaptive estimation method.

- S1：`Comparisons / have been carried out`，baseline [27] 靠近比较动作。S2：`details / are shown`，又用 `where` 解释三列；`Table III` 指 manuscript 编号。S3：`We / can see`，从表过渡到总体精度判断。S1–S3 与 S10 的参数段近乎同文；其间插入附表 Table 2，显示作者依赖大表而不是逐项数值阅读。

**Language fingerprint / status**：`action → Table locator + where 列说明 → observation` 在 S10/S16 重复，`SAME-SCENE REPEATED`，但两处复用同一比较材料，不能算完全独立实验。`Table` 介词定位与 `We can see from...` 的连续用法还见 S10，属于本 PDF 的 `REPEATED/STABLE` 表达机制。**SOURCE DEFECT**：同一答复先 `Table II` 后 `Table III`，PDF 附表标 `Table 2`；Section V 与 S10 对该比较的 Section IV, Page 8 冲突；第 1、10、14、21 等行的所提值并非比 adaptive 值更接近真值，总体 “more estimation accuracy” 无限定；`The detailed of...`、`has more estimation accuracy` 语法不妥。

## 3. 跨 scene 的证据状态索引（仅记录本 PDF 的可观察事实）

| 观察 | 具体 scene / PDF 页 | 状态与边界 |
|---|---|---|
| 致谢之后很快进入具体 concern 或已做动作；局部小问题通常在动作/位置/修订摘录后停下 | S02–S08、S11–S12、S16；pp.4, 7–10, 18, 20 | `REPEATED/STABLE`；S04/S09/S10 的实质问题明显更长，不能统一成短模板。 |
| manuscript 对象作主语、完成时被动报告修订 | S02 `typos`、S03 `statement`、S05 `statement`、S06 `derivation`、S12 `Figure 1`；pp.4, 7–9, 18 | `REPEATED/STABLE`；`corrected and updated` 等重叠动词是 `SOURCE DEFECT`。 |
| 先报 revised location，再贴修订文字/公式；location 不总是最后一句 | S03、S06–S08、S13、S16；pp.7, 9–10, 18–21 | `REPEATED/STABLE` 的是具体位置可查；“location 一定最后收尾”与原文不符。 |
| 用技术对象与明确条件承接数学争议，再进入证明 | S04；pp.7–8 | `SINGLE INSTANCE`；`D` 正定结论必须保留 PE 条件，严格不等号另需核验。 |
| 局部 equation/definition 问题采用“完成动作 + 简短解释/公式 + 修订位置或摘录” | S05–S08；pp.8–10 | `SAME-SCENE REPEATED`；每条长度由所需公式决定，S05 有定义，S06/S08 重推导，S07 改极限。 |
| purpose 或具体操作进入新 test/comparison，再给 setting/baseline | S01、S10、S13、S14；pp.3, 12–13, 18–20 | `REPEATED/STABLE` 的是“先指出做了什么，再交代条件”；“每个实验句都以 To further... 起头”不成立（S13 用 In addition）。 |
| Figure/Table 作为 locator，紧接读图/读表 | S01、S10、S13、S16；pp.3–4, 13/17, 18–19, 20–21 | `REPEATED/STABLE`；数值化读图（S01 的 ±2/4/6 cm）是 `SINGLE INSTANCE`，其他多为定性。 |
| 结果先承认 baseline 的可取处再给差异 | S10 PID/MBAC 图段、S09 NE/Lagrange 段；pp.11–13/17 | `SAME-SCENE REPEATED` 于比较场景；比较对象/维度有时不对称，相关句标 `SOURCE DEFECT`。 |
| 大表说明真值与两种估计结果，再只给总体判断 | S10、S16；pp.17, 20–21 | `SAME-SCENE REPEATED`；两处几乎复用同文与同表，不可当独立验证。 |
| 有限测试后直接说 effectiveness/robustness “verified” 或保证一般优势 | S01、S10、S13–S15；pp.4, 17–20 | 重复出现的**源缺陷**，`SOURCE DEFECT`；出现频率不使过强结论变成有效写法。 |

## 4. 与既有 `00_TIE_2621_sentence_realization基准.md` 的只读冲突核对

此节区分实际范围冲突与基准尚未列出的源缺陷；不改动基准文件，也不以它决定本库取样。

1. `00` §2“新增 experiment/comparison 与 setup”及 §6 总体判定把“实验句稳定使用 purpose fronting 后进入 conducted/carried out + by/based on”写成跨 scene 机制；**S13/R4-C3，PDF p.18** 的实际 experiment excerpt 用 “In addition, experiments have been further performed based on...” 起首，随后平台 → 任务；没有 purpose-fronting。S01、S10 有 purpose-fronting，不能说所有实验句稳定如此。
2. **遗漏，非冲突**：`00` §1 #9 和 §4 虽指出部分编号不一致，但未覆盖 **S01/R1-C2，PDF p.3**：“The simulation results are depicted as shown in Figs. 2-5” 与随后的 Figs. 1–6。`00` §1 #12 已把 R4-C3 的笼统 robustness 结论标为过强，本库进一步记录其证据只涉及 nominal convergence。

除此之外，本轮未发现 `00` 所引英文句子有可确认的逐字误引；对其“稳定”判定仍须按本库 scene 边界使用，不能作为最终写作规则。

## 5. 覆盖边界

- 16/16 个实质 reviewer response 均有 card；两条单句认可（R1-C1、R4-C1）和 AE-C1 已清点。每张 card 均含 PDF 页、真实 concern、完整功能顺序、连续句段、句间推进与 evidence status。
- 原 PDF 自身没有提供 R4-C4 三种指定非理想因素的逐项测试，也没有给 S10 所称真实实验的完整 setup；这属于**原文答复的证据缺口**，不是本轮未读页。图表编号、表内反例和推导条件已作为源缺陷保留，不代为修正。
- 本文件只记录原始 response 的场景实现与可核验边界；不生成通用模板，不据此修改其他文件。

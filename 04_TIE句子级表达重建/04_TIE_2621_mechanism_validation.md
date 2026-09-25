# TIE_2621 mechanism validation：冻结预测与揭示核对

## 0. Validation protocol 与可盲性边界

本文件验证 `03_TIE_2621_response_mechanism_candidates.md` 的 A1–A6、B1–B6。依据是 `02_TIE_2621_scene_response_corpus.md` 的 S01–S16；必要时回查 21 页 PDF。`00_TIE_2621_sentence_realization基准.md` 只读，不供预测。PDF 页码为物理页。

**诚实边界**：同一分析者已经参与前两轮，历史上看过全部 scene；因此这里不能声称“对分析者本人完全盲”。为防止本轮的伪盲测，采用可审查的**先冻结、后揭示**：先只用已知 reviewer-comment 清单和去掉目标后的其他 scene 支持，写入下表的六层预测；在此文件首次写入以前，本轮不重新打开目标 scene 的 response/card。随后才读取 02 中的 held-out card 并与 PDF 必要页核对，在后续章节追加 revealed actual。下表在揭示后不回改。历史暴露这一限制会影响“严格独立预测”的解释；验证结论将对此从严，尤其不把 target 自己对 03 候选的贡献冒充 remaining evidence。

每一折先按 comment 判 situation，再预测 entry、功能块、句间状态、language（subject/verb、条件/基线、Figure/Table、术语与 location）、stop。预测的是**语义结构，不是原句**。一个机制至少两折；对双实例 B2/B3/B4/B5 做双向排除。`remaining` 栏只列**非目标**独立 scene，S10/S16 的同表材料、S01/S14 的同扰动材料均不算两个独立实验/表。若去除目标后没有独立依据，直接判 `INSUFFICIENT INDEPENDENT EVIDENCE`，不伪造预测通过。

匹配判定：`M` = 必要核心状态命中；`V` = 情形特有变体；`D` = 原文 source defect 导致偏离；`X` = 机制自身预测错误；`W` = 无害表面措辞差异。只有 `X` 才是直接机制 blocker；但若机制把 `D` 当成必然的优良 realization，也不能 PASS。最终每条只给 `PASS / REVISE / DOWNGRADE`。

## 1. Phase P：held-out 预测（在重新揭示目标 response 前冻结）

以下每行的 `P` 按 **situation｜entry｜organization｜semantic transitions｜language realization｜stop** 六项顺序记。目标 comment 只提供 reviewer 需求，不提供作者如何答。这里的 scene ID 是排除对象；它在自己那一行的 remaining evidence 中没有贡献。

| 折 / held-out reviewer situation | Remaining independent evidence（只用非目标） | 冻结预测 P：六层 |
|---|---|---|
| **A1-α S04/R2-C2**：D 正定性/Theorem 证明受质疑 | S03/R2-C1 p.7 对象改动；S09/R3-C1 pp.11–12 技术差异；S15/R4-C5 p.20 技术动机 | **核心理论质疑｜技术事实/成立条件｜条件命题→所需证明→修订定位｜事实→条件→依据→推论｜D/PE 等技术对象作主语、条件贴命题；不预测公式｜命题及证明可核查后停**。 |
| **A1-β S12/R4-C2b**：Figure 1 输入输出不清 | S02/R1-C3 p.4、S03/R2-C1 p.7、S11/R4-C2a p.18 的局部修改 | **局部图示澄清｜Figure 1 已完成修改｜对象/动作→必要说明或位置｜concern→action→locator｜Figure 作改动对象、modified/updated 类动词；不需技术长论｜图改动与查找位置说明后停**。 |
| **A2-α S03/R2-C1**：Jacobian 句子错 | S02/R1-C3 p.4、S12/R4-C2b p.18 的短答；S04/R2-C2 pp.7–8、S10/R3-C2 pp.12–17 的长技术答 | **局部 wording｜完成修订动作｜动作→替换句/位置｜对象已改→可核对文本｜statement 作主语、corrected；公式可随替换句出现｜无需背景/新实验，替换可核查即停**。 |
| **A2-β S10/R3-C2**：PID/自适应比较及实验 | S01/R1-C2 pp.3–4 的 test、S13/R4-C3 pp.18–19 的真实实验、S09/R3-C1 pp.11–12 的多差异长答 | **复合 evidence 请求｜比较/实验动作或 baseline｜各子问 action→setup/baselines→Figures/Table→读数→位置｜一个证据块完成后转下个 concern｜results 作 locator 主语，PID/MBAC 邻比较维度，术语连续｜所有子问有 evidence 后停，预计比局部问题长**。 |
| **A3-α S01/R1-C2**：噪声/扰动缺测 | S03 p.7 manuscript object；S04 pp.7–8 technical object；S13 pp.18–19 experiments/results；S09 p.11 we/design | **新增 robustness test｜作者承接 concern 或 test 动作｜动作→setup→图→观察→位置｜测试对象转设置再转结果｜we/tests 可报告执行，disturbance/parameters 管设置，results 管图，obs 可 we 或对象作主语｜所测条件与结果清楚后停**。 |
| **A3-β S06/R2-C4**：Eq.(19) 首等号缺推导 | S03 p.7 修订对象、S04 pp.7–8 数学对象、S08 p.10 式链、S05 pp.8–9 定义 | **局部 derivation｜derivation 已补｜前提→中间式→所用事实/位置｜数学对象/关系引出下一式｜derivation 作动作主语，Vc/Uc 等作技术对象，derive/obtain；无图｜缺失等号可逐步核查后停**。 |
| **A4-α S04/R2-C2**：D 正定条件 | S07/R2-C5 pp.9–10 的零/非零条件；S08/R2-C6 p.10 的已知等式；S09/R3-C1 pp.11–12 比较 baseline | **证明核心前提｜受条件约束的技术命题｜条件→证明→该条件内结论｜前提贴 claim，再入推导｜PE 等条件与 D claim 相邻；技术名词重复；不预测具体不等号｜有条件的结论可追溯后停**。 |
| **A4-β S10/R3-C2**：PID/MBAC 比较 | S09/R3-C1 pp.11–12 [20]/Lagrange 对照；S04/R2-C2 p.7 条件限定；S01/R1-C2 p.3 测试设置 | **实证比较｜baseline/新增比较动作｜基线→图/表→同维度差异｜baseline 功能转区分指标｜PID/MBAC 靠 tracking/metric 判断，设置靠结果；术语不漂移｜所要求的维度读出后停**。 |
| **A5-α S01/R1-C2**：新增噪声图证据 | S10/R3-C2 pp.13/17 的 Figures+读图；S13/R4-C3 pp.18–19 的 Figure+nominal 观察 | **实验+Figure｜测试/设置｜locator→扰动/估计 observation→条件内解释｜图号只定位，下一句读可见变化｜results/disturbances 作主语、shown in Fig；数字可能但不要求；location 可先后｜读出所测结果后停**。 |
| **A5-β S13/R4-C3**：真实机器人实验 | S01/R1-C2 pp.3–4 噪声图+读值；S10/R3-C2 pp.13/17 tracking 图+读比较 | **真实 experiment+Figure｜实验动作/平台｜setup→Figure→估计结果观察→可支持解释｜从 locator 读 nominal/轨迹结果｜experiments/results 作主语，Fig 作 locator；不预设数字｜平台、任务和图中观察到位后停**。 |
| **A6-α S03/R2-C1**：修改 Jacobian 叙述 | S02/R1-C3 p.4 末尾位置；S06/R2-C4 p.9 位置先于式；S08/R2-C6 p.10 位置先于式 | **局部改句｜改动动作｜对象→位置和/或替换摘录｜位置承担核查而非必为末句｜statement/corrected，Section/Page 具体，术语连续｜摘录或位置使改句可找到即停**。 |
| **A6-β S10/R3-C2**：多图/表比较 | S01/R1-C2 p.4 结果后位置；S03/R2-C1 p.7 摘录前位置；S13/R4-C3 p.18 位置先于实验摘录 | **复合比较｜完成 action｜各证据块→某处 Section/Page｜位置可早可晚，跟随可核对修订｜results/Table 等对象与具体位置；不预测最后一句｜各子问可定位后停**。 |
| **B1-α S02/R1-C3**：两处错词 | S03/R2-C1 p.7、S11/R4-C2a p.18、S12/R4-C2b p.18 | **局部 typo｜typos 已改｜动作→必要校对范围/位置｜对象改动后即核查｜typos 作主语、corrected，可能 we 作 proofreading；无结果图｜错误及位置交代后停**。 |
| **B1-β S12/R4-C2b**：Figure 1 不清 | S02/R1-C3 p.4、S03/R2-C1 p.7、S11/R4-C2a p.18 | **局部 Figure clarification｜Figure 已改｜动作→必要修订说明/位置｜对象清楚后给 locator｜Figure 作主语、modified；图说明条件型｜图的修改可查后停，预计短**。 |
| **B2-α S05/R2-C3**：Eq.(18) typo + SVD 关系 | S07/R2-C5 pp.9–10 的局部定义/极限；S03/R2-C1 p.7 公式附近 wording | **局部定义兼 typo｜方程/前文已改｜动作→解释必要符号关系→新式/摘录→位置｜局部关系支撑表达｜formula/matrices 作技术主语，符号重复，条件近对应式｜新关系与修订式可查后停**。 |
| **B2-β S07/R2-C5**：零特征值极限 | S05/R2-C3 pp.8–9 的修订+定义；S03/R2-C1 p.7 的替换式 | **局部公式/definition｜已修改表达｜定义/条件→新公式或两类情形→位置/摘录｜修订对象转它的数学后果｜F(t)/eigenvalue 作主语，zero/nonzero 邻各自 claim｜极限疑问被新表达回答后停**。 |
| **B3-α S06/R2-C4**：Eq.(19) 首等号 | S08/R2-C6 p.10 的已知关系→多步不等式 | **缺代数步骤｜已补 derivation｜引用前提→中间式链→所用事实｜先可用关系，再变形式｜technical object/derive/obtain；公式为主体，位置可先给｜所问等号连通即停**。 |
| **B3-β S08/R2-C6**：Eq.(34) 末两不等式 | S06/R2-C4 p.9 的正交关系→等号链 | **缺不等式步骤｜已补 derivation｜已有关系/条件→逐步不等式→新符号/结论｜前提必须先于比较号｜equation/relationship 作对象，derive/obtain；位置可先给｜不等式依据及末步符号可核查后停**。 |
| **B4-α S01/R1-C2**：新增噪声/扰动测试 | S13/R4-C3 pp.18–19 的独立真实机器人实验；S10 p.13 仅宣布实验，不作完整第二证据 | **新增实验｜承接噪声 concern 或测试动作｜操作→噪声设置→图→观察→与所测条件相称的结论/位置｜setup 后才能给 locator｜tests/disturbance/results 作主语；强度可能量化，不预设｜测试条件、结果及修订可查后停**。 |
| **B4-β S13/R4-C3**：新增真实实验 | S01/R1-C2 pp.3–4 的独立噪声测试；S14 pp.19–20 是复用，排除 | **新增 experiment｜实验动作｜平台/任务→结果图→观察→条件内结论/位置｜setup→locator→reading｜experiments/robot/results 顺序承责；平台与图号紧邻｜实际平台结果可查后停**。 |
| **B5-α S09/R3-C1**：与 [20] 的 originality 对照 | S10/R3-C2 pp.12–13/17 的 PID/MBAC 可取处→差异 | **prior-work 比较｜前作已做事实｜baseline capability→本文不同技术维度→原因/证据｜先承认再区分｜[20] 贴它的作用，本文对象贴差异；不预设贡献数量｜差异维度说明到位后停**。 |
| **B5-β S10/R3-C2**：控制器对比 | S09/R3-C1 pp.11–12 的 [20]/Lagrange 范围与效率对照 | **多 baseline 实证比较｜既有控制器作用或 comparison action｜各 baseline 可取处→同指标差异→Figures/Table｜能力与局限连接｜PID/MBAC 靠 tracking/暂态，Figures locator→观察｜请求的比较维度有 evidence 后停**。 |
| **B6-α S05/R2-C3**：typo + SVD 解释 | S10/R3-C2 pp.12–17 多 comparison/experiment 子问；S14/R4-C4 pp.19–20 文献/非理想因素（仅 action 分块作参考，不用其未覆盖项） | **多 concern｜先改 typo 对象｜修错块→SVD 关系块→位置/摘录｜第一动作完成后再进入定义｜typos 与 formula 分别作主语；连接词只标换块｜两项均有可查答复后停**。 |
| **B6-β S14/R4-C4**：文献 + 量化/延迟/脏微分 | S05/R2-C3 pp.8–9、S10/R3-C2 pp.12–17 的多子问结构；S01 的扰动测试不算对目标三项的独立支持 | **多 concern｜文献处理或 test action｜引用文献块→量化/延迟/脏微分各有相应设置/证据块→各位置｜每块完成后转下一要求｜studies/tests/results 各担主语，具体测试条件紧贴 claim｜三种非理想因素均被覆盖才停**。 |

**冻结点**：以上 24 折预测已写入。以下章节仅在此后读取目标 Sxx 的完整 card/原文并追加，不反向修订 Phase P。

## 2. Phase R：揭示目标 scene 后的逐折核对

Phase P 首次写入时的 SHA-256 为 `1BC41DA7384EFA7A0701745B21960DB1710AAB27D66F596486F5CDF11C226989`。此后才重新读取 02 的目标 card。下表 “实际”按 entry→organization→transition→language→stop 简述；situation 已由 comment 冻结。`remaining sufficient?` 判断在排除目标且排除复用材料后作出。每行的机制结论在 §3 汇总，不以措辞不同判错。

### 2.1 A1–A6（每条两折）

| 折 / remaining sufficient? | 揭示的 actual response（来源） | 与冻结 P 的 match / mismatch 及归因 |
|---|---|---|
| **A1-α S04；是**：S03/S09/S15 仍支持实质入口 | R2-C2，PDF pp.7–8：感谢→PE 对收敛的重要性和在线核验难点→`if Rf is PE, D positive definite`→证明→Remark/location；技术对象 `PE/D` 连续，末尾复贴 Remark | **M** 技术条件入口与证明命中；**V** 原文先用两句背景再给命题，P 未要求“第一句必须是命题”；**D** 严格不等号、`D(t)>σ` 和重复摘录，不算机制成功的必要内容 |
| **A1-β S12；是**：S02/S03/S11 三个局部修订 | R4 原文第二个 C2，PDF p.18：感谢→`Figure 1 has been modified and updated`→Section II, Page 3→止；Figure 作主语、动作是完成修订 | **M** entry/action/location/短止均命中；**D** 未解释输入输出且动词重复，P 的“必要说明”条件型没有被满足，不能把简短等同充分 |
| **A2-α S03；是**：短例 S02/S12，长例 S04/S10 | R2-C1，PDF p.7：具体 statement 已改→Section II, Page 2→替换句与 Jacobian 公式→止 | **M** 小范围导致短答、替换内容收尾命中；**V** location 在摘录前；无机制错误 |
| **A2-β S10；是**：S01/S13/S09 支持复杂请求有多块 | R3-C2，PDF pp.12–17：长 rationale/NE/SVD→比较、参数表、实验的动作宣告→Figs.7–14 tracking/RMSE 读图→Table 读表→Section IV/Page 8；真实实验只报已做，本 scene 未展开 setup；行动与 rationale 有重复 | **M** “多要求→多块、较长”命中；**X** P 的“所有子问有 evidence 后停”并非 actual：实验子问只被宣告，且多个已完成动作反复说。不能以 source defect 让 A2 当前 stop claim PASS；需收缩 |
| **A3-α S01；是**：S03/S04/S13/S09 的主语责任仍独立 | R1-C2，PDF pp.3–4（附图至 p.6）：`we agree / we conduct`、`tests are conducted`、`disturbance is chosen`、`parameters are chosen`、`results/performance are shown`、`we can see`；位置前后各一次 | **M** 作者/设置/证据主语转换和动词功能命中；**V** `we` 与被动同在，不影响；**D** 语法和重复动作被隔离 |
| **A3-β S06；是**：S03/S04/S08/S05 仍覆盖对象与数学关系 | R2-C4，PDF p.9：`derivation ... has been ... formulated`→`Vc` 满足正交条件→`we can obtain`→`QUc` 连续式→`fact Ac is diagonal`→止 | **M** 修订对象、技术对象、`obtain`/式链与无图命中；**D** `detailed formulated/on both side` 不进入机制 |
| **A4-α S04；是**：S07/S08/S09 的条件或 baseline 邻接 | R2-C2，PDF pp.7–8：PE 条件紧贴 D 正定命题；证明窗口只在 `t>T>0` 下展开；技术名词重复 | **M** 条件位置和 proof transition 命中；**D** 最终严格 `>` 与矩阵/标量表述错误，不证明数学命题正确 |
| **A4-β S10；是**：S09 prior-work 对照与 S01 setup 独立 | R3-C2，PDF pp.12–13/17：PID、MBAC 的作用/局限贴着 tracking/暂态读取；`[16]` 为控制器比较，参数表转 `[27]`；先 Fig tracking 后 Table 估计 | **M** baseline 与比较维度邻接；**V** 多个 baseline/metric 分不同段，P 未要求同句；**D** `[20]/[27]` 错配和不对称比较需隔离 |
| **A5-α S01；是**：S10 的 tracking Figures 与 S13 的实验 Figure 独立 | R1-C2，PDF pp.3–4：奇数图给噪声，随后 ±2/4/6 cm；偶数图给估计，随后收敛 observation；再写 robustness claim 和 location | **M** locator→具体 observation 命中；**V** 数字只在此出现，P 未强求；**D** 图号总述错配、`verified robustness` 过强，候选 A5 本来未把后者设必需 |
| **A5-β S13；是**：S01 噪声图与 S10 tracking 图独立 | R4-C3，PDF pp.18–19：Baxter 左臂→轨迹图→估计 Fig.15→`most parameters close to nominal values (dashed line)`→robustness 结论 | **M** setup→locator→定性 observation 和主语选择命中；**D** 图号错配与过强 robustness 结论；不拿缺数字判失败 |
| **A6-α S03；是**：S02 末尾位置、S06/S08 前置位置 | R2-C1，PDF p.7：修订动作后给 Section II/Page 2，然后才贴新句与公式；末尾是公式 | **M** 位置为可核查线索、并非必然末句；无位置顺序错误 |
| **A6-β S10；是**：S01 的末尾位置、S03/S13 的前置位置 | R3-C2，PDF p.13 先报实验 Section IV/Page 7，p.17 比较段再以 Section IV/Page 8 收束；不同 evidence 块各有位置 | **M** 位置可早可晚、服务不同块；**D** 重复与错号不计 A6 的必需实现 |

### 2.2 B1–B6（同类优先双向）

| 折 / remaining sufficient? | 揭示的 actual response（来源） | 与冻结 P 的 match / mismatch 及归因 |
|---|---|---|
| **B1-α S02；是**：S03/S11/S12 仍为局部修订 | R1-C3，PDF p.4：typos 已改→全文 proofreading→蓝色标记和 Section I/Page 1→止；`typos` 与 `we` 轮换主语 | **M** 对象/动作/短止/位置命中；**V** 扩大到全稿校对是相邻但非必需动作；**D** `have been all corrected` 不迁移 |
| **B1-β S12；是**：S02/S03/S11 仍支持局部修订 | R4 第二个 C2，PDF p.18：Figure 1 修改→Section II/Page 3→止，未描述新输入输出 | **M** 候选的最小 organization 命中；**D** reviewer 具体问题未被文字充分解答，不能把这种不足纳入 B1 的 stop 充分性 |
| **B2-α S05；是**：S07 独立局部定义；S03 为邻近参考 | R2-C3，PDF pp.8–9：改 Eq.(18) typo→重写式前 statement→用 SVD 解释 `Uc=VcAcYcᵀ`→定义矩阵→Section III/Page 5→贴修订段 | **M** 动作→局部关系→新文本与位置命中；**V** 两个改动对象使段更长；**D** `σ1...σr/a1...an` 与 SVD 维数问题 |
| **B2-β S07；是**：S05 独立局部定义；S03 邻近 | R2-C5，PDF pp.9–10：报 equation/typo 已改→给 F(t) 新定义与 nonzero/zero 极限→Section III/Page 5→贴新 F(t) 及 `QUc=I−F`→止 | **M** action→条件/公式→摘录命中；**V** 原文先在说明句预告极限，再贴完整公式；**D** 极限所需参数条件未在局部清楚重述 |
| **B3-α S06；是**：S08 是独立不等式推导 | R2-C4，PDF p.9：旧/新式号→location→`VcᵀVc=I`→左乘得关系→代入 `QUc` 式链→说明 Ac 对角性→止 | **M** 前提→中间式→末步事实完整命中；**V** 推导比 S08 短，公式性质不同 |
| **B3-β S08；是**：S06 是独立等式推导 | R2-C6，PDF p.10：旧/新式号→location→由 Eq.(22) 与两恒等式进入 `L̇d` 多步不等式→定义 `μd,ρd`→紧集/负导数结论 | **M** 关系先行、中间链、新符号及 stop 区域命中；**V** 末尾还连接 theorem 所需结论；数学有效性未由结构匹配证明 |
| **B4-α S01；是**：S13 是独立真实实验；S14/S01 复用不算 | R1-C2，PDF pp.3–4：承接 measurement noise→测试动作和早期 location→白噪声 setup、σ/公平参数→配对图→偏差数值/估计收敛→一般 robustness claim→重复 location | **M** action/setup/Figure/reading 核心命中；**D/X** P 的“与所测条件相称的结论”未发生，作者直接写一般 `verified robustness`。这是当前 B4 把应有的证据边界混入了原文预测；需修订，不以过强 claim 帮它 PASS |
| **B4-β S13；是**：S01 是独立加噪实验 | R4-C3，PDF pp.18–19：Baxter 实验动作/前置 location→左臂平台→轨迹任务→估计图→多数参数接近 nominal→一般 robustness verified | **M** platform/task/locator/observation 命中；**D/X** 再次不命中“条件内结论”；真实实验并未测试 robustness。两个独立实验均暴露同一过宽的末块 |
| **B5-α S09；是，但只对共同子机制**：S10 是独立实验比较 | R3-C1，PDF pp.11–12：先承认 [20] 的动态估计→本文还估运动学→另起 NE/Lagrange 和 SVD/PE 维度→Section I/Page 2 | **M** baseline capability→技术差异命中；**V** 第二维以 NE 先行再给 [20] baseline，不是所有维度都 baseline 句先出现；候选只要求比较关系邻接；**D** 强 PE/效率 claim |
| **B5-β S10；是，但只对共同子机制**：S09 是独立前作比较 | R3-C2，PDF pp.12–13/17：承认 PID 已有应用、三控制器均可稳态 tracking→PID 大误差/MBAC 暂态差→Figs.7–14 和 RMSE→参数表 | **M** 可取表现→区分点与读图命中；**V** 多指标/表格超过 S09 的概念比较；**D** 图表与引文错配，不改变共同子机制 |
| **B6-α S05；是**：S10 仍有多个子问；S14 的分块可观察但其不完整不作充分性证据 | R2-C3，PDF pp.8–9：typo 动作→`Additionally` 转 statement/SVD 关系→位置/摘录；两个 concern 都有对应动作 | **M** 分 concern 的 action/explanation 命中；**V** 未编号，也没有显式 inventory 句；P 未强制版式 |
| **B6-β S14；是，仅支持“分成两个动作块”**：S05/S10；S01 的外扰材料排除 | R4-C4，PDF pp.19–20：引用并定位审稿人给的研究→`Additionally` 切到一般外扰测试和泛化观察→Section IV/Page 7→止；量化、延迟、脏微分均无独立 evidence | **M** 文献块→另一动作块的转换；**X/D** P 预测三种因素各有对应 setup/evidence，实际没有。B6 的“逐项覆盖才停”是审计条件，不是可靠的原文组织预测；S10 的实验子问也仅有宣告。需定点修订 |

### 2.3 对 mismatch 的分类判准

- **机制 blocker `X`**：A2 的“覆盖后才停”无法预测 S10；B4 的“必然限定 conclusion”无法预测 S01/S13；B6 的“每项均有证据才停”无法预测 S14，也受 S10 的部分覆盖削弱。这三条不能按现写法 PASS。
- **scenario variation `V`**：S04 的 PE 背景、S09 第二维先说 NE 再说 Lagrange、S10 多 baseline、S13 的平台/任务、S06/S08 的式链长短等，均不推翻保留的语义推进。
- **source defect `D`**：未覆盖 concern、冗余、错号、过强结论与语法错误照实记录；不为“预测准确”去复制它们，也不把这些缺陷默认为作者稳定的合格机制。
- **surface wording `W`**：`As suggested / According to... / In addition`、主被动选择的差异未被当成失败，因为预测没有指定连接词或逐字句。

## 3. A1–A6 / B1–B6 的机制级裁决

| Mechanism | 两折的 remaining evidence 与核心预测 | 裁决 | 原因与可保留边界 |
|---|---|---|---|
| **A1** | 每折移除目标后仍有多个独立实质入口例；S04 条件命题、S12 修改动作均命中 | **PASS** | “进入可回答对象/动作”有实质预测力；不规定感谢后的确切第几句 |
| **A2** | 短/长响应对比仍有独立例；S03 短答命中，S10 多块命中但 stop 预测错误 | **REVISE** | “篇幅随任务所需块变化”可保留；“覆盖后即停”不是可靠的原文行为，且 S12/S14/S10 可在未充分覆盖时结束 |
| **A3** | 两折剩余有修订、数学、实验、图表的不同 subject；S01/S06 均命中 | **PASS** | 语义责任→subject/verb 类别成立；不设 `we` 禁令、语态比例或具体词汇表 |
| **A4** | S04 去除后有 S07/S08/S09，S10 去除后有 S09/S01 等；条件/baseline 位置命中 | **PASS** | 限“受约束 claim 与条件/基线相邻”；不把数学证明本身的正确性一并验证 |
| **A5** | S01、S13 各可由另一独立实验图及 S10 图预测；locator→observation 均命中 | **PASS** | 支持证据定位与读取；过强 effectiveness/robustness claim 被隔离，非 A5 必需末块 |
| **A6** | S03/S10 各自排除后仍有位置前置/后置独立例，实际位置顺序命中 | **PASS** | 条件是 response 报告可定位稿件修改；location 用于核查而非必为尾句 |
| **B1** | S02 与 S12 双向由其他局部修正预测，短行动与位置命中 | **PASS** | 只保留组织；S12 内容不足不证明“动作+location”足以答所有 Figure clarification |
| **B2** | S05↔S07 双向仍有一条独立局部定义例，并有 S03 边缘支撑；动作→局部关系→新表达命中 | **PASS** | 只允许“局部 definition/equation”触发；SVD/极限的具体数学内容仍是单例 |
| **B3** | S06↔S08 双向各有一条独立 derivation scene；前提→式链→末步依据/符号命中 | **PASS** | 等号与不等式只共享结构，不共享具体运算 |
| **B4** | S01↔S13 两个独立实验支持 action/setup/locator/observation；两条的 bounded conclusion 预测都未命中 | **REVISE** | 原机制把“应有的范围约束”误写成原文可靠末块。保留实验中段；把 bounded conclusion 改为独立 evidence-quality gate，不能当已验证 TIE fingerprint |
| **B5** | S09↔S10 是两种独立比较；baseline capability→差异命中，完整多图表形式不作为本机制 | **PASS** | 限共同的 comparison 子机制；S09 第二维先给本文 NE 再给 Lagrange 仍保持 baseline 邻接，不强制先后句序 |
| **B6** | S05 与 S14 两折仍有其他多 concern scene；分成动作块命中，逐项 evidence/stop 在 S14 失败，S10 也不完整 | **REVISE** | 保留“按 concern 分块及转换”；把逐项覆盖移到独立 audit criterion，不描述为作者稳定的完成/停止方式 |

**总体判定**：12 条均完成至少两折，并明确排除了复用表与复用外扰的假独立性。9 条 `PASS`、3 条 `REVISE`、0 条 `DOWNGRADE`。这不是“全部可以升级 00”：A2、B4、B6 的现行文字是 blocker，须先定点收缩并在下一阶段单独复核；本轮没有修改 03 或 00。

## 4. C1–C6 独立复例复查

LEVEL C 不做 PASS 验证，只按 02 全量 16 scene 和 PDF 目录复查是否出现**真正独立的第二例**。

| C | 唯一完整场景 | 似乎相似但不能升级的材料 | 复查结果 |
|---|---|---|---|
| **C1** 核心证明条件→窗口推导 | S04/R2-C2，PDF pp.7–8 | S06/S08 是局部等号/不等式推导，不质疑 theorem 的根基；S04 还含 source defect | **仍保持 C；无独立复例** |
| **C2** novelty 多差异维度 | S09/R3-C1，PDF pp.11–12 | S15 是为何选方法，S10 的 rationale 不能当第二条 originality challenge | **仍保持 C；无独立复例** |
| **C3** PID/MBAC 图+RMSE+参数表综合链 | S10/R3-C2，PDF pp.12–17 | S16 的表段是同一份材料；S13 的真实实验未构成第二套多控制器比较 | **仍保持 C；无独立复例** |
| **C4** method motivation 完整链 | S15/R4-C5，PDF p.20 | S09/S10 有部分既有法 rationale，但 reviewer situation 与完整入口/收尾不同 | **仍保持 C；无独立复例** |
| **C5** 单独 Table/data request | S16/R4-C6，PDF pp.20–21 | S10 p.17 的参数表与 S16 同表、同段落，不能二计 | **仍保持 C；无独立复例** |
| **C6** σ 与三组偏差/配对图 | S01/R1-C2，PDF pp.3–6 | S14 只复述同一外扰测试；无第二套强度/数字图 | **仍保持 C；无独立复例** |

## 5. Validation-induced revisions（只写定点改法，不修改 03）

| 当前候选 | 失败位置与为何不能按现文通过 | 应收缩到的候选范围 | 升级 00 前的 blocker |
|---|---|---|---|
| **A2** `功能块数量由问题所需证据决定，已覆盖即停` | S10/R3-C2 pp.12–17 重复 rationale/action，真实实验仅宣告；S12/R4-C2b p.18 与 S14/R4-C4 pp.19–20 也在具体 concern 未充分解释时停止。当前 stop clause 把理想完成标准伪装成稳定作者行为 | “问题涉及的独立技术/证据任务越多，response 往往出现更多不同功能块；局部错处通常短。原文停止点可能早于充分覆盖，也可能在重复后才停。”停止充分性另作 audit，不属描述机制 | **现文 A2 不能直接进 00**；需删除“已覆盖即停”作为 TIE 事实，只保留有 LOO 支持的范围-块数关系 |
| **B4** `action→setup→Figure→observation→与测试范围相称的解释` | S01/R1-C2 p.4 和 S13/R4-C3 p.19 都从有限观察跳到一般 robustness verified；冻结预测的 bounded conclusion 连续两折失败。用作者的错 claim 反向证明候选是不正当 source-defect contamination | “新增独立实验的可预测主体为 action→具体 setup→evidence locator→observation（位置可前/后）。是否继续给结论及其范围，作为独立证据质量检查；原文没有稳定的 bounded-conclusion 实现。” | **现文 B4 不能直接进 00**；不能把规范性 bounded claim 标为原文 fingerprint |
| **B6** `逐项映射→分块给 action/evidence→回查遗漏；所有 concern 有证据才停` | S05/R2-C3 pp.8–9 两项均处理，但 S14/R4-C4 pp.19–20 只引用文献加一般外扰，未覆盖三种指定因素；S10/R3-C2 p.13 的真实实验也仅宣告。冻结预测对 S14 失败 | “多 concern 往往由不同 action/evidence blocks 承接，块间以新内容转换；**并不保证**每项均被充分回答。逐项覆盖检查是单独的验证门槛。” | **现文 B6 不能直接进 00**；必须把 descriptive 分块与 normative completeness 拆开 |

不为 A1/A3/A4/A5/A6/B1/B2/B3/B5 做措辞性修订；它们的两折均命中核心语义推进。`PASS` 只表示当前有限语料内该机制经排除目标后仍可预测，不表示其适用于其他期刊、稿件或所有 reviewer 情形。

## 6. Final validated set 与失败类型审计

| 结果 | ID | 后续使用边界 |
|---|---|---|
| **VALIDATED A** | **A1、A3、A4、A5、A6** | 可作为本 PDF 的跨 scene 候选；每次仍需核对新 comment 的真实对象和数据 |
| **VALIDATED B** | **B1、B2、B3、B5** | 只在对应 situation 触发；不能推广到核心证明、完整 novelty 或综合比较全链 |
| **REVISE** | **A2、B4、B6** | 定点修订见 §5；当前文本阻碍直接升级 `00` |
| **DOWNGRADE** | **无** | 本轮没有一条在去除目标后完全失去独立依据或核心转移全盘失败；三条 REVISE 均保有可缩窄的中段机制 |
| **C remains reference only** | **C1–C6** | 全部仍缺真正独立复例；不得升级成可复用生成规则 |

**六类失败检查**：

1. **Hindsight bias**：发现于 A2、B4、B6 的末端叙述：先知道 response 结构/希望的完成标准，再把“应当充分、应当有边界”写成貌似原文规律。冻结预测对 S10、S01/S13、S14 的失败暴露了它们。本轮因分析者历史上读过目标，仍不能宣称完全消除 hindsight；但所有折的 prediction 在本轮揭示前冻结。
2. **Evidence leakage**：S10/S16 同表、S01/S14 同测试在 remaining 栏明确去重。B2/B3/B4/B5 的双向测试只用真正另一 scene 的共同功能；没有以目标自己的 card 作为其预测依据。历史知识不可从分析者记忆剥离，已在 §0 明示。
3. **Overgeneralization**：A2 停止充分性、B4 bounded conclusion、B6 逐项完成超出原文；C1–C6 未升级。
4. **Under-specification**：A1 若只说“回答 reviewer”会不可证伪；本轮具体预测了技术事实/修订对象的 entry 和后续状态。A3 具体到语义责任与主语/动词类型；A5 具体到 locator 后的 observation。剩余机制均按六层预测接受检验。
5. **Over-specification**：未要求 `To further...`、`However`、固定段数、Figure 作主语或 location 末置；S04 背景、S09 第二维顺序作为 variation 而非失败。
6. **Source-defect contamination**：PDF 中过强 robustness、错图/表号、未覆盖子问、冗余和语法错误均未作为可生成依据；B4/B6 因候选把规范性边界混入描述而被 REVISE。

**升级门槛**：若要把本验证结果用于更新 `00`，本轮发现的 blocker 是 **A2、B4、B6 现行候选文字**，以及 C1–C6 的独立证据不足。这里没有修改 `00`、`01`、`02`、`03`、最终知识库或 TCYB 文件，也没有进入下一步。

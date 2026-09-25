# A2 Codex：Comment 1 response 原始证据与决策记录

## 0. 文档性质与范围

- 记录对象：第二个 Codex 账号在读取 `comment-response1-交接` 后，继续处理 TCYB `Comment 1 response` 的完整可恢复工作历史。
- 时间范围：从接收四个 handoff 文件开始，到当前 TeX 中完成明确 Fig. 面板引用和 `real-time feasibility criterion` 定点修改为止。
- 记录目的：保真保存来源、用户反馈、判断、修改、纠正和当前状态，供后续知识库提炼使用。
- 本文不是最终写作规则，不把一次性措辞、个别 TIE 写法或尚未裁决的偏好上升为通则。
- 本文不覆盖第一个账号的记录。第二个账号读取并继承 handoff，不意味着 handoff 中的内容是第二个账号独立发现的。

### 状态标签

- `INHERITED_CONFIRMED`：由第一个账号形成，并在四个 handoff 文件中明确交接为已确认内容。
- `NEW_CONFIRMED`：handoff 之后，经本账号实际修改、用户反馈、TIE 原文核对、JAS／稿件核对或实际验收新确认的内容。
- `CASE_SPECIFIC`：只适用于当前 Comment 1、当前 reviewer、当前稿件、当前正式图或当前项目的事实与裁决。即使同时标记为 `INHERITED_CONFIRMED` 或 `NEW_CONFIRMED`，也不能直接抽取为通用规则。
- `SUPERSEDED`：早期判断、术语或状态后来被用户明确的新判断替代。保留它只为呈现纠错链，当前执行以替代后的判断为准。
- `REJECTED`：曾出现、曾被建议或曾被错误泛化，随后被用户否决、被原始资料反证或被后续裁决删除的内容。不得转写为最终规则。
- `UNRESOLVED`：现有证据不足、仍有占位符、尚未同步编译，或当前可访问对话记录不能完整还原的内容。不得转写为最终规则。

`INHERITED_CONFIRMED` 或 `NEW_CONFIRMED` 只表示在相应来源和适用范围内已经确认，不自动表示可以进入通用知识库。能否抽象迁移，仍须经过后续三源交叉裁决。

---

## 1. 来源边界：继承内容与本账号新增内容

### 1.1 `INHERITED_CONFIRMED`：handoff 交付时的总状态

范围说明：本节的 Comment 1 主线、实验事实、符号、数值、文件边界和 reviewer 阅读假设同时属于 `CASE_SPECIFIC`。这里只记录 handoff 时已确认的项目状态，不把它们写成跨稿件规则。

1. **任务性质**
   - 原始交接措辞：`当前任务仍是“表达与组织优化”，不是重新设计回答思路，也不是扩展实验。`
   - 继承结果：不改变作者已确认的科学主线、实验事实、数值和结论边界；不从头另写一套逻辑。

2. **表达依据的优先级**
   - TIE 范例 PDF 原文与三份 TIE 总结是表达和组织的主要依据。
   - JAS 原论文与当前稿件只用于核实实验内容、变量、符号、比较对象和设置。
   - `nature-response`／`nature-polishing` 只作克制、claim 边界和一致性检查；与 TIE 实际写法冲突时，以 TIE 为准。
   - 旧 Response 只可吸收局部有效结构，不能整体回退或堆叠。

3. **Comment 1 的两条核心回答**
   - 计算目标是满足实时控制要求，不证明相对于所有方法的最低计算成本。
   - 接受审稿人对不同任务／设置下 computational-efficiency 结论的质疑，用 task cost 与 computation-time 证据补足回答。

4. **最小认知框架**
   - ILC 跨迭代以 task cost `\(\mathcal J_j\)` 观察收敛。
   - 每一迭代包含多个控制步，实时性由每步在线计算能否在 control period `\(\Delta t\)` 内完成判断。
   - “较少迭代次数”不能直接推出“每步计算成本更低”。

5. **比较口径**
   - fast-AGP 与 standard Gaussian process (GP) 比较。
   - CRBFNN 与 lattice-distributed RBFNN 比较。
   - 不得把 fast-AGP 相对 GP 的计算减负扩大为相对 IL-SOGP 的最低计算成本。

6. **实验与事实边界**
   - 不新增实验，不改实验结果，不换正式结果图。
   - JAS Cases 1/2 用于提供不同 interaction tasks 的证据。
   - 原 two-DOF task 中补充不同 `\(W_x\)` 与 `\(S_e(t)\)` 的证据。
   - proposed method 的计算时间可以如实高于 IL-SOGP；不能回避不利比较。

7. **正式变量与符号**
   - task cost `\(\mathcal J_j\)`，第 10 次迭代结果为 `\(\mathcal J_{10}\)`。
   - control period `\(\Delta t\)`。
   - position-error weight `\(W_x\)`、force-integral weight `\(W_f\)`。
   - environment stiffness `\(S_e(t)\)`。
   - 不使用图文件名中的 `b:c` 作为正式变量，不使用稿件未定义的 `\(S_{e,\max}\)`。

8. **不可越过的工作边界**
   - 不修改 Comment 1 之外的内容。
   - 不修改稿件正文、旧 Response 或正式图文件。
   - 不从源代码补充设置。
   - 不虚构 revised-manuscript 位置。
   - JAS 文献对应的 revised-manuscript 编号保留 `[XX]`，不得猜测。

9. **handoff 时的具体实验事实**
   - Cases 1/2 使用 simulated seven-DOF Franka Emika Panda，外环 `\(\Delta t=10\)` ms。
   - Case 1：accurate tracking，`\(C=[25,0,1]\)`；`\(\mathcal J_{10}\)` 为 proposed 80.40、IL-SOGP 86.01、classical IL 88.61；proposed computation time 为 4.75 ms。
   - Case 2：compliant interaction，`\(C=[100,0,0.1]\)`；`\(\mathcal J_{10}\)` 为 proposed 64.83、IL-SOGP 66.86、classical IL 72.06；proposed computation time 为 4.65 ms。
   - `\(W_x=20I,50I,200I\)`，`\(W_f=I\)` 固定。
   - `\(S_e(t)=10(\sin\pi t)^2I,30(\sin\pi t)^2I,50(\sin\pi t)^2I\)`。
   - 原机器人实验 proposed method 的旧口径 maximum total computation time per step 为 9.90 ms，`\(\Delta t=20\)` ms；standard GP 在相同条件下超过控制周期。

10. **handoff 时尚未完成的状态**
    - handoff 明确称最近一轮英文尚未完成 TIE 风格最终逐句验收。
    - handoff 时 TeX 与 PDF 不同步。
    - 开头语气、JAS 设置密度、变量信息分配、目的句重复和图文分页仍待判断。

### 1.2 继承内容在本账号中的处理原则

- handoff 中的既有标准只记录一次，归入 `INHERITED_CONFIRMED`。
- 本账号后续只有在用户给出新裁决、TIE 原文进一步核对或当前版本实际验收后，才记录为 `NEW_CONFIRMED`。
- `SUPERSEDED`、`CASE_SPECIFIC`：handoff 中旧术语 `maximum total computation time per step` 后来被用户正式更名；该旧术语仅作为历史状态保存，不是当前 Comment 1 的现行术语，更不是通用规则。
- `SUPERSEDED`、`CASE_SPECIFIC`：handoff 曾把明确的实时性收束主要落在新增 JAS Cases 1/2。A2 后续在加入并核验 `W_x`／`S_e(t)` 的 computation-time 图后，用户接受的当前结论改为同时覆盖 two tested interaction tasks 与 reported variations，但仍不允许推广到未测试任务、平台或设置。

---

## 2. handoff 后的工作时间线与关键变化

### 阶段 A2-01：接管与优先级确认

**用户要求**

> “先完整阅读……4 个交接文件，准确继承其中已经确认的要求、标准、纠正、边界和当前工作状态。不要重新解释任务，不要推倒重来。”

> “最终版本必须在整体写作习惯和所有细节上，都达到 TIE 范例体现出的顶刊 reviewer response 水平。”

**处理结果**

- `INHERITED_CONFIRMED`：确认 TIE PDF 和三份总结为表达主标准，JAS／稿件为事实来源，Nature Skill 仅辅助。
- `NEW_CONFIRMED`：用户进一步强调，既往反馈不是孤立修改点，而是在校准“从各方面与 TIE 实际写作风格保持一致”的整体标准。
- 后续修改不能只做逐项替换，应从全文逻辑、组织、句法和读者路径统一检查。

### 阶段 A2-02：独立验收与 16 项问题复核

**用户要求**

> “先逐字逐句检查，再分析整体结构与组织……尤其判断是否还存在‘内容正确，但不符合 TIE 作者实际写作习惯’的地方。”

随后用户要求把先前列出的 16 个问题逐条分为：

1. 有 TIE／总结／JAS／稿件／既定要求明确支持的真实问题；
2. 只是推断或泛化写作偏好；
3. 是问题但受既定边界限制不能如此处理。

**裁决意义**

- `NEW_CONFIRMED`：不能因为某种写法“更专业”就自动视为必须采用。
- `NEW_CONFIRMED`：不能把 TIE 的个别句式或一次性组织方式泛化为硬性规则。
- `NEW_CONFIRMED`：之后只允许使用复核后保留的标准；被删除的问题不得重新引入。
- `NEW_CONFIRMED`：受限问题只能在边界内处理，尤其是不改正式图、不虚构 revised-manuscript 位置、不替换 `[XX]`。
- `UNRESOLVED`：当前可访问的压缩对话记录未保留当时 16 项原始列表和逐项裁决全文，不能凭后续印象重建其逐条内容。可恢复的是上述分类方法、被后续明确保留的修改锚点以及不得重新引入已删除标准的约束。

### 阶段 A2-03：按裁决后的标准整体收敛

**用户要求**

> “不要机械地逐条修补‘保留问题’，而是……重新从整体上审视并收敛全文的逻辑、表达和组织。”

**本阶段确认的修改锚点**

- 实验进入方式要先说明该证据单元为什么做、验证什么，再给设置、结果和结论。
- 指标、变量和判据要在需要的位置同时保留含义与符号，避免 `task cost`、`control period`、`this time`、`its`、`weight settings`、`environment stiffness settings` 等需要回读的表达。
- 术语不得在后文改用近义说法。
- `nature-response` 只检查回应边界和 claim 强度，表达仍以 TIE 为准。

**用户再次校准**

> “不要把本轮修改限制为你列出的这三项操作……仍需逐字逐句检查整个 Comment 1 response……但不要改动已经正确的内容。”

**结果**

- `NEW_CONFIRMED`：检查锚点用于发现同类问题，不等于无限新增写作规则。
- `NEW_CONFIRMED`：整体检查与最小改动同时成立；正确内容应保持不动。

### 阶段 A2-04：最终收敛，以同一主线做减法

**用户给出的唯一核心论证线**

> “审稿人质疑 computational-efficiency 结论在不同任务/设置下是否成立 → 明确本文真正的计算判据是 maximum total computation time per step 是否低于 control period `\(\Delta t\)` → 补充不同任务和不同设置下的 task cost `\(\mathcal J_j\)` 与 computation-time 证据 → 根据结果给出有限结论。”

状态说明：这段引文真实记录了当时的主线，但其中 `maximum total computation time per step` 后来被正式指标名替代，现标为 `SUPERSEDED`；主线本身仍有效。

**要求删除或压缩的重复**

- 首段与 `1) Computational objective and evaluation criteria` 不重复解释 real-time criterion。
- Section 2 总起段与 JAS Cases 引入不重复宣布“接下来做什么”。
- Case 1、Case 2、`\(W_x\)`、`\(S_e(t)\)` 不机械复制完整论证模板。
- 结尾不重新枚举全部结果。

**同期三个具体修正**

1. 首段对新增证据的概括必须覆盖 Cases 1/2、`\(W_x\)`、`\(S_e(t)\)`，但不堆具体数值。
2. lattice-distributed RBFNN 首次出现处补 response 内正式文献，并保留 revised manuscript `[29]` 对应关系。
3. 删除免责声明式结尾 `This conclusion does not imply minimum computation time...`，改为由证据自然得到正面、简洁且限定于测试条件的结论。

**实际结果**

- `NEW_CONFIRMED`：首段改为完整概括三类新增比较及主要结果。
- `NEW_CONFIRMED`：加入 `respLiuTCYB2025`，正文写为 `lattice-distributed RBFNN~\cite{respLiuTCYB2025} ([29] in the revised manuscript)`。
- `NEW_CONFIRMED`：结尾不再引入 `minimum computation time` 这一新免责声明术语。
- `NEW_CONFIRMED`：保持现有两个编号部分的总体结构。

### 阶段 A2-05：版本总体通过后的三处定点修正与一次编译

**用户状态判断**

> “当前版本整体已经通过内容、逻辑和表达验收，不要再重写或调整已经正确的部分。”

**三处定点修改**

1. `we clarify the evaluation criterion and compare...` 改为直接的“已进行比较”式表达。
2. `To further evaluate the criterion...` 中含糊的 `the criterion` 改为明确的 real-time feasibility／计算判据。
3. `differ from those in the manuscript` 改为明确指向 `the original two-DOF task`。

**实际文本变化**

- 首段使用 `comparisons ... have been conducted`，避免以元话语说明“我们澄清什么”。
- 进入 Cases 1/2 时直接写 `To further evaluate real-time feasibility...`。
- 对不同任务的说明写为 `differ from those used in the original two-DOF task`。

**构建状态**

- `NEW_CONFIRMED`：当时运行 `latexmk -pdf -interaction=nonstopmode -halt-on-error Response-TCYB.tex` 成功，得到 15 页 PDF。
- 新增的 `respLiuTCYB2025` 第一次编译出现未定义，第二次编译已解析。
- 当时剩余一个位于 Comment 1 之外的非致命 `Underfull \hbox` 警告。
- 该次编译发生在后续 Section 2 重组和 `t_{\mathrm{comp}}^{\max}` 统一之前，因此不能代表当前 TeX。

### 阶段 A2-06：结果图正文重组与 computation-time 指标正式统一

**用户指出的问题 A**

> “TIE 的共同逻辑不是‘每张图各自写一套完整 response’。”

用户给出的实际推进顺序为：

> “统一说明为什么补实验/比较 → 给必要实验设置 → 一组图统一呈现结果 → 直接指出 reviewer 真正需要看到的关键现象 → 一次性得到有限结论。”

**用户指出的问题 B**

> “computation-time 指标需要正式统一为 `\(t_{\mathrm{comp}}^{\max}\)`。”

正式名称改为：

> `maximum online computation time per control step (t_{\mathrm{comp}}^{\max})`

判据改为：

> `t_{\mathrm{comp}}^{\max}<\Delta t`

**TIE 原文核对**

- 本账号直接读取并定位 TIE R1-2、R3-2、R4-3。
- R1-2 的可见动作是：先统一说明加入不同噪声／扰动测试与公共设置，再统一指向图组，随后读出关键现象并一次收束鲁棒性结论。
- R3-2 的可见动作是：说明新增 PID／MBAC 比较与实验，再统一写 comparison results，随后从图组读出审稿人关心的性能差异。
- R4-3 的可见动作是：先说明补做 Baxter 机器人实验，再给平台／轨迹、图中估计结果和有限结论。
- `NEW_CONFIRMED`：迁移的是证据组的组织方式、信息密度和句法节奏，不是机械复制 `The comparison results are depicted...` 等固定句式。

**实际重组**

以下分组、符号、数值、图文分工和结论均为 `NEW_CONFIRMED`、`CASE_SPECIFIC`。它们记录当前 Comment 1 的最终应用，不自动构成所有 response 的固定模板。

1. Cases 1/2 合并为第一个 evidence block。
   - 公共目的：检验不同于原 two-DOF task 的 interaction tasks 下 real-time feasibility。
   - 公共设置：Panda robot、different trajectory/contact environment、`\(\Delta t=10\)` ms、compared methods。
   - Case-specific 设置仍保留：Case 1 `\(C=[25,0,1]\)`；Case 2 `\(C=[100,0,0.1]\)`。
   - Case-specific 结果仍保留：两组 `\(\mathcal J_{10}\)` 全部数值、4.75 ms、4.65 ms，以及 proposed computation time 高于 IL-SOGP 但低于 `\(\Delta t\)`。

2. `\(W_x\)` 与 `\(S_e(t)\)` 合并为第二个 evidence block。
   - 公共目的：检查原 two-DOF task 中不同 task objectives 与 environment conditions。
   - `\(W_x=20I,50I,200I\)` 与固定 `\(W_f=I\)` 保留。
   - 三个 `\(S_e(t)\)` 表达式完整保留。
   - 两类图各自的关键结果保留：proposed 的 `\(\mathcal J_{10}\)` 均低于 IL-SOGP；proposed 的 `\(t_{\mathrm{comp}}^{\max}\)` 一般高于 IL-SOGP，但在所报比较中满足 `\(t_{\mathrm{comp}}^{\max}<20\)` ms。

3. 正文与 caption 分工。
   - caption 继续自足，保留方法／条件、指标、面板含义与 control-period 虚线。
   - 正文只读出 reviewer 判断 computational efficiency／real-time feasibility 所需的变化条件、`\(\mathcal J_{10}\)` 比较、`\(t_{\mathrm{comp}}^{\max}<\Delta t\)` 和 proposed 相对 IL-SOGP 的不利时间比较。

4. 全 Comment 1 术语替换。
   - 第一次出现完整定义 `maximum online computation time per control step ($t_{\mathrm{comp}}^{\max}$)`。
   - 后文优先使用符号 `\(t_{\mathrm{comp}}^{\max}\)`。
   - 相关 subcaption／caption 同步使用新名称和符号。
   - 旧短语 `maximum total computation time per step` 在当前 Comment 1 中清零。

5. 结论。
   - 当前结尾为：`These results verify that the proposed method satisfies the real-time feasibility criterion $t_{\mathrm{comp}}^{\max}<\Delta t$ under the two tested interaction tasks and the reported variations in $W_x$ and $S_e(t)$.`
   - `NEW_CONFIRMED`：该结论只覆盖 two tested interaction tasks 与 reported variations；不推出所有任务、平台或设置下的普遍保证。

### 阶段 A2-07：对 evidence block 的重要校准

**用户补充**

> “不要把‘实验目的和设置集中交代一次’理解为整个 Section 2 只能出现一次设置说明。”

> “目标是消除‘重复论证’，不是删除‘必要证据’。”

**核对结果**

- `NEW_CONFIRMED`、`CASE_SPECIFIC`：共同目的和公共设置只在同一 evidence block 内集中交代一次。
- `NEW_CONFIRMED`、`CASE_SPECIFIC`：不同实验不可替代的设置、数值与结果必须保留。
- 当前 Cases 1/2 block 已保留各自 `C`、`\(\mathcal J_{10}\)` 和 `\(t_{\mathrm{comp}}^{\max}\)` 数值。
- 当前 `\(W_x\)`／`\(S_e(t)\)` block 已保留两类变量设置和各自关键结果。
- 本轮检查后无须修改文件。

### 阶段 A2-08：最后两处定点表达修正

**用户要求**

1. 将含糊的 `panels (c)`／`Panels (d)` 改为直接图号引用。
2. 将 `real-time-feasibility criterion` 改为 `real-time feasibility criterion`。

**实际结果**

本阶段两项均为 `NEW_CONFIRMED`、`CASE_SPECIFIC` 的定点修改，不外推为所有 response 的图号或复合定语规则。

- 当前正文使用：
  - `As shown in Figs.~\ref{fig:jas_case1}(c) and~\ref{fig:jas_case2}(c), ...`
  - `Figs.~\ref{fig:jas_case1}(d) and~\ref{fig:jas_case2}(d) show that ...`
- 当前结尾使用 `real-time feasibility criterion`。
- `[XX]` 未处理。
- captions 未增加 IL-SOGP 的 revised-manuscript 编号或重复引用。

---

## 3. `NEW_CONFIRMED`：本账号新增确认的判断

本节记录 A2 新确认的项目决策。除非条目明确说明可迁移且随后通过三源裁决，否则均不得仅因 `NEW_CONFIRMED` 标签而升级为通用规则。包含当前句子、变量、数值、图号、caption、引用或 reviewer 路径的条目同时标记为 `CASE_SPECIFIC`。

### NC-01：整篇验收必须区分“正确”与“像 TIE 作者实际会写”

- 状态：`NEW_CONFIRMED`。这是当前以 TIE 为最高表达标准的项目验收原则；是否抽象为通用知识仍待三源裁决。
- 用户反复使用的标准：`内容正确，但不符合 TIE 作者实际写作习惯` 仍属于需要修正的问题。
- 依据：TIE PDF 三处新实验／比较回复的句间动作、三份总结对信息位置和证据链的拆解、用户的逐轮验收。
- 处理结果：不仅检查语法和事实，还检查首段动作、证据进入、图组组织、读图句、结论收束和重复模板。
- 边界：这不授权新增未经 TIE 或项目资料支持的“更专业”偏好。

### NC-02：当前 Comment 1 首段直接报告已完成的比较

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 被修正表达：`we clarify the evaluation criterion and compare...`
- 当前方向：`comparisons ... have been conducted`。
- 依据：TIE 常在感谢后直接报告已做的 tests/comparisons；用户定点要求。
- 原因：审稿人需要先看到采取了什么行动和证据，而不是作者对自己写作动作的描述。
- 纠错链：用户要求把 `we clarify...` 改成直接“已进行比较”式表达 → A2 改为 `comparisons ... have been conducted` → 复核其必要性是因为当前首段需要立即交代新增证据 → TIE R1-2／R3-2 的 action-first 推进与用户最终裁决共同支持 → 当前句子保留，但不据此禁止所有 response 中的 `clarify`。

### NC-03：当前首段证据概括与后文三类证据对应

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 必须覆盖 Cases 1/2、`\(W_x\)`、`\(S_e(t)\)` 三类比较。
- 不在首段提前堆具体数值。
- 当前主要结果概括：`\(\mathcal J_{10}\)` 低于 IL-SOGP；`\(t_{\mathrm{comp}}^{\max}\)` 一般高于 IL-SOGP，但在测试条件下低于相应 `\(\Delta t\)`。

### NC-04：当前 Cases 进入句明确 real-time feasibility

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 被修正表达：`To further evaluate the criterion...`
- 当前表达：`To further evaluate real-time feasibility...`
- 原因：前文同时出现 task cost、computational burden、control period，`the criterion` 会迫使审稿人回读。
- 纠错链：用户指出 `the criterion` 含糊 → A2 直接写 `real-time feasibility` → 重新核验发现当前段落附近存在多个评价量与判据 → 用户定点裁决和当前技术语境支持修改 → 只确认本句需显化对象，不把“任何 criterion 都必须展开全称”写成通则。

### NC-05：当前不同任务比较明确指向 original two-DOF task

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 被修正表达：`differ from those in the manuscript`。
- 当前表达：`differ from those used in the original two-DOF task`。
- 原因：明确“不同任务”的比较基准，避免把稿件整体当作模糊先行项。
- 纠错链：用户要求明确指向 original two-DOF task → A2 替换模糊的 manuscript 参照 → 复核 JAS Cases 与当前稿件原任务的事实关系 → JAS／当前稿件与用户最终措辞共同支持 → 当前参照对象确认，不外推为禁止所有 `the manuscript`。

### NC-06：当前 Section 2 按两个 evidence blocks 组织

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`；其中 evidence-block 是否可抽象迁移，留待三源裁决。
- Cases 1/2 是一个 block；`\(W_x\)`／`\(S_e(t)\)` 是另一个 block。
- 同一 block：共同目的和公共设置集中说明，结果图统一进入，关键现象集中读取，结论只收束一次。
- 不同 block：仍各自保留必要进入；同一 block 内不同实验不可替代的设置、数值和结果也必须保留。
- 依据：TIE R1-2、R3-2、R4-3 的实际推进，以及用户明确校准。
- 纠错链：A2 最初按用户要求压缩逐图重复 → 用户随后担心“集中说明一次”被误解为删除所有独立设置 → A2 回查当前文本并确认 Case-specific `C`、`\mathcal J_{10}`、4.75/4.65 ms 以及 `W_x/W_f/S_e(t)` 均保留 → TIE 图组组织与用户二次校准共同支持 → 最终含义严格限定为“同一 block 的共同信息集中，独有证据不删”。

### NC-07：当前压缩只删除重复论证，不删除必要证据

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 必须保留 Case-specific `C`、全部 `\(\mathcal J_{10}\)` 数值、4.75/4.65 ms。
- 必须保留 `\(W_x\)`、`\(W_f\)`、三个 `\(S_e(t)\)` 设置及两类图的关键结果。
- 可压缩的是重复的 purpose → setup → result → mini-conclusion 模板。

### NC-08：当前 Comment 1 的 computation-time 指标名称和符号已更名

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`；旧名称为 `SUPERSEDED`。
- 当前正式名称：`maximum online computation time per control step ($t_{\mathrm{comp}}^{\max}$)`。
- 当前判据：`$t_{\mathrm{comp}}^{\max}<\Delta t$`。
- 当前 Comment 1 正文与必要 captions 已统一。
- 纠错链：用户正式指定新名称与符号 → A2 在 Comment 1 首次定义并统一正文与必要 captions → 回查旧短语在 Comment 1 中为零 → 用户裁决与当前 TeX 支持 → 新名称只作为当前 Comment 1 的正式指标；可供后续抽象的仅是“指标定义稳定、判据明确”，且仍须三源裁决。

### NC-09：当前 Cases 1/2 结果句直接列出具体 Fig. 与 panel

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 被修正表达：`panels (c)`／`Panels (d)`。
- 当前写法直接列出 `Figs. 1(c) and 2(c)`、`Figs. 1(d) and 2(d)` 的 LaTeX 引用。
- 依据：TIE 原文倾向直接点出具体 Fig.，用户最后定点裁决。
- 纠错链：用户指出两个 figures 并列时只写 panels 会含糊 → A2 改为具体 figure-panel references → 复核目的为减少当前 reviewer 回读和错配 → 当前句子结构与用户裁决支持 → 不升级为“所有 response 必须逐一列完整 Fig. 编号”的通则。

### NC-10：当前 figures 的 caption／正文分工与 citation 取舍

- 状态：`NEW_CONFIRMED`；当前 caption citation 裁决同时为 `CASE_SPECIFIC`。
- caption 保留定义、参数、面板意义和虚线含义。
- 正文不机械复述 caption，而是读取 reviewer 需要判断的关键现象。
- 正文中首次引用 IL-SOGP 已有正确文献；caption 不需为形式统一重复添加 revised-manuscript `[10]` 或其他编号。
- 纠错链：用户要求 caption 自足但正文不要重复 → A2 保留 caption 内容并压缩正文 → 用户进一步明确当前 captions 不需机械重复 IL-SOGP 引用 → 当前 TeX 与用户裁决支持 → 只记录本项目的 citation 取舍，不形成所有期刊 caption 的引用规则。

### NC-11：当前结尾正面收束并限定到测试条件

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 被删除方向：`This conclusion does not imply minimum computation time...`
- 原因：免责声明式结尾重复防御，并引入新的 `minimum computation time` 术语。
- 当前结尾直接使用已建立的 real-time feasibility criterion，并限定于 two tested tasks 与 reported variations。

### NC-12：lattice-distributed RBFNN 首次出现需要 response 内正式来源

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 当前正文：`lattice-distributed RBFNN~\cite{respLiuTCYB2025} ([29] in the revised manuscript)`。
- response 末尾新增 C. Liu et al., IEEE Transactions on Cybernetics, 2025 的 bibliography item。
- `[29]` 是 revised manuscript 中已知对应关系；JAS 的 `[XX]` 仍不猜测。

### NC-13：当前允许的 claim 边界

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`；handoff 中更窄的“明确实时性只由 JAS Cases 收束”表述已被当前版本 `SUPERSEDED`，但仍保留为历史链。
- 可以说：在 two tested interaction tasks 与 reported `\(W_x\)`／`\(S_e(t)\)` variations 下，`\(t_{\mathrm{comp}}^{\max}<\Delta t\)`。
- 可以说：上述比较中 proposed 的 `\(\mathcal J_{10}\)` 低于 IL-SOGP。
- 必须同时保留：proposed 的 `\(t_{\mathrm{comp}}^{\max}\)` 一般高于 IL-SOGP。
- 不能说：proposed／fast-AGP 在所有方法、任务或平台上具有最低 computation time；不能给出普遍实时保证。
- 说明：handoff 的较窄表述强调 JAS Cases 是“不同任务”层面的明确实时性证据；本账号后续版本在用户验收下进一步明确，`\(W_x\)`／`\(S_e(t)\)` 图也可支持“所报设置下满足判据”，但不支持推广。
- 纠错链：handoff 先限制实时性收束于两个新增 Cases → A2 后续同时纳入 `W_x/S_e(t)` 的正式 computation-time 图 → 用户要求主线以所有 tested tasks/settings 的 `t_{\mathrm{comp}}^{\max}<\Delta t` 证据有限收束 → 正式图关系、当前 TeX 与用户最终裁决共同支持 → 现行 claim 只覆盖 tested/reported conditions；proposed time 一般高于 IL-SOGP 的不利事实必须保留，minimum computation time 与 universal guarantee 仍被排除。

### NC-14：`real-time feasibility criterion` 不加内部连字符

- 状态：`NEW_CONFIRMED`、`CASE_SPECIFIC`。
- 被修正表达：`real-time-feasibility criterion`。
- 当前表达：`real-time feasibility criterion`。
- 此为当前句子的定点语言裁决，不外推为所有复合定语的普遍标点规则。
- 纠错链：用户要求去掉当前短语中的内部连字符 → A2 定点替换 → 复核未发现需要借此改动其他文本 → 用户最终裁决支持 → 仅保存为当前句子的语言微调，不标记为 TIE 特有规则。

---

## 4. 用户在本账号中的具体问题、修改意见与标准校准

以下按出现顺序保存，均属于本账号 post-handoff 记录。

1. **不得推倒重来。**完整继承 handoff，并先说明理解到的状态，等待下一步。
2. **最高目标不是一般学术英语。**整体写作习惯和所有细节必须达到 TIE 范例所体现的 reviewer-response 水平。
3. **反馈不是孤立修改点。**应从用户具体反馈反推出完整表达标准，再审视全文。
4. **先验收后修改。**曾要求只报告问题与依据，不直接修改。
5. **对问题清单做证据复核。**每条必须区分资料明确支持、推断／泛化偏好、边界限制；不得新增标准。
6. **删除项不得回流。**后续修改只能采用裁决后成立的标准。
7. **受限项只在边界内处理。**不改正式图、不虚构 revised-manuscript 位置、不替换 `[XX]`。
8. **三类主要问题只是检查锚点。**实验进入、表达完整、术语稳定之外，仍需检查全文同类问题，但不改正确内容。
9. **先做减法。**全文只能围绕 computational-efficiency concern → criterion → evidence → bounded conclusion 的主线推进。
10. **首段与 Section 1 不重复判据。**Section 2 总起与 Cases 引入不重复宣布计划。
11. **四个实验单元不能复制同一完整模板。**Case 1/2、`W_x`、`S_e(t)` 需要高密度组织。
12. **结尾不重复枚举结果。**删除免责声明式新术语，由证据自然收束。
13. **首段要完整概括三类证据。**Cases 1/2、`W_x`、`S_e(t)` 都要可见。
14. **补 lattice-distributed RBFNN 正确来源。**同时保留稿件 `[29]` 对应关系。
15. **版本整体通过后只允许三处定点修改。**direct performed-comparison wording、明确 real-time feasibility、明确 original two-DOF task；修改后停止并编译。
16. **图相关正文仍需继续向 TIE 收敛。**按 evidence block 而非逐图 mini-response 组织。
17. **正式指标改为 `t_{\mathrm{comp}}^{\max}`。**第一次完整定义，后文用符号；判据固定为 `t_{\mathrm{comp}}^{\max}<\Delta t`。
18. **正文与 caption 分工。**caption 自足，正文只保留 reviewer 判断所需结果；不删必要定义，也不机械重复。
19. **设置集中说明只在 block 内适用。**不能删各 Case／variation 的不可替代设置、数值和结果。
20. **最后图号引用必须具体。**不用 `panels (c)`；直接写具体 Figs. 与 panels。
21. **最后术语微调。**使用 `real-time feasibility criterion`。
22. **不得为形式统一在 captions 重复加 IL-SOGP `[10]`。**正文首次出现处的引用足够。
23. **图文件由另一窗口处理。**本账号的 response 文字工作不得修改任何图文件。

---

## 5. `REJECTED`：不得包装为最终写作规则的内容

### 5.1 从 handoff 继承的已否定做法

以下由第一个账号记录并交接，本账号仅继承，不计作 A2 新发现：

- `REJECTED`：把用户反馈当作零散替换清单，只改被点名的几句话。
- `REJECTED`：把总结者写出的 `The point we wish to clarify...`／`We wish to clarify...` 当成 TIE 原文语言指纹。
- `REJECTED`：直接写 `We do not claim that...` 或 `The manuscript does not claim...` 与审稿人正面对抗。
- `REJECTED`：使用泛化 academic-English 元话语，如 `Our earlier wording did not clearly...`，代替研究动作和证据。
- `REJECTED`：创造或使用不正式术语 `full-GP`、`IEEE-JAS Case 1`、`stiffness-only task-cost curves`。
- `REJECTED`：把图号写成悬空括号附件。
- `REJECTED`：用 `Next, we vary...`、`Finally, we vary...` 等执行顺序代替论证目的。
- `REJECTED`：含糊使用 `its`、`this computation time` 等，让审稿人回读。
- `REJECTED`：漏掉外部方法的 response 引用，或只给 manuscript 编号。
- `REJECTED`：用 CRBFNN 神经元数、网络大小或跟踪误差充当 fast-AGP 运行时间证据。
- `REJECTED`：在 response 中堆计时代码、实现过程或无助于判据判断的旁注。
- `REJECTED`：把图文件名中的 `b:c` 当正式变量，或使用稿件未定义的 `S_{e,\max}`。
- `REJECTED`：用 JAS 资料反向设计本稿权重／刚度术语，或从源代码补 response 设置。
- `REJECTED`：JAS 设置过少到无法说明不同任务，或过多到复述 Methods。
- `REJECTED`：混淆 iteration convergence、per-step computational burden 与 real-time feasibility。
- `REJECTED`：写最低成本、普遍适用、普遍实时或 `guarantee` 等超证据结论。
- `REJECTED`：整体回退旧 Response，或把旧新版堆成更长回复。
- `REJECTED`：擅自换正式图或使用候选图。
- `REJECTED`：未完成验收即宣称已达到 TIE 水平。

### 5.2 本账号 post-handoff 新出现并被否决／纠正的做法

1. `REJECTED`：把一轮独立验收得到的 16 项全部当成确定规则。
   - 用户要求逐条回到 TIE、三份总结、JAS／稿件和既定要求复核。
   - 单纯“更专业”或“我推断 TIE 可能喜欢”不足以保留。

2. `REJECTED`：把 TIE 的个别用法泛化为硬规则。
   - 例如 `To further show...`／`To further verify...` 只能作为功能性进入的例子，不能机械复制四次。

3. `REJECTED`：把本轮三个主要问题锚点理解为修改上限。
   - 用户明确说三类问题只是主要发现和检查锚点；应检查同类问题，但仍不得新增未经确认的标准。

4. `REJECTED`、`CASE_SPECIFIC`：`we clarify the evaluation criterion and compare...`。
   - 原因：元话语；当前改为直接报告 comparisons 已完成。

5. `REJECTED`、`CASE_SPECIFIC`：`To further evaluate the criterion...`。
   - 原因：`the criterion` 在多指标语境下不明确；当前直接写 real-time feasibility。

6. `REJECTED`、`CASE_SPECIFIC`：`differ from those in the manuscript`。
   - 原因：参照对象模糊；当前点明 original two-DOF task。

7. `REJECTED`：首段／Section 1 重复解释 real-time criterion，Section 2 多次重复宣布后续实验。
   - 用户要求按单一主线做减法。

8. `REJECTED`、`CASE_SPECIFIC`：Case 1、Case 2、`W_x`、`S_e(t)` 各自重启一套 purpose → setup → result → mini-conclusion。
   - 当前改为两个 evidence blocks。

9. `REJECTED`、`CASE_SPECIFIC`：结尾使用 `This conclusion does not imply minimum computation time...`。
   - 原因：免责声明式、引入新术语、重复防御。

10. `SUPERSEDED`、`CASE_SPECIFIC`：当前项目早期使用的正式名称 `maximum total computation time per step`。
    - 用户已正式指定新名称与符号；旧名称并非一般意义上的错误术语，但在当前 Comment 1 中已失效，仅保留为历史证据。

11. `REJECTED`、`CASE_SPECIFIC`：把“公共设置集中一次”解释为整个 Section 2 只能出现一次设置说明。
    - 正确裁决只适用于同一 evidence block 的共同信息；不可替代设置与结果必须保留。

12. `REJECTED`、`CASE_SPECIFIC`：在当前 Cases 1/2 结果句中用 `panels (c)`／`Panels (d)` 概括两个不同 figures 的面板。
    - 当前改为逐一列出具体 figure references。

13. `REJECTED`、`CASE_SPECIFIC`：当前句子中的 `real-time-feasibility criterion`。
    - 当前定点改为 `real-time feasibility criterion`。

14. `REJECTED`、`CASE_SPECIFIC`：为了“引用统一”在当前 captions 中重复给 IL-SOGP 添加 revised-manuscript `[10]` 或类似编号。
    - 用户明确否决；正文首次出现的引用足够。

15. `REJECTED`：在当前版本已通过整体内容／逻辑／表达验收后继续泛化式润色。
    - 后续只允许用户指定的定点修改。

---

## 6. 经原始资料或验收确认的证据映射

### 6.1 TIE PDF 直接确认

- R1-2：一个 robustness-tests block 中统一交代多个噪声强度、公共条件、图组结果和一次性结论。
- R3-2：新增 comparisons 先统一说明比较对象与目的，再以图组读取 reviewer 所需差异。
- R4-3：真实机器人实验按“补了什么 → 平台／轨迹 → 图中结果 → 有限结论”推进。
- 确认事项：TIE 原文支持把相关 tests/comparisons 作为连续证据组推进、在图组附近直接读结果、先报告行动并有限收束。当前两-block 分组方式仍是 `CASE_SPECIFIC` 的项目应用。
- 未确认事项：不能把这些 comment 中任何单一句式提升为所有实验回复的固定模板。

### 6.2 三份总结确认

- `Response_写作规则.md`：直接答案、可检查证据链、比较对象／指标／条件／范围、图文扫读性、最小充分。
- `Response_表达范式.md`：感谢后转具体动作；`According to your suggestion` 等只能按功能少量使用；其中 `The point we wish to clarify...` 被明确标为项目增强而非 TIE 原句。
- `TIE范例_逐条拆解.md`：R1-2、R3-2、R4-3 的原始结构观察，以及 R4-4 “相近证据不能替代原问题”的反例。
- 职责边界：三份总结用于辅助定位、结构诊断和识别“不照搬”事项，不能替代 TIE PDF 对作者实际措辞和推进方式的直接核验。

### 6.3 JAS 原论文确认

- 论文题目：`Robot Impedance Iterative Learning with Sparse Online Gaussian Process`。
- Case 1 为 accurate tracking，`\(\alpha=10\)`、`\(C=[25,0,1]\)`。
- Case 2 为 compliant interaction，`\(\alpha=20\)`、`\(C=[100,0,0.1]\)`。
- 使用 Franka Emika Panda；outer-loop sampling delay 为 10 ms。
- JAS 只确认 Cases 的事实与命名，不决定 TCYB response 的英文风格，也不决定本稿 `W_x/W_f/S_e(t)` 的术语。
- JAS 不包含本项目新增 proposed-method comparison figures 中的全部 `\mathcal J_{10}` 和 `t_{\mathrm{comp}}^{\max}` 数值；这些结果须回到最终正式结果图，不能由 JAS 替代。

### 6.4 当前稿件确认

- `S=[W_x\;0\;W_f]`，`W_x` 与 `W_f` 分别对应 tracking 与 force-integral terms。
- 环境刚度使用 `S_e(t)`。
- 稿件原有运行时间段给出 proposed 9.90 ms、`\(\Delta t=20\)` ms，以及 standard GP 超过 control interval 的事实。
- lattice-distributed RBFNN 在稿件中对应文献 `[29]`。

### 6.5 最终正式结果图确认

- `CASE_SPECIFIC`：Case 1/2 的 task-cost 与 online-computation-time figures 是新增比较数值、曲线关系和控制周期虚线的直接图形证据。
- `CASE_SPECIFIC`：`W_x`／`S_e(t)` figures 是不同 reported variations 下 `\mathcal J_{10}` 比较、proposed 相对 IL-SOGP 的 computation-time 关系以及 `t_{\mathrm{comp}}^{\max}<\Delta t` 的直接图形证据。
- 职责边界：图负责新增比较的数值与可见关系；JAS 负责 Cases 的原始任务定义；当前稿件负责本稿正式变量和既有事实。三者不能互相替代。
- 完成边界：A2 没有修改图文件；图文件最终替换与视觉状态由另一窗口处理，仍保留在 `UNRESOLVED`。

### 6.6 用户原始对话与实际验收确认

- post-handoff 原始对话是用户要求、纠正、适用范围和最终裁决的直接来源。
- 当前版本在 A2-05 前已被用户明确判断为“整体已经通过内容、逻辑和表达验收”。
- 后续修改范围被严格限缩为用户点名的术语、图引用与 evidence-block 组织问题。
- 对 evidence-block 必要证据保留的复查结果为“当前版本符合，无需修改”。
- 职责边界：用户裁决能确定当前项目如何处理，但不能单独证明某写法是 TIE 的普遍习惯；涉及 TIE 风格的判断仍需回到 TIE PDF。

---

## 7. `CASE_SPECIFIC`：当前版本已确认正确的部分

本节全部条目只描述当前 Comment 1 的已确认状态，不是通用 reviewer-response 规则。

1. 保留两个编号部分：
   - `1) Computational objective and evaluation criteria.`
   - `2) Additional comparisons under different tasks and settings.`
2. 首段承认上一版证据缺口，并直接报告三类 comparisons 已完成。
3. ILC 跨迭代 task cost 与每 control step 在线计算的认知框架完整。
4. 判据明确为 `\(t_{\mathrm{comp}}^{\max}<\Delta t\)`。
5. fast-AGP／GP 与 CRBFNN／lattice-distributed RBFNN 的比较口径清楚。
6. lattice-distributed RBFNN 已有 response 引用与 `[29]` 对应关系。
7. Cases 1/2 作为一个 evidence block，公共设置集中、特有设置和数值完整。
8. `W_x/S_e(t)` 作为一个 evidence block，两类变量设置和关键结果完整。
9. proposed 的 computation time 高于 IL-SOGP 的事实没有被删除或弱化。
10. 正文使用具体 Figs. 与 panel references，不再使用 `panels (c)` 等模糊表达。
11. captions 保持自足，没有为形式统一重复添加 IL-SOGP manuscript 编号。
12. 结尾只收束一次，使用 `real-time feasibility criterion`，并限定到测试条件。
13. 图文件、实验、数值、两个部分结构及 Comment 1 之外的内容未在本轮文字修改中改变。
14. 未虚构 revised-manuscript 页码、行号或 Section 位置；这一项是当前项目边界已被遵守，不属于待解决问题。

---

## 8. `UNRESOLVED`：当前仍不能作为正式规则或完成状态的事项

1. **`[XX]` 未处理。**
   - 当前为 `IL-SOGP~\cite{respPanJAS2025} ([XX] in the revised manuscript)`。
   - 这是用户明确要求保留的占位符，最终编号需作者提供。

2. **当前 TeX 与 PDF 再次不同步。**
   - 当前 `Response-TCYB.tex` 修改时间晚于 `Response-TCYB.pdf`。
   - 15 页成功编译对应 A2-05 状态；之后进行了 Section 2 evidence-block 重组、指标更名、具体 figure references 和连字符修正。
   - 用户后续未要求编译，因此当前 PDF 不能作为最新版文字的版面证据。

3. **最新版尚未做编译后视觉验收。**
   - 未检查新增长指标名称在 subcaption 中的换行、分页或图文距离。
   - 本项是交付状态，不是语言问题，也不能据此继续擅自改写。

4. **16 项问题清单的逐条原文不可完整恢复。**
   - 当前对话压缩记录保存了用户要求的分类方法与后续裁决结果，但没有保存助手当时列出的 16 项全文和逐项分类答复。
   - 不得凭推测重新创建“第 1–16 条”并声称是历史原文。

5. **其他窗口处理的图文件状态不在本记录中验收。**
   - 本账号遵守“不修改任何图文件”。
   - 图文件内部新旧标记、最终替换状态由另一窗口负责，不能从本账号 response 文本工作中推断完成。

---

## 9. 当前最终边界快照

- 当前主文件：`D:\桌面\科研_response\ilc优化版_tcyb\第三轮\response_TCYB2\Response-TCYB.tex`
- 当前 Comment 1 大致位于 TeX 第 207–342 行，以审稿意见 `The authors did not respond well...` 和下一项 `\item[2.]` 为边界；行号会随编辑变化。
- 当前正式指标：`maximum online computation time per control step ($t_{\mathrm{comp}}^{\max}$)`。
- 当前判据：`$t_{\mathrm{comp}}^{\max}<\Delta t$`。
- 当前结构：两个编号部分、两个 Section 2 evidence blocks、一次有限结论。
- 当前可接受 claim：仅覆盖测试的 interaction tasks 与 reported `W_x/S_e(t)` variations。
- 当前不得做：替换 `[XX]`、修改图文件、重写正确内容、扩展到其他 Comments、增加未经确认的规则或结论。
- 状态：本节整体为 `CASE_SPECIFIC`；旧指标名称和旧窄结论边界仅以 `SUPERSEDED` 历史存在。

---

## 10. 供后续知识库整理者使用的保真提示

1. `INHERITED_CONFIRMED` 与 `NEW_CONFIRMED` 不可合并计数为两套独立发现。
2. 本文中的具体当前句子是项目决策证据，不自动成为跨项目固定模板。
3. `REJECTED` 只用于记录错误路径和防止回流，不能抽取为正向规则。
4. `UNRESOLVED` 不能通过“合理猜测”补全。
5. 可提交给三源交叉裁决的候选抽象点主要集中在：
   - evidence block 而非逐图 mini-response；
   - 公共设置集中与特有证据保留的同时成立；
   - 正文／caption 的证据分工；
   - 指标定义稳定、判据明确；当前具体名称 `t_{\mathrm{comp}}^{\max}` 仍为 `CASE_SPECIFIC`；
   - 降低图号歧义和 reviewer 回读成本；当前逐一列出具体 figures 仍为 `CASE_SPECIFIC`；
   - 已通过整体验收后停止泛化式润色。
6. 上述仅为候选，不是已经可迁移的规则。后续必须再次回到 TIE 原文、用户对话与来源索引做三源裁决，不能仅从本记录中的英文例句反推。

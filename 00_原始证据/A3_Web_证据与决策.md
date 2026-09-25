# A3 Web：Comment 1 response 与 TIE 写作标准形成的原始证据与决策记录

> 用途：保真保存当前网页版 ChatGPT 对话中，与 TCYB 第三轮 Comment 1 response、TIE 范例学习、reviewer-response 写作标准形成有关的用户要求、模型判断、纠正、否决、证据核对和最终裁决。
>
> 本文不是最终知识库，不与 A1/A2 合并，不主动去重，也不把所有用户偏好直接泛化成通用规则。
>
> 本文只记录当前网页版对话可恢复的内容；A1/A2 不作为本文件的替代来源，也不用于填补当前网页对话中不存在的历史。

## 0. 状态定义

- `CONFIRMED`：已经由用户最终确认，或经当前网页版对话中实际核对的 TIE 原文、response 文件、JAS 原论文、稿件/正式符号等支持。
- `REJECTED`：曾由 ChatGPT/Codex 建议、解释或采用，但随后被用户否决，或重新回到 TIE/事实来源核验后证明不是应保留的判断。
- `UNRESOLVED`：在当前网页版对话中仍缺少最终裁决、最终版本或充分证据，不能写成正式规则。
- `CASE_SPECIFIC`：当前 Comment 1、当前 reviewer、当前图或当前稿件的具体事实/处理，不能直接泛化为顶刊 reviewer response 通则。
- `SUPERSEDED`：曾经是阶段性要求，但后续被用户或重新核验后的裁决替代。最终知识库不得把旧版本与新版本并列为同时有效规则。

---

## 1. 当前网页版对话中的总目标与最高优先级

### 1.1 `CONFIRMED`：目标不是“普通学术英语正确”，而是与 TIE 范例的实际写法对齐

用户反复强调，Comment 1 的验收标准不是语法正确、流畅或“看起来专业”，而是：

- 回应逻辑；
- 信息组织；
- 句法节奏；
- 措辞和语气；
- 术语与符号；
- 实验进入方式；
- 结果图写法；
- 图文关系；
- claim 边界；
- 结论收束方式；

都要尽可能达到 TIE 范例作者实际 reviewer-response 写作所体现的水平。

用户进一步指出：某个具体短语被点名只是暴露了一个更大的标准问题。不能把反馈理解成“只改这一句”，而应把它视为对整篇 response 写作标准的校准。

### 1.2 `CONFIRMED`：TIE 原文高于模型自行补充的一般 academic-writing 偏好

当前网页版对话中多次出现同一流程：

1. ChatGPT 提出一个看似更规范、更专业或更完整的写法；
2. 用户要求“不要凭一般写作经验，回到 TIE 范例本身核验”；
3. 再核验后发现该建议并非 TIE 的必要特征，有时甚至与用户要模仿的 TIE 风格冲突；
4. 该建议被撤回或降级为非必须项。

因此当前网页对话形成了一个非常重要的来源纪律：

> “更规范的 academic English”不能自动升级为“与 TIE 对齐的必须规则”。

### 1.3 `CONFIRMED`：TIE 可迁移的是写作机制，不是错误、偶然句式或机械模板

当前对话最终反复确认：

- 学习 TIE 的信息密度、段落动作、证据位置、读图方式和结论收束；
- 不机械复制固定连接词；
- 不复制 TIE 自身可能存在的语法错误、拼写错误或过强 claim；
- 不把某一条 Comment 中偶然出现的一种句型升级为所有 response 的硬规则。

---

## 2. 用户具体反馈不是“点状修改”，而是标准校准

### 2.1 `CONFIRMED`：`we wish to clarify` 是一个校准案例，不是孤立替换

网页版讨论中，用户明确指出当前 response 中出现类似 `we wish to clarify` 的写法，与 TIE 范例的实际语言习惯不一致。

用户真正表达的不是“只删这几个词”，而是：

- 不要用泛化的 meta-writing 告诉 reviewer “我们要澄清什么”；
- 更接近 TIE 的做法是直接进入作者采取的动作、事实、证据或实验；
- 应回查全文所有类似“作者谈自己正在写什么”的元话语。

`REJECTED`：把 `we wish to clarify`、`The point we wish to clarify...` 等当作 TIE 的语言指纹。

### 2.2 `REJECTED`：把用户列出的几个问题当作完整修改清单

用户多次指出类似：

- `we wish to clarify`
- `do not claim`
- `for the original task`
- `its`
- `for the same task`

这些例子只是用户“扫一眼就能发现”的显性问题，不能说明只需修改这些地方。

后续形成的正确理解是：

> 具体例子用于反推完整标准，再用该标准审查同类表达，而不是逐条打补丁。

### 2.3 `CONFIRMED`：逐句审计与“不要重写正确内容”必须同时成立

当前对话形成了两个同时成立的约束：

- 必须从全文和各类细节检查是否与 TIE 对齐；
- 一旦某一部分已经通过验收，不得因为 Agent 又想到一个“更专业”的表达就继续泛化式润色。

因此“全面审计”不等于“全面重写”。

---

## 3. Comment 1 的主论证线与内容边界

### 3.1 `CASE_SPECIFIC / CONFIRMED`：当前 Comment 1 的主线

用户最终确认的核心链条是：

> reviewer 质疑 computational-efficiency 结论在不同任务/设置下是否成立  
> → 明确真正的在线实时判据  
> → 区分 task-cost convergence 与 per-control-step online computation  
> → 补充不同 interaction tasks 与不同 settings 下的 task cost + computation-time 证据  
> → 如实保留 proposed method 相对 IL-SOGP 的不利 computation-time 比较  
> → 只在已测试条件内形成有限的 real-time-feasibility 结论。

### 3.2 `CONFIRMED`：不能把“更少迭代”偷换成“更低单步计算成本”

用户要求保持最小认知框架：

- iteration level：`\(\mathcal J_j\)` 用于观察跨迭代 convergence；
- control-step level：每步在线计算必须在 control period `\(\Delta t\)` 内完成；
- “accelerated convergence”不能直接推出“per-step computation 更低”。

### 3.3 `CASE_SPECIFIC / CONFIRMED`：计算负担 claim 的比较对象必须明确

当前项目中：

- fast-AGP 的 reduced computational burden 是相对 standard GP；
- CRBFNN 的 reduced computational burden 是相对 lattice-distributed RBFNN；
- 不能把这些比较扩大成“proposed method 相对 IL-SOGP 或所有方法具有最低 computation time”。

### 3.4 `CONFIRMED`：不利证据不能被隐藏

在 Cases 1/2 以及后续 variations 中，proposed method 的 computation time 可以高于 IL-SOGP。

用户与网页版对话最终坚持：

- 这类事实应如实保留；
- response 的目标不是证明“最低计算成本”；
- 真实证据比防御性包装更重要。

---

## 4. TIE 范例中结果图/新增实验的真实组织方式

### 4.1 `CONFIRMED`：用户最终认可的核心模式

网页版对话围绕 TIE 的以下三处进行了反复核验：

- Referee No. 1 – Comment 2；
- Referee No. 3 – Comment 2；
- Referee No. 4 – Comment 3。

最终确认的共同特征不是某个固定句子，而是：

> 统一说明为什么补实验/比较  
> → 给必要实验设置  
> → 相关图作为一个证据组进入  
> → 直接指出 reviewer 真正需要看到的关键现象  
> → 一次性得到有限结论。

### 4.2 `CONFIRMED`：evidence block 解决的是“重复论证”，不是“删除必要证据”

用户特别校准：

> “不要把‘实验目的和设置集中交代一次’理解为整个 Section 2 只能出现一次设置说明。”

正确理解是：

- 同一 evidence block 内，共同目的和公共设置集中交代；
- 不同实验不可替代的设置、数值和结果仍必须保留；
- 压缩的是重复的 `purpose → setup → result → mini-conclusion` 模板，而不是必要证据。

### 4.3 `CASE_SPECIFIC / CONFIRMED`：当前 Section 2 的两个 evidence blocks

当前 Comment 1 最终采用：

1. Cases 1/2 作为一个 evidence block；
2. `\(W_x\)` 与 `\(S_e(t)\)` variations 作为第二个 evidence block。

这是当前项目的最佳组织，不应直接泛化成“所有 response 都必须分成两个 evidence blocks”。

### 4.4 `REJECTED`：每张图各写一套完整 mini-response

用户明确认为以下做法造成啰嗦和主线松散：

- Case 1：目的—设置—结果—结论；
- Case 2：再来一次；
- `W_x`：再来一次；
- `S_e(t)`：再来一次；
- 最后又整体总结一次。

当前对话最终将其压缩成两个证据组，并只做一次自然结论收束。

---

## 5. Caption、正文与结果图的分工

### 5.1 `CONFIRMED`：caption 自足，不等于正文机械复述 caption

当前网页讨论最终确认：

- caption 应让图在脱离正文时仍可识别方法、条件、指标/面板含义和必要参考线；
- 正文只提 reviewer 作判断真正需要的关键结果；
- caption 和正文承担不同功能，因此不能通过删除 caption 的必要信息来“压缩”。

### 5.2 `CONFIRMED`：正文必须读图，而不是只挂图号

被否决的写法包括：

- 句末悬空 `(Fig. ... )`；
- 只有图号、没有说明图显示了什么；
- 模糊的 `panels (c)` / `Panels (d)` 在两个不同 figures 并列时要求 reviewer 自己回找。

当前项目后续将其定点改为：

- `Figs. 1(c) and 2(c)`；
- `Figs. 1(d) and 2(d)`。

### 5.3 `CASE_SPECIFIC / CONFIRMED`：当前 reviewer 的扫读路径影响信息位置

当前项目中，用户认为 reviewer 主要关注：

- 正式结果图；
- caption；
- 图前后几句；
- computational-cost claim 是否严谨。

因此当前 response 要把核心判据、关键数值和 claim 边界放在 reviewer 扫图时能看到的位置。

这属于当前 reviewer 的项目级阅读假设，不应未经证据泛化成“所有 reviewer 都这样读”。

---

## 6. 实验设置：最小充分，而不是“越多越完整”

### 6.1 `CONFIRMED`：不同任务必须让 reviewer 看得出“真的不同”

用户不接受只写 `Cases 1 and 2` 而不给必要差异，因为 reviewer 的原始质疑正是“仅变化 stiffness 不算充分不同的 task/setup”。

因此 Cases 1/2 需要保留足以说明任务性质不同的设置。

### 6.2 `CONFIRMED`：但不能复述 JAS Methods

网页版对话同时明确：

- JAS 用于核实 Case 1/2 的任务、平台、`C`、控制周期等事实；
- 不需要把机器人模型、环境方程、核参数和全部控制参数搬入 response；
- 信息密度必须服务于 reviewer 的判断，而不是证明作者“掌握了很多设置”。

### 6.3 `CONFIRMED`：不能从源代码补 response 设置

用户明确要求实验设置从：

- JAS 原论文；
- 当前稿件；

核对。

`REJECTED`：

- 从源代码；
- 绘图脚本；
- 运行日志；
- 临时代码变量；

补充 response 中的实验事实、术语或设置。

---

## 7. 术语、变量与符号

### 7.1 `CONFIRMED`：变量应使用稿件正式定义，不用图文件名或临时代号

当前网页版对话确认：

- `b:c` 不是 response 的正式变量；
- 应使用 `\(W_x:W_f\)`；
- environment stiffness 使用 `\(S_e(t)\)`；
- 不使用未在稿件正式定义的 `\(S_{e,\max}\)`；
- 当前图中使用 `\(I\)`，不使用 `\(I_2\)`。

### 7.2 `CONFIRMED`：变量名称与符号在关键位置同时明确

用户多次要求：

- 不要只写一个裸符号；
- 也不要只写一个泛化名词；
- 关键指标第一次出现时，应让 reviewer 同时知道“它是什么”和“它的符号是什么”。

但当前对话也确认：

> 完整不等于每一句都机械重复长名称和完整定义。

### 7.3 `CONFIRMED`：computation-time 正式指标最终统一为

`maximum online computation time per control step \(t_{\mathrm{comp}}^{\max}\)`

判据：

`\[
t_{\mathrm{comp}}^{\max}<\Delta t.
\]`

### 7.4 `SUPERSEDED`：`T_{\mathrm{on}}^{\max}`

网页版对话中 ChatGPT 一度建议使用 `\(T_{\mathrm{on}}^{\max}\)`。

后续用户认为应加正式符号，经过继续讨论和实际图/正文统一，最终项目采用：

`\(t_{\mathrm{comp}}^{\max}\)`。

因此 `T_{\mathrm{on}}^{\max}` 只能作为历史候选，不能写入最终知识库规则。

### 7.5 `REJECTED`：旧短语 `maximum total computation time per step`

用户最终要求统一为 `maximum online computation time per control step`，因为它直接对应实时在线计算的真实评价对象。

---

## 8. 模糊代词与指代

### 8.1 `CONFIRMED`：问题不是“禁止代词”，而是避免让 reviewer 回读

用户曾点名：

- `its`
- `this computation time`
- `the criterion`
- `those in the manuscript`
- `weight settings`
- `environment stiffness settings`

当前对话最终形成的更准确判断是：

> 当一个句子附近同时存在多个方法、指标、实验对象或先行项时，不要依赖模糊代词/泛化名词让 reviewer 回读定位。

### 8.2 `REJECTED`：把“不要含糊代词”泛化成“永远不能用代词”

这不是用户要求，也不是 TIE 规则。

问题是认知负担和歧义，而不是代词本身。

---

## 9. 首段、目的句和元话语

### 9.1 `CONFIRMED`：首段应优先报告做了什么和主要证据，而不是描述写作动作

当前网页对话最终认可：

- `comparisons ... have been conducted` 比 `we clarify the evaluation criterion and compare...` 更符合当前 TIE 对齐目标；
- reviewer 首先要看到作者采取了什么研究动作和补了什么证据。

### 9.2 `REJECTED`：`we clarify...` / `we wish to clarify...` 作为常规开段

原因：

- 容易变成 meta-writing；
- 与用户指定的 TIE 实际写法不匹配；
- 占用最宝贵的首段注意力。

### 9.3 `CONFIRMED`：目的句有用，但不能每组图重复启动

TIE 中确实有：

- `To further show...`
- `To further verify...`

等目的性进入。

但网页版最终确认：

- 迁移的是“让 reviewer 知道这组证据为什么存在”的功能；
- 不能把这些句型当作每个实验都必须重复的模板。

---

## 10. Claim 边界与结论收束

### 10.1 `CONFIRMED`：结论强度必须与已测证据范围一致

当前项目可支持：

- 在已测试的 interaction tasks；
- 已报告的 `\(W_x\)` / `\(S_e(t)\)` variations；
- 对应 control period；

下验证 `\(t_{\mathrm{comp}}^{\max}<\Delta t\)`。

不能自动扩成：

- 所有任务；
- 所有硬件；
- 所有采样周期；
- 相对所有方法最低 computation time；
- 普遍 real-time guarantee。

### 10.2 `REJECTED`：免责声明式结尾重复防御

曾出现类似：

`This conclusion does not imply minimum computation time...`

后续被删除。

原因：

- 已经在正文中限定了 claim；
- 结尾再次防御会稀释证据主线；
- 引入 `minimum computation time` 这一新术语；
- 不像 TIE 的自然收束节奏。

### 10.3 `CONFIRMED`：结尾应由证据自然推出，一次收束

用户希望结尾表现为：

- 正面；
- 简洁；
- 有限；
- 不再重新枚举所有图和数值；
- 不额外开启新的防御话题。

---

## 11. ChatGPT 曾经提出、后被重新核验否决/降级的建议

这一节是 A3 最重要的历史证据之一，因为它直接区分“真正的 TIE 规律”与“模型自行补充的 academic-writing 偏好”。

### 11.1 `REJECTED`：caption 中所有 `IL-SOGP` 都必须重复加 `[10]`

阶段性判断：

ChatGPT 曾在图/全局审计中认为：

- caption 中出现 `IL-SOGP` 就应重复带 `[10]`；
- 未重复引用属于未通过项。

用户随后追问：

> “核心点是与范例 TIE 对齐，这些细节是要改的吗？”

重新回到 TIE 原文后，ChatGPT 修正：

- TIE 会在正文首次介绍比较方法时给引用；
- 后续 caption/图不必为了形式统一机械重复文献号；
- “caption 每次重复引用”不是 TIE 对齐的必要规则。

最终状态：

`REJECTED` 作为通用 TIE 规则。

注意：当前项目图内是否固定显示 `[10]` 是独立的 `CASE_SPECIFIC` 图形决定，不能反向推出“所有 caption 必须重复引用”。

### 11.2 `REJECTED`：把一般 academic-English 微调当作 TIE 风格硬标准

例如 ChatGPT 曾把：

`real-time-feasibility criterion`

改为：

`real-time feasibility criterion`

这是合理的英语微调，用户也接受了当前句子的修改。

但重新核验后明确：

- 这是当前句子的语言准确性处理；
- 不能把它包装成“TIE 特有写作规则”。

最终状态：

`CASE_SPECIFIC / CONFIRMED` 当前句子修改；
`REJECTED` 作为 TIE 通用规则。

### 11.3 `CONFIRMED`：具体 Fig. 引用更清楚，但不能过度泛化

ChatGPT 曾提出将：

- `panels (c)`
- `Panels (d)`

改为：

- `Figs. 1(c) and 2(c)`
- `Figs. 1(d) and 2(d)`

重新对照 TIE 后发现，TIE 在多图讨论时确实常直接点明具体 Fig.。

最终用户接受这一处定点修改。

但这应理解为：

- 当存在多个 figures/panels，模糊 panel 引用增加回读成本时，直接点图号更适合当前文本；
- 不是“所有结果句都必须逐一重复完整 Fig. 编号”的机械规则。

### 11.4 `REJECTED`：只要是“更专业”的写法就应该改

这是网页版对话中最重要的模型错误模式之一。

用户最终要求：

> 一旦当前内容已经正确并通过 TIE 对齐验收，不要因为模型又想到一个一般性的专业写法就继续修改。

---

## 12. 当前 Comment 1 图形相关的项目级决策

本节为 `CASE_SPECIFIC`，用于保存历史，不应直接进入通用写作规则。

### 12.1 Figure 3

- 图内 `b:c` 改为 `\(W_x:W_f\)`；
- 三组条件为 `20:1 / 50:1 / 200:1`；
- task-cost row 与 timing row 条件标注一致；
- timing plots 右上角显示对应 weight condition。

### 12.2 Figure 4

- `S_e` 改为 `\(S_e(t)\)`；
- `I_2` 改为 `\(I\)`；
- 三组 stiffness expressions 保持与稿件正式符号一致；
- timing plots 右上角重复对应 stiffness condition。

### 12.3 Timing metric

- y-axis/指标最终采用 `\(t_{\mathrm{comp}}^{\max}\)`；
- 正式语义为 maximum online computation time per control step；
- 不再使用 `total`。

### 12.4 图文件修改边界

用户要求：

- 不改数据；
- 不改曲线；
- 不改轴范围；
- 不改实验关系；
- 不因样式调整引入新内容；
- 图修改与 response 正文修改可在不同窗口执行，互不越界。

---

## 13. 当前网页版关于“什么属于 TIE 风格”的最终分层

### 13.1 `CONFIRMED`：高置信度 TIE-native 特征

- 感谢后快速进入具体研究动作；
- concern 与对应证据直接匹配；
- 实验目的/必要设置/结果/结论形成紧凑链；
- 相关图作为证据组，而非每图重启整套论证；
- 图附近直接读 reviewer 真正关心的现象；
- 结论一次性收束；
- 信息密度高；
- 少用泛化元话语；
- 不让读者频繁回读寻找比较对象、指标或先行项；
- 新增证据的范围和 claim 边界相互匹配。

### 13.2 `CONFIRMED`：TIE-inspired，但需要项目情境决定

- 是否使用编号 `1)` / `2)`；
- 保留多少实验设置；
- 是否具体列出每个 Fig./panel；
- 首段概括到什么粒度；
- caption 中需要重复哪些信息。

### 13.3 `REJECTED`：不能因为“看起来更规范”就归入 TIE 风格

- 所有 caption 都重复文献；
- 所有结果段都必须用固定 `To further...`；
- 所有图都必须用固定 `As shown...`；
- 所有变量每次出现都重复完整定义；
- 所有 response 都必须采用同一种段落长度；
- 一般 academic phrasebook 自动高于 TIE 原文。

---

## 14. 当前网页版中关于 Nature Skill / Academic Research Suite 的定位

### 14.1 `CONFIRMED`：可以吸收，但不能覆盖 TIE

用户后续规划知识库时明确希望吸收：

- Nature Skill；
- Academic Research Suite；

中成熟且不与 TIE 冲突的原则。

当前网页版形成的优先级思想是：

1. TIE 原文：核心表达/组织风格基准；
2. 用户在真实修改中的最终裁决：用于校准如何迁移 TIE；
3. JAS/稿件/正式结果：事实、符号和证据来源；
4. Nature Skill / Academic Research Suite：补充 claim discipline、source discipline、consistency/QA 等；
5. 若外部 Skill 的通用写法与 TIE 实际风格冲突，不采用其表达层建议。

### 14.2 `UNRESOLVED`

当前网页版尚未正式完成 Nature Skill / Academic Research Suite 与 TIE 规则的系统兼容性筛选。

因此此部分只能记录未来知识库的整合原则，不能提前写成最终知识条目。

---

## 15. 当前网页版中形成的错误模式清单

### 15.1 `REJECTED`：只修表面词句

只把用户点名表达替换掉，而不检查同类问题。

### 15.2 `REJECTED`：把具体例子升级为硬规则

例如看到 TIE 一次使用 `To further show...`，就要求所有实验都这样开头。

### 15.3 `REJECTED`：模型自行添加“更规范”细节

不经过 TIE 核验，就把一般 academic-writing 偏好当成必须修改项。

### 15.4 `REJECTED`：为了简洁删除必要证据

把 evidence block 压缩误解成删掉 Case-specific 设置、数值和不利结果。

### 15.5 `REJECTED`：为了完整机械重复

变量、指标、caption、purpose、结论在多个位置重复同一内容。

### 15.6 `REJECTED`：把 reviewer concern 改写成作者想回答的另一个问题

例如用 robustness、network size 或 implementation detail 替代 computational-efficiency concern。

### 15.7 `REJECTED`：把当前项目的特例误写成通用顶刊标准

例如：
- 当前 reviewer 的扫图习惯；
- 当前 Comment 1 的两个 evidence blocks；
- 当前图的具体符号；
- 当前 caption 的文献处理。

---

## 16. 可迁移与不可直接泛化的边界

### 16.1 `CONFIRMED`：高层机制可迁移

可以进入后续裁决池的候选包括：

- concern → direct response action → evidence → bounded conclusion；
- 证据与 claim 一一对应；
- evidence block；
- 最小充分设置；
- 图旁关键读图句；
- 明确比较对象、指标、条件和范围；
- 不用元话语代替研究动作；
- 不用模糊指代增加 reviewer 回读；
- 结论强度不超过证据。

### 16.2 `CASE_SPECIFIC`：必须保留为当前项目事实

- `\(t_{\mathrm{comp}}^{\max}\)`；
- `\(\mathcal J_{10}\)` 的具体数值；
- Panda / Case 1 / Case 2；
- `\(W_x\)` / `\(W_f\)` / `\(S_e(t)\)`；
- 10 ms / 20 ms；
- Fig. 1–4 的具体 panel；
- `[XX]`；
- IL-SOGP 当前稿件/response 的具体引用编号。

---

## 17. 当前仍未解决、不能进入最终规则的事项

### 17.1 `UNRESOLVED`：`[XX]`

当前用户明确要求先不处理。

这是最终提交/编号问题，不属于 TIE 风格知识。

### 17.2 `UNRESOLVED`：A1/A2/A3 尚未交叉裁决

当前 A3 只保存网页版历史。

不能因为 A3 中某条被写成 `CONFIRMED`，就自动认为它应进入最终知识库；后续还需要：

- 与 A1/A2 比对；
- 回到原始来源；
- 合并同义项；
- 解决冲突；
- 区分通用规则与项目特例。

### 17.3 `UNRESOLVED`：Nature / Academic Research Suite 的正式吸收范围

尚未执行系统兼容性过滤。

---

## 18. 当前网页版证据中最关键的因果链

1. 用户不断否决“只改被点名句子”，因为这些句子只是暴露完整风格标准的样本。
2. 用户不断要求回到 TIE 原文，因为模型倾向用一般 academic-writing 偏好填充空白。
3. 结果图写法最终转向 evidence block，是因为原版本对 Case 1、Case 2、`W_x`、`S_e(t)` 重复启动相同论证，降低信息密度。
4. evidence block 不能删必要设置，是因为 reviewer 必须确认两个 tasks/settings 的差异真实存在。
5. computation-time 指标必须明确为 per-control-step online metric，是因为 reviewer 的原关切不能由 iteration-level task cost 回答。
6. 不利的 IL-SOGP timing comparison必须保留，是因为当前 response 的目标是证明有限实时可行性，而不是制造“最低计算成本”结论。
7. caption 自足但正文不复述，是因为 reviewer 需要快速扫图，同时正文还必须保持高信息密度。
8. 不能强制 caption 重复引用，是因为重新对照 TIE 后发现这是模型自行增加的规范偏好，而不是 TIE 的实际必要特征。
9. 最后停止泛化式润色，是因为此前反复发生“模型新增一个看似专业的要求 → 用户回到 TIE 核验 → 发现并非必要”的循环。
10. 因此未来知识库最重要的能力之一，不只是“会生成好句子”，而是“知道什么不能被模型自行升级为规则”。

---

## 19. 本文件的边界

- 本文不与 A1/A2 合并。
- 本文不做三源去重。
- 本文不决定最终知识库文件结构。
- 本文不把当前 Comment 1 英文当作通用范文。
- 本文不判断 Nature Skill / Academic Research Suite 中哪些具体规则最终保留。
- 本文保留阶段性错误和被否决判断，因为它们是后续防止模型回流错误的重要训练证据。

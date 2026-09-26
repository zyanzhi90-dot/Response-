# A1 Codex：Comment 1 response 原始证据与决策记录

> 用途：保真保存本 Codex 账号围绕 TCYB 第三轮 Comment 1 response 形成的历史证据、用户纠正、错误路径、确认结果和未决事项。本文不是最终写作规则，也不把当前英文当作范文。
>
> 记录范围：从最初读取旧 Response、当前 Response、稿件和作者思路，经过多轮 TIE 对照、Comment 1 改写与验收、handoff 整理，到其后的 Comment 1 图内文字修改、正式图替换、重新编译和 response 文件夹清理。记录截止于本文件生成时。

## 0. 状态定义与来源职责

- `CONFIRMED`：得到用户明确确认，或可由相应原始材料直接核对。它只表示该事实或裁决在所述范围内成立；除非另有明确依据，不自动等于可推广的写作规则。
- `REJECTED`：曾被 Agent 提出、写入或视作合理，但随后被用户明确否决，或被原始材料证明不成立。
- `UNRESOLVED`：当时只提出过、仍需用户判断，或不同阶段材料存在冲突，不能转写成知识库规则。
- `CASE_SPECIFIC`：只适用于本次 TCYB Comment 1 的事实、符号、图形处理、审稿人阅读路径或项目裁决，不能直接推广到其他 reviewer response。可与前三种状态并列。
- `SUPERSEDED`：某个较早状态或指令后来被用户明确替换。保留它是为了保存演变链；当前有效的是其后明确标出的版本。可与 `CASE_SPECIFIC`、`REJECTED` 等并列。

以下是不可互相替代的来源职责，不构成一条统一的“权威等级”：

1. `CONFIRMED`：TIE 范例 PDF 原文和三份总结是表达与组织的主要依据。TIE 原文决定“该范例作者实际怎样写”；三份总结帮助定位论证动作，但总结者补写的句式不能冒充 TIE 原句，也不能把单一范例的观察直接泛化为所有顶刊规则。
2. `CASE_SPECIFIC · CONFIRMED`：作者已确认的 Comment 1 思路、实验事实和核心论证决定“本次回答什么”，不得为了模仿范例而重构内容。
3. `CASE_SPECIFIC · CONFIRMED`：JAS 原论文和当前稿件只用于核对任务含义、实验设置、符号、比较对象和引文；结果数值、曲线关系和由图直接支持的结论只依据作者指定的最终正式结果图。不能从源代码、绘图脚本、代码生成的图注或运行说明补充设置或撰写结果，也不能用 JAS 的符号重写本稿变量。
4. `CASE_SPECIFIC · CONFIRMED`：`本审稿人阅读习惯.txt` 用于决定本回复的信息位置、强调顺序和最小认知框架。
5. `CONFIRMED`：Nature response/polishing 能力仅作辅助；若通用 academic writing 与 TIE 原文的实际表达习惯冲突，以 TIE 为准。现有记录只证明它被设定为辅助来源，不证明其中任何通用句式已获用户确认。
6. `CASE_SPECIFIC · CONFIRMED`：旧 Response 只能提供结构或图文位置方面的取舍参考，不能整体回退或把旧、新内容叠加。

## 1. 任务演进与关键决策时间线

### 1.1 初始分析阶段

- `CASE_SPECIFIC · CONFIRMED` 用户最初要求同时读取旧 Response、当前 `Response-TCYB.tex`、当前 PDF 和 `response思路_作者原文.txt`，只分析 Comment 1，不修改文件。
- `CASE_SPECIFIC · CONFIRMED` 用户随后用自己的话确认了两个核心点：
  1. 先纠正“本文声称最低计算成本”的先入理解。本文关心的是每个控制步的在线计算能否在控制周期内完成；“加速”主要对应较少的 ILC 迭代轮次。稿件中“减轻计算负担”的两组比较基准分别是 fast-AGP 对 standard GP、CRBFNN 对 RBFNN。
  2. 接受审稿人关于计算效率普适性的质疑，用不同任务和不同设置下的任务代价与在线计算时间补证据。不同任务来自 JAS 案例，不同设置来自权重和刚度变化。
- `CASE_SPECIFIC · CONFIRMED` 用户特别提出最小认知框架的必要性：ILC 每轮产生一个任务代价，跨轮看收敛；每轮的每个时间步都需要在线计算；实时性指该计算能在本控制步结束前完成。

### 1.2 TIE 对照与多轮改写阶段

- `CASE_SPECIFIC · CONFIRMED` 用户要求只改当前 Comment 1，保留已确认核心逻辑和正式结果图，不改其他 Comment、旧 Response或稿件。
- `CASE_SPECIFIC · CONFIRMED` 用户不接受“语法正确、英语流畅”作为合格标准，要求从逻辑组织、信息层级、证据顺序、图文关系、语气、术语、句式、篇幅和 claim 边界等所有层面与 TIE 范例的写法精髓对齐。
- `CASE_SPECIFIC · CONFIRMED` 用户多次指出：列出的具体短语不是零散替换清单，而是在校准完整标准。每发现一个例子，必须回查全文同类问题。
- `REJECTED` Agent 曾反复只修用户点名的五处或八处表达，随后过早声称“达到 TIE 水平”。用户明确认为仍有大量隐藏问题，要求逐句、逐词和逐段复核。
- `CASE_SPECIFIC · CONFIRMED` 用户把 response 的最终目的界定为：让审稿人快速理解、认可并接受算法证据。实现细节若不能推进这一目的，应删除。
- `CASE_SPECIFIC · CONFIRMED` 在后期再次验收前，用户明确说“当前 response 我又进行了调整”。因此当前 Comment 1 文本具有用户与 Agent 共同修改的混合来源；不能把其中每句话都追溯为 Agent 判断，也不能因用户曾调整文件就推定全文已经获用户批准。

### 1.3 审稿人阅读路径校准阶段

- `CASE_SPECIFIC · CONFIRMED` 用户要求读取 `本审稿人阅读习惯.txt` 后调整信息位置：审稿人主要扫最终正式图、放入正式 response 的 caption 及图前后几句话，并带着“最低计算成本”的先入理解寻找不严谨处。这里的 caption 是 response 的作者写作输出，不是代码或绘图程序生成的图注，也不是实验结果的上游证据。
- `CASE_SPECIFIC · CONFIRMED` 因此，最低计算成本并非本文主张这一点必须首先可见；任务代价、迭代收敛、每步在线计算和控制周期的关系必须在几秒内重建；图周围必须放置能独立理解的核心文字。
- `REJECTED` “参数组图中的 20 ms 仅作原机器人实验的参考”被用户明确判定为与说服目的无关的旁枝，应删除。
- `REJECTED` fast-AGP 的计时操作、计时代码、预测/更新如何测时等实现过程被用户明确要求全部删除。

### 1.4 Handoff 时点

- `CASE_SPECIFIC · CONFIRMED` 2026-09-21 形成四份 handoff 文件。该时点的共识是：核心逻辑和证据结构已经确定，但最新英文尚未完成 TIE 原文逐句验收，也未获用户最终确认。
- `CASE_SPECIFIC · CONFIRMED` handoff 明确要求下一轮不能推倒重来，也不能把最新英文直接视为范文；只能继承主线继续收敛表达。

### 1.5 Handoff 后的图形阶段

- `CASE_SPECIFIC · CONFIRMED` 用户随后暂停正文修改，只处理 Comment 1 的结果图文字、符号、引用与对齐；禁止改正文叙述、数据、曲线、坐标范围、图例顺序、布局和比较关系。
- `CASE_SPECIFIC · CONFIRMED` 经过多轮图形反馈后，用户要求把候选图直接替换进 `response_TCYB2/fig` 并重新编译。十张 Comment 1 图已替换，PDF 曾成功生成。
- `CASE_SPECIFIC · CONFIRMED` 用户随后要求清理 response 文件夹；旧 `Response-TCYB-reviewed.*`、预览目录和未被 TeX 引用的 EPS 被删除，当前 `.tex`、PDF、编译记录和引用中的图 PDF 被保留。
- `CASE_SPECIFIC · UNRESOLVED` 本证据整理时，当前 `Response-TCYB.tex` 的修改时间为 2026-09-22 12:32:29，晚于当前 PDF 的 2026-09-22 11:42:52；因此现在不能再据当时的成功编译断言当前 TeX 与 PDF 同步。本步按用户要求不重新编译、不修改 response。

## 2. Comment 1 的原始关切与作者确认的回答主线

> 本节全部为 `CASE_SPECIFIC`。其中的 `CONFIRMED` 只表示本次 Comment 1 的关切、事实或回答边界已经确认，不构成其他 response 的通用规则。

### 2.1 审稿人实际关切

- `CASE_SPECIFIC · CONFIRMED` 审稿人指出上一版仅改变环境刚度并给出 task-cost convergence curves，不能证明 fast-AGP 在不同任务或设置下具有计算优势。
- `CASE_SPECIFIC · CONFIRMED` 审稿人特别区分了 convergence performance 与 generality of the computational-efficiency conclusion。
- `CASE_SPECIFIC · CONFIRMED` 审稿人认为仅变化环境刚度不足以构成充分不同的任务/设置，并指出曲线没有直接展示计算成本。

### 2.2 第一核心回答：计算主张和评价尺度

- `CASE_SPECIFIC · CONFIRMED` 回答必须先让审稿人看到：本文的目标是控制周期内的实时在线计算可行性，而不是证明 fast-AGP 具有所有比较方法中的最低计算成本。
- `CASE_SPECIFIC · CONFIRMED` 必须区分两个时间尺度：
  - iteration domain：每轮任务产生 task cost `\(\mathcal{J}_j\)`，跨轮下降反映 convergence；“accelerated convergence”是达到给定任务代价所需迭代轮次更少。
  - control-step domain：每轮包含多个控制步，每步均有在线计算；real-time feasibility 由单步最大在线计算时间与 control period `\(\Delta t\)` 比较。
- `CASE_SPECIFIC · CONFIRMED` 原机器人实验中，proposed method 的最大单步在线计算时间为 9.90 ms，控制周期为 20 ms；standard GP 在相同条件下超过该周期。该事实来自当前稿件。
- `CASE_SPECIFIC · CONFIRMED` “reduced computational burden”必须交代各自比较基准：fast-AGP 与 standard GP 比，CRBFNN 与 lattice-distributed RBFNN 比。
- `REJECTED` 不能由“更少迭代轮次”直接推出“每步计算更低”或“累计计算成本最低”。
- `REJECTED` 不能把 fast-AGP 相对 standard GP 的减负，扩大成相对 IL-SOGP 或所有 sparse GP 都最低。

### 2.3 第二核心回答：不同任务和不同设置的对应证据

- `CASE_SPECIFIC · CONFIRMED` 必须明确承认上一版证据缺口：只改变 `\(S_e(t)\)` 并报告 `\(\mathcal{J}_j\)` 只涉及 convergence，不能直接回答 computational efficiency。
- `CASE_SPECIFIC · CONFIRMED` 不同任务部分采用 JAS 原论文的 Case 1 和 Case 2，并同时给 task cost 和 maximum online computation time per control step。
- `CASE_SPECIFIC · CONFIRMED` 不同设置部分采用当前两自由度任务中的 cost-function weights 和 environment stiffness 变化，也同时给 task cost 和 online computation time。
- `CASE_SPECIFIC · CONFIRMED` 两类实验的作用不能混成泛泛的“robustness”；JAS 案例回答不同 interaction tasks，权重和刚度回答原任务内的不同 objectives/settings。
- `REJECTED` 只补 task-cost curves 仍不能回答 computational-efficiency concern。

## 3. TIE 原文及三份总结提供的具体证据

### 3.1 可直接核对的语言和段落动作

- `CONFIRMED` TIE 原文 19 个 `Response:` 首句中，多数使用 `Thanks for ...` 或 `The authors sincerely thank ...`；感谢后通常转为 `we` 描述具体动作。该统计来自 `Response_表达范式.md` 和 `TIE范例_逐条拆解.md`。
- `CONFIRMED` TIE R1-2（PDF 第 3 页）使用 `According to your suggestion` 引出已补测试，并紧接 `To further show ...` 进入测试目的；随后说明设置，再用 `The simulation results are depicted ...` 和 `It can be observed ...` 读图。
- `CONFIRMED` TIE R3-2（PDF 第 12–17 页）先解释为何 PID/MBAC 是有意义的比较对象，再宣布新增 comparison studies，随后将图表和读图结论放在对应论点附近。原文有 `According to your suggestion, comparisons have been conducted ...`、`To further verity ...` 和 `As seen from the figures ...`。其中 `verity` 是原文拼写错误，只能作为段落动作证据，不能照抄。
- `CONFIRMED` TIE R4-3（PDF 第 18–19 页）以“补做什么实验—平台/轨迹—图显示什么—有限结论”的顺序进入真实机器人实验，图直接跟在相应解释后。
- `CONFIRMED` TIE R3-1（PDF 第 11–12 页）面对原创性质疑时，先承接前作，再分别说明本文动作与动机；这与本项目“先温和界定主张，再给证据”的需求相似，但其部分绝对化比较不可照搬。
- `CONFIRMED` TIE R4-4 是反面证据：用外扰试验笼统回应量化、延迟和速度估计等多个不同问题，存在证据不对应。该例支持本 Comment 每一关切必须有直接证据，不能以相近实验代替。

### 3.2 TIE 的组织证据

- `CONFIRMED` 复杂新实验回复的稳定结构是：先概述已做动作和主要结果，再给比较对象、指标与必要条件，随后放图/表并直接读出结果，最后指向稿件位置或限定结论。
- `CONFIRMED` 证据应靠近主张。TIE 的复杂实验回复把图、表、推导放在对应论点后，而不是在远处集中堆放。
- `CONFIRMED` 篇幅随证据需求变化：简短修正很短；证明、新颖性或系统比较可以较长，但文字仍围绕可核验链条。
- `CASE_SPECIFIC · CONFIRMED` 本项目另有用户明确要求：一条 comment 有两个独立关切时用 `1)`、`2)` 分点。TIE 原文自身并不稳定使用编号分点，因此这不是“照搬 TIE 格式”，而是结合本审稿人的扫读习惯所作的项目决定。

### 3.3 不可机械复制的 TIE 内容

- `REJECTED` 不复制 TIE 原文的语法错误或非地道搭配，如 `Comparing with`、`cost expensive`、`To further verity`。
- `REJECTED` 不复制 TIE 中 `far less`、`guarantee`、`more suitable` 等可能超过证据的强结论。
- `REJECTED` 不把 TIE 的具体图、平台、参数或结果迁移为本稿证据。
- `REJECTED` 不因为 TIE 回复较长、图较多，就以篇幅或图量代替证据质量。

## 4. 用户指出过的具体表达问题与最终处理状态

### 4.1 开场、语气与元话语

| 状态 | 当时表达或判断 | 用户反馈/材料证据 | 最终记录及原因 |
|---|---|---|---|
| `REJECTED` | `We wish to clarify ...` | 用户明确指出 TIE 范例没有这种写法；对 TIE 全文检索亦未发现该惯用开场。 | 不能把它当作 TIE 语言指纹。应直接写研究目标、动作或证据。 |
| `REJECTED` | `The point we wish to clarify ...` 被当作 TIE 原句 | 该句来自三份总结中的“项目增强”，不是 TIE 原文。 | 总结可以提供功能，但不得伪装为范例作者原话。 |
| `REJECTED` | `Our earlier wording did not clearly ...` | 用户称“根本没有这种写法”，认为是泛化 academic English。 | 不以抽象 wording 元话语开段；若承认不足，应直接指出缺少了哪类证据。 |
| `CASE_SPECIFIC · UNRESOLVED` | `We do not claim that fast-AGP has the lowest computational cost ...` 的精确语气 | 用户先问“是否过于强硬（我不确定）”，后续持续要求重新判断；handoff 只确认正面界定范围，未确认最终英文。 | 不能把直接否定当作已批准句式，也不能误记为已被最终否决。已确认的是避免对抗、优先正面说明真实计算目标。 |
| `CASE_SPECIFIC · UNRESOLVED` | `rather than to achieve the lowest computational cost` | handoff 认为比直接否定缓和，但尚未获用户最终验收。 | 只记录为候选，不得转成规则。 |
| `CONFIRMED` | 一句感谢后立即进入具体问题 | TIE 原文和三份总结均支持；用户要求简洁。 | 感谢用于礼貌承接，不应堆叠或拖延核心回答。 |

### 4.2 不存在、笨重或不专业的术语

| 状态 | 具体例子 | 处理结果与理由 |
|---|---|---|
| `REJECTED` | `stiffness-only task-cost curves` | 用户一眼判定不专业；后续过度解释版本也被认为啰嗦。应直接说明上一版“只变化环境刚度并报告任务代价”，不创造压缩标签。 |
| `REJECTED` | `full-GP` | 当前稿件无此正式名称。使用 `standard Gaussian process (GP)`。 |
| `REJECTED` | `IEEE-JAS Case 1 [5]` | 不是原论文正式命名，且来源定位机械。 |
| `REJECTED` | `Case 1 in the study by Pan et al.` | 虽可理解，但用户认为啰嗦。当前方向是 `Case 1 in \cite{...}` 或共同介绍 `Cases 1 and 2 in \cite{...}`。精确英文仍需结合句子。 |
| `REJECTED` | 从图文件名把 `b:c` 当作正式变量 | 当前稿件定义的是 `\(W_x\)` 和 `\(W_f\)`；JAS 与该权重无关。 |
| `REJECTED` | `\(S_{e,\max}\)` | 稿件使用 `\(S_e(t)\)`，不能从“峰值”概念另造变量。 |

### 4.3 句式、指代与衔接

| 状态 | 具体例子 | 处理结果与理由 |
|---|---|---|
| `REJECTED` | `Next, we vary ...` | 只报告操作顺序，没有说明该实验回答什么。 |
| `REJECTED` | `Finally, we vary ...` | 同上；流程顺序不能替代论证目的。 |
| `REJECTED` | `For the original task, we varied ...` | 用户明确判定不符合 TIE 的自然表达。 |
| `REJECTED` | `For the same task, we also varied ...` | 与上一条相同，且 `also` 不能补足逻辑。 |
| `CONFIRMED` | 用 `To further show ...` / `To further verify ...` 的“目的性进入”功能 | TIE R1-2、R3-2 有直接依据；用户明确要求不同实验部分先交代目的。 | 目的句后必须立刻给必要设置和对应证据，不能只换连接词。 |
| `CASE_SPECIFIC · UNRESOLVED` | 多段重复 `To further evaluate/examine/verify ...` | 功能方向获认可，但 handoff 明确指出模板重复密度尚未最终验收。 |
| `REJECTED` | 含糊的 `its`、`this computation time`、`these results` | 用户要求检查所有同类指代。并非禁用代词本身，而是多个方法/指标并列时不能让审稿人回读找先行项。 |

### 4.4 图号与图文关系

| 状态 | 具体例子 | 处理结果与理由 |
|---|---|---|
| `REJECTED` | 句末孤立的 `(Fig.~\ref{...}(d))` | 用户要求参考 TIE 的完整读图句；图号必须与“显示什么”建立语法关系。 |
| `CONFIRMED` | `As shown in Fig. ...` / `Fig. ... shows ...` 的功能 | TIE 使用 `The simulation results are depicted ...`、`As seen from the figures ...` 等完整关系；当前 response 应自然读图，不机械只用一个模板。 |
| `CONFIRMED` | 图前说明目的和比较对象，正式 response caption 与图旁文字写清指标、条件、结果与边界 | 来自 TIE R1-2、R3-2、R4-3及审稿人扫图习惯。正式 caption 是写给审稿人的输出。 |
| `CASE_SPECIFIC · CONFIRMED` | 结果写作只依据作者指定的最终正式结果图 | 用户反复强调不能换旧图、候选图或 Agent 重新生成的版本，也不能依据源代码、绘图脚本、代码生成的图注或运行说明写结果。 |

### 4.5 文献与编号

- `CASE_SPECIFIC · CONFIRMED` 本回复涉及的 external method 首次出现时必须有文献。用户特别指出 `Classical IL` 后不能漏引。
- `CASE_SPECIFIC · CONFIRMED` 用户要求同时呈现 response 自身的引用与 revised manuscript 编号，例如 `classical IL~\cite{respLiGe2014} ([18] in the revised manuscript)`。
- `CASE_SPECIFIC · CONFIRMED` IL-SOGP 对应 response 文献 `\cite{respPanJAS2025}`；当时稿件编号尚未补，保留 `[XX]` 占位符，不可猜测。
- `CASE_SPECIFIC · CONFIRMED` response 末尾补 Li–Ge 和 Pan et al. 两条文献。
- `CASE_SPECIFIC · UNRESOLVED` 当前 `Response-TCYB.tex` 仍含 revised manuscript 编号占位符 `[XX]`；提交前必须由稿件最终参考文献编号确定。

## 5. 实验信息、术语与符号的证据记录

### 5.0 事实来源的职责边界

- `CASE_SPECIFIC · CONFIRMED` JAS 原论文和当前稿件用于确认任务是什么、设置如何定义、采用什么符号、比较对象是谁以及文献如何引用。
- `CASE_SPECIFIC · CONFIRMED` 作者指定的最终正式结果图是 response 中结果数值、曲线高低关系、方法间比较和图示结论的直接依据。
- `CASE_SPECIFIC · CONFIRMED` 不读取源代码、绘图脚本、代码生成的图注、自动 caption、运行日志或说明文字来补充 response 的设置或结果。这一边界针对本次项目的既定证据链，不能擅自扩成所有科研写作都不得查看代码的通则。
- `CASE_SPECIFIC · CONFIRMED` 正式 response caption 需要根据最终正式图和已核实设置重新撰写，使审稿人扫图时能够理解；它是最终 response 的组成部分，不是用来反向推断实验结果的原始来源。

### 5.1 JAS 原论文的可核对事实

- `CASE_SPECIFIC · CONFIRMED` JAS 原论文 Section IV-B 明确写：Case 1 用于 accurate tracking，`\(\alpha=10\)`、`\(C=[25,0,1]\)`；Case 2 用于 compliant interaction，`\(\alpha=20\)`、`\(C=[100,0,0.1]\)`。
- `CASE_SPECIFIC · CONFIRMED` JAS 原论文采用 simulated 7-DoF Franka Emika Panda；inner loop sampling delay 为 1 ms，outer-loop admittance-control sampling delay 为 10 ms。
- `CASE_SPECIFIC · CONFIRMED` 用户认可可用“tracking / compliant interaction”简要说明两类任务目的。
- `CASE_SPECIFIC · UNRESOLVED` response 中究竟保留 Panda、uneven surface、trajectory/contact environment、`\(\alpha\)`、`\(C\)` 到什么程度，handoff 时尚未最终确认。用户明确说交代 tracking / compliant interaction 的目的可以，但“写到什么程度”必须服从本回复的整体论证。判断标准是能否证明任务确实不同并解释实时判据，而不是复现 JAS Methods。
- `CASE_SPECIFIC · UNRESOLVED` 仅写 `Cases 1 and 2` 是否必然信息不足并未被用户单独裁决；用户确认的是需要根据整体逻辑交代两类任务的目的，精确的最小充分表达仍待定。因此不再把这条记作 `REJECTED`。
- `CASE_SPECIFIC · CONFIRMED` 用户明确反对为显得完整而堆入与说服链无关的设置。是否保留某个 JAS 平台或参数仍须逐项判断；“把机器人模型、环境方程、核参数和全部控制参数全部搬入 response”只记录为被排除的处理倾向，而不是曾经出现过并被逐句否决的具体草稿。

### 5.2 当前稿件的符号和事实

- `CASE_SPECIFIC · CONFIRMED` 当前稿件定义 `\(S=[W_x\;0\;W_f]\)`，其中 `\(W_x\)` 是 position/tracking term 的权重，`\(W_f\)` 是 force-integral term 的权重。
- `CASE_SPECIFIC · CONFIRMED` 权重比较正式写法采用 `\(W_x:W_f=20:1\)`、`50:1`、`200:1`；正文可完整写 `\(W_x=20I,50I,200I\)` 且 `\(W_f=I\)`。
- `CASE_SPECIFIC · CONFIRMED` 刚度设置使用 `\(S_e(t)=10(\sin\pi t)^2I\)`、`30(\sin\pi t)^2I`、`50(\sin\pi t)^2I`；用户明确要求不用 `\(S_{e,\max}\)`，图中不用 `\(I_2\)`。
- `CASE_SPECIFIC · CONFIRMED` 涉及变量、指标或符号时，用户要求写出变量名和符号，尤其在首次出现、设置变化处、正式 response caption 和核心读图句中。
- `CASE_SPECIFIC · UNRESOLVED` 信息分配的精确密度仍需逐句判断。handoff 特别提醒：完整不等于每一句机械重复同一长串定义。

### 5.3 已采用结果和结论边界

- `CASE_SPECIFIC · CONFIRMED` JAS Case 1 的 `\(\mathcal{J}_{10}\)`：proposed 80.40、IL-SOGP 86.01、classical IL 88.61；proposed `\(t_{\mathrm{comp}}^{\max}=4.75\)` ms。
- `CASE_SPECIFIC · CONFIRMED` JAS Case 2 的 `\(\mathcal{J}_{10}\)`：proposed 64.83、IL-SOGP 66.86、classical IL 72.06；proposed `\(t_{\mathrm{comp}}^{\max}=4.65\)` ms。
- `CASE_SPECIFIC · CONFIRMED` 两个 JAS 案例中 proposed method 的时间均高于 IL-SOGP，但低于 10 ms outer-loop control period。必须如实保留不利比较，不能暗示其计算成本低于 IL-SOGP。
- `CASE_SPECIFIC · CONFIRMED` 权重和刚度图用于展示相应设置下 task cost 与 online computation time；不能由这些有限设置推出所有任务、硬件或采样周期的普遍保证。
- `REJECTED` `fast-AGP has the lowest computational cost`、`generally applicable`、`universally`、对未测试平台的 `guarantee`。
- `CASE_SPECIFIC · CONFIRMED` handoff 时的保守结论边界是：明确的实时可行性收束在两个新增 JAS Case；权重/刚度结果只说明所测设置下的任务代价与计算时间表现。
- `CASE_SPECIFIC · UNRESOLVED` 当前 `Response-TCYB.tex` 第 340–342 行把 `t_comp^max < Delta t` 的结论扩大到两个任务及 `W_x`、`S_e(t)` 变化；这与 handoff 的更窄边界不完全一致，且该版英文未获用户最终验收。因此不能把当前句子提升为知识库规则。

## 6. 被否决的内容扩张和错误证据替代

### 6.1 CRBFNN 细节

- `REJECTED` 曾写：`CRBFNN used 20 neurons, compared with 729 for the lattice-based RBFNN, and achieved lower tracking errors. The neuron counts describe network size, not measured runtime.`
- 用户明确评价为“不准确且不切题”。原因：神经元数量、网络规模和 tracking error 不是 fast-AGP 的 runtime evidence，且会把 Comment 1 拖入另一条论证。
- `CASE_SPECIFIC · CONFIRMED` 若需要解释“reduced computational burden”的范围，只保留比较口径：CRBFNN 与 lattice-distributed RBFNN 比。不得把 CRBFNN 扩成独立实验单元。
- `CASE_SPECIFIC · SUPERSEDED` 作者最初提出“CRBFNN 可以把汤发的那段话发上去”这一候选方向，后来被“删除不切题细节、只保留比较口径”的明确要求替代。该早期方向保留为历史，不能恢复为当前有效方案。

### 6.2 计时实现细节

- `REJECTED` 计时函数、程序操作、prediction/update 如何计时、时间统计过程等均被用户判定为细枝末节。
- `CASE_SPECIFIC · CONFIRMED` reviewer response 只需呈现比较对象、指标、数值、控制周期和有限结论。

### 6.3 旧 Response 的取舍

- `CASE_SPECIFIC · CONFIRMED` 用户认为旧 `Response-TCYB-旧.pdf` 在内容和格式上“不错”，主要问题是英语表达不专业。
- `CASE_SPECIFIC · CONFIRMED` 允许吸收旧版更有效的信息层级、文本框、分点或图文位置，但必须逐项判断。
- `REJECTED` 整体回退旧版，或把旧版和当前版堆叠成更长回复。
- `REJECTED` 旧/早期版本中的 `stiffness-only task-cost curves`、`full GP`、`IEEE-JAS Case 1`、`Next`、`Finally`、20 ms reference 辩解和 CRBFNN neuron paragraph。
- `CASE_SPECIFIC · SUPERSEDED · REJECTED` 旧图或早期文字中的 `b:c` 与 `S_{e,\max}` 后来分别被稿件符号 `W_x:W_f` 与 `S_e(t)` 取代；旧形式仅用于保存错误路径。
- `CASE_SPECIFIC · UNRESOLVED` `We do not claim ...` 只被用户提出“是否过强、需重新判断”，没有被最终否决。被否决的是把它未经核验地当成 TIE 式稳妥开场；其精确语气状态见 4.1。

## 7. Comment 1 结果图的历史决策

### 7.1 指标符号的变更链

- `CASE_SPECIFIC · SUPERSEDED` 初始图形要求中的 `\(T_{\mathrm{on}}^{\max}\)` 后来被用户明确替换；它不是当前有效符号。
- `CASE_SPECIFIC · CONFIRMED` 最终指定符号为 `\(t_{\mathrm{comp}}^{\max}\)`，含义为 maximum online computation time per control step。
- `CASE_SPECIFIC · CONFIRMED` 用户最终指定纵轴表达为 `Maximum online computation time per control step \(t_{\mathrm{comp}}^{\max}\) (ms)`，并明确不要“变量名 + 逗号 + 符号”的格式。
- `CASE_SPECIFIC · CONFIRMED` 用户最后又要求“把所有图的逗号去掉，其他不变”。
- `CASE_SPECIFIC · UNRESOLVED` 当前正式图的 timing y-axis 已无逗号，但 task-cost 图仍可由 PDF 文本抽取得到 `Task cost, \(\mathcal{J}_j\)`。由于用户随后授权替换整组候选图，这一现状已进入 response；但它与“所有图的逗号去掉”的字面要求存在潜在不一致。本步只记录，不擅自修图或把任一解释写成规则。

### 7.2 图内术语、引用与对齐

- `CASE_SPECIFIC · CONFIRMED` Figure 3 权重条件改为 `\(W_x:W_f=20:1\)`、`50:1`、`200:1`，不能保留 `b:c`。
- `CASE_SPECIFIC · CONFIRMED` Figure 4 全部采用 `\(S_e(t)\)` 和 `\(I\)`，不用 `S_e`、`I_2` 或 `S_{e,\max}`。
- `CASE_SPECIFIC · CONFIRMED` 每个 computation-time panel 的右上角应显示与对应 task-cost panel 相同的权重或刚度条件，使单看计时图也能识别设置。
- `CASE_SPECIFIC · CONFIRMED` 所有图内 `IL-SOGP` 后加 `[10]`。用户后来明确指出此前未加引用是错误。
- `CASE_SPECIFIC · CONFIRMED` 若右上角条件标注无法与 task-cost panel 对齐，则将所有 timing panel 的 `control period` 统一移至左侧，让右上角留给 `S_e(t)` / `W_x:W_f`；`Proposed method`、`IL-SOGP [10]` 的位置与字体也需在配对图间对齐。
- `REJECTED` 为追求像素级不动而引入额外修改或偏离用户指定文字。用户明确说不要再受“底层 PDF 内容流造成 4 pt 位移”等内部技术说明影响，若因此产生改动应恢复。
- `CASE_SPECIFIC · CONFIRMED` 图形修改边界：不改数据、曲线、坐标范围、虚线位置、图例顺序、图例含义、布局、尺寸、分辨率和比较关系。

### 7.3 图形当前状态

- `CASE_SPECIFIC · CONFIRMED` 十张修改后的 Comment 1 图已替换进 `response_TCYB2/fig`；随后曾重新编译 `Response-TCYB.pdf`。
- `CASE_SPECIFIC · CONFIRMED` 当前最终正式图 PDF 可直接抽取到：`IL-SOGP [10]`、`W_x:W_f` 条件、`S_e(t)` 条件及 `t_comp^max` timing label；这些图本身而非代码生成的图注，是图示结果写作的依据。
- `CASE_SPECIFIC · CONFIRMED` 图内 `[10]` 是 response 文献表中的编号，用户已明确要求加在 `IL-SOGP` 后；正文的 `\cite{respPanJAS2025}` 由 response 文献表解析。`[XX] in the revised manuscript` 是另一套编号体系中的占位符，二者用途不同，不构成冲突。仍未解决的只有 revised manuscript 中 `[XX]` 的最终编号。

## 8. 当前 response 文本与 handoff 状态

### 8.1 当前文件实际内容

- `CASE_SPECIFIC · CONFIRMED` 当前 Comment 1 位于 `response_TCYB2/Response-TCYB.tex` 约第 207–342 行，以 `The authors did not respond well ...` 定位，以 `\item[2.]` 结束。
- `CASE_SPECIFIC · CONFIRMED` 当前文本已经具有两个编号单元：`1) Computational objective and evaluation criteria.` 和 `2) Additional comparisons under different tasks and settings.`
- `CASE_SPECIFIC · CONFIRMED` 当前文本已包含 ILC 最小认知框架、fast-AGP/GP 与 CRBFNN/RBFNN 的比较口径、JAS 两个 Case、权重与刚度图、两条主要 response references。
- `CASE_SPECIFIC · CONFIRMED` 当前文本使用 `standard Gaussian process (GP)`、`W_x/W_f`、`S_e(t)` 和 `t_comp^max`，没有恢复 `full-GP`、`b:c` 或 `S_{e,\max}`。
- `CASE_SPECIFIC · CONFIRMED` 这些只是本次整理时的文件快照。结合 1.2 所记的用户手动调整，不能据此推定所有现有句子均是 Agent 方案或均已获用户确认。

### 8.2 不能误判为已定稿的部分

- `CASE_SPECIFIC · UNRESOLVED` 当前首段英文尚未经过用户最终验收。历史上用户已多次证明“逻辑对”不代表“TIE 风格表达合格”。
- `CASE_SPECIFIC · UNRESOLVED` 当前 JAS 设置密度仍可能偏高。Panda、uneven surface、trajectory/contact environment 与 `C` 的保留量未获最终确认。
- `CASE_SPECIFIC · UNRESOLVED` 当前多个目的句、变量名+符号的重复密度和结尾 claim 边界未完成最终逐句审核。
- `CASE_SPECIFIC · UNRESOLVED` 当前 TeX 比 PDF 新，故当前 PDF 不可作为最新文本的可靠渲染证据。
- `REJECTED` 不得描述为“完全达到 TIE 范例水平”“最终定稿”或“提交版”，除非重新逐句验收、同步编译并获得用户确认。

## 9. 已确认边界、被否决判断与未决判断汇总

### 9.1 `CASE_SPECIFIC · CONFIRMED`

- 只处理 Comment 1，核心逻辑、实验事实和正式结果不推倒重来。
- 两个核心回答是“计算主张/评价尺度”与“不同任务和不同设置的对应证据”。
- 最低计算成本必须在最前部被温和地纠正；最小认知框架必须早出现。
- TIE 原文与三份总结决定表达和组织；JAS/稿件核对任务、设置、符号、比较对象与引文；最终正式结果图决定图示结果及其可支持的结论；Nature 只辅助。
- 用户的例子用于反推全文标准，不能只做点状替换。
- 不写计时实现细节，不用 CRBFNN 网络规模替代 fast-AGP runtime evidence。
- 不创造方法名或变量；不使用 `full-GP`、`IEEE-JAS Case 1`、`b:c`、`S_{e,\max}`。
- 外部方法需要引文；图文要在审稿人扫读路径上自足；结论不能超过已测条件。
- 只用作者指定的最终正式图撰写图示结果，不看源代码、绘图脚本或代码生成的图注；正式 response caption 仍需面向审稿人准确撰写。图内文字的最终确认链如第 7 节所记。

### 9.2 `REJECTED`

- 把用户反馈当成若干局部短语替换。
- 把 `we wish to clarify` 或总结者补写句当成 TIE 原文习惯。
- 用直接、对抗式否定责备审稿人，或写 `we already stated ...`。
- 用实验操作顺序 `Next/Finally/For the original task` 代替证据目的。
- 用悬空括号图号、含糊代词、无来源术语和泛化 adjective 推进回复。
- 从源代码、绘图脚本、代码生成的图注或运行说明补写设置和结果；堆测时实现、网络规模或与本 concern 无关的防御性旁注。
- 声称最低计算成本、普遍实时性或相对 IL-SOGP 的计算成本优势。
- 整体回退旧 Response、换图、扩展到其他 Comment，或在未验收时宣称完成。

### 9.3 `CASE_SPECIFIC · UNRESOLVED`

- 最终用于温和表达“最低成本不是本文主张”的精确英文。
- 当前 `rather than ...`、`do not claim ...` 等候选的最终语气判断。
- JAS 设置的最小充分保留量。
- 多个目的句和变量/符号重复的最终密度。
- 当前结尾是否可把 20 ms 作为权重/刚度图的真实 control period，并据此把实时性结论覆盖到这些设置。
- revised manuscript 中 `[XX]` 的最终参考文献编号；图内 `[10]` 属于 response 文献体系，已确认，不与该占位符构成冲突。
- 当前图中 task-cost y-axis 逗号与用户“所有图去逗号”字面要求的差异。
- 当前 TeX/PDF 的同步状态和 Comment 1 英文的最终 TIE 验收。

## 10. 重要因果关系记录

1. 之所以把“最低计算成本并非本文要证明的结论”前移，不只是为了礼貌，而是因为审稿人带着这一先入理解先扫图；若不先纠正，后续所有 computation-time 证据会被错误口径解读。
2. 之所以增加最小认知框架，是因为 reviewer 把 accelerated convergence、computational burden 和 real-time feasibility 混在一起；这三个概念分属不同指标和时间尺度。
3. 之所以同时给 task cost 和 online computation time，是因为 reviewer 明确指出上一版只证明 convergence，没有证明 computational efficiency。
4. 之所以加入 JAS Case 1/2，是因为仅改刚度不能构成充分不同任务；跟踪与柔顺交互可最简洁地证明任务目的不同。
5. 之所以仍保留权重和刚度设置，是为了回应 different settings，但它们不能被描述成全新任务，也不能单独支撑普遍实时性。
6. 之所以如实写 proposed method 的时间高于 IL-SOGP，是为了保持证据诚实，并防止“最低成本”误解再次出现。
7. 之所以删除测时实现细节和 CRBFNN neuron paragraph，是因为它们不直接回答 reviewer 的判断标准，反而稀释核心证据。
8. 之所以要求图前、图中和图后文字自足，是因为本审稿人主要扫图和附近几句；信息远离图等于审稿路径中不可见。
9. 之所以不能机械复制 TIE 连接词，是因为 TIE 可迁移的是论证步态与证据位置，而其原文也含语法错误、重复和过强结论。
10. 之所以保留 `UNRESOLVED` 项，是因为此前最大的流程错误之一就是把“一轮改写完成”误报成“已达到范例水平”。

### 10.1 关键“先提出、后核验或替代”的完整决策链

| 状态 | 用户反馈 | 当时的 response / Agent 判断 | 重新核验的原因与依据 | 最终处理 |
|---|---|---|---|---|
| `REJECTED` | “TIE 范例中并没有 `we wish to clarify` 这种写法。” | Agent 曾把 `We wish to clarify ...` 当作自然且接近 TIE 的开场。 | 回查 TIE PDF 原文未发现该惯用开场；相似句来自总结中的“项目增强”，不是范例原句。 | 不能把该短语当作 TIE 语言指纹；本次回复应直接进入目标、动作或证据。 |
| `CASE_SPECIFIC · UNRESOLVED` | 用户问 `We do not claim ...` 是否过强，并要求重新判断。 | 早期版本使用该直接否定，后又有人将其与其他已否决措辞并列。 | 原始对话只有质疑和重审要求，没有最终批准或否决；TIE 对照只支持温和界定主张，不能替用户决定精确句式。 | 保留为未决候选；被否决的是把它未经核验地视为合格的 TIE 式开场。 |
| `CASE_SPECIFIC · SUPERSEDED · REJECTED` | 用户指出 `b`、`c` 应根据本稿判断，而本稿并未使用这两个符号。 | Agent 曾从图文件名、脚本或外部案例把 `b:c` 当作正式权重写法。 | 回查当前稿件可见 `S=[W_x\;0\;W_f]`；JAS 论文不负责定义本稿权重符号。 | 当前采用 `W_x:W_f`；`b:c` 只保留为错误路径。 |
| `CASE_SPECIFIC · SUPERSEDED` | 用户最初允许考虑加入“CRBFNN 那段话”，后明确说神经元数量段落“不准确且不切题”。 | Agent 扩写了 `20 neurons`、`729 neurons`、tracking error 与 runtime 的说明。 | 该信息不能直接证明 fast-AGP 的在线计算时间，也把本 comment 拖入另一条论证。 | 早期候选被后续要求替代；只保留 CRBFNN 与 lattice-distributed RBFNN 的比较口径。 |
| `CASE_SPECIFIC · CONFIRMED` | 用户澄清“不看”的是代码产生的图注，而审稿人会看的正式 response caption 必须写好。 | 早期记录容易把“不要看图注”笼统理解为所有 caption 都不可用。 | 对话进一步区分了上游证据与最终写作输出；最终正式图才是数值和曲线关系的直接证据。 | 不用代码生成的图注、脚本或运行说明补写结果；正式 response caption 仍须根据核实材料撰写。 |
| `CASE_SPECIFIC · SUPERSEDED` | 用户先指定 `T_{\mathrm{on}}^{\max}`，后明确改为 `t_{\mathrm{comp}}^{\max}`。 | 初始图形方案采用前一符号。 | 后一条用户指令直接替换前一条，并继续规定完整纵轴表达。 | 仅 `t_{\mathrm{comp}}^{\max}` 为当前有效符号；旧符号保留作历史。 |
| `CASE_SPECIFIC · CONFIRMED` | 用户要求图内 `IL-SOGP` 后加 `[10]`，同时稿件中的对应编号尚未补齐而用 `[XX]`。 | 早期记录把二者列为可能的编号冲突。 | `[10]` 属于 response 文献表，`[XX]` 明示为 revised manuscript 编号占位符，是两套不同引用语境。 | 图内 `[10]` 已确认；仅稿件 `[XX]` 的最终编号仍为 `UNRESOLVED`。 |

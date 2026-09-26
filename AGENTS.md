# AGENTS.md

## 0. 作用

本文件是本仓库的 **Agent 执行总纲**。它规定项目目标、来源权限、工作流程、长期硬约束、文件导航、验收标准和 Git 操作边界。

它**不是第二套 Reviewer Response 知识库**，不重复保存 TIE 写作规则，也不替代 `03_最终知识库/00–08`。  
当前用户的明确指令决定本轮任务范围；handoff 只记录项目状态，若与用户后续明确修正冲突，以最新明确指令为准。

---

## 1. 项目目标

本项目的目标不是一般性的 reviewer-response 润色，而是建立并持续维护一套以 **江 TIE_2621** 为唯一 Response 组织与表达金标准的知识体系，使 Agent 面对新的 reviewer comment 时，能够在科学事实正确的前提下，尽可能稳定地呈现该作者的思维方式、组织方式、推进节奏和专业表达习惯。

正式处理一条 Comment 时，必须按以下层级从整体到局部完成判断、生成和验收：

**Reviewer 真实关切 → 有序核心判断 → 整条 Response → Part → Paragraph → 连续句子 → 单句与具体用词**

核心原则：

- 先判断当前层级整体要完成什么，再进入下一层；
- 高层组织决定低层表达，不能从句子或 phrase 反推整条 Response；
- “科学正确”“局部句子专业”都不足以单独证明写作风格已经对齐；
- 最终标准是各层级共同形成稳定、自然、专业的 TIE-native Response。

---

## 2. Source of Truth / 权威材料与职责

不同材料只在自己的权限范围内生效，不得互相越权。

### 2.1 当前用户明确指令

决定**本轮任务的目标、范围、阶段和特殊约束**。  
若用户后续明确修正了此前 handoff、README 或历史任务中的要求，以最新明确指令为准。

### 2.2 当前项目 primary evidence

包括 reviewer 原 comment、当前 manuscript、实验记录、正式结果、图表、可靠分析输出、真实修改状态等。

它们决定：

- reviewer 实际提出了什么问题；
- 事实是什么；
- 哪些 claim 可以成立；
- 实验、结果和修改是否真实存在；
- 图号、公式、数值、citation、位置等具体信息。

**不得用 TIE 风格、一般学术常识或语言润色补造事实。**

### 2.3 作者明确确认的 response plan

决定当前任务中已经确认的：

- scientific mainline；
- concern decomposition；
- 必要的推理依赖；
- 明确指定的主要回答顺序。

只记录作者真正确认的约束。作者仅列出若干待回答事项时，不自动把其排列顺序冻结为写作顺序。

若作者方案与 reviewer concern、primary evidence、数学正确性或可支持的 claim 明确冲突，不静默改写，也不机械照做；指出冲突并等待裁决。

### 2.4 `Response_TIE_江_No.17-TIE-2621.pdf`

是本项目 **Response organization / expression 的唯一原始写作金标准**。

它用于判断和学习：

- 如何理解并组织一条 reviewer response；
- 信息如何排序和推进；
- Part、Paragraph 和连续句如何承担不同功能；
- 实验、推导、比较、图表和修改位置如何进入回复；
- 句法、措辞、节奏和语气如何实现。

TIE 中的原始缺陷、漏答、错号、非地道表达或过强 claim 不因来自范例而自动成为可迁移规则。

### 2.5 `03_最终知识库/00–08`

是已经提炼、验证并供 Agent 直接调用的正式知识层。

它负责把 TIE-derived 规律组织成可执行规则，但**不能覆盖 TIE 原文，也不能替当前项目材料决定事实**。

### 2.6 TIE 构建与验证材料

包括 scene corpus、sentence-realization baseline、mechanism candidates、mechanism validation 及相关 provenance 材料。

它们用于：

- 理解最终知识的来源和适用边界；
- 对可疑规则进行溯源；
- 审计知识是否正确提炼；
- 在需要时辅助判断当前写法是否真正符合 TIE。

这些材料可以在分析、写作或审计中按需查阅，但其作用是**证据与解释**，不能把单例 scene 直接升级成通则，也不能绕过最终知识库的既有验证边界。

### 2.7 Nature Skills / Academic Research Suite

只可借鉴：

- 知识组织方式；
- 分阶段执行；
- source / evidence / claim discipline；
- validation、QA、handoff 等知识工程方法。

**不得提供或覆盖 TIE 的 Response 文风、句式、组织规律，也不得建立第二套写作体系。**

---

## 3. Agent 工作流程

开始任何任务前，先判断本轮属于哪一种模式：

**Audit / Knowledge-base Update / Response Drafting / Response Audit / Point Fix / Repository Operation**

只完成用户要求的当前阶段，不自动推进下一阶段。

### 3.1 理解任务与材料

1. 读取本文件。
2. 读取用户本轮明确指定的材料。
3. 按文件导航读取与当前任务直接相关的知识；不要无目的遍历整个仓库。
4. 区分：
   - 项目事实；
   - 作者确认的 scientific route；
   - TIE-derived 写作知识；
   - supporting QA 规则；
   - 历史状态或 handoff。

### 3.2 理解 Comment

正式写作前必须先形成内部判断：

1. reviewer 真正关心什么；
2. 是否包含多个独立 concern；
3. reviewer 最终需要接受哪些**核心判断**；
4. 每个判断需要什么事实、动作或 evidence 才成立；
5. 这些判断之间有什么前后依赖，应该按什么顺序回答。

不要把“逐项列出问题”误当成已经完成整条 Response 的逻辑设计。

### 3.3 自上而下规划 Response

在写英文前，依次完成：

1. **Whole Response**：整条回复最终要解决什么，核心论证主线是什么；
2. **Part**：需要几个实质部分，每部分承担什么独立职责，前后为什么这样排列；
3. **Paragraph**：每个 Part 需要哪些段落，每段只推进什么主要判断，段间如何承接；
4. **Continuous Sentence Sequence**：每段从第一句到最后一句如何连续推进；
5. **Sentence / Wording**：再决定主语、核心动词、时态、限定语、连接方式、句式和具体用词。

Part、Paragraph、句子数量都由当前 reviewer concern、证据和 TIE 规律自然决定，**不得预设固定数量或模板**。

### 3.4 起草

起草时同时满足：

- 事实完全来自当前项目可核查材料；
- 科学主线服从作者已确认且无冲突的 response plan；
- 尚有自由度的组织与表达按 TIE-derived 规律决定；
- 语言朴素、准确、简洁、专业；
- 连续句之间存在真实的认知和逻辑推进；
- 图、实验、推导、比较和 manuscript location 只在 reviewer 理解所需时进入正文；
- 内部分析可以细，但 reviewer-facing Response 只保留**最小充分信息**，不得机械外显分析过程。

### 3.5 修改知识库

只有在发现**有证据支持、可迁移、会影响未来任务**的真实缺口时，才修改最终知识库。

先判断缺口属于：

1. **Knowledge gap**：TIE 的稳定规律尚未被正确提炼；
2. **Execution gap**：知识已经存在，但 workflow 没有正确调用；
3. **Representation / usability gap**：知识存在，但组织方式使 Agent 难以可靠理解或使用。

修改原则：

- 优先最小定点修正；
- 已验证且无真实缺口的内容保持冻结；
- 当前任务中的 failure 只作为诊断线索，不能自动升级为通则；
- 新规则必须有 TIE 或既有验证材料支持；
- 不因“还能优化”而扩大修改范围。

---

## 4. 长期硬约束

以下规则长期有效：

- 不把当前 C1/C2 或任何其他单例任务的具体 failure、变量、实验、段落形态或修法直接泛化为通则。
- C 类单例证据只能保持其已验证边界；不得因为某一 scene 写得完整，就复制其固定段数、图数或完整路径。
- 不建立固定 Part 数、Paragraph 数、句数、开头模板或结尾模板。
- 不把 TIE 的具体原句当 phrasebook；迁移的是稳定的功能、组织、推进和语言实现规律。
- 不把 TIE 原文中的错误、漏答、错号、非地道表达或过强结论当作风格规则。
- 不用 Nature Skills / Academic Research Suite 的文风覆盖 TIE。
- 不用一般 academic-writing 偏好推翻已有 TIE-derived 证据。
- 不把内部分析、分类、scope reasoning 或 process preview 机械写进 reviewer-facing Response。
- 不为了显得“完整”而重复 evidence、scope、disclaimer、Case identity 或已经回答过的内容。
- 不补造实验、结果、citation、figure、line/page、修改状态或 reviewer 意图。
- 不因存在“还能更好”的空间判定 FAIL；只有真实 blocker 才阻止进入下一阶段。
- 不在未授权时扩大任务范围、重构无关文件或顺手清理仓库。
- 不自动从 Audit 进入修改、从修改进入 Response 写作、从验收进入 Git 发布；除非用户当前任务明确要求。

---

## 5. 文件导航

### `03_最终知识库/`

正式运行知识。优先按职责定位，不重复全量读取。

- `00_使用说明与来源职责.md`：知识库定位、来源职责、调用边界。
- `01_TIE_Response_核心逻辑与组织.md`：Response 主线、功能块、段落与组织规律。
- `02_TIE_表达_句法_语气.md`：连续句、单句、句法、措辞、语气和节奏。
- `03_实验_结果图_Caption.md`：实验、结果、图、caption 与正文协作。
- `04_证据_Claim_术语_引用.md`：evidence、claim、数学正确性、来源、术语与引用一致性。
- `05_错误模式与负例.md`：已验证的错误模式和禁止路径。
- `06_Response生成与验收流程.md`：正式生成和验收 workflow。
- `07_条件型补充规则.md`：仅在对应条件触发时调用。
- `08_阶段3验收与候选映射.md`：历史候选、验证与映射记录；不得用历史 PASS 覆盖新的真实 failure。

### `04_TIE句子级表达重建/`

TIE 写作规律的构建、scene、realization、candidate、validation 与 provenance 材料。  
主要用于溯源、研究、审计和必要的写作核查，不得把单例直接泛化。

### TIE PDF

`Response_TIE_江_No.17-TIE-2621.pdf` 为原始写作金标准。若派生总结、知识条目或解释与 PDF 明确冲突，以 PDF 为准，并记录该冲突。

### 当前任务材料

当前 manuscript、reviewer comment、Response 草稿、作者思路、实验结果、图表及修改记录以用户本轮指定的真实文件为准。  
不要根据旧版本、相似文件名或历史 handoff 猜测当前事实。

---

## 6. 验收规则

验收必须与生成使用**同一层级**，从整体到局部进行：

### 6.1 Whole Response

检查：

- 是否准确回答 reviewer 真正关切；
- 是否形成清楚、有证据支撑的核心判断链；
- 回答顺序是否符合当前问题的认知依赖和 TIE 的组织习惯；
- 是否存在漏答、错答、无关展开或重复。

### 6.2 Part

检查：

- 每个 Part 是否有明确且独立的整体职责；
- Part 之间是否存在合理的前后关系；
- 是否有两个 Part 实际重复同一任务，或一个 Part 混入多个无关任务。

### 6.3 Paragraph

检查：

- 每段整体要表达什么是否明确；
- 是否主要推进一个可判断的内容；
- 段首、段中证据与段尾/下一段之间是否形成自然推进；
- 段落数量和边界是否由内容需要产生，而非模板产生。

### 6.4 Continuous Sentence Sequence

逐段从第一句顺读到最后一句，检查：

- 每一句为什么出现在这里；
- 是否回应上一句留下的实际需求；
- setup、evidence、observation、explanation、inference、location 等是否按真实逻辑推进；
- 是否出现跳步、重复、突兀转折或局部正确但整体失序。

### 6.5 Sentence / Wording

检查：

- 主语与核心动词是否承担正确语义责任；
- 时态、限定条件、baseline、metric 和 comparison 是否准确；
- 连接词是否表达真实关系；
- 技术术语和指代是否稳定、唯一；
- 用词、句式和语气是否朴素、自然、专业，并符合顶刊论文与 reviewer response 的实际表达习惯；
- 不复制 TIE 的 source defects。

### 6.6 Supporting Gates

同时必须通过：

- concern completeness；
- evidence sufficiency；
- claim boundary；
- 数学与技术正确性；
- source / citation 可追踪性；
- 图号、表号、公式、术语、数值和版本一致性；
- reviewer-facing necessity；
- 历史错误模式检查。

### 6.7 PASS / FAIL

- 只把会影响正确性、完整性、TIE 风格一致性或后续执行可靠性的真实问题视为 blocker。
- “还可以更优雅”“还能再润色”本身不是 FAIL。
- 无 blocker 时直接 PASS，并停止无边界优化。
- 若某一层失败，先定位该层的根因，只修该层及其受影响链条；不要默认整篇重写。

---

## 7. Git 工作流

仅在当前任务要求仓库修改或发布时执行 Git 操作。

标准流程：

**inspect → modify scoped files → diff → validate → commit → push**

具体要求：

1. 先检查工作区状态，识别用户已有的未提交修改。
2. 只修改本轮授权范围内的文件；不得覆盖、reset、丢弃或顺手整理无关改动。
3. 修改后先查看相关 `git diff`，确认实际变化与任务目标一致。
4. 完成内容验收和必要检查后再 commit。
5. commit 只包含本轮相关文件，message 准确描述实质修改。
6. Push 行为按本文最后的“自动提交与推送”规则执行。
7. Git 操作失败时报告真实状态，不通过强制 push、reset 或重写历史来“解决”。

---

## 8. 执行停止条件

Agent 在满足当前任务目标后立即停止。

特别地：

- Audit 完成后，不自行修改；
- Knowledge-base Update 完成后，不自行进入 Response 修改；
- Response Draft / Point Fix 完成后，不自行宣布最终 PASS；
- Validation 只报告真实 blocker；无 blocker 即 PASS；
- Git 发布完成后，不继续做额外清理或优化。

任何阶段都以**准确、完整、最短充分**为原则：明确核心目标、必要内容、准则和约束；不重复、不空泛、不预设可由 Agent 根据实际材料可靠推导的无关细节。

## 9. 自动提交与推送

凡本轮任务实际修改了仓库文件，任务完成并通过必要检查后，默认自动完成本轮相关修改的 commit，并执行 `git push`。

除非用户本轮明确要求不提交或不推送。

只提交本轮相关修改，不包含用户已有或其他无关改动。禁止 force push、reset、rebase 或其他改写历史的操作。

若 commit 或 push 失败，报告真实错误和当前状态，不得声称已成功同步。

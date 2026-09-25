# Response 生成与验收流程

这是未来 Agent 的主执行入口。流程以一条 comment 为单位运行；多位 reviewer 或复合 comment 的附加处理见 `07`。

## SD-04 surgical audit 与完成门槛

SD-04 贯穿全流程：发现问题后先定位其所在层级，检查有证据定义的同类位置，只修改该层及受影响链条；完成后分别报告写作、事实、版本和提交状态，不把其中一种通过冒充全部完成。

## Step 1 读取并锁定材料

保留 reviewer comment 原文。识别当前稿件版本、正式实验/图表、作者确认的动作、可核查修改位置和外部来源；同时识别是否存在作者明确确认的 project-specific response plan 及其确认范围。先写清各来源职责；若版本关系不明，不进行精确编号或完成声明。

**产物：** comment 原文、source map、当前版本标识、作者方案的确认状态、未决事实。

## Step 2 建立 concern card

建 card 前先顺读 reviewer 的完整 argument：辨认用于支撑质疑的事实、比较与推理，读出 reviewer 据此形成的判断，再确定真正要求作者回答、解释、证明、补证据或修改的 response obligations。论据不因单独成句就自动成为新 concern；只有它本身要求处理，或不处理就无法闭合最终质疑时，才纳入核心回答链。内部可记录必要论据的核验任务，但不据其数量决定 Part 或段数。

用最少字段记录：

- reviewer 真正要判断什么，以及必须分别闭合的 response obligations；
- reviewer situation 属于 B1 局部 correction、B2 局部 equation/definition、B3 缺推导、B4 新实验、B5 comparison、B6 多 concern 中哪一种或哪几种；
- 一句话直接答案；
- 支撑直接答案所需的核心判断及其初步先后依赖；数量由 concern 和证据决定，不把内部判断列表写成对 reviewer 的固定提纲；
- 需要什么动作或直接 evidence；
- conclusion 在什么条件下成立；
- 稿件改动或位置；
- 当前状态是已核验、仅报告未核验、计划中还是缺失。
- **project-specific response constraints：** 只记录作者明确确认的 scientific mainline、concern decomposition、主要先后关系和必要推理依赖；未明确规定顺序时，不自行补成顺序约束。

若 comment 含多个独立 response obligations，触发 CS-01。不要把广义 concern 缩成最容易回答的一小部分，也不要把每项 supporting premise 机械拆成独立要求。此时按已验收 realization 基准选 A1–A6 的跨场景关系和实际触发的 B1–B6；核心 proof、novelty、完整多控制器比较、method motivation、明确 Table 请求或定量噪声链若只匹配 C1–C6，回查原 scene，不能按单例生成固定路径。

## Step 3 做 evidence gate

对每个 concern 执行 SD-01：判断标准、动作、evidence 和 claim 是否直接对应。

- evidence 足够：进入组织。
- 只部分覆盖：明确已覆盖与未覆盖部分，并缩小 claim。
- evidence 缺失：保留可见缺口或作者输入需求，不起草完成式语句。
- 存在实质不利结果：保留，并据此校准 conclusion。

## Step 4 规划 TIE-native 主干

先核对拟采用的组织是否改变 Step 2 记录的 project-specific response constraints。若作者方案与 reviewer 原 concern、Step 3 的 evidence/claim 检查、数学事实或前后逻辑发生明确冲突，标记冲突及原因，保留原方案并等待作者决定；不得静默重排，也不得机械照写。只有作者未规定该处顺序，或用户明确授权重新优化方案时，才由 TIE-native 机制选择主要先后关系。

1. **整条 Response：** 用 Step 3 的 evidence gate 修订 Step 2 的初步核心判断，先确定直接回答、必需判断及其有序关系，再决定整条回复如何从实质入口走向证据或解释。按作者已确认的项目路线保留必要先后；其余顺序由 reviewer 的判断需求、理解依赖和 TN-02 决定。用 TN-01/A1 规划尽快进入实质；必要的最小框架可以先于细节，不表示所有 action/evidence 都应提前。
2. **各 Part：** 为每个实际需要的 Part 确定整体回答任务、所承接的前一状态、若有后一 Part 时需要交接的问题，以及对应的核心判断和证据。按所触发的 B 规划尚有自由度的功能块：B1 对象/修改/可查表达；B2 修订/局部关系/新式；B3 前提/中间式/末步依据；B4 action/setup/locator/observation；B5 baseline capability/区分维度；B6 一个实质块转另一个实质块。B6 识别的是实质功能，不凭某项 manuscript action 看起来独立就切断作者明确确认的同一科学回应链。C1–C6 只供回查，不给固定组织。
3. **各 Paragraph：** 在每个 Part 内先确定各段要完成的局部判断或推进动作、需要的理由或 evidence、段间如何承接，再决定是否需要下一段。用 TN-03 把同一子问题下实际需要的实验、推导或图表组成 evidence blocks；用 TN-04/05 规划 figure、caption、正文与 observation。Part 和 Paragraph 的数量及形式由实际任务决定，不预设标题、编号或篇幅。
4. **段内连续句：** 在写英文前，按本段任务规划第一句如何进入实质、后续句分别回应前句留下的什么需求、何时进入条件、推导、设置、图表、观察或可查位置，以及本段如何结束或交给下段。此处只确定语义推进，不预设句数或套用连接词。
5. 若确需结论，调用 TN-07 与 SD-01 检查其直接证据、范围及非重复；不为每个 block 强制生成 conclusion。用 TN-08/A2 按独立任务数量估计功能块和篇幅，不从作者的停止位置推断充分覆盖。

先完成这一步，再写英文；不要从 phrase 开始拼接。

## Step 5 起草

沿 Step 4 已确定的整条逻辑、Part/Paragraph 职责和段内连续推进，从各段第一句起草到该段任务完成；每句均须接续前句留下的实际问题，或明确进入下一局部任务。逐句按 `02` 的 SL-01 至 SL-11 落实句法与用词。根据 reviewer situation、当前段落任务和上一句留下的 semantic state 确定下一句的认知任务，再依次决定：

1. 谁承担语法主语：作者动作、技术对象、display evidence，还是对紧邻证据的 inference；
2. 使用哪个具体动作/关系动词，以及 completed revision 与稳定事实所需的时态；
3. 条件、baseline、metric、definition 和 location 放在哪个紧邻槽位；
4. 前后句是 uptake、原因、增加、转折、实例、推论还是定位关系；
5. 核心技术名词是否准确复现，代词和 `this/these/the above` 是否只有一个清楚先行项。

关键量首次进入正文时，用当前项目确定的技术名称与正式符号建立对应；后文在新的 Paragraph/evidence block、关键 criterion、主要结果读取、comparison、claim 或 conclusion 处，按 reviewer 的阅读需要就近保留“含义＋符号”，紧邻重复或局部公式推导可简化。选择每个条件、方式、比较和范围短语时，同时调用 `04` 的 SD-01/SD-03：它修饰哪个实际对象、操作、测试条件、baseline 或 metric，覆盖哪些 evidence，支持多强的 claim。`with/under/by/across/all/selected/generally/respectively` 等词只有与 primary evidence 的真实关系一致时才可使用；不能让语言顺畅掩盖实验层级或 scope 的变化。

礼貌承接后尽快进入可回答的对象、技术事实或动作；purpose 仅在有实际解释作用时出现。新增实验由 action 进入具体 setup、locator 和 observation；结果句显化有歧义的对象，Figure/Table 不必作语法主语，也不要求每个结果都给数字。条件与 baseline 贴近受其限定的 claim 或比较维度，术语连续复现，连接词只标真实关系；location 可在摘录或证据前后。若写结论，在该句同步按 SD-01 核对证据范围，并于 Step 6 汇总跨句 claim 检查。句法槽位用于组织信息，不从 TIE 抽取整句模板。

上述有序判断、Part/Paragraph 划分和逐句规划均是内部生成机制，不得机械外显为 reviewer-facing 的论点清单、标题或流程预告。对准备进入最终 Response 的每句话或信息，判断它是否真实帮助 reviewer 回答当前 concern、理解必要逻辑或 evidence、判断或限定 conclusion、消除真实歧义、核查 evidence 或 manuscript revision 的具体位置，或承担必要且简短的礼貌承接。有真实功能则保留最小充分表达；功能成立但表达过量则压缩；只对内部分析、规划或审计有用则删除。**内部分析需要 ≠ reviewer 必须看到。**“下面我们将……”等流程预告不能仅凭宽泛的“导航”作用保留；帮助 reviewer 核查 evidence 或 manuscript revision 的具体定位可以保留。

起草时不复制 TIE 句子，不补造实验、结果、citation、figure、line/page 或修改状态。

## Step 6 两层审计

进入两层审计前，先核对项目路线：

- response 是否忠实实现作者明确确认的 scientific mainline、concern decomposition 和主要先后关系？
- 是否有 TIE-native 的一般倾向擅自重排了已明确指定的项目关系？
- 是否把作者仅列出的事项或未确认的建议错误冻结为顺序约束？

### 6.1 TIE-style audit

严格按下列层级自上而下检查。每层先判断其任务是否完成，再按相应 reviewer situation 对照已验证的 TIE A/B 机制和作用相近的 scene；C1–C6 仅作单例参考。上层未通过时，不以局部句子流畅代替上层修复；发现问题只回到该层及受影响链条。

1. **整条 Response：** 是否先正确还原 reviewer 的完整 argument，区分 supporting premises 与真正的 response obligations，再准确回答其真实关切；有序核心判断和整体逻辑是否由当前问题、证据与已确认的项目路线支持；首段是否尽快落到答案、动作或核心 evidence？
2. **各 Part：** 每部分是否承担明确的整体任务、对应必要的核心判断；前后 Part 是否接续实际理解需求或转入另一实质任务，而非只靠编号、连接词或动作发生次序；evidence blocks 是否集中公共信息且保留独有 evidence？
3. **各 Paragraph：** 每段是否有清楚的局部判断或推进动作，所需理由、推导或 evidence 是否放在恰当位置；段数与分段是否由任务决定，段尾是否自然完成本段任务或交给下段？有图表时，figure、caption 与正文是否各司其职？
4. **段内连续句子：** 从第一句顺读到最后一句，下一句是否回应前句留下的实际问题；必要条件、前提、setup、locator、observation、推论或修改位置是否无跳步地接续？有图表时是否从 locator 读出具体 observation；location 或摘录是否可追溯且未被固定为末句？
5. **单句与具体用词：** 对每句、每个会改变科学含义的关键 phrase，**同时调用 `02` 的 SL 语言实现与 `04` 的 SD-01/SD-03 科学核对**。主语、核心动词、时态和连接词是否承担正确语义责任；关键位置的技术含义与符号是否可直接读懂，回指是否唯一？实际实验对象、测试条件、baseline、metric、modifier scope、evidence range 和 claim scope 是否与 primary evidence 一致；范围词或介词短语究竟修饰什么，有无把 parameter/setting 改称其他实验层级或扩大 evidence？每句话或信息是否通过 Step 5 的 reviewer-facing necessity gate，并避免把内部规划机械外显？**语言 realization 与 evidence-semantic correctness 均通过，单句层才可 PASS；语法自然不能代替科学附着核验。**

### 6.2 supporting audit

此处汇总跨句、跨图表和整条回复的事实与质量门槛；不替代 6.1 第 5 层已经同步执行的 phrase-level 科学核对。

- 所有 concern 是否各有直接 evidence 或显式缺口？
- 若有 conclusion，claim 是否超出测试/证明范围；是否隐藏会改变 claim 的实质不利结果？
- 定义、维度、时间区间、量词、条件及每步等式/不等式是否数学成立？
- source 与 citation 是否可追踪且未越权？
- 术语、符号、图号、Table、panel、数值和位置是否与最新 artifact 一致？
- 语言、搭配或重复是否把 TIE 原文的 source defect 带入新 response？
- 是否命中 `05` 中的历史错误模式？

## Step 7 完成判断与停止

分别给出四种状态，不得混写：

1. **response writing**：逻辑、组织、表达是否通过；
2. **fact/evidence**：所有动作、结果、claim 是否已由 artifact 核验；
3. **version/package**：response、稿件、图表、caption、citation 与定位是否同步；
4. **submission readiness**：是否仍有 placeholder、未决证据、未编译/未视觉核对或其他阻塞项。

只有约定范围全部核验后才能宣布完成。通过后，除非出现新 evidence、明确缺陷或用户新要求，不再以一般写作偏好继续重写。这是项目执行与交付的停止规则，不是江 TIE_2621 作者“充分覆盖后才停”的 A2 fingerprint。

## 同类问题回查规则

当用户或审计发现一个缺陷：

1. 把缺陷定义为可识别类别，例如“多先行项时的模糊指代”；
2. 只搜索受该类别影响的范围；
3. 定点修复所有同类实例；
4. 重开相关 evidence、交叉引用和版本同步检查；
5. 不修改已经正确且不受影响的内容。

**Provenance:** CK-002、CK-019；CK-013/014 提供 source 与 consistency 边界；Nature/ARS 只支持 action、work status、readiness 分离和可核验完成。

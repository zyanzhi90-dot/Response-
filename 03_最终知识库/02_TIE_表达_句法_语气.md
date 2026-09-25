# TIE 表达、句法与语气

## TN-06 句子功能与节奏

TIE 风格的可迁移部分不是某组固定短语，而是句子功能清楚、连续句之间有明确任务关系。先由 reviewer situation 和当前功能块判断上一句留下的认知需求，再决定下一句的语义责任、主语、动词和句法。信息密度随任务变化，不规定每句必须承载固定数量的功能。

阶段 3B 在 TN-06 内增加 **11 个 sentence-level language units（SL-01 至 SL-11）**。它们回答“这个功能具体怎样写”，但不改变 `01` 已确定的信息顺序和证据链。下文出现的方括号结构是句法槽位，不是可直接复制的模板。

下文所称 **TIE 稳定倾向**，是指 PDF 中多个 response 上下文反复呈现的功能—语言对应；为剔除原文自身的语法问题、非地道搭配或过强 claim 而给出的自然化写法，仅是**最小专业化修正**，不属于 TIE 原句或额外的 TIE 语言指纹。

## 1. 使用入口：从 reviewer situation 和 semantic state 调用 SL 单元

先按 `01` 判定 B1–B6 的功能块，确认当前句群下一步需要 action、局部解释、推导、setup、locator 还是 observation，再用本表把 sentence intent 路由到 SL-01～SL-11。本表不构成第二套 response organization 规则。

| 功能 | 这句话要完成什么 | 常见位置 | 主要调用 |
|---|---|---|---|
| 礼貌承接 | 简短认可 reviewer 的实质 concern 或建议 | response 首句 | SL-01 |
| 直接答案 | 给出该 concern 在当前证据下的回答 | 首段前部 | SL-02、SL-10、SL-11 |
| 动作句 | 说明已纠正、增加、比较、推导或测试什么 | 首段或子问题开头 | SL-03、SL-04 |
| purpose 句（若需要） | 说明后续 evidence 为什么存在、检验什么 | 需要显化检验目的时 | SL-07、SL-09 |
| 设置句 | 给出理解 evidence 所需的对象、指标、条件和基准 | 实验动作后、locator 前；可与动作相邻 | SL-05、SL-07 |
| 结果读取句 | 明确对象在给定指标和条件下呈现什么现象 | 图表或公式附近 | SL-04、SL-08、SL-10 |
| 结论或定位句（若需要） | 对已读 evidence 作有依据的推论，或指出真实修改位置 | 由 concern 和修订位置决定，可在摘录前后 | SL-10、SL-11 |

若一句无法归入这些功能之一，通常是可删的元话语、重复背景或无关细节；若删除会使推理跳步，则应改写为上表中的明确功能句。

## 2. 十一个可迁移的 sentence-level language units

### SL-01 一句礼貌承接，并立即交棒给实质

**适用功能：** 每条 response 的礼貌入口；纯赞许 comment 可在此结束。

**信息组织：** 通常用一个 `thank/appreciate + reviewer + for + 具体 comment/point` 结构完成礼貌，不在同一句中加入背景、证据和结论。除纯赞许 comment 可在此结束外，下一句通常直接进入答案、动作或 concern uptake。

**专业表达选择：** 保持普通动词和短名词组。`constructive comment`、`helpful comment`、`recognition` 在 TIE 中反复承担的是礼貌标记，而不是科学评价；未来写作不需要轮换同义词来显得华丽。

**衔接：** 礼貌句本身不制造推理前提，因此不能仅用 `Therefore` 把感谢与实质内容连成因果。后句通常直接进入 `We have...`、`We agree that...` 或具体技术对象。

**不可迁移：** 连续使用 `sincerely`、`very much`、`which is appreciated` 等多层强化；在条目末尾再次感谢；把感谢句扩成作者态度说明。

**TIE anchors：** R1-1、R4-1 展示一句结束；R1-2、R2-1 至 R2-6、R4-2 至 R4-6 展示感谢后转入动作。

### SL-02 用 concern uptake 建立“为什么要回应”

**适用功能：** reviewer 的 concern 合理，且其重要性是后续动作的直接理由。

**常见句法形态：** 可用 `We agree that [concern-relevant proposition], since/because [project-specific reason].`；也可用 `As the reviewer pointed out, [precise proposition]` 承接。它们是 TIE 中可观察的实现方式，不是每次 uptake 的固定开头；主句应确认具体问题，而不是泛泛赞扬 reviewer。

**词汇选择：** 复用 comment 和稿件中的准确技术名词；使用 `important` 之类朴素评价词时，应就近给出原因。TIE R1-2 的“考虑 measurement noise 很重要，因为真实传感数据受噪声影响”体现了这一结构。

**衔接：** 理由之后紧接动作句，形成“concern 的现实/理论意义 → 作者做了什么”。若没有真实认同或该理由不推进 evidence，省略 uptake，直接报告动作。

**不可迁移：** 用一整段领域背景表达认同；把 `As the reviewer pointed out` 当作每条回复的固定开场；先承认 reviewer 再悄悄缩窄其 concern。

**TIE anchors：** R1-2、R3-1、R4-5。R3-1 的背景过长，只支持“准确承接前作/concern”的功能，不支持其篇幅。

### SL-03 用具体动作动词报告已完成修改

**适用功能：** 纠错、补充推导、增加实验、改图、加入文献或修改正文。

**主语与语态：** 当作者的决定和动作是焦点时，TIE 常用 `we have + 过去分词 + 具体对象`；当修改对象是焦点时，也常用 `[specific artifact] has/have been + 过去分词`。两种形式都出现，选择取决于信息焦点；主动、被动均不是唯一正确形式。

**时态：** 对已完成且可核验的 revision，present perfect 是 TIE 的稳定倾向；对论文中的稳定事实、公式关系和图中现象，present simple 是常见选择。若时间关系或句法环境另有要求，可采用其他合乎事实的时态；未完成工作不能套用完成式。

**动词类型：** 从动作本身选一个足够具体的动词，如 `corrected`、`rewritten`、`added`、`derived`、`conducted`、`presented`、`discussed`、`cited`。宾语写出被改的 statement、equation、figure、analysis、test 或 comparison。

**衔接：** 可在句首用简短 request-uptake adjunct 指明这是对 comment 的响应，随后立即写动作和对象；下一句给内容、evidence 或位置。

**不可迁移：** `modified and updated`、`conducted and performed`、`read, checked and polished` 这类同义动作堆叠；只写 `the manuscript has been improved` 而不说改了什么；用完成式掩盖未核验状态。

**来源边界：** 上述主语焦点和 present perfect/present simple 分工来自 TIE 的重复用法；删除双动词、修正主谓与完成式误用属于最小专业化修正，不应反向标注为 TIE 原文指纹。

**TIE anchors：** R1-3、R2-1、R2-3 至 R2-6、R4-2a/b、R4-3、R4-6。

### SL-04 让语法主语随证据责任变化，并保持术语复现

**适用功能：** 在作者动作、技术事实、display evidence 和推论之间切换。

**常见主语分工：**

- `we/the authors` 常承担选择、修改、测试和报告等可归责动作；
- 技术对象常承担定义和性质，如 `[matrix/condition/method] is/satisfies/requires...`；
- `the results/Fig./Table/the comparison` 常承担展示或报告；
- `this/these` 适合承担对紧邻前文的归纳或推论。

**词汇连续性：** TIE 在证明中持续复现 `PE condition`、`matrix D`，在实验中持续复现 `disturbance`、`estimation results`、`comparison results`。可迁移的是准确重复核心技术名词，而不是为避免重复轮换近义词。

**符号可读性：** 关键量首次进入 reviewer-facing prose 时，给出来自当前项目材料的清楚技术名称与正式符号；之后保持同一名称与符号的对应。在新的 Paragraph 或 evidence block、关键 criterion、主要结果读取、comparison、claim 和 conclusion 等需直接判断含义的位置，优先让技术含义与符号同时可见，不让连续表述退化为裸符号解码。紧邻重复、局部公式推导或上下文已无歧义时可只用符号；不要求每次重写全称。TIE 的技术名词连续复现支持可读性选择，具体名称与符号仍由当前项目证据决定。

**衔接：** TIE 常借主语变化标记段落阶段：作者动作 → 技术对象/设置 → evidence → inference；这是一种清楚的推进倾向，不要求每段逐项复现。只有先行项唯一且紧邻时，才宜用代词或 `this/these`。

**不可迁移：** 同一技术对象在近义词间漂移；多先行项后使用 `it/this/those`；每句都用 `we`，使 evidence 看起来只是作者判断。

**TIE anchors：** R1-2 的 tests/disturbances/results 链；R2-2 的 PE condition/matrix D 链；R3-2 与 R4-6 的 comparison/table 链。

### SL-05 用主句识别对象，用附属结构定义而不扩写

**适用功能：** 定义符号、说明公式构成、列出 table schema、区分有序对象或给出必要条件。

**常见句法形态：** TIE 多次先用主句完成关系判断，再用 `where` 定义符号、用 `with/under` 附加条件，或用平行结构列出对象。也可拆成相邻短句，只要关系与限定仍清楚。`respectively` 只在两组顺序完全可恢复时使用；旧/新编号可在对象后用简短 parenthetical 对应。

**词汇选择：** 优先 TIE 原文反复使用的 `is`、`satisfies`、`is defined as`、`is of the form` 等透明关系表达；定义句不需要 `novel`、`advanced` 等评价词。

**节奏：** 一个主句识别一个对象；多项定义保持平行语法。若 `where` 从句承载了新的推论或过多对象，拆成后续句。

**不可迁移：** 以 `Generally`、`It is well known that` 等宽泛起句代替当前定义；模糊的 `the above-mentioned equation`；顺序不清仍使用 `respectively`。

**来源边界：** `where/with/under` 等透明关系表达是 TIE 可迁移的稳定观察；避免空泛垫句、修正搭配和在必要时拆句，是为保证专业英语与指代清楚所做的最小规范化。

**科学附着：** `with/under/by` 等结构除了语法通顺，还必须确实修饰所写的对象、操作或条件；`respectively` 所连的两组对象须与实际 evidence 一一对应。用 `04` 的 SD-01/SD-03 核对这些关系，不从介词形式推断实验层级或证据范围。

**TIE anchors：** R1-2 的 disturbance 定义，R2-3 的 SVD 矩阵定义，R2-5 的 auxiliary term 与两类 eigenvalue，R4-6 的表格列说明。

### SL-06 让局部推导的前提、中间式和末步依据连续

**适用功能：** reviewer 指出具体等号或不等式缺少中间步骤时的局部推导。核心 proof challenge 的完整组织仅是 C1 参考。

**连续状态：** 被问的式号及所用前提或恒等式 → 必要的连续中间式 → 末步所用事实或新符号。S06 的等号链与 S08 的不等式链共享此组织；实际缺哪一步决定说明句和公式的数量。`From/Since` 可引前提，`obtain/derive` 可对应具体操作，`This implies` 仅在前文确实推出该结论时出现；它们不是固定四句话。

**动词与时态：** TIE 通常用 present simple 描述恒等式和逻辑关系；`obtain/derive/rewrite/imply/satisfy` 可直接对应推导动作。能写出具体 operation 时，不宜用空泛的 `it can be clearly seen`。

**衔接：** 新句或公式接续刚建立的关系，缺失的运算在式链中可逐步核查；location 可以先于摘录/式链，也可以在其后。句间组织不能代替 `04` 的数学正确性核查。

**不可迁移：** 连续多句机械重复 `we can obtain that`；把多个代数步骤压在一个逗号长句中；条件尚未建立就使用 `therefore`；把有条件命题写成无条件性质。

**TIE anchors：** R2-2、R2-4、R2-6。

### SL-07 由实验动作进入具体设置、证据定位与观察

**适用功能：** 新增 experiment 的 evidence block；comparison 的 baseline 与差异另由 B5 决定。

**句间状态：** 已做 test/experiment → 具体通道、强度、公平条件或平台与任务 → Figure/Table locator → 可观察的结果。若检验目的尚不清楚，可在动作前或动作句中说明；R4-3 直接由实验动作进入平台和任务，故不以 purpose-fronting 规定入口。设置可用 `in/under/with`、变量赋值句或公平比较句实现，按实际实验选择。

**动词选择：** `conduct tests/comparisons`、`add disturbances`、`compare methods`、`present/show results` 等 TIE 原文动作与实际操作一一对应。公平比较可用独立句或清楚的附属结构说明哪些条件保持一致。

**衔接：** action 需要 setup 才能解释图表；locator 告诉读者看哪里，随后 observation 读出可见变化。若目的或设置已由上下文明确，可压缩相应说明；B4 的稳定链止于 observation，结论及其范围另审。

**不可迁移：** 把 TIE 的 `To further show/verify...` 固定复制到每个实验；在 evidence 尚不足时使用 `verify`；用 `Next/Finally` 只报操作顺序；用不必要的 `Without loss of generality` 装饰普通实验设置。

**TIE anchors：** R1-2、R3-2、R4-3。

### SL-08 清楚定位 figure/table，并以可核验对象读结果

**适用功能：** 图表进入、panel 对应、数值/趋势读取和表格比较。

**常见句法形态：** TIE 可让 `results/disturbances/performance` 等证据对象作主语，用 `shown/depicted in Fig./Table` 定位；Figure/Table 常位于介词短语中，也可按本句责任作主语。随后由 measured object、method、result 或 `we` 读出方向、数值或条件关系。若 locator 与 observation 在一句中仍无歧义，也可合并；图号/panel 不能替代可核验的结果内容。

**词汇选择：** `show`、`present`、`depict` 可用于 display；结果句宜使用可测关系动词和比较级，并在必要时显式给出 metric/condition。TIE 原文也出现 `we can see/observe`；在易产生主观或空泛感时，改由 `the results` 或具体 measured quantity 作主语，是最小专业化修正，而不是 TIE 唯一的主语形式。

**衔接：** 已验证的子链是 locator → observation；是否再作 inference 取决于当前 concern 和证据范围，不是固定第三步。多个 panels 共同回答一项 concern 时应先消除分工歧义，再集中读取；不同 figures 并列时写全必要引用，定性观察也可回答问题。

**不可迁移：** `As seen from the figures` 后只给抽象优越性；图前有多个 candidates 却只写 `panels (c)`；逐字复述 caption；让 `clearly`、`satisfactory` 代替指标。

**TIE anchors：** R1-2、R3-2、R4-3、R4-6。

### SL-09 连接词只标记真实的论证关系

**适用功能：** 转折、增加 evidence、切换平行方面、给例子、建立结果或由问题进入解决动作。

**功能分工：**

- `However`：已有命题与限制或例外之间的真实转折；
- `In addition/Additionally`：新增但仍服务同一 concern 的动作或 evidence；
- `On the other hand`：切换到独立的平行方面，而不是同义重复；
- `For example/For instance`：把一般机制落实为可识别实例；
- `As a result/Therefore`：前文足以推出的结果；
- `To improve/To remedy/For this reason`：从已说明的问题进入对应动作。

这些连接形式只在相应关系确实需要显化时选用；相邻句关系已经清楚时，可以不用显式连接词，也可用功能相同且语法自然的其他表达。

**句法节奏：** TIE 常把连接词放在句首或紧邻逻辑转折点，并让后文尽快出现新的明确主语。一个句子通常不叠加多个 discourse markers。

**不可迁移：** 为了“流畅”机械加入连接词；`On the other hand` 后仍重复同一方面；`Therefore` 后给未经支持的比较；照搬原文非地道的 `Comparing with`。

**来源边界：** 各连接词承担的论证关系来自 TIE 上下文；把 `Comparing with` 等非地道形式改成自然比较结构属于最小专业化修正，不构成新的 TIE 句型。

**TIE anchors：** R3-1、R3-2、R4-4、R4-5；其中 R4-4 只支持 `Additionally` 的增加关系，不支持其 evidence sufficiency。

### SL-10 比较句同时锁定 baseline、metric、condition 与强度

**适用功能：** 方法比较、效果判断和 claim strength 控制。

**信息组织：** 应先使比较对象唯一，再写 measured relation；metric 和 condition 可放在同句或可无歧义回指的紧邻句。比较结构可以前置 baseline，也可以让方法、结果或指标作主语，但不能只写 `better/faster/more efficient`。

**动词强度：** 直接可见的实验关系可用 `show`；形式推导后的逻辑结果可用 `imply/satisfy`；`guarantee/verify` 只有在 evidence 真正达到证明强度时使用。TIE 反复使用 `show/observe/verify`，可迁移的是“evidence verb 紧跟 evidence type”，不是其过强用词。

**词汇纪律：** 优先报告可测差异，少用 `superior`、`significant`、`satisfactory`、`far less` 等未量化评价。若形容词保留，必须能回指图、表、数值或条件。

**衔接：** baseline 的已有作用应紧邻真正的 comparison dimension；有图表时先定位并读取 observation。若另写 implication，其范围由 `04` 的 evidence→claim gate 核查，不作为 TIE 比较段的必需末句。

**不可迁移：** R3-1/R3-2 中无充分边界的 `superior`、`far less`、`more suitable` 和 `guarantee`；语法不当的 `in comparison with` 变体不能作为句型样本。

**来源边界：** baseline—metric—condition 的邻近组织是 TIE 比较段可迁移的功能倾向；降低无证据强化词、修正比较搭配和收紧 claim 属于最小专业化修正，不是对 TIE 原句的复制。

**范围词核对：** 在比较和结论句中，`across/all/selected/generally` 等词会改变覆盖范围或判断强度。按 `04` 的 SD-01 核对它们究竟限定哪些对象、设置、baseline 与 metric，是否对应实际 evidence range；语法自然不等于范围正确。这是科学正确性的执行 gate，不是新增 TIE 固定词表。

**TIE anchors：** R3-1、R3-2、R4-3、R4-5、R4-6；R2-2 提供数学强度的对照。

### SL-11 用紧邻回指连接推论、摘录或修改位置

**适用功能：** 需要综合推论、预告修订摘录或报告稿件位置时。

**常见句法形态：** `This/These + inference verb` 适合回指紧邻且单一的分析或结果；`the above analysis/discussion/results` 可在 block 边界压缩已经明确的一组内容。位置句常以具体 artifact 为主语并给出 verified location；主动表达同样可用。若后面给摘录，通常先用独立句说明 revised/added text follows。

**衔接：** 紧邻 evidence 可接有依据的 synthesis，修改动作可接 location 或 excerpt；S03/R2-C1 和 S06/R2-C4 的 location 在摘录/式链前，S01/R1-C2 可在结果后给位置。A6 只要求位置可追溯，不规定其为末句；是否需要 synthesis 和 response 是否充分完成由实际 concern 与独立审计决定。

**不可迁移：** 先行内容复杂时用模糊的 `the above`；把“摘录如下”和“见某页”写成逗号拼接长句；收束后重列结果、再加免责声明或重复感谢。

**来源边界：** 紧邻且唯一的回指、具体 location 的可追溯性是可迁移的表达选择；位置靠后只是部分 scene 的实现，不能作为稳定末尾规则。拆除逗号拼接、修正位置搭配和避免不实完成式属于最小专业化修正；充分覆盖后停止属于独立 completeness audit。

**TIE anchors：** R1-2、R2-1 至 R2-6、R3-1/2、R4-3、R4-6。

## 3. SL 层的统摄边界

SL-01～SL-11 是本文件唯一的 sentence-level knowledge layer。使用时只保留以下不能由单个 SL 独立承担的总原则：

- **逻辑先于措辞。** 先由 `01` 确定 concern、答案、evidence、information order 与 claim boundary，再调用相应 SL；不得为了套用句型改变事实关系。
- **功能连续，而非形式齐全。** 下一句应回答上一句留下的必要问题，但并非每条 response 都要出现感谢、uptake、purpose、figure reading、synthesis 和 location。短纠错可由动作句直接闭合，复杂证明或实验才展开相应链条。
- **节奏由任务决定。** 动作或判断宜尽早落地；必要条件、机制与 evidence 随后展开。局部问题通常短，独立任务增多时功能块和篇幅往往增加；短句、中等句和局部长句均可，TIE 的表面句长、固定语态、固定停止位置和重复短语不构成规则。完成核验后停止由 `06` 作为工作流程门槛执行。
- **语气服从证据。** 保持礼貌、就事论事和非防御；不同意时准确承接 concern，再用定义、scope 或 evidence 说明。比较与结论的强度不得超过可核验依据。
- **语言与科学关系同步。** `02` 决定句子如何实现；每个关键 phrase 的实际实验对象、测试条件、baseline、metric、修饰范围、evidence range 与 claim scope 同时由 `04` 和当前项目 primary evidence 核对。不能先把句子判为语言 PASS，再把科学附着留给另一轮整体审计。
- **区分观察与修正。** SL 中标为 TIE 稳定倾向的内容可作为表达指纹；为修复原文语法、搭配、指代或过强 claim 而采取的自然化处理，仅保证专业正确性，不得宣称为 TIE 的固定写法。

## 4. 句法级 TIE-style audit

先核对 reviewer situation 与当前 semantic state，再逐句检查：

1. 这句承担哪一种功能？
2. 它是否回答上一句留下的必要问题？
3. 语法主语是否承担了正确责任：作者动作、技术事实、display evidence 或 inference？
4. 动词是否具体对应 correction、addition、derivation、test、display 或 inference，而非泛称“improved/addressed”？
5. 时态是否如实表达 revision 状态和事实时间关系，而不是机械套用 present perfect 或 present simple？
6. 指代对象是否唯一，核心技术名词与符号是否稳定对应；在新的段落/证据块及关键判断句中，reviewer 能否直接读出符号的技术含义，而无需反复回查定义？
7. 对每个关键 phrase，条件、baseline、metric 与 scope 是否贴近并准确附着于其所限定的对象、比较或 claim？`with/under/by/across/all/selected/generally/respectively` 等表达各修饰什么，是否与 primary evidence 中的真实实验层级和范围一致？
8. 连接词是否标记真实关系，而不是为了表面流畅？
9. 删除后是否仍能无跳步地理解和核验？若能，删去或并入邻句。
10. 它是否把 TIE 的一种主语、语态、时态、figure/result 表达或连接形式误当成唯一规则？
11. 它是否复制了 TIE 的语法问题、非地道搭配、冗余动词或过强语气？若是，只做功能等价的最小专业化修正，不把修正后的形式反标为 TIE 指纹。

逐句逐词验收须同时调用本文件的语言 realization 与 `04` 的 SD-01/SD-03，核对实际对象、条件、baseline、metric、modifier scope、evidence range 和 claim scope。**sentence-level PASS = 语言实现正确且科学附着正确**；任何一边未核实或不成立，都不能凭语法通顺判 PASS。

## 5. 用未作为主要示例的 TIE 句段反向解释

| TIE 条目 | 为什么这样推进 | 可迁移的 language units | 不迁移部分 |
|---|---|---|---|
| R1-3 / R4-2a | comment 只要求语言纠错，因此感谢后直接报告 proof-reading/correction，再给标记或位置 | SL-01、SL-03、SL-11 | `tried our best`、多重修饰和未具体化的全篇质量宣称 |
| R2-3 | reviewer 同时指出 typo 与 SVD 解释不清；作者用两个完成式动作句分别承接，再以主句加 `where` 从句定义矩阵 | SL-03、SL-05、SL-09 | `carefully rewritten and the presentation has been improved` 的泛化/重复表达 |
| R2-4 | 先交代旧/新 equation number，再以前提、矩阵操作和等式结果逐步推进 | SL-05、SL-06 | `detailed formulated`、`listed as below` 等非地道搭配 |
| R2-5 | 先点明被改对象，再把 nonzero/zero eigenvalue 两种情形写成平行条件 | SL-03、SL-05 | 冗长的引号套引号和语法错误 |
| R2-6 | 先点名 prior relations，再说 equation 可重写，随后逐行给 inequality chain | SL-06 | 仅凭 `more details` 代替真实中间步 |
| R4-2b | 原文以图示修改对象与位置两句结束；输入输出仍未具体解释，短止不等于充分覆盖 | SL-03、SL-11 | `modified and updated` 的同义动词堆叠及 coverage gap |
| R4-5 | 用 `However` 从一般用途转向既有方法限制，以 `This implies` 给后果，再用 `To improve` 进入本文动作 | SL-02、SL-09、SL-10 | 最后的 `guarantee` 与 `better performance` 缺少足够限定 |
| R4-6 | 先报告 comparative study，再解释 table columns，最后读表并定位稿件 | SL-03、SL-05、SL-08、SL-11 | Table II/Table III/Table 2 不一致及不自然比较表达 |

该复核说明 11 个单元能解释这些 scene 的局部句子功能与语言实现；R2-2 的完整 proof、R3-1 的 novelty、R4-5 的 method motivation 与 R4-6 的完整 Table 请求仍是 C1/C2/C4/C5 单例参考，不能由表中的一句或数句还原为可生成的固定路径。

## 6. 本阶段明确不升级为表达惯例的观察

- **Case-specific：** 算法名、机器人平台、参数、公式、图表编号、section/page 和具体比较对象。
- **个体重复：** 高频使用 `According to your suggestion`、`For your convenience`、`in this paper`、`the update text of...` 只说明作者习惯，不能要求每条 response 复现。
- **冗余礼貌：** `sincerely`、`very much`、`which is appreciated`、条目末尾再次感谢。
- **冗余动作：** `modified and updated`、`conducted and performed`、`added and presented` 等双动词。
- **非地道语法/搭配：** `Comparing with`、`cost expensive`、`previous literatures`、`detailed performed/formulated`、`listed as below`、主谓/冠词/单复数错误及逗号拼接句。
- **无证据强化：** `superior`、`far less`、`more suitable`、`satisfactory`、`clearly`、`guarantee` 或 `verify` 在证据不足时的使用。
- **空泛垫句：** `Generally`、`It is well known that` 等若不提供当前推理所需前提，不构成 TIE-native 专业表达。
- **分号的同作者语料校准：** 江 TIE_2621 的 reviewer-response 作者正文中未观察到 semicolon。当分号把两个本来承担不同 semantic responsibilities 的独立 response functions 强行接成一句，而拆成相邻句同样自然、清楚时，优先考虑句号，以贴近该作者的实际 sentence rhythm。这仅是 corpus-level same-author soft calibration，不是顶刊禁用 semicolon、academic-English 通则或 A/B/C mechanism；不要求删除所有 semicolon。
- **固定语态和固定句长：** TIE 同时使用 active/passive、短答和长推导，不能从表面分布推出统一语态或字数规则。

**Provenance:** TN-06 汇入 CK-001、CK-008、CK-010、CK-016、CK-018；SL-01 至 SL-11 均由 TIE PDF 多个 reviewer-response 上下文交叉支持。Nature/ARS 未作为语言样本，只保留 factuality 和 claim boundary 的 supporting 职责。

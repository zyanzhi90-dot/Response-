# A3 Web：来源索引

> 用途：记录当前网页版 ChatGPT 对话在形成 Comment 1 response、TIE 对齐标准和后续知识库规划时，实际参与讨论、核验或裁决的重要来源。
>
> 本文件只做来源索引，不提炼最终写作规则。
>
> A1/A2 文件不作为本轮 A3 的替代来源；它们属于后续三源交叉裁决阶段。

## 0. 来源标签

- `WEB_PRIMARY`：当前网页版 ChatGPT 对话本身，是 A3 中用户要求、纠正、否决与最终裁决的第一来源。
- `WEB_DIRECT`：在当前网页版对话中实际上传、读取、引用或核验过的文件。
- `WEB_REFERENCED`：当前网页版对话明确提到并参与任务理解，但本 A3 阶段不能证明每一轮都重新直接读取。
- `EXTERNAL_AUXILIARY`：被讨论为可辅助的 Skill / workflow，但不决定 TIE 风格。
- `EXCLUDED_FROM_A3`：明确不用于替代当前网页版历史的来源。

---

## 1. `WEB_PRIMARY`：当前网页版 ChatGPT 对话

### 1.1 当前对话完整工作历史

作用：

- 保存用户对 Comment 1 response 的逐轮要求；
- 保存用户对 ChatGPT/Codex 输出的即时评价；
- 保存具体短语为何被否决；
- 保存“这不是局部修改，而是在校准完整 TIE 标准”的元层裁决；
- 保存 ChatGPT 曾经提出、后被撤回的过度泛化建议；
- 保存当前知识库建设路线的形成过程。

A3 中以下类型的判断主要依赖当前对话本身：

- `CONFIRMED / REJECTED / UNRESOLVED / CASE_SPECIFIC` 的最终用户状态；
- 哪些具体例子是“校准标准”而非“一次性替换”；
- 何时需要回到 TIE 原文重新核验；
- 何时应停止继续泛化式润色；
- caption 重复引用等模型过度规范化判断为何被撤回。

限制：

- 当前网页版对话包含大量阶段性候选措辞；“曾出现”不等于“最终确认”。
- 后续知识库必须优先采用用户最终裁决，而不是较早版本的 ChatGPT 判断。

---

## 2. `WEB_DIRECT`：TIE 范例 PDF

### 2.1 `Response_TIE_江_No.17-TIE-2621...pdf`

当前网页版对话中多次用于：

- 提取原文；
- 翻译；
- 查找涉及结果图的 response；
- 比较当前 Comment 1 与范例的组织差异；
- 核验 TIE 是否真的使用某些句型；
- 重新判断“caption 重复引用”“具体 Fig. 引用”等细节是否属于 TIE 真实风格。

重点讨论/核验位置：

- Referee No. 1 – Comment 2；
- Referee No. 3 – Comment 2；
- Referee No. 4 – Comment 3；
- 另有对 TIE 整体 response 表达的多轮总结。

A3 中主要支持：

- evidence-block 组织；
- 新实验/比较的进入方式；
- 图组统一呈现；
- `It can be observed...` / `As seen from the figures...` 等“读图功能”；
- 一次性结论收束；
- 不机械复制固定句式；
- 区分 TIE 原文与后人总结中的“项目增强”句式。

限制：

- TIE 原文不是 TCYB 当前项目的事实来源；
- TIE 中的语法错误、拼写错误、过强 claim 不应照搬；
- 某个 Comment 的个别用法不能自动升级为通用规则。

---

## 3. `WEB_DIRECT`：三份 TIE 总结文件

当前网页版对话曾上传/读取：

1. `Response_表达范式.md`
2. `Response_写作规则.md`
3. `TIE范例_逐条拆解.md`

作用：

- 帮助定位 TIE 中的常见段落动作；
- 梳理首段、证据链、图文关系、claim 边界；
- 识别哪些句式只是总结者补写而不是 TIE 原文；
- 为回查 TIE PDF 提供索引。

关键历史作用：

- `The point we wish to clarify...` 被识别为总结中的“项目增强”，不能冒充 TIE 原句；
- 总结只能作为二级分析来源，发生冲突时必须回到 PDF。

限制：

- 不能把总结中的候选表达自动当作 TIE 作者原始习惯；
- 后续最终知识库应保留“来源层级”。

---

## 4. `WEB_DIRECT`：TCYB response 各版本

当前网页版对话中实际上传、读取、翻译或审计过多个版本，包括但不限于：

- `Response-TCYB-旧.pdf`
- `Response-TCYB(20260915-095010).pdf`
- `Response-TCYB(20260915-095857).pdf`
- `Response-TCYB(20260915-102055).pdf`
- `Response-TCYB(20260920-122832).pdf`
- `Response-TCYB(20260920-130127).pdf`
- `Response-TCYB(20260921-115828).pdf`
- `Response-TCYB(20260921-131252).pdf`
- `Response-TCYB(20260921-161605).pdf`
- `Response-TCYB(20260922-034524).pdf`
- `Response-TCYB(5).tex`
- 其他同一 Comment 1 的中间迭代版本。

作用：

- 比较不同改写阶段；
- 识别重复论证、元话语、术语漂移、claim 边界问题；
- 验证结果图正文是否按 TIE evidence-block 方式收敛；
- 检查 computation-time 指标是否统一；
- 检查具体 Fig. 引用、caption 与正文分工。

限制：

- 早期版本主要是错误路径/演化证据；
- 当前版本的正确表达也不能直接未经裁决写成“通用范文”。

---

## 5. `WEB_DIRECT`：JAS 原论文

### 5.1 `JAS_原论文_指定版本.pdf`

当前网页版对话曾用于：

- 回答 Case 1 与 Case 2 有什么区别；
- 核实 Case 1 accurate tracking、Case 2 compliant interaction；
- 核对 Franka Emika Panda；
- 核对 `\(C\)`、`\(\alpha\)`、10 ms outer-loop sampling delay 等事实。

在 Comment 1 中的职责：

- 证明新增 Cases 的任务性质和必要设置；
- 不决定 TCYB response 的英语风格；
- 不决定本稿 `\(W_x/W_f/S_e(t)\)` 的正式符号；
- 不把 JAS Methods 全量搬入 response。

---

## 6. `WEB_DIRECT / WEB_REFERENCED`：当前稿件与正式符号/结果来源

当前网页版讨论反复依据当前稿件或 Codex 对当前稿件的核对结果，确认：

- `\(W_x\)`；
- `\(W_f\)`；
- `\(S_e(t)\)`；
- standard Gaussian process (GP)；
- lattice-distributed RBFNN；
- 9.90 ms / 20 ms；
- 比较对象与 revised-manuscript 编号。

作用：

- 事实与符号来源；
- 不能被 TIE 范例或 JAS 的符号替代。

限制：

- 稿件版本会更新；
- 页码/参考文献编号等最终提交信息需按最终版本核验。

---

## 7. `WEB_DIRECT`：当前正式结果图与图内修改讨论

网页版对话中实际查看或讨论了：

- JAS Case 1/2 相关结果图；
- `\(W_x\)` variations；
- `\(S_e(t)\)` variations；
- computation-time panels；
- 图内 `b:c`、`W_x:W_f`；
- `S_e(t)` / `I`；
- `t_{\mathrm{comp}}^{\max}`；
- `IL-SOGP [10]`；
- 条件标签在 timing panel 中的位置。

作用：

- 确认图示结果；
- 约束 response 中可描述的数值/趋势；
- 保存图文一致性决策。

限制：

- 当前图形细节为项目级证据，不直接形成通用 reviewer-response 规则。

---

## 8. `WEB_REFERENCED`：handoff 内容

当前网页版对话明确讨论并依赖了 handoff 的存在与作用，包括：

- `00_交接说明.md`
- `01_TIE_Response_写作标准.md`
- `02_已踩坑与错误理解.md`
- `03_Comment1_当前状态.md`

作用：

- 让第二个 Codex 账号继承第一个账号的工作；
- 防止推倒重来；
- 区分已确认标准、已踩坑项和当前未完成状态。

A3 中的边界：

- handoff 内容不是当前网页版对话的替代来源；
- A3 只记录网页版如何引用、评价和继续校准这些 handoff 结论；
- A3 不把 handoff 中的全部内容重新复制为自己的“发现”。

---

## 9. `EXTERNAL_AUXILIARY`：Nature Skill / Academic Research Suite

当前网页版对话中的定位：

- Nature Skill / `nature-response` 可用于 claim 强度、回应边界、证据纪律等；
- Academic Research Suite 计划作为后续知识库补充来源；
- 二者不能覆盖 TIE 的表达风格；
- 只有与 TIE 不冲突的成熟原则才考虑纳入最终知识库。

当前 A3 的限制：

- 网页对话尚未完成对这两套 Skill 的系统逐条兼容性审计；
- 因此不能把它们的具体规则直接记作 `CONFIRMED` TIE 标准。

---

## 10. `EXCLUDED_FROM_A3`：A1 / A2

以下文件当前已存在，但本轮明确不读取它们来替代网页版历史：

- `A1_Codex_证据与决策.md`
- `A1_来源索引.md`
- `A2_Codex_证据与决策.md`
- `A2_来源索引.md`

作用：

- 后续 A1/A2/A3 三源交叉裁决时使用。

当前 A3 阶段：

- 不用于填补 A3；
- 不合并；
- 不去重；
- 不用 A1/A2 的结论反向改写当前网页版历史。

---

## 11. 来源优先级（仅记录当前网页版形成的理解，不是最终知识库规则）

针对不同问题，当前网页对话实际采用的来源职责是：

### 11.1 表达/组织风格

1. TIE 原文；
2. 三份 TIE 总结（辅助定位）；
3. 用户在真实修改中的最终裁决；
4. Nature / academic-writing 仅辅助。

### 11.2 科学事实、实验设置、符号

1. 当前稿件；
2. JAS 原论文；
3. 作者指定的最终正式结果图。

### 11.3 项目边界与读者路径

1. 用户当前指令和最终裁决；
2. 当前 reviewer 的实际 Comment；
3. 项目中关于 reviewer 阅读习惯的内部判断。

### 11.4 禁止作为上游证据的来源

- 源代码；
- 绘图脚本；
- 临时变量名；
- Agent 自行猜测的术语；
- 早期候选 response；
- 一般 phrasebank 在未经过 TIE 核验时。

---

## 12. 当前来源索引的边界

- 本索引不判断最终应该进入知识库的规则。
- 本索引不合并 A1/A2/A3。
- 本索引不解决 `[XX]`。
- 本索引不把当前项目图形或具体数值泛化为通用写作规则。
- 后续必须进行三源交叉裁决，才能形成正式、可复用的 reviewer-response 知识库。

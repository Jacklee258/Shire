---
id: calendar-spread-arbitrage-intake-25
title: 套利交易系统需求调研问卷（25题）
description: |
  面向套利交易系统客户访谈和一期系统需求确认的调研问卷。
  本试卷共 25 题，其中单选题 7 题、多选题 11 题、简答题 7 题，预计 20 分钟完成。
  重点收集客户现有套利类型、重点品种、交易频率、资金规模、当前工具、人工流程、人员投入、策略信号、风控边界、一期系统形态和预算接受度。
  本问卷用于需求调研、方案拆分和交付边界确认，不构成投资建议、收益承诺、代客理财服务或自动交易授权。
tags: [futures, arbitrage, intake, quant-infra, customer-discovery, pre-sales]
schema_version: 2
format: qml-v2
question_count: 25
question_counts:
  single: 7
  multiple: 11
  short: 7
estimated_duration_minutes: 20
trait:
  dimensions: [ACTIVE, EARLY, PAIN, SIGNAL, RISK, AUTO, BUDGET]
  dimension_meanings:
    ACTIVE: 已经有真实套利交易流程、人员投入、资金规模或复盘记录。
    EARLY: 仍处观察、试验或需求澄清阶段，需要先做轻量验证。
    PAIN: 对人工盯盘、记录、复盘或流程标准化有明显减负诉求。
    SIGNAL: 更关注套利机会识别、指标计算、信号评分和策略沉淀。
    RISK: 更关注风险提示、禁止交易、仓位边界、止损和责任留痕。
    AUTO: 对自动下单、程序化交易或实盘闭环有较强期待。
    BUDGET: 预算、验收和合作方式需要重点确认。
  analysis_guidance:
    paired_dimensions:
      - ACTIVE/EARLY：判断客户是真实交易中的系统化升级，还是仍在观察验证阶段。
      - PAIN/SIGNAL/RISK：判断一期价值主线是人力替代、信号提效还是风控约束。
      - AUTO/BUDGET：判断是否需要把自动交易拆到二期，并提前确认预算边界。
    scoring_method:
      - 单选题使用 traits 辅助识别客户阶段和推进优先级，不用于投资适当性或收益判断。
      - 多选题和简答题以原始信息采集为主，访谈后人工整理为一期方案和报价范围。
    interpretation:
      - ACTIVE、PAIN、SIGNAL、RISK 较高时，适合推进一期“监控 + 信号 + 风控 + 复盘”。
      - EARLY 较高时，建议先做 PoC 或轻量看板，避免直接承诺复杂系统。
      - AUTO 较高时，应明确自动下单、双腿成交、撤单追单和程序化报备属于二期或单独报价。
      - BUDGET 较高时，应尽早确认 30 万左右的一期预算是否可讨论，以及功能验收和收益责任边界。
llm:
  model: gpt-5
  temperature: 0.0
  prompt_template: |
    请根据评分标准对答题者的简答内容进行信息完整度评分。
    只输出 JSON，不要解释，不要 Markdown。
    JSON 必须包含字段：score、reason、relevance、risk_flags。
    - score：0 到 {{max_points}} 的整数
    - reason：1 到 3 句，说明覆盖到的关键信息与缺失项
    - relevance：0 到 3 的整数
    - risk_flags：字符串数组，列出需求不清、无真实交易、预算不足、要求自动赚钱、收益验收、自动交易等风险点；没有则输出空数组

    题目：{{question}}
    评分标准：{{rubric}}
    回答：{{answer}}
---

## Q1 [multiple] (1) {partial=true, answer_time=45s}

你们目前主要做哪类套利交易？可多选。

- A*) 股指期货跨期套利
- B*) 商品期货跨期套利
- C*) 跨品种套利
- D*) 期现套利
- E*) 期权 / 波动率套利
- F*) 其他套利类型

## Q2 [short] {max=8, answer_time=4m}

请说明目前重点关注的品种、合约和主要交易逻辑。也请写出暂不考虑的品种。

[rubric]
8 分：清楚写出重点品种、重点合约、主要交易逻辑和暂不考虑品种。
6-7 分：写出重点品种和部分合约或逻辑，但边界不够完整。
3-5 分：只列出少量品种，缺少合约、逻辑或排除范围。
0-2 分：无法判断交易对象，或回答与套利交易无关。
[/rubric]

## Q3 [single] (0) {scoring=traits, answer_time=30s}

现在的套利交易频率大概是多少？

- A) 每天多次 {traits=ACTIVE:2}
- B) 每天 1-2 次 {traits=ACTIVE:2}
- C) 每周数次 {traits=ACTIVE:1}
- D) 有机会才做 {traits=EARLY:1}
- E) 目前还在观察阶段 {traits=EARLY:2}

## Q4 [single] (0) {scoring=traits, answer_time=30s}

单笔或单组套利交易的资金规模大概是多少？

- A) 10 万以内 {traits=EARLY:1}
- B) 10 万 - 50 万 {traits=EARLY:1,ACTIVE:1}
- C) 50 万 - 100 万 {traits=ACTIVE:1}
- D) 100 万 - 500 万 {traits=ACTIVE:2}
- E) 500 万以上 {traits=ACTIVE:2,RISK:1}

## Q5 [multiple] (1) {partial=true, answer_time=45s}

你们希望这个系统首先解决什么问题？最多选 3 项。

- A*) 自动发现套利机会
- B*) 减少人工盯盘
- C*) 提高信号判断效率
- D*) 提前提示风险
- E*) 做持仓跟踪和交易复盘
- F*) 后续接自动交易

## Q6 [multiple] (1) {partial=true, answer_time=45s}

目前主要使用哪些软件或工具？可多选。

- A*) 文华财经
- B*) 快期
- C*) 无限易 / ATP 套利系统
- D*) 金字塔
- E*) Excel / Python 脚本
- F*) 自研系统或其他工具

## Q7 [short] {max=8, answer_time=4m}

请描述现在一个套利机会从发现到下单、持仓、平仓和复盘的实际流程。

[rubric]
8 分：完整覆盖发现信号、判断是否可做、确认风控、下单、持仓跟踪、平仓和复盘。
6-7 分：覆盖大部分流程，但部分环节不够清楚。
3-5 分：只描述发现、下单或平仓中的少数环节。
0-2 分：流程无法复原，或回答与题目无关。
[/rubric]

## Q8 [multiple] (1) {partial=true, answer_time=45s}

当前哪些环节最依赖人工经验？可多选。

- A*) 选品种
- B*) 看价差
- C*) 判断入场
- D*) 判断退出
- E*) 控制仓位
- F*) 判断风险或复盘总结

## Q9 [single] (0) {scoring=traits, answer_time=30s}

目前有没有固定的交易记录或复盘记录？

- A) 有，比较完整 {traits=ACTIVE:2}
- B) 有，但比较零散 {traits=ACTIVE:1,PAIN:1}
- C) 主要靠人工记忆 {traits=PAIN:2}
- D) 目前没有系统记录 {traits=PAIN:2,EARLY:1}

## Q10 [short] {max=8, answer_time=4m}

目前有几个人参与套利相关工作？请按交易员、研究员、风控、技术/数据和其他角色分别填写人数。

[rubric]
8 分：清楚写出各角色人数和合计人数。
6-7 分：写出主要角色人数，但合计或部分角色不清楚。
3-5 分：只写出大概人数，角色拆分不足。
0-2 分：无法判断人员投入。
[/rubric]

## Q11 [short] {max=8, answer_time=4m}

请说明每个角色主要负责什么，以及每天在盯盘扫描、信号判断、下单执行、持仓跟踪、交易记录和复盘总结上大概花多少时间。

[rubric]
8 分：清楚写出角色职责、关键工作项、每日耗时和主要负责人。
6-7 分：覆盖主要职责和耗时，但部分工作项缺失。
3-5 分：只写出大致分工，缺少耗时或负责人。
0-2 分：无法判断人力成本或工作分工。
[/rubric]

## Q12 [multiple] (1) {partial=true, answer_time=45s}

如果系统上线，你们最希望它替代或减轻哪些工作？最多选 3 项。

- A*) 自动扫描价差
- B*) 自动计算分位数 / Z-score
- C*) 自动提示交易信号
- D*) 自动提示风险
- E*) 自动生成日报 / 周报
- F*) 自动记录和复盘交易过程

## Q13 [single] (0) {scoring=traits, answer_time=30s}

如果系统能减少一部分人工工作量，你们预期大概能节省多少？

- A) 20% 左右 {traits=PAIN:1}
- B) 30% - 50% {traits=PAIN:2}
- C) 50% 以上 {traits=PAIN:2,BUDGET:1}
- D) 可以替代 0.5 个人 {traits=PAIN:2,BUDGET:1}
- E) 可以替代 1 个人 {traits=PAIN:2,BUDGET:2}
- F) 不确定，需要试运行评估 {traits=EARLY:1}

## Q14 [multiple] (1) {partial=true, answer_time=60s}

你们现在判断套利机会主要看哪些指标？可多选。

- A*) 价差、价差分位数或 Z-score
- B*) 基差、期限结构或主力换月
- C*) 成交量、持仓量或席位持仓
- D*) 仓单、库存或现货基本面
- E*) 技术指标
- F*) 主观经验或其他指标

## Q15 [single] (0) {scoring=traits, answer_time=30s}

目前有没有固定的开仓、平仓、止损规则？

- A) 有明确规则 {traits=ACTIVE:2,SIGNAL:1}
- B) 有大致规则 {traits=ACTIVE:1,SIGNAL:1}
- C) 主要靠人工判断 {traits=PAIN:1,SIGNAL:1}
- D) 还没有形成标准 {traits=EARLY:1,SIGNAL:1}

## Q16 [short] {max=8, answer_time=4m}

如果已有规则，请描述开仓、平仓、止损、加仓或减仓规则。

[rubric]
8 分：清楚写出开仓、平仓、止损和加减仓规则。
6-7 分：覆盖主要规则，但部分条件或阈值不清。
3-5 分：只有方向性描述，缺少可执行条件。
0-2 分：没有规则，或回答与题目无关。
[/rubric]

## Q17 [short] {max=8, answer_time=4m}

过去哪些信号比较有效？例如价差极端、贴水修复、主力移仓、临近交割、基差收敛或库存变化。

[rubric]
8 分：列出多个有效信号，并说明适用品种、触发条件或有效原因。
6-7 分：列出有效信号，但适用条件不够完整。
3-5 分：只列出泛泛信号，缺少经验解释。
0-2 分：无法说明有效信号。
[/rubric]

## Q18 [multiple] (1) {partial=true, answer_time=45s}

哪些原因最容易导致信号失效或误判？可多选。

- A*) 行情继续极端
- B*) 流动性不足
- C*) 临近交割
- D*) 基本面变化
- E*) 人工执行问题
- F*) 止损不及时

## Q19 [multiple] (1) {partial=true, answer_time=45s}

如果系统给信号，你们更希望它呈现成什么形式？可多选。

- A*) 只提示观察机会
- B*) 给出信号等级，如 S/A/B/C
- C*) 给出建议方向
- D*) 给出风险原因
- E*) 给出仓位或止盈止损参考
- F*) 给出 AI 解释文字或生成日报周报

## Q20 [multiple] (1) {partial=true, answer_time=60s}

过去套利交易里，主要风险或亏损来自哪些方面？可多选。

- A*) 价差继续扩大或单边剧烈波动
- B*) 临近交割风险
- C*) 流动性不足或双腿成交不一致
- D*) 保证金压力或仓位过大
- E*) 止损不及时或人工误操作
- F*) 信号失效或其他风险

## Q21 [short] {max=8, answer_time=4m}

请写出当前硬性风控限制：单笔最大亏损、单日最大亏损、单品种/单组合最大仓位、最大回撤、保证金占用上限和临近交割处理规则。

[rubric]
8 分：清楚写出全部或大部分硬性风控限制，并包含具体数值或规则。
6-7 分：写出主要限制，但部分数值或规则缺失。
3-5 分：只有原则性描述，缺少具体阈值。
0-2 分：没有明确风控限制，或回答无法用于系统配置。
[/rubric]

## Q22 [multiple] (1) {partial=true, answer_time=60s}

哪些情况下，系统应该直接提示“禁止交易”或“暂停交易”？可多选。

- A*) 临近交割
- B*) 成交量或持仓量不足
- C*) 价差突破历史极值
- D*) 保证金不足或单日亏损超限
- E*) 节假日前或重大事件前
- F*) 人工确认前不得交易

## Q23 [multiple] (1) {partial=true, answer_time=45s}

一期系统更适合做成哪种形态？可多选。

- A*) 价差监控看板
- B*) 信号与风控预警系统
- C*) 持仓跟踪系统
- D*) 交易复盘系统
- E*) AI 解释与报告系统
- F*) 自动交易系统

## Q24 [single] (0) {scoring=traits, answer_time=30s}

如果一期先做“监控、信号、风控、复盘”，不做自动下单，你们是否能接受？

- A) 可以接受 {traits=BUDGET:1,RISK:1}
- B) 希望尽快接自动下单 {traits=AUTO:1,BUDGET:1}
- C) 必须一开始就自动交易 {traits=AUTO:2,BUDGET:2}
- D) 需要内部讨论 {traits=BUDGET:1}

## Q25 [single] (0) {scoring=traits, answer_time=30s}

如果一期先不做自动下单，重点做套利机会监控、信号评分、风控预警、持仓跟踪和复盘，预算控制在 30 万左右，你们觉得是否符合预期？

- A) 可接受 {traits=BUDGET:1,ACTIVE:1}
- B) 偏高 {traits=BUDGET:2}
- C) 偏低 {traits=ACTIVE:1}
- D) 要看功能范围 {traits=BUDGET:1}
- E) 需要内部评估 {traits=BUDGET:1}

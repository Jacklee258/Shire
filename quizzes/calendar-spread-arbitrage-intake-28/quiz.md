---
id: calendar-spread-arbitrage-intake-28
title: 期限套利系统需求访谈问卷（28题）
description: |
  面向期货期限套利、跨期套利或相关套利系统建设项目前的首访需求澄清问卷。
  本试卷共 28 题，其中单选题 12 题、多选题 12 题、简答题 4 题，预计 22 分钟完成。
  重点收集项目目标、套利范围、品种组合、数据源、策略逻辑、执行方式、风控边界、Kanban 看板、回测验收、接口条件、竞品参考与商务边界，用于形成一期系统范围、实施计划和报价拆分。
  本问卷只用于系统需求调研、售前诊断和交付边界确认，不构成投资建议、收益承诺、代客理财服务或自动交易授权。
tags: [futures, calendar-spread, arbitrage, intake, quant-infra, kanban, pre-sales]
schema_version: 2
format: qml-v2
question_count: 28
question_counts:
  single: 12
  multiple: 12
  short: 4
estimated_duration_minutes: 22
trait:
  dimensions: [RESEARCH, SIGNAL, AUTO, DATA, RISK, KANBAN, INTEG, COMM]
  dimension_meanings:
    RESEARCH: 更偏研究辅助、价差观察、历史分析、回测验证和人工决策支持。
    SIGNAL: 更偏自动扫描、策略信号、机会排序、预警推送和交易决策辅助。
    AUTO: 更偏自动下单、双腿执行、撤单追单、成交回报和实盘闭环。
    DATA: 数据源、历史行情、实时行情、基本面数据和数据质量依赖较强。
    RISK: 对保证金、回撤、临近交割、流动性、黑名单和风控留痕要求较强。
    KANBAN: 对多角色看板、任务流、复盘、日报周报和管理展示要求较强。
    INTEG: 涉及 CTP、柜台、第三方行情、企业微信/钉钉、内部系统或部署集成。
    COMM: 涉及预算、周期、源代码、独家、运维、培训、责任边界等商务确认。
  analysis_guidance:
    paired_dimensions:
      - RESEARCH/SIGNAL/AUTO：识别一期应定位为研究辅助、交易决策还是自动交易闭环。
      - DATA/INTEG：识别数据接口、历史数据、实时性和部署集成的交付复杂度。
      - RISK/KANBAN：识别风控治理、复盘留痕和管理看板是否是一期开箱重点。
      - COMM：识别是否需要提前锁定合同边界、责任排除和分阶段报价。
    scoring_method:
      - 使用 traits 的单选题用于粗分需求类型和交付复杂度，不作为投资适当性或收益判断。
      - 多选题和简答题以信息采集为主，由访谈人结合原始回答整理需求说明书。
    interpretation:
      - RESEARCH 较高时，一期宜聚焦价差看板、组合管理、回测和人工确认。
      - SIGNAL 较高时，一期宜加入机会扫描、信号规则、风控过滤、推送和复盘。
      - AUTO 较高时，应把自动下单、撤单追单、缺腿处理和实盘风控拆为二期或单独报价。
      - DATA 或 INTEG 较高时，应先确认数据授权、接口可用性、程序化报备、服务器和期货公司配合。
      - RISK 或 KANBAN 较高时，应把风控阈值、任务流、交易日志、复盘报告和权限角色写入验收标准。
      - COMM 较高时，应在报价前明确不承诺收益、亏损责任排除、数据费用承担和源代码/复用权边界。
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
    - risk_flags：字符串数组，列出需求不清、接口不明、收益承诺、自动交易、合规责任等风险点；没有则输出空数组

    题目：{{question}}
    评分标准：{{rubric}}
    回答：{{answer}}
---

## Q1 [single] (0) {scoring=traits, answer_time=30s}

本次建设期限套利系统，最核心的目标是什么？

- A) 看价差、看历史分位和辅助研究 {traits=RESEARCH:2}
- B) 自动扫描机会并给出交易信号 {traits=SIGNAL:2,KANBAN:1}
- C) 统一风控、日志、复盘和团队协作 {traits=RISK:2,KANBAN:2}
- D) 自动下单、双腿执行和实盘闭环 {traits=AUTO:2,INTEG:1}
- E) 用于客户展示、募资、投顾或对外服务 {traits=KANBAN:2,COMM:2}
- F) 目标还不清楚，需要先诊断 {traits=RESEARCH:1,COMM:1}

## Q2 [single] (0) {scoring=traits, answer_time=30s}

第一阶段你们更希望系统定位为哪一种？

- A) 研究辅助工具，人工判断和人工下单 {traits=RESEARCH:2}
- B) 交易决策工具，系统出信号，交易员确认 {traits=SIGNAL:2,RISK:1}
- C) 风控管理工具，重点监控持仓、风险和复盘 {traits=RISK:2,KANBAN:2}
- D) 自动交易工具，系统自动完成下单与平仓 {traits=AUTO:2,INTEG:2}
- E) 管理展示工具，重点给老板、客户或团队看 {traits=KANBAN:2,COMM:1}

## Q3 [multiple] (1) {partial=true, answer_time=45s}

系统一期主要给哪些角色使用？可多选。

- A*) 交易员
- B*) 研究员
- C*) 风控人员
- D*) 老板 / 投资负责人
- E*) 客户 / 投资人 / 外部展示对象
- F*) 技术或运维人员

## Q4 [multiple] (1) {partial=true, answer_time=45s}

当前已经使用或参考过哪些工具？可多选。

- A*) 文华财经 / 麦语言 / 睿期等
- B*) 快期 / 天勤量化 / 信易相关工具
- C*) 无限易 / 筋斗云 / 量投相关工具
- D*) Wind / iFinD / 钢联 / 卓创等数据终端
- E*) Python 脚本、Excel 或内部自研工具
- F*) 期货公司自带交易终端
- G*) 暂时没有固定工具

## Q5 [multiple] (1) {partial=true, answer_time=60s}

一期最希望覆盖哪些品种或板块？可多选。

- A*) 黑色系，如螺纹、热卷、铁矿、焦煤、焦炭
- B*) 化工系，如 PTA、甲醇、乙二醇、PVC、纯碱
- C*) 农产品，如豆粕、豆油、棕榈油、玉米、白糖
- D*) 有色金属，如铜、铝、锌、镍、锡
- E*) 能源或贵金属，如原油、燃油、沥青、黄金、白银
- F*) 股指期货或国债期货
- G*) 具体品种还需要访谈后确认

## Q6 [single] (0) {scoring=traits, answer_time=30s}

一期建议先覆盖多少个重点品种或组合？

- A) 1-3 个，先做 PoC 验证 {traits=RESEARCH:2}
- B) 4-8 个，覆盖核心交易池 {traits=SIGNAL:1,DATA:1}
- C) 9-15 个，形成可用监控池 {traits=SIGNAL:2,DATA:1}
- D) 15 个以上，接近全市场扫描 {traits=DATA:2,INTEG:1}
- E) 暂不确定，需要按历史机会和数据质量筛选 {traits=RESEARCH:1,DATA:1}

## Q7 [multiple] (1) {partial=true, answer_time=45s}

你们希望系统支持哪些套利类型？可多选。

- A*) 同品种不同合约的跨期套利
- B*) 主力合约与次主力合约价差
- C*) 固定月份组合，如 1-5、5-9、9-1
- D*) 跨品种套利，如产业链或替代品关系
- E*) 期现套利
- F*) 内外盘套利
- G*) 期权相关套利

## Q8 [single] (0) {scoring=traits, answer_time=30s}

价差定义希望如何统一？

- A) 近月价格 - 远月价格 {traits=RESEARCH:1}
- B) 远月价格 - 近月价格 {traits=RESEARCH:1}
- C) 按交易方向自动换算成多空组合盈亏 {traits=SIGNAL:1,RISK:1}
- D) 每个组合可自定义公式和腿比例 {traits=DATA:1,INTEG:1}
- E) 还没有统一口径，需要系统方案给默认规则 {traits=RESEARCH:1,COMM:1}

## Q9 [single] (0) {scoring=traits, answer_time=30s}

合约切换和组合构造更接近哪种需求？

- A) 固定月份组合，不自动换月 {traits=RESEARCH:1}
- B) 按主力/次主力自动切换 {traits=SIGNAL:1,DATA:1}
- C) 支持人工维护组合池和黑名单 {traits=RISK:1,KANBAN:1}
- D) 支持两腿以上多腿组合 {traits=DATA:1,INTEG:1}
- E) 需要完整移仓换月和执行联动 {traits=AUTO:2,INTEG:2}

## Q10 [single] (0) {scoring=traits, answer_time=30s}

一期能接受的数据频率是什么？

- A) 日线为主，盘后更新即可 {traits=RESEARCH:2}
- B) 日线 + 盘中定时刷新 {traits=SIGNAL:1,DATA:1}
- C) 5 分钟或 15 分钟级别 {traits=SIGNAL:2,DATA:1}
- D) 1 分钟或 Tick 级别实时行情 {traits=DATA:2,INTEG:1}
- E) 必须实时行情并联动下单 {traits=AUTO:2,INTEG:2}

## Q11 [multiple] (1) {partial=true, answer_time=60s}

目前可以提供或协调哪些数据条件？可多选。

- A*) 期货历史日线数据
- B*) 分钟线或 Tick 历史数据
- C*) 实时行情接口
- D*) CTP 行情或交易接口
- E*) 库存、仓单、基差、现货价格等基本面数据
- F*) 手工历史交易记录或复盘记录
- G*) 目前还不能确定数据来源

## Q12 [single] (0) {scoring=traits, answer_time=30s}

数据接口和数据费用由谁负责更符合现状？

- A) 对方已有数据源和接口，可直接配合 {traits=DATA:1,INTEG:1}
- B) 对方负责采购或协调，开发方只做接入 {traits=DATA:1,COMM:1}
- C) 希望开发方一起推荐和代为接入数据源 {traits=DATA:2,COMM:1}
- D) 暂无数据源，需要先用公开或样例数据验证 {traits=RESEARCH:1,DATA:1}
- E) 需要接多家数据源并做口径统一 {traits=DATA:2,INTEG:2}

## Q13 [multiple] (1) {partial=true, answer_time=60s}

你们希望一期信号逻辑包含哪些内容？可多选。

- A*) Z-score 均值回归
- B*) 历史分位数或极值区间
- C*) 价差趋势或突破过滤
- D*) 季节性或固定月份规律
- E*) 成交量、持仓量、流动性过滤
- F*) 库存、仓单、基差等基本面过滤
- G*) 自定义策略规则或人工规则录入

## Q14 [single] (0) {scoring=traits, answer_time=30s}

第一版是否接受“均值回归 + 分位数 + 风控过滤”作为默认策略框架？

- A) 可以，先验证系统闭环 {traits=RESEARCH:1,SIGNAL:1}
- B) 可以，但参数必须可配置 {traits=SIGNAL:1,KANBAN:1}
- C) 不够，需要加入基本面过滤 {traits=DATA:1,RISK:1}
- D) 不够，需要接入自有策略规则 {traits=INTEG:1,SIGNAL:1}
- E) 不接受，需要先做策略研究再开发系统 {traits=RESEARCH:2,COMM:1}

## Q15 [multiple] (1) {partial=true, answer_time=60s}

哪些策略参数必须可配置？可多选。

- A*) 观察窗口，如 60/120/250 个交易日
- B*) 开仓阈值，如 Z-score 达到正负 2
- C*) 平仓阈值，如 Z-score 回到正负 0.5
- D*) 止损阈值，如 Z-score 突破正负 3
- E*) 最大持仓天数或时间止损
- F*) 临近交割不新开仓天数
- G*) 手续费、滑点和保证金假设

## Q16 [single] (0) {scoring=traits, answer_time=30s}

一期执行方式更适合哪种？

- A) 只显示机会和建议，不进入下单流程 {traits=RESEARCH:2}
- B) 系统出信号，交易员人工确认下单 {traits=SIGNAL:2,RISK:1}
- C) 生成下单建议单，复制到外部交易终端 {traits=SIGNAL:1,KANBAN:1}
- D) 接 CTP 或柜台接口，但仍需人工确认 {traits=INTEG:2,RISK:1}
- E) 自动下单、撤单追单和成交回报闭环 {traits=AUTO:2,INTEG:2,RISK:1}

## Q17 [single] (0) {scoring=traits, answer_time=30s}

程序化交易或外接接口条件目前处于什么状态？

- A) 暂不做程序化，只做研究和人工确认 {traits=RESEARCH:1}
- B) 已向期货公司确认可申请或已开通 {traits=INTEG:1,AUTO:1}
- C) 需要开发方协助整理报备材料或测试流程 {traits=INTEG:2,COMM:1}
- D) 不确定，需要先问期货公司 {traits=INTEG:1,COMM:1}
- E) 涉及多账户、多柜台或资管柜台 {traits=INTEG:2,AUTO:1}

## Q18 [multiple] (1) {partial=true, answer_time=60s}

一期必须包含哪些风控规则？可多选。

- A*) 单品种资金占比上限
- B*) 单组合最大手数或最大保证金占用
- C*) 单日亏损或总回撤触发停手
- D*) 组合止损、时间止损或价差异常止损
- E*) 临近交割强制退出或禁止新开仓
- F*) 流动性不足禁止开仓
- G*) 品种黑名单、合约黑名单或特殊事件暂停

## Q19 [single] (0) {scoring=traits, answer_time=30s}

对临近交割、流动性和异常行情的态度更接近哪种？

- A) 只做提示，由交易员自行处理 {traits=RESEARCH:1}
- B) 触发风险时禁止新开仓 {traits=RISK:1,SIGNAL:1}
- C) 触发风险时建议减仓或强制退出 {traits=RISK:2}
- D) 自动撤单、平仓或切换合约 {traits=AUTO:2,RISK:2}
- E) 规则还不清楚，需要按品种单独制定 {traits=RISK:1,COMM:1}

## Q20 [multiple] (1) {partial=true, answer_time=60s}

Kanban 首页最需要展示哪些模块？可多选。

- A*) 今日套利机会和信号优先级
- B*) 价差曲线、Z-score、历史分位
- C*) 当前持仓、保证金占用和盈亏
- D*) 风控预警、禁开原因和临近交割提示
- E*) 策略任务状态、数据更新时间和异常日志
- F*) 交易记录、复盘结论和日报周报
- G*) 品种池、组合池和参数配置

## Q21 [multiple] (1) {partial=true, answer_time=45s}

需要哪些通知或导出能力？可多选。

- A*) 企业微信或钉钉推送
- B*) 邮件推送
- C*) 手机端查看
- D*) Excel 导出
- E*) 自动生成日报
- F*) 自动生成周报或月报
- G*) 暂时只需要系统内查看

## Q22 [single] (0) {scoring=traits, answer_time=30s}

回测验收更应采用哪种口径？

- A) 功能验收为主，收益只作为展示指标 {traits=COMM:2,RESEARCH:1}
- B) 功能验收 + 回测指标完整性验收 {traits=RESEARCH:1,RISK:1}
- C) 必须达到指定收益或回撤指标才验收 {traits=COMM:2,RISK:1}
- D) 先做 PoC，确认策略有效性后再签开发范围 {traits=RESEARCH:2,COMM:1}
- E) 暂时没有想清楚验收标准 {traits=COMM:1}

## Q23 [multiple] (1) {partial=true, answer_time=60s}

回测报告至少需要包含哪些指标？可多选。

- A*) 累计收益、年化收益和净值曲线
- B*) 最大回撤、收益回撤比和恢复期
- C*) 胜率、盈亏比、平均持仓天数
- D*) 单品种、单组合和分年度表现
- E*) 手续费、滑点、保证金和换月影响
- F*) 参数敏感性或压力测试
- G*) 交易明细和信号明细导出

## Q24 [multiple] (1) {partial=true, answer_time=60s}

商务和交付边界中，哪些事项必须提前写清楚？可多选。

- A*) 不承诺收益，不承担交易亏损
- B*) 数据费用、行情授权和接口协调由谁承担
- C*) 是否交付源代码
- D*) 是否部署到对方服务器或云服务器
- E*) 是否包含培训、运维和策略持续优化
- F*) 是否要求独家，以及是否允许复用底层框架
- G*) 自动交易、程序化报备和实盘责任边界

## Q25 [short] {max=8, answer_time=4m}

请描述你们现在做期限套利或跨期套利的完整流程：从发现机会、判断入场、下单执行、持仓监控到平仓复盘，分别由谁负责？

[rubric]
8 分：清楚覆盖发现机会、入场判断、执行、持仓监控、平仓和复盘，并说明角色分工。
6-7 分：覆盖主要流程和部分分工，但有少量环节不清。
3-5 分：只描述部分流程，缺少执行、风控或复盘细节。
0-2 分：回答过于笼统，或与期限套利流程无关。
[/rubric]

## Q26 [short] {max=8, answer_time=4m}

请列出一期系统必须解决的 3 个问题，并按优先级排序。

[rubric]
8 分：列出 3 个明确问题，能体现优先级，且问题可转化为系统功能或验收标准。
6-7 分：列出 3 个问题，但优先级或验收表达不够清楚。
3-5 分：列出 1-2 个问题，或描述仍偏愿望化。
0-2 分：无法形成明确问题，或只写“赚钱”“稳定”等不可验收目标。
[/rubric]

## Q27 [short] {max=8, answer_time=4m}

请说明你们已有或计划使用的数据源、历史数据范围、实时行情条件、接口权限和期货公司配合情况。

[rubric]
8 分：明确说明数据源、历史范围、频率、实时行情、接口权限和期货公司配合状态。
6-7 分：说明大部分数据条件，但缺少一两项关键接口或权限信息。
3-5 分：只说明当前使用的软件或数据名称，缺少频率、范围或接口状态。
0-2 分：数据条件基本不清楚，或无法判断是否能支持开发。
[/rubric]

## Q28 [short] {max=8, answer_time=4m}

请写出你们希望参考或替代的竞品/现有工具，以及它们最值得学习和最不能接受的地方。

[rubric]
8 分：能列出具体竞品或工具，并分别说明优点、缺点、收费感受或替代原因。
6-7 分：能列出具体工具和部分优缺点，但对收费或替代原因不够清楚。
3-5 分：只列出工具名称，缺少明确优缺点。
0-2 分：没有竞品参考，或回答与系统建设无关。
[/rubric]

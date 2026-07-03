---
id: fundraising-partner-screening-22
title: 私募基金募资合伙人筛选问卷（22题）
description: |
  面向基金管理公司筛选募资合伙人的初筛与面试前置问卷。
  本问卷共 22 题，其中单选题 13 题、多选题 3 题、简答题 6 题，预计 32 分钟完成。
  重点评估候选人的核心城市与资金资源、机构/高净值客户沉淀、历史转化能力、收益结构预期、合规稳定性、销售逻辑、团队协同和潜在风险信号。
  单选题按 traits 累计形成候选画像，简答题按 rubric 辅助面试官进行结构化评分；建议结合背景调查、历史业绩证明与模拟路演后再做最终判断。
tags: [fundraising, private-fund, partner-screening, partner-intake, wealth-management]
schema_version: 2
format: qml-v2
question_count: 22
question_counts:
  single: 13
  multiple: 3
  short: 6
estimated_duration_minutes: 32
trait:
  dimensions: [RESOURCE, INSTITUTION, TRACK, INCENTIVE, COMPLIANCE, PITCH, COLLAB, REDFLAG]
  dimension_meanings:
    RESOURCE: 核心城市、高净值客户、资金渠道或产业资源与公司募资方向的匹配度。
    INSTITUTION: 家族办公室、私行、三方财富、地方国资、母基金等机构渠道的深度。
    TRACK: 过往募资业绩、持续转化、客户维护和可验证 Pipeline 的成熟度。
    INCENTIVE: 对固定收入、管理费分成、Carry、门槛收益率和回拨机制的长期对齐程度。
    COMPLIANCE: 合规执业、客户适当性、材料边界、利益冲突披露和职业稳定性。
    PITCH: 对公司策略卖点、规模约束、回撤管理和客户异议的结构化表达能力。
    COLLAB: 参与周会、维护 Pipeline、配合投研/法务/品牌和跨部门协同的意愿。
    REDFLAG: 需要人工复核的风险信号，如资源不可验证、短期佣金导向、合规边界模糊或协作抗拒。
  analysis_guidance:
    paired_dimensions:
      - RESOURCE/INSTITUTION/TRACK：共同判断候选人是否具备可转化的资金来源，而不是只有泛社交资源。
      - INCENTIVE/COMPLIANCE：共同判断候选人是否适合长期合伙机制，而不是短期返佣代理。
      - PITCH/COLLAB：共同判断候选人是否能代表公司对外沟通，并能在内部形成可管理的销售流程。
      - REDFLAG：不是正向能力分，若明显偏高，应进入人工复核或背景调查。
    scoring_method:
      - 单选题按选项 traits 累计，用于形成候选画像；可参考 RESOURCE 30%、INSTITUTION 20%、TRACK 15%、INCENTIVE 15%、COMPLIANCE 10%、PITCH 5%、COLLAB 5% 做人工加权。
      - 简答题建议按 rubric 评分后补充到 PITCH、COMPLIANCE、TRACK 和 COLLAB 的人工评估中。
      - 75 分可作为入围面试或模拟路演的参考线，85 分以上建议优先进入背景调查和合伙协议沟通。
    interpretation:
      - RESOURCE、INSTITUTION、TRACK 同时较高时，候选人更适合作为核心募资合伙人推进。
      - INCENTIVE 较高且 REDFLAG 较低时，说明候选人更可能接受长期业绩绑定与回拨机制。
      - PITCH 较高但 COMPLIANCE 较低时，应重点核查销售话术、适当性边界和历史投诉记录。
      - COLLAB 较低时，即便资源较强，也建议先以项目制或观察期方式合作。
      - REDFLAG 明显较高时，不建议直接进入合伙协议，应先做资源证明、合规记录和利益冲突核查。
llm:
  model: gpt-5
  temperature: 0.0
  prompt_template: |
    请根据评分标准对候选人的简答内容进行招聘筛选评分。
    只输出 JSON，不要解释，不要 Markdown。
    JSON 必须包含字段：score、reason、evidence_strength、risk_flag。
    - score：0 到 {{max_points}} 的整数
    - reason：1 到 3 句，说明覆盖到的关键点与缺失项
    - evidence_strength：0 到 3 的整数，表示回答是否包含可核验事实、数据、案例或具体动作
    - risk_flag：true 或 false，表示是否出现明显夸大、合规边界模糊、短期佣金导向或协作抗拒

    题目：{{question}}
    评分标准：{{rubric}}
    回答：{{answer}}
---

## Q1 [short] {max=4, answer_time=4m}

请填写候选人基本信息：姓名、当前主要办公城市、可长期深耕的核心城市/地区、过往主要任职机构或募资相关经历。

[rubric]
1) 信息完整，至少包含姓名、主要办公城市、核心城市/地区和主要经历。
2) 城市/地区表述清晰，能看出是否覆盖公司目标市场。
3) 募资经历描述具体，能初步判断与私募基金、财富管理或机构渠道的相关性。
4) 若只填写泛泛履历、缺少联系方式或核心地区，应适当扣分。
[/rubric]

## Q2 [multiple] (1) {partial=true, answer_time=45s}

您目前可以持续深耕并直接触达资金资源的城市或地区有哪些？可多选。

- A*) 北京
- B*) 上海
- C*) 深圳
- D*) 广州
- E*) 杭州
- F*) 成都
- G*) 苏州 / 南京 / 长三角其他城市
- H*) 香港 / 新加坡 / 境外华人资金圈
- I*) 其他城市或地区

[rubric]
本题用于采集候选人的核心地域覆盖，不单独作为优劣判断。后续应结合公司目标募集城市、客户类型和历史转化记录核验。
[/rubric]

## Q3 [single] (0) {scoring=traits, answer_time=35s}

您当前最有把握直接触达并推进转化的资源类型是：

- A) 已维护多年的高净值个人客户，可直接安排产品沟通 {traits=RESOURCE:2,TRACK:1}
- B) 家族办公室、私行、三方财富或券商财富渠道 {traits=INSTITUTION:2,RESOURCE:1}
- C) 地方国资、母基金、上市公司或产业资本 {traits=INSTITUTION:2,RESOURCE:1}
- D) 产业链企业家、项目方或上下游资源，可辅助资本与产业协同 {traits=RESOURCE:1,PITCH:1}
- E) 主要是泛社交关系，尚未形成可验证投资人名单 {traits=REDFLAG:1}
- F) 目前资源有限，希望加入后由公司提供主要客户线索 {traits=REDFLAG:2,COLLAB:1}

## Q4 [single] (0) {scoring=traits, answer_time=35s}

过去 3 年内，您主导或深度参与的累计募资规模更接近：

- A) 5000 万元以下，且主要为零散客户 {traits=REDFLAG:1}
- B) 5000 万 - 1 亿元，有少量可复购客户 {traits=RESOURCE:1,TRACK:1}
- C) 1 亿 - 3 亿元，具备稳定客户维护记录 {traits=RESOURCE:2,TRACK:1}
- D) 3 亿 - 10 亿元，有明确产品或策略募集案例 {traits=RESOURCE:2,TRACK:2}
- E) 10 亿元以上，且能提供可核验项目、渠道或客户证明 {traits=RESOURCE:2,TRACK:2,INSTITUTION:1}
- F) 不便披露，也暂时无法提供可核验证明 {traits=REDFLAG:2}

## Q5 [single] (0) {scoring=traits, answer_time=35s}

您最稳定的客户或渠道关系更接近以下哪一类？

- A) 单个高净值客户为主，客户集中度较高 {traits=RESOURCE:1}
- B) 高净值个人客户池较分散，但复购和转介绍较稳定 {traits=RESOURCE:2,TRACK:1}
- C) 私行、券商财富、三方财富等渠道负责人关系较深 {traits=INSTITUTION:2,TRACK:1}
- D) 家族办公室、企业家社群或上市公司实控人圈层 {traits=INSTITUTION:2,RESOURCE:1}
- E) 地方国资、政府基金、母基金或产业资本 {traits=INSTITUTION:2,COMPLIANCE:1}
- F) 资源仍在积累阶段，尚未形成可稳定转化的客户池 {traits=REDFLAG:1}

## Q6 [multiple] (1) {partial=true, answer_time=50s}

您目前可以触达的投资人或渠道主要偏好哪些策略或产品？可多选。

- A*) 量化策略 / 指数增强 / 中性策略
- B*) 股权投资 / 产业投资 / 并购协同
- C*) 固收、固收+ 或低波动类产品
- D*) FOF / MOM / 多策略组合
- E*) 私募证券基金
- F*) 私募股权或创投基金
- G*) 家族资产配置、税务传承或综合财富规划
- H*) 暂不清楚，需要进一步访谈确认

[rubric]
本题用于判断候选人资源与公司策略的匹配度。若大量选择但无法在后续简答或面试中说明具体客户偏好、过往案例和转化路径，应降低资源可信度。
[/rubric]

## Q7 [single] (0) {scoring=traits, answer_time=35s}

您与核心资金方的关系深度通常处于哪一层？

- A) 可直接约到最终出资人或实际决策人 {traits=RESOURCE:2,TRACK:2}
- B) 可约到家族办公室、机构投资部门或渠道负责人 {traits=INSTITUTION:2,TRACK:1}
- C) 主要通过中间人转介绍，需要进一步打通决策链 {traits=RESOURCE:1}
- D) 只认识一线客户经理或外围联系人，决策链不稳定 {traits=REDFLAG:1}
- E) 多数资源目前停留在名片或社群层面 {traits=REDFLAG:2}

## Q8 [single] (0) {scoring=traits, answer_time=35s}

如果加入合作，您预计 90 天内可推进到什么程度？

- A) 可拿出明确名单、历史沟通记录和首批重点客户拜访计划 {traits=RESOURCE:2,TRACK:2,COLLAB:1}
- B) 可组织 2-3 场小范围路演或闭门沟通 {traits=RESOURCE:2,PITCH:1,COLLAB:1}
- C) 可先完成客户访谈和策略适配，但转化周期不确定 {traits=TRACK:1,COLLAB:1}
- D) 需要公司先提供品牌背书、材料和客户线索后才能推进 {traits=COLLAB:1,REDFLAG:1}
- E) 暂时无法承诺明确动作或时间表 {traits=REDFLAG:2}

## Q9 [single] (0) {scoring=traits, answer_time=35s}

除资金资源外，您能给公司带来的产业或投研协同更接近：

- A) 可引入特定产业链专家、企业家或项目撮合资源 {traits=RESOURCE:1,PITCH:1}
- B) 可帮助公司验证行业趋势、项目质量或企业经营情况 {traits=PITCH:1,COMPLIANCE:1}
- C) 可协助公司进入企业家圈层或产业资本圈层 {traits=RESOURCE:2}
- D) 主要贡献在资金销售，产业协同暂时较少 {traits=TRACK:1}
- E) 暂无明确协同资源，但愿意配合学习公司策略 {traits=COLLAB:1}

## Q10 [single] (0) {scoring=traits, answer_time=35s}

您对固定收入或管理费型收入的期望更接近：

- A) 接受较低固定津贴，更看重后端分成和长期绑定 {traits=INCENTIVE:2}
- B) 希望有合理基本保障，同时接受业绩导向的浮动机制 {traits=INCENTIVE:2,COLLAB:1}
- C) 固定收入与浮动收入都重要，需要根据资源投入协商 {traits=INCENTIVE:1}
- D) 希望固定底薪或固定管理费分成占主要部分 {traits=REDFLAG:1}
- E) 不接受明显业绩门槛，希望无条件获得较高固定报酬 {traits=REDFLAG:2}

## Q11 [single] (0) {scoring=traits, answer_time=40s}

对于 Carry、门槛收益率和回拨机制，您的态度更接近：

- A) 理解并接受门槛收益率、阶梯式分成和必要回拨 {traits=INCENTIVE:2,COMPLIANCE:1}
- B) 接受与长期业绩绑定，但希望梯度和结算周期清晰 {traits=INCENTIVE:2}
- C) 可以讨论，但需要公司先给出行业对标方案 {traits=INCENTIVE:1,COLLAB:1}
- D) 更关注前端返佣，对门槛收益和回拨接受度低 {traits=REDFLAG:2}
- E) 不熟悉相关机制，需要系统了解后再判断 {traits=COLLAB:1}

## Q12 [single] (0) {scoring=traits, answer_time=40s}

关于合规执业和客户适当性，以下哪项最符合您的过往做法？

- A) 有完整合规意识，能主动区分事实陈述、风险揭示和收益预期 {traits=COMPLIANCE:2,PITCH:1}
- B) 熟悉私募募集流程，能配合留痕、适当性和材料审批 {traits=COMPLIANCE:2,COLLAB:1}
- C) 主要依赖公司合规部门把关，自己按材料执行 {traits=COMPLIANCE:1,COLLAB:1}
- D) 过往较少受到严格合规约束，需要重新适应 {traits=REDFLAG:1}
- E) 认为客户关系更重要，合规流程可以灵活处理 {traits=REDFLAG:2}

## Q13 [single] (0) {scoring=traits, answer_time=35s}

您对客户名单、Pipeline 和拜访记录的管理习惯更接近：

- A) 有结构化客户分层、拜访纪要、投资偏好和后续动作记录 {traits=TRACK:2,COMPLIANCE:1,COLLAB:1}
- B) 有较完整 Excel、CRM 或个人表格，可迁移到公司流程 {traits=TRACK:2,COLLAB:1}
- C) 主要靠个人记忆和微信沟通记录维护 {traits=TRACK:1,REDFLAG:1}
- D) 不习惯共享 Pipeline，担心客户资源归属不清 {traits=REDFLAG:2}
- E) 愿意共享阶段性进展，但需要先明确客户保护机制 {traits=COLLAB:1,COMPLIANCE:1}

## Q14 [multiple] (1) {partial=true, answer_time=50s}

为了更好转化客户，您最需要公司提供哪些支持？可多选。

- A*) 标准路演材料和一页纸产品说明
- B*) 针对不同客户类型的定制化版本
- C*) 投研人员参与重点客户沟通
- D*) 历史业绩、回撤、风控和归因材料
- E*) 法务、合规和适当性流程支持
- F*) 品牌背书、媒体露出或客户活动支持
- G*) 投后服务、客户复盘和定期报告支持
- H*) 暂不需要太多后端支持，自己可以独立推进

[rubric]
本题用于识别候选人对公司后端支持的需求。选择越多不代表越好，重点看其需求是否具体、合理、能与实际转化场景对应。
[/rubric]

## Q15 [single] (0) {scoring=traits, answer_time=35s}

对于每周例会、Pipeline 汇报和市场反馈同步，您的态度是：

- A) 可以稳定参加，并主动更新客户阶段、阻碍和下一步动作 {traits=COLLAB:2,TRACK:1}
- B) 可以参加，但希望会议短、目标明确、少做形式化汇报 {traits=COLLAB:2}
- C) 愿意按月汇报，周会频率可能偏高 {traits=COLLAB:1}
- D) 不习惯固定汇报，更希望结果导向、不干预过程 {traits=REDFLAG:1}
- E) 明确不接受规律性会议或客户过程透明化 {traits=REDFLAG:2}

## Q16 [single] (0) {scoring=traits, answer_time=35s}

您更偏好的日常沟通与协同方式是：

- A) 重点客户线下深度沟通，日常线上快速同步 {traits=COLLAB:2,PITCH:1}
- B) 线上为主，必要时安排闭门会或陪访 {traits=COLLAB:2}
- C) 由本人主导客户沟通，公司在关键节点介入 {traits=TRACK:1,COLLAB:1}
- D) 希望公司团队深度参与多数客户沟通 {traits=COLLAB:1}
- E) 更倾向独立推进，较少与公司团队同步 {traits=REDFLAG:1}

## Q17 [short] {max=10, answer_time=8m}

基于“产业 + 资本 + 量化”的投资策略，您认为当前市场环境下最能打动目标资金方的募资卖点是什么？请结合目标客户类型说明。

[rubric]
1) 能明确区分高净值个人、家族办公室、机构渠道或产业资本的不同关注点。
2) 能解释产业资源、资本配置和量化能力之间的协同关系，而不是只堆概念。
3) 能结合当前市场环境说明低相关性、回撤控制、策略容量、透明度或投研闭环等卖点。
4) 能说明适合哪些客户、不适合哪些客户，体现适当性边界。
5) 表达有结构，便于转化成路演话术或一页纸材料。
[/rubric]

## Q18 [short] {max=10, answer_time=8m}

如果首期路演中，意向客户质疑“管理规模限制在 40 亿左右会不会影响收益或成长空间”，您会如何回应？

[rubric]
1) 能先承认客户问题合理，并解释规模约束与策略有效性、容量管理、流动性和执行效率之间的关系。
2) 能把“规模限制”转化为风控纪律、投资人体验和长期收益质量的正面信号。
3) 不夸大收益，不承诺规模越小收益越高。
4) 能补充后续扩容条件、分策略容量、投资人排队或封闭安排等可执行口径。
5) 能保持专业、克制和合规表达。
[/rubric]

## Q19 [short] {max=10, answer_time=8m}

如果客户追问历史回撤、阶段性亏损和净值修复周期，您会如何组织回答？

[rubric]
1) 能主动披露回撤口径，如最大回撤、回撤持续时间、修复周期、极端行情表现。
2) 能解释策略风控机制、仓位控制、止损或风险预算，而不是只强调历史收益。
3) 能提醒客户历史表现不代表未来收益，避免收益承诺。
4) 能根据客户风险承受能力判断是否继续推进，而不是强行销售。
5) 能说明需要投研或风控同事补充哪些材料。
[/rubric]

## Q20 [short] {max=10, answer_time=8m}

请设计您加入后的前 90 天募资推进计划，至少包括目标客户分层、拜访节奏、路演安排、预计转化里程碑和需要公司配合的事项。

[rubric]
1) 有明确客户分层，如核心可转化、重点培育、渠道共建、长期维护。
2) 有可执行时间表和动作频率，如名单梳理、首轮访谈、闭门会、复访、材料定制。
3) 有合理转化里程碑，不只写最终募集金额。
4) 能说明需要投研、法务、品牌、运营或高管支持的具体节点。
5) 能体现 Pipeline 管理、风险预警和复盘机制。
[/rubric]

## Q21 [single] (0) {scoring=traits, answer_time=35s}

您更希望与公司形成哪种合作定位？

- A) 核心募资合伙人，承担明确目标并参与长期利益绑定 {traits=INCENTIVE:2,TRACK:1,COLLAB:1}
- B) 区域或渠道合伙人，围绕优势城市/渠道建立阶段目标 {traits=RESOURCE:2,COLLAB:1}
- C) 项目制合作，先用若干客户或路演验证双方匹配 {traits=COLLAB:1,TRACK:1}
- D) 短期佣金代理，主要按单次转化结算 {traits=REDFLAG:1}
- E) 暂时不确定，希望先了解公司资源和支持力度 {traits=COLLAB:1}

## Q22 [short] {max=8, answer_time=6m}

请说明是否存在可能影响合作的事项，例如竞业限制、客户归属争议、历史合规处罚、未披露佣金安排、利益冲突或时间投入限制。如无，也请明确说明。

[rubric]
1) 主动披露潜在限制或风险事项，信息具体可核验。
2) 能说明风险事项的当前状态、影响范围和解决方案。
3) 若无相关事项，能作出明确陈述。
4) 回避、含糊或明显与履历不一致时应扣分，并建议进入背景调查。
[/rubric]

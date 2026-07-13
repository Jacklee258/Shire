---
id: aidc-shaoguan-project-owner-screening-24
title: 韶关 AIDC 智算中心项目负责人招聘深筛问卷
description: |
  面向韶关 AIDC 智算中心项目负责人候选人的面试前深筛问卷。
  本试卷共 24 题，其中单选题 12 题、多选题 4 题、简答题 8 题，预计 35 分钟完成。
  重点评估候选人是否具备数据中心 / 智算中心项目从选址锁地、政府预审、客户锁单、方案测算、审批开工到交付运营的真实推进经验。
  本问卷特别关注阿里云、腾讯云、华为云、百度智能云、运营商或大型 IDC / AIDC 项目经历，以及电力能耗、报批报建、客户锁单、投融资测算和跨线协同能力。
  单选题按 traits 累计形成候选画像，简答题按 rubric 辅助面试官进行结构化评分；建议结合简历、项目证明、背调、客户资源核验和面试追问后再做最终判断。
tags: [recruitment, aidc, data-center, shaoguan, project-owner, infrastructure]
schema_version: 2
format: qml-v2
question_count: 24
question_counts:
  single: 12
  multiple: 4
  short: 8
estimated_duration_minutes: 35
trait:
  dimensions: [IDC_EXP, BIG_TECH, GOV_LAND, POWER_ENERGY, TECH_SOLUTION, CLIENT_ORDER, APPROVAL, FIN_MODEL, EXECUTION, REDFLAG]
  dimension_meanings:
    IDC_EXP: 数据中心、智算中心或高密算力基础设施从立项、建设到交付的真实项目经验。
    BIG_TECH: 阿里云、腾讯云、华为云、百度智能云、运营商、大型 IDC 或大型算力中心的工作与项目方法沉淀。
    GOV_LAND: 政府、园区、招商、发改、自然资源、工信 / 数据局等部门沟通及土地锁定能力。
    POWER_ENERGY: 电力接入、能耗统筹、节能审查、绿电比例、PUE 指标和供电周期成本判断能力。
    TECH_SOLUTION: 高密机柜、GPU/NPU、液冷、HVDC、网络架构、运维标准和技术方案落地能力。
    CLIENT_ORDER: 云厂商、运营商、模型公司、算力租赁客户、央国企数字化客户的需求访谈和订单转化能力。
    APPROVAL: 备案 / 核准、节能审查、环评、规划许可、消防审查、施工许可、水保 / 排水等审批路径能力。
    FIN_MODEL: 土地、土建、机电、电力接入、液冷、服务器 / GPU、融资成本、租金收入、回收期和 IRR 测算能力。
    EXECUTION: 多工作线并行推进、跨部门协同、项目节奏管理、风险闭环和结果交付能力。
    REDFLAG: 需要人工复核的风险信号，如经验不可验证、只会泛泛而谈、关键审批或电力认知薄弱。
  analysis_guidance:
    paired_dimensions:
      - IDC_EXP/BIG_TECH：共同判断候选人是否做过真实 AIDC / IDC 项目，而不是只熟悉概念或供应商话术。
      - GOV_LAND/POWER_ENERGY/APPROVAL：共同判断候选人能否把土地、电力、能耗和审批打通，这是韶关项目的前置生死线。
      - TECH_SOLUTION/CLIENT_ORDER/FIN_MODEL：共同判断技术方案、客户需求和投资收益是否能相互闭环。
      - EXECUTION/REDFLAG：共同判断候选人是否适合作为总负责人承担跨线推进，REDFLAG 高时必须人工复核。
    scoring_method:
      - 单选题按选项 traits 累计，用于形成候选画像；可参考 IDC_EXP 15%、BIG_TECH 10%、GOV_LAND 12%、POWER_ENERGY 15%、TECH_SOLUTION 10%、CLIENT_ORDER 10%、APPROVAL 10%、FIN_MODEL 8%、EXECUTION 10% 做人工加权。
      - 简答题建议按 rubric 评分后补充到对应维度，尤其关注候选人是否给出可核验项目、部门、时间、容量、电力、客户、审批和投资数据。
      - 85 分以上建议优先面试并核验项目证明；75-84 分可进入面试并针对短板追问；60-74 分更适合作为专项角色候选；60 分以下不建议进入核心岗位面试。
    interpretation:
      - POWER_ENERGY、GOV_LAND、APPROVAL 任一明显偏弱时，不建议直接担任韶关项目总负责人。
      - CLIENT_ORDER 高但 POWER_ENERGY 或 APPROVAL 低时，更适合商务角色而非项目总负责。
      - TECH_SOLUTION 高但 GOV_LAND、FIN_MODEL 或 EXECUTION 低时，更适合技术负责人或顾问角色。
      - REDFLAG 明显偏高时，即使其他维度较高，也应先做项目证明、背调和面试深挖。
llm:
  model: gpt-5
  temperature: 0.0
  prompt_template: |
    请根据评分标准对候选人的简答内容进行招聘筛选评分。
    只输出 JSON，不要解释，不要 Markdown。
    JSON 必须包含字段：score、reason、evidence_strength、risk_flag、interview_followup。
    - score：0 到 {{max_points}} 的整数
    - reason：1 到 3 句，说明覆盖到的关键点与缺失项
    - evidence_strength：0 到 3 的整数，表示回答是否包含可核验项目、数据、部门、时间、合同、审批或成本信息
    - risk_flag：true 或 false，表示是否出现明显夸大、空泛表述、回避关键约束、审批 / 电力 / 客户认知薄弱或经验不可验证
    - interview_followup：1 到 3 个建议面试追问点

    题目：{{question}}
    评分标准：{{rubric}}
    回答：{{answer}}
---

## Q1 [short] {max=6, answer_time=2m}

请填写候选人基本信息：姓名、当前城市、可接受的常驻 / 出差安排、过往主要任职机构、参与过的数据中心 / 智算中心 / 算力基础设施项目名称和个人角色。

[rubric]
1) 信息完整，至少包含姓名、城市、常驻 / 出差安排、主要任职机构和项目经历。
2) 能明确说明个人在项目中的角色，如总负责、技术负责人、报批负责人、商务负责人、PMO 或顾问。
3) 项目经历包含可核验线索，如项目所在地、容量、机柜数、投资额、客户、供电等级、建设阶段或交付时间。
4) 若只写泛泛履历、没有项目名称或无法看出个人职责，应明显扣分。
[/rubric]

## Q2 [multiple] (1) {partial=true, answer_time=45s}

您深度参与过以下哪些类型的项目？可多选。

- A*) 传统 IDC 数据中心新建或扩建项目
- B*) 智算中心 / AIDC 项目
- C*) 云厂商或运营商大型资源池 / 算力集群项目
- D*) GPU / NPU 高密算力机房建设或改造项目
- E*) 液冷数据中心或高功率密度机柜部署项目
- F*) 园区级数字基础设施、东数西算或区域算力节点项目
- G*) 只参与过一般机房、弱电、网络或软件项目
- H*) 暂无上述项目的深度参与经历

[rubric]
本题用于采集项目类型覆盖面。选择越多不代表越好，面试时应重点核验候选人是否能说明具体项目、角色、容量、周期和交付结果。
[/rubric]

## Q3 [single] (0) {scoring=traits, answer_time=35s}

您与阿里云、腾讯云、华为云、百度智能云、运营商或大型 IDC / AIDC 服务商的经历最接近：

- A) 曾在阿里云 / 腾讯云 / 华为云 / 百度智能云等云厂商任职，并深度参与算力基础设施或数据中心项目 {traits=BIG_TECH:2,IDC_EXP:2,TECH_SOLUTION:1}
- B) 曾在中国移动 / 中国电信 / 中国联通或其专业公司任职，并参与大型数据中心或算力资源池项目 {traits=BIG_TECH:2,IDC_EXP:1,POWER_ENERGY:1}
- C) 曾在大型 IDC / AIDC 服务商任职或作为核心乙方深度参与项目交付 {traits=IDC_EXP:2,BIG_TECH:1,EXECUTION:1}
- D) 主要以设计院、施工单位、设备厂商或集成商身份服务过上述客户 {traits=TECH_SOLUTION:1,IDC_EXP:1,EXECUTION:1}
- E) 主要参与地方园区或中小型机房项目，尚无大厂或大型服务商项目经历 {traits=IDC_EXP:1,REDFLAG:1}
- F) 暂无相关经历 {traits=REDFLAG:2}

## Q4 [single] (0) {scoring=traits, answer_time=30s}

您过往在数据中心 / 智算中心项目中最接近的角色是：

- A) 项目总负责人，统筹土地、政府、电力、客户、设计、施工、融资和交付 {traits=IDC_EXP:2,EXECUTION:2,GOV_LAND:1}
- B) 技术负责人，主导基础设施、机电、液冷、高密算力或运维方案 {traits=TECH_SOLUTION:2,IDC_EXP:1,POWER_ENERGY:1}
- C) 政府 / 土地 / 报批负责人，主导窗口沟通、审批清单和手续推进 {traits=GOV_LAND:2,APPROVAL:2,EXECUTION:1}
- D) 商务 / 客户负责人，主导云厂商、运营商、模型公司或算力客户需求转化 {traits=CLIENT_ORDER:2,BIG_TECH:1,EXECUTION:1}
- E) 财务 / 投融资 / 法务负责人，主导投资测算、合作结构和融资条件 {traits=FIN_MODEL:2,EXECUTION:1}
- F) 主要是专项支持或外围配合，尚未承担项目主责 {traits=REDFLAG:1}

## Q5 [single] (0) {scoring=traits, answer_time=30s}

您主导或深度参与过的最大数据中心 / 智算中心项目规模更接近：

- A) 只参与过小型机房或单点改造，规模和负荷较小 {traits=REDFLAG:2}
- B) 1000 个机柜以内，或 5MW 以下负荷 {traits=IDC_EXP:1}
- C) 1000-3000 个机柜，或 5-20MW 负荷 {traits=IDC_EXP:2,EXECUTION:1}
- D) 3000-8000 个机柜，或 20-60MW 负荷 {traits=IDC_EXP:2,POWER_ENERGY:1,EXECUTION:1}
- E) 8000 个机柜以上，或 60MW 以上负荷，且能说明电力、审批和交付路径 {traits=IDC_EXP:2,POWER_ENERGY:2,EXECUTION:2}
- F) 不便披露，也暂时无法提供可核验项目线索 {traits=REDFLAG:2}

## Q6 [short] {max=12, answer_time=4m}

请描述一个您深度参与过的数据中心 / 智算中心项目，从立项、选址、方案、审批、建设到交付的关键节点。请尽量写清项目所在地、建设规模、负荷容量、客户或用途、您的角色、关键难点和最终结果。

[rubric]
1) 能按时间线说明项目从立项到交付或当前阶段的关键节点。
2) 包含具体项目事实，如地点、机柜 / 算力 / MW 规模、电力接入、PUE、建设周期、投资额或客户类型。
3) 能说明个人真实职责和决策贡献，而不是只描述团队或公司整体工作。
4) 能指出至少 2 个关键难点，如土地、能耗、电力、审批、客户锁单、资金或施工协调。
5) 能说明最终结果、未完成原因或阶段性交付物，并体现可核验性。
6) 若回答只有概念堆砌、没有项目事实或回避个人职责，应明显扣分。
[/rubric]

## Q7 [short] {max=10, answer_time=3m}

如果您入职后负责韶关 AIDC 项目，首月最优先验证哪 5 件事？请按优先级说明每件事的目标、对接对象和输出物。

[rubric]
1) 能覆盖土地可建、电力可接、能耗可批、客户真实、资金闭环等核心门槛。
2) 能明确对接对象，如招商主管部门、发改、自然资源、工信 / 数据局、园区、供电局、潜在客户、银行或施工方。
3) 每件事都有明确输出物，如候选地块对比表、窗口沟通纪要、负荷接入口径、客户访谈表、一期测算表。
4) 优先级符合 AIDC 项目规律，不能把电力、能耗或审批放到土地摘牌后才处理。
5) 表达具体可执行，能看出 30 天内的推进节奏。
[/rubric]

## Q8 [multiple] (1) {partial=true, answer_time=45s}

候选地块对比时，您认为必须优先核查哪些因素？可多选。

- A*) 土地性质、规划用途和是否支持数据中心 / 智算中心建设
- B*) 出让方式、地价、容积率、投资强度和供地周期
- C*) 周边变电站、可接入容量、接入电压等级、接入距离和接入成本
- D*) 能耗指标、节能审查口径、绿电比例和 PUE 可达性
- E*) 环评敏感点、用水、排水、水保、消防和施工条件
- F*) 政府态度、园区支持政策、项目专班或会议纪要可能性
- G*) 周边餐饮、酒店和通勤便利性
- H*) 地块外观是否大气、宣传照片是否好看

[rubric]
本题用于识别候选人是否理解地块筛选的关键约束。A-F 是核心核查项；G 可作为配套信息但不是优先门槛；H 不应作为决策依据。
[/rubric]

## Q9 [single] (0) {scoring=traits, answer_time=30s}

假设韶关已有 3 个候选地块，您判断哪个地块可以进入下一阶段时，最接近以下哪种做法？

- A) 建立地块对比表，同时核查土地性质、规划用途、供地方式、电力接入、能耗口径、环评敏感点、政府态度和主要风险 {traits=GOV_LAND:2,POWER_ENERGY:1,APPROVAL:1,EXECUTION:1}
- B) 先设置淘汰条件，凡土地用途不支持、一期电力无法明确、能耗无法统筹或审批态度不清晰的地块先剔除 {traits=GOV_LAND:1,POWER_ENERGY:2,APPROVAL:1}
- C) 先看客户交付时间和一期规模，再反推地块、电力、投资强度和建设周期是否匹配 {traits=CLIENT_ORDER:1,FIN_MODEL:1,EXECUTION:1}
- D) 优先选择地价最低、政府补贴最积极的地块，再逐步解决电力和能耗 {traits=GOV_LAND:1,REDFLAG:1}
- E) 优先选择面积最大、形象最好、后续扩展空间最大的地块 {traits=REDFLAG:1}
- F) 主要依赖政府推荐，不单独建立淘汰框架 {traits=REDFLAG:2}

## Q10 [single] (0) {scoring=traits, answer_time=30s}

韶关项目政府预审阶段，您会优先推动哪种沟通路径？

- A) 先由招商主管部门牵头，联动发改、自然资源、工信 / 数据局、园区和供电，争取形成专班或会议纪要 {traits=GOV_LAND:2,APPROVAL:1,EXECUTION:2}
- B) 先单独找自然资源部门确认土地，再视情况逐个找其他部门 {traits=GOV_LAND:1}
- C) 先找供电局确认容量，再由电力结果反推地块和审批路径 {traits=POWER_ENERGY:2,EXECUTION:1}
- D) 先找园区谈政策和补贴，等政策满意后再补审批和电力 {traits=REDFLAG:1}
- E) 先找设计院出完整方案，用方案倒逼政府部门表态 {traits=TECH_SOLUTION:1,REDFLAG:1}
- F) 主要依靠领导或中间人关系推进，暂不需要结构化会议纪要 {traits=REDFLAG:2}

## Q11 [single] (0) {scoring=traits, answer_time=30s}

您主导或深度参与 AIDC / IDC 项目报批报建或牌照相关事项的经历最接近：

- A) 主导过备案 / 核准、节能审查、环评、规划许可、消防、施工许可和电力接入等完整路径 {traits=APPROVAL:2,GOV_LAND:1,POWER_ENERGY:1,EXECUTION:1}
- B) 深度参与过节能审查、能耗统筹、电力接入或绿电方案等关键事项 {traits=POWER_ENERGY:2,APPROVAL:1,EXECUTION:1}
- C) 深度参与过规划、施工许可、消防、环评、水保 / 排水等建设手续 {traits=APPROVAL:2,GOV_LAND:1}
- D) 参与过 IDC / 数据中心业务许可、云服务合作准入或运营商合作准入 {traits=APPROVAL:1,CLIENT_ORDER:1,BIG_TECH:1}
- E) 主要依赖设计院、顾问或政府代办，个人负责协调跟进 {traits=GOV_LAND:1,EXECUTION:1,REDFLAG:1}
- F) 只了解概念，未深度参与具体办理 {traits=REDFLAG:2}

## Q12 [short] {max=12, answer_time=4m}

请列出 AIDC 项目开工前通常需要完成或明确的审批路径和关键前置条件。请尽量按事项、主管部门、材料 / 口径、预计周期和依赖关系描述。

[rubric]
1) 覆盖备案 / 核准、节能审查、能耗统筹、环评、规划许可、施工许可、消防、水保 / 排水、电力接入等关键事项。
2) 能对应主管部门，如发改、生态环境、自然资源、住建、消防、工信 / 数据局、供电、水务或园区。
3) 能说明前置依赖，如土地性质、规划条件、能耗指标、电力接入口径、设计方案、客户需求和投资强度。
4) 能区分开工前必须完成事项、可并行推进事项和运营前完成事项。
5) 能指出常见卡点和规避动作，如节能审查、环评敏感点、消防审查、电力外线周期或材料闭环。
6) 若把审批描述成单一备案或只写“找政府协调”，应明显扣分。
[/rubric]

## Q13 [short] {max=12, answer_time=4m}

电力与能耗是项目生死线。请说明您会如何对韶关项目一期负荷可接入性进行初判，包括需要问谁、问什么、拿什么材料、如何判断周期和成本。

[rubric]
1) 能明确对接供电局、能源 / 发改环资口、园区、售电公司、绿电交易方、设计院或电力顾问。
2) 能核查一期负荷、远期负荷、接入电压等级、变电站距离、可用间隔、外线工程、接入系统方案、接入周期和成本。
3) 能把电力判断与土地选择、建设分期、PUE、液冷方案、节能审查和绿电比例联动。
4) 能说明需要形成的材料或口径，如供电初步意见、接入方案、负荷测算、外线成本估算或会议纪要。
5) 能指出风险，如容量口径不稳定、外线周期过长、能耗指标不足、绿电比例不达标或客户交付期冲突。
6) 若回答认为电力可在摘牌后再解决，应明显扣分。
[/rubric]

## Q14 [single] (0) {scoring=traits, answer_time=30s}

您对高密机柜、液冷、HVDC、GPU/NPU、网络架构和运维标准的熟悉程度更接近：

- A) 主导过完整技术方案设计、评审、招采、施工配合和交付验收，可独立输出方案 {traits=TECH_SOLUTION:2,IDC_EXP:1,EXECUTION:1}
- B) 深度参与过方案评审和落地，对关键参数、风险和供应商边界比较熟悉 {traits=TECH_SOLUTION:2,IDC_EXP:1}
- C) 熟悉部分模块，如液冷、机电、电力、网络或 GPU 服务器部署，但需要专家配合整合 {traits=TECH_SOLUTION:1,EXECUTION:1}
- D) 主要从管理或商务角度理解，对技术细节依赖设计院或供应商 {traits=EXECUTION:1,REDFLAG:1}
- E) 只了解行业概念和趋势，未参与具体方案落地 {traits=REDFLAG:2}

## Q15 [multiple] (1) {partial=true, answer_time=45s}

一期方案测算中，您认为必须先锁定哪些技术和商业参数？可多选。

- A*) 一期建设规模、负荷容量、远期扩容路径和建设周期
- B*) 机柜功率密度、GPU / NPU 或服务器配置、网络和存储方案
- C*) PUE 目标、液冷比例、供配电架构、HVDC / UPS 方案和运维标准
- D*) 电力接入方式、外线工程、接入成本、绿电比例和能耗审批路径
- E*) 客户类型、租赁 / 托管 / 算力服务模式、价格区间、交付时间和付款方式
- F*) 土地成本、土建、机电、液冷、服务器 / GPU、融资成本和收入假设
- G*) 办公装修风格、品牌视觉和招商展厅面积
- H*) 先不用锁定参数，等客户签约后再整体倒推

[rubric]
本题用于判断方案测算是否把技术、客户、电力、资金和建设周期联动。A-F 是核心参数；G 不是一期测算关键门槛；H 会带来重大推进风险。
[/rubric]

## Q16 [single] (0) {scoring=traits, answer_time=30s}

如果潜在客户只给了“未来可能需要算力”的泛泛意向，您会如何判断是真需求还是假需求？

- A) 通过需求规模、机型 / 机柜要求、交付时间、价格区间、付款方式、合同决策链和容量预留意愿逐项验证 {traits=CLIENT_ORDER:2,EXECUTION:2}
- B) 先推动签署 LOI、框架协议或容量预留条款，并把关键商务条件写清楚 {traits=CLIENT_ORDER:2,FIN_MODEL:1}
- C) 先安排技术和商务访谈，区分租赁、托管、算力服务和联合运营模式 {traits=CLIENT_ORDER:2,TECH_SOLUTION:1}
- D) 只要客户是大厂或央国企，就可以先按强需求进入投资测算 {traits=REDFLAG:2}
- E) 客户需求可以后置，先把土地和机房建起来再招商 {traits=REDFLAG:2}

## Q17 [short] {max=10, answer_time=3m}

请设计一张 AIDC 客户需求访谈表。请列出您会问客户哪些问题，以及每类问题如何帮助判断合同可能性。

[rubric]
1) 覆盖客户类型、业务场景、需求规模、GPU / NPU 或机柜要求、网络和交付时间。
2) 覆盖租赁、托管、算力服务、联合运营或容量预留等合作模式。
3) 覆盖价格区间、付款方式、合同周期、违约 / 退出安排和决策链。
4) 能识别真实需求证据，如预算、内部立项、现有资源缺口、明确时间表、技术验收标准或可签 LOI / 框架协议。
5) 能把访谈结果转化为客户需求访谈表、机会等级和下一步动作。
[/rubric]

## Q18 [single] (0) {scoring=traits, answer_time=30s}

在韶关 AIDC 项目五条线中，您最有把握直接牵头的是：

- A) 政府与土地线：候选地块、部门沟通、政府支持口径和项目专班 {traits=GOV_LAND:2,APPROVAL:1,EXECUTION:1}
- B) 客户订单线：云厂商、运营商、模型公司、算力租赁客户和央国企数字化客户 {traits=CLIENT_ORDER:2,BIG_TECH:1,EXECUTION:1}
- C) 能耗电力线：供电、能源、发改环资、绿电和接入系统方案 {traits=POWER_ENERGY:2,TECH_SOLUTION:1,EXECUTION:1}
- D) 报批报建线：备案、节能、环评、规划、消防、施工许可和设计院协调 {traits=APPROVAL:2,GOV_LAND:1,EXECUTION:1}
- E) 投融资法务线：一期投资测算、融资结构、政府支持、合同条件和退出路径 {traits=FIN_MODEL:2,EXECUTION:1}
- F) 都可以参与，但目前没有一条线能独立牵头 {traits=REDFLAG:1}

## Q19 [short] {max=12, answer_time=3m}

如果土地、电力、客户、融资四条线互相卡住：土地方要投资承诺，银行要客户订单，客户要交付时间，供电要明确负荷方案。您会如何拆解优先级并推动闭环？

[rubric]
1) 能识别四条线的条件联动关系，而不是单点推进。
2) 能提出阶段性锁定动作，如政府会议纪要、供电初步口径、客户 LOI / 容量预留、一期测算、融资意向函或条件清单。
3) 能区分必须先拿到的硬口径和可并行推进的软意向。
4) 能说明如何降低各方不确定性，如分期建设、里程碑条件、退出条款、成本敏感性测算或多客户组合。
5) 能体现总负责人视角，统筹政府、客户、电力、财务、法务、设计院和施工方。
6) 若只回答“找领导协调”或“先签客户再说”，应明显扣分。
[/rubric]

## Q20 [multiple] (1) {partial=true, answer_time=45s}

一期投资测算中，您认为必须包含哪些成本和收入项？可多选。

- A*) 土地成本、税费、前期咨询、设计、报批报建和政府相关约束成本
- B*) 土建、机电、暖通、消防、弱电、安防和装修工程
- C*) 电力接入、外线工程、变配电、备用电源和用电价格假设
- D*) 液冷系统、高密机柜、服务器 / GPU / NPU、网络、存储和运维工具
- E*) 融资成本、建设期利息、保证金、设备账期和施工方垫资条件
- F*) 租金 / 托管 / 算力服务收入、上架率、客户付款节奏、回收期、IRR 和退出路径
- G*) 品牌广告费、发布会和媒体传播预算
- H*) 不需要详细测算，先看政府补贴和客户意向即可

[rubric]
本题用于判断投资测算完整性。A-F 是核心项；G 可作为运营或招商预算但不是一期投资闭环核心；H 反映财务闭环意识不足。
[/rubric]

## Q21 [single] (0) {scoring=traits, answer_time=30s}

对于融资、政府支持、客户订单、施工方垫资和设备账期之间的关系，您的理解更接近：

- A) 应建立条件联动模型：土地和政策取决于项目强度，融资取决于订单和资产，施工 / 设备账期取决于付款保障和项目确定性 {traits=FIN_MODEL:2,EXECUTION:2}
- B) 先用一期测算和客户 LOI 形成融资沟通材料，再把银行、城投、施工方和设备方条件拉齐 {traits=FIN_MODEL:2,CLIENT_ORDER:1,EXECUTION:1}
- C) 可以分阶段推进，先拿政府支持和银行意向，再逐步补客户与设备条件 {traits=FIN_MODEL:1,GOV_LAND:1}
- D) 主要依靠政府补贴或平台公司兜底，商业订单可以后置 {traits=REDFLAG:2}
- E) 主要靠施工方和设备方垫资，项目现金流后续自然会解决 {traits=REDFLAG:2}

## Q22 [single] (0) {scoring=traits, answer_time=30s}

您认为韶关项目进入下一阶段最关键的决策门槛是：

- A) 土地可建、电力可接、能耗可批、客户真实、资金闭环五项同时有明确口径 {traits=EXECUTION:2,GOV_LAND:1,POWER_ENERGY:1,CLIENT_ORDER:1,FIN_MODEL:1}
- B) 只要政府态度积极并愿意给地，就可以先进入下一阶段 {traits=GOV_LAND:1,REDFLAG:1}
- C) 只要客户需求足够大，就可以边建边解决土地、电力和审批 {traits=CLIENT_ORDER:1,REDFLAG:2}
- D) 只要技术方案先进、PUE 目标漂亮，就可以先推动立项 {traits=TECH_SOLUTION:1,REDFLAG:1}
- E) 只要资金方愿意投，就可以先推进土地和建设 {traits=FIN_MODEL:1,REDFLAG:1}

## Q23 [single] (0) {scoring=traits, answer_time=30s}

面对过往项目中的失败、延期、预算超支、审批卡点或交付风险，您的处理方式最接近：

- A) 能坦诚复盘风险来源，快速拆解责任、时间线、替代方案和升级机制，并沉淀到后续项目流程 {traits=EXECUTION:2,IDC_EXP:1,APPROVAL:1}
- B) 能识别土地、电力、能耗、客户、施工、供应商、资金等关键风险，并推动跨部门闭环 {traits=EXECUTION:2,POWER_ENERGY:1,GOV_LAND:1}
- C) 能通过调整分期、技术方案、客户交付节奏或成本测算控制损失 {traits=EXECUTION:1,TECH_SOLUTION:1,FIN_MODEL:1}
- D) 主要依赖上级、政府或外部顾问协调，个人负责信息同步和跟进 {traits=EXECUTION:1,REDFLAG:1}
- E) 过往项目基本没有重大失败或风险，暂时没有可复盘案例 {traits=REDFLAG:1}
- F) 遇到重大风险通常由其他部门负责，自己不直接参与处置 {traits=REDFLAG:2}

## Q24 [short] {max=12, answer_time=3m}

如果您明天入职，请写出韶关 AIDC 项目 30 天推进计划。请按周列出关键动作、对接对象、交付物和需要公司支持的事项。

[rubric]
1) 计划按 30 天或 4 周拆解，能体现节奏和优先级。
2) 覆盖候选地块、政府预审、客户访谈、电力能耗、审批清单、一期测算和融资条件。
3) 每周有明确交付物，如地块对比表、政府沟通纪要、客户需求访谈表、电力与能耗初判表、审批路径清单和一期投资测算表。
4) 能说明需要公司提供的资源，如领导背书、项目资料、客户名单、技术顾问、设计院、电力顾问、财务法务支持。
5) 能设置进入下一阶段的决策门槛和风险复盘机制。
6) 若计划只写口号或日常拜访安排，缺少具体交付物，应明显扣分。
[/rubric]

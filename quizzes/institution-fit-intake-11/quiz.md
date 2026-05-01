---
id: institution-fit-intake-11
title: 量化投研适配性调研
description: |
  面向机构客户扫码进入在线客服或预约 Demo 前的前置诊断问卷。
  本试卷共 11 题，其中单选题 5 题、多选题 6 题，预计 5 分钟完成。
  重点收集客户类型、团队规模、投研流程、主要市场、数据源、回测痛点、信号管理痛点、风控留痕需求、PoC 条件与试点意愿，用于判断机构适配度和准备后续沟通。
  本问卷只用于需求诊断和 Demo 准备，不构成投资建议、收益承诺或代客理财服务。
tags: [institution-fit, quant-infra, customer-discovery, pre-sales, appointment]
schema_version: 2
format: qml-v2
question_count: 11
question_counts:
  single: 5
  multiple: 6
  short: 0
estimated_duration_minutes: 5
trait:
  dimensions: [FIT, NURTURE, COMPLEX, GOV, AUTO]
  dimension_meanings:
    FIT: 场景、团队、数据或试点条件相对清晰，适合进入 Demo 或 PoC 讨论。
    NURTURE: 当前需求仍在澄清期，适合先做需求访谈、材料补齐或方法论培育。
    COMPLEX: 涉及多市场、多接口、实时交易、权限或系统集成，交付复杂度需要提前评估。
    GOV: 更关注流程规范、风控留痕、审计复盘、管理看板与跨角色协作。
    AUTO: 更关注信号自动运行、任务调度、异常提醒与人工流程替代。
  analysis_guidance:
    paired_dimensions:
      - FIT/NURTURE：比较当前是否已具备进入 Demo 或 PoC 的清晰度。
      - COMPLEX/FIT：比较交付复杂度与先行试点可控性。
      - GOV/AUTO：识别客户更偏流程治理、风控留痕，还是更偏自动化运行和预警。
    scoring_method:
      - 单选题按选项 traits 累计，用于形成售前跟进优先级，不作为客户能力或投资适当性判断。
      - 多选题以信息采集为主，结合已选市场、数据源、痛点和 PoC 条件进行人工判断。
    interpretation:
      - FIT 较高且 PoC 条件完整时，优先安排 Demo 并准备试点范围。
      - NURTURE 较高时，先安排需求访谈或发送方法论材料，不急于推进系统报价。
      - COMPLEX 较高时，优先确认数据授权、接口权限、实时性、回测粒度和交付边界。
      - GOV 或 AUTO 较高时，Demo 应分别突出风控留痕/管理看板或自动运行/异常提醒能力。
---

## Q1 [single] (0) {scoring=traits, answer_time=25s}

您/贵机构最接近以下哪类？

- A) 私募基金 / 资管团队 {traits=FIT:2,GOV:1}
- B) 券商机构业务 / 财富管理 / 投顾服务团队 {traits=GOV:2,COMPLEX:1}
- C) 独立投研 / 量化研究团队 {traits=FIT:2,AUTO:1}
- D) 金融内容 / 策略服务团队 {traits=NURTURE:1,AUTO:1}
- E) 其他机构 {traits=NURTURE:1}

## Q2 [single] (0) {scoring=traits, answer_time=25s}

当前直接参与投研、量化、交易或风控的人数大约是？

- A) 1-3 人 {traits=NURTURE:1}
- B) 4-10 人 {traits=FIT:2,AUTO:1}
- C) 11-30 人 {traits=FIT:2,GOV:1}
- D) 30 人以上 {traits=COMPLEX:2,GOV:2}

## Q3 [single] (0) {scoring=traits, answer_time=30s}

目前贵机构的投研、回测或信号管理流程更接近哪种状态？

- A) 主要依赖 Excel、人工记录或临时表格 {traits=NURTURE:1,AUTO:1}
- B) 主要依赖 Notebook / Python 脚本，流程由研究员各自维护 {traits=FIT:1,AUTO:2}
- C) 已有自研系统，但数据、策略版本或复盘口径仍不统一 {traits=COMPLEX:1,GOV:2}
- D) 已使用专业终端或量化平台，希望进一步形成内部流程 {traits=FIT:2,GOV:1}
- E) 暂时没有稳定的投研或回测流程 {traits=NURTURE:2}

## Q4 [multiple] (1) {partial=true, answer_time=45s}

当前主要研究、服务或交易哪些标的？可多选。

- A*) A 股个股
- B*) A 股板块 / 行业 ETF
- C*) A 股宽基 ETF
- D*) 股指期货 / 股指期权
- E*) 商品期货 / 商品期权
- F*) 港股
- G*) 美股
- H*) 可转债
- I*) 基金 / FOF / 组合
- J*) 其他明确市场
- K*) 暂不确定

## Q5 [multiple] (1) {partial=true, answer_time=45s}

当前已使用或计划接入哪些数据源？可多选。

- A*) 聚宽 / JQData
- B*) Longbridge / 富途 / 老虎等 OpenAPI
- C*) QMT / MiniQMT
- D*) CTP
- E*) Wind / iFinD / Bloomberg
- F*) 券商柜台 / 极速柜台
- G*) 交易所授权行情 / 专业行情商
- H*) 内部数据
- I*) 暂不确定

## Q6 [multiple] (1) {partial=true, answer_time=45s}

当前回测或研究验证最明显的问题是什么？可多选。

- A*) 回测结果难复现，换人或换环境后结果不一致
- B*) 参数、窗口、标的池和成本假设难以横向比较
- C*) 结果散落在脚本、表格或个人电脑里
- D*) 缺少统一复盘口径和可沉淀的研究记录
- E*) 暂时没有稳定回测流程
- F*) 暂时没有明显回测痛点

## Q7 [multiple] (1) {partial=true, answer_time=45s}

当前信号或策略运行最明显的问题是什么？可多选。

- A*) 每天靠人工筛选、导表或手动运行脚本
- B*) 任务失败、数据缺失或运行异常不容易及时发现
- C*) 历史信号无法完整回填、追溯或复盘
- D*) 信号、评分、预警和复盘没有统一看板
- E*) 缺少定时调度、权限分工或任务交接机制
- F*) 暂时没有明确的信号管理需求

## Q8 [multiple] (1) {partial=true, answer_time=45s}

贵机构是否需要以下风控、留痕或管理能力？可多选。

- A*) 数据来源、处理口径和版本留痕
- B*) 策略版本、参数、标的池和成本假设留痕
- C*) 任务执行、失败重试和异常原因留痕
- D*) 风险阈值、持仓暴露或异常波动提醒
- E*) 审计、复盘或管理层报告
- F*) 暂时不需要

## Q9 [multiple] (1) {partial=true, answer_time=45s}

如果进入小范围 PoC，贵机构目前可以提供哪些材料或条件？可多选。

- A*) 1 个明确标的池
- B*) 1-2 个已有策略、公式、脚本或研究规则
- C*) 至少 1 个可用数据源或数据样例
- D*) 1 名业务 owner 参与需求确认与验收
- E*) 可以提供历史样例、日报、复盘表或现有流程截图
- F*) 暂时无法提供

## Q10 [single] (0) {scoring=traits, answer_time=30s}

本事项通常由谁推动或决策？

- A) 交易员本人 / 策略负责人 {traits=FIT:2,AUTO:1}
- B) 机构实控人 / 核心合伙人 {traits=FIT:2,GOV:1}
- C) 公司管理层 {traits=GOV:2}
- D) 投研 / 量化负责人 {traits=FIT:2,AUTO:1}
- E) 风控 / 合规负责人 {traits=GOV:2,COMPLEX:1}
- F) 多角色共同评估 {traits=COMPLEX:1,GOV:2}
- G) 暂不确定 {traits=NURTURE:2}

## Q11 [single] (0) {scoring=traits, answer_time=30s}

如果后续进入在线客服沟通或预约 Demo，贵机构当前更接近哪种状态？

- A) 已有明确场景和材料，希望尽快看 Demo 并评估 PoC {traits=FIT:2}
- B) 痛点明确，但还需要先梳理数据源、策略样本或验收口径 {traits=FIT:1,NURTURE:1}
- C) 涉及实时行情、交易接口或多系统集成，需要先评估可行性 {traits=COMPLEX:2}
- D) 主要想了解方法论和参考案例，暂不急于试点 {traits=NURTURE:2}
- E) 暂时只是了解，不进入试点或采购流程 {traits=NURTURE:2}

---
id: hnw-strategy-fit-14
title: 高净值客户策略适配画像问卷（14题）
description: |
  面向高净值客户策略沟通场景设计的画像型量表。
  本试卷共 14 题，均为单选题，以风险阈值选择题与偏好判断题为主，预计 6 分钟完成。
  每题按 traits 累计到 DDTIGHT/DDFLEX、LIQHIGH/LIQNORM、LEVNO/LEVOK、CAREFREE/CONTROL、STABLE/GROWTH、SIMPLE/COMPLEX 六组维度，用于形成风险边界、流动性偏好、杠杆接受度与省心程度画像。
  若同组维度平分，则依次比较 +2 次数、+1 次数；若仍平分，固定落位 DDTIGHT/LIQHIGH/LEVNO/CAREFREE/STABLE/SIMPLE。
  本问卷用于客户沟通中的风险收益偏好画像，不构成投资建议，也不直接替代投资适配性判断。
tags: [wealth, strategy-fit, client-profiling, traits, advisory]
schema_version: 2
format: qml-v2
question_count: 14
question_counts:
  single: 14
  multiple: 0
  short: 0
estimated_duration_minutes: 6
trait:
  dimensions: [DDTIGHT, DDFLEX, LIQHIGH, LIQNORM, LEVNO, LEVOK, CAREFREE, CONTROL, STABLE, GROWTH, SIMPLE, COMPLEX]
  dimension_meanings:
    DDTIGHT: 更关注本金安全和回撤控制，希望净值曲线更平稳。
    DDFLEX: 可接受更明显的净值波动，以换取更高的收益弹性。
    LIQHIGH: 更看重资金可用性，希望资金调用灵活、回撤恢复快。
    LIQNORM: 可接受较长持有周期与阶段性沉淀，不要求高流动性。
    LEVNO: 明确排斥杠杆或放大波动的配置方式。
    LEVOK: 在风险可解释、边界可控时，可接受一定杠杆或增强手段。
    CAREFREE: 更希望系统自动运行、减少盯盘和决策参与，偏省心托管。
    CONTROL: 更希望保留过程知情权和决策参与感，偏强控制感。
    STABLE: 更重视稳健复利、回撤约束与长期可持有体验。
    GROWTH: 更看重收益成长性，愿意接受阶段性回撤换取更高弹性。
    SIMPLE: 更偏好逻辑清晰、可解释性高、容易理解的策略框架。
    COMPLEX: 可接受相对复杂的模型与执行逻辑，只要结果与风控可验证。
  analysis_guidance:
    paired_dimensions:
      - DDTIGHT/DDFLEX：比较回撤约束优先与收益弹性容忍的主导倾向。
      - LIQHIGH/LIQNORM：比较高流动性诉求与正常持有周期接受度。
      - LEVNO/LEVOK：比较杠杆回避与受控杠杆接受度。
      - CAREFREE/CONTROL：比较省心托管诉求与过程控制诉求。
      - STABLE/GROWTH：比较稳健复利偏好与收益成长偏好。
      - SIMPLE/COMPLEX：比较可解释性优先与复杂模型接受度。
    scoring_method:
      - 将每组对立维度分别累计总分，取分高的一侧作为该组主倾向。
      - 若同组平分，则依次比较 +2 次数、+1 次数；若仍平分，固定落位 DDTIGHT/LIQHIGH/LEVNO/CAREFREE/STABLE/SIMPLE。
    interpretation:
      - 结果用于辅助顾问识别客户的风险边界、沟通方式与策略接受条件，不用于系统自动推荐唯一策略。
      - 若 DDTIGHT、STABLE、LIQHIGH 同时较强，优先讨论低回撤、低干预、恢复期较短的策略版本。
      - 若 GROWTH、DDFLEX、LEVOK 较强，可进入更高弹性的版本讨论，但仍需先说明回撤与恢复周期。
      - 若 CAREFREE 较强，应重点展示系统的自动化、省心与预警能力；若 CONTROL 较强，应重点展示逻辑透明与过程解释。
      - 若 SIMPLE 较强，优先展示逻辑清晰、规则明确的策略版本；若 COMPLEX 较强，可补充模型框架与风控分层说明。
---

## Q1 [single] (0) {scoring=traits, answer_time=20s}

如果是长期配置资金，你更容易接受的策略历史最大回撤区间是：

- A) 5%以内 {traits=DDTIGHT:2,STABLE:1}
- B) 5% - 10% {traits=DDTIGHT:2}
- C) 10% - 15% {traits=DDTIGHT:1}
- D) 15% - 20% {traits=DDFLEX:1}
- E) 20% - 30% {traits=DDFLEX:2,GROWTH:1}
- F) 30%以上 {traits=DDFLEX:2,GROWTH:2}

## Q2 [single] (0) {scoring=traits, answer_time=20s}

只要资金总体安全，我可以接受阶段性净值有较明显波动，以换取更高收益弹性。

- A) 非常同意 {traits=DDFLEX:2}
- B) 比较同意 {traits=DDFLEX:1}
- C) 中立
- D) 比较不同意 {traits=DDTIGHT:1}
- E) 非常不同意 {traits=DDTIGHT:2}

## Q3 [single] (0) {scoring=traits, answer_time=20s}

如果有临时资金使用需求，你更希望策略资金在多长时间内能完成大部分调出？

- A) 1个交易日内 {traits=LIQHIGH:2}
- B) 3个交易日内 {traits=LIQHIGH:2}
- C) 1周内 {traits=LIQHIGH:1}
- D) 1个月内 {traits=LIQNORM:1}
- E) 1-3个月内 {traits=LIQNORM:2}
- F) 3个月以上也可以接受 {traits=LIQNORM:2,STABLE:1}

## Q4 [single] (0) {scoring=traits, answer_time=20s}

对策略中使用杠杆或增强手段，你更接近哪种态度？

- A) 完全不能接受 {traits=LEVNO:2,DDTIGHT:1}
- B) 原则上不接受，除非非常特殊 {traits=LEVNO:2}
- C) 只在杠杆很克制、风控很清晰时可接受少量增强 {traits=LEVOK:1}
- D) 只要边界可控，可以接受一定增强 {traits=LEVOK:2}
- E) 为了提高收益弹性，可以接受更积极的增强方式 {traits=LEVOK:2,GROWTH:1}

## Q5 [single] (0) {scoring=traits, answer_time=20s}

我更希望系统自动运行并给出预警，不想自己频繁盯盘或参与日常决策。

- A) 非常同意 {traits=CAREFREE:2}
- B) 比较同意 {traits=CAREFREE:1}
- C) 中立
- D) 比较不同意 {traits=CONTROL:1}
- E) 非常不同意 {traits=CONTROL:2}

## Q6 [single] (0) {scoring=traits, answer_time=20s}

相比追求更高收益，我更看重长期可持有、体验平稳和净值回撤可控。

- A) 非常同意 {traits=STABLE:2}
- B) 比较同意 {traits=STABLE:1}
- C) 中立
- D) 比较不同意 {traits=GROWTH:1}
- E) 非常不同意 {traits=GROWTH:2}

## Q7 [single] (0) {scoring=traits, answer_time=20s}

如果一套策略逻辑比较复杂，即使收益不错，我也会因为不好理解而降低投入意愿。

- A) 非常同意 {traits=SIMPLE:2}
- B) 比较同意 {traits=SIMPLE:1}
- C) 中立
- D) 比较不同意 {traits=COMPLEX:1}
- E) 非常不同意 {traits=COMPLEX:2}

## Q8 [single] (0) {scoring=traits, answer_time=20s}

只要回撤能压在我能接受的范围内，我愿意牺牲一部分收益上限。

- A) 非常同意 {traits=STABLE:2,DDTIGHT:1}
- B) 比较同意 {traits=STABLE:1,DDTIGHT:1}
- C) 中立
- D) 比较不同意 {traits=GROWTH:1}
- E) 非常不同意 {traits=GROWTH:2,DDFLEX:1}

## Q9 [single] (0) {scoring=traits, answer_time=20s}

对于一笔用于策略配置的资金，你更容易接受的最短考核/观察周期是：

- A) 1周以内就要能看出效果 {traits=LIQHIGH:2,CONTROL:1}
- B) 1个月内 {traits=LIQHIGH:1}
- C) 1-3个月 {traits=LIQNORM:1}
- D) 一个季度左右 {traits=LIQNORM:2}
- E) 半年甚至更久也可以接受 {traits=LIQNORM:2,STABLE:1}

## Q10 [single] (0) {scoring=traits, answer_time=20s}

我希望了解策略为什么调仓、为什么风控，而不是只看最终收益结果。

- A) 非常同意 {traits=CONTROL:2,SIMPLE:1}
- B) 比较同意 {traits=CONTROL:1}
- C) 中立
- D) 比较不同意 {traits=CAREFREE:1}
- E) 非常不同意 {traits=CAREFREE:2}

## Q11 [single] (0) {scoring=traits, answer_time=20s}

如果一个版本历史收益更高，但需要接受更长回撤恢复期，我仍愿意认真考虑。

- A) 非常同意 {traits=GROWTH:2,DDFLEX:1}
- B) 比较同意 {traits=GROWTH:1}
- C) 中立
- D) 比较不同意 {traits=STABLE:1}
- E) 非常不同意 {traits=STABLE:2,DDTIGHT:1}

## Q12 [single] (0) {scoring=traits, answer_time=20s}

只要结果可验证、风控透明，我可以接受相对复杂的模型和执行过程。

- A) 非常同意 {traits=COMPLEX:2}
- B) 比较同意 {traits=COMPLEX:1}
- C) 中立
- D) 比较不同意 {traits=SIMPLE:1}
- E) 非常不同意 {traits=SIMPLE:2}

## Q13 [single] (0) {scoring=traits, answer_time=20s}

对于长期资金，我更愿意把“低回撤、稳定复利”放在“冲击更高收益”之前。

- A) 非常同意 {traits=STABLE:2,DDTIGHT:1}
- B) 比较同意 {traits=STABLE:1}
- C) 中立
- D) 比较不同意 {traits=GROWTH:1}
- E) 非常不同意 {traits=GROWTH:2,DDFLEX:1}

## Q14 [single] (0) {scoring=traits, answer_time=20s}

只要规则明确、风险可控，我并不排斥把一部分资金配置到更有成长性的版本里。

- A) 非常同意 {traits=GROWTH:2,LEVOK:1}
- B) 比较同意 {traits=GROWTH:1}
- C) 中立
- D) 比较不同意 {traits=STABLE:1}
- E) 非常不同意 {traits=STABLE:2,LEVNO:1}

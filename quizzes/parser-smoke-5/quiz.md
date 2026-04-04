---
id: parser-smoke-5
title: 系统解析测试问卷（5题）
description: |
  用于验证 md-quiz / QML 系统解析能力的最小样例问卷。
  本试卷共 5 题，其中单选题 3 题、多选题 1 题、简答题 1 题，预计 5 分钟完成。
  覆盖普通单选、多选、简答、traits 量表题、media 字段、welcome/end image、quiz 级与题目级评分块等常见解析要素。
tags: [parser, smoke-test, qml, demo, system-test]
schema_version: 2
format: qml-v2
question_count: 5
question_counts:
  single: 3
  multiple: 1
  short: 1
estimated_duration_minutes: 5
llm:
  model: gpt-5
  temperature: 0.0
  prompt_template: |
    请根据评分标准对考生答案打分。
    只输出 JSON，不要解释。
    JSON 必须包含字段：score、reason。

    题目：{{question}}
    评分标准：{{rubric}}
    考生回答：{{answer}}
trait:
  dimensions: [PLAN, FLEX]
  dimension_meanings:
    PLAN: 更偏向先列字段、边界和步骤，再开始实现或配置。
    FLEX: 更偏向先快速试运行，再根据反馈迭代调整。
  analysis_guidance:
    paired_dimensions:
      - PLAN/FLEX：比较结构化规划与快速试错的主导倾向。
    scoring_method:
      - 累计 PLAN 与 FLEX 的总分，取分高的一侧作为主偏好。
    interpretation:
      - 差值较大说明解析或配置习惯更稳定。
      - 差值接近说明两种工作方式都可接受，适合按任务选择。
---

![intro](./assets/test.png)

## Q1 [single] (2) {answer_time=20s}

下面哪一种题型默认要求恰好一个正确答案？

- A*) single
- B) multiple
- C) short
- D) scoring=traits

[rubric]
`single` 题默认要求恰好一个正确答案，因此答案是 A。
[/rubric]

## Q2 [multiple] (3) {partial=true, answer_time=30s}

以下哪些元素适合放进一份“解析能力测试问卷”里？

- A*) `{partial=true}`
- B*) `[rubric]...[/rubric]`
- C) 在 traits 量表题中继续使用 `*`
- D*) YAML 字符串列表形式的 `tags`
- E*) `answer_time=30s`

[rubric]
`partial=true`、`[rubric]`、YAML `tags` 和 `answer_time` 都是常见解析要素；traits 量表题中不得出现 `*`，因此 A、B、D、E 正确。
[/rubric]

## Q3 [short] {max=5, answer_time=2m}

请用一句话说明这份问卷的用途。

[rubric]
1) 随便怎么回答都给满分
[/rubric]

[llm]
prompt_template=请只输出一个 0 到 {{max_points}} 的整数，不要输出其他内容。
[/llm]

## Q4 [single] (0) {scoring=traits, answer_time=20s}

当我拿到一份新的 DSL 或配置规范时，我更倾向于先把字段和边界条件列清楚。

- A) 非常同意 {traits=PLAN:2}
- B) 比较同意 {traits=PLAN:1}
- C) 中立
- D) 比较不同意 {traits=FLEX:1}
- E) 非常不同意 {traits=FLEX:2}

[rubric]
本题为 traits 量表题，不设置正确答案，得分来自选项上的 `traits`。
[/rubric]

## Q5 [single] (2) {media=./assets/test.png, answer_time=30s, difficulty=demo}

这道题题头里的 `media=./assets/test.png` 最主要是为了测试什么？

- A*) 题头属性和资源路径是否能被系统正确识别
- B) 图片内容本身的美观程度
- C) traits 维度如何累计
- D) 简答题的自动评分效果

[rubric]
这里的 `media` 字段主要用于测试题头属性和资源路径解析，不是为了测试图片审美、traits 计算或简答评分，因此答案是 A。
[/rubric]

![outro](./assets/test.png)

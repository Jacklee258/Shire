---
id: ai-workstyle-50
title: AI 时代工作方式问卷（50题）
description: |
  面向通用知识工作者的培训诊断型混合问卷。
  本试卷共 50 题，其中 30 题为工作方式量表题，20 题为 AI 工作方式认知判断题，预计 20 分钟完成。
  画像部分按 EXP/STD、AUTO/CTRL、FAST/VERIFY、OPEN/SOLO、ITER/FIXED 五组维度累计，最终输出 5 维画像与成长建议型解释。
  认知分统一统计为 0-20 分，不并入画像结果；若维度平分，则依次比较 +2 次数、+1 次数，若仍平分，固定落位 STD/CTRL/VERIFY/OPEN/ITER。
  新增 10 道进阶工程实践题聚焦模型选型、检索增强、评测、成本与工程流水线等更深层工作方式判断。
tags: [ai, workflow, productivity, agent, future-of-work, training]
schema_version: 2
format: qml-v2
question_count: 50
question_counts:
  single: 50
  multiple: 0
  short: 0
estimated_duration_minutes: 20
trait:
  dimensions: [EXP, STD, AUTO, CTRL, FAST, VERIFY, OPEN, SOLO, ITER, FIXED]
  dimension_meanings:
    EXP: 更偏向主动尝试新工具、新流程和新方法。
    STD: 更偏向沿用已验证做法，优先追求稳定和可复制性。
    AUTO: 更偏向在边界清晰时把任务委托给 AI 或自动化流程。
    CTRL: 更偏向手动掌控关键步骤，降低黑盒不确定性。
    FAST: 更偏向先快速试跑、尽快看到结果，再逐步优化。
    VERIFY: 更偏向先验证来源、规则和风险，再进入正式使用。
    OPEN: 更偏向公开分享经验、促进团队协作和方法扩散。
    SOLO: 更偏向先独立摸索、形成闭环后再决定是否分享。
    ITER: 更偏向持续复盘和迭代，愿意不断调整 prompt、工具和流程。
    FIXED: 更偏向固化流程和稳定执行，减少频繁变化带来的成本。
  analysis_guidance:
    paired_dimensions:
      - EXP/STD：比较探索尝新与稳定沿用的主导倾向。
      - AUTO/CTRL：比较自动化委托与手动掌控的主导倾向。
      - FAST/VERIFY：比较快速试用与审慎验证的主导倾向。
      - OPEN/SOLO：比较开放协同与独立闭环的主导倾向。
      - ITER/FIXED：比较迭代学习与固定流程的主导倾向。
    scoring_method:
      - 将每组对立维度分别累计总分，取分高的一侧作为该组主倾向。
      - 若同组平分，则依次比较 +2 次数、+1 次数；若仍平分，固定落位 STD/CTRL/VERIFY/OPEN/ITER。
      - 认知判断题单独统计，不并入 traits 画像结果。
    interpretation:
      - 优先看成对维度的差值，差值越大说明工作方式偏好越稳定。
      - 若差值较小，建议解释为具备双向切换能力，而不是简单贴单一风格标签。
      - 分析时应结合岗位、任务类型和团队协作环境，不宜脱离具体工作场景孤立解读。
---

## Q1 [single] (0) {scoring=traits, answer_time=20s}

面对重复性工作时，我愿意主动尝试新的 AI 工具或方法来提升效率。

- A) 非常同意 {traits=EXP:2}
- B) 比较同意 {traits=EXP:1}
- C) 中立
- D) 比较不同意 {traits=STD:1}
- E) 非常不同意 {traits=STD:2}

## Q2 [single] (0) {scoring=traits, answer_time=20s}

只要边界清晰，我愿意先让 AI 处理部分初稿、整理或归类工作。

- A) 非常同意 {traits=AUTO:2}
- B) 比较同意 {traits=AUTO:1}
- C) 中立
- D) 比较不同意 {traits=CTRL:1}
- E) 非常不同意 {traits=CTRL:2}

## Q3 [single] (0) {scoring=traits, answer_time=20s}

拿到一个新工具时，我通常会先快速试一轮，再慢慢总结规则。

- A) 非常同意 {traits=FAST:2}
- B) 比较同意 {traits=FAST:1}
- C) 中立
- D) 比较不同意 {traits=VERIFY:1}
- E) 非常不同意 {traits=VERIFY:2}

## Q4 [single] (1) {answer_time=30s}

以下哪种提示最有助于让 AI 输出更稳定、可直接使用的结果？

- A*) 明确目标、受众、约束和输出格式
- B) 只说“帮我写得更专业一点”
- C) 先不给背景，等结果不对再说
- D) 尽量保持笼统，让 AI 自由发挥

[rubric]
高质量 prompt 通常需要明确目标、使用场景、约束条件和期望输出格式，A 最符合这一原则。
[/rubric]

## Q5 [single] (1) {answer_time=30s}

面对一项需要在效果、响应速度和预算之间做平衡的任务，哪种模型选型思路更合理？

- A*) 先明确任务目标与约束，再比较质量、延迟、成本和上下文需求
- B) 只要预算允许，就默认选择参数最大的模型
- C) 只看排行榜第一名，不必考虑具体场景
- D) 选最便宜的模型，后续质量问题再说

[rubric]
模型选型应基于目标、约束和场景权衡，而不是单看体量、价格或排行榜，答案选 A。
[/rubric]

## Q6 [single] (0) {scoring=traits, answer_time=20s}

我愿意把自己验证过的 AI 用法分享给同事、同学或团队成员。

- A) 非常同意 {traits=OPEN:2}
- B) 比较同意 {traits=OPEN:1}
- C) 中立
- D) 比较不同意 {traits=SOLO:1}
- E) 非常不同意 {traits=SOLO:2}

## Q7 [single] (0) {scoring=traits, answer_time=20s}

我会根据每次使用结果不断调整 prompt、流程或工具搭配。

- A) 非常同意 {traits=ITER:2}
- B) 比较同意 {traits=ITER:1}
- C) 中立
- D) 比较不同意 {traits=FIXED:1}
- E) 非常不同意 {traits=FIXED:2}

## Q8 [single] (0) {scoring=traits, answer_time=20s}

只要现有方法足够稳定，我通常不会主动切换到新的 AI 工具。

- A) 非常同意 {traits=STD:2}
- B) 比较同意 {traits=STD:1}
- C) 中立
- D) 比较不同意 {traits=EXP:1}
- E) 非常不同意 {traits=EXP:2}

## Q9 [single] (1) {answer_time=30s}

当你使用 AI 对一份正式材料做总结，最应该先做什么？

- A*) 对关键事实、数字和结论回查原始材料
- B) 只要语气自然就可以直接发送
- C) 结构完整就默认内容准确
- D) 再让另一个 AI 改写一次即可

[rubric]
AI 可以帮助提炼信息，但正式使用前必须回查关键事实和结论，A 是最稳妥的做法。
[/rubric]

## Q10 [single] (1) {answer_time=30s}

当任务依赖外部知识库且知识会频繁更新时，哪种方案通常比单纯微调更合适？

- A*) 先构建可更新的检索增强流程，再决定是否需要额外微调
- B) 只要做一次微调，就不再需要考虑知识更新
- C) 把所有资料都复制进 prompt，就能替代系统设计
- D) 完全依赖人工记忆资料内容即可

[rubric]
知识频繁变化时，先建立可更新的检索增强流程通常更稳妥，答案选 A。
[/rubric]

## Q11 [single] (0) {scoring=traits, answer_time=20s}

即使任务相对标准，我也更放心自己一步步手动完成。

- A) 非常同意 {traits=CTRL:2}
- B) 比较同意 {traits=CTRL:1}
- C) 中立
- D) 比较不同意 {traits=AUTO:1}
- E) 非常不同意 {traits=AUTO:2}

## Q12 [single] (0) {scoring=traits, answer_time=20s}

在把 AI 产出用于正式场景前，我通常会做较完整的核验。

- A) 非常同意 {traits=VERIFY:2}
- B) 比较同意 {traits=VERIFY:1}
- C) 中立
- D) 比较不同意 {traits=FAST:1}
- E) 非常不同意 {traits=FAST:2}

## Q13 [single] (0) {scoring=traits, answer_time=20s}

我更习惯先自己摸索清楚，再决定是否把方法告诉别人。

- A) 非常同意 {traits=SOLO:2}
- B) 比较同意 {traits=SOLO:1}
- C) 中立
- D) 比较不同意 {traits=OPEN:1}
- E) 非常不同意 {traits=OPEN:2}

## Q14 [single] (1) {answer_time=30s}

当 AI 给出一个你无法在来源材料里找到的“事实”时，最稳妥的处理是？

- A*) 标记为未核实，并回到来源或补充检索验证
- B) 因为表述具体，所以先当作可用
- C) 只要和常识不冲突就直接采用
- D) 用更强烈的语气要求 AI “不要出错” 即可

[rubric]
无法验证的内容就不应直接采用，最稳妥的做法是明确标记并回到来源验证，答案选 A。
[/rubric]

## Q15 [single] (1) {answer_time=30s}

在做检索增强系统时，哪种切分思路通常更有利于召回和引用质量？

- A*) 让每个片段尽量保持语义完整，并保留必要上下文
- B) 固定切成最短长度，越碎越好
- C) 不做切分，整库直接塞给模型
- D) 只按文件名分段，不看内容结构

[rubric]
检索增强中的切分需要兼顾语义完整性和可检索性，答案选 A。
[/rubric]

## Q16 [single] (0) {scoring=traits, answer_time=20s}

一旦找到一个能用的方法，我更希望把它固定下来，少做改动。

- A) 非常同意 {traits=FIXED:2}
- B) 比较同意 {traits=FIXED:1}
- C) 中立
- D) 比较不同意 {traits=ITER:1}
- E) 非常不同意 {traits=ITER:2}

## Q17 [single] (0) {scoring=traits, answer_time=20s}

即使现有流程基本可用，我也会继续寻找 AI 是否能带来新的工作路径。

- A) 非常同意 {traits=EXP:2}
- B) 比较同意 {traits=EXP:1}
- C) 中立
- D) 比较不同意 {traits=STD:1}
- E) 非常不同意 {traits=STD:2}

## Q18 [single] (0) {scoring=traits, answer_time=20s}

面对结构化、重复性的任务时，我会优先考虑是否能自动化。

- A) 非常同意 {traits=AUTO:2}
- B) 比较同意 {traits=AUTO:1}
- C) 中立
- D) 比较不同意 {traits=CTRL:1}
- E) 非常不同意 {traits=CTRL:2}

## Q19 [single] (1) {answer_time=30s}

在处理包含敏感内部信息的任务时，最合适的做法是？

- A*) 先确认工具和流程是否被允许，并尽量脱敏后再处理
- B) 只要效率高，就把原始资料完整上传
- C) 把敏感信息拆成多次输入就没有风险
- D) 只在非工作时间使用就没问题

[rubric]
涉及敏感数据时，应先确认合规边界并进行脱敏，答案选 A。
[/rubric]

## Q20 [single] (1) {answer_time=30s}

如果需要让模型稳定输出 JSON、表格字段或可调用的动作参数，哪种能力最值得优先利用？

- A*) 结构化输出约束或工具调用机制
- B) 让模型自由发挥，后处理再猜字段
- C) 只增加回答长度，让内容自然变结构化
- D) 反复复制同一句 prompt 直到碰巧成功

[rubric]
结构化输出和工具调用是处理规范字段与动作参数的更稳妥方案，答案选 A。
[/rubric]

## Q21 [single] (0) {scoring=traits, answer_time=20s}

面对模糊任务时，我更愿意先让 AI 生成几个版本，再择优调整。

- A) 非常同意 {traits=FAST:2}
- B) 比较同意 {traits=FAST:1}
- C) 中立
- D) 比较不同意 {traits=VERIFY:1}
- E) 非常不同意 {traits=VERIFY:2}

## Q22 [single] (0) {scoring=traits, answer_time=20s}

在团队里，我乐于和别人共同打磨 prompt 或工作流。

- A) 非常同意 {traits=OPEN:2}
- B) 比较同意 {traits=OPEN:1}
- C) 中立
- D) 比较不同意 {traits=SOLO:1}
- E) 非常不同意 {traits=SOLO:2}

## Q23 [single] (0) {scoring=traits, answer_time=20s}

一个方法即使现在有效，我也会持续迭代它，而不是长期照搬。

- A) 非常同意 {traits=ITER:2}
- B) 比较同意 {traits=ITER:1}
- C) 中立
- D) 比较不同意 {traits=FIXED:1}
- E) 非常不同意 {traits=FIXED:2}

## Q24 [single] (1) {answer_time=30s}

以下哪类工作最适合作为 AI 自动化的第一批对象？

- A*) 重复、规则相对明确、出错影响可控的任务
- B) 高风险且没有复核环节的最终决策任务
- C) 需要承担法律责任的最终审批任务
- D) 完全依赖隐性经验、无法描述标准的任务

[rubric]
AI 自动化应优先从低风险、规则清晰、可复核的任务开始，答案选 A。
[/rubric]

## Q25 [single] (1) {answer_time=30s}

如果想判断一个 AI 工作流是否真的可用，哪种评测思路更可靠？

- A*) 先定义代表性样本、验收标准和失败类型，再持续对比结果
- B) 只看一两个成功案例就可以下结论
- C) 只要主观感觉更快，就是更好的流程
- D) 只问团队里最懂工具的人是否满意

[rubric]
可靠评测依赖代表性样本、验收标准和持续比较，而不是零散成功案例，答案选 A。
[/rubric]

## Q26 [single] (0) {scoring=traits, answer_time=20s}

比起不断尝试新的工作流，我更愿意沿用已经熟悉的做法。

- A) 非常同意 {traits=STD:2}
- B) 比较同意 {traits=STD:1}
- C) 中立
- D) 比较不同意 {traits=EXP:1}
- E) 非常不同意 {traits=EXP:2}

## Q27 [single] (0) {scoring=traits, answer_time=20s}

很多工作即使能交给 AI，我仍倾向于亲自掌控细节。

- A) 非常同意 {traits=CTRL:2}
- B) 比较同意 {traits=CTRL:1}
- C) 中立
- D) 比较不同意 {traits=AUTO:1}
- E) 非常不同意 {traits=AUTO:2}

## Q28 [single] (0) {scoring=traits, answer_time=20s}

即使时间紧，我也不太愿意跳过对 AI 结果的交叉检查。

- A) 非常同意 {traits=VERIFY:2}
- B) 比较同意 {traits=VERIFY:1}
- C) 中立
- D) 比较不同意 {traits=FAST:1}
- E) 非常不同意 {traits=FAST:2}

## Q29 [single] (1) {answer_time=30s}

以下哪种场景最需要保留人工最终把关？

- A*) 对外发布、影响决策或风险较高的正式内容
- B) 日常个人灵感整理
- C) 私人草稿记录
- D) 低风险的标题备选列表

[rubric]
高风险、正式、对外的内容应保留人工最终审定，答案选 A。
[/rubric]

## Q30 [single] (1) {answer_time=30s}

如果希望降低幻觉风险，哪种做法通常比“单纯让模型更谨慎”更有效？

- A*) 让输出尽量基于可引用来源，并把无法确认的部分显式暴露出来
- B) 只把温度调低，就不用再核查来源
- C) 让模型用更自信的语气回答
- D) 只要回答更长，错误就会自动减少

[rubric]
降低幻觉更依赖 grounding、引用和不确定性暴露，而不是只调语气或参数，答案选 A。
[/rubric]

## Q31 [single] (0) {scoring=traits, answer_time=20s}

即使发现了有效的 AI 工作方法，我也未必会主动推广给别人。

- A) 非常同意 {traits=SOLO:2}
- B) 比较同意 {traits=SOLO:1}
- C) 中立
- D) 比较不同意 {traits=OPEN:1}
- E) 非常不同意 {traits=OPEN:2}

## Q32 [single] (0) {scoring=traits, answer_time=20s}

对我来说，稳定遵守既定步骤比频繁优化流程更重要。

- A) 非常同意 {traits=FIXED:2}
- B) 比较同意 {traits=FIXED:1}
- C) 中立
- D) 比较不同意 {traits=ITER:1}
- E) 非常不同意 {traits=ITER:2}

## Q33 [single] (0) {scoring=traits, answer_time=20s}

遇到新任务时，我愿意先试几种 AI 辅助方式，再决定保留哪一种。

- A) 非常同意 {traits=EXP:2}
- B) 比较同意 {traits=EXP:1}
- C) 中立
- D) 比较不同意 {traits=STD:1}
- E) 非常不同意 {traits=STD:2}

## Q34 [single] (1) {answer_time=30s}

面对一个需要基于多份资料持续回答问题的任务，哪种思路更合理？

- A*) 先明确资料边界和更新方式，再选适合检索与引用的工具流程
- B) 直接用任何聊天工具，不必区分资料来源
- C) 先让 AI 自由生成，再决定要不要看资料
- D) 只要模型参数更大，就不用考虑流程设计

[rubric]
持续性的资料型任务，关键在于先明确资料边界与更新方式，再设计合适的工具流程，答案选 A。
[/rubric]

## Q35 [single] (1) {answer_time=30s}

在重要任务中设计人机协同时，哪种做法最符合 Human-in-the-loop 思路？

- A*) 让 AI 负责提议或预处理，关键判断和高风险动作由人确认
- B) 让 AI 全自动执行所有决策，人工只看最终结果
- C) 只要模型足够强，就不再需要人工复核
- D) 只在出错后再临时决定是否介入

[rubric]
Human-in-the-loop 的核心是把关键判断和高风险节点保留给人，答案选 A。
[/rubric]

## Q36 [single] (0) {scoring=traits, answer_time=20s}

如果流程可控，我乐于让 AI 先完成 80% 的基础工作，再由我补充定稿。

- A) 非常同意 {traits=AUTO:2}
- B) 比较同意 {traits=AUTO:1}
- C) 中立
- D) 比较不同意 {traits=CTRL:1}
- E) 非常不同意 {traits=CTRL:2}

## Q37 [single] (0) {scoring=traits, answer_time=20s}

我能接受先用一个可用版本启动，再逐步打磨输出质量。

- A) 非常同意 {traits=FAST:2}
- B) 比较同意 {traits=FAST:1}
- C) 中立
- D) 比较不同意 {traits=VERIFY:1}
- E) 非常不同意 {traits=VERIFY:2}

## Q38 [single] (0) {scoring=traits, answer_time=20s}

如果一种 AI 方法对团队有帮助，我愿意推动形成共享做法。

- A) 非常同意 {traits=OPEN:2}
- B) 比较同意 {traits=OPEN:1}
- C) 中立
- D) 比较不同意 {traits=SOLO:1}
- E) 非常不同意 {traits=SOLO:2}

## Q39 [single] (1) {answer_time=30s}

当你发现一个有效的 prompt 或 AI 工作流后，最好的下一步是？

- A*) 记录适用场景、输入模板、检查点和注意事项，便于复用
- B) 只保存在聊天记录里，之后靠搜索回忆
- C) 只记住大概感觉，不必结构化沉淀
- D) 每次从头试，避免流程固化

[rubric]
有效方法需要沉淀为可复用的模板和检查点，才能真正放大价值，答案选 A。
[/rubric]

## Q40 [single] (1) {answer_time=30s}

在 AI 工程流水线里，哪种组合最有助于后续定位问题和持续优化？

- A*) 保留输入版本、关键中间结果、输出日志和失败样本
- B) 只记录最终成功结果，失败无需保留
- C) 只要有人记得当时怎么做，就不需要日志
- D) 为了省事，流程变化尽量不做任何记录

[rubric]
可观测性和失败样本沉淀是定位问题、优化流水线的关键，答案选 A。
[/rubric]

## Q41 [single] (0) {scoring=traits, answer_time=20s}

我愿意把 AI 工作流当作持续优化的对象，而不是一次定型的流程。

- A) 非常同意 {traits=ITER:2}
- B) 比较同意 {traits=ITER:1}
- C) 中立
- D) 比较不同意 {traits=FIXED:1}
- E) 非常不同意 {traits=FIXED:2}

## Q42 [single] (0) {scoring=traits, answer_time=20s}

对我来说，减少工具切换比追求新方法更重要。

- A) 非常同意 {traits=STD:2}
- B) 比较同意 {traits=STD:1}
- C) 中立
- D) 比较不同意 {traits=EXP:1}
- E) 非常不同意 {traits=EXP:2}

## Q43 [single] (0) {scoring=traits, answer_time=20s}

对我来说，亲手完成关键过程比提升速度更重要。

- A) 非常同意 {traits=CTRL:2}
- B) 比较同意 {traits=CTRL:1}
- C) 中立
- D) 比较不同意 {traits=AUTO:1}
- E) 非常不同意 {traits=AUTO:2}

## Q44 [single] (1) {answer_time=30s}

如果希望团队成员使用 AI 时得到更稳定的结果，最重要的做法是？

- A*) 固定关键步骤、输入要求和复核标准
- B) 让每个人完全自由发挥，结果自然会趋同
- C) 只强调“多试试”即可，不需要记录流程
- D) 把所有差异都归因于模型本身

[rubric]
稳定结果来自清晰流程和复核标准，而不是纯经验或自由发挥，答案选 A。
[/rubric]

## Q45 [single] (1) {answer_time=30s}

当推理成本较高而请求量持续增长时，哪种策略最有助于控制整体成本？

- A*) 优先考虑缓存、批处理、路由分层和按任务复杂度匹配模型
- B) 一律使用最强模型处理全部请求
- C) 只通过缩短 prompt 来解决一切成本问题
- D) 先不监控成本，等预算超了再说

[rubric]
成本优化通常依赖缓存、批处理、分层路由和任务分级，而不是单点做法，答案选 A。
[/rubric]

## Q46 [single] (0) {scoring=traits, answer_time=20s}

对我来说，确认依据和边界通常比尽快拿到答案更重要。

- A) 非常同意 {traits=VERIFY:2}
- B) 比较同意 {traits=VERIFY:1}
- C) 中立
- D) 比较不同意 {traits=FAST:1}
- E) 非常不同意 {traits=FAST:2}

## Q47 [single] (0) {scoring=traits, answer_time=20s}

对我来说，个人先跑通自己的闭环，比和团队共同制定规则更自然。

- A) 非常同意 {traits=SOLO:2}
- B) 比较同意 {traits=SOLO:1}
- C) 中立
- D) 比较不同意 {traits=OPEN:1}
- E) 非常不同意 {traits=OPEN:2}

## Q48 [single] (0) {scoring=traits, answer_time=20s}

如果当前流程已经达标，我通常不会再花太多精力继续调整。

- A) 非常同意 {traits=FIXED:2}
- B) 比较同意 {traits=FIXED:1}
- C) 中立
- D) 比较不同意 {traits=ITER:1}
- E) 非常不同意 {traits=ITER:2}

## Q49 [single] (1) {answer_time=30s}

团队开始使用 AI 工具时，最值得优先建立的共识是？

- A*) 哪些场景可用、哪些数据不能用、谁负责复核与沉淀
- B) 让每个人各自摸索，避免讨论规则
- C) 只要能提高效率，默认所有场景都可直接使用
- D) 先统一品牌偏好，其他问题以后再说

[rubric]
团队级使用 AI 时，优先级最高的是使用边界、数据限制、复核责任和沉淀机制，答案选 A。
[/rubric]

## Q50 [single] (1) {answer_time=30s}

如果团队希望一个 prompt 或 workflow 在几周后仍能稳定复现，最关键的做法是？

- A*) 对输入模板、依赖资料、版本变更和检查标准进行明确记录
- B) 只把最终答案保存下来即可
- C) 完全依赖个人经验，不需要版本化
- D) 每次重新探索，避免约束方法

[rubric]
可复现性依赖输入模板、依赖资料、版本变更和检查标准的记录，答案选 A。
[/rubric]

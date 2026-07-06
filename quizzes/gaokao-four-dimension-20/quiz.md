---
id: gaokao-four-dimension-20
title: 高考报志愿四维测试简化版
description: |
  面向直播间免费测评场景设计的高考志愿方向测试。
  本测试共 20 题，均为 5 选 1 单选题，预计 5 分钟完成。
  测试从“学校、专业、城市、就业”四个维度判断考生和家庭在志愿选择中的优先级。
  结果只用于初步方向判断，不预测录取概率，不替代省考试院政策、高校招生章程、正式招生专业目录和志愿填报系统。
  请不要在公开直播间提交身份证号、准考证号、手机号、志愿系统账号密码、家庭详细地址等敏感信息。
tags: [gaokao, college-application, volunteer-choice, live, traits]
schema_version: 2
format: qml-v2
question_count: 20
question_counts:
  single: 20
  multiple: 0
  short: 0
estimated_duration_minutes: 5
trait:
  dimensions: [SCHOOL, MAJOR, CITY, CAREER]
  dimension_meanings:
    SCHOOL: 更重视学校层次、平台、名气、保研升学和长期资源。
    MAJOR: 更重视专业兴趣、学习内容、能力适配和专业发展路径。
    CITY: 更重视城市资源、实习机会、生活半径和未来发展地点。
    CAREER: 更重视就业稳定、收入回报、职业路径和家庭资源匹配。
  analysis_guidance:
    scoring_method:
      - 每题选项按 SCHOOL、MAJOR、CITY、CAREER 四个维度累计得分。
      - 单一维度明显最高时，判断为该维度优先型。
      - 最高两个维度接近时，判断为双核心型，例如“专业城市型”“城市就业型”“学校专业型”。
      - 四个维度接近时，判断为平衡稳妥型。
    interpretation:
      - 本测试用于帮助家庭讨论取舍顺序，不用于预测录取概率。
      - 正式填报前必须核验当年招生计划、专业组代码、选科要求、招生章程、学费、校区、体检限制和单科要求。
      - 如果家庭分歧明显，应先明确底线，再做冲稳保方案。
---

## Q1 [single] (0) {scoring=traits, answer_time=20s}

如果学校层次和专业兴趣发生冲突，你更倾向怎么选？

- A) 优先学校层次，专业可以适当妥协 {traits=SCHOOL:2}
- B) 学校略优先，但专业不能太差 {traits=SCHOOL:1,MAJOR:1}
- C) 学校和专业都要具体比较 {traits=SCHOOL:1,MAJOR:1}
- D) 专业兴趣更重要，学校可以降一点 {traits=MAJOR:2}
- E) 还没有想清楚 {traits=CAREER:1}

## Q2 [single] (0) {scoring=traits, answer_time=20s}

你最希望大学给你带来什么？

- A) 更好的学校平台和学历背书 {traits=SCHOOL:2}
- B) 真正适合自己的专业能力 {traits=MAJOR:2}
- C) 更好的城市见识和机会 {traits=CITY:2}
- D) 更明确的就业出路 {traits=CAREER:2}
- E) 四个方面都想兼顾 {traits=SCHOOL:1,MAJOR:1,CITY:1,CAREER:1}

## Q3 [single] (0) {scoring=traits, answer_time=20s}

如果能去更好的城市，但学校层次一般，你能接受吗？

- A) 很能接受，城市机会很重要 {traits=CITY:2}
- B) 可以接受，但专业要匹配 {traits=CITY:1,MAJOR:1}
- C) 需要看具体学校和专业 {traits=SCHOOL:1,MAJOR:1,CITY:1}
- D) 不太接受，学校层次更重要 {traits=SCHOOL:2}
- E) 更看毕业就业是否稳定 {traits=CAREER:2}

## Q4 [single] (0) {scoring=traits, answer_time=20s}

你现在最担心志愿填报出现什么问题？

- A) 分数没用好，学校层次亏了 {traits=SCHOOL:2}
- B) 被录到不喜欢或不适合的专业 {traits=MAJOR:2}
- C) 城市太偏，未来机会少 {traits=CITY:2}
- D) 毕业后不好就业或收入不稳定 {traits=CAREER:2}
- E) 滑档、退档或规则没看懂 {traits=CAREER:1,SCHOOL:1}

## Q5 [single] (0) {scoring=traits, answer_time=20s}

选择专业时，你最看重哪一点？

- A) 这个专业是否在强校里读 {traits=SCHOOL:2}
- B) 自己是否真的感兴趣、学得进去 {traits=MAJOR:2}
- C) 这个专业所在城市有没有产业机会 {traits=CITY:2}
- D) 未来就业、考公、考研是否有路径 {traits=CAREER:2}
- E) 家长和孩子能否达成一致 {traits=MAJOR:1,CAREER:1}

## Q6 [single] (0) {scoring=traits, answer_time=20s}

面对热门专业，你的态度更接近哪一种？

- A) 热门专业最好在更高层次学校里读 {traits=SCHOOL:2}
- B) 要看自己能力和兴趣是否匹配 {traits=MAJOR:2}
- C) 要看城市产业是否支撑这个方向 {traits=CITY:2}
- D) 要看就业是否真的稳定和有回报 {traits=CAREER:2}
- E) 不想盲目跟风，需要综合判断 {traits=MAJOR:1,CAREER:1}

## Q7 [single] (0) {scoring=traits, answer_time=20s}

如果一个专业你喜欢，但就业不确定，你会怎么选？

- A) 如果学校平台好，可以接受 {traits=SCHOOL:2}
- B) 仍愿意优先考虑，因为兴趣重要 {traits=MAJOR:2}
- C) 如果城市机会多，可以尝试 {traits=CITY:2}
- D) 会谨慎，优先选择就业更稳的方向 {traits=CAREER:2}
- E) 需要家里一起讨论后决定 {traits=MAJOR:1,CAREER:1}

## Q8 [single] (0) {scoring=traits, answer_time=20s}

你对离开本省读大学的态度是？

- A) 只要学校层次好，全国都可以 {traits=SCHOOL:2}
- B) 如果专业合适，可以去外省 {traits=MAJOR:2}
- C) 更愿意去大城市或产业强城市 {traits=CITY:2}
- D) 要看毕业就业和家庭支持情况 {traits=CAREER:2}
- E) 尽量不离家太远 {traits=CITY:1,CAREER:1}

## Q9 [single] (0) {scoring=traits, answer_time=20s}

你更希望毕业后在哪里发展？

- A) 学校平台能带我去哪里都可以 {traits=SCHOOL:2}
- B) 去专业对口的地方 {traits=MAJOR:2}
- C) 一线、新一线或省会城市 {traits=CITY:2}
- D) 哪里工作稳定、收入合适就去哪里 {traits=CAREER:2}
- E) 优先本省或家乡附近 {traits=CITY:1,CAREER:1}

## Q10 [single] (0) {scoring=traits, answer_time=20s}

家庭对大学费用的态度更接近哪一种？

- A) 为了更好学校，可以适当增加投入 {traits=SCHOOL:2}
- B) 为了适合专业，可以接受合理投入 {traits=MAJOR:2}
- C) 城市生活成本也要重点考虑 {traits=CITY:2}
- D) 要看性价比和就业回报 {traits=CAREER:2}
- E) 尽量选择稳妥、低风险方案 {traits=CAREER:2}

## Q11 [single] (0) {scoring=traits, answer_time=20s}

你对考研的态度更接近哪一种？

- A) 希望本科平台好，为考研或保研打基础 {traits=SCHOOL:2}
- B) 希望专业方向适合长期深造 {traits=MAJOR:2}
- C) 希望城市有更好高校和实习资源 {traits=CITY:2}
- D) 看就业需要，必要时再考研 {traits=CAREER:2}
- E) 暂时没想过 {traits=CAREER:1}

## Q12 [single] (0) {scoring=traits, answer_time=20s}

如果专业组里有你不太接受的专业，你会怎么处理？

- A) 为了学校层次，可以接受一定调剂 {traits=SCHOOL:2}
- B) 不愿意，专业不适合风险太大 {traits=MAJOR:2}
- C) 如果城市和学校都好，可以再考虑 {traits=CITY:1,SCHOOL:1}
- D) 要看调剂后就业风险大不大 {traits=CAREER:2}
- E) 需要逐个专业核验后再决定 {traits=MAJOR:1,CAREER:1}

## Q13 [single] (0) {scoring=traits, answer_time=20s}

你觉得“好大学”的核心价值是什么？

- A) 名气、平台、校友和升学资源 {traits=SCHOOL:2}
- B) 强专业和高质量课程 {traits=MAJOR:2}
- C) 所在城市带来的机会 {traits=CITY:2}
- D) 更好的就业起点 {traits=CAREER:2}
- E) 帮学生找到长期方向 {traits=MAJOR:1,CAREER:1}

## Q14 [single] (0) {scoring=traits, answer_time=20s}

家长和孩子意见不一致时，你认为应优先解决什么？

- A) 先明确能上到什么学校层次 {traits=SCHOOL:2}
- B) 先确认孩子到底适合什么专业 {traits=MAJOR:2}
- C) 先确认能接受哪些城市 {traits=CITY:2}
- D) 先确认未来就业和家庭底线 {traits=CAREER:2}
- E) 先把四个维度排序 {traits=SCHOOL:1,MAJOR:1,CITY:1,CAREER:1}

## Q15 [single] (0) {scoring=traits, answer_time=20s}

你更认同下面哪句话？

- A) 学校平台会影响未来很多机会 {traits=SCHOOL:2}
- B) 专业不适合，大学四年会很痛苦 {traits=MAJOR:2}
- C) 城市决定见识、实习和机会密度 {traits=CITY:2}
- D) 志愿最终要服务就业和长期生活 {traits=CAREER:2}
- E) 没有绝对答案，要看孩子情况 {traits=SCHOOL:1,MAJOR:1,CITY:1,CAREER:1}

## Q16 [single] (0) {scoring=traits, answer_time=20s}

如果分数刚好够冲一个更高层次学校，你会怎么做？

- A) 值得冲，学校层次很关键 {traits=SCHOOL:2}
- B) 只有专业能接受才冲 {traits=MAJOR:2}
- C) 如果城市好，也愿意冲 {traits=CITY:2}
- D) 要先看退档、调剂和就业风险 {traits=CAREER:2}
- E) 冲稳保要分层，不能全冲 {traits=CAREER:1,SCHOOL:1}

## Q17 [single] (0) {scoring=traits, answer_time=20s}

你最希望测评结果帮你解决什么？

- A) 判断学校层次怎么取舍 {traits=SCHOOL:2}
- B) 初步筛选适合的专业方向 {traits=MAJOR:2}
- C) 判断适合去哪些城市 {traits=CITY:2}
- D) 判断未来就业路径和风险 {traits=CAREER:2}
- E) 帮家长和孩子统一思路 {traits=MAJOR:1,CAREER:1}

## Q18 [single] (0) {scoring=traits, answer_time=20s}

对于医学、法学、师范、金融这类家长高关注专业，你更看重什么？

- A) 是否在高层次学校或强校读 {traits=SCHOOL:2}
- B) 孩子是否适合长期学习这个方向 {traits=MAJOR:2}
- C) 所在城市是否有行业资源 {traits=CITY:2}
- D) 就业门槛、稳定性和投入产出 {traits=CAREER:2}
- E) 不能盲目跟风，要综合判断 {traits=MAJOR:1,CAREER:1}

## Q19 [single] (0) {scoring=traits, answer_time=20s}

如果只能牺牲一个维度，你最不愿意牺牲的是？

- A) 学校层次 {traits=SCHOOL:2}
- B) 专业方向 {traits=MAJOR:2}
- C) 所在城市 {traits=CITY:2}
- D) 就业确定性 {traits=CAREER:2}
- E) 现在还无法排序 {traits=SCHOOL:1,MAJOR:1,CITY:1,CAREER:1}

## Q20 [single] (0) {scoring=traits, answer_time=20s}

最后做志愿方案时，你更希望采用哪种策略？

- A) 平台优先，在可接受专业内冲更好学校 {traits=SCHOOL:2}
- B) 专业优先，围绕适合方向选学校 {traits=MAJOR:2}
- C) 城市优先，围绕发展城市做组合 {traits=CITY:2}
- D) 就业优先，优先稳妥路径和风险控制 {traits=CAREER:2}
- E) 平衡型，学校、专业、城市、就业都别太偏 {traits=SCHOOL:1,MAJOR:1,CITY:1,CAREER:1}

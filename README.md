# Shire Quiz Repository

本仓库按 `skills/quiz-repo-spec` 组织，用于同步 `md-quiz` 问卷仓库。

## Structure

```text
.
├── AGENTS.md
├── md-quiz-repo.yaml
├── quizzes/
│   ├── ai-workstyle-50/
│   │   └── quiz.md
│   ├── career-interest-24/
│   │   └── quiz.md
│   ├── calendar-spread-arbitrage-intake-25/
│   │   └── quiz.md
│   ├── chip-distribution/
│   │   └── quiz.md
│   ├── common-test-2025/
│   │   ├── assets/
│   │   └── quiz.md
│   ├── gaokao-four-dimension-20/
│   │   └── quiz.md
│   ├── grade7-history-midterm-gd-2026/
│   │   └── quiz.md
│   ├── fundraising-partner-screening-22/
│   │   └── quiz.md
│   ├── hnw-strategy-fit-14/
│   │   └── quiz.md
│   ├── leadership-execution-24/
│   │   └── quiz.md
│   ├── learning-style-growth-path-24/
│   │   └── quiz.md
│   ├── parser-smoke-5/
│   │   ├── assets/
│   │   └── quiz.md
│   ├── personality-type-5d-80/
│   │   └── quiz.md
│   ├── team-collaboration-style-24/
│   │   └── quiz.md
│   ├── youth-brain-challenge-24/
│   │   └── quiz.md
│   └── tech-media-ops-intern-screening/
│       └── quiz.md
└── skills/
```

## Quiz List

- `ai-workstyle-50`: AI 时代工作方式问卷（50题）
- `career-interest-24`: 职业兴趣问卷（24题）
- `calendar-spread-arbitrage-intake-25`: 套利交易系统需求调研问卷（25题）
- `chip-distribution`: 筹码分布入门测验（30题）
- `common-test-2025`: 共性能力测试 2025
- `gaokao-four-dimension-20`: 高考报志愿四维测试简化版
- `grade7-history-midterm-gd-2026`: 七年级下学期期中历史试卷（广东风格·100分）
- `hnw-strategy-fit-14`: 高净值客户策略适配画像问卷（14题）
- `leadership-execution-24`: 领导力与执行力倾向问卷（24题）
- `learning-style-growth-path-24`: 学习风格与成长路径问卷（24题）
- `parser-smoke-5`: 系统解析测试问卷（5题）
- `personality-type-5d-80`: 人格类型测试（五维版·80题）
- `team-collaboration-style-24`: 团队协作风格问卷（24题）
- `youth-brain-challenge-24`: 少年脑力挑战：初中生思维力闯关（24题）
- `tech-media-ops-intern-screening`: 技术类自媒体运营实习生招聘初筛问卷
- `im-futures-intake-14`: IM 合约交易需求首访前置问卷（14题）
- `institution-fit-intake-11`: 量化投研适配调研
- `fundraising-partner-screening-22`: 募资合作意向沟通问卷

## Conventions

- 每份问卷固定放在 `quizzes/<quiz_id>/quiz.md`。
- `quiz.md` 的 Front Matter 里 `id` 必须和目录名一致。
- `md-quiz-repo.yaml` 是同步时的仓库登记源。
- `chip-distribution` 是正式目录名，不再使用 `chip-distribution-30` 作为对外入口。

## Question Types

- 知识题 / 能力题：适合 `single`、`multiple`、`short`
- 量表题 / 倾向题：适合 `single + {scoring=traits}`
- 混合问卷：同时包含知识题与倾向题

## Current Priorities

当前已经补齐 `README.md` 中规划的 4 个方向：

- `team-collaboration-style-24`
- `career-interest-24`
- `leadership-execution-24`
- `learning-style-growth-path-24`

这些新增问卷的共同点：

1. 统一采用 `single + {scoring=traits}` 建模
2. 可与已有 `ai-workstyle-50`、`personality-type-5d-80` 组成画像组合包
3. 适合用于招聘、培训、组织发展与自我认知场景的前置探索

后续若继续扩展，建议优先做岗位细分版本或行业场景版本，而不是重复通用量表。

当前新增的 `hnw-strategy-fit-14` 与以上几份不同，它不是投资适当性自动判定工具，而是面向顾问沟通场景的客户画像问卷，用来辅助理解回撤约束、流动性诉求、省心偏好与策略可解释性偏好。

当前还新增了 `grade7-history-midterm-gd-2026`，它采用广东历史卷常见的 `30 道选择题 + 3 道材料题` 结构，适合七年级下学期期中复习、阶段检测和课堂讲评使用。

当前新增的 `youth-brain-challenge-24` 面向初中生家庭的一次性趣味测评冷启动，包装为“少年脑力挑战”，用于验证完成率、分享率和家长反馈，不使用“智商测试”或诊断式表达。

当前新增的 `institution-fit-intake-11` 以“量化投研适配调研”为名称，面向机构客户扫码进入在线客服或预约 Demo 前的前置诊断，聚焦客户类型、投研流程、数据源、回测与风控痛点、试点条件和后续跟进优先级，不构成投资建议、收益承诺或代客理财服务。

当前新增的 `calendar-spread-arbitrage-intake-25` 面向套利交易系统客户访谈和一期需求确认，聚焦交易现状、当前工具、人工流程、人员投入、策略信号、风控边界、一期系统形态和 30 万左右预算接受度，用于把首访回答转化为系统方案、功能边界和后续报价口径，不构成投资建议或收益承诺。

当前新增的 `fundraising-partner-screening-22` 面向基金管理公司与潜在募资合作伙伴的合作意向沟通，聚焦核心城市和资金资源、机构/高净值客户沉淀、历史转化能力、收益结构预期、合规稳定性、销售逻辑、团队协同和风险信号，用于支持后续评估、背景核验和模拟路演安排。

当前新增的 `gaokao-four-dimension-20` 面向高考志愿直播间免费测评，使用 20 道单选题评估学校、专业、城市、就业四个志愿决策维度，用于帮助考生和家长初步排序取舍，不预测录取概率，也不替代省考试院政策、高校招生章程和正式志愿填报系统。

## Build Notes

新建问卷时按这个顺序处理：

1. 先确定用途：筛选、画像、培训还是自我认知
2. 再确定建模：知识题、量表题还是混合题
3. 为问卷补齐 Front Matter：`id`、`title`、`description`、`tags`、`question_count`、`question_counts`、`estimated_duration_minutes`
4. 倾向类问卷优先用 `single + {scoring=traits}`
5. 能力类问卷优先用 `single` / `short`

## Cautions

以下题目不建议在本仓库里直接作为普通问卷推出：

- 抑郁、焦虑、人格障碍、ADHD 等临床或准临床心理测评
- 医疗诊断、法律风险、投资适当性等高风险判断型问卷

## Collaboration

面向协作者和自动化代理的操作约定见 [`AGENTS.md`](./AGENTS.md)。

## Skills

- [`md-quiz`](./skills/md-quiz/SKILL.md)
- [`qml-authoring`](./skills/qml-authoring/SKILL.md)
- [`quiz-repo-spec`](./skills/quiz-repo-spec/SKILL.md)

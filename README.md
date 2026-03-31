# Shire Quiz Repository

本仓库已按 `skills/quiz-repo-spec` 重构为可同步的 `md-quiz` 仓库。

## 结构

```text
.
├── md-quiz-repo.yaml
├── quizzes/
│   └── common-test-2025/
│       ├── quiz.md
│       └── assets/
└── skills/
```

## Quiz 列表

- `common-test-2025`: 共性能力测试2025

## Skills

仓库内当前维护两份与问卷编辑直接相关的 skill：

- [`qml-authoring`](./skills/qml-authoring/SKILL.md)
  用于编写、修订和校验 `quiz.md` 的 QML 语法，包括题头格式、`answer_time`、`[rubric]`、首尾图片和 parser 边界。对应参考规范见 [`qml-spec.md`](./skills/qml-authoring/references/qml-spec.md)。
- [`quiz-repo-spec`](./skills/quiz-repo-spec/SKILL.md)
  用于维护可同步的问卷仓库结构，包括 `md-quiz-repo.yaml`、`quizzes/<quiz_id>/quiz.md`、`assets/` 路径和同步契约。对应参考规范见 [`repo-contract.md`](./skills/quiz-repo-spec/references/repo-contract.md)。

## 协作约定

面向协作者和自动化代理的仓库操作约定见 [`AGENTS.md`](./AGENTS.md)。

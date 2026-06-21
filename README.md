# Interview Review Coach Skill

一个面向产品经理面试复盘的 Agent Skill，重点适用于产品经理和 AI 产品岗位。它帮助智能体读取面试记录、JD 和简历，生成结构化复盘、薄弱点诊断、追问练习和跨面试记忆。

## 适用场景

- 产品经理面试复盘
- AI 产品岗位面试复盘
- 面试记录、JD、简历的交叉分析
- 下一轮面试追问准备
- 候选人薄弱点的长期追踪

## 文件结构

```text
interview-review-coach-skill/
├── SKILL.md
├── references/
│   └── interview-review-v2.md
└── memory/
    └── MEMORY.md
```

## 安装方式

把整个 `interview-review-coach-skill/` 文件夹放到目标智能体支持的 skills 目录中，或在对话中显式要求智能体读取该目录。

常见目录示例：

- Codex: `~/.codex/skills/` 或 `~/.agents/skills/`
- Claude Code: `~/.claude/skills/`

## 使用方式

准备同一个面试的材料：

- 面试记录或会议纪要
- 岗位 JD
- 候选人简历

然后让智能体使用 `interview-review-coach` 进行复盘。默认输出中文，除非用户明确要求其他语言。

## 迁移到其他岗位

如果仍是产品经理或 AI 产品岗位，只需要替换简历、JD 和面试记录。

如果要用于非产品经理岗位，可以保留文件读取、证据提取、复盘、练习和 memory 流程，但需要调整 `references/interview-review-v2.md` 中的岗位能力模型：

- 问题分类
- 评分维度
- 回答框架
- 模拟追问
- 薄弱点追踪分类

## 说明

`SKILL.md` 是智能体读取的入口；`references/interview-review-v2.md` 是详细复盘模板；`memory/MEMORY.md` 用于沉淀候选人画像、历史面试记录和反复出现的薄弱点。

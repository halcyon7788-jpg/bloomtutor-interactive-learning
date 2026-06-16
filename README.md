# BloomTutor Interactive Learning

基于 Bloom 精熟学习理论的交互式 Markdown 学习系统——Claude Code Skill。

## 这是什么

BloomTutor 把你和 Claude 的对话变成一套结构化的交互式课程。每节课是一个 Markdown 文件，包含讲解、脚手架练习、多层次测验、费曼复述和反馈区。你学完后在同一个文件底部写下答案和疑问，Claude 读取反馈后决定：继续下一课、补救薄弱点、还是插入整合回顾。


## 安装

把 `SKILL.md` 放到 `~/.claude/skills/bloomtutor-interactive-learning/` 下：

```bash
mkdir -p ~/.claude/skills/bloomtutor-interactive-learning
cp SKILL.md ~/.claude/skills/bloomtutor-interactive-learning/SKILL.md
```

不需要重启，Claude Code 自动发现新 skill。

## 使用

在 Claude Code 中说：

- "带我系统学认知失调理论"
- "我想用交互式学习的方式读《思考，快与慢》"
- "我写完了"（提交当前课的答案，获取下一课）
- "上一课我没太懂"（触发补救）

## 文件结构

```
认知失调理论/
├── 00_前测诊断.md      # 诊断现有水平，调整路线
├── 01_核心概念.md      # 第一课
├── 02_失调强度.md      # 第二课
├── 03_减少策略.md      # 第三课（含间隔检索）
├── 04_整合回顾.md      # 整合检查点
└── ...
```

## 适合谁

- 想系统学一个领域但不想被课程平台锁定的自学者
- 偏好 Markdown + 本地文件、希望学习记录完全归自己所有
- 需要结构化引导而非被动阅读的学习者

## 许可

MIT

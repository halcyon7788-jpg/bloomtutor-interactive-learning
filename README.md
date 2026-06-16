# BloomTutor Interactive Learning

基于 Bloom 精熟学习理论的交互式 Markdown 学习系统——Claude Code Skill。

## 这是什么

BloomTutor 把你和 Claude 的对话变成一套结构化的交互式课程。每节课是一个 Markdown 文件，包含讲解、脚手架练习、多层次测验、费曼复述和反馈区。你学完后在同一个文件底部写下答案和疑问，Claude 读取反馈后决定：继续下一课、补救薄弱点、还是插入整合回顾。

## 与原始版的区别

原始版来自 [cryyy020416/bloomtutor-interactive-learning-skill](https://github.com/cryyy020416/bloomtutor-interactive-learning-skill)，本版新增以下改进：

| 改进 | 说明 |
|------|------|
| **费曼复述** | 每节课要求用户用大白话解释核心概念，AI 挑出理解缺口 |
| **前测诊断** | 学习前先评估现有知识，调整路线，不盲目从零开始 |
| **间隔检索** | 第 3 课起，每节开头 2 道来自旧课的题目，对抗遗忘 |
| **Bloom 六层提问** | 记忆→理解→应用→分析→评价→创造，系统覆盖 |
| **多样化补救** | 5 种误解类型对应 5 种策略，不再只有"讲简单一点" |
| **认知负荷阶梯** | 完整示例（跟着看）→ 补全练习（补一半）→ 章末检验（独立做） |
| **精简模板** | 去掉全局导航、术语单独成段等冗余，术语改为内联解释 |
| **跨课整合** | 每 4 课一次整合回顾，把知识从列表变成网络 |

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

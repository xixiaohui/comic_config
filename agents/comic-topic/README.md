# comic-topic - 《父与女》选题策划助手

![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![OpenClaw](https://img.shields.io/badge/OpenClaw-2026.3.12+-brightgreen)

## 📋 简介

**comic-topic** 是《父与女》四格漫画 IP 的选题策划官。它负责：

- 🔍 每日分析小红书热点
- 💡 生成 5-7 条高质量选题
- 📊 基于数据驱动的选题评分
- 🎯 为 comic-script 提供精准选题
- 📈 持续优化选题模型，支持 IP 增长

---

## 🎯 核心职责

| 职责 | 说明 |
|------|------|
| **热点分析** | 每日采集小红书热搜、评论、用户需求 |
| **选题生成** | 生成适配四格漫画的创意选题建议 |
| **智能评分** | 使用数据驱动模型为选题评分（1-10 分） |
| **文案生成** | 为每条选题生成 3 个标题和 5-8 个标签 |
| **故事框架** | 提供四格漫画的故事大纲和视觉指导 |
| **模型迭代** | 根据实际反馈持续优化评分模型 |

---

## 📂 文件说明

| 文件 | 用途 | 关键内容 |
|------|------|--------|
| **SOUL.md** | 角色定义 | 使命、原则、工作范围 |
| **IDENTITY.md** | 身份卡 | 基本信息、能力清单、关系图 |
| **AGENTS.md** | 工作流程 | 日度、周度、月度任务详解 |
| **TOOLS.md** | 工具清单 | browser、file_read/write、json_processor |
| **USER.md** | 项目配置 | 人物设定、KPI、发布计划、评分模型 |
| **MEMORY.md** | 长期记忆 | 历史选题、评分数据、协作记录 |
| **BOOTSTRAP.md** | 首次启动 | 初始化检查、自定义配置 |
| **HEARTBEAT.md** | 定时任务 | 日度、周度、月度任务清单 |
| **README.md** | 本文档 | 快速参考和常见问题 |

---

## 🚀 快速开始

### 前置条件

- OpenClaw 2026.3.12+
- 小红书账号（已登录，获取 Cookie）
- 网络连接正常

### 首次运行

\`\`\`bash
# 1. 验证所有文件都已就位
ls -la agents/comic-topic/
# 应输出 9 个 .md 文件

# 2. 启动 OpenClaw Gateway（如果还未启动）
openclaw gateway start &

# 3. 加载 comic-topic 这个 agent
sleep 2
openclaw agents add comic-topic ./agents/comic-topic

# 4. 尝试第一次运行
openclaw chat --agent comic-topic "生成本周选题 4 个"
\`\`\`

---

## 📊 评分模型

comic-topic 使用 4 维度的综合评分模型：

\`\`\`
FINAL_SCORE = 
  情感共鸣度 × 0.40 +
  平台互动潜力 × 0.30 +
  热点相关度 × 0.15 +
  差异化程度 × 0.15
\`\`\`

---

## 🔧 常用命令

### 生成选题

\`\`\`bash
# 生成 5 条选题（默认）
openclaw chat --agent comic-topic "生成选题"

# 生成特定主题的选题
openclaw chat --agent comic-topic "生成春季主题的选题 3 个"
\`\`\`

### 启动定时任务

\`\`\`bash
# 启动所有定时任务
openclaw heartbeat start comic-topic

# 查看任务状态
openclaw heartbeat status comic-topic
\`\`\`

---

## 📈 KPI 目标（3 个月）

| 指标 | 目标 | 说明 |
|------|------|------|
| **粉丝增长** | 0 → 2000-3000 | 第一个月 500-1500 |
| **单篇点赞** | 3k → 8k | 平均点赞数 |
| **评分准确度** | R² > 0.75 | 预测值与实际值 |
| **选题采纳率** | > 90% | comic-script 采纳率 |

---

## 📞 获取帮助

### 常见问题

**Q: 如何修改人物设定？**
A: 编辑 USER.md 中的 father 和 daughter 部分，然后重新加载配置。

**Q: 选题评分准确度不高怎么办？**
A: 查看 MEMORY.md 中的评分历史，找出规律，调整 USER.md 中的权重参数。

**Q: 能否提高选题生成频率？**
A: 可以，在 HEARTBEAT.md 中修改调度时间。

---

## 📄 许可证

MIT License

---

**让我们一起为《父与女》创造温暖而有趣的故事！** ✨🎨
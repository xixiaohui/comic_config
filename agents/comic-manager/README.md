# comic-manager - 《父与女》IP 运营管理助手

**Status**: Active | **Version**: 1.0.0 | **Role**: Operations Manager

## 📋 简介

comic-manager 是《父与女》四格漫画 IP 的总运营官。它负责：

- 📊 协调 comic-topic、comic-script、comic-draw 三个 agent
- 🔄 管理从选题到发布的完整生产流程
- 📈 监控 IP 运营数据和读者反馈
- 🎯 优化内容策略，推动 IP 持续成长

## 🎯 核心职责

| 职责 | 说明 |
|------|------|
| 流程协调 | 统筹三个创作 agent 的协作流程 |
| 质量管控 | 审核最终内容，确保发布标准 |
| 数据分析 | 分析运营数据，驱动策略优化 |
| 异常处理 | 监控并处理流程异常 |
| 报告生成 | 定期生成运营报告 |

## 📂 文件说明

| 文件 | 用途 |
|------|------|
| SOUL.md | 运营官的灵魂与使命 |
| IDENTITY.md | 运营官的身份卡 |
| AGENTS.md | 运营流程与步骤 |
| TOOLS.md | 可用工具清单 |
| USER.md | 运营配置与发布计划 |
| MEMORY.md | 历史数据与最佳实践 |
| BOOTSTRAP.md | 首次启动引导 |
| HEARTBEAT.md | 定时任务清单 |
| README.md | 运营快速参考 |

## 🚀 快速开始

```bash
# 1. 加载 comic-manager agent
openclaw agents add comic-manager ./agents/comic-manager

# 2. 启动定时任务
openclaw heartbeat start comic-manager

# 3. 启动每日运营流程
openclaw chat --agent comic-manager "开始今日运营"
```

## 📊 管理架构

```
comic-manager (总指挥)
    ├─ comic-topic (选题生成)
    ├─ comic-script (脚本编写)
    └─ comic-draw (漫画绘制)
```

## 📈 核心 KPI

| 指标 | 目标 |
|------|------|
| 日更完成率 | > 95% |
| 生产周期 | < 2 小时 |
| 质量合格率 | > 90% |
| 读者满意度 | > 4.5/5 |
| 月增粉率 | > 10% |

---

让《父与女》IP 持续成长，感动更多读者！ 📊✨
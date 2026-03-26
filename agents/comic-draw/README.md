# comic-draw - 《父与女》漫画绘制助手

**Status**: Active | **Version**: 1.0.0 | **Role**: Lead Artist

## 📋 简介

comic-draw 是《父与女》四格漫画 IP 的首席画师。它负责：

- 🎨 接收 comic-script 提供的脚本 JSON
- 🖼️ 将脚本转化为精美的四格漫画图像
- 👥 维护角色视觉一致性
- ✨ 确保每幅漫画达到发布标准

## 🎯 核心职责

| 职责 | 说明 |
|------|------|
| 脚本解析 | 理解并分析脚本的视觉要求 |
| 漫画绘制 | 生成高质量的四格漫画图像 |
| 角色维护 | 保持父亲和七七的视觉一致性 |
| 质量控制 | 确保漫画达到发布标准 |
| 反馈沟通 | 与 comic-script 反馈绘制问题 |

## 📂 文件说明

| 文件 | 用途 |
|------|------|
| SOUL.md | 画师的灵魂与艺术理念 |
| IDENTITY.md | 画师的身份卡 |
| AGENTS.md | 绘制流程与步骤 |
| TOOLS.md | 可用工具清单 |
| USER.md | 角色视觉规范与画风配置 |
| MEMORY.md | 历史绘制记录与角色参考 |
| BOOTSTRAP.md | 首次启动引导 |
| HEARTBEAT.md | 定时任务清单 |
| README.md | 画师快速参考 |

## 🚀 快速开始

```bash
# 1. 加载 comic-draw agent
openclaw agents add comic-draw ./agents/comic-draw

# 2. 启动定时任务
openclaw heartbeat start comic-draw

# 3. 首次测试绘制
openclaw chat --agent comic-draw "根据脚本绘制漫画"
```

## 📊 质量标准

- 角色一致性：> 95%
- 脚本还原度：> 90%
- 发布就绪率：> 90%
- 平均完成时间：< 60 min

---

让每一幅漫画都成为 IP 的经典！ 🎨✨
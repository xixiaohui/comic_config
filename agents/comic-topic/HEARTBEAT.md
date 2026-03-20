# Heartbeat - comic-topic 定时任务清单

## 心跳任务概述

comic-topic 通过定期的自动化任务（HEARTBEAT）保持活力。这些任务确保我们每天都能坚持生成高质量的选题。

---

## 日度任务 (DAILY @ 08:00)

**触发时间**: 每日早晨 08:00
**预计耗时**: 15-20 分钟
**优先级**: 🔴 最高

### 任务清单

\`\`\`
[08:00] DAILY HEARTBEAT START
  ├─ [ ] 加载配置文件 (USER.md, MEMORY.md)
  ├─ [ ] 采集小红书热点数据 (browser tool)
  │   ├─ [ ] 浏览热搜 TOP 20
  │   ├─ [ ] 采集亲子相关话题
  │   └─ [ ] 记录热点关键词
  ├─ [ ] 生成 5-7 条选题
  ├─ [ ] 评分与排序
  ├─ [ ] 生成标题和标签
  ├─ [ ] 生成选题 JSON
  ├─ [ ] 验证数据完整性
  ├─ [ ] 更新 MEMORY.md
  └─ [ ] 输出结果
[08:20] DAILY HEARTBEAT END ✅
\`\`\`

---

## 周度任务 (WEEKLY @ MON 14:00)

**触发时间**: 每周一下午 14:00
**预计耗时**: 30-40 分钟

### 任务清单

\`\`\`
[14:00] WEEKLY ANALYSIS START
  ├─ [ ] 汇总本周数据
  ├─ [ ] 深度分析
  ├─ [ ] 模型微调
  ├─ [ ] 生成周度报告
  └─ [ ] 发送报告给 comic-commander
[14:40] WEEKLY ANALYSIS END ✅
\`\`\`

---

## 月度任务 (MONTHLY @ 1ST 09:00)

**触发时间**: 每月 1 日早晨 09:00
**预计耗时**: 60-90 分钟

### 任务清单

\`\`\`
[09:00] MONTHLY REVIEW START
  ├─ [ ] 数据汇总
  ├─ [ ] 评分模型评估
  ├─ [ ] 策略调整
  ├─ [ ] 生成月度报告
  └─ [ ] 分享给全部 agents
[10:30] MONTHLY REVIEW END ✅
\`\`\`

---

## 快速参考

### 启动 Heartbeat

\`\`\`bash
# 启动所有定时任务
openclaw heartbeat start comic-topic

# 查看任务状态
openclaw heartbeat status comic-topic
\`\`\`

### 手动触发任务

\`\`\`bash
# 触发日度任务
openclaw chat --agent comic-topic "执行日度分析"

# 查看日志
tail -f logs/comic-topic_$(date +%Y-%m-%d).log
\`\`\`

---

**记住**: 定时任务是系统的心跳。只要心跳保持规律，《父与女》的故事就会源源不断地诞生。💫
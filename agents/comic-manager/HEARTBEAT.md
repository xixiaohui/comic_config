# Heartbeat - comic-manager 定时任务清单

## 心跳任务概述
comic-manager 通过持续监控和定期复盘保障 IP 稳定运营。

## 日度任务 (DAILY)

### 晨间巡检 (DAILY @ 09:00)
```
[09:00] MORNING CHECK START
  ├─ 检查所有 agent 状态
  ├─ 确认当日选题就绪
  ├─ 预览当日生产计划
  └─ 发送晨报摘要
[09:10] END
```

### 傍晚发布确认 (DAILY @ 18:30)
```
[18:30] PUBLISH CHECK START
  ├─ 确认当日漫画完成
  ├─ 最终质量审核
  ├─ 确认发布时间
  └─ 准备发布素材
[18:45] END
```

### 晚间数据复盘 (DAILY @ 21:00)
```
[21:00] EVENING REVIEW START
  ├─ 收集当日发布数据
  ├─ 分析读者互动
  ├─ 记录异常情况
  ├─ 更新 MEMORY.md
  └─ 生成日报
[21:15] END
```

## 周度任务 (WEEKLY @ SUN 20:00)
```
[20:00] WEEKLY REVIEW START
  ├─ 汇总本周数据
  ├─ 评估各 agent 表现
  ├─ 分析内容效果趋势
  ├─ 优化下周选题方向
  └─ 生成周报
[21:00] END
```

## 月度任务 (MONTHLY @ LAST DAY 21:00)
```
[21:00] MONTHLY REVIEW START
  ├─ 汇总本月所有数据
  ├─ 评估 IP 整体发展
  ├─ 制定下月运营策略
  └─ 生成月报
[22:00] END
```

记住: 稳定的运营是 IP 成功的基石。📊
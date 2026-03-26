# Bootstrap - comic-manager 首次启动引导

## 欢迎来到《父与女》IP 运营管理中心！

📊 您好！我是 comic-manager，IP 的总运营官。

---

## 初始化检查清单

### ✅ Step 1: 验证核心文件

请确认以下文件已在 agents/comic-manager/ 目录中：
- [x] SOUL.md
- [x] IDENTITY.md
- [x] AGENTS.md
- [x] TOOLS.md
- [x] USER.md
- [x] MEMORY.md
- [x] HEARTBEAT.md
- [x] README.md

### ✅ Step 2: 验证其他 Agent 状态

确认以下 agent 已就绪：
- agents/comic-topic/ ✅
- agents/comic-script/ ✅
- agents/comic-draw/ ✅

### ✅ Step 3: 首次运营测试

启动完整流水线测试：
```bash
openclaw chat --agent comic-manager "启动今日内容生产流程"
```

## 常见问题

**Q: 如何处理 agent 故障？**
A: 参考 AGENTS.md 中的异常处理流程，根据故障级别执行对应预案。

**Q: 如何查看运营数据？**
A: 查看 MEMORY.md 中的运营数据汇总，或使用 data_analyzer 工具。

---

祝运营顺利！让《父与女》IP 持续扩大影响力。 📊✨
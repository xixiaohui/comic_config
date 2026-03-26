# Bootstrap - comic-script 首次启动引导

## 欢迎来到《父与女》脚本编写部门！

🎬 您好！我是 comic-script，您的脚本编导。

---

## 初始化检查清单

### ✅ Step 1: 验证核心文件

请确认以下文件已在 agents/comic-script/ 目录中：
- [x] SOUL.md
- [x] IDENTITY.md
- [x] AGENTS.md
- [x] TOOLS.md
- [x] USER.md
- [x] MEMORY.md
- [x] HEARTBEAT.md
- [x] README.md

### ✅ Step 2: 验证依赖项

确认以下文件和目录存在：
- data/templates/script-template.json
- data/schema/script.schema.json
- data/outputs/
- data/examples/

### ✅ Step 3: 首次测试

创建一个测试脚本：
```bash
openclaw chat --agent comic-script "根据这个选题编写脚本：{选题 JSON}"
```

## 常见问题

**Q: 如何编写高质量脚本？**
A: 参考 USER.md 中的脚本编写标准、表情指导、构图建议。

**Q: 脚本需要修改多少次？**
A: 目标首次通过率 > 80%。

**Q: 能否和 comic-draw 直接沟通？**
A: 可以。通过发送结构化的脚本 JSON 和详细说明。

---

祝您创作愉快！让我们一起把故事变成精美的四格漫画。 🎨🎬
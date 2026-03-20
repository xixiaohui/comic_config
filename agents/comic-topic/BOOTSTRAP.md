# Bootstrap - comic-topic 首次启动引导

## 欢迎来到《父与女》选题策划助手！

🎉 您好！我是 comic-topic，您的内容策划官。

本文件在您**首次运行**时执行，用于完成系统的初始化。完成后可删除此文件。

---

## 初始化检查清单

### ✅ Step 1: 验证核心文件

请确认以下文件已在 agents/comic-topic/ 目录中：

- [x] SOUL.md
- [x] IDENTITY.md
- [x] AGENTS.md
- [x] TOOLS.md
- [x] USER.md
- [x] MEMORY.md
- [x] HEARTBEAT.md
- [x] README.md

### ✅ Step 2: 验证环境变量

确认以下环境变量已在 .env 中配置：

\`\`\`bash
OPENCLAW_GATEWAY_URL=http://localhost:3000
OPENAI_API_KEY=sk-xxx
XIAOHONGSHU_COOKIE=xxx
\`\`\`

### ✅ Step 3: 检查数据目录

确保以下目录存在：

\`\`\`
data/
├─ templates/
├─ schema/
├─ examples/
└─ outputs/

logs/
\`\`\`

### ✅ Step 4: 首次运行测试

尝试触发第一次选题生成：

\`\`\`bash
openclaw chat --agent comic-topic "生成春季选题 3 个"
\`\`\`

---

## 常见问题

### Q: 如何修改人物设定？
A: 编辑 USER.md 中的人物部分，然后重新加载配置。

### Q: 选题评分准确度不高怎么办？
A: 查看 MEMORY.md 中的评分历史，找出规律，调整 USER.md 中的权重参数。

### Q: 首次运行后是否需要保留 BOOTSTRAP.md？
A: 可以删除或保留都可以。

---

**祝您使用愉快！让我们一起为这个世界创造更多温暖的故事。** 🎨✨
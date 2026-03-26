# Bootstrap - comic-draw 首次启动引导

## 欢迎来到《父与女》漫画绘制部门！

🎨 您好！我是 comic-draw，您的首席漫画画师。

---

## 初始化检查清单

### ✅ Step 1: 验证核心文件

请确认以下文件已在 agents/comic-draw/ 目录中：
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
- data/references/characters/ (角色参考图)
- data/outputs/scripts/ (接收 comic-script 的脚本 JSON)
- data/outputs/comics/ (输出漫画图像)

### ✅ Step 3: 首次测试

测试绘制流程：
```bash
openclaw chat --agent comic-draw "根据这个脚本绘制漫画：{脚本 JSON}"
```

## 常见问题

**Q: 如何保持角色一致性？**
A: 参考 MEMORY.md 中的角色参考图，并严格遵循 USER.md 中的视觉规范。

**Q: 脚本描述不清楚怎么办？**
A: 反馈给 comic-script，请求补充说明。

---

祝您创作愉快！用画笔讲述最美的父女故事。 🎨✨
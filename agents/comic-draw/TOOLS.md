# Tools - comic-draw 可用工具清单

## 工具总览

| 工具 | 用途 | 频率 | 耗时 | 成本 |
|------|------|------|------|------|
| image_generate | AI 图像生成 | 每次执行 | 30-60 s | $0.02 |
| image_edit | 图像编辑修改 | 按需 | 20-40 s | $0.01 |
| file_read | 读取脚本和参考 | 每次执行 | < 100 ms | $0 |
| file_write | 保存图像和日志 | 每次执行 | < 500 ms | $0 |

---

## 工具详解

### 1. **image_generate** - AI 图像生成工具

**用途**: 根据脚本描述生成漫画图像

**参数配置**:
- 风格: 日漫风格、温暖色调、四格漫画
- 分辨率: 1200×1600px（四格竖版）
- 格式: PNG

---

### 2. **image_edit** - 图像编辑工具

**用途**: 修改已生成图像，修正细节

**常见操作**:
- 调整角色表情
- 修改背景元素
- 优化色彩

---

### 3. **file_read** - 文件读取工具

**文件清单**:
- data/outputs/scripts_YYYY-MM-DD.json (脚本)
- data/references/characters/ (角色参考图)
- agents/comic-draw/MEMORY.md (历史记录)

---

### 4. **file_write** - 文件写入工具

**文件路径约定**:
- 图像输出: data/outputs/comics_YYYY-MM-DD/
- 日志: logs/comic-draw_YYYY-MM-DD.log

---

## 成本与性能

| 工具 | 日均调用 | 日均成本 |
|------|---------|---------|
| image_generate | 4-8 | $0.08-0.16 |
| image_edit | 2-4 | $0.02-0.04 |
| file_read/write | 10-16 | $0 |
| **总计** | **~20** | **< $0.25/day** |
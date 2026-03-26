# Tools - comic-script 可用工具清单

## 工具总览

| 工具 | 用途 | 频率 | 耗时 | 成本 |
|------|------|------|------|------|
| file_read | 读取选题和参考资料 | 每次执行 | < 100 ms | $0 |
| file_write | 保存脚本和日志 | 每次执行 | < 100 ms | $0 |
| json_processor | 生成和验证脚本 JSON | 每次执行 | < 500 ms | $0 |

---

## 工具详解

### 1. **file_read** - 文件读取工具

**用途**: 读取选题 JSON、参考资料、脚本模板、历史脚本

**文件清单**:
- data/outputs/topics_YYYY-MM-DD.json (选题)
- data/templates/script-template.json (脚本模板)
- agents/comic-script/MEMORY.md (历史脚本)
- data/examples/ (参考脚本)

---

### 2. **file_write** - 文件写入工具

**用途**: 保存生成的脚本、记录日志、更新内存

**文件路径约定**:
- 脚本输出: data/outputs/scripts_YYYY-MM-DD.json
- 日志: logs/comic-script_YYYY-MM-DD.log
- 内存更新: agents/comic-script/MEMORY.md

---

### 3. **json_processor** - JSON 处理工具

**用途**: 生成脚本 JSON、验证数据结构、转换数据格式

#### 子功能 A: validate - JSON 验证
验证生成的脚本 JSON 是否符合 Schema 定义。

#### 子功能 B: generate - JSON 生成
使用模板和变量生成完整的脚本 JSON。

---

## 工具使用规范

✅ **DO**:
- 每次生成脚本后立即验证 JSON 格式
- 使用 append 模式保留脚本历史
- 记录详细的日志信息
- 与 comic-topic 和 comic-draw 及时沟通

❌ **DON'T**:
- 不要直接修改 comic-topic 的选题
- 不要删除历史脚本数据
- 不要绕过质量检查流程
- 不要生成无法绘制的内容

---

## 成本与性能

| 工具 | 日均调用 | 性能 |
|------|---------|------|
| file_read | 4-7 | < 100 ms |
| file_write | 4-7 | < 100 ms |
| json_processor | 8-14 | < 500 ms |
| **总计** | **~20** | **< 25 min** |
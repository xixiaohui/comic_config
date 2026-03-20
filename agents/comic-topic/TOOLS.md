# Tools - comic-topic 可用工具清单

## 工具总览

| 工具 | 用途 | 频率 | 耗时 | 成本 |
|------|------|------|------|------|
| browser | 采集热点数据 | 每日 1 次 | 5-7 min | $0 |
| file_read | 读取配置与历史数据 | 每次执行 | < 100 ms | $0 |
| file_write | 更新内存和日志 | 每日 1 次 | < 100 ms | $0 |
| json_processor | JSON 生成与验证 | 每日多次 | < 500 ms | $0 |

---

## 工具详解

### 1. **browser** - 热点数据采集工具

**用途**: 浏览小红书，采集热点话题、评论、互动数据

**调用场景**: 每日 HEARTBEAT @ 08:00

**示例代码**:
\`\`\`json
{
  "tool": "browser",
  "action": "fetch_xiaohongshu_trending",
  "params": {
    "url": "https://xiaohongshu.com/explore/trending",
    "keywords": ["父女", "亲子", "成长", "教育"],
    "limit": 20,
    "timeout": 300
  }
}
\`\`\`

**使用限制**:
- 每日最多调用 1 次（避免频繁请求）
- 遵守小红书 robots.txt
- 返回结果自动缓存 24 小时

---

### 2. **file_read** - 文件读取工具

**用途**: 读取 MEMORY.md、USER.md、历史数据和配置

**调用频率**: 每次工作流执行时都会调用

**文件清单**:
- agents/comic-topic/MEMORY.md
- agents/comic-topic/USER.md
- data/templates/topic-template.json
- data/schema/topic.schema.json

---

### 3. **file_write** - 文件写入工具

**用途**: 更新 MEMORY.md、记录选题历史、写入日志

**调用频率**: 每日执行结束时（1 次）

**使用规范**:
- mode: "append" 追加到文件末尾（保留历史）
- timestamp: true 自动添加时间戳
- 每次写入不超过 10 KB

---

### 4. **json_processor** - JSON 处理工具

**用途**: 生成选题 JSON、验证数据结构、转换数据格式

#### 子功能 A: **validate** - JSON 验证
验证生成的选题 JSON 是否符合 Schema 定义。

#### 子功能 B: **generate** - JSON 生成
使用模板和变量生成完整的选题 JSON。

#### 子功能 C: **transform** - JSON 转换
将多个选题 JSON 转换为 CSV 或其他格式。

---

## 成本与性能

| 工具 | 日均调用 | 月均成本 | 性能 |
|------|---------|---------|------|
| browser | 1 | $0 | 5-7 min |
| file_read | 3-5 | $0 | < 100 ms |
| file_write | 2 | $0 | < 100 ms |
| json_processor | 20+ | $0 | < 500 ms |
| **总计** | **~25** | **$0** | **< 20 min** |

---

## 工具最佳实践

✅ **DO**:
- browser 工具仅在 08:00 执行，避免频繁请求
- file_write 使用 append 模式保留历史数据
- json_processor 每次生成后必须验证
- 遵守小红书 robots.txt 和服务条款

❌ **DON'T**:
- 不要并发调用 file_write（易产生冲突）
- 不要使用 browser 抓取个人隐私信息
- 不要删除或覆盖 MEMORY.md 中的历史数据
- 不要生成违反小红书社区规则的选题
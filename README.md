
## 📦 Skill 包清单

### 1. 🗜️ asclaude-compact (v1.0.0)

**文件名**: `session-compact-1.0.0.tar.gz` (11KB)

**简介**:
智能会话压缩工具，基于 Claude Code 的 Session Memory Compact 机制。自动归档长对话、生成结构化摘要、节省 90-98% tokens，零成本运行（不调用 LLM）。

**核心功能**:
- ✅ 自动归档长对话（50k tokens 阈值）
- ✅ 生成结构化摘要（关键决策、错误修复）
- ✅ 微压缩清理旧工具结果
- ✅ 自动监控会话长度
- ✅ 持久化记忆到 session-memory.md
- ✅ 支持手动 `/compact` 命令

**适用场景**:
- 对话太长，响应变慢
- 需要回顾之前的关键决策
- 节省 tokens 成本
- 知识沉淀和归档

**安装方式**:
```bash
openclaw skills install session-compact
```

**文件结构**:
```
session-compact-1.0.0/
├── SKILL.md                 # 主文档（详细使用说明）
├── README.md                # 快速入门
├── scripts/
│   ├── compact-trigger.py   # 手动压缩脚本
│   ├── micro-compact.py     # 微压缩脚本
│   └── compact-monitor.py   # 自动监控脚本
└── docs/                    # 技术文档（可选）
```

**性能指标**:
- 压缩率: 90-98%
- 速度: 100ms (Micro) / 1-3s (Full)
- 成本: $0（不调用 LLM）
- Token 节省: 50k → 1-5k

---

### 2. 🔍 asclaude-grep (v1.0.0)

**文件名**: `file-search-tools-1.0.0.tar.gz` (6.4KB)

**简介**:
智能文件搜索工具，提供 GrepTool（内容搜索）和 GlobTool（路径匹配）两大功能。支持正则表达式、上下文行、通配符匹配、JSON 输出，速度快、零成本、精准搜索。

**核心功能**:

**GrepTool** - 文件内容搜索:
- ✅ 支持正则表达式
- ✅ 显示上下文行（前后 N 行）
- ✅ 多文件并行搜索
- ✅ JSON 格式输出
- ✅ 最大结果数限制

**GlobTool** - 文件路径匹配:
- ✅ 支持通配符 `*`, `**`, `?`
- ✅ 按文件类型过滤（file/dir/all）
- ✅ 显示文件大小统计
- ✅ 递归搜索支持
- ✅ JSON 格式输出

**适用场景**:
- 代码审查：查找特定函数、变量
- 错误排查：搜索错误信息、日志
- 重构辅助：查找所有使用某函数的地方
- 文件定位：快速找到特定类型文件
- 项目分析：统计文件类型、大小

**安装方式**:
```bash
openclaw skills install file-search-tools
```

**文件结构**:
```
file-search-tools-1.0.0/
├── SKILL.md                 # 主文档（详细使用说明）
├── README.md                # 快速入门
├── scripts/
│   ├── grep-tool.py         # GrepTool 核心脚本
│   └── glob-tool.py         # GlobTool 核心脚本
└── docs/                    # 高级用法文档（可选）
```

**性能对比**:
| 工具 | 速度 | 成本 | 灵活性 | 易用性 |
|------|------|------|--------|--------|
| GrepTool | ⚡⚡⚡ | $0 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| GlobTool | ⚡⚡⚡ | $0 | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| LLM 搜索 | ⚡ | $0.5-2 | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |

---

<p align="center">
  <img src="docs/images/logo.png" alt="OpenClaw Skill Developer Guide" width="200">
</p>

<h1 align="center">OpenClaw Skill Developer Guide</h1>

<p align="center">
  <strong>🦞 从零到一掌握 OpenClaw Skill 开发的权威指南</strong>
</p>

<p align="center">
  <a href="#-项目介绍">介绍</a> •
  <a href="#-效果展示">效果展示</a> •
  <a href="#-快速开始">快速开始</a> •
  <a href="#-文档目录">文档</a> •
  <a href="#-示例项目">示例</a> •
  <a href="#-贡献指南">贡献</a>
</p>

<p align="center">
  <a href="https://github.com/openclaw/openclaw-skill-developer-guide/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-Apache%202.0-blue.svg" alt="License">
  </a>
  <a href="https://docs.openclaw.ai">
    <img src="https://img.shields.io/badge/docs-openclaw.ai-green.svg" alt="Documentation">
  </a>
  <a href="https://clawhub.com">
    <img src="https://img.shields.io/badge/marketplace-clawhub.com-purple.svg" alt="ClawHub">
  </a>
  <a href="https://discord.gg/clawd">
    <img src="https://img.shields.io/discord/123456789.svg?label=Discord&logo=discord" alt="Discord">
  </a>
</p>

---

## 📖 项目介绍

**OpenClaw Skill Developer Guide** 是一个面向开发者的 OpenClaw Skill 开发教程与示例项目合集。无论你是刚接触 OpenClaw 的新手，还是想要深入了解 Skill 开发的资深开发者，这个项目都能帮助你快速上手并掌握最佳实践。

### 什么是 OpenClaw？

[OpenClaw](https://github.com/openclaw/openclaw) 是一个开源的个人 AI 助手平台，支持多种消息渠道（WhatsApp、Telegram、Discord、Slack 等），可运行在任何操作系统上。

### 什么是 Skill？

Skill 是 OpenClaw 的核心扩展机制。一个 Skill 就像是一个"专家指南"，它告诉 AI 助手如何完成特定的任务：

- 🎯 **专注领域** - 每个 Skill 专注于一个特定领域或任务
- 🔧 **工具集成** - 提供命令行工具、API 调用等能力
- 📚 **知识注入** - 将专业知识和最佳实践注入 AI
- 🚀 **即插即用** - 安装后立即可用，无需重启

### 为什么需要这个项目？

- ✅ **完整的开发教程** - 从概念到实践的完整指南
- ✅ **可运行的示例** - 3 个完整可运行的 Skill 项目
- ✅ **最佳实践** - 符合官方规范的开发模式
- ✅ **安全合规** - 隐私保护、权限管理的最佳实践
- ✅ **发布指南** - 如何发布到 ClawHub 市场

---

## 🎬 效果展示

### 示例 1：文件自动保存 Skill

```
用户: 帮我把这份报告保存到 data 目录
OpenClaw: ✅ 已将报告保存到 /root/.openclaw/workspace/data/report.md
         📄 文件大小: 2.3 KB
         📅 保存时间: 2026-03-12 10:30:00
```

### 示例 2：定时任务 Skill

```
用户: 每天早上 9 点提醒我开晨会
OpenClaw: ✅ 已创建定时任务
         ⏰ 触发时间: 每天 09:00 (Asia/Shanghai)
         📝 任务内容: 提醒开晨会
         🔄 下次执行: 2026-03-13 09:00:00
```

### 示例 3：AI 文章生成 Skill

```
用户: 帮我写一篇关于 Molmo2 的技术文章
OpenClaw: ✅ 已生成技术文章
         📊 字数: 约 8000 字
         📁 保存位置: data/articles/molmo2-technical-report.md
         ⏱️ 生成耗时: 45 秒
```

---

## 🚀 快速开始

### 前置要求

- **OpenClaw** >= 2026.3.0
- **Node.js** >= 22.0.0
- **Git**
- **curl** (用于下载资源)

### 安装步骤

#### 方式一：克隆仓库

```bash
# 克隆项目
git clone https://github.com/openclaw/openclaw-skill-developer-guide.git

# 进入项目目录
cd openclaw-skill-developer-guide

# 安装示例 Skill
./scripts/install-examples.sh
```

#### 方式二：从 ClawHub 安装

```bash
# 安装示例 Skill
openclaw skill install openclaw-skill-developer-guide/auto-save
openclaw skill install openclaw-skill-developer-guide/timer-task
openclaw skill install openclaw-skill-developer-guide/ai-article-generator
```

### 验证安装

```bash
# 查看已安装的 Skill
openclaw skill list

# 测试 Skill 是否工作
openclaw agent --message "帮我保存一段测试文本到 test.txt"
```

---

## 📚 文档目录

### 入门教程

| 文档 | 描述 | 难度 |
|------|------|------|
| [01-什么是Skill](docs/01-what-is-skill.md) | 理解 Skill 的概念和作用 | ⭐ |
| [02-环境准备](docs/02-environment-setup.md) | 配置开发环境 | ⭐ |
| [03-第一个Skill](docs/03-first-skill.md) | 创建你的第一个 Skill | ⭐⭐ |
| [04-目录结构](docs/04-directory-structure.md) | 理解 Skill 目录结构 | ⭐⭐ |
| [05-SKILL.md详解](docs/05-skill-md-guide.md) | 掌握 SKILL.md 编写规范 | ⭐⭐⭐ |

### 进阶教程

| 文档 | 描述 | 难度 |
|------|------|------|
| [06-脚本开发](docs/06-script-development.md) | 编写 Shell/Python 脚本 | ⭐⭐⭐ |
| [07-引用文件](docs/07-references-guide.md) | 使用 references 管理知识 | ⭐⭐⭐ |
| [08-模板资源](docs/08-assets-guide.md) | 使用 assets 管理资源 | ⭐⭐⭐ |
| [09-调试技巧](docs/09-debugging.md) | Skill 调试与测试 | ⭐⭐⭐ |
| [10-发布流程](docs/10-publishing.md) | 发布到 ClawHub | ⭐⭐⭐⭐ |

### 安全与最佳实践

| 文档 | 描述 |
|------|------|
| [安全规范](docs/security-guidelines.md) | 隐私保护、权限管理、数据安全 |
| [代码规范](docs/coding-standards.md) | 编码风格、命名约定、注释规范 |
| [性能优化](docs/performance-tips.md) | 优化 Skill 性能的最佳实践 |
| [常见问题](docs/faq.md) | FAQ 与故障排除 |

---

## 🎯 示例项目

### 示例 1：文件自动保存 Skill

**位置**: `examples/auto-save/`

**功能**:
- 智能保存文本到指定目录
- 自动创建目录结构
- 文件冲突处理
- 保存历史记录

**学习要点**:
- 基础 Skill 结构
- Shell 脚本集成
- 错误处理
- 用户反馈

```bash
# 安装
openclaw skill install ./examples/auto-save

# 使用
openclaw agent --message "保存这份会议纪要到 data/meetings/"
```

### 示例 2：定时任务 Skill

**位置**: `examples/timer-task/`

**功能**:
- 创建、管理定时任务
- 支持 cron 表达式
- 任务状态监控
- 任务历史记录

**学习要点**:
- OpenClaw Cron API 集成
- Python 脚本开发
- 状态管理
- 事件通知

```bash
# 安装
openclaw skill install ./examples/timer-task

# 使用
openclaw agent --message "每天下午3点提醒我喝水"
```

### 示例 3：AI 文章生成 Skill

**位置**: `examples/ai-article-generator/`

**功能**:
- AI 驱动的文章生成
- 多种文章模板
- 自动保存和索引
- 文章元数据管理

**学习要点**:
- 复杂工作流设计
- 多文件协作
- 模板系统
- 输出格式化

```bash
# 安装
openclaw skill install ./examples/ai-article-generator

# 使用
openclaw agent --message "帮我写一篇关于量子计算的技术文章"
```

---

## 🛠️ 项目结构

```
openclaw-skill-developer-guide/
├── 📁 docs/                      # 文档目录
│   ├── 📁 images/                # 图片资源
│   ├── 01-what-is-skill.md       # 什么是 Skill
│   ├── 02-environment-setup.md   # 环境准备
│   ├── 03-first-skill.md         # 第一个 Skill
│   ├── ...                       # 更多教程
│   ├── security-guidelines.md    # 安全规范
│   ├── coding-standards.md       # 代码规范
│   └── faq.md                    # 常见问题
│
├── 📁 examples/                  # 示例 Skill
│   ├── 📁 auto-save/             # 示例1: 文件自动保存
│   │   ├── SKILL.md              # Skill 定义
│   │   ├── scripts/              # 脚本目录
│   │   │   └── save_file.sh      # 保存脚本
│   │   └── references/           # 参考文档
│   │       └── best-practices.md
│   │
│   ├── 📁 timer-task/            # 示例2: 定时任务
│   │   ├── SKILL.md
│   │   ├── scripts/
│   │   │   ├── create_cron.py    # 创建任务
│   │   │   ├── list_crons.py     # 列出任务
│   │   │   └── delete_cron.py    # 删除任务
│   │   └── references/
│   │       └── cron-format.md    # Cron 格式说明
│   │
│   └── 📁 ai-article-generator/  # 示例3: AI文章生成
│       ├── SKILL.md
│       ├── scripts/
│       │   └── generate_article.py
│       ├── references/
│       │   ├── writing-guide.md  # 写作指南
│       │   └── templates.md      # 模板说明
│       └── assets/
│           ├── tech-template.md   # 技术文章模板
│           └── tutorial-template.md
│
├── 📁 templates/                 # Skill 模板
│   ├── basic/                    # 基础模板
│   └── advanced/                 # 高级模板
│
├── 📁 scripts/                   # 工具脚本
│   ├── create-skill.sh           # 创建新 Skill
│   ├── validate-skill.sh         # 验证 Skill
│   ├── package-skill.sh          # 打包 Skill
│   └── install-examples.sh       # 安装示例
│
├── 📁 config/                    # 配置文件
│   └── skill-template.yaml       # Skill 模板配置
│
├── .github/                      # GitHub 配置
│   └── workflows/                # CI/CD 工作流
│       └── validate-skills.yml   # 验证 Skill
│
├── README.md                     # 项目说明（本文件）
├── LICENSE                       # 开源协议
├── CONTRIBUTING.md               # 贡献指南
└── CHANGELOG.md                  # 更新日志
```

---

## 💡 核心概念

### Skill 的组成部分

```
┌─────────────────────────────────────────────────────────┐
│                    Skill 架构图                          │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │              SKILL.md (必需)                     │   │
│  │  ┌───────────────────────────────────────────┐  │   │
│  │  │  YAML Frontmatter (元数据)                │  │   │
│  │  │  - name: skill-name                       │  │   │
│  │  │  - description: 描述                       │  │   │
│  │  └───────────────────────────────────────────┘  │   │
│  │  ┌───────────────────────────────────────────┐  │   │
│  │  │  Markdown Body (指令)                     │  │   │
│  │  │  - 使用说明                               │  │   │
│  │  │  - 脚本调用                               │  │   │
│  │  │  - 最佳实践                               │  │   │
│  │  └───────────────────────────────────────────┘  │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │           scripts/ (可选 - 脚本目录)            │   │
│  │  • 可执行脚本 (Python/Shell/etc.)               │   │
│  │  • 提供确定性操作                               │   │
│  │  • 避免重复代码                                 │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │         references/ (可选 - 参考文档)           │   │
│  │  • 领域知识                                     │   │
│  │  • API 文档                                     │   │
│  │  • 最佳实践                                     │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │          assets/ (可选 - 资源文件)              │   │
│  │  • 模板文件                                     │   │
│  │  • 图片/字体                                    │   │
│  │  • 配置文件                                     │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

### 渐进式加载机制

Skill 采用三层加载机制，优化上下文窗口使用：

```
┌─────────────────────────────────────────────────────────┐
│                    加载层级                              │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  第1层: 元数据 (始终加载)                               │
│  ├── name + description                                │
│  ├── 约 100 词                                         │
│  └── 用于判断是否触发 Skill                            │
│                                                         │
│  第2层: SKILL.md 正文 (触发后加载)                      │
│  ├── 详细使用说明                                      │
│  ├── 建议不超过 500 行                                 │
│  └── 核心工作流程                                      │
│                                                         │
│  第3层: 资源文件 (按需加载)                             │
│  ├── scripts/ - 可执行，无需加载                        │
│  ├── references/ - 需要时读取                          │
│  └── assets/ - 输出时使用                              │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## 🔒 安全规范

### 核心原则

1. **隐私优先** - 不上传任何用户数据
2. **最小权限** - 只请求必要的权限
3. **透明操作** - 明确告知用户将要执行的操作
4. **安全默认** - 默认配置应该是最安全的

### 安全检查清单

- [ ] 脚本不包含硬编码的密钥或凭据
- [ ] 不向外部服务器发送用户数据
- [ ] 文件操作限制在工作目录内
- [ ] 使用参数化输入，避免命令注入
- [ ] 敏感操作需要用户确认

详细规范请参考 [安全规范文档](docs/security-guidelines.md)。

---

## 🧪 测试与验证

### 本地测试

```bash
# 验证 Skill 格式
./scripts/validate-skill.sh examples/auto-save

# 本地安装测试
openclaw skill install ./examples/auto-save

# 运行测试
openclaw agent --message "保存测试文本到 test.txt"
```

### 自动化测试

```bash
# 运行所有测试
npm test

# 运行特定测试
npm test -- --grep "auto-save"
```

---

## 📦 发布到 ClawHub

### 准备工作

1. 注册 [ClawHub](https://clawhub.com) 账号
2. 获取 API Token
3. 配置本地环境

```bash
# 配置 ClawHub Token
openclaw config set clawhub.token YOUR_TOKEN
```

### 发布流程

```bash
# 1. 验证 Skill
./scripts/validate-skill.sh examples/auto-save

# 2. 打包 Skill
./scripts/package-skill.sh examples/auto-save

# 3. 发布
openclaw skill publish ./dist/auto-save.skill
```

详细流程请参考 [发布指南](docs/10-publishing.md)。

---

## 🤝 贡献指南

我们欢迎所有形式的贡献！

### 贡献方式

- 📝 改进文档
- 🐛 报告 Bug
- 💡 提出新功能建议
- 🔧 提交代码

### 开发流程

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 创建 Pull Request

详细指南请参考 [CONTRIBUTING.md](CONTRIBUTING.md)。

---

## 📄 开源协议

本项目采用 [Apache 2.0](LICENSE) 协议开源。

---

## 🙏 致谢

- [OpenClaw](https://github.com/openclaw/openclaw) - 强大的个人 AI 助手平台
- [ClawHub](https://clawhub.com) - Skill 市场
- 所有贡献者

---

## 📞 联系方式

- **GitHub Issues**: [提交问题](https://github.com/openclaw/openclaw-skill-developer-guide/issues)
- **Discord**: [加入社区](https://discord.gg/clawd)
- **文档**: [docs.openclaw.ai](https://docs.openclaw.ai)

---

<p align="center">
  Made with ❤️ by the OpenClaw Community
</p>

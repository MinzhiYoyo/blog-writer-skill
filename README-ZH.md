# Blog Writer Skill for OpenCode

一个用于撰写高质量技术博客文章的结构化技能，具备规范的工作流程、审查流程和专业格式。

## 功能特性

- **结构化工作流程**：收集需求 → 确认输入 → 生成方案 → 撰写内容
- **自动审查**：资深技术写作专家 AI 自动审查内容（最多5轮）
- **多部分支持**：将长篇博客分割成多个文件，采用规范命名
- **质量保证**：防止编造信息，确保一致性，保持专业标准
- **双语支持**：提供英文版和中文版

## 可用版本

| 版本 | 目录 | 说明 |
|------|------|------|
| 英文版 | `blog-writer-skill/` | 适用于英文能力较强的语言模型 |
| 中文版 | `blog-writer-zh-skill/` | 适用于中文能力较强的语言模型 |

## 安装步骤

### 第一步：克隆仓库

```bash
git clone https://github.com/MinzhiYoyo/blog-writer-skill.git
cd blog-writer-skill
```

### 第二步：选择版本

**询问您的语言模型更擅长哪种语言：**

```
你更擅长哪种语言：中文还是英文？
```

**根据回答选择：**

- **英文** → 安装 `blog-writer-skill/`（英文版）
- **中文** → 安装 `blog-writer-zh-skill/`（中文版）

> **注意**：只需安装一个版本。如果同时安装两个版本，技能可能无法正常工作。

### 第三步：复制到 OpenCode 技能目录

**安装英文版：**
```bash
cp -r blog-writer-skill ~/.config/opencode/skills/
```

**安装中文版：**
```bash
cp -r blog-writer-zh-skill ~/.config/opencode/skills/
```

### 第四步：验证安装

```bash
ls ~/.config/opencode/skills/
```

您应该能看到 `blog-writer-skill` 或 `blog-writer-zh-skill` 其中之一。

## 使用方法

安装后，当您提到以下内容时，技能会自动激活：

- "写博客"
- "博客文章"
- "技术文章"
- "教程"
- 或任何类似的表述

### 示例提示词

```
写一篇关于 Docker 容器化技术的博客文章，面向初学者
```

```
Write a blog post about React Hooks with practical examples
```

```
帮我创建一个 Python 异步编程的技术教程
```

## 工作流程

1. **收集需求**：技能会询问主题、读者、风格、长度和输出格式
2. **生成方案**：创建博客大纲并估算字数
3. **等待确认**：用户确认方案后才开始写作
4. **撰写内容**：按照方案生成博客文章
5. **自动审查**：资深技术写作专家 AI 审查并改进内容（最多5轮）
6. **输出文件**：保存最终的博客文章

## 配置选项

技能使用以下默认设置：

| 设置项 | 默认值 |
|--------|--------|
| 输出目录 | 当前目录 |
| 文件格式 | Markdown |
| 博客类型 | 技术博客 |
| 长度 | 完整版 |
| 风格 | 自动判断 |
| 多部分 | 单部分 |
| 审查 | 启用 |

## 仓库结构

```
blog-writer-skill/
├── blog-writer-skill/           # 英文版 skill
│   └── SKILL.md
└── blog-writer-zh-skill/       # 中文版 skill
    └── SKILL.md
```

## 系统要求

- 支持技能的 OpenCode
- 能够遵循结构化工作流程的代理
- 可用于内容生成和审查的 AI 模型

## 许可证

本项目采用 GNU 通用公共许可证 v3.0 - 详见 [LICENSE](https://github.com/MinzhiYoyo/blog-writer-skill/blob/main/LICENSE) 文件。

## 贡献

欢迎提交问题和功能增强请求！

# Blog Writer Skill for OpenCode

A structured skill for writing high-quality technical blog posts with proper workflow, review process, and professional formatting.

## Features

- **Structured Workflow**: Collect requirements → Confirm inputs → Generate plan → Write content
- **Auto-Review**: Senior Technical Writer AI reviews content automatically (up to 5 rounds)
- **Multi-Part Support**: Split long blogs into multiple files with proper naming
- **Quality Assurance**: Prevents hallucination, ensures consistency, maintains professional standards
- **Bilingual Support**: Available in English and Chinese versions

## Available Versions

| Version | Directory | Description |
|---------|-----------|-------------|
| English | `blog-writer-skill/` | English version for English language models |
| Chinese | `blog-writer-zh-skill/` | Chinese version for Chinese language models |

## Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/MinzhiYoyo/blog-writer-skill.git
cd blog-writer-skill
```

### Step 2: Choose Your Version

**Ask your language model which language it performs better in:**

```
Which language do you perform better in: English or Chinese?
```

**Based on the answer:**

- **English** → Install `blog-writer-skill/` (English version)
- **Chinese** → Install `blog-writer-zh-skill/` (Chinese version)

> **Note**: Only install ONE version. The skill will not work correctly if both versions are installed.

### Step 3: Copy to OpenCode Skills Directory

**For English version:**
```bash
cp -r blog-writer-skill ~/.config/opencode/skills/
```

**For Chinese version:**
```bash
cp -r blog-writer-zh-skill ~/.config/opencode/skills/
```

### Step 4: Verify Installation

```bash
ls ~/.config/opencode/skills/
```

You should see either `blog-writer-skill` or `blog-writer-zh-skill` in the list.

## Usage

Once installed, the skill will automatically activate when you mention:

- "Write a blog"
- "Blog post"
- "Technical article"
- "Tutorial"
- Any similar phrasing

### Example Prompts

```
Write a blog about Docker containerization for beginners
```

```
帮我写一篇关于 React Hooks 的技术教程
```

```
Create a technical blog post about Python async programming
```

## Workflow

1. **Collect Requirements**: The skill asks about topic, audience, style, length, and output format
2. **Generate Plan**: Creates a blog outline with word count estimate
3. **Wait for Approval**: User confirms the plan before writing begins
4. **Write Content**: Generates the blog post according to the plan
5. **Auto-Review**: Senior Technical Writer AI reviews and improves content (up to 5 rounds)
6. **Output Final File**: Saves the polished blog post

## Configuration

The skill uses these default settings:

| Setting | Default |
|---------|---------|
| Output directory | Current directory |
| File format | Markdown |
| Blog type | Technical blog |
| Length | Full version |
| Style | Auto-detect |
| Multi-part | Single part |
| Review | Enabled |

## Repository Structure

```
blog-writer-skill/
├── blog-writer-skill/           # English version skill
│   └── SKILL.md
└── blog-writer-zh-skill/       # Chinese version skill
    └── SKILL.md
```

## Requirements

- OpenCode with skill support
- Agent capable of following structured workflows
- Access to AI models for content generation and review

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](https://github.com/MinzhiYoyo/blog-writer-skill/blob/main/LICENSE) file for details.

## Contributing

Feel free to submit issues and enhancement requests!

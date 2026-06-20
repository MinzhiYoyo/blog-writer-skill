---
name: blog-writer
description: |
  Write high-quality technical blog posts with proper structure and professional formatting. Use this skill whenever the user mentions writing a blog, blog post, technical article, tutorial, or any form of technical documentation that should be published as a blog. This skill enforces a structured workflow: collect requirements → confirm inputs → generate outline → wait for approval → write content. It prevents hallucination, ensures consistency, and produces publication-ready markdown with proper headings, code blocks, tables, and diagrams.
---

# Blog Writing Skill

A structured approach to writing high-quality technical blog posts.

## Core Principles

### 1. Never Start Writing Immediately

You must NOT generate blog content directly. Always follow this sequence:

1. Collect user requirements
2. Output a blog writing plan
3. Wait for user confirmation

Only begin writing after receiving explicit approval signals like:
- "Start writing"
- "Go ahead"
- "Begin"
- "Start generating"

### 2. Never Fabricate Information

Do NOT invent:
- Data or statistics
- Research papers or citations
- Official documentation or APIs
- Configuration options
- Experimental results

If information cannot be verified:
1. Ask the user
2. Search reliable sources
3. Clearly state it cannot be confirmed

### 3. Proactively Identify Issues

If you detect:
- Insufficient information
- Ambiguity
- Incomplete descriptions
- Multiple valid interpretations

You must ask questions. Never guess or assume.

### 4. Maintain Consistency

The entire blog must maintain:
- Consistent naming
- Consistent terminology
- Consistent style
- Consistent context
- Consistent logic

No repetition, conflicts, or contradictions allowed.

## Execution Workflow

Follow this exact sequence. Never skip steps.

```
Collect Requirements
        ↓
Confirm User Inputs (including part count)
        ↓
Generate Blog Plan with Word Count Estimate
        ↓
Wait for User Approval
        ↓
Begin Writing
        ↓
Auto-Review (Senior Engineer Review, up to 5 rounds)
        ↓
Output Final File
```

## User Input Requirements

Before writing, confirm these details:

### Output Location (Default: Current Directory)

Confirm:
- Save directory
- File name
- File format

Defaults:
- Current directory
- Markdown
- Auto-generate filename from title

### Target Audience (Default: Technical Blog Readers)

Confirm:
- User group
- Prerequisites
- Reading level

### Writing Style (Default: Auto-detect from Topic)

Supported styles:
- Technical tutorial
- Concept explanation
- Practical experience
- Blog post
- Popular science
- Best practices

### Article Length (Default: Full Version)

Options:
- Brief
- Standard
- Full (default)

### Multi-Part Structure (Default: Single Part)

When the topic is complex or lengthy, the blog can be split into multiple parts.

**Process:**
1. Estimate total word count based on the topic scope
2. Present word count estimate to the user
3. Ask if they want to split into multiple parts
4. If splitting, confirm the number of parts and naming convention

**Common split strategies:**
- By depth: Part 1 (Basics), Part 2 (Advanced), Part 3 (Expert)
- By sections: Each major section becomes a separate file
- By length: Upper/Middle/Lower (3 parts)

**File naming for multi-part blogs:**
- Base filename + part suffix: `blog-title-part-1.md`, `blog-title-part-2.md`
- Or descriptive: `blog-title-basics.md`, `blog-title-advanced.md`

**Default:** Single part (no splitting)

## Content Requirements

### Breadth

Cover multiple dimensions, keep it as comprehensive as possible, and need to confirm with the user whether the breadth is sufficient.
### Depth

Each section should expand layer by layer，such as:

```
Concept
    ↓
Principle
    ↓
Implementation
    ↓
Application
    ↓
Practical Experience
```

### Objectivity

When making recommendations or evaluations, state:
"Personal opinion, for reference only."

## Formatting Requirements

### Headings

- H1: Blog title, chapter title
- H2: Section title
- H3: Subsection title
- H4+: Not allowed

### Information Density

Prefer:
- Tables
- Lists
- Blockquotes
- Mermaid diagrams
- ASCII diagrams

### Lists

Use multi-level lists for complex content.

### Tables

If column names don't convey full meaning, add a "Remark" column.

### Comparisons

Use comparison tables when evaluating multiple options.

### Preface

Before the main content, add a preface using H1 that includes:
- Target audience
- Prerequisites
- Reading benefits

### Disclaimer

Add this disclaimer in bold-italic under Blog Title:`Parts of this article were generated with AI assistance. The author has carefully reviewed it, but any oversights are welcome to be pointed out. If you mind, please do not read.`

### Formulas

Explain formulas and symbols when they first appear.

### Code

All code must include:
- Comments
- Parameter explanations
- Input/output descriptions
- Usage scenarios

## Quality Requirements

Prioritize:
- **Correctness**: Accurate information
- **Completeness**: Cover all necessary aspects
- **Consistency**: No contradictions
- **Readability**: Clear and engaging

Never reduce quality to shorten length.

## Review Process

After writing is complete, the review phase begins automatically without user confirmation.

### Review Agent Role

The review is performed by an independent AI agent acting as a **Senior Technical Writer** with:
- 10+ years of writing experience
- Deep expertise in the blog's subject matter
- Strong editorial and quality standards

### Review Criteria

The reviewer evaluates:

**Content Quality:**
- Technical accuracy and correctness
- Completeness of coverage
- Logical flow and coherence
- Depth of explanation

**Writing Quality:**
- Clarity and readability
- Consistent terminology
- Proper grammar and style
- Engaging narrative

**Structure & Format:**
- Proper heading hierarchy
- Effective use of visuals (tables, diagrams)
- Code example quality
- Citation accuracy

**Professional Standards:**
- Audience-appropriate language
- Balanced perspective and objectivity
- Actionable takeaways
- Appropriate length

### Review Output

The reviewer provides:
1. **Overall Assessment**: Pass/Needs Revision with summary
2. **Section-by-Section Feedback**: Specific issues per section
3. **Suggested Improvements**: Concrete recommendations
4. **Quality Score**: 1-10 rating with justification

### Review Workflow

```
Blog Written
      ↓
Auto-trigger Review Agent (Senior Technical Writer)
      ↓
Review Agent Analyzes Content
      ↓
Generate Review Report
      ↓
Evaluate if Revisions Needed
      ↓
[If revisions needed] Apply Changes → Re-review (up to 5 rounds)
      ↓
[No revisions needed OR 5 rounds reached] Output Final File
```

### Review Iteration Rules

- Review executes automatically without user intervention
- After each review, if changes are needed, apply them and re-review
- Maximum 5 review rounds, then force output current version
- All issues found during review must be documented in the review report

### Review Agent Invocation

When spawning the review agent, use this prompt structure:

```
You are a Senior Technical Writer reviewing a technical blog post.

Your role:
- Act as an experienced editor with deep domain expertise
- Evaluate content against professional technical writing standards
- Provide constructive, specific feedback
- Focus on clarity, accuracy, and reader value

Review the following blog and provide:
1. Overall assessment (Pass/Needs Revision)
2. Section-by-section feedback
3. Specific improvement suggestions
4. Quality score (1-10) with justification

Be thorough but constructive. The goal is to ensure the blog meets publication standards.
```

## Error Handling

When encountering:
- Insufficient information
- Content conflicts
- Unverifiable claims

Priority order:
1. Ask the user
2. Search online
3. Clearly state it cannot be confirmed

Never fabricate.

## Default Behaviors

| Item | Default |
|------|---------|
| Output directory | Current directory |
| File format | Markdown |
| Filename | Auto-generated |
| Blog type | Technical blog |
| Length | Full version |
| Style | Auto-detect |
| Multi-part | Single part |
| Review | Enabled |

## Output Format

### Single Part Blog

Generate the blog as a single Markdown file with proper structure:

```markdown
# [Title]

***Parts of this article were generated with AI assistance. The author has carefully reviewed it, but any oversights are welcome to be pointed out. If you mind, please do not read.***

# Preface

[Target audience, prerequisites, reading benefits]

# [Chapter 1]

## [Section 1.1]

### [Subsection 1.1.1]

[Content with proper formatting: tables, lists, code blocks, diagrams]

# [Chapter 2]

...

# Summary and Outlook

## Article Summary

[Key takeaways]

## Further Reading

[References and resources]

# References

[All links and citations used in this article]
```

### Multi-Part Blog

When the blog is split into multiple parts, generate separate files:

**File Structure:**
```
blog-title/
├── blog-title-part-1.md
├── blog-title-part-2.md
├── blog-title-part-3.md
└── README.md (optional: index with links to all parts)
```

**Each Part File:**
```markdown
# [Title] - Part [N]: [Part Title]

# Preface

[Target audience, prerequisites, reading benefits]

**"Parts of this article were generated with AI assistance. The author has carefully reviewed it, but any oversights are welcome to be pointed out."**

[Part-specific content]

## Navigation

- Previous: [Link to Part N-1] (if applicable)
- Next: [Link to Part N+1] (if applicable)
- [Back to Index](README.md) (if README exists)
```

**README.md (Optional Index):**
```markdown
# [Title]

[Brief description of the entire series]

## Parts

1. [Part 1: Title](blog-title-part-1.md) - [Brief description]
2. [Part 2: Title](blog-title-part-2.md) - [Brief description]
3. [Part 3: Title](blog-title-part-3.md) - [Brief description]
```

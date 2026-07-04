---
name: jd-resume-reverse-engineer
description: Reverse-engineer job descriptions into resume screening logic, ATS keyword libraries, evidence requirements, and module-by-module resume rewrite guidance. Use when the user provides a JD, role description, recruiter notes, screenshots of job requirements, or asks to infer hiring criteria, resume keywords, interview evaluation points, or how to tailor a resume for a specific role.
---

# JD Resume Reverse Engineer

## Overview

Convert a job description into a practical resume-targeting artifact: what the company is likely screening for, which keywords matter, what proof the resume must show, and how each resume section should be rewritten.

Do not merely summarize the JD. Infer the hidden evaluation model behind it.

## Workflow

1. **Extract role context**
   - Identify company, team, role title, seniority, product domain, user type, and business stage.
   - Separate explicit requirements from implied requirements.
   - If screenshots are provided, read visible text and combine it with pasted text.

2. **Build the screening model**
   - Infer hard filters: years, education, domain, tools, language, location, role ownership.
   - Infer ATS keyword filters: product nouns, technical nouns, methodology nouns, metrics, tools.
   - Infer human evaluation criteria: ownership, taste, judgment, ambiguity handling, cross-functional influence, user empathy.
   - Infer interview focus: what stories, tradeoffs, metrics, and failures they will likely ask about.

3. **Create a keyword library**
   - Group keywords by screening dimension, not alphabetically.
   - Mark priority as `S / A / B`:
     - `S`: must appear if truthful.
     - `A`: useful differentiator.
     - `B`: supporting detail or technical color.
   - Include bilingual variants when the JD mixes Chinese and English.
   - Prefer exact JD wording for ATS-sensitive phrases.

4. **Map keywords to resume modules**
   - For each resume section, specify which keywords belong there.
   - Recommended modules:
     - Profile / Summary
     - Core Skills / Keywords
     - Work Experience
     - Projects
     - Tools / Technical Fluency
     - Education
   - For each major work experience, state the target positioning, evidence to show, and example bullet patterns.

5. **Detect evidence gaps**
   - Identify requirements not yet supported by the user's resume or known history.
   - Separate:
     - `Can claim if true`: likely experience that needs clearer wording.
     - `Need evidence`: requires metrics, examples, artifacts, or scope.
     - `Do not fake`: high-risk claims that should not be invented.

6. **Write actionable output**
   - Use concrete resume phrasing, not generic advice.
   - Avoid vague words like "responsible for product work" unless paired with product object, user, action, and metric.
   - Preserve truthfulness: optimize wording, do not fabricate experience.

## Output Format

Use the template in [references/output-template.md](references/output-template.md) when the user asks for a Markdown artifact, keyword library, or reusable analysis.

If the user wants a quick answer, compress the same structure into:

1. Screening logic
2. S-level keywords
3. Resume modules to strengthen
4. Example rewrite bullets
5. Missing evidence

## Keyword Extraction Rules

Prioritize terms in this order:

1. Repeated phrases in the JD.
2. Phrases in headings such as requirements, responsibilities, bonus points, qualifications.
3. Product category nouns: `Agent`, `Skill Market`, `open platform`, `knowledge base`.
4. Technical mechanism nouns: `Tool Use`, `MCP`, `API`, `LLM`, `workflow`, `RAG`.
5. Evaluation verbs: `plan`, `define`, `measure`, `iterate`, `collaborate`, `launch`, `optimize`.
6. Metrics: `retention`, `conversion`, `task completion`, `activation`, `A/B test`, `funnel`.
7. Stakeholders: `researchers`, `engineers`, `developers`, `operations`, `community`, `enterprise users`.

## Resume Bullet Pattern

For recommended resume bullets, use this pattern:

`Role ownership + product object + user/problem + product action + measurable or observable outcome`

Examples:

- `负责 Skill Market 平台与后台管理，覆盖技能上架、审核、分类、权限与版本管理，支撑开发者供给、运营治理和团队级使用。`
- `基于转写完成率、内容消费与留存漏斗确定 Roadmap 优先级，联合算法团队优化专业词汇召回、声纹切分与跨语种对齐指标。`
- `将 Agent Template 设计为承载智能工作流的容器，降低用户从任务意图到可执行工作流的使用门槛。`

## Quality Bar

A good analysis should make the user able to answer:

- What will this JD screen out first?
- Which exact words should appear in my resume?
- Where should each keyword appear?
- What experiences should I emphasize or downplay?
- What proof do I need before claiming a match?
- What interview questions are likely to follow from these requirements?

Do not over-index on ATS at the cost of readability. The final resume should still read like a coherent career story.

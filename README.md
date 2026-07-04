# JD Resume Reverse Engineer

Turn any job description into resume screening logic, ATS keywords, resume rewrite strategy, and interview signals.

This is a Codex Skill for candidates, career coaches, recruiters, and AI agents who need to understand what a role is really screening for.

## What It Does

Given a JD, recruiter note, or job screenshot, this skill reverse-engineers:

- Hidden screening logic behind the role
- ATS keyword library with `S / A / B` priority
- Resume module strategy for Profile, Skills, Experience, Projects, and Tools
- Evidence gaps: what can be claimed, what needs proof, and what should not be faked
- Likely interview probes based on the JD

It is especially useful for roles involving:

- AI Product Manager
- Agent Product Manager
- Developer Platform PM
- Growth PM
- UX / Product Design
- Technical PM
- Open platform / ecosystem / marketplace roles

## Why This Exists

Most resume optimization advice stops at "add keywords."

That is not enough.

A strong resume needs to show the hiring team:

1. You match the explicit JD requirements.
2. You understand the hidden evaluation criteria.
3. You can prove the right experience with concrete product objects, actions, metrics, and tradeoffs.

This skill helps Codex infer that evaluation model and turn it into a practical resume plan.

## Example Prompt

```text
Use $jd-resume-reverse-engineer to analyze this JD and produce:
1. screening logic
2. ATS keyword library
3. resume module strategy
4. evidence gaps
5. likely interview probes
```

You can paste a full JD, recruiter message, or screenshots of job requirements.

## Output Structure

The skill produces a Markdown report with:

- Role snapshot
- Inferred screening mechanism
- S / A / B keyword library
- Resume module strategy
- Evidence gap checklist
- Likely interview probes
- Final resume storyline

See [examples/deepseek-agent-pm.md](examples/deepseek-agent-pm.md) for a concrete example.

## Install

Copy this folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/qike7777/jd-resume-reverse-engineer.git ~/.codex/skills/jd-resume-reverse-engineer
```

Then invoke it in Codex:

```text
Use $jd-resume-reverse-engineer to reverse-engineer this JD for my resume.
```

## Repository Structure

```text
jd-resume-reverse-engineer/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   └── output-template.md
└── examples/
    └── deepseek-agent-pm.md
```

## Best For

- Tailoring a resume to a specific JD
- Extracting ATS keywords without keyword stuffing
- Turning vague experience into role-aligned resume bullets
- Preparing for interviews from a JD
- Building AI-agent workflows for career coaching

## Design Principle

Do not fabricate experience.

Optimize signal, structure, and evidence. The best resume reads like a coherent career story, not a bag of keywords.

---
name: interview-review-coach
description: Use when reviewing product manager or AI/education product interviews from transcripts, resumes, JDs, meeting notes, or post-interview self-reflections; especially when the user wants structured debriefs, weakness tracking, follow-up drills, next-round prep, or cross-interview memory updates.
---

# Interview Review Coach

Use this skill to produce a reusable, evidence-grounded interview debrief for product manager interviews.

## Core Assumptions

- The goal is not a generic summary. Produce a diagnosis, repair plan, drills, and next-round preparation.
- Keep state issues separate from capability issues. Lateness, wrong meeting room, nervousness, or poor condition are repairable context, not proof of weak ability.
- Do not invent missing JD, resume, or transcript facts. Mark gaps clearly and continue with available evidence when useful.
- If the current directory is a broad parent folder with many interview folders, do not scan everything as one interview. Select the user-mentioned company/folder, infer the most relevant single subfolder, or ask a brief clarification.

## Scope And Role Adaptation

This skill is intentionally scoped to product manager interviews, especially AI product and education product roles. For another company or another PM role, keep the skill unchanged and replace only the resume, JD, and interview transcript.

When adapting this skill to a non-PM role, keep the file-reading, evidence extraction, debrief, drill, and memory workflow, but replace the role-specific capability model in `references/interview-review-v2.md`:

- question categories: replace product strategy, data metrics, solution design, technical-link understanding, and project review with the target role's interview dimensions
- scoring table: replace PM dimensions with the target role's must-have competencies
- answer frameworks: replace P-T-S-D, STAR, or PM-specific framing only when the target role needs different evidence structures
- simulated follow-ups: generate pressure questions from the target JD and role seniority, not from PM defaults
- memory taxonomy: track recurring weaknesses using the target role's competency language

## Files To Use

In the skill folder:

- `references/interview-review-v2.md`: canonical report schema and interaction protocol. Read it before generating a full debrief or drill flow.
- `memory/MEMORY.md`: cross-interview memory for candidate profile, recurring weaknesses, practice history, and interview outcomes.

For an interview task, also read task-local materials:

- Interview transcript or meeting notes: `.txt`, `.md`, `.docx`, PDF text exports, or Feishu/Miaojiji transcripts.
- Resume: `.pdf`, `.docx`, `.txt`, or pasted resume text.
- JD: text, `.md`, `.txt`, `.docx`, PDF, or image screenshot when image reading/OCR is available.

## Workflow

1. Read `memory/MEMORY.md` if it exists and use it as prior context, not as current evidence.
2. Identify the interview folder and classify files as transcript, resume, JD, prior report, or supporting material.
3. Tell the user the inferred file roles briefly, then continue unless the mapping is genuinely ambiguous or risky.
4. Extract candidate background from the resume and role requirements from the JD.
5. Compare interview answers against JD demands and resume claims.
6. Generate the report using the module order and output requirements in `references/interview-review-v2.md`.
7. Stop before module seven unless the user has completed at least one drill and says `开始补课总结`, `我准备好了`, or an equivalent trigger.
8. After a full debrief, update `memory/MEMORY.md` with only durable learnings:
   - candidate profile changes
   - interview record: company, role, date if known, round/type, overall rating, core improvement point
   - weakness tracking: new, repeated, improved, or unresolved

## Output Rules

- Default to Chinese for interview debriefs, drills, memory updates, and follow-up prep unless the user explicitly asks for another language.
- Lead with the interview judgment and highest-priority repair point, then provide the structured report.
- Preserve direct evidence: quote or paraphrase the candidate's actual answer before criticizing it.
- Give speakable replacements, not just abstract advice.
- For drills, ask realistic interview questions and wait for the user's answer. Do not attach the model answer immediately.
- In Socratic drill feedback, identify only the most important issue per turn, then ask a pressure follow-up.
- For AI product interviews, explicitly separate PM ownership from algorithm/engineering ownership: quality bar, bad-case taxonomy, fallback strategy, user experience standard, and launch criteria belong in PM framing.
- For education product interviews, check whether the candidate explained the user problem, learning scenario, form factor, evaluation boundary, and measurable effect.

## Common Failure Modes

- Treating all files in a parent directory as one interview. Use one interview folder at a time.
- Repeating the full v2 template inside this file. Keep `SKILL.md` as the routing and execution layer; keep the detailed report schema in `references/interview-review-v2.md`.
- Collapsing nervous performance into ability failure. Separate state, expression, and capability.
- Giving polished reference answers before the user practices. Drills should force the user to answer first.
- Updating memory with one-off details. Store only reusable patterns and stable candidate facts.

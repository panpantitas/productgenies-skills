---
name: nielsen-heuristic-audit
description: Audit a UI (screenshot, Figma frame, flow description, or live page) against Jakob Nielsen's 10 usability heuristics and produce a prioritized report with severity ratings. Use when the user asks for a UX review, heuristic evaluation, UI audit, or "is this good UX?" on a screen or flow.
---

# Nielsen Heuristic Audit

You act as a heuristic evaluator, the same role Nielsen and Molich designed the method for: inspect an interface against ten broad usability principles, list every violation you can find, and rate how serious each one is.

This is a first-pass inspection. It predicts problems; it does not measure them. It supports user testing and never replaces it.

## Language

Write the report in the language the user writes in. If the user writes Thai, report in Thai and keep the heuristic names in English in parentheses, e.g. การมองเห็นสถานะของระบบ (Visibility of system status).

## Inputs

Accept any of: screenshots, exported frames, a Figma link, a flow described in text, or a URL.

Before auditing, confirm three things from the input or by asking one short question if missing:
1. Who the users are and what they are trying to do.
2. Which screen or flow is in scope.
3. Platform (mobile, web, desktop, voice, AI chat).

If the user gives no context, state your assumptions at the top of the report and continue.

## The 10 heuristics

Check the interface against each one separately.

1. **Visibility of system status.** The interface keeps users informed about what is happening through timely feedback (loading, progress, confirmation, "you are here").
2. **Match between system and the real world.** Language, icons, and order follow what users already know, not internal jargon.
3. **User control and freedom.** Users can back out of mistakes easily: undo, redo, cancel, clearly marked exits.
4. **Consistency and standards.** The same words and actions mean the same thing everywhere (internal consistency), and the design follows platform and industry conventions (external consistency).
5. **Error prevention.** The design removes error-prone conditions or asks for confirmation before costly actions. Use constraints and good defaults.
6. **Recognition rather than recall.** Options, labels, and actions are visible or easy to retrieve, so users do not have to remember information across screens.
7. **Flexibility and efficiency of use.** Shortcuts and personalization help experts without getting in the way of novices.
8. **Aesthetic and minimalist design.** No irrelevant or rarely needed information competing with what matters. This is about focus, not about flat design.
9. **Help users recognize, diagnose, and recover from errors.** Error messages use plain language, state the problem precisely, and suggest a fix.
10. **Help and documentation.** Ideally unnecessary. When needed, it is searchable, task-focused, concise, and available in context.

## Process

1. **First pass:** go through the interface once to understand the flow and scope.
2. **Second pass:** go through it again, element by element, and check each against all ten heuristics.
3. **Record each violation** with: where it is, which heuristic it breaks, what you observed, and why it hurts users.
4. **Rate severity** for each finding (scale below).
5. **Recommend a fix** that is specific and actionable, not "improve clarity."
6. **Note what you could not judge** (see Limits).

Work from evidence. Quote the label, describe the element, or point to the screen. Never invent a problem to fill a heuristic, and never claim a screen contains something you cannot see. If a heuristic has no issues, say "no issues found" and mention one thing that works well.

## Severity scale (Nielsen)

Rate each finding from 0 to 4, using impact on users, how often it occurs, and how hard it is to work around:

- **0:** not a usability problem.
- **1:** cosmetic only. Fix if time allows.
- **2:** minor problem. Low priority.
- **3:** major problem. High priority to fix.
- **4:** usability catastrophe. Fix before release.

A problem that blocks a core task, affects many users, or risks money or data deserves a higher rating than a rare annoyance.

## Report format

Use exactly this structure:

**1. Scope and assumptions** — users, task, platform, what was reviewed.

**2. Summary** — two or three sentences: overall impression and the top issues.

**3. Findings table**

| # | Heuristic | Location | Observation | Severity (0-4) | Recommendation |
|---|-----------|----------|-------------|----------------|----------------|

Sort by severity, highest first.

**4. What works well** — two or three things, each tied to a heuristic.

**5. Heuristic scorecard** — for each of the 10: number of findings and the highest severity.

**6. Limits and next steps** — what could not be judged from the material provided, and which findings should be validated with real users.

## Limits to state honestly

- A single evaluator typically finds only a portion of the problems (Nielsen's research suggests roughly a third), because different evaluators find different problems. Say so, and recommend a second reviewer or user testing for important flows.
- Static screenshots cannot show animation, response time, hover states, or error states that were not captured. List what is missing.
- Heuristics can conflict (for example minimalism versus showing more information). When they do, explain the trade-off instead of picking silently.
- Heuristics are rules of thumb, not guaranteed laws. Findings are predictions.

## Optional: AI products

If the interface is an AI assistant, chatbot, or generative tool, also check these extensions of the classic heuristics:

- **Control (3):** can users stop generation, undo AI actions, edit outputs, and override suggestions? Does the AI ask before irreversible actions?
- **Consistency (4):** does the AI behave and respond in a consistent style to similar requests?
- **Error prevention (5):** does the design help catch mistakes in what the AI produces, not only in what the user does?
- **Visibility (1):** does the user know what the AI is doing, what sources or data it uses, and what it cannot do?

These extensions come from early-stage design commentary, not from an established standard. Present them as suggestions.

## Attribution

Heuristics by Jakob Nielsen, derived in 1994 from a factor analysis of 249 usability problems. Credit: Nielsen Norman Group, "10 Usability Heuristics for User Interface Design", https://www.nngroup.com/articles/ten-usability-heuristics/

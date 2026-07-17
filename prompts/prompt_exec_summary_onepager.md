# Executive Summary One-Pager Prompt

Create a concise executive summary for program leadership using only the facts provided in the input.

## Audience

- Directors
- Senior Directors
- VPs

## Purpose

Provide a fast, high-level status update that explains:
- where the program stands now
- what has already been decided
- which risks, issues, and open points matter most in the next 14 days
- what action is being taken and who owns it

## Writing Style

- Keep it concise and executive-friendly
- Use plain language
- Focus on business and delivery relevance, not engineering detail
- Avoid long background explanations
- Do not repeat the same point across sections
- Do not invent facts, dates, owners, or commitments
- If a fact is uncertain or unconfirmed, either omit it or describe it as not yet confirmed

## Input Contract

Use the following inputs when available:
- Reporting date
- Current program status
- Major accomplishments or alignment reached
- Key decisions made
- Top open points
- Top risks
- Current issues
- Actions underway
- Owners for each action
- Optional due dates only if confirmed

## Output Structure

Produce exactly this structure in Markdown:

# Executive Summary - [Program Name] ([Reporting Date])

## Current Status
- 3 to 5 bullets only
- Summarize the current state of execution
- Explain what is true now and what is still not stable or confirmed
- Keep each bullet short and direct

## Decisions Made
- 3 to 5 bullets only
- Include only decisions already made
- Do not include proposed next steps here

## 14-Day Plan
- Create a Markdown table with these columns only:
  - Topic
  - Action
  - Owner
- Merge risks, issues, and open points into this single table
- Each row should state:
  - the topic or concern
  - the action being taken
  - the owner of that action
- Include only the most important items for executive attention
- Default to 5 to 7 rows maximum
- Do not include a due date column unless explicitly requested

## Content Rules

- Prefer the most important execution concerns over a complete inventory
- Focus on delivery confidence, dependency readiness, scope clarity, customer impact, and schedule confidence
- Keep the summary to one page equivalent
- If dates are not confirmed, do not present them as commitments
- If ownership is unclear, state "Owner to be confirmed"

## Quality Check Before Finalizing

Verify that:
- the Current Status section is concise and fact-based
- the Decisions Made section contains only completed decisions
- the 14-Day Plan table merges risks, issues, and open points cleanly
- the table actions are specific enough to be useful
- no unconfirmed dates are shown as fact
- no technical detail is included unless it affects delivery or commitments

## Final Instruction

Generate the executive summary now using the provided input and this exact format.
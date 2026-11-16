# Research notes and candidate queue

Updated: 2026-11-17

## 2026-11-17 — Starter-kit selection and format

- OpenAI's official [Skills guide](https://openai.com/academy/skills/) describes skills as repeatable workflows with a clear job, inputs, outputs, and guardrails. It recommends small building blocks and splitting unrelated work instead of making one oversized skill.
- OpenAI's [API skills documentation](https://developers.openai.com/api/docs/guides/tools-skills) says skills use a `SKILL.md` manifest with front matter and instructions and are compatible with the open Agent Skills standard. Product-specific installation still varies, so this repo does not claim automatic installation across every assistant.
- Based on those design principles, the first starter kit covers distinct common jobs: triaging messages, preparing/following up meetings, comparing choices, planning a week, drafting replies, shopping research, truthful job applications, safe troubleshooting, learning, and trip planning. This selection is a usefulness hypothesis, not a measured ranking or proof of demand.
- Every workflow is designed to produce a reviewable draft or plan. It must not imply that it sent, booked, purchased, applied, edited, or otherwise changed anything unless a user explicitly authorizes a connected tool action.
- **Decision:** Publish the starter kit as practical drafts, clearly label demand as unvalidated, and gather user feedback before claiming any individual skill is proven or adding features for popularity alone.

## 2026-11-17 — First evidence check

- A [Reddit post in r/Students](https://www.reddit.com/r/Students/comments/1r5f5go/found_tool_that_explains_confusing_letters_bank/) describes a newly built tool for explaining confusing letters, listing deadlines, and surfacing next steps. One commenter mentions confusion with research-approval documents. The author is promoting their own tool, so this is a useful problem signal but not independent product validation.
- A [community proposal](https://community.openai.com/t/product-development-proposal-for-openai/1411012) gives examples such as understanding a bank letter and renewing an identity document, but it is one proposal, not measured demand.
- Existing alternatives are strong: [Microsoft OneDrive Copilot](https://support.microsoft.com/en-us/onedrive/review-pdfs-using-copilot-context-menu-and-ai-actions) can explain selected PDF text in plain language, while [Gemini in Drive](https://support.google.com/drive/answer/16686465?hl=en-GR) can summarize files and answer questions about them. This makes a generic document-summary skill a weak differentiator.
- **Decision:** Keep `document-to-next-steps` as a draft only. A potential gap may be a source-grounded, “what must I do / by when / what is unclear?” checklist across assistants, but we have not established that users need this beyond current product features. Seek more independent reports and test whether precise source references, accessibility, or cross-platform portability address a real unmet need.

## Initial direction

**Hypothesis:** Many people have documents that contain instructions but are hard to act on. A small AI skill can help turn them into a clear checklist without pretending to replace a professional.

This is a starting hypothesis, not evidence of broad demand. Daily research should seek repeated, specific user problems and look for counter-evidence before expanding the collection.

## Format and quality evidence

- The [Open Agent Skills specification](https://openagentskills.dev/docs/specification) defines a skill as a folder with a `SKILL.md` file, required `name` and `description` fields, and optional supporting references/scripts. It recommends keeping the main instructions concise and validating the format.
- [OpenAI's Skills documentation](https://developers.openai.com/api/docs/guides/tools-skills) describes skills as reusable instructions plus supporting files and says they are compatible with the open Agent Skills standard. Product-specific installation still needs to be checked before being documented.
- A 2026 study, [After the Party: Governing What a Viral Agent-Skill Ecosystem Left Behind](https://arxiv.org/abs/2609.17274), reports that popularity signals were not reliable quality measures in its study window and that the skills ecosystem carried meaningful privilege/security risks. This is a reason to prioritize review, transparent limitations, and safe-by-default instructions—not to chase stars alone.
- A third-party leaderboard currently shows many large skill repositories centered on software development, design, and security. Treat its counts/rankings as a changing snapshot, not verified demand or proof that another broad bundle will succeed: [Skill Leaderboard](https://www.skillleaderboard.com/).

## First candidate: document to next steps

**User problem hypothesis:** A person receives a long or unfamiliar document and cannot quickly tell what it asks them to do.

**Proposed result:** A short plain-language summary; action checklist; dates copied exactly from the source; unfamiliar terms explained; unclear/missing information called out; and page/heading references where available.

**Guardrails:** Never invent a deadline or obligation, silently omit uncertainty, make a legal/medical/financial decision, or send the document to a service. The skill should work on user-provided text/files only and remind users to verify important details against the original.

**Evidence still needed:** Find independent examples across different kinds of users/documents; identify a specific gap beyond existing document assistants; test with representative sample documents; record failures and revise. Do not describe the problem as validated until that work is complete.

## Candidate status

| Candidate | Evidence | Next check | Decision |
|---|---|---|---|
| Document to next steps | One user-stated direction plus general product hypothesis; no independent demand sample yet | Search public discussions for repeated document-comprehension/actionability problems and review existing solutions | Keep as an early draft; do not claim market validation |

## Recurring research record

For every research pass, record the date, direct source links, the specific user problem, whether it is a repeat signal or a single anecdote, existing alternatives, what would disprove the idea, and the decision (keep, combine, split, revise, or discard). Do not copy source text beyond short attributed excerpts; write original instructions.

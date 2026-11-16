---
name: troubleshoot-step-by-step
description: Diagnose a technical or practical problem by understanding the setup, checking evidence, and changing one low-risk thing at a time. Use when something is broken and the user wants safe, trackable troubleshooting.
---

# Troubleshoot without making things worse

1. Restate the symptom and desired result. Ask for the exact error, when it began, what changed, and what has already been tried; do not ask the user to repeat details already provided.
2. Sketch the relevant setup and dependencies before proposing fixes. Separate observed facts from likely causes.
3. Check the safest, most informative evidence first: status screens, logs, configuration names, or a read-only reproduction. Protect passwords, tokens, and personal data in any output.
4. Rank likely causes and propose one meaningful change at a time. Explain why it helps and how to undo it.
5. Before any destructive, irreversible, security-sensitive, or externally visible change, explain the effect and ask for explicit approval. Recommend a backup before edits that could lose data.
6. After each approved change, check whether the symptom changed and record the result. If it did not, revert when safe before trying another variable.
7. Stop when evidence points to a service owner, hardware fault, or high-risk repair beyond the available access. Give the evidence and the next safe escalation.

## Output

Summarize the setup, verified findings, likely causes, steps already tried, next safe step, and rollback. Never say something was fixed unless a check confirms it.

## Example request

“My printer stopped connecting after I changed Wi-Fi routers. Help me check it one step at a time. Don’t reset it or change network settings without explaining what will be lost.”

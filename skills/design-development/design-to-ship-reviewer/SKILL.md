---
name: design-to-ship-reviewer
description: Turn a product brief or UI reference into a coherent interface, implement a focused improvement, and review the rendered result. Use for web-app design, frontend polish, or design QA when a coding agent and browser preview are available.
---

# Design to ship reviewer

Help the user move from a product goal to a polished, usable interface and a reviewable result. Make the design intentional, fit the existing product, and verify the rendered experience instead of relying on source code alone.

## Before changing the interface

1. Identify the target user, the task they need to complete, the screen or flow in scope, and any supplied reference, brand, or acceptance criteria. If a detail is missing, make a small visible assumption rather than inventing product requirements.
2. Inspect the existing project before editing: framework, routes, shared components, design tokens, assets, responsive patterns, and current run or preview instructions. Preserve working conventions unless the brief calls for a change.
3. State a concise design direction tied to the product and audience. Prefer one clear visual idea, a small type and color system, useful hierarchy, and purposeful spacing over generic gradients, decorative cards, or unrequested redesign.
4. Identify the key interaction and its important states: at minimum the normal state plus relevant loading, empty, error, disabled, focus, or success states. Include only states that the chosen flow actually needs.

## Design and implementation

1. Keep the change focused on the user's requested outcome. Reuse existing components and tokens where they fit; add or adjust a component only when it improves consistency or clarity.
2. Make the primary action, content hierarchy, and next step easy to understand. Use labels people recognize, readable text, visible focus, adequate contrast, and controls that work with keyboard and touch.
3. Make the layout adapt to narrow and wide screens. Avoid horizontal overflow, tiny tap targets, clipped content, and controls hidden behind hover-only behavior.
4. Use supplied images, copy, and brand assets faithfully. Do not invent testimonials, product claims, customer logos, or data. Use a clearly identified placeholder only when an asset is missing and a placeholder is useful.
5. Keep motion purposeful and restrained. Respect reduced-motion preferences when adding nonessential animation.

## Review the rendered result

1. Run the project using its documented or existing preview workflow when available. Open the actual changed route in a browser; source inspection alone is not visual verification.
2. Inspect at least one narrow/mobile viewport and one desktop viewport. If a reference image or Figma frame was provided, use a comparable viewport and check the major layout, typography, spacing, color, and content differences.
3. Exercise the key interaction, keyboard focus path, and relevant states. Check for obvious layout overflow, missing assets, console errors, and failed requests when browser tools expose them.
4. Fix the highest-impact issues found, then revisit the affected view. Do not claim a check was performed if the required preview, reference, or tool was unavailable.
5. When a coding or browser tool is unavailable, finish the useful review that can be done from the supplied evidence and list the unverified items explicitly.

## Deliver the handoff

Summarize:

- **Goal and design direction:** what was improved and why it suits the user and product.
- **Changes:** the important screens, components, or states changed.
- **Checks performed:** viewports, interaction, keyboard/accessibility basics, and visible errors actually checked.
- **Remaining gaps:** decisions or visual comparisons that could not be verified.
- **Evidence:** provide screenshots or preview links when the environment makes them available.

Keep the handoff short and factual. Never call a screen “pixel-perfect,” “fully accessible,” or “production-ready” unless the evidence supports that exact claim.

## Example request

“Review this small-business dashboard against the attached brief. Improve the main screen using its existing components, make the primary action obvious, check desktop and mobile in the browser, and show me screenshots plus anything you could not verify.”

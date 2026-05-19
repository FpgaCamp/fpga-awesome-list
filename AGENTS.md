# Repository Agent Rules

This repository is an English, practical awesome list for the FPGA ecosystem. Keep it useful for readers who need to learn, design, verify, build, debug, select hardware, or find maintained IP.

## README structure

- Keep `README.md` in English.
- Use concise, decision-oriented descriptions.
- Resource sections must use tables with these columns: `Resource`, `Use it for`, `Status`, `Activity`, `Stars`.
- Keep the colored status badges from the README reference definitions.
- Valid statuses are `active`, `stable`, `unknown`, and `legacy`.
- Sort rows in each resource table by status in this order: active, stable, unknown, legacy.
- Within the same status, sort by newest source-confirmed `Activity`, then GitHub stars descending, then resource name.
- Keep the `Source audit` section as a table with these columns: `Source`, `Scope`, `Action`, `Status`, `Activity`, `Stars`, `Audit result`.
- Valid source audit actions are `use_as_seed`, `manual_review`, and `monitor_only`.

## Activity and stars

- `Activity` must be `YYYY-MM` only.
- For GitHub repositories, `Activity` is the repository `pushed_at` month from GitHub metadata.
- For articles, marketplaces, releases, and normal websites, use `Activity` only if the source itself exposes a publication, release, or last-updated month.
- Never use the manual audit/check date as `Activity`.
- If a source-confirmed activity date cannot be extracted, leave `Activity` empty.
- For GitHub repository resources, fill `Stars` with the current GitHub star count.
- For GitHub organizations/users and non-GitHub resources, leave `Stars` empty unless the row links to a specific GitHub repository.
- At the time of each audit, classify GitHub-backed rows as `active` when activity is within the last 18 months, `stable` when useful but older than active and not clearly abandoned, and `legacy` when archived or clearly stale. Leave non-GitHub activity blank unless the source exposes a date.

## Curation requirements

- Audit new sources for consistency, reachability, accessibility, and practical value before adding entries.
- Prefer official docs, active projects, maintained examples, reproducible flows, and useful communities.
- Do not dump every item from a source list.
- Remove or skip generic search pages, duplicate landing pages, personal/contact-only links, dead mirrors, region-only social posts, and resources with unclear FPGA relevance.
- Keep legacy resources only when they are still useful for older flows, old devices, historical context, or durable references.
- If an external mirror is inaccessible but points to a useful canonical GitHub repository, prefer the canonical repository and note mirror limitations only when helpful.
- If a mirror or GitHub slug redirects to an unrelated project, mark it in `Source audit` and do not use it as a source for FPGA resources.

# Workly — continuation roadmap (from uploaded continuation prompt)

## Blocker: source code not yet available
- The GitHub repo `maddypandya44-a11y/adit-step1` is private (clone/API return 404) and this Lovable project is still a fresh TanStack Start template.
- Waiting on the user to either: (a) download the repo ZIP from GitHub and attach it in chat, or (b) make the repo public temporarily, or (c) re-import via "Import from GitHub".
- Do not start building until the source arrives — the prompt forbids starting from scratch.

## Once source arrives
- [ ] STEP 0 audit (routes, components, backend, secrets, mocked vs real) — report in ~10 lines
- [ ] Fix known bugs: toasts never appear (mount Sonner), tab title "Lovable App" → real title + meta/OG/favicon, end-to-end flow test
- [ ] Backend: Lovable Cloud tables w/ owner-only RLS: profiles, resumes, resume_versions, watched_companies, jobs, job_scores, applications, follow_ups, alerts, integrations
- [ ] Resume-Matcher port (TypeScript): parsing, keywords, match 0–100, rewrite suggestions, improve → resume_version; credit in README
- [ ] JobRadar port: Greenhouse/Lever/Ashby fetchers, stable job IDs, closed postings, LLM score w/ rules, daily token budget, scheduled digest email + in-app alerts
- [ ] AI tailoring + apply packages (PDF/DOCX export, confirmation before submit)
- [ ] Follow-ups (Gmail OAuth w/ approval + caps), integrations page
- [ ] Polish + tests + README credits
- [ ] Paywall audit: no upgrade/pricing/premium/pro/waitlist/stripe/checkout/subscribe/paywall/locked anywhere

## Hard rules
- NO paywall of any kind; every user gets everything instantly. Only invisible generous rate limits ("try again later" + reset time).
- Optional per-user LLM API key.
- Resumes private per user (RLS). Secrets server-side only. Confirmation before any application submit / email send.
- Keep Vite/React (TanStack) stack. Do not re-theme, do not regenerate whole files, small batched changes.

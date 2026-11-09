<!--
  ─────────────────────────────────────────────────────────────
  SWAP LIST (everything you need to change is marked YOUR-/Your)
  1. assets/hero.svg   → name, title line, city, tagline, stack line
  2. assets/route.svg  → the three stages of your own path
  3. Badge URLs below  → portfolio, LinkedIn, email, LeetCode
  4. Shipped table     → your projects (keep the "what it is" prose style)
  5. Numbers           → never ship this with my placeholder numbers in it
  ─────────────────────────────────────────────────────────────
-->

<img src="assets/hero.svg" alt="Your Name — AI engineer, full-stack" width="100%">

Engineer who works the whole path: the interface people touch, the services behind it,
the model call in the middle, and the unglamorous parts that decide whether any of it is
trustworthy — evals, retries, rate limits, tracing, a cost ceiling that actually holds.
**X years** of shipping things that were still up the next morning.

<a href="https://YOUR-PORTFOLIO"><img src="https://img.shields.io/badge/Portfolio-0B0E14?style=flat-square&logo=vercel&logoColor=E6EDF3&labelColor=0B0E14"></a>
<a href="https://linkedin.com/in/YOUR-HANDLE"><img src="https://img.shields.io/badge/LinkedIn-0B0E14?style=flat-square&logo=linkedin&logoColor=6EE7A8&labelColor=0B0E14"></a>
<a href="https://leetcode.com/YOUR-HANDLE"><img src="https://img.shields.io/badge/LeetCode-0B0E14?style=flat-square&logo=leetcode&logoColor=A78BFA&labelColor=0B0E14"></a>
<a href="mailto:YOUR@EMAIL"><img src="https://img.shields.io/badge/Email-0B0E14?style=flat-square&logo=gmail&logoColor=8B949E&labelColor=0B0E14"></a>

<br>

## The route so far

<img src="assets/route.svg" alt="Frontend to full-stack to AI systems" width="100%">

<br>

## Shipped

| Project | What it is | Links |
| --- | --- | --- |
| **PROJECT ONE** | One sentence on what a stranger can *do* with it, then the mechanism: what the front end is built on, what the back end actually does, and the one guardrail you're proud of. Name the model, the store, the retrieval strategy. End with a number — latency, accuracy, cost. | [Live](#) · [Code](#) |
| **PROJECT TWO** | The interesting constraint first ("runs the whole pipeline on free-tier inference", "answers in under 2s on a 400k-chunk index"), then how you met it. Say which part is a shortcut. | [Live](#) · [Code](#) |
| **PROJECT THREE** | The one from a real job. Scope it honestly: services, auth model, data layer, who used it. Private repos are fine — say "production (private)" and describe it well enough that the interviewer asks about it. | Production (private) |
| **PROJECT FOUR** | The one you're in the middle of. Two lines, no promises. | In progress |

<br>

## Things that cost me a weekend

- **Measure before you optimise.** A page felt slow, so I cached the wrong layer for two days. The trace said the time was in N sequential calls that had no reason to be sequential. Fanning them out took it from Xs to Ys. The fix was ten lines; finding it was the work.
- **Thresholds don't transfer.** A cutoff tuned by hand on one model was wrong on the next one, and wrong in the direction that silently answers questions it shouldn't. Now nothing ships with a hand-picked number unless there's a small eval set behind it.
- **Guardrails in layers, not one wall.** A relevance check, a prompt that can only cite what it retrieved, limits that can't be bypassed by changing a header, a daily spend cap, and a switch that turns the whole thing off. Any one of them alone is theatre.
- **Say what isn't done.** Every project here has a section at the bottom of its README listing what's missing. It has never once cost me an interview; it has twice started the best conversation in one.

<br>

## Stack

|  |  |
| --- | --- |
| **Front end** | React · TypeScript · Zustand · TanStack Query · Tailwind · Vite · Vitest |
| **Back end** | Python · FastAPI · Node · PostgreSQL · Redis · REST |
| **AI** | OpenAI / Anthropic APIs · embeddings · hybrid retrieval · evals · tracing |
| **Infra** | Docker · GitHub Actions · a cloud you can name confidently · Nginx |
| **Daily** | Git · your editor · your debugger |

<br>

## Off the clock

| What I do | What it carries over to |
| --- | --- |
| **Thing one** | The one-line principle it taught you. Keep it concrete — "scales before improvising" beats "discipline". |
| **Thing two** | Make the mapping slightly surprising. If the reader can guess the right-hand column from the left, cut the row. |
| **Thing three** | Four to eight rows. More than that and it reads as filler. |
| **Thing four** | At least one should be funny. |

<br>

## Currently

- Building **PROJECT**, in public, and writing down each thing that broke.
- Contributing to **OPEN SOURCE PROJECT** — link the PRs, not the org.
- Going deeper on the boring half: queues, caching, auth, and what "monitoring" means when the output is text.

<sub>Ask my demo a question it has no documents for and it will tell you it doesn't know. That's the guardrail, not a bug report.</sub>

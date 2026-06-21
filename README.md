# FallSeed IFA Firm

> **A Progressive Web App (PWA) seed for UK IFA firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-ifa/

## What this is

`fallseed-ifa` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the IFA wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

IFA · financial planning · investments (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`falladviser-v2`](https://sjgant80-hub.github.io/falladviser-v2/) | Client register · risk profile · suitability reports · KYC · vulnerable-customer flags · FCA-aligned recordkeeping |
| onboard | [`fallonboard`](https://sjgant80-hub.github.io/fallonboard/) | Client onboarding wizard · ID & verification · objectives · fact-find · risk questionnaire · KYC · consent capture |
| paper | [`fallpaper`](https://sjgant80-hub.github.io/fallpaper/) | Suitability letters · CIDD · KFI/illustrations · annual review packs · Consumer Duty fair-value templates |
| practice | [`fallpractice`](https://sjgant80-hub.github.io/fallpractice/) | Pipeline · ongoing servicing · MIFAR / Consumer Duty monitoring · breach log · file reviews · FOS / FSCS tracker |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-ifa-v2`) on your device
- **BroadcastChannel mesh** — `fall-ifa` for cross-tool sync; `fall-signal` for global hello
- **P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1031**, spine-clean mod 127. Mesh channel **`fall-ifa`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.

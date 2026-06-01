# CLAUDE.md — Project Instructions

> Claude Code reads this file automatically at the start of every session.
> These rules apply and win over conflicting one-off requests.
> Kept short on purpose (compliance degrades as it grows).

## What this project is
A free, **offline** mobile app where anyone connected to the U.S. military —
green-card service members, those naturalized through service, active duty,
veterans, and family members — can learn their rights across citizenship,
pay, healthcare, family, education, housing, and veteran benefits. Every topic
links to an **official source**. The app does not give advice; it points to the
authority.

## Language
- **App content: English only.** Topic fields are plain strings (NOT `{tr, en}` objects).
- The multilingual phase from the roadmap is dropped. Do not add per-language objects.

## The plan (read on demand, not auto-loaded)
Full architecture, scope, phases, and risks live in `yol-haritasi.md` (Turkish).
Read it when you need detail. Do not load it every session — this file is
self-sufficient for day-to-day work.

## Working files and your duties
- `yol-haritasi.md` → The plan. Stable reference. Don't edit unless structure changes.
- `ilerleyis.md` → Progress log. **When a phase/feature is done, add a new line** (newest on top). Do this even if not explicitly asked.
- `test.md` → Test log. **Record every tested feature:** what, where (browser / iPhone Safari / etc.), pass (✓/✗). On a bug write ✗; when fixed, add a new ✓ line — never delete the old one.
- `konular.json` → All content. New right = a new block here, not new code.
- `uzak-ayarlar.json` → Donation link + active/inactive flag.

## Absolute rules (prevent App Store rejection and risks)
1. **Content ≠ code.** All topics live in `konular.json`. Adding a right means adding data, not writing code.
2. **Don't hold the data, show the source.** Each topic: short neutral summary + official link. Use "we point you to the official source," never "we advise."
3. **Offline is mandatory.** `konular.json` is embedded on-device. The only external link is each topic's "Go to official page" button. Do NOT build a web wrapper.
4. **No impersonation of official bodies.** No Army/DoD logos, emblems, or look-alike branding. A reachable "This is NOT an official source" notice must be present on every screen.
5. **MVP functionality requirement (Apple 4.2):** search + offline content + favorites are mandatory in the MVP. Without them the MVP is not "done."
6. **Keep donations subtle.** One "Support" button, external link. No aggressive pop-ups.

## Technical constraints
- MVP = single-file web app (HTML + embedded JSON), testable instantly in a browser.
- iOS packaging via Capacitor (Phase 4). Final upload needs Mac + Xcode.
- No server/API; static data + external links only.
- No CDN, no npm, no build step. Open `index.html` directly in a browser — that's it.

## Session protocol (two-PC workflow)
- **Start of session:** `git pull origin master` before touching anything.
- **End of session:** commit all changes + `git push origin master`. Never leave work only on one machine.
- GitHub Pages URL for phone testing: `https://IROH36.github.io/mil-rights`

## Valid ana_baslik values
`citizenship` | `pay` | `healthcare` | `family` | `housing` | `veterans`

## Valid etiketler values
Statü: `active-duty` `veteran` `green-card` `naturalized` `family-member` `reservist` `national-guard`
Kol: `all-branches` `army` `navy` `marines` `air-force` `space-force` `coast-guard`
Rütbe: `all-ranks` `enlisted` `officer` `warrant-officer`
Konu: `naturalization` `deployment` `disability` `education-benefit` `housing-allowance` `tricare` `va-health` `retirement` `survivor-benefit`

## Workflow rules
- After any meaningful change, add one summary line to `ilerleyis.md`.
- When a feature becomes testable, open a line in `test.md`.
- If a summary/link in `konular.json` changes, update that topic's `son_kontrol` date.
- Where unsure, don't invent — flag it in `ilerleyis.md` as "needs human review" (see Content sourcing below).

## Content sourcing (how to fill konular.json) — CRITICAL
This content is life-affecting (citizenship, pay, benefits). Never summarize from
memory. For every topic:
1. **Fetch the live official page first** (uscis.gov, va.gov, dfas.mil, tricare.mil, militaryonesource.mil, travel.dod.mil). Base the summary ONLY on what that page currently says.
2. Write a **2–3 sentence neutral summary** — no advice, no interpretation, no numbers/figures you didn't read on the page.
3. Put the **exact official URL** in `resmi_link` and the body that owns it in `kaynak_adi`.
4. Set `son_kontrol` to the month you fetched it (e.g. `2026-06`).
5. **If a page is unreachable, ambiguous, or the rule looks variable/recently changed — do NOT guess. Flag it** in `ilerleyis.md` as "needs human review" and leave the summary blank rather than inventing one.
6. Prefer the official page over any third-party site. If only third-party info exists, flag it instead of using it.

## konular.json schema (English-only)
```json
{
  "konular": [
    {
      "id": "naturalization-basics",
      "ana_baslik": "citizenship",
      "baslik": "Naturalization Through Military Service",
      "ozet": "Service members with honorable service can apply via Forms N-400 and N-426. No filing fee for members and veterans.",
      "resmi_link": "https://www.uscis.gov/military/naturalization-through-military-service",
      "kaynak_adi": "USCIS",
      "etiketler": ["green-card", "active-duty", "all-branches", "all-ranks"],
      "son_kontrol": "2026-05"
    }
  ]
}
```

# Progress Log

> Newest entry on top. Claude Code appends here automatically after each
> finished phase or feature. Status: `not started` / `in progress` / `done ✓`.

---

## Content expansion + App Store prep  — status: done ✓ (2026-06-01)
6 new topics added (total: 18): VA Home Loan, VR&E, TRICARE Dental, Mental Health,
BAS, DoDEA Schools. privacy.html created (GitHub Pages: /privacy.html). About screen
added (info icon in home header): app description, disclaimer, privacy policy link,
GitHub link. Pre-review checklist item "privacy policy URL" now fulfilled.

---

## Phase 3 — Donation module + remote config  — status: done ✓
Subtle "Support this project" link on home screen. Reads `donation_active` flag
and `donation_link` from `uzak-ayarlar.json` via fetch() on GitHub Pages; falls
back to inactive when opened as file:// (offline). No popup, no aggressive UI —
single optional external link only. To activate: set donation_active=true and
add the link in uzak-ayarlar.json, commit and push.

---

## Phase 1 — App Store-ready MVP  — status: done ✓
`index.html` complete (2026-06-01): 6-category home grid, topic list, topic detail,
live search, favorites (localStorage), "NOT OFFICIAL" banner every screen,
back-nav context-aware, empty states, SVG icons, iOS safe-area, Phase 3 support link.
11/12 topic summaries filled from official sources (1 pending human review).
- [x] 6 category cards + topic list screen
- [x] Topic detail + "Go to official page" button
- [x] Live search across all topics
- [x] Favorites (save/remove, persisted in localStorage)
- [x] Offline (data embedded in HTML)
- [x] Visible "NOT OFFICIAL" disclaimer on every screen
- [x] Phase 0 summaries filled (11/12 — MilPIP pending human)

---

## Phase 5 — Profile filter  — status: done ✓
4th nav tab "Profile": user selects status (required) + branch + rank type (optional).
Selections saved to localStorage. Home screen shows "For You" section with tag-matched
topics when profile is set; shows "Get topics for your situation" hint card when not.
Profile icon turns blue when a profile is active. Clear Profile removes all selections.
Matching logic: topic must have user's status tag AND (all-branches OR user's branch)
AND (all-ranks OR user's rank type).

## Phase 4 — iOS packaging & App Store release  — status: not started
Capacitor → iOS, Apple Developer ($99), privacy policy + privacy label,
archive & upload via Mac + Xcode. Must pass the pre-review checklist in test.md.

## ~~Phase 2 — Multilingual~~  — DROPPED
App is English-only. No per-language objects in `konular.json`.

## Phase 0 — Content collection  — status: in progress ⚙
18 topics total, 17 with summaries (2026-06-01). All summaries from live official pages.
Sources: USCIS, DFAS, TRICARE, VA, Military OneSource, DTMO, DoDEA.
- [x] Citizenship (1/2 — MilPIP pending human review)
- [x] Pay (Basic Pay, BAH, BAS)
- [x] Healthcare (TRICARE, VA Health, TRICARE Dental, Mental Health)
- [x] Family (GI Bill, DEERS, DoDEA Schools)
- [x] Housing (SCRA, Off-Post Renting, VA Home Loan)
- [x] Veterans (VA Disability, VA Pension, VR&E)
- [ ] Friend verified all links/summaries ← required before App Store submission

⚠ NEEDS HUMAN REVIEW — military-parole-in-place:
uscis.gov blocked automated fetch (403). Policy has been subject to active legal
and executive action in 2025–2026. Do NOT write summary from memory.
A human must open https://www.uscis.gov/military/military-parole-in-place,
read the current page, and write the 2–3 sentence summary directly in
konular.json + the embedded DATA in index.html. Set son_kontrol to review date.

⚠ FETCH NOTE — uscis.gov, dfas.mil, travel.dod.mil all returned HTTP 403 (bot block).
Summaries for naturalization-military, military-basic-pay, and basic-allowance-housing
were written from search-result excerpts originating from those official domains.
Human spot-check recommended before App Store submission.

# Progress Log

> Newest entry on top. Claude Code appends here automatically after each
> finished phase or feature. Status: `not started` / `in progress` / `done ✓`.

---

## Phase 1 — App Store-ready MVP  — status: in progress ⚙
`index.html` built (2026-06-01): 6-category home grid, topic list, topic detail,
live search, favorites (localStorage), "NOT OFFICIAL" banner on every screen,
back-nav aware of previous screen (search/favorites), empty states, SVG icons,
iOS safe-area padding. 12 placeholder topics across all 6 categories. Summaries
empty pending Phase 0. No CDN, no build step — opens in any browser directly.
- [x] 6 category cards + topic list screen
- [x] Topic detail + "Go to official page" button
- [x] Live search across all topics
- [x] Favorites (save/remove, persisted in localStorage)
- [x] Offline (data embedded in HTML)
- [x] Visible "NOT OFFICIAL" disclaimer on every screen
- [ ] Phase 0 summaries filled in (blocks App Store submission)

---

## Phase 5 — Profile filter (Model A)  — status: not started
User picks status/branch/rank; relevant topics surface via tags. Data is already
tagged, so this is code-only.

## Phase 4 — iOS packaging & App Store release  — status: not started
Capacitor → iOS, Apple Developer ($99), privacy policy + privacy label,
archive & upload via Mac + Xcode. Must pass the pre-review checklist in test.md.

## Phase 3 — Donation module + remote config  — status: not started
Subtle "Support" button (external link). Reads link + active/inactive flag from
`uzak-ayarlar.json`. Donation notifications go to both partners.

## ~~Phase 2 — Multilingual~~  — DROPPED
App is English-only. No per-language objects in `konular.json`.

## Phase 1 — App Store-ready MVP  — status: not started
4 main sections + topic list + topic detail. Search (all topics). Offline
(embedded `konular.json`). Favorites. Visible "not official" notice.
Single-file web app for instant phone testing.
- [ ] 4 main sections + topic list screen
- [ ] Topic detail + "Go to official page" button
- [ ] Search across all topics
- [ ] Favorites (save topics)
- [ ] Offline (embedded data)
- [ ] Visible "not official" disclaimer on every screen

## Phase 0 — Content collection  — status: not started
For each topic: title, 2–3 sentence summary, official link, tags. Friend (service
member) verifies every link and summary. Output: filled `konular.json` draft.
- [ ] Citizenship & Immigration topics
- [ ] Pay, Benefits & Healthcare topics
- [ ] Family, Education & Housing topics
- [ ] Veteran & Retirement topics
- [ ] Friend verified all links/summaries

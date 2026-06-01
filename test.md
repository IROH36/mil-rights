# Test Log

> Claude Code records every tested feature here. On a bug write ✗; when fixed,
> add a new ✓ line below — never delete the old one. Keep the history.

## Test layers (where we test)
1. **Browser (desktop)** — daily work. Open the HTML file, refresh, check.
2. **Browser phone view** — F12 → device toolbar (iPhone size). Layout/fit checks.
3. **Friend's iPhone (US)** — real device via a shared link (e.g. GitHub Pages). Real touch, real screen.
4. **Xcode on a Mac** — only near Phase 4, app installed as a real app before any App Store submission.

---

## Phase 1 — MVP tests
| Date | Feature tested | Where | Result |
|------|----------------|-------|--------|
|      | Home: 6 category cards render, correct topic counts | Browser desktop | |
|      | Home: tap category → opens topic list | Browser desktop | |
|      | Topic detail: "Go to Official Page" opens correct URL in new tab | Browser desktop | |
|      | Topic detail: Save/Remove toggles correctly, red dot appears in list | Browser desktop | |
|      | Search: live filter works, correct results for "veteran", "tricare", "naturalization" | Browser desktop | |
|      | Search: empty state shown when no query | Browser desktop | |
|      | Favorites: saved topics appear, empty state shown when none | Browser desktop | |
|      | Back navigation: from topic → returns to category | Browser desktop | |
|      | Back navigation: from topic (via search) → returns to search | Browser desktop | |
|      | Disclaimer banner: visible on every screen | Browser desktop | |
|      | Layout: no overflow, no cut-off elements on iPhone size (375px) | Browser phone view (F12) | |
|      | Favorites persist after page refresh | Browser desktop | |
|      | All above on real device | Friend's iPhone (US) | |

## Phase 0 — Content tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | Links open the correct official page | Browser |  |
|      | Summaries match the official source | Browser (friend) |  |

---

## Pre-review checklist (iOS — Apple, from roadmap §4.4)
- [ ] Search works
- [ ] Content opens offline
- [ ] Favorites work
- [ ] Privacy policy URL ready + privacy label filled
- [ ] Visible "not official" disclaimer reachable on every screen
- [ ] No official logos/emblems anywhere
- [ ] Donation button is subtle, single, optional

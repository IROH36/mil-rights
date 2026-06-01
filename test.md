# Test Log

> Claude Code records every tested feature here. On a bug write ✗; when fixed,
> add a new ✓ line below — never delete the old one. Keep the history.

## Test layers (where we test)
1. **Browser (desktop)** — daily work. Open the HTML file, refresh, check.
2. **Browser phone view** — F12 → device toolbar (iPhone size). Layout/fit checks.
3. **Friend's iPhone (US)** — real device via a shared link (e.g. GitHub Pages). Real touch, real screen.
4. **Xcode on a Mac** — only near Phase 4, app installed as a real app before any App Store submission.

---

## App Store prep tests
| Date | Feature tested | Where | Result |
|------|----------------|-------|--------|
|      | privacy.html opens at /privacy.html and renders correctly | Browser desktop | |
|      | privacy.html "Back to Mil-Rights" link works | Browser desktop | |
|      | About screen: info icon (ⓘ) visible in home header | Browser desktop | |
|      | About → Privacy Policy button opens privacy.html in new tab | Browser desktop | |
|      | About → GitHub button opens correct repo | Browser desktop | |
|      | 18 topics total render correctly (check each category count) | Browser desktop | |

## Phase 5 — Profile filter tests
| Date | Feature tested | Where | Result |
|------|----------------|-------|--------|
|      | Profile screen opens via nav tab | Browser desktop | |
|      | Tapping status pill selects it (highlights); tapping again deselects | Browser desktop | |
|      | Branch + rank pills work independently | Browser desktop | |
|      | Home: "Get topics for your situation" hint shown when no profile set | Browser desktop | |
|      | Home → profile → select Active Duty → Done → "For You" section appears | Browser desktop | |
|      | "For You" topics match selected status/branch/rank tags correctly | Browser desktop | |
|      | "Edit Profile" link on home → opens profile screen | Browser desktop | |
|      | Clear Profile → For You section disappears, hint card returns | Browser desktop | |
|      | Profile persists after page refresh | Browser desktop | |
|      | Profile tab icon turns blue when profile is active | Browser desktop | |
|      | All above on real device | Friend's iPhone (US) | |

## Phase 3 — Donation module tests
| Date | Feature tested | Where | Result |
|------|----------------|-------|--------|
|      | donation_active=false → support link NOT visible on home | Browser desktop | |
|      | donation_active=true + link set → support link visible, subtle | Browser desktop | |
|      | Support link opens correct external URL in new tab | Browser desktop | |
|      | file:// access → support link hidden (fetch fails, default inactive) | Browser desktop (file://) | |
|      | On real device via GitHub Pages: link visible when active | Friend's iPhone (US) | |

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
|      | naturalization-military: link opens correct USCIS page | Browser | |
|      | military-basic-pay: link opens correct DFAS page | Browser | |
|      | basic-allowance-housing: link opens DTMO BAH page | Browser | |
|      | tricare-plans: link opens TRICARE eligibility page | Browser | |
|      | va-health-care: link opens VA health care page | Browser | |
|      | gi-bill: link opens VA GI Bill page | Browser | |
|      | dependent-id-deers: link opens Military OneSource ID page | Browser | |
|      | scra-rights: link opens Military OneSource SCRA page | Browser | |
|      | off-post-renting: link opens Military OneSource housing page | Browser | |
|      | va-disability: link opens VA disability page | Browser | |
|      | veterans-pension: link opens VA pension page | Browser | |
|      | All summaries verified against live official pages | Browser (friend) | |
|      | military-parole-in-place: human reads current USCIS page, writes summary | Browser (friend) | PENDING |

---

## Pre-review checklist (iOS — Apple, from roadmap §4.4)
- [ ] Search works
- [ ] Content opens offline
- [ ] Favorites work
- [ ] Privacy policy URL ready + privacy label filled
- [ ] Visible "not official" disclaimer reachable on every screen
- [ ] No official logos/emblems anywhere
- [ ] Donation button is subtle, single, optional

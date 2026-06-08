# Test Log

> Claude Code records every tested feature here. On a bug write ✗; when fixed,
> add a new ✓ line below — never delete the old one. Keep the history.

## Test layers (where we test)
1. **Browser (desktop)** — daily work. Open the HTML file, refresh, check.
2. **Browser phone view** — F12 → device toolbar (iPhone size). Layout/fit checks.
3. **Friend's iPhone (US)** — real device via a shared link (e.g. GitHub Pages). Real touch, real screen.
4. **Xcode on a Mac** — only near Phase 4, app installed as a real app before any App Store submission.

---

## New topics (2026-06-08 pay + family batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | involuntary-separation-pay: link opens 10 U.S.C. §1174 on law.cornell.edu | Browser | |
|      | disability-severance-pay: link opens MyArmyBenefits DSP page | Browser | |
|      | mypay-dfas-portal: link opens dfas.mil/mypayinfo | Browser | |
|      | healthcare-professional-special-pays: link opens militarypay.defense.gov special pays page | Browser | |
|      | reserve-guard-retirement-points: link opens DFAS retirement eligibility page | Browser | |
|      | family-care-plan: link opens militaryonesource.mil FCP page | Browser | |
|      | joint-spouse-macp: link opens militaryonesource.mil dual military couples page | Browser | |
|      | gi-bill-mha: link opens va.gov Post-9/11 GI Bill rates page | Browser | |
|      | military-child-support-garnishment: link opens dfas.mil garnishment page | Browser | |

## New topics (2026-06-08 citizenship + housing expansion batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | ina-329-hostilities-periods: link opens USCIS Policy Manual Vol.12 Part I Chapter 3 | Browser | |
|      | guard-reserve-naturalization: link opens USCIS Policy Manual Vol.12 Part I Chapter 5 | Browser | |
|      | n-600-certificate-citizenship: link opens uscis.gov/n-600 | Browser | |
|      | expedited-oath-deploying: link opens USCIS Policy Manual Vol.12 Part J Chapter 6 | Browser | |
|      | advance-parole-military-adjustment: link opens uscis.gov/i-131 | Browser | |
|      | noncitizen-enlistment-lpr: link opens mepcom.army.mil Applicants page | Browser | |
|      | lpr-return-from-deployment: link opens uscis.gov international travel as permanent resident | Browser | |
|      | afghan-siv-com-process: link opens uscis.gov Afghan SIV page | Browser | |
|      | bah-dependency-status: link opens militaryonesource.mil BAH page | Browser | |
|      | military-relocation-assistance: link opens militaryonesource.mil RAP page | Browser | |
|      | scra-vehicle-storage-lien: link opens militaryonesource.mil SCRA page | Browser | |
|      | on-base-housing-waitlist: link opens militaryonesource.mil on-installation housing page | Browser | |
|      | tle-domestic: updated summary shows 21-day figure (Nov 2024 JTR change) | Browser | |

## New topics (2026-06-08 citizenship + healthcare + family + housing batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | n-648-disability-exemption: link opens uscis.gov/n-648 | Browser | |
|      | i-360-special-immigrant-military: link opens uscis.gov/i-360 | Browser | |
|      | deferred-action-military-family: link opens USCIS discretionary options page (⚠ May 2026 policy update — human spot-check) | Browser | |
|      | naturalization-after-discharge: link opens USCIS Policy Manual Vol.12 Part I Chapter 2 (⚠ 403 flagged — human spot-check) | Browser | |
|      | aila-military-assistance: link opens militaryonesource.mil AILA page | Browser | |
|      | va-loan-entitlement-restoration: link opens va.gov home loans eligibility page | Browser | |
|      | scra-lease-termination: link opens militaryonesource.mil SCRA lease page | Browser | |
|      | active-duty-dental-addp: link opens tricare.mil/addp | Browser | |
|      | tricare-mental-health: link opens tricare.mil mental health page | Browser | |
|      | tricare-maternity: link opens tricare.mil maternity page | Browser | |
|      | tricare-guard-reserve-activation: link opens tricare.mil Guard/Reserve activation page | Browser | |
|      | reserve-drill-pay: link opens DFAS drill pay table (⚠ DFAS 403 flagged — human spot-check) | Browser | |
|      | military-cdc-childcare: link opens militaryonesource.mil child care page | Browser | |
|      | yellow-ribbon-reintegration: link opens yellowribbon.mil | Browser | |
|      | esgr-ombudsman: link opens esgr.mil (⚠ SSL issues — human spot-check) | Browser | |

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

## New topics (2026-06-05 ninth batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | military-efmp: link opens Military OneSource EFMP page | Browser | |
|      | military-childcare-fee-assistance: link opens Military OneSource child care page | Browser | |
|      | bah-differential: link opens DFAS BAH rates page (⚠ 403 flagged — human spot-check) | Browser | |
|      | va-joint-loan: link opens VA home loans page | Browser | |
|      | va-residual-income: link opens VA home loans page | Browser | |

## New topics (2026-06-05 eighth batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | va-multifamily-loan: link opens VA purchase loan page | Browser | |
|      | overseas-military-naturalization: link opens USCIS overseas naturalization page (⚠ 403 flagged — human spot-check) | Browser | |
|      | uscis-expedite-military: link opens USCIS expedite requests page (⚠ 403 flagged — human spot-check) | Browser | |
|      | va-emergency-care-non-va: link opens VA community care emergency page | Browser | |
|      | military-spouse-federal-hiring: link opens OPM military spouses hiring page | Browser | |

## New topics (2026-06-05 seventh batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | home-sale-tax-exclusion-military: link opens IRS Topic 701 | Browser | |
|      | scra-interest-rate-cap: link opens Military OneSource SCRA page | Browser | |
|      | uscis-fee-exemption-military: link opens USCIS fee waiver info page (⚠ 403 flagged — human spot-check) | Browser | |
|      | military-caregiver-leave: link opens DOL Fact Sheet 28M(a) (⚠ 403 flagged — human spot-check) | Browser | |
|      | advance-pay-pcs: link opens DFAS PCS travel pay page (⚠ 403 flagged — human spot-check) | Browser | |

## New topics (2026-06-05 sixth batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | i-751-military-waiver: link opens USCIS I-751 page (⚠ 403 flagged — human spot-check) | Browser | |
|      | va-home-loan-closing-costs: link opens VA funding fee & closing costs page | Browser | |
|      | va-condo-approval: link opens VA LGY condo report tool | Browser | |
|      | va-loan-occupancy: link opens VA home loan eligibility page | Browser | |
|      | bah-guard-reserve-activation: link opens Military OneSource BAH page | Browser | |

## New topics (2026-06-05 fifth batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | posthumous-citizenship: link opens USCIS N-644 page (⚠ 403 flagged — human spot-check) | Browser | |
|      | vawa-immigrant-spouse: link opens USCIS abused spouses page (⚠ 403 flagged — human spot-check) | Browser | |
|      | ppm-dity-move: link opens Military OneSource PPM page | Browser | |
|      | va-minimum-property-requirements: link opens VA home buying process page | Browser | |

## New topics (2026-06-05 fourth batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | va-loan-entitlement-limits: link opens VA loan limits page | Browser | |
|      | va-manufactured-home: link opens VA purchase loan page | Browser | |
|      | va-loan-assumption: link opens VA eligibility page | Browser | |
|      | naturalization-spouse-abroad: link opens USCIS military family citizenship page (⚠ 403 flagged — human spot-check) | Browser | |
|      | n-426-military-naturalization: link opens USCIS N-426 page (⚠ 403 flagged — human spot-check) | Browser | |

## New topics (2026-06-05 third batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | va-construction-loan: link opens VA News construction loan page | Browser | |
|      | va-energy-efficient-mortgage: link opens VA home loans page | Browser | |
|      | tdy-per-diem-rates: link opens DTMO per diem page (⚠ 403 flagged — human spot-check) | Browser | |
|      | military-pay-allotments: link opens DFAS allotments page (⚠ 403 flagged — human spot-check) | Browser | |
|      | pcs-household-goods: link opens Military OneSource PCS entitlements page | Browser | |

## New topics (2026-06-05 second batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | n-600k-military-child-abroad: link opens USCIS N-600K page | Browser | |
|      | lpr-reentry-permit-deployment: link opens USCIS I-131 page | Browser | |
|      | n-470-preserve-naturalization-residence: link opens USCIS N-470 page | Browser | |
|      | immvets-deported-veterans: link opens DHS ImmVets page (⚠ 403 flagged — human spot-check) | Browser | |
|      | va-cash-out-refinance: link opens VA cash-out refinance page | Browser | |
|      | crsc-combat-related-compensation: link opens VA CRSC page | Browser | |
|      | survivor-benefit-plan-sbp: link opens Military OneSource SBP page | Browser | |

## New topics (2026-06-05 batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | purple-heart-benefits: link opens VA News Purple Heart page | Browser | |
|      | military-parental-leave: link opens Military OneSource parental leave page | Browser | |
|      | military-protective-order: link opens Military OneSource domestic abuse page | Browser | |

## New topics (2026-06-05 first batch) — content link tests
| Date | What checked | Where | Result |
|------|--------------|-------|--------|
|      | va-tbi-polytrauma: link opens polytrauma.va.gov page | Browser | |
|      | military-fmla: link opens DOL FMLA page (⚠ DOL 403 flagged — human spot-check) | Browser | |
|      | sdvosb-vetcert: link opens SBA VetCert page | Browser | |
|      | va-audiology-hearing: link opens VA audiology page | Browser | |
|      | va-solid-start: link opens VA Solid Start page | Browser | |
|      | survivor-outreach-services: link opens Army MWR SOS page | Browser | |
|      | assignment-incentive-pay: link opens DFAS AIP page (⚠ DFAS 403 flagged — human spot-check) | Browser | |
|      | va-blind-rehabilitation: link opens VA blind/low vision page | Browser | |
|      | dodea-virtual-high-school: link opens DoDEA Virtual High School page (⚠ DoDEA 403 flagged — human spot-check) | Browser | |

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

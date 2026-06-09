# Mil-Rights

**A free, offline app for U.S. military members, veterans, and their families.**

Know your rights — citizenship, pay, healthcare, family, education, housing, and veteran benefits. 431 topics, every one linked to an official government source.

> This app does not give advice. It points to the authority.

**This is NOT an official government or military resource.**

---

## Try it now

**[Open the app →](https://iroh36.github.io/mil-rights)**

Works in any browser on phone or desktop — no install, no account, no server.

---

## Status

| Phase | Description | Status |
|---|---|---|
| 0 | Content collection (328 topics, official sources) | done ✓ |
| 1 | Offline web MVP — search, favorites, 6 categories | done ✓ |
| 3 | Donation module (remote config via uzak-ayarlar.json) | done ✓ |
| 5 | Profile filter — For You section, tag-based matching | done ✓ |
| — | Privacy policy + About screen | done ✓ |
| 4 | iOS packaging + App Store (needs Mac + Xcode) | not started |

## Privacy

**[Privacy policy](https://iroh36.github.io/mil-rights/privacy.html)**

The app stores only favorites and profile settings in `localStorage` — on your device, never transmitted. No analytics, no accounts, no server.

## Structure

```
index.html          ← single-file app (no dependencies, opens in any browser)
privacy.html        ← privacy policy (hosted on GitHub Pages)
konular.json        ← all content (official sources only, mirrors embedded data)
uzak-ayarlar.json   ← donation config (set donation_active: true to enable)
CLAUDE.md           ← AI assistant rules
yol-haritasi.md     ← full architecture and phase plan (Turkish)
ilerleyis.md        ← progress log
test.md             ← test log
```

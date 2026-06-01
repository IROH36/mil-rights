# Yol Haritası — Mil-Rights

> Mimari kararlar, kapsam, riskler ve faz planı burada.
> CLAUDE.md'de tanımlanan günlük kurallar bu belgeye göre önceliklidir.

---

## Proje Özeti

**Ne:** ABD askeri bağlantılı bireyler (yeşil kartlı er/erbaşlar, hizmetle vatandaşlaştırılanlar, aktif görev, gaziler, aile üyeleri) için ücretsiz, offline mobil haklar rehberi.

**Ne değil:** Hukuki tavsiye aracı, resmi kaynak, DoD/Army affiliate.

**Temel prensip:** Her hak = kısa tarafsız özet + resmi kaynak linki. Biz yönlendiririz, tavsiye vermeyiz.

---

## Kapsam — Ana Başlıklar (ana_baslik değerleri)

| Değer (kodda) | Kullanıcıya görünen |
|---|---|
| `citizenship` | Citizenship & Immigration |
| `pay` | Pay & Benefits |
| `healthcare` | Healthcare |
| `family` | Family & Education |
| `housing` | Housing |
| `veterans` | Veterans & Retirement |

---

## Etiket Taxonomy (konular.json → etiketler)

### Statü
- `active-duty`
- `veteran`
- `green-card` — vatandaşlık almamış hizmet üyeleri
- `naturalized` — hizmetle vatandaşlaştırılan
- `family-member` — eş, çocuk, bağımlı
- `reservist`
- `national-guard`

### Kol
- `all-branches`
- `army`
- `navy`
- `marines`
- `air-force`
- `space-force`
- `coast-guard`

### Rütbe (gerekli durumlarda)
- `all-ranks`
- `enlisted`
- `officer`
- `warrant-officer`

### Konu spesifik
- `naturalization`
- `deployment`
- `disability`
- `education-benefit` — GI Bill vb.
- `housing-allowance` — BAH
- `tricare`
- `va-health`
- `retirement`
- `survivor-benefit`

---

## Resmi Kaynaklar (Phase 0 için fetch listesi)

| Site | Konu |
|---|---|
| uscis.gov | Vatandaşlık, yeşil kart, doğallaşma |
| va.gov | Gaziler yardımları, sağlık, engellilik |
| dfas.mil | Maaş, tazminat |
| tricare.mil | Sağlık sigortası |
| militaryonesource.mil | Aile, eğitim, konut |
| travel.dod.mil | Seyahat, taşınma (PCS) |
| myarmybenefits.us.army.mil | Ordu spesifik yardımlar |
| gibill.benefits.va.gov | GI Bill eğitim yardımları |

---

## Teknik Mimari

```
mil-rights/
├── index.html          ← tek dosya MVP (HTML + inline CSS + inline JS)
├── konular.json        ← tüm içerik (index.html bunu embed eder)
├── uzak-ayarlar.json   ← bağış linki + aktif/pasif flag
├── CLAUDE.md           ← Claude kuralları
├── yol-haritasi.md     ← bu dosya
├── ilerleyis.md        ← ilerleme logu
└── test.md             ← test logu
```

**index.html nasıl çalışır:**
- `konular.json` içeriği build sırasında HTML'e embed edilir (veya `fetch()` ile aynı dizinden okunur — ikisi de offline çalışır, GitHub Pages'de fetch tercih edilir)
- Harici bağımlılık: yok (CDN bile kullanma, offline zorunlu)
- iOS packaging: Capacitor ile Phase 4'te

**GitHub Pages:** `main` branch → `index.html` → `https://IROH36.github.io/mil-rights`
Arkadaşın iPhone testi için bu URL kullanılır.

---

## Faz Planı

### Phase 0 — İçerik Toplama
- Her konu için: resmi sayfayı fetch et → 2-3 cümle tarafsız özet yaz → link + kaynak ekle
- Arkadaş (hizmet üyesi) her linki ve özeti doğrular
- Output: dolu `konular.json`
- Tahmini: 4-6 saat araştırma + 1 doğrulama turu

### Phase 1 — App Store'a Hazır MVP
**Gereksinimler (Apple 4.2 için zorunlu):**
- 4 ana bölüm + konu listesi + konu detayı
- Tüm konularda arama
- Favoriler (cihazda sakla, localStorage)
- Offline çalışma (embed data)
- Her ekranda görünür "Bu resmi bir kaynak değildir" uyarısı
- "Resmi sayfaya git" butonu (harici link)

**Teknik:**
- Tek HTML dosyası, CDN yok, inline CSS+JS
- `konular.json` fetch ile yüklenir (GitHub Pages'de çalışır)

### Phase 2 ~~Çok dilli~~ — KALDIRILDI
Uygulama yalnızca İngilizce.

### Phase 3 — Bağış Modülü + Uzak Config
- "Support" butonu (harici link, subtle)
- `uzak-ayarlar.json`'dan link + aktif/pasif flag okur
- Agresif popup yok (App Store reddi riski)

### Phase 4 — iOS Paketleme + App Store
- Capacitor kurulumu → iOS build
- Apple Developer hesabı ($99/yıl)
- Privacy policy URL + privacy label
- Mac + Xcode gerekli (build aşamasında)
- Pre-review checklist: test.md'de

### Phase 5 — Profil Filtresi
- Kullanıcı statü/kol/rütbe seçer → etiket bazlı filtreleme
- Veri zaten etiketli, bu aşama sadece kod

---

## Riskler

| Risk | Olasılık | Çözüm |
|---|---|---|
| Apple 4.2 reddi (yeterli içerik yok) | Orta | MVP'de en az 15-20 konu olsun |
| Resmi sayfa URL'leri değişir | Yüksek | `son_kontrol` tarihi ile periyodik güncelleme |
| Hukuki itiraz (tavsiye izlenimi) | Düşük | "Bu resmi kaynak değildir" + "biz tavsiye vermeyiz" dili |
| İçerik yanlışlığı | Orta | Arkadaş doğrulaması zorunlu (Phase 0) |

---

## Çift PC Çalışma Protokolü

1. **Oturum başında:** `git pull origin master`
2. **Oturum sonunda:** tüm değişiklikleri commit + `git push origin master`
3. Yerel bağımlılık yok — sadece tarayıcı ve bu repo yeterli
4. Test için: `index.html`'i doğrudan tarayıcıda aç veya GitHub Pages URL'ini kullan

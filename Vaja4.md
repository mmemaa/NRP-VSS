# 🧪 Vaja 4: UX/UI zasnova aplikacije

## 🎯 Naloga
Izdelajte **UX in UI zasnovo** svoje aplikacije.  
Cilj je določiti **kako aplikacija deluje** in **kako so elementi razporejeni na zaslonih**.

---

## ✅ Kaj morate narediti

### 1️⃣ Seznam vseh zaslonov aplikacije

Aplikacija vsebuje naslednje zaslone:

1. **Vstopna stran (Landing Page)** - Marketinška stran za nove obiskovalce
2. **Prijava (Login)** - Prijava v obstoječi račun
3. **Registracija (Sign Up)** - Ustvarjanje novega računa
4. **Domača stran (Dashboard)** - Pregled vseh wishlist seznamov in obvestil
5. **Wishlist seznami** - Organizacija izdelkov po kategorijah
6. **Dodaj izdelek** - Dodajanje novega izdelka z URL ali ročno
7. **Podrobnosti izdelka** - Detajli izdelka, zgodovina cen, pravila obveščanja
8. **Iskanje trgovin** - Seznam podprtih trgovin in dodajanje novih
9. **Obvestila** - Pregled vseh prejetih obvestil o cenah in akcijah
10. **Profil uporabnika** - Osebni podatki in statistika prihrankov
11. **Nastavitve** - Konfiguracija obvestil, računa in preferenc
12. **Premium upgrade** - Prehod na premium račun

---

### 2️⃣ UX struktura (kaj se dogaja na strani)

#### 1. Vstopna stran (Landing Page)
**Glavni namen:** Predstaviti vrednost aplikacije novim obiskovalcem in jih prepričati k registraciji.

**Akcije uporabnika:**
- Prebere glavno vrednostno ponudbo (hero sekcija)
- Pregleda funkcionalnosti (features)
- Prebere reference/testimonials
- Klikne na "Začni brezplačno" → Navigacija na Registracijo
- Klikne na "Prijavi se" → Navigacija na Prijavo

**Navigacija:**
- CTA gumb (hero): Registracija
- Header: Login, Sign Up
- Footer: O nas, Kontakt, Pogoji uporabe, Zasebnost

---

#### 2. Prijava (Login)
**Glavni namen:** Omogočiti uporabnikom dostop do svojega računa.

**Akcije uporabnika:**
- Vnese email naslov
- Vnese geslo
- (Opcijsko) Označi "Zapomni si me"
- Klikne "Prijavi se" → Navigacija na Dashboard
- Klikne "Pozabljeno geslo?" → Email za reset gesla
- Klikne "Nisi član? Registriraj se" → Navigacija na Registracijo
- (Opcijsko) Prijava z Google/Facebook

**Navigacija:**
- Nazaj na Landing page (logo/link)
- Link na Registracijo

---

#### 3. Registracija (Sign Up)
**Glavni namen:** Ustvariti nov uporabniški račun.

**Akcije uporabnika:**
- Vnese ime in priimek
- Vnese email naslov
- Vnese geslo (z validacijo moči gesla)
- Sprejme pogoje uporabe in politiko zasebnosti
- Klikne "Ustvari račun" → Navigacija na Dashboard (po verifikaciji)
- Klikne "Že imaš račun? Prijavi se" → Navigacija na Prijavo
- (Opcijsko) Registracija z Google/Facebook

**Navigacija:**
- Nazaj na Landing page
- Link na Prijavo

---

#### 4. Domača stran (Dashboard)
**Glavni namen:** Osrednje mesto za pregled vseh wishlist seznamov, najnovejših obvestil in hitrih akcij.

**Akcije uporabnika:**
- Pregleda aktivna obvestila (npr. "3 izdelki so na akciji!")
- Vidi statistiko: prihranki tega meseca, število spremljanih artiklov
- Pregleda vse wishlist sezname (kartice)
- Klikne na wishlist seznam → Navigacija na Wishlist podrobnosti
- Klikne "+ Nov seznam" → Ustvari nov wishlist
- Klikne "+ Dodaj izdelek" → Navigacija na Dodaj izdelek
- Pregleda najnovejša obvestila (zadnjih 5)
- Klikne "Vse obvestila" → Navigacija na Obvestila

**Navigacija:**
- Top bar: Logo, Iskanje, Obvestila (zvonček), Profil
- Spodnji navigation bar (mobile): Domov, Wishlists, Dodaj, Obvestila, Profil

---

#### 5. Wishlist seznami
**Glavni namen:** Pregled izdelkov znotraj specifičnega wishlist seznama.

**Akcije uporabnika:**
- Pregleda vse izdelke v seznamu (kartice z sliko, naslov, trenutna cena, trend cene)
- Filtrira izdelke (vsi / na akciji / dosežena ciljna cena / razprodano)
- Sortira izdelke (datum dodajanja, cena, % popusta)
- Klikne na izdelek → Navigacija na Podrobnosti izdelka
- Klikne "Dodaj izdelek" → Navigacija na Dodaj izdelek
- Uredi ime seznama
- Izbriše seznam
- Deli seznam (opcijsko za Premium)

**Navigacija:**
- Nazaj na Dashboard
- Top bar navigacija ostane enaka

---

#### 6. Dodaj izdelek
**Glavni namen:** Dodati nov izdelek za spremljanje v wishlist.

**Akcije uporabnika:**
- Prilepi URL izdelka iz spletne trgovine
- (Avto-parsing) Sistem pridobi ime, sliko, ceno, trgovino
- (Ročno) Popravi podatke, če auto-parsing ni natančen
- Izbere wishlist seznam (dropdown)
- Nastavi pravila obveščanja:
  - Ciljna cena (npr. "obvestilo, če cena pade pod €50")
  - % popusta (npr. "obvestilo pri >30% popustu")
  - Ponovna razpoložljivost (če je razprodano)
- Klikne "Dodaj v wishlist" → Izdelek je dodan, navigacija nazaj na Dashboard ali Wishlist
- Klikne "Prekliči" → Navigacija nazaj

**Navigacija:**
- Nazaj na prejšnjo stran (Dashboard ali Wishlist)

---

#### 7. Podrobnosti izdelka
**Glavni namen:** Prikazati vse informacije o izdelku, zgodovino cen in možnost urejanja pravil.

**Akcije uporabnika:**
- Pregleda trenutno ceno in trgovino
- Vidi graf zgodovine cen (zadnjih 30/60/90 dni)
- Pregleda nastavljena pravila obveščanja
- Uredi pravila obveščanja
- Klikne "Obišči trgovino" → Odpre izdelek v trgovini (novi tab)
- Premakne izdelek v drug wishlist
- Izbriše izdelek iz wishlist-a
- Deli izdelek (opcijsko)

**Navigacija:**
- Nazaj na Wishlist
- Top bar navigacija ostane enaka

---

#### 8. Iskanje trgovin
**Glavni namen:** Prikazati seznam podprtih trgovin in možnost predlaganja novih.

**Akcije uporabnika:**
- Pregleda vse podprte trgovine (ikone/logotipi)
- Uporablja iskanje za filtriranje trgovin
- Filtrira po državi/regiji
- Klikne na trgovino → Pregled vseh izdelkov iz te trgovine v wishlistih
- Klikne "Predlagaj trgovino" → Odpre obrazec za predlog nove trgovine

**Navigacija:**
- Dostopno iz Dashboard-a (link ali sekcija)
- Nazaj na Dashboard

---

#### 9. Obvestila
**Glavni namen:** Pregled vseh prejetih obvestil o cenah, akcijah in razpoložljivosti.

**Akcije uporabnika:**
- Pregleda vse obvestila (najnovejša najprej)
- Filtrira obvestila (neprebrana / prebrana / akcije / razpoložljivost)
- Klikne na obvestilo → Navigacija na Podrobnosti izdelka
- Označi obvestilo kot prebrano
- Izbriše obvestilo

**Navigacija:**
- Nazaj na Dashboard
- Top bar navigacija ostane enaka

---

#### 10. Profil uporabnika
**Glavni namen:** Prikazati osebne podatke uporabnika in statistiko uporabe.

**Akcije uporabnika:**
- Pregleda osebne podatke (ime, email)
- Vidi statistiko:
  - Skupni prihranki
  - Število spremljanih izdelkov
  - Število obvestil (ta mesec)
  - Najboljši prihranek (izdelek)
- Klikne "Uredi profil" → Uredi ime, profilno sliko
- Klikne "Premium" → Navigacija na Premium upgrade (če je free tier)
- Klikne "Nastavitve" → Navigacija na Nastavitve

**Navigacija:**
- Nazaj na Dashboard
- Link na Nastavitve

---

#### 11. Nastavitve
**Glavni namen:** Konfiguracija računa, obvestil in preferenc.

**Akcije uporabnika:**
- **Obvestila:**
  - Vklop/izklop push obvestil
  - Vklop/izklop email obvestil
  - (Premium) Vklop/izklop SMS obvestil
  - Nastavi čas tišine (ne moti)
- **Račun:**
  - Spremeni email
  - Spremeni geslo
  - Izbriši račun
- **Preference:**
  - Izbere valuto (EUR, USD, GBP...)
  - Izbere jezik
  - Tema (svetla/temna)
- **Premium:**
  - Pregled Premium funkcij
  - Upgrade/Cancel subscription
- **Zasebnost:**
  - Prenesi podatke
  - Izbris podatkov (GDPR)

**Navigacija:**
- Nazaj na Profil ali Dashboard
- Top bar navigacija ostane enaka

---

#### 12. Premium Upgrade
**Glavni namen:** Prikazati prednosti Premium računa in omogočiti upgrade.

**Akcije uporabnika:**
- Primerja Free vs Premium funkcije (tabela)
- Izbere način plačila (mesečno €4,99 / letno €49)
- Klikne "Upgrade na Premium" → Plačilni proces (Stripe/PayPal)
- Klikne "Nadaljuj z brezplačno verzijo" → Navigacija nazaj

**Navigacija:**
- Nazaj na Profil ali Dashboard

---

### 3️⃣ UI postavitev (razpored elementov)

#### 1. Vstopna stran (Landing Page)

**Header:**
- Logo (levo)
- Navigacija: Funkcije, Cene, O nas (desno)
- Gumba: "Prijavi se" | "Začni brezplačno" (CTA, barven)

**Hero sekcija:**
- Naslov: "Nikoli več ne zamudi najboljše akcije pri nakupovanju mode"
- Podnaslov: "Centralno spremljaj cene izdelkov iz vseh EU trgovin in prejmi instant obvestila o akcijah."
- Ilustracija/slika aplikacije (mockup)
- CTA gumb: "Začni brezplačno"
- Dodatno: "Brez kreditne kartice potrebne"

**Features sekcija (3-4 kartice):**
- Ikona + naslov + kratki opis za vsako funkcionalnost:
  1. "Avtomatsko spremljanje cen" - Dodaj izdelek, mi spremljamo
  2. "Instant obvestila" - Mobile push, ko se sproži akcija
  3. "Zgodovina cen" - Vedno veš, ali je dobra ponudba
  4. "Organizacija po seznamih" - Vse na enem mestu

**Social Proof:**
- Statistika: "3,000+ uporabnikov" | "€150 avg. prihranki/leto" | "10+ podprtih trgovin"

**Pricing teaser:**
- Free tier: Do 10 izdelkov, osnovne funkcije
- Premium: Neomejeno, instant checks, prioritetna podpora
- CTA: "Začni brezplačno"

**Footer:**
- O nas | Kontakt | Pogoji uporabe | Politika zasebnosti
- Social media ikone
- Newsletter signup

---

#### 2. Prijava (Login)

**Layout (centroid, minimalistično):**
- Logo (top center)
- Naslov: "Dobrodošel nazaj"
- Vnosno polje: Email (ikona @)
- Vnosno polje: Geslo (ikona ključavnica, gumb za prikaz/skrij)
- Checkbox: "Zapomni si me"
- Primarni gumb: "Prijavi se"
- Link: "Pozabljeno geslo?"
- Divider: "ALI"
- Sekundarni gumbi: "Nadaljuj z Google" | "Nadaljuj z Facebook"
- Besedilo + Link: "Nisi član? Registriraj se"

---

#### 3. Registracija (Sign Up)

**Layout (centroid):**
- Logo (top center)
- Naslov: "Ustvari račun"
- Vnosno polje: Ime in priimek
- Vnosno polje: Email
- Vnosno polje: Geslo (z indikatorjem moči gesla)
- Checkbox: "Sprejemam pogoje uporabe in politiko zasebnosti"
- Primarni gumb: "Ustvari račun"
- Divider: "ALI"
- Sekundarni gumbi: "Nadaljuj z Google" | "Nadaljuj z Facebook"
- Besedilo + Link: "Že imaš račun? Prijavi se"

---

#### 4. Domača stran (Dashboard)

**Top bar:**
- Logo (levo)
- Iskanje (center)
- Ikona obvestil z badge številom (desno)
- Avatar uporabnika (desno)

**Glavni del (scrollable):**

**Alert banner (če obstajajo aktivna obvestila):**
- "🎉 3 izdelki so na akciji! - Poglej zdaj"

**Stats sekcija (horizontal kartice):**
- Kartica 1: "Prihranki ta mesec: €47"
- Kartica 2: "Spremljanih izdelkov: 23"
- Kartica 3: "Premium: Upgrade" (ali status Premium)

**Wishlist seznami sekcija:**
- Naslov: "Moji seznami"
- Kartica "+ Nov seznam"
- Kartica za vsak seznam:
  - Ime seznama
  - Število izdelkov
  - Preview slike (3-4 izdelki)
  - Quick action ikone (uredi, deli, izbriši)

**Najnovejša obvestila sekcija:**
- Naslov: "Najnovejša obvestila" + "Prikaži vse" link
- Seznam zadnjih 5 obvestil:
  - Slika izdelka
  - Naslov obvestila
  - Časovna značka
  - Akcijska ikona (%)

**Floating action button (FAB):**
- "+" ikona za dodajanje novega izdelka (spodaj desno)

**Bottom navigation bar (mobile):**
- Ikone: Domov (aktiven) | Wishlists | Dodaj | Obvestila | Profil

---

#### 5. Wishlist seznami

**Header:**
- Nazaj gumb (levo)
- Naslov seznama (center)
- Ikone: Uredi, Deli, Izbriši (desno)

**Filter bar:**
- Chips: "Vsi" | "Na akciji" | "Ciljna cena dosežena" | "Razprodano"

**Sort dropdown:**
- "Razvrsti po: Datum dodajanja ↓"

**Izdelki (grid/list):**
- Vsak izdelek:
  - Slika izdelka
  - Naslov izdelka
  - Trgovina (logo)
  - Trenutna cena (velika)
  - Prejšnja cena (prečrtano, če je popust)
  - % popusta badge (če obstaja)
  - Trend ikona (↓ padajoča cena, ↑ naraščajoča)
  - Quick actions (opcijski): Uredi pravila, Izbriši

**FAB:**
- "+ Dodaj izdelek"

**Bottom navigation bar (mobile):**
- Enako kot Dashboard

---

#### 6. Dodaj izdelek

**Header:**
- Nazaj gumb (levo)
- Naslov: "Dodaj izdelek" (center)

**Main form:**
- **Step 1: URL Input**
  - Vnosno polje: "Prilepi URL izdelka"
  - Gumb: "Pridobi podatke"
  - Loading spinner med parsanjem

- **Step 2: Pregled in urejanje**
  - Preview slika izdelka
  - Vnosno polje: Ime izdelka (editable)
  - Read-only: Trgovina (logo + ime)
  - Read-only: Trenutna cena
  - Dropdown: Izberi wishlist
  - Toggle: "Nastavi pravila obveščanja"

- **Step 3: Pravila obveščanja (če vklopljeno)**
  - Radio buttons:
    - "Obvestilo pri ciljni ceni" → Vnosno polje (npr. "50")
    - "Obvestilo pri % popustu" → Vnosno polje (npr. "30")
    - "Obvestilo pri ponovni razpoložljivosti" (checkbox)

- **Gumbi:**
  - Primarni: "Dodaj v wishlist"
  - Sekundarni: "Prekliči"

---

#### 7. Podrobnosti izdelka

**Header:**
- Nazaj gumb (levo)
- Naslov: Ime izdelka (center, skrajšano)
- Ikone: Deli, Izbriši (desno)

**Glavni del (scrollable):**

**Izdelek info:**
- Velika slika izdelka
- Ime izdelka (polni naslov)
- Trgovina (logo + link)
- Trenutna cena (prominenten font)
- Prejšnja cena (če obstaja)
- % popusta badge
- Razpoložljivost status
- Gumb: "Obišči trgovino" (CTA)

**Zgodovina cen:**
- Tab buttons: 30 dni | 60 dni | 90 dni
- Line chart (cena preko časa)
- Najnižja/najvišja cena označena

**Pravila obveščanja:**
- Kartica:
  - "Obvestilo pri ceni pod €50" ✓
  - "Obvestilo pri >30% popustu" ✓
  - Gumb: "Uredi pravila"

**Dodatne akcije:**
- "Premakni v drug seznam" (dropdown)
- "Izbriši iz wishlist-a"

---

#### 8. Iskanje trgovin

**Header:**
- Nazaj gumb (levo)
- Naslov: "Podprte trgovine" (center)

**Iskanje:**
- Vnosno polje: "Išči trgovino..."

**Filter:**
- Dropdown: "Vse države" | "Slovenija" | "Nemčija" | "Avstrija" | ...

**Grid trgovin:**
- Vsaka trgovina:
  - Logo (kvadratna kartica)
  - Ime trgovine
  - Število spremljanih izdelkov iz te trgovine

**Bottom gumb:**
- "Predlagaj novo trgovino"

---

#### 9. Obvestila

**Header:**
- Nazaj gumb (levo)
- Naslov: "Obvestila" (center)
- Ikona: Označi vse kot prebrane (desno)

**Filter tabs:**
- "Vsa" | "Neprebrana" | "Akcije" | "Razpoložljivost"

**Seznam obvestil:**
- Vsako obvestilo:
  - Slika izdelka (levo)
  - Vsebina:
    - Naslov obvestila (npr. "Cena padla za 35%!")
    - Ime izdelka
    - Nova cena
    - Časovna značka
  - Barvni indicator (neprebrano - točka)
  - Swipe actions: Izbriši

---

#### 10. Profil uporabnika

**Header:**
- Nazaj gumb (levo)
- Naslov: "Profil" (center)

**User info:**
- Profilna slika (center)
- Ime in priimek
- Email
- Gumb: "Uredi profil"

**Premium status:**
- Badge: "Free tier" ali "Premium ⭐"
- (Če Free) Gumb: "Nadgradi na Premium"

**Statistika (kartice v grid):**
- "Skupni prihranki: €347"
- "Spremljanih izdelkov: 23"
- "Obvestil ta mesec: 47"
- "Najboljši prihranek: €89 (Nike jakna)"

**Nastavitve in akcije:**
- Link: "Nastavitve"
- Link: "Pomoč in podpora"
- Link: "Odjavi se"

---

#### 11. Nastavitve

**Header:**
- Nazaj gumb (levo)
- Naslov: "Nastavitve" (center)

**Sekcije (grouped list):**

**Obvestila:**
- Toggle: "Push obvestila"
- Toggle: "Email obvestila"
- Toggle: "SMS obvestila" (Premium only - lock ikona)
- Time picker: "Čas tišine: 22:00 - 8:00"

**Račun:**
- Link: "Spremeni email"
- Link: "Spremeni geslo"
- Link: "Izbriši račun" (rdeče)

**Preference:**
- Dropdown: "Valuta: EUR"
- Dropdown: "Jezik: Slovenščina"
- Toggle: "Temna tema"

**Premium:**
- Link: "Upravljaj naročnino" (če Premium)
- Link: "Nadgradi na Premium" (če Free)

**Zasebnost:**
- Link: "Prenesi moje podatke"
- Link: "Izbriši moje podatke"
- Link: "Politika zasebnosti"

---

#### 12. Premium Upgrade

**Header:**
- Nazaj gumb (levo)
- Naslov: "Premium" (center)

**Hero:**
- Ikona/ilustracija Premium
- Naslov: "Nadgradi na Premium"
- Podnaslov: "Prihrani več, hitreje."

**Comparison table:**
| Funkcija | Free | Premium |
|----------|------|---------|
| Številu izdelkov | 10 | Neomejeno |
| Price checks | 1x/dan | 4x/dan |
| Obvestila | Email + Push | Email + Push + SMS |
| Zgodovina cen | 30 dni | 90 dni |
| Prioritetna podpora | ❌ | ✓ |

**Pricing cards:**
- Kartica 1: "Mesečno €4,99" (gumb: "Izberi")
- Kartica 2: "Letno €49" (badge: "Prihrani 18%", gumb: "Izberi")

**Testimonials:**
- 2-3 kratke reference Premium uporabnikov

**FAQ:**
- "Kdaj lahko prekličem?"
- "Kako deluje plačilo?"

**CTA:**
- Primarni gumb: "Nadgradi zdaj"
- Link: "Nadaljuj z brezplačno verzijo"

---

### 4️⃣ Prompt za "Stitch Google" osnovne funkcije

Na podlagi zgornje UX/UI zasnove, tukaj so **prompts** za izdelavo osnovnih strani aplikacije z AI orodji (npr. ChatGPT, Claude, Cursor):

---

#### 📝 Prompt 1: Homepage (Landing Page)

```
Naredi mi popolnoma funkcionalno HTML/CSS/JS landing page za aplikacijo za spremljanje cen modnih izdelkov. 

**Zahteve:**
- Modern, clean dizajn z gradient background (oranžna/vijolična)
- Hero sekcija z naslovom "Nikoli več ne zamudi najboljše akcije pri nakupovanju mode"
- Podnaslov in CTA gumb "Začni brezplačno"
- Features sekcija s 4 karticami (ikone Font Awesome):
  1. Avtomatsko spremljanje cen
  2. Instant obvestila
  3. Zgodovina cen
  4. Organizacija po seznamih
- Stats sekcija: "3,000+ uporabnikov | €150 avg. prihranki | 10+ trgovin"
- Pricing teaser (Free vs Premium)
- Responsive design (mobile-first)
- Smooth scroll animacije

**Tehnologije:**
- Vanilla HTML/CSS/JavaScript (brez frameworkov)
- Font Awesome za ikone
- Google Fonts (Inter ali Poppins)
```

---

#### 📝 Prompt 2: Izdelek - Podrobnosti (Product Detail Page)

```
Naredi mi funkcionalno stran za prikaz podrobnosti izdelka za price tracking aplikacijo.

**Zahteve:**
- Header z nazaj gumbom in naslovom izdelka
- Hero sekcija:
  - Velika slika izdelka (placeholder)
  - Ime izdelka
  - Logo trgovine
  - Trenutna cena (velik, bold font)
  - Prejšnja cena (prečrtano)
  - % popusta badge (zeleni)
  - "Obišči trgovino" CTA gumb
- Zgodovina cen sekcija:
  - Tab buttons: 30 / 60 / 90 dni
  - Line chart (uporabi Chart.js)
  - Mock podatki: cene zadnjih 30 dni
- Pravila obveščanja:
  - Kartica z aktivnimi pravili
  - Checkbox elementi: "Obvestilo pri €50", "Obvestilo pri >30% popustu"
  - "Uredi pravila" gumb
- Bottom actions: "Premakni v drug seznam", "Izbriši izdelek"
- Responsive design

**Tehnologije:**
- HTML/CSS/JavaScript
- Chart.js za graf (CDN)
- Font Awesome za ikone
```

---

#### 📝 Prompt 3: Profil in nastavitve (Profile & Settings)

```
Naredi mi dve povezani strani: Profil uporabnika in Nastavitve za price tracking aplikacijo.

**Profil stran:**
- Header: Avatar, ime, email
- Premium status badge
- Statistika v 2x2 grid:
  - Skupni prihranki
  - Spremljanih izdelkov
  - Obvestil ta mesec
  - Najboljši prihranek
- Gumbi: "Uredi profil", "Nadgradi na Premium" (če Free)
- Navigacija na Nastavitve

**Nastavitve stran:**
- Grouped list dizajn (iOS style)
- Sekcije:
  1. Obvestila (3 toggle switches: Push, Email, SMS)
  2. Račun (linki: Spremeni email, Spremeni geslo, Izbriši račun)
  3. Preference (dropdowns: Valuta, Jezik, Toggle: Temna tema)
  4. Premium (link: Upravljaj naročnino)
  5. Zasebnost (linki: Prenesi/Izbriši podatke)
- Mobile-first design
- Toggle switches z animacijo

**Tehnologije:**
- HTML/CSS/JavaScript
- CSS Grid za statistiko
- Toggle switches z custom CSS
- Responsive design
```

---

#### 📝 Bonus Prompt: Dashboard (Home Page)

```
Naredi mi glavni dashboard za price tracking aplikacijo z vsemi funkcionalnostmi.

**Zahteve:**
- Top navigation bar:
  - Logo
  - Search bar
  - Obvestila ikona (badge s številom)
  - Avatar dropdown
- Alert banner: "3 izdelki na akciji!"
- Stats kartice (horizontal scroll):
  - Prihranki ta mesec
  - Spremljanih izdelkov
  - Premium status
- Wishlist seznami sekcija:
  - Grid kartic (responsive)
  - Vsaka kartica: ime, število izdelkov, preview slike
  - "+ Nov seznam" kartica
- Najnovejša obvestila:
  - Seznam 5 najnovejših
  - Vsako: slika, naslov, čas, akcijska ikona
  - "Prikaži vse" link
- Floating Action Button (FAB) za dodajanje izdelka
- Bottom navigation bar (mobile): 5 ikon

**Tehnologije:**
- HTML/CSS/JavaScript
- CSS Grid + Flexbox
- Mobile-first responsive
- Font Awesome ikone
```

---

### 🎨 UX/UI skice (tekstovni opisi)

Zaradi omejitev tekstovnega formata, prilagam tekstovne opise ključnih zaslonov:

#### Dashboard (ASCII mockup):
```
┌─────────────────────────────────────┐
│ [Logo]    [Search]    [🔔3] [👤]   │
├─────────────────────────────────────┤
│                                     │
│  🎉 3 izdelki na akciji! →         │
│                                     │
│  [€47]      [23]        [Premium]  │
│  Prihranki  Izdelkov    Upgrade    │
│                                     │
│  Moji seznami                       │
│  ┌─────┐ ┌─────┐ ┌─────┐          │
│  │ [+] │ │Zima │ │Sport│          │
│  │ Nov │ │ 12  │ │  7  │          │
│  └─────┘ └─────┘ └─────┘          │
│                                     │
│  Najnovejša obvestila        [Vse] │
│  • Nike jakna -35% | 2h            │
│  • Zara hlače nazaj na zalogi | 5h │
│  • Adidas copati €49 | 1d          │
│                                     │
└─────────────────────────────────────┘
│ [🏠] [📋] [➕] [🔔] [👤]          │
└─────────────────────────────────────┘
```

#### Podrobnosti izdelka (ASCII mockup):
```
┌─────────────────────────────────────┐
│ [←] Nike Air Max 90      [⋮]       │
├─────────────────────────────────────┤
│                                     │
│     ┌─────────────────────┐        │
│     │                     │        │
│     │   [Slika izdelka]   │        │
│     │                     │        │
│     └─────────────────────┘        │
│                                     │
│  Nike Air Max 90 White              │
│  [Nike logo] Nike.com               │
│                                     │
│  €79  €129  [-39%]                 │
│                                     │
│  [Obišči trgovino →]               │
│                                     │
│  Zgodovina cen                      │
│  [30d] [60d] [90d]                 │
│  ┌─────────────────────┐           │
│  │      📈             │           │
│  │    /\  /\           │           │
│  │   /  \/  \___       │           │
│  └─────────────────────┘           │
│                                     │
│  Pravila obveščanja                 │
│  ✓ Obvestilo pri €50               │
│  ✓ Obvestilo pri >30%              │
│  [Uredi pravila]                    │
│                                     │
│  [Premakni v drug seznam]          │
│  [Izbriši izdelek]                  │
│                                     │
└─────────────────────────────────────┘
```

#### Profil (ASCII mockup):
```
┌─────────────────────────────────────┐
│ [←] Profil                          │
├─────────────────────────────────────┤
│                                     │
│           [👤]                      │
│        Janez Novak                  │
│     janez@example.com               │
│                                     │
│     [Free tier] [Upgrade →]        │
│                                     │
│  ┌──────────┐ ┌──────────┐        │
│  │  €347    │ │    23    │        │
│  │Prihranki │ │ Izdelkov │        │
│  └──────────┘ └──────────┘        │
│  ┌──────────┐ ┌──────────┐        │
│  │    47    │ │   €89    │        │
│  │Obvestil  │ │Najboljši │        │
│  └──────────┘ └──────────┘        │
│                                     │
│  → Nastavitve                       │
│  → Pomoč in podpora                 │
│  → Odjavi se                        │
│                                     │
└─────────────────────────────────────┘
```

---

## ✅ Zaključek

Ta dokument vsebuje:
- ✅ Seznam vseh 12 zaslonov aplikacije
- ✅ UX strukturo za vsak zaslon (namen, akcije, navigacija)
- ✅ UI postavitev za vsak zaslon (elementi, gumbi, vsebina)
- ✅ Prompts za implementacijo osnovnih funkcij ("stitch google")
- ✅ ASCII mockups za vizualizacijo ključnih zaslonov

Aplikacija sledi modernim UX/UI principom:
- **Mobile-first design** - vse zaslon so optimizirani za mobilne naprave
- **Progressive disclosure** - informacije so razkrite postopoma
- **Jasna navigacija** - uporabnik vedno ve, kje je in kam lahko gre
- **Consistency** - enotni dizajn vzorci skozi celotno aplikacijo
- **Accessibility** - jasne ikone, berljiv font, dobri kontrasti
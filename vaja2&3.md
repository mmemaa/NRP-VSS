# VAJA 2 & 3 – Value Proposition, Product Vision in Business Model

## Namen vaj

- Prevesti realen problem specifičnega uporabnika v **jasno, merljivo vrednost**
- Oblikovati **produktno vizijo**, ki ni le slogan, ampak strateška definicija
- Preveriti, ali ima rešitev **poslovni smisel** (osnovni Business Model Canvas + ključne hipoteze)

Ključno pravilo:  
**Ne gradimo aplikacije – gradimo rešitev za konkretno frustracijo konkretnega uporabnika.**

---

## 2.1 Value Proposition Canvas (VPC)

### Customer Profile (Profil uporabnika)

**Izbrani segment:**  
Modni navdušenci in strateški nakupovalci oblačil v EU (starost 18–35 let), ki redno spremljajo več spletnih trgovin, iščejo najboljše ponudbe in želijo biti obveščeni o akcijah za specifične izdelke, ki jih zanimajo.

#### Pains (največje frustracije / bolečine)

- Ročno preverjanje cen pri več trgovcih → porabijo **3–5 ur na teden** za iskanje najboljših ponudb
- Zamujajo akcije in popuste, ker ne spremljajo vseh trgovin dovolj pogosto
- Nima centralnega sistema za organizacijo wishlist artiklov iz različnih trgovin
- Newsletter overload – preveč splošnih promocijskih emailov, premalo ciljnih obvestil
- Obstojača orodja so omejena na določene trgovce (npr. samo Amazon) ali ne delujejo dobro z EU lokalnimi trgovci
- Frustracija, ko izdelek razprodajo ali ko se cena zviša pred nakupom
- Težko sledijo zgodovini cen in ne vedo, ali je trenutna cena res ugodna

#### Gains (želene koristi / idealni izid)

- Takojšnja push obvestila na mobilni telefon, ko artikel doseže ciljno ceno ali dobi popust
- Vsi željeni izdelki iz različnih trgovin organizirani na enem mestu
- Prihranek vsaj 20–30 % pri nakupih zaradi pravočasnega ujemanja akcij
- Manj časa porabljenega za iskanje ponudb → več časa za uživanje v nakupovanju
- Transparency cen – vidijo zgodovino cen in vedo, kdaj je prava priložnost
- Možnost nastavitve lastnih pravil (npr. obvestilo pri >30% popustu ali ko cena pade pod 50€)

#### Jobs to be Done (opravila uporabnika)

- Spremljanje cen specifičnih modnih artiklov pri različnih trgovcih
- Organizacija wishlist artiklov po kategorijah (jakne, čevlji, dodatki)
- Odločanje, kdaj je pravi trenutek za nakup
- Odkrivanje najboljših ponudb brez pretirane porabe časa

### Value Map (Rešitev)

#### Pain Relievers (kako lajšamo bolečine)

- **Avtomatsko spremljanje cen** za vse dodane izdelke – uporabnik ne potrebuje več ročno preverjati
- **Instant mobile push obvestila** takoj, ko se sprožijo pravila (popust, ciljna cena, ponovna razpoložljivost)
- **Unificirani wishlist** za izdelke iz poljubnih EU trgovcev – vsi artikli na enem dashboard-u
- **Pametna filtriranja obvestil** – uporabnik dobi samo relevantna obvestila glede na svoja pravila, ne spam-a
- **Podpora za lokalne EU trgovce** – ne samo veliki igralci, ampak tudi regionalne spletne trgovine
- **History tracking** – graf zgodovine cen za vsak artikel, da uporabnik vidi trende

#### Gain Creators (kako ustvarjamo dodatne koristi)

- **Personalizirana pravila obveščanja** – uporabnik nastavi % popusta ali absolutno ceno
- **Organizacija po seznamih** – kategorije (zima 2026, poletje, posebne priložnosti)
- **Prioritetno spremljanje** – premium uporabniki dobijo pogostejše checks in hitrejša obvestila
- **Affiliate integracija** – neposredne povezave do izdelkov z možnostjo takojšnjega nakupa
- **Analitika prihrankov** – aplikacija prikaže, koliko je uporabnik prihranil z akcijami
- **Collaborative wishlist** – možnost delitve seznamov z družino/prijatelji (npr. za darila)

#### Products & Services (funkcionalnosti)

- **Web aplikacija** s PWA podporo za mobile push
- **Browser extension** za enostavno dodajanje izdelkov z URL
- **Email digest** (opcijsko) – tedenski pregled akcij
- **Premium tier** z instant checks, SMS obvestili in neomejenim številom artiklov

---

## 2.2 Product Vision Statement

**Za** modne navdušence in strateške nakupovalce v EU,  
**ki** porabljajo preveč časa za ročno spremljanje cen pri različnih trgovcih in pogosto zamujajo najboljše akcije,  
**je naš produkt** inteligentna spletna aplikacija za centralizirano spremljanje izdelkov in instant obveščanje o cenah,  
**ki** omogoča uporabnikom, da prihranijo vsaj 20–30 % pri nakupih mode in 3–5 ur tedensko, ki bi jih sicer porabili za iskanje ponudb,  
**za razliko od** obstoječih orodij (Karma, Honey, Distill.io), ki so globalno usmerjeni in ne pokrivajo dobro lokalnih EU trgovcev ter nimajo granularnih pravil obveščanja in organizacije wishlistov.

**Naša diferenciacija:**  
- Fokus na EU trg in regionalne trgovce  
- Granularna pravila obveščanja (%, absolutna cena, ponovna razpoložljivost)  
- Mobile-first pristop z instant push obvestili  
- Organizacija po uporabniških seznamih in kategorijah  

---

## 3.1 Business Model Canvas (osredotočeni 4 elementi)

| Element              | Opis                                                                                   |
|----------------------|----------------------------------------------------------------------------------------|
| **Customer Segments** | **Primarni segment:** Mladi odrasli (18–35 let) v EU, modni navdušenci, študenti in mladi profesionalci z omejenim proračunom<br>**Sekundarni segment:** Lokalne in regionalne spletne trgovine, ki želijo ciljano obveščati zainteresirane kupce<br>**B2C model** – končni uporabniki; možnost **B2B2C** – partnerstva s trgovci |
| **Value Proposition** | **Za uporabnike:** 20–30 % prihrankov pri nakupih mode + 3–5 ur tedensko prihranjenega časa za iskanje ponudb<br>**Za trgovce:** Kanal za ciljano obveščanje zainteresiranih kupcev o akcijah in posebnih ponudbah |
| **Revenue Streams**   | **Freemium model:**<br>- Brezplačno: spremljanje do 10 artiklov, daily price checks, email obvestila<br>- Premium (€4,99/mesec ali €49/leto): neomejeno artiklov, instant checks (4x/dan), mobile push, SMS, prioritetna podpora<br>**Affiliate prihodki:** provizija pri posredovanju kupcev trgovcem (2–10 % od prodaje)<br>**B2B licenciranje:** trgovci plačajo za white-label widget ali integracije (€99–499/mesec) |
| **Cost Structure**    | **Razvoj:** Backend scraping infrastructure, worker queues, mobile push sistem (~40 %)<br>**Infrastruktura:** Cloud hosting, proxy services, headless browsers, rate limiting (~25 %)<br>**Operativa:** Vzdrževanje shop connectors, API integracije, anti-bot handling (~20 %)<br>**Marketing:** Social media ads (Instagram, TikTok), influencer partnerships (~10 %)<br>**Podpora:** Customer success, GDPR compliance (~5 %) |

**Ključno ekonomsko vprašanje:**  
Če uporabnik prihrani €100–200/leto z boljšimi nakupi in 150+ ur letno časa, je €49/leto (ali €4,99/mesec) zelo dostopna naložba. Break-even ob približno 5.000 premium uporabnikih + affiliate prihodki.

---

## 3.2 Ključne poslovne hipoteze (top 5)

1. **Uporabniki so pripravljeni plačevati €4,99/mesec** za orodje, ki jim zanesljivo prinaša vsaj €15–20 prihrankov mesečno pri nakupih.  
   → **Test:** Landing page z prednaročili, intervjuji z 30+ potencialnimi uporabniki, A/B testiranje cenovnih točk

2. **Največja bolečina je zamujanje akcij in poraba časa, ne pomanjkanje wishlist funkcionalnosti nasploh.**  
   → **Test:** Vprašalnik 100+ uporabnikom (rangiranje frustracij), analiza konkurenčnih review-jev (Reddit, Trustpilot)

3. **Uporabniki bodo aktivno uporabljali aplikacijo vsaj 2× tedensko**, če bodo obvestila dovolj natančna (>85 % accuracy) in relevantna.  
   → **Test:** Beta testiranje z 200 uporabniki, merjenje retention (7-day, 30-day), engagement metrics

4. **Affiliate konverzija bo vsaj 5–8 %** – uporabniki, ki dobijo obvestilo, bodo kliknili in kupili pri trgovcu.  
   → **Test:** Pilot s 3–5 trgovci, sledenje CTR in conversion rate iz obvestil

5. **EU lokalni trgovci so pripravljeni sodelovati** (API/feed dostop ali B2B licenca), če jim to prinaša ciljano publiko.  
   → **Test:** Pogovori z 10–15 lokalnimi trgovci, pilotno partnerstvo z 2–3 trgovci

---

## 3.3 Go-to-Market strategija (ključni elementi)

### Začetni segmenti (MVP)
- **Geografija:** Slovenija, Avstrija, Nemčija (testni trgi z dobro spletno infrastrukturo)
- **Kategorija:** Moda (oblačila, obutev, dodatki)
- **Trgovci:** 5–10 največjih lokalnih + mednarodnih trgovcev (Zalando, ASOS, About You, H&M + lokalni igralci)

### Pridobivanje uporabnikov
- **Social media marketing:** Instagram, TikTok ads – targeting fashion enthusiasts
- **Influencer partnerships:** Mikro-influencerji v modi (10k–100k sledilcev)
- **Content marketing:** Blog z nasveti za pametno nakupovanje, seasonal guides
- **Referral program:** "Povabi prijatelja" – oba dobita 1 mesec premium brezplačno

### Merjenje uspeha (KPIs)
- **Število aktivnih uporabnikov** (daily/monthly active users)
- **Retention rate:** 7-day, 30-day, 90-day
- **Notification CTR:** % uporabnikov, ki klikne obvestilo
- **Conversion rate:** % klikov, ki vodijo do nakupa (affiliate tracking)
- **Premium conversion rate:** % free → premium uporabnikov
- **Average time saved:** ocena prihranjenih ur na uporabnika (survey)
- **Average savings:** dejanski prihranki pri nakupih (tracker)

---

## Naslednji koraki

1. **Validacija hipotez** (intervjuji z 30+ potencialnimi uporabniki, landing page MVP)
2. **Pilot s 5 trgovci** (pogajanja za API dostop ali dovoljenje za scraping)
3. **MVP razvoj** – web app + basic scraping + email/push notifications za 1–2 kategorije
4. **Beta testiranje** z 200 uporabniki (merjenje engagement, retention, CTR)
5. **Iteracija VPC in BMC** glede na povratne informacije iz beta testiranja
6. **Pravna validacija** (GDPR compliance, scraping ToS, affiliate agreements)
7. **Scale strategija** – dodatne kategorije, države, trgovci

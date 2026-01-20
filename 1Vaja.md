# Vaja 1 — Identifikacija kompleksnega problema in tržne priložnosti

Tema  
Spletna aplikacija za spremljanje izdelkov iz spletnih trgovin (osredotočeno na modo) z unificirano wishlist funkcionalnostjo: uporabnik doda izdelek iz poljubnega trgovca v EU, aplikacija spremlja ceno, razpoložljivost in promocije ter pošilja takojšnja obvestila (mobile push + email). Vsi izdelki so organizirani po seznamih/kategorijah in uporabniških pravilih (npr. ob >30 % popustu ali ko cena pade pod ciljno vrednost).

---

## 1. Problem Statement

Kontekst  
- Spletna modna prodaja v EU raste; potrošniki pogosto spremljajo več trgovcev (lokalnih in mednarodnih) za iskanje najboljših ponudb.  
- Trgovci oglašujejo popuste v različnih kanalih (splet, newsletter, lokalne strani), vendar je ročno spremljanje več izdelkov pri več trgovcih zamudno in neučinkovito.

Koga problem zadeva  
- Potrošniki mode v EU (mladi odrasli, pri katerih so impulzni nakupi in omejeni proračuni pogosti).  
- Kupci, ki želijo slediti specifičnim artiklom (npr. kos nakita, jakna, teniske) pri različnih verigah.  
- Mala/ regionalna spletna trgovina, ki želi bolj izpostaviti posebne ponudbe.

Natančen problem  
- Ni enotnega, enostavnega orodja, ki bi omogočalo centralno upravljanje seznamov želja prek različnih trgovcev v EU in ki bi zagotavljalo zanesljiva, instantna potrošniška obvestila (mobile push) glede akcij, posebnih ponudb ali obnove zalog. Obstoječa orodja so pogosto omejena na enega velikega prodajalca (npr. Amazon trackers), so globalno usmerjena in ne pokrivajo dobro lokalnih trgovcev ali specifičnih pravil obveščanja.

Posledice, če problem ostane nerešen  
- Potrošniki zamujajo priložnosti za prihranek; poraba časa in frustracija zaradi ročnega preverjanja.  
- Trgovci, zlasti lokalni, izgubijo kanale za ciljano izpostavitev akcij zainteresiranim kupcem.  
- Tržna razpoka za orodje, ki bi združevalo UX (wishlist management), natančne obvestilne mehanizme in lokalno pokritost, ostaja neizkoriščena.

Zakaj gre za večplasten (multidisciplinaren) problem  
- Tehnični izzivi: robustno spremljanje (scraping vs. API), produktna identifikacija med trgovci (fuzzy match), skalabilnost, reliability in notifikacijski sistemi (push).  
- Pravni/etični vidiki: skladnost z GDPR, pravila glede scraping-a in Terms of Service trgovcev.  
- Poslovni vidiki: monetizacija (freemium, affiliate, B2B), partnerstva s trgovci.  
- UX in produkt: enostavno dodajanje izdelkov, upravljanje seznamov, upravljanje false-positives obvestil in upravljanje zaupanja uporabnikov.

---

## 2. Market Research (ključne številke in utemeljitev)

Glavni tržni signali (EU, moda, spletna prodaja)
- E‑commerce penetracija v EU: velik delež prebivalstva redno nakupuje preko spleta — to ustvarja bazo uporabnikov, ki izkoriščajo spletne ponudbe in popuste. (Vir: Eurostat)  
  Vir: Eurostat — e‑commerce statistics (podatki o deležu posameznikov, ki kupujejo preko spleta)  
  https://ec.europa.eu/eurostat

- Velikost evropskega spletnega modnega trga: spletna moda je ena največjih kategorij v e‑commerce - v Evropi gre za desetine milijard EUR letne prodaje (trendi rasti e‑commerce in mode opredeljujejo zanimanje potrošnikov za ceno in promocije). (Vir: Statista / McKinsey State of Fashion)  
  - Statista — Fashion e‑commerce market (evropske številke in napovedi).  
    https://www.statista.com
  - McKinsey & Business of Fashion — The State of Fashion (trend rasti e‑commerce v modni industriji).  
    https://www.mckinsey.com/featured-insights

- Uporabniško vedenje in obveščanje: smartphone penetracija in navada uporabe push notifikacij omogočata visoke stopnje angažiranosti pri takih obvestilih; web aplikacija z mobile push (PWA + web push) je primeren prvi korak. (Vir: GSMA / Eurostat mobilna uporaba)

Konkurenca in priložnost za diferenciranje
- Obstajajo izdelki, ki deloma prekrivajo funkcionalnost:
  - Karma (prej Shoptagr) — wishlist + obvestila za različne trgovine (globalno) — https://karma.com/  
  - Honey — kuponi & popusti (posebnosti pri checkout) — https://www.joinhoney.com/  
  - Distill.io / Visualping — univerzalno spremljanje sprememb strani (generično, ne UX-oriented wishlist) — https://distill.io/  
- Te rešitve pogosto ne pokrivajo specifične EU/regionalne trgovinske pokritosti, nimajo granularnih pravil obveščanja ali močnih možnostih organizacije seznamov po uporabniških pravilih in prioritetah — to je priložnost za diferenciranje.

Poslovni potencial
- Monetizacija: freemium (omejeno število spremljanih artiklov), premium (instant push, SMS), affiliate prihodki ob posredovanju kupcev, B2B licenciranje za trgovce (white‑label widgets). Affiliate programi so v e‑commerce uveljavljena monetizacijska pot (Vir: Awin / CJ).  
  - Primer affiliate networks: Awin, CJ Affiliate — https://www.awin.com

Podatki za validacijo (predlog KPIjev)
- % uporabnikov, ki dodajo vsaj 5 artiklov v prvem tednu,  
- stopnja konverzije iz obvestila v klik na trgovca (CTR obvestil),  
- število uspešnih obvestil (dejanski popusti ujemeni s pravili),  
- zadržanje uporabnikov (30‑dnevni retention) — KPI za freemium model.

Viri (vsaj 3 verodostojne reference)
1. Eurostat — e‑commerce statistics (podatki o internetnih nakupih v EU).  
   https://ec.europa.eu/eurostat

2. Statista — Fashion e‑commerce market in Europe; e‑commerce growth statistics.  
   https://www.statista.com

3. McKinsey & Company / Business of Fashion — The State of Fashion (trend rasti spletne prodaje in potrošniškega vedenja).  
   https://www.mckinsey.com/featured-insights

4. GDPR & EU data protection — pristope za skladnost pri obdelavi uporabniških podatkov.  
   https://gdpr.eu

5. Primeri konkurentov/benchmark: Karma, Honey, Distill.io.  
   - https://karma.com/  
   - https://www.joinhoney.com/  
   - https://distill.io/

---

## 3. Tehnični pregled, pravni izzivi in MVP

Tehnični izzivi (ključni)
- Product matching: isti izdelek pri različnih trgovcih lahko nima istega SKU → potreben fuzzy matching (naslovi, slike, opis), opcijsko image‑based matching ali sodelovanje preko trgovskih feedov/APIjev.  
- Stabilno spremljanje: trgovine spreminjajo HTML in imajo anti‑bot zaščite → kombinacija metod: trgovinski API/feeds (če so na voljo), selektivni headless browser scraping, rotacija proxyjev, rate limiting in cache layer.  
- Skalabilnost: worker queue (npr. Redis + Celery / Sidekiq), scheduler za pogoste/priority checks, event system za instant notifikacije.  
- Notifikacije: web push (VAPID), mobile push (PWA + service workers) in email; podpora za SMS kot premium opcija.

Pravni in etični izzivi
- Scraping Terms of Service in intelektualna lastnina — politikam trgovcev je treba slediti; za dolgoročno rešitev je priporočljivo vzpostaviti partnerstva ali uporabiti javne APIje/trgovinske feed‑e.  
- GDPR: pravilna obdelava osebnih podatkov, soglasje za obvestila, enostavna možnost izbrisa (right to be forgotten), varnost shranjenih podatkov.

MVP feature set (web app, moda, mobile push)
- Uporabniški račun + osnovni dashboard za sezname (wishlist folders).  
- Dodajanje izdelka z URL (parsanje strani ali ročni vnos) in možnost nastavitev pravila obveščanja (ciljna cena, % popusta).  
- Periodično preverjanje (worker) + history price log.  
- Mobile web push notifikacije + email obvestila.  
- Enostaven admin za upravljanje shop connectors in rate limits.  
- Logika za prioritete: instant checks za premium uporabnike.

Metrike uspeha in pilot
- Pilot na 5–10 večjih EU modnih trgovcev + 200 beta uporabnikov iz treh držav. KPI: % obvestil, CTR, conversion-to-affiliate, retention.

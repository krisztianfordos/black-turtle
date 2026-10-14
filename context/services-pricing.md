# Services and pricing

Last verified: 2026-10-14

## Sources
- https://blackturtlesalon.salonic.hu/services (Salonic booking site, scraped into `content/services.json`)
- `content/services.json` (full scraped list, 30 entries = 10 services × 3 stylist levels)
- `content/salon-facts.md` (English glosses of service names; price cross-check)

## Notes
- Currency: HUF. Values are copied from `content/services.json` (raw value 7000 is shown as "7 000 HUF").
- Duration strings are copied verbatim from `content/services.json` (Hungarian: "perc" = minutes, "óra" = hour).
- Prices are indicative (Salonic booking policy, see `context/booking-policy.md`).
- Name variant: `services.json` spells the Stylist-level "Gépi egy hossz hajvágás" as "Gépi egy hossz hájvágás" (with á). All other entries, and `salon-facts.md`, use "hajvágás". Copied verbatim; likely a typo, confirm with the salon before publishing.
- Level names are uppercase in the JSON (JUNIOR STYLIST, STYLIST, SENIOR STYLIST); shown here in title case. Level meanings are in `context/team.md`.

## Overview

| # | Service (HU) | English (gloss) | Junior Stylist | Stylist | Senior Stylist |
|---|---|---|---|---|---|
| 1 | Basic hajvágás | Basic haircut (no skin fade) | 7 000 HUF · 40 perc | 7 500 HUF · 40 perc | 8 000 HUF · 30 perc |
| 2 | Basic hajvágás & szakáll igazítás | Basic haircut & beard trim | 10 000 HUF · 1 óra 10 perc | 11 000 HUF · 1 óra 10 perc | 12 000 HUF · 1 óra |
| 3 | Gépi egy hossz hajvágás | Single-length clipper cut | 4 000 HUF · 20 perc | 4 500 HUF · 20 perc | 5 000 HUF · 20 perc |
| 4 | Gépi egy hossz hajvágás & szakáll igazítás | Clipper cut & beard trim | 7 500 HUF · 45 perc | 8 000 HUF · 45 perc | 8 500 HUF · 45 perc |
| 5 | Gyerek hajvágás | Kids' cut (up to 12) | 6 000 HUF · 40 perc | 6 500 HUF · 40 perc | 7 000 HUF · 30 perc |
| 6 | Hosszú hajvágás | Long haircut (scissors only) | 8 000 HUF · 1 óra | 9 000 HUF · 1 óra | 10 000 HUF · 1 óra |
| 7 | Hosszú hajvágás & szakáll igazítás | Long haircut & beard trim | 11 000 HUF · 1 óra 30 perc | 12 500 HUF · 1 óra 30 perc | 14 000 HUF · 1 óra 30 perc |
| 8 | Skinfade hajvágás | Skin fade | 8 000 HUF · 1 óra | 9 000 HUF · 1 óra | 10 000 HUF · 1 óra |
| 9 | Skinfade hajvágás & szakáll igazítás | Skin fade & beard trim | 11 000 HUF · 1 óra 30 perc | 12 500 HUF · 1 óra 30 perc | 14 000 HUF · 1 óra 30 perc |
| 10 | Szakáll igazítás | Beard trim | 5 000 HUF · 30 perc | 5 500 HUF · 30 perc | 6 000 HUF · 30 perc |

Each cell: price · duration.

## Full descriptions (Hungarian, verbatim)

### 1. Basic hajvágás — Basic haircut (no skin fade)

**All levels:**

NEM SKINFADE hajvágás, klasszikus és letisztult fazonok készítésére szolgál. A szolgáltatás egy rövid konzultációval kezdődik, ahol a borbély a vendég igényeihez igazítja a kívánt stílust. A hajvágás után a finish a vendég által választott prémium termékkel történik a tökéletes megjelenés érdekében.

### 2. Basic hajvágás & szakáll igazítás — Basic haircut & beard trim

**All levels:**

NEM SKINFADE, klasszikus hajvágást és precíz szakállformázást tartalmaz. A kezelés konzultációval kezdődik, ahol a borbély a vendég stílusához igazítja a haj és szakáll végső megjelenését. A szolgáltatás finisheléssel zárul, a vendég által választott prémium haj- és szakállápoló termékek használatával.

### 3. Gépi egy hossz hajvágás — Single-length clipper cut

**All levels:**

Az egyhossz gépi hajvágás kizárólag géppel készül, a haj teljes felületén egységes hossz kialakításával. A szolgáltatás egy rövid konzultációval indul, ahol a vendég kiválasztja a kívánt méretet és megjelenést. A hajvágást finishelés zárja, a vendég által választott styling termékkel a letisztult végeredményért.

### 4. Gépi egy hossz hajvágás & szakáll igazítás — Clipper cut & beard trim

**All levels:**

Az egyhossz gépi hajvágás és szakáll igazítás szolgáltatás teljesen géppel egy méretre történő hajvágást és precíz szakállformázást tartalmaz az egységes, letisztult megjelenésért. A kezelés rövid konzultációval kezdődik, ahol a borbély a vendég igényeihez igazítja a kívánt haj- és szakállstílust. A szolgáltatás finisheléssel zárul, prémium haj- és szakállápoló termékek használatával a tökéletes végeredményért.

### 5. Gyerek hajvágás — Kids' cut (up to 12)

**All levels:**

A gyerek hajvágás szolgáltatás 12 éves korig vehető igénybe, barátságos és türelmes környezetben. A hajvágás előtt rövid konzultáció történik a szülő és a gyermek igényei alapján a kívánt stílus kialakításához. A frizura finishelése a gyermek számára megfelelő styling termékkel történik a rendezett megjelenésért.

### 6. Hosszú hajvágás — Long haircut (scissors only)

**All levels:**

A hosszú haj vágás kizárólag ollós technikával készül, a természetes forma és textúra megőrzésére fókuszálva. A szolgáltatás konzultációval kezdődik, ahol a borbély a vendég elképzeléseihez és hajtípusához igazítja a kívánt fazont. A vágást finishelés zárja, a vendég által választott prémium termékkel a rendezett és stílusos megjelenésért.

### 7. Hosszú hajvágás & szakáll igazítás — Long haircut & beard trim

**All levels:**

A hosszú haj vágás és szakáll igazítás szolgáltatás kizárólag ollós hajvágást és precíz szakállformázást tartalmaz a természetes, ápolt megjelenésért. A kezelés konzultációval kezdődik, ahol a borbély a vendég hajtípusához, arcformájához és stílusához igazítja a kívánt fazont. A szolgáltatás finisheléssel zárul, prémium haj- és szakállápoló termékek használatával a tökéletes végeredményért.

### 8. Skinfade hajvágás — Skin fade

**All levels:**

A Skinfade hajvágás precíz átmenettel készül, ahol a haj fokozatosan a bőrig rövidül az oldalsó részeken. A szolgáltatás személyes konzultációval indul, hogy a végeredmény tökéletesen illeszkedjen a vendég stílusához és arcformájához. A hajvágást finishelés zárja, a vendég által választott prémium styling termékkel a maximális megjelenésért.

### 9. Skinfade hajvágás & szakáll igazítás — Skin fade & beard trim

**All levels:**

A skinfade és szakáll igazítás szolgáltatás precíz bőrig átmenetes hajvágást és részletes szakállformázást tartalmaz a modern megjelenésért. A szolgáltatás konzultációval kezdődik, ahol a borbély a vendég stílusához és arcformájához igazítja a haj és szakáll végső formáját. A szolgáltatás finisheléssel zárul, prémium haj- és szakállápoló termékek használatával a tökéletes végeredményért.

### 10. Szakáll igazítás — Beard trim

**All levels:**

A szakáll igazítás során a szakáll formázása precíz kontúrok kialakításával és borotválással történik az ápolt megjelenés érdekében. A szolgáltatás rövid konzultációval kezdődik, ahol a borbély a vendég arcformájához és stílusához igazítja a kívánt formát. A kezelés finisheléssel zárul, prémium szakállápoló termékek használatával a tökéletes végeredményért.

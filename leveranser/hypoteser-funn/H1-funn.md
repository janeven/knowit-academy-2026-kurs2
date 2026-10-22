# H1 – Gul og håndterbar – recovery virker, avviket er definisjonsstøy

**Eier:** Person C  ·  **Dato:** 2026-10-22  ·  **Status:** FERDIG – FALSIFISERT
**Dom:** **FALSIFISERT**

*Hypotesen er definert i [`../02-hypoteser.md`](../02-hypoteser.md) (avsnitt H1). Ikke endre den der. Skriv funn her.*

## 1. Testbare påstander

| # | Påstand (fra «Hva må være sant?») | Test (kilde + beregning) | Utfall | Sikkerhet (fakta / sannsynlig / antakelse) |
|---|---|---|---|---|
| 1 | Med normaliserte definisjoner ligger sporene innenfor ca. 4 uker av recovery-datoene. | **Terskel:** ≤ 4 uker. **Data:** TECH-003 (recovery → nåværende prognose): dataprofilering 30.4 → 31.10 = 184 d = **26,3 u**; bølge 1 readiness 15.8 → 30.11 = **15,3 u**; bølge 1 cutover 30.9 → 18.12 = 79 d = **11,3 u**; bølge 2 15.12 → 31.3 = **15,1 u**; bølge 3/sluttdato 28.2 → 30.6.2027 = 122 d = **17,4 u**. Kortest avvik er 2,8 × terskelen. OF-008 gir samme størrelsesorden for plattform (11 u bak recovery). **Retning:** recovery-baselinen brukte allerede den *myke* definisjonen («teknisk klar for test» lukker milepælen) [OF-013 §3–4, OF-003, EM-024]. Å normalisere til «godkjent» flytter milepælene *senere*, ikke tidligere. Støy-argumentet virker derfor motsatt vei. **Programmets egen RAID:** 30.4 var alle 5 risikoer gule, 0 røde (OF-009). 31.8 er 7 risikoer røde, 0 gule (OF-010). R-014, R-026 og R-031 gikk gul → rød. | **Motbeviser** | Avstandene er *sannsynlig* (TECH-003 er fagprognose, ikke godkjent dato [EM-089]). Retningen er *fakta* (OF-013, to kilder). Tellingene (14/27, 9/23, 18/64) er *fakta* (TECH-004, TECH-005, OF-008). |
| 2 | 395 kan forsvares; 438/459/472 består av ubestilte risikoer som sannsynligvis ikke inntreffer. | **(a) Allerede bundet:** påløpt 318 + forpliktet 91 = **409 brutto** (FIN-007; kontrollsum 318+91+63 = 472 i FIN-005). 409 − 395 = **+14 over 395 før én krone er brukt til uforpliktet arbeid.** **(b) Med full kreditt (34):** 409 − 34 = 375, så igjen 395 − 375 = **20** til alt uforpliktet. FIN-005 har 97 brutto (63 netto) uforpliktet. Hvis bare Kvales «nær sikre» 12 faller: 409 − 12 = 397, altså over 395 [EM-065]. **(c) Per kategori** (navn lik i FIN-003 og FIN-007): intern 99 mot 92, konsulenter 110 mot 86, Convergent 133 mot 128 (brutto før kreditt). Tre av fem kategorier har allerede påløpt + forpliktet over *hele* 395-budsjettet. **(d) Sensitivitet:** 472 uten *all* contingency (22) = **450**, fortsatt 55 over 395. 395 + kun forlengelsen (41) = 436. **(e)** Laveste scenario i Finance (455) ligger 60 (15,2 %) over 395 [FIN-004]. **(f)** «Base er 472», ikke en risikosum [EM-172, EM-173]. | **Motbeviser** | *Fakta*: 409 > 395 (FIN-007 og FIN-005 uavhengig, kontrollsum stemmer). Kategorisammenlikningen (c) er *sannsynlig* (navnene er like, men definisjonen av kreditt i 395 er uavklart, se §7). |
| 3 | Piloten viser at skalering til 286 er mulig uten ny runde med rensing og beslutninger. | 42/286 = 14,7 %. Representative testløp for 61/286 (21 %), uten alvorlighetsgrad 1–2-feil for **38/286 (13,3 %)** [EM-083]. Fakturakorreksjon i pilot **7,8 %**, som er 3,1 × H1-terskelen på 2,5 % og 3,9 × januarverdien (2,0) [EM-094, OPS-001]. 17/42 (40 %) trengte manuell fakturakontroll; 8/42 (19 %) har åpne portal-/ordreavvik [OPS-003, EM-087]. Kundedrift tåler maks 50 kunder med manuell kontroll; 286/50 = **5,7 ×** [EM-084]. «Håndterbart for piloten, men ikke for 286» [EM-078]. 13 av 61 pilotavtaler (21 %) har tom basisdato, feil indekskode eller manglende SLA-regel [EM-162]. 19 kontrakter holdes utenfor automatisk kjøring [EM-081]. Pilotens egen etteranalyse sier at neste bølge ikke bør åpnes før fakturakontroll og eier er på plass [OPS-003]. CFO har stoppet nye migreringer med uavklarte pris-/kredittrutiner [EM-165]. | **Motbeviser** | *Fakta* for tellingene (OPS-003, EM-087, EM-091 stemmer). Hvordan de 42 ble valgt, står ikke i korpuset («risikobasert sekvensering» [EM-085]). Retningen på skjevheten er derfor *ukjent*. |
| 4 | SLA-fallet er sesong/fravær, ikke ressursuttak til OneFlow. | SLA 95,8 → 94,9 → 93,2 → 91,4 (jan → aug). Fallrate per måned: −0,30 (jan–apr), −0,85 (apr–jun), −1,10 (jun–jul, 92,1 [EM-136]), −0,70 (jul–aug). Fallraten er 2,8 × høyere apr–jun enn jan–apr, og den begynte etter at ni fagpersoner gikk inn i OneFlow-test fra februar [EM-134/135]. Fallet fortsatte etter at linjen tok folk *tilbake* i mai (4 + 3) og juli [EM-141, EM-143], så tilbakeføringene snudde ikke trenden. Det er forenlig både med forsinket effekt og med andre årsaker. Fraværet steg 5,5 → 7,1 (+29 % relativt). OPS-002 sier at fallet er *størst i enheter som har avgitt erfarne fagfolk*, og at fravær/sesong/marked også bidrar. Køen er størst i NO og DK, der flest kontrakts-/prosesseksperter ble avgitt [EM-136]. En ren sesong- eller fraværsforklaring skulle truffet alle enheter likt. | **Motbeviser delvis** | *Sannsynlig* (B/D: OPS-002 og én enkeltuttalelse som er part). Andelen kan **ikke** beregnes. Det finnes ingen 2025-data, ingen årsakskoding og bare fire KPI-punkter pluss juli. |

## 2. Falsifiseringsforsøk

Jeg forsøkte først å *redde* H1:
- Lette etter en revidert, godkjent milepælsdefinisjon som viser at sporene er innenfor ca. 4 uker. Søkte OF-003/005/006/007/008/013, TECH-003, EM-014–019, EM-024, EM-085/086/089/090. **Fant ingen.** OF-013 §3 krever tvert imot at forretningsgodkjenning og produksjonsklarhet «følges separat».
- Lette etter en kilde som sier at 472 er en risikosum og ikke et forventet estimat. Fant det motsatte: «Base er 472» [EM-172, EM-173] og at 382 «ikke lenger er et forventningsrett estimat» [EM-167].
- Prøvde å fjerne alt som kan kalles spekulativt: all contingency (→ 450), og kun forlengelse (→ 436). Begge ligger fortsatt over 395.
- Lette etter noe som viser at pilotens 7,8 % er et uheldig utvalg. Fant det ikke. Utvalget er «ikke representativt» [EM-084], men retningen er ukjent.

**Det H1 har rett i:**
1. 395 var aldri en ramme, bare en intern prognose «med vesentlig usikkerhet» [OF-013 §2, EM-018].
2. Juni 2027 er et fagestimat og ikke en godkjent dato [EM-089].
3. Kjernen er ikke et totalhavari [TECH-002 (utkast), OPS-003].
4. «Gul mot recovery» er teknisk sant på recovery-definisjonene.

Ingen av disse gjør programmet *håndterbart innenfor 395 / 28. feb.*

**Recovery-planens egne forutsetninger er brutt** [OF-013 pkt. 5]:
- **7-dagers beslutninger:** 12 av 12 saker i loggen overskrider 7 dager. Korteste er 29 dager og median 35,5. 6 er fortsatt åpne [OF-011].
- **Stabile krav fra april:** scope-frys-saken har stått åpen siden 10.8 [OF-011], og først 10.9 stanset styringsgruppen godkjenning av nye forbedringsønsker [OF-014 pkt. 3]. «Nye varianter kommer inn hver uke» [EM-050, 4.9].
- **Bekreftet linjekapasitet:** drift trakk tilbake folk i mai og juli og «kan ikke avgi ytterligere kapasitet» [EM-141, EM-143, OF-014]. Gapet er 49 FTE [HR-002].
- **Ukentlig leverandørrecovery:** R-014 gikk fra gul («ukentlig recovery-plan») til rød («kreditt og ny plan») [OF-009, OF-010].

OF-013 krevde ny vurdering av dato og kost ved vesentlig brudd. Første sak i loggen ble reist 19.4 og avgjort først 2.6 (44 dager mot 7). Da var bruddet dokumentert. Reassessering kom på styringsgruppens agenda 10.9, 100 dager senere, og endelig beslutning ble utsatt til 22.9 [OF-014].

## 3. «Hva ville fått oss til å endre mening?»

*Observasjonen fra 02-hypoteser.md. Fant du den?*
- (a) Revidert, godkjent milepælsdefinisjon som viser innenfor 4 uker: **Nei.** Lette i alle statusrapporter, referater og PMO-/styringsgruppetråder, og fant det motsatte.
- (b) Silje Tran bekrefter at 472 er en risikosum: **Nei.** Hun skriver «base» og «forventningsrett».
- (c) Bølge 1 kan utvides til flere hundre kunder med korreksjonsrate < 2,5 %: **Nei.** Piloten ligger på 7,8 %, og OPS-003, EM-097 og EM-165 anbefaler eller krever at neste bølge ikke åpnes.

## 4. Alternative forklaringer testet

- **«Forskjellen er bare ulike baselines.»** Delvis sant for *etiketter*. Men recovery-baselinen var selv brutt, og to kilder (OF-008, TECH-003) viser 11–26 uker mot den.
- **«Gapet 395 → 472 er bare forlengelse (41).»** Nei. 395 + 41 = 436, og påløpt + forpliktet er 409 (utenom de 63 uforpliktede).
- **«Gul er en rapporteringskonvensjon, ikke en realitetsvurdering.»** Støttet av hva dokumentene viser: PMO foreslo rød [OF-008] og dataleder nektet «følger plan» [EM-008]. Total gul ble holdt etter instruks [EM-010/011/013]. Rødt på arbeidsstrøm, gult på total [EM-011]. Vi trekker ingen slutning om hensikt. Funnet er at fargen *ikke* er definisjonsstøy; den er et valg om hvilken baseline som gjelder.
- **«Kredittforventningen redder tallet.»** Ikke under noen kreditt-antakelse (se test 2b). Convergent tilbyr 24–34 *kun* mot scope-frys og felles plan [VEN-002]. Å vente med frys for å beskytte kreditten er derfor selvmotsigende.

## 5. Dom og begrunnelse

**FALSIFISERT** på kost og dato, med primærdata og to uavhengige kilder, slik 02-hypoteser.md forventet.
- 409 mill. er påløpt eller forpliktet mot en prognose på 395. Selv full kreditt gir bare 20 mill. igjen til alt uforpliktet, mot 97 brutto i Finance.
- Alle spor er 11–26 uker bak *recovery*-datoene, og definisjonsendringene var mykere, ikke strengere.
- Alle fire forutsetninger i recovery-planen er brutt.
- Bakgrunnen for 395 → 472 er ikke «ubestilte risikoer» alene: 450 gjenstår selv uten contingency.

H1 beholder tre gyldige poeng, nevnt over: 395 er en prognose, juni er et fagestimat, kjernen er ikke et havari.

## 6. Kilder brukt

| Kilde-ID | Type (A–D) | Hva den viser | Merknad (kvalitet, versjon, konflikt) |
|---|---|---|---|
| FIN-007 | A | Påløpt 318, forpliktet 91, sum 409 | Ekskluderer 11,2 linjekost. Convergent 133 er *før* kreditnota. |
| FIN-005 | A | Brutto 506, kreditt −34, netto 472. Kontrollsum 318+91+63 | Autoritativ (16.9). Kategorier ≠ FIN-007, så sammenliknes kun på totalnivå. |
| FIN-003 / FIN-004 | A (mellomversjoner) | 395-komponenter, 438, 455/459/494 | Forelder av FIN-005. Reserve 17 i 395 er fordelt på poster i 438. |
| FIN-001 | A | Plan: 92 + 142 + 46 = 280 | Gevinstlinjer summerer til 602, ikke 620 (se §7). |
| BOARD-001/002/003/004/005 | A (protokoll) / B (pakker) | Ramme 280. Pakkene sa 395 og gul. Protokollen: «ikke fremlagt som ny ramme» | Risikovedlegget til 26.8 mangler. |
| OF-013, OF-003 | A / B | Recovery-forutsetninger og de myke definisjonene | OF-013 er «endelig, intern». Ikke styregodkjent. |
| OF-005/006/007/008 | B (OF-008: C, utkast) | Gul-linjen, PMO-forslag om rød | OF-008 er *ikke godkjent* men mest ærlig. |
| OF-009, OF-010 | A | RAID 30.4 (alle gule) mot 31.8 (alle røde) | R-051 uten eier. |
| OF-011 | A | 12 beslutninger: 29–56 dager, median 35,5, 6 åpne | Backfill står åpen selv om Vik godkjente 4 uker 6.9 [EM-140]. |
| OF-014 | A | Reset utsatt til 22.9. Ingen nye ønsker før da | – |
| TECH-003 | A/B | Original / recovery / nåværende datoer | Fagprognose, ikke godkjent [EM-089]. |
| TECH-002 | C (utkast, part) | Kjernen levedyktig, 30.6.2027 | Brukes kun til poenget «ikke havari». |
| OPS-001/002/003 | A | KPI, SLA-forklaring, pilotutfall | OPS-002 blander fravær/sesong/uttak. |
| VEN-001, VEN-002 | A (utdrag) / C | Kontrakt og kreditttilbud 24–34 mot scope-frys | VEN-002 er forhandlingsposisjon. |
| HR-002 | A | Bemanning 168 / 119, gap 49 | – |
| EM-008–013, 014–019, 024, 047–051, 062–068, 077–090, 091–097, 134–145, 166–173, 180–183 | D | Hvem sa hva, når | Enkeltsyn. Brukt til dato og kontekst, ikke som eneste bevis for noen konklusjon. |

## 7. Åpne spørsmål / hva som mangler

1. **Er leverandørkreditten (34) allerede inne i 395?** Bro-regnestykket 395 + 41 + 22 + 19 + 29 = 506 stemmer kun hvis 395 er *brutto* av kreditt. Silje og CFO sier 395 *inkluderer* kreditt [EM-172, BOARD-004], og da er 506 *netto* og 472 trekker kreditten to ganger. Avgjør om gapet er 77 eller 111. **Hvem:** Silje Tran. Dette endrer ikke dommen (395 faller uansett), men det avgjør tallet CEO skal bruke.
2. **382 → 395:** Silje skriver 382 i juni [EM-166/167], men 395 står i mars-rapporten [OF-005/013]. Hva er de 13 millionene?
3. **«14–20 uker bak original» holder ikke mot TECH-003.** Samme datoer gir 26–31 uker for bølgene og **82,7 uker** for dataprofilering (31.3.2025 → 31.10.2026). Tallet 14–20 kommer fra OF-008/EM-088 og bruker trolig en annen milepæl. Må avklares med Camilla Bruun / Julie Nystad før det står i CEO-briefen.
4. **Er bølge 1 allerede i drift?** TECH-003 setter «bølge 1 cutover» til 18.12 (status «manuelle kontrollsteg»; readiness: «42 av 286 kunder valgt»). Samtidig er de 42 migrert og stabilisert 18.8 (34 av 42 [EM-087]) og analysert i OPS-003. **01-situasjonsbilde.md** skriver at «ingen av Bølge 1 er i drift» ved 31.12. Dette ser ut til å motsi OPS-003/EM-087. **Hvem:** Camilla Bruun / Lars Pettersen.
5. **Påløpt 318 mot planlagt 234 (2025 + 2026)** er +84 (+36 %), men FIN-007s avgrensning (aktiverbar intern tid) er ikke sammenliknet med rammens definisjon. Retning klar, størrelse uklar.
6. **FIN-001 gevinstlinjer summerer til 602, ikke stated 620.** 2025: linjer 0 mot total 18. 2026: 43 mot 61. 2027: 139 mot 121. NPV 218 er ikke regnet om.
7. **Styrepakke juni sa gevinst 184 fra 2028** [BOARD-003]. FIN-006 sier 128 fra 2029. Begge er «gevinstreduksjon», men de er ulike tall.
8. **Risikovedlegget til styrepakke 26.8 mangler.** Vi vet ikke hva styret ble varslet om.

## 8. Til fellesmøtet *(fylles kun ut hvis dom er STØTTET eller STERKT STØTTET)*

*Ikke relevant: dom er FALSIFISERT.*

## 9. AI-bruk *(del av leveransen «AI-arbeidslogg»)*

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Selv kontrollert mot original |
|---|---|---|---|
| Claude leste alle H1-kilder i `oppgave/CaseCorpus` (CSV, MD og PDF direkte; FIN/OPS/OF/TECH-CSV-ene, BOARD-001–005, OF-003–014, TH-002/003/004/007/008/010/012/013/014/020–028/030/039). Den regnet alle tall selv i Python og skrev utkast til denne filen. | Datoene, tellingene og tabellene fra originalkildene. Formuleringen av «hva H1 har rett i». | **Forkastet:** «14–20 uker bak original» som felles tall (§7 p. 3). **Flagget som motstrid:** 01-situasjonsbilde sin påstand om at ingenting av bølge 1 er i drift (§7 p. 4). **Ikke brukt:** EM-127–133 og EM-052–061/098–111 er lest kun via 01/02, ikke selv. | **Claude:** alle beløp og datoer i §1 er hentet fra CSV/MD/PDF og regnet på nytt. **Person C bør selv stikkprøve:** (1) 409 vs 395 (FIN-007 mot FIN-005), (2) uker-tabellen (TECH-003), (3) OF-011-medianen. `.xlsx`-filene er ikke åpnet; CSV er brukt. |

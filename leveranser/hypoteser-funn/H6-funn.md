# H6 – Kunde- og inntektsskaden dominerer og må styre rekkefølgen

**Eier:** Person C  ·  **Dato:** 2026-10-22  ·  **Status:** FERDIG – SVEKKET
**Dom:** **SVEKKET** (dominanspåstanden). Sekvenseringsdelen («stans neste bølge, én eier, kundeplan») står på egne ben og støttes av uavhengige kilder uten at H6 må være sann (se §5).

*Hypotesen er definert i [`../02-hypoteser.md`](../02-hypoteser.md) (avsnitt H6). Ikke endre den der. Skriv funn her.*

## 1. Testbare påstander

| # | Påstand (fra «Hva må være sant?») | Test (kilde + beregning) | Utfall | Sikkerhet (fakta / sannsynlig / antakelse) |
|---|---|---|---|---|
| 1 | Forverringen i SLA/churn skyldes i vesentlig grad OneFlow, ikke sesong/fravær/marked. | **Gap mot mål, august:** SLA 5,6 pp (97,0 − 91,4), churn 2,4 pp (6,7 − 4,3), fakturakorrigering 3,7 pp (4,9 − 1,2) [OPS-001]. Av dette fantes allerede **21 % / 29 % / 22 %** i januar (1,2 / 0,7 / 0,8 pp). De øvrige **79 % / 71 % / 78 %** er forverring jan–aug. Alle seks KPI-er var allerede dårligere enn mål i januar. For attribusjon: OPS-002 sier fallet er størst der fagfolk er avgitt, og at fravær (7,1 %), sesong og marked også bidrar. «Hele utviklingen kan ikke tilskrives programmet.» Køen er størst i NO og DK, der flest eksperter er avgitt [EM-136]. Tilbakeføringene i mai/juli snudde ikke trenden [EM-141, EM-143]. Fraværet steg 5,5 → 7,1. | **Uavklart** (peker delvis mot H6) | *Sannsynlig* at OneFlow bidrar vesentlig (OPS-002 og én part [EM-136]). Andelen kan **ikke** beregnes: ingen 2025-data, ingen årsakskoding av SLA-fall i korpuset, fravær og uttak beveger seg samtidig. |
| 2 | Minst noen av de tre fornyelsene med OneFlow-signaler går tapt hvis ingenting gjøres (105 mill.). | **Nedbrytning av 146 [OPS-004]:** direkte OneFlow-signal (EnergiVest 42 + Skandia 29) = **71 (49 %)**; indirekte via ressurstrekk (Nordbygg 34) = **34 (23 %)**; pris/marked (Metrohandel 23 + Svea 18) = **41 (28 %)**. Sum 146. «105» (72 %) slår sammen direkte og indirekte. I e-posttråden er mønsteret det samme: to med faktura-/portalavvik, én indirekte (MedicoLog, ikke migrert [EM-148]), og en av de to «direkte» (Fjordkraft) har også pågående prisdiskusjon. **Søk etter oppsigelse:** i hele korpuset er det **ingen** kunde som har varslet oppsigelse eller sagt at de signerer uansett. Metrohandel og EnergiVest forekommer kun i OPS-004. Tid til fornyelse fra 17.9: 28, 44, 74, 89 og 105 dager. | **Uavklart** | Tallene 146 og 3/2-splitten er *fakta* (to kilder: OPS-004, EM-149/150). Sannsynlighet for tap er *antakelse*. Verdien er **årlig kontraktsverdi, ikke dekningsbidrag**, og kontraktslengder og marginer finnes ikke i korpuset. |
| 3 | Eksponeringen vokser ved neste bølge (manuell kontroll skalerer ikke). | Kundedrift tåler maks **50** kunder med manuell fakturakontroll [EM-084]; 286/50 = **5,7 ×**. Med pilotens rate 17/42 (40 %) ville ca. **116** av 286 trenge manuell kontroll (286 × 17/42), 2,3 × kapasiteten. «Håndterbart for piloten, men ikke for 286» [EM-078]. Ingrid Mørk krever < 5 kunder med manuell kontroll før neste bølge [EM-097]; nå er det 17 (3,4 ×). Korreksjon 7,8 % mot 2,0 % [EM-094]. TECH-004: fakturamottaker mangler eller er tvetydig i 8,4 % av aktive kontrakter, og berørte kunder skal ikke migreres uten manuell kontroll. 13/61 pilotavtaler (21 %) har data-/regelfeil [EM-162]. | **Støtter** | *Fakta* for regnestykket (EM-078/084, OPS-003 stemmer). Pilotens representativitet er ukjent [EM-084, EM-094], så *skaleringsraten er antakelse*. 5,7 × er uavhengig av raten. |
| 4 | Resultatrisikoen (3,6 bekreftet + inntil 7,2) er reell, ikke bare timing. | **Regnskap [OPS-005]:** 16,8 + 3,6 + 8,9 − 1,7 = 27,6 (stemmer). Resultatrisiko = 3,6 + (8,9 − 1,7) = **10,8** (stemmer). 3,6 er avstemt med omposteringer tatt ut [EM-159, Jonas Aas]. 8,9 er «øvre arbeidsestimat, ikke bokført tap» [EM-163]. 16,8 er «hovedsakelig arbeidskapital» [EM-155] (6,2 uavklart mottaker + 3,4 pris/kontrakt + 2,1 tvist + 5,1 ordinært = 16,8). Thomas Vik: 8,9 holdes utenfor program-EAC før sannsynlighetsvurdering [EM-165]. Overlapp mellom 16,8 og 8,9 / 3,6 er **ikke** kontrollert. 13,9 → 16,8 (28.8 → 2.9.) skyldes ny datakobling, ikke vekst [EM-154]. | **Støtter delvis** | *Fakta*: 3,6. *Antakelse*: 7,2 (ikke sannsynlighetsvurdert). 16,8 er timing og skal ikke kalles tap (*sannsynlig*, enighet mellom Silje Tran, Ragnhild Moen, Mari Heggen). |
| 5 | **Hovedpåstanden:** kunde-/inntektsskaden er større og mer akutt enn programkost. | **Målbart (A):** resultatrisiko inntil 10,8 + linjekost 11,2 [OPS-002] = **≤ 22,0** (trolig noe overlapp, siden 11,2 inkluderer krediteringer). Programkost: **+77** mot 395 (472 − 395) og **+192** mot ramme 280 [FIN-005]. 22,0 / 77 = 29 %; 22,0 / 192 = 11 %. **Inntektseksponering** (ikke målbar): for å matche +77 på ett års horisont må tapssannsynlighet × dekningsgrad være ≥ 0,73 på 105, ≥ 0,53 på 146 og ≥ 1,08 på 71 (umulig). Flerårs-horisont endrer dette, men ingen kontraktslengder er oppgitt. **Mer akutt:** fornyelsene faller 28–105 dager frem, før noe programeffekt. Dette er den eneste delen som står. Kategoriene er ulike (årsinntekt mot engangskost), så sammenlikningen er illustrativ. | **Motbeviser** på målbare tall; **uavklart** på inntektseksponering | *Fakta* for tallene på begge sider. *Antakelse* for alt som krever margin/sannsynlighet. |
| 6 | (Handling) Navngi *én* eier av kunde-/inntektsrisiko. | R-051 (registrert 27.8) har **tom eier** [OF-010]. SG 10.9: «avklarte ikke … samlet eierskap» [OF-014]. **Men:** Eirik Solheim koordinerer operativ oppfølging, og finans følger beløp [OF-014 pkt. 5]. Beate Høyer eier samlet fornyelsesoversikt [EM-151, 12.9]. Karin Eide eier «samlet kunde- og driftsbilde» til neste beslutningssak [BOARD-005]. | **Støtter delvis** | *Fakta*. 01-situasjonsbilde sin «ingen eier» er for sterk: tre midlertidige eiere finnes, ingen formell. |

## 2. Falsifiseringsforsøk

- **Forsøkte å vise at tapene er små i forhold til program.** Lyktes på målbare tall: ≤ 22 mot +77 / +192. Jeg *forsøkte også å redde H6* ved å regne bakover (hvor stor må tapsandelen være?), og kommer til ≥ 0,73 på 105 mill. på ett år. Det kan hverken bekreftes eller avvises uten margin- og kontraktsdata.
- **Forsøkte å finne bevis på reelt tap av en fornyelse.** Ingen funnet i hele korpuset (søk: oppsig*, terminate, cancel, churn, konkurrent, kundenavn). Det er heller ingen kunde som har sagt at de signerer uansett. Tomt begge veier.
- **Sjekket at støyen holdes ute.** TH-039: fem av sju saker er ordinære [EM-231]; Vestbygg-portalfeilen var cache og lukket på 4 dager [EM-232/233]; SFTP/SMS-sakene hører ikke til OneFlow [EM-234/235]. Ingrid Mørk støtter at den ordinære køen ikke skal brukes som bevis [EM-236]. Jeg har ikke brukt disse sakene som bevis.
- **Sjekket om kundeproblemene kan være eldre enn OneFlow-tiltakene.** Delvis ja: 21–29 % av gapet mot mål fantes allerede i januar, og alle seks KPI-er var under mål da.
- **Sjekket om 27,6 bør brukes.** Nei: den summerer arbeidskapital, bekreftet kreditering og risiko som ikke er bokført.

## 3. «Hva ville fått oss til å endre mening?»

- (a) Årsakskoding viser at flertallet av SLA-fallet og de tre fornyelsene har andre rotårsaker: **Nei, finnes ikke i korpuset**, ikke bestilt ferdig, heller ikke for fornyelsene ut over Mari Heggens muntlige inndeling [EM-149]. Gjelder begge veier.
- (b) Fornyelsene signeres uansett: **Nei, ingen opplysninger.** Motsatt: Metrohandel (15.10) eller EnergiVest (31.10) varsler oppsigelse med henvisning til fakturaproblemer: **Nei, ingen slik e-post** (korpus slutter 16.9).
- (c) Pilotens 7,8 % er representativ: **Nei, motsatt:** «ikke representativt» [EM-084, EM-094]. Utvalgskriterier er ikke oppgitt.

## 4. Alternative forklaringer testet

- **Marked og pris.** To av fem fornyelser (41 mill., 28 %) har pris/konkurrent som hovedårsak [OPS-004]. Svea: konkurrenttilbud. Arctiq: oppkjøp hos kunden [EM-147].
- **Fravær og sesong.** Fravær 7,1 % mot <5,0 % mål [OPS-001]. Sesong kan ikke testes (ingen 2025).
- **Eldre datakvalitet i Cobalt, ikke OneFlow i seg selv.** Dubletter 11,7 % og uklar mottaker 8,4 % [TECH-004] ligger i legacy-data, og migrering utløser eksponeringen. Camilla Bruun advarer mot å si at data alene er rotårsak, siden prisregel og manuell håndtering også inngår [EM-160]. Dette peker mot at *å migrere* er det som skaper kundeeksponering, altså samme konklusjon som sekvenseringen.
- **Kundesiden er ikke hovedbegrunnelsen for programmet.** Av korrigert varig gevinst (128) ligger bare 18 (14 %) i churn/mersalg og feil/kreditering [FIN-006]. Dette er kontekst, ikke bevis for eller mot H6.

## 5. Dom og begrunnelse

**SVEKKET.** Mer imot enn for på dominanspåstanden, men ikke avvist siden inntektssiden ikke kan måles.
- På *målbare* tall er kunde-/resultateffekten ≤ 22 mill. mot +77 i programkost. Dominanspåstanden krever at nesten hele årsverdien av OneFlow-signalerte fornyelser går tapt, på nær full margin.
- «105 mill. OneFlow-risiko» overdriver. 34 er indirekte (ressurstrekk), og 41 er pris/marked. Direkte signal er **71**.
- Ingen fornyelse er varslet tapt. SLA/churn-forverringen kan ikke fordeles på årsak.

**Det som står, og som gruppen bør vurdere uavhengig av H6:**
- **Tidspunktet (akutthet):** første fornyelse om 28 dager, den første med OneFlow-signal om 44.
- **Skaleringsregnestykket:** 286 / 50 = 5,7 ×.
- **Stans av nye migreringer til fakturakontroll er løst:** anbefalt av OPS-003 og Ingrid Mørk [EM-097], og allerede besluttet av CFO [EM-165]. Dette trenger ikke H6 for å være riktig.
- **Én formell eier.**

Disse er lav-anger-tiltak uansett om H6 eller H3/H4 er rotårsak. Bølge 2 er uansett ikke planlagt før 31.3.2027 [TECH-003].

## 6. Kilder brukt

| Kilde-ID | Type (A–D) | Hva den viser | Merknad (kvalitet, versjon, konflikt) |
|---|---|---|---|
| OPS-001 | A | KPI jan/apr/jun/aug vs mål | Juli finnes bare i EM-136 (92,1 %). |
| OPS-002 | A/B | SLA-fall størst der folk er avgitt. 11,2 mill. linjekost | Blander fravær, sesong, marked, uttak. 11,2 trolig overlapper 3,6. 8,7 (14.8) → 11,2 er trolig tidsforskjell, ikke avklart [EM-138]. |
| OPS-003 | A | Pilot 42: 17 manuell, 8 avvik, 7,8 %, ingen havari | Lite, ikke-representativt utvalg. |
| OPS-004 | A | Fem fornyelser, 146, 3/2-split | **Kundenavn ≠ TH-022** (Fjordkraft, ScanMarine, MedicoLog, Vestbygg, Arctiq). Ingen overlapp. Totalen 146 og 3/2-splitten er lik i begge. |
| OPS-005 | A (blandet) | 16,8 / 3,6 / 8,9 / −1,7 / 27,6 / 7,2 | Regnestykket stemmer. Overlapp 16,8 mot 8,9/3,6 ikke kontrollert. |
| FIN-005 | A | +77 mot 395. 472 base | Autoritativ. Programkost, ikke linjekost eller inntekt [EM-172]. |
| FIN-006 | A | Gevinst 128 etter −40/−42 | Kategoriseringen av kundegevinster er ikke begrunnet. |
| BOARD-004, BOARD-005 | B / A | «Håndterbar … ingen vesentlig inntektseffekt på konsernnivå» (pakke). Styret ba om samlet kunde-/inntektsbilde (protokoll) | Risikovedlegg mangler. Vi kan ikke vurdere konsernmateriellhet (konsernomsetning mangler). |
| OF-006, OF-007 | B | «Ingen samlet fremstilling av SLA og linjekost» | Viser rapporteringshull, ikke årsak. |
| OF-010, OF-014 | A | R-051 uten eier. SG 10.9 uavklart | Presisering 11.9 [OF-014 pkt. 5]. |
| TECH-003, TECH-004 | A/B | Bølge 2 31.3.2027. Fakturamottaker 8,4 % | – |
| TH-022 (EM-146–151) | D | Fornyelser, 3/2-split, ledereiere | Navn og OPS-004 i konflikt. |
| TH-023 (EM-152–156) | D | 13,9 → 16,8 → 16,5; kategorier | Silje Trans «9,6 mill. med data/kontrakt/kundetvist» = 6,2 + 3,4 (uten tvist 2,1). Etikettfeil, ikke betydelig. |
| TH-024 (EM-157–160) | D | 3,6 bekreftet, 1,7 overlapp | Jonas Aas (regnskap), Camilla Bruun. |
| TH-025 (EM-161–165) | D | 8,9, 7,2, 61 avtaler / 13 med feil | Mari Heggen: «øvre arbeidsestimat». |
| TH-014, TH-013 (EM-082–097) | D | Pilot-feil, 50-kapasitet, krav om < 5 manuelle | – |
| TH-020/021 (EM-134–145) | D | SLA og ressurstrekk | Kun parter (Mørk, Solheim, Berg). |
| TH-039 (EM-230–236) | støy | Skiller ordinære saker | Brukt kun til avgrensning. |

## 7. Åpne spørsmål / hva som mangler

1. **Kundelønnsomhet og kontraktslengder** for de fem fornyelsene (hvem: Beate Høyer, kommersielt). Uten dem kan «inntektsskade» ikke sammenliknes med programkost.
2. **Årsakskoding av SLA-fallet** og av hver fornyelse (Ingrid Mørk, Mari Heggen). Dette er testen som faktisk avgjør H6.
3. **Kundenavn:** OPS-004 mot TH-022 (Beate Høyer). Før noe kunde navngis i styrepapirer.
4. **Resultatet av Mari Heggens kontroll av de berørte fornyelsene** (frist onsdag 16.9 [EM-165]). Ligger ikke i korpuset.
5. **Overlapp mellom 16,8 og 8,9/3,6** i OPS-005 (Sander Lie, Jonas Aas).
6. **Utvalgskriterier for de 42** (Ragnhild Moen). Avgjør om 7,8 % er en under- eller overdrivelse.
7. **Konsernomsetning/EBITDA** for å vurdere om kundeeffekten er vesentlig på konsernnivå (Thomas Vik / Silje Tran). Treasury sier covenant holder ved 470 [EM-181], altså ingen bindende begrensning enda.
8. **Er pilotkundene «bølge 1 i drift»?** Se H1-funn §7 p. 4. Det påvirker hvor mye av eksponeringen som allerede er realisert.

## 8. Til fellesmøtet *(fylles kun ut hvis dom er STØTTET eller STERKT STØTTET)*

*Ikke relevant: dom er SVEKKET. De fire tiltakene i §5 («Det som står») bør likevel tas opp som lav-anger-punkter uavhengig av hvilken rotårsak gruppen lander på.*

## 9. AI-bruk *(del av leveransen «AI-arbeidslogg»)*

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Selv kontrollert mot original |
|---|---|---|---|
| Claude leste alle H6-kilder direkte (OPS-001–005, FIN-001–007, BOARD-001–005, OF-010/014, TECH-003/004, HR-003 og TH-002/012/013/014/020/021/022–028/039). Den regnet alle tall i Python og skrev utkastet. | Tellinger og beløp fra CSV/MD/PDF. Nedbrytningen 71/34/41. | **Endret:** 01-situasjonsbilde sin «ingen eier» (tre midlertidige eiere finnes). **Forkastet:** 27,6 som tall; «105 mill. OneFlow-effekt» som uforbeholden formulering. **Flagget:** kundenavn-konflikt, etikettfeil i EM-155. | **Claude:** alle regnestykker i §1 er regnet på nytt fra originalfilene. **Person C bør selv stikkprøve:** (1) 71/34/41-nedbrytningen mot OPS-004, (2) SLA-gapdekomponeringen mot OPS-001, (3) at EM-141/143 beskriver *tilbakeføring til linjen*, ikke uttak fra den. `.xlsx`-filene er ikke åpnet; CSV er brukt. |

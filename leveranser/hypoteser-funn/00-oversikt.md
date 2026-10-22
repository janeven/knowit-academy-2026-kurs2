# Oversikt – hypotesetest

*Status: alle seks hypoteser er testet (2026-10-22). Dommene står i hver funnfil. Statuskoder: `FERDIG – FALSIFISERT` · `FERDIG – SVEKKET` · `LØFTES` (støttet/sterkt støttet). Instruks: [`../PROMPT-hypotesetest.md`](../PROMPT-hypotesetest.md). Bakgrunn: [`../01-situasjonsbilde.md`](../01-situasjonsbilde.md) og [`../02-hypoteser.md`](../02-hypoteser.md).*

## Dommer

| Hyp. | Kort | Eier | Status | Dom | Én-linjers begrunnelse | Funnfil |
|---|---|---|---|---|---|---|
| H1 | Gul og håndterbar (definisjonsstøy) | Person C | FERDIG – FALSIFISERT | **FALSIFISERT** | 409 mill. er allerede påløpt/forpliktet mot 395; alle spor 11–26 uker bak recovery (som selv brukte de myke definisjonene); alle 4 recovery-forutsetninger brutt. | [H1-funn.md](H1-funn.md) |
| H2 | Leverandøren er hovedårsak | Person A | FERDIG – FALSIFISERT | **FALSIFISERT** (primærårsak) | Leverandørfeil er 28–33 % av 18 uferdige integrasjoner (begge parter enige); Bølge 1 var blokkert av Nordflow-eide data/prosess uavhengig av verktøy; kontrakten gir ikke grunnlag for å tilskrive én part. Reell *forsterker*. | [H2-funn.md](H2-funn.md) |
| H3 | Styring/beslutningsrett er hovedårsak | Person B | LØFTES | **STØTTET** | Portene ble brutt ved start; alle 12 kritiske saker tok >4× målet (median 35,5) og blokkerer 10/18 integrasjoner. Mekanismen er beslutningsdisiplin, ikke bare uklar rett (saker med klar eier tok like lang tid). | [H3-funn.md](H3-funn.md) |
| H4 | Kapasitetskonflikt linje/program | Person B | FERDIG – SVEKKET | **SVEKKET** | Gapet på 49 FTE er reelt og på kritisk sti, men består fordi ingen prioriterer (H3). Forsinkelsene i 2025 kommer før målt gap, og lokalkunnskap kan ikke kjøpes. Forsterker, ikke primærårsak. | [H4-funn.md](H4-funn.md) |
| H5 | Kjernen/løsningen ikke levedyktig | Person A | FERDIG – SVEKKET | **SVEKKET** | 46/64 integrasjoner klare, bare 5–6 kode-/konfigfeil, ingen kilde sier kjernen er ubrukelig, pilot uten systematisk havari, grov forward-beregning gir break-even 44–83 mill./år mot 128. Ikke falsifisert: ingen uavhengig teknisk verifikasjon, og 4 danske kontraktspunkter er uavklarte. | [H5-funn.md](H5-funn.md) |
| H6 | Kunde-/inntektsskade dominerer | Person C | FERDIG – SVEKKET | **SVEKKET** | Målbar kunde-/resultateffekt ≤ 22 mill. mot +77 programkost; direkte OneFlow-signal er 71 av 146 (ikke 105); ingen tapt fornyelse i korpuset. Sekvensering (stans bølge, én eier) står uavhengig av H6. | [H6-funn.md](H6-funn.md) |

**Mønsteret:** Den ene hypotesen som holder (H3) er et *Nordflow-internt* styringsproblem. De to «ytre» forklaringene (H2 leverandør, H5 teknologi) holder ikke som hovedårsak. Kapasitet (H4) og kunder (H6) er reelle, men er forsterker og konsekvens. Den offisielle «gul og håndterbar»-linjen (H1) er motbevist.

---

## Felles konklusjon

| Rolle | Hypotese(r) | Begrunnelse |
|---|---|---|
| **Rotårsak** | **H3: styring og beslutningsdisiplin** (STØTTET) | Programmet ble startet i strid med mandatets og styrets portkrav (prosesseiere, dataprofilering, testdata, bemanning) og har siden kjørt uten en mekanisme som tvinger frem beslutninger. Alle 12 kritiske beslutninger brukte >4× målet (median 35,5 dager mot 7), og de blokkerer direkte 10 av 18 uferdige integrasjoner samt data- og testkjeden. Uavhengig støtte fra H2-funnene (begge parter er enige om at ≥ 10 av 18 er kundeskapt) og H5-funnene (pilotavvik er mest regel-/eierproblemer, ikke plattformfeil). **Forbehold:** kritisk-sti-effekten er ikke tallfestet, og mekanismen er «disiplin» mer enn «uklar rett». |
| **Forsterker(e)** | **H4: kapasitetskonflikt** (SVEKKET som primær) | 49 FTE gap, 37 over 120 %, 12 avganger; tilbakeføringer til linjen kostet anslagsvis seks uker i data/test. Konflikten består fordi ingen tar prioriteringsbeslutningen (H3). Å fylle gapet alene løser ikke saker som venter på beslutning eller lokalkunnskap. |
| | **H2: leverandørsvikt** (FALSIFISERT som primær) | Reelle og erkjente feil (verktøy forsinket, to arkitektbytter, 5–6 av 18 integrasjoner), men bare en minoritet av gapet. Kontrakten gir ikke grunnlag for å tilskrive hele avviket Convergent. Kreditttilbudet (24–34 mill.) er betinget av scope-frys + felles styrt plan. |
| | *Utenfor de seks hypotesene (funnet underveis):* | (i) **Datakvalitet og uavklarte forretningsregler** uten navngitt dataeier (11,7 % duplikater, 8,4 % uklar fakturamottaker). (ii) **Scope-vekst uten uttak** (47 endringer, 63 400 timer, 38 mill.). (iii) **Rapporteringspraksis** som hindret tidlig korrigering (omdefinerte milepæler, byttet baseline uten styrebehandling, bølgekutt og bottoms-up ikke vist for styret). *Disse er ikke testet som egne hypoteser; (iii) bør vurderes eksplisitt før det skrives i CEO-brief.* |
| **Symptom(er)** | Fall i SLA/FCR/svartid, churn 5,0 → 6,7 %, fakturakorrigering 7,8 % i pilot, fornyelsesrisiko, kø på 1 900 saker | H6 er SVEKKET: målbar kunde-/resultateffekt er ≤ 22 mill. mot +77 programkost. Likevel akutt i tid (første fornyelse om 28 dager). |
| **Avvist** | **H1** (gul og håndterbar); **H2** som hovedårsak; **H6** som «dominerende» | Se dommer. |
| **Ikke avvist, men ikke bekreftet** | **H5** (kjernen levedyktig) | Arbeidsantakelse: «kjernen er levedyktig». Ikke uavhengig verifisert. |

### Retning for anbefalingen (til CEO-brief, lederpresentasjon og 90-dagersplan)

1. **Konsernreset, ikke IT-reset.** Det er H3 som må løses: navngitt beslutningstaker per sakstype, 72-timers frist med automatisk eskalering til CEO, krav til innhold i beslutningsunderlag, håndhevede portkriterier, scope-frys med dokumentert unntaksprosess (juridisk/regulatorisk/kontraktsmessig). Samme konklusjon kommer uavhengig fra CIO-review (TECH-002), som sier at en ren teknisk reset ikke er tilstrekkelig.
2. **Beskytt kapasiteten (H4 som forsterker):** skjerm de ~23 kritiske rollene, finansier backfill i drift, fjern dobbeltallokering. CEO må beslutte prioriteringsregelen mellom linje og program.
3. **Behold kjernen som arbeidsantakelse (H5), men verifiser uavhengig** (2–3 uker) og regn en reell NPV på 472 (455–494) og 128/år.
4. **Kommersielt spor (H2):** bruk 34 som *krav*, ikke som sikker kreditt (CFO, EM-068); bruk «12 nær sikkert»; knytt scope-frys til felles plan innen leverandørens frister.
5. **Lav-anger-tiltak uavhengig av rotårsak (fra H6):** ikke åpne nye migreringsbølger før fakturakontroll og eierskap er løst (allerede besluttet av CFO, EM-165); formell eier av kunde-/inntektsrisiko; lederplan per berørt fornyelse; skill OneFlow-effekt fra pris/marked i all rapportering.
6. **Styret:** BOARD-005 pkt. 5 krever at vesentlige endringer legges frem uten å vente på ordinær syklus, og 472/juni 2027 er slike endringer. Styret fikk 395 på tross av at finans hadde 438 (17.6.) og 459 (18.8.).

### Må undersøkes videre (prioritert)

| # | Hva | Hvorfor | Hvem (i Nordflow) |
|---|---|---|---|
| 1 | **Kritisk-sti-analyse** med scenarioene «beslutninger på 7 dager», «leverandør i rute» og «full bemanning» | Eneste test som rent skiller H2/H3/H4 og tallfester H3 | Julie Nystad, Lars Pettersen |
| 2 | **Kostnadsbro 395 → 472:** ligger kreditten (34) allerede i 395? | Avgjør om CEO sier +77 eller +111, og om 472 trekker kreditten to ganger | Silje Tran |
| 3 | **Ekte NPV** (472, 128/år, redusert kjerne) | Brukes mot «fullfør vs stopp»; vår grovmodell er ikke en NPV | Silje Tran / Thomas Vik |
| 4 | **Uavhengig teknisk verifikasjon** av kjernen | Eneste som kan gjøre H5 endelig | Amina Rahman |
| 5 | **Verktøyets faktiske ankomst** (6.5. vs 13.6.) | Påvirker kredittkravet (5,4 vs 10,6 uker) | Lars Pettersen, Ole Martin Kvale |
| 6 | **Fire danske kontraktspunkter:** endelig fagbekreftelse og modellérbarhet | Åpner/lukker H5; må løses før migrering | Beate Høyer, Mikkel Sørensen, Nora Steen |
| 7 | **Årsakskoding** av SLA-fall og de tre/fem fornyelsene; kundelønnsomhet og kontraktslengder | Avgjør om H6 kan løftes eller avskrives | Ingrid Mørk, Mari Heggen, Beate Høyer |
| 8 | **Komplett beslutningslogg 2025–26** (ikke bare 12 kritiske); **bemanning per kvartal 2025** | Styrker H3, avgjør årsaksrekkefølge for H4 | Julie Nystad, Henrik Dahl |
| 9 | **Rapporteringspraksis** som egen analyse (hva ble vist for hvem, når) | Er funnet i alle spor, men ikke testet som hypotese | Team (ikke i korpuset å avgjøre hensikt) |
| 10 | **Risikovedlegget til styrepakke 26.8.** | Vi vet ikke hva styret ble varslet om | Thomas Vik / Julie Nystad |

---

## Avklarte kildekonflikter og felles tall

*Alle leveranser (CEO-brief, lederpresentasjon, 90-dagersplan, evidenslogg) skal bruke tallene i «Avklart verdi». «Bekreftet av» betyr at tallet er kontrollregnet fra originalfilene. **Åpen** betyr at korpuset ikke kan avgjøre det og tallet må ha forbehold til eieren har svart.*

| Tall / spørsmål | Avklart verdi (bruk dette) | Kilde | Status / bekreftet av |
|---|---|---|---|
| **Kontrollert sluttkostnad** | **472 mill. netto** (intervall 455–494); brutto 506 med antatt kreditt 34 | FIN-005, EM-173 | Avklart. Kontrollert av Finance 16.9. |
| Ligger leverandørkreditt allerede i 395? | **Åpen.** Brosummen 395+41+22+19+29 = 506 stemmer kun hvis 395 er *brutto* av kreditt, men CFO/Finance sier 395 *inkluderer* kreditt. Gapet er derfor enten 77 eller 111. *Bruk til CEO:* «472 netto forutsetter full kreditt på 34; uten kreditt 506» | FIN-005, EM-172/173, BOARD-004 | **Åpen** (Silje Tran). Flagget av Person A og C |
| Rapportert vs vedtatt ramme | Styrets ramme **280**; rapportert prognose 395 er ikke godkjent ramme; **påløpt 318, forpliktet 91 (409), gjenstår uforpliktet 63** | BOARD-002, FIN-001, FIN-007, FIN-005 | Avklart. Definisjon (aktiverbar tid) ikke sammenlignet mot rammens definisjon, retningen er klar |
| 382 vs 395 | **Åpen.** 382 står i Silje Trans juni-e-poster, 395 i styrepakker | EM-166/167 vs BOARD-003 | **Åpen** (Silje Tran). Ikke bruk 382 |
| Varig gevinst | **128 mill./år fra 2029** (210 fra 2028 opprinnelig; 184 var en tidligere, ufullstendig nedjustering i juni) | FIN-006, BOARD-003, EM-178/179 | Avklart. Bekreftet av Beate Høyer og Thomas Vik |
| Business case 620 vs 602 | Fasingen i FIN-001 summerer ikke: linjene gir 0/43/139/210/210 = **602**, ikke 620 (rad «Brutto gevinst» 18/61/121/210/210). NPV 218 er ikke regnet om | FIN-001, BOARD-001 | **Åpen**; kontrollregnet av Person A. Bruk 210/128 for steady state, ikke kumulativ |
| Dobbelttelling mot Cobalt | **40 mill. dobbelttelt, 42 mill. øvrig nedjustering** (ikke blandet) | FIN-006, EM-177–179 | Avklart (CFO-formulering) |
| **Forsinkelse mot original plan** | Sporstatus: prosess ~14, integrasjon 17, data ~20 uker. **Bølgene (TECH-003):** Bølge 1 +28,7, Bølge 2 +26, Bølge 3 +26 uker; dataprofilering +82,7 uker mot 31.3.2025. Fullføring **30.6.2027** (CIO, mest sannsynlig) | OF-008, EM-088, EM-104, EM-118, TECH-003 | **Delvis åpen** (Camilla Bruun / Julie Nystad: hvilken milepæl ligger bak «14–20»?). Bruk: «11–26 uker bak recovery» (H1), «14–20 uker bak original på sporene» |
| Verktøyforsinkelse | **Minst 5 uker (opptil 10,6 uker)**: forecast 6.5., men plattformleder skriver at verktøyet kom først 13.6. (EM-056); planlagt 31.3. | EM-052–056, VEN-002, OF-010 | **Åpen** (Lars Pettersen, Ole Martin Kvale). Påvirker kredittkravet |
| Uferdige integrasjoner (18 av 64) | **18 av 64**; leverandør 5–6, Nordflow beslutning/krav + testdata 10, delt 3 | TECH-005, VEN-002, EM-104 | Avklart. Nordflows og leverandørens tellinger er enige om kundesiden |
| Leverandørkreditt | **Krav 34**; «nær sikkert ~12»; leverandørens tilbud 24–34 *betinget* av scope-frys + felles plan | EM-062–068, VEN-002 | Avklart som posisjoner. Ikke avtalt beløp |
| Fornyelsesrisiko | **146 mill.** (5 kunder): **71 direkte** OneFlow-signal (EnergiVest 42, Skandia 29), **34 indirekte** via ressurstrekk (Nordbygg), **41 pris/marked** (Metrohandel 23, Svea 18). Ikke bruk «105 mill. OneFlow-effekt» uten forbehold | OPS-004, EM-149/150 | Avklart. Kontrollregnet av Person A (71 + 34 + 41 = 146) og bekreftet av Person C |
| Kundenavn for fornyelser | **Åpen.** OPS-004 (EnergiVest, Nordbygg, Skandia, Metrohandel, Svea) ≠ TH-022 (Fjordkraft, ScanMarine, MedicoLog, Vestbygg, Arctiq). Totalen 146 og «3 av 5» er like. *Ikke navngi kunder i styrepapirer* | OPS-004, EM-147–150, EM-164 | **Åpen** (Beate Høyer) |
| Inntekts-/resultateksponering | **Ikke bruk 27,6** (blandet sum). Bruk: **bekreftet kreditering 3,6**, **mulig ytterligere ≤ 7,2** (= resultatrisiko ≤ **10,8**), **arbeidskapital 16,8** (16,5 per 11.9), og **linjekost 11,2** hittil i 2026 (ikke i programprognosen); målbart i alt ≤ ~22 | OPS-005, EM-159/163, OPS-002 | Avklart. Person C og A |
| Linjekost 2026 | **11,2 mill.** (8,7 mill. var tilstanden 14.8.) | OPS-002, EM-138 | Avklart (tidsforskjell) |
| Pilot | **42 av 286** kunder (−85 %); 17 manuell fakturakontroll, 8 portal/ordreavvik, **7,8 %** fakturakorreksjon. Alle 42 ligger i manuell kontroll | OPS-003, EM-078, EM-087 | Avklart |
| Er Bølge 1 «i drift»? | **Åpen.** Pilotkundene (42) er migrert, 34 stabilisert (EM-087), men TECH-003 setter «Bølge 1 cutover» til 18.12.2026. Skriv «pilot på 42 er migrert; Bølge 1 er ikke avsluttet» | TECH-003, EM-085/087, OPS-003 | **Åpen** (Camilla Bruun, Lars Pettersen). Rettet i 01-situasjonsbilde |
| Bemanning | Plan **168**, reelt **119**, gap **49**; 37 over 120 %; 12 avganger siden januar (5 i data/integrasjon) | HR-002, EM-130–132 | Avklart |
| Beslutningskø | **Median 35,5 dager** mot mål 7; 12 kritiske saker, alle >4× mål, 6 åpne | OF-011, EM-030 | Avklart |
| Backfill-beslutning | Åpen i **56 dager** fra 18.7. (OF-011), eller **148 dager** fra R-029 (11.4., OF-009) til godkjenning 6.9. Begge riktige, ulike startpunkt. Godkjent maks 1,8 mill. i fire uker | OF-009, OF-011, EM-140 | Avklart |
| Eier av kunde-/inntektsrisiko | Ingen *formell* eier. Midlertidig: Eirik Solheim koordinerer operativt, finans følger beløp, Beate Høyer eier fornyelsesoversikten | OF-014, EM-038/039/151 | Avklart; formell eier skal besluttes |
| Leverandørnavn | Convergent (dokumenter) = antatt samme selskap som `synervia.example` (e-postdomene) | VEN-001/002, TH-009 | Åpen, men trolig anonymiseringsartefakt. Logg i evidensloggen |
| CIO | Rolf Nygaard (mars, OF-013) vs Amina Rahman (aug/sept, HR-001, OF-014) | OF-013, HR-001 | Sannsynlig personskifte. Ikke avklart |
| Dato for styremøte | Oppgaven: «i morgen» = 18.9.; Karin Eide 14.9. skriver «torsdag» (17.9.) | Nordflow-oppgave.md, EM-001 | Åpen, men uten betydning for analysen |

## Hva som er gjort og hva som gjenstår

- **Ferdig:** seks funnfiler med dom, kilder og AI-logg. Tall i oversikten er kontrollregnet mot originalfilene.
- **Gjenstår før levering:** (1) avklare de «Åpne» radene over, særlig kostnadsbroen og verktøyforsinkelsen; (2) vurdere om rapporteringspraksis skal testes som egen hypotese før den omtales i CEO-brief; (3) bygge de fem leveransene (CEO-brief, lederpresentasjon, 90-dagersplan, evidenslogg, AI-arbeidslogg) på disse tallene. AI-loggene i funnfilene er et godt utgangspunkt for AI-arbeidsloggen.

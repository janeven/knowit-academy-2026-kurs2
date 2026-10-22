# H2 – Leverandøren (Convergent) er hovedårsaken

**Eier:** Person A  ·  **Dato:** 2026-10-22  ·  **Status:** FERDIG – FALSIFISERT (som *primærårsak*)
**Dom:** **FALSIFISERT** som hovedårsak. Leverandøren er en reell, **medvirkende** årsak og bør føres som *forsterker* i felles konklusjon, ikke som rotårsak.

*Hypotesen er definert i [`../02-hypoteser.md`](../02-hypoteser.md) (avsnitt H2). Skala for sikkerhet: **fakta** = primærdata eller to uavhengige/motstridende kilder som er enige; **sannsynlig** = én god kilde; **antakelse** = ukontrollert.*

## 1. Testbare påstander

| # | Påstand (fra «Hva må være sant?») | Test (kilde + beregning) | Utfall | Sikkerhet |
|---|---|---|---|---|
| 1 | Leverandørfeil står for **mesteparten** av de 18 uferdige integrasjonene | TECH-005 (Nordflow, 9.9): 5 leverandør, 6 beslutning/krav, 4 testdata, 3 delt. VEN-002 (leverandøren): 5 / 10 kunde / 3 delt. Lars Pettersen EM-104: 6 / 5 / 4 / 3. Leverandørandel = 5–6 av 18 = **28–33 %**. Selv om *alle 3 delte* tillegges leverandøren: 8–9 av 18 = **44–50 %**. Av 64 totalt: 5–6 = 8–9 % | **Motbeviser** | **Fakta.** Nordflows egen telling og leverandørens er enige om kundesiden (10 av 18), selv om partene har motstridende interesser |
| 2 | Nordflows egne forsinkelser (beslutninger, testdata, scope) ville ikke gitt vesentlig forsinkelse uten leverandørens | Kontrafaktisk: *Hvis verktøyet kom 31. mars, kunne Bølge 1 gått som planlagt?* Nei: dataprofilering er forecast ferdig **31.10.2026** (TECH-003, planlagt 31.03.2025), 14 av 27 dataobjekter er godkjent, 9 av 23 prosesser signert, og rensekapasitet gir full migrering tidligst juni 2027 (EM-088). Kun 61 av 286 kunder hadde representative testløp i juli (EM-083). Datalederen: «Data er … den viktigste begrensningen» (EM-076). CIO: februar utilrådelig «selv ved full leverandørbemanning» (EM-189, bekreftet av test EM-190) | **Motbeviser** | **Sannsynlig.** Tre Nordflow-kilder (data, CIO, test) + datoene i TECH-003. Ingen uavhengig kritisk-sti-analyse finnes |
| 3 | Kontrakten gir Nordflow klart krav på kreditt nær 34 mill. | VEN-001: kreditt kun for avvik «som kan henføres til leverandøren»; manglende kundeforutsetninger gir leverandøren rett til planjustering; kontrakten «gir ikke grunnlag for å tilskrive hele programavviket én part». Nordflows egen kontraktsansvarlig: **~12 mill. nær sikkert**, 12–22 til krever forhandling (EM-065). Convergent tilbyr 24–34 *kun* mot scope-frys + felles styrt plan, avviser netto 34 og dokumenterer **31 kundeskapte forsinkelseshendelser** (VEN-002, EM-067) | **Motbeviser** | **Fakta** om hva kontrakten sier. Beløpet er forhandlingsposisjon (C) |
| 4 | Leverandørskapte forhold forklarer en dominerende del av *kostnadsoverskridelsen* | Nordflows eget maksimale krav er 34 mill. = **15 %** av brutto overskridelse mot ramme (506 − 280 = 226) og **31 %** av gapet mellom brutto og rapportert (506 − 395 = 111) [FIN-005, EM-173]. Krediten ligger dessuten allerede *i* netto 472 | **Motbeviser** | **Sannsynlig.** Brobeløpene (41/22/19/29) er ikke fordelt på årsak, så leverandørandelen er en *øvre* grense fra krav, ikke målt |
| 5 | Leverandøren har reelle, dokumenterte avvik | Ja: verktøy forsinket, to arkitektbytter, 5–6 integrasjoner med leverandørfeil, defekt i mappingmotoren, feil på nordisk fakturavariant og volumkjøring (EM-052–057, VEN-002, TECH-005). **Convergent erkjenner selv** verktøy, arkitektbytter og tre kritiske integrasjoner (VEN-002, EM-111). RAID R-014 er rød [OF-010] | **Støtter (delvis)** | **Fakta** |

## 2. Falsifiseringsforsøk

*Hva forsøkte jeg å motbevise, og hva fant jeg?*

- **Forsøk 1: kan leverandørandelen være høyere enn tellingene viser?** Nordflows plattformleder bestrider plasseringen i Convergents juni-telling (prisindeks og hendelseskø står som «kundebeslutning», men feilen ligger i levert mapping) [EM-100]. Hans egen telling gir 6 av 18 (33 %). Selv med alle «delte» saker lagt til leverandøren blir andelen 50 % og ikke «mesteparten». Konklusjonen holder under alle tre tellinger.
- **Forsøk 2: tendens over tid.** Leverandørskapte saker har *ikke* gått ned mens totalen falt: 4 av 21 (27.6., Convergents telling, EM-099) → 6 av 19 (12.8., EM-102) → 6 av 18 (9.9., EM-104) / 5 av 18 (TECH-005). Kundeskapte (beslutning + data) falt fra 14 til 9–10. *Tolkning (sannsynlig, klassifiseringen er omstridt):* når Nordflow rydder egne avhengigheter, blir leverandørandelen i resten synlig større (19 % → 33 %). Dette peker på at leverandørproblemene er reelle, men *bak* Nordflows egne i rekkefølge.
- **Forsøk 3: er leverandørens påstand om sene Nordflow-beslutninger bare retorikk?** Kryssjekket mot Nordflows egen beslutningslogg: 12 kritiske beslutninger brukte **29–56 dager** (4,1–8 uker) mot mål 7 [OF-011], i samme størrelsesorden som Convergents «4–9 uker» (VEN-002, EM-055). Plattformleder bekrefter at komplett testdata kom **17. juni, over tre uker for sent**, og at «akkurat dette testvinduet ble blokkert av oss» (EM-108). Programdirektøren er «enig i fakta» (EM-109). Leverandørens påstand er altså *delvis bekreftet av Nordflows egne data* (merk: loggen dekker 12 saker, Convergent nevner 11, ikke samme sett).
- **Forsøk 4: ledelsens egen fortelling.** Styrepakken 24. juni kaller leverandørens verktøy «hovedflaskehals» [BOARD-003], og risikorangeringen i OF-007 setter «leverandør» først. Dette er den offisielle versjonen av H2. De kontrollerte dataene (TECH-005, OF-010 med R-031/R-044/R-047 rød) peker mot Nordflow-eide avhengigheter.

## 3. «Hva ville fått oss til å endre mening?»

Observasjonene fra `02-hypoteser.md`, og hva jeg fant:

| Observasjon som ville endret mening | Funnet? |
|---|---|
| Uavhengig kritisk-sti-analyse viser at leverandørleveranser alene flytter sluttdato >50 % | **Nei, finnes ikke i korpuset.** Grenseberegning: selv om verktøyforsinkelsen er 5 uker, utgjør den 17 % av Bølge 1-forsinkelsen (31.5. → 18.12.2026 = 29 uker) og 29 % av integrasjonssporets 17 uker. Forsinkelser er ikke additive, så dette er kun en øvre/nedre ramme |
| Verktøyforsinkelsen er egentlig ~10 uker og ikke 5 | **Ja, delvis.** Verktøyet skulle vært i test 31.3. (EM-052). Alle dokumenter sier «fem uker» (6.5. forecast, EM-053/055, VEN-002, R-014), men plattformleder skriver at verktøyet *kom først 13.6.* og da feilet (EM-056). 31.3. → 13.6. = **10,6 uker** (6.5. → 13.6. = 5,4 uker). Med 10,6 uker blir andelen 37 % av Bølge 1-forsinkelsen og 62 % av integrasjonssporet. Dette *styrker* H2 på integrasjon/migrering og **øker leverandørkreditt-kravet**, men endrer ikke at data og prosess (Nordflow-eid) er bundet uavhengig av verktøyet. Må avklares (se §7) |

## 4. Alternative forklaringer testet

- **H3 (styring/beslutningsrett):** støttes av de samme dataene: ti av tolv kritiske beslutninger >30 dager [OF-011], to av fire lange prosesssaker ventet på «avklaring av beslutningsrett» (EM-117), og kundeskapte avhengigheter ≥ 50 % av de uferdige integrasjonene.
- **H4 (kapasitet):** Convergent peker selv på at «testdata og kundebeslutninger» var flaskehalser, og Nordflow mistet testressurser til linjen i mai og juli (EM-141–145).
- **Datakvalitet (Nordflow-eid):** 12,4 % → 11,7 % duplikater mot krav <2 %, kjent siden okt. 2025 (EM-069, EM-072, TECH-004).
- **Scope-vekst:** 47 endringer, 63 400 timer og 38 mill. «uten uttak» (EM-043); VEN-002 sier krav endret seg etter konfigurasjon, og TECH-005 har 3 saker med «endring etter bygg».

## 5. Dom og begrunnelse

**FALSIFISERT som hovedårsak.** Tre sentrale «må være sant»-punkter er motbevist: (1) leverandørfeil er 28–33 % av uferdige integrasjoner (maks 50 % under ekstrem allokering), bekreftet av *begge* parter; (2) Bølge 1 var blokkert av Nordflow-eide data-, prosess- og testdatagap uavhengig av verktøyet; (3) kontrakten gir ikke grunnlag for å tilskrive avviket én part, og vår egen kontraktsansvarlige regner kun ~12 mill. som sikkert. Leverandørens svikt er likevel reell og erkjent, og er en **forsterker** som bør følges opp kommersielt. *Det som ikke kan avgjøres:* hvor stor andel av *migreringssporets* forsinkelse som skyldes selve verktøyet, siden TECH-005 dekker integrasjoner og ikke migrering.

## 6. Kilder brukt

| Kilde-ID | Type (A–D) | Hva den viser | Merknad (kvalitet, versjon, konflikt) |
|---|---|---|---|
| TECH-005 | A | 18 av 64 uferdige; 5/6/4/3-fordeling | Nordflows eget, 9.9. Dekker integrasjoner, ikke migreringsverktøy |
| VEN-002 | C | 5/10/3-fordeling, 11 sene beslutninger, kredittvilkår | Leverandørposisjon, ikke avtalt årsaksfordeling (sier det selv). Dato «august» men nevner 18 uferdige (Nordflows august-telling var 19) |
| VEN-001 | A (utdrag) | Ansvarsdeling, kreditt- og planjusteringsvilkår | Kun utdrag; full kontrakt ikke i korpuset |
| OF-010 / OF-009 | A | RAID: R-014 verktøy rød, 5 uker; R-026/R-031/R-044 rød | RAID er rød *per 31.8.*, gul per 30.4. |
| OF-011 | A | 12 beslutninger, 29–56 dager | Kun 12 «kritiske»; 6 åpne; kan ikke direkte matches mot Convergents 11 |
| TECH-003 | A | Dataprofilering 31.10.2026 (orig. 31.3.2025), Bølge 1 18.12.2026 | Fremtidige datoer er prognose |
| FIN-005 / EM-173 | A | Brutto 506, kreditt −34, bro 41/22/19/29 | Brobeløp ikke fordelt på årsak |
| EM-052–061 | D | Tidslinje verktøy: 31.3. → 6.5. (forecast) → 13.6. (ankomst) | **Konflikt:** «fem uker» vs 10,6 uker |
| EM-062–068 | D | Kreditt: 12 sikkert, 24–34 krav, 31 kundeskapte hendelser | Forhandlingsposisjoner |
| EM-098–105 | D | Telling av uferdige integrasjoner over tid | Klassifisering omstridt (EM-100) |
| EM-106–111 | D | Testdata kom 17.6., >3 uker for sent; Nordflow bekrefter | Ellers lite omstridt |
| EM-076, EM-088, EM-189/190 | D | Data/CIO/test: data hovedbegrensning, februar utilrådelig selv med full leverandørbemanning | Alle tre er interne parter; CIO-dokument er utkast (TECH-002) |
| BOARD-003, OF-007 | B | Ledelsens bilde: leverandør «hovedflaskehals» | Kuratert, selektiv |

*Støy ikke brukt:* TH-032–040, OTHER-001 (Aurora). Merknad: e-post fra leverandøren har domenet `synervia.example`, mens dokumentene kaller selskapet Convergent. Antatt samme selskap (e-postene refererer til «Convergent»), sannsynligvis anonymiseringsartefakt, men bør nevnes i evidensloggen.

## 7. Åpne spørsmål / hva som mangler

1. **Faktisk ankomstdato for migreringsverktøyet** (6.5. «fem uker» vs 13.6.). Hvem: **Lars Pettersen / Ole Martin Kvale**, mot leveranselogg og kontraktens milepælsplan. Påvirker kredittkravet direkte.
2. **Kritisk-sti-analyse** som viser hva sluttdato ville vært med (a) leverandør i rute, (b) 7-dagers beslutninger, (c) full bemanning. Hvem: **Julie Nystad (PMO)**. Dette er testen som faktisk skiller H2/H3/H4.
3. **Leverandørandel av migreringssporet** (ikke bare integrasjoner): hvor mye av data/migrering (~20 uker bak) skyldes verktøyet vs. rensing? Hvem: **Camilla Bruun**.
4. **Hele hovedavtalen** (VEN-001 er et utdrag): milepælsplan, kredittmekanikk, bemanningsbestemmelse (arkitektkontinuitet, EM-054).

## 8. Til fellesmøtet *(fylles kun ut hvis dom er STØTTET eller STERKT STØTTET)*

*Ikke aktuelt: dommen er FALSIFISERT. Se under for det som likevel bør løftes til gruppen.*

**Funn som bør deles på tvers (ikke eskalering av H2, men nyttig for andre):**
- **Til H3-eier:** Leverandørens påstand om sene Nordflow-beslutninger (4–9 uker) er *bekreftet av Nordflows egen beslutningslogg* (29–56 dager). To uavhengige kilder peker på samme flaskehals.
- **Til felles tall / evidenslogg:** verktøyforsinkelse (5,4 / 10,6 uker) og leverandørnavn (Convergent vs `synervia.example`).
- **Til kreditt-/anbefalingsarbeidet:** Convergents kredittilbud (24–34) er betinget av scope-frys + felles styrt plan; deres plan forutsatte frys **15. sept.**, som er passert (EM-060). Kommersiell tidsfrist finnes, og den er sammenfallende med behovet for et konsernreset.

## 9. AI-bruk *(del av leveransen «AI-arbeidslogg»)*

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Selv kontrollert mot original |
|---|---|---|---|
| Lese hele korpuset, bygge første situasjonsbilde og hypoteser (tidligere økt) | Kildeoversikt og tall fra `01-situasjonsbilde.md` som *utgangspunkt* | — | Alle tall i tabellene over er re-verifisert mot originalfilene (CSV/MD/PDF, e-postene) i denne økten |
| Beregne andeler, uker og bidrag (awk) | Alle beregninger vist i teksten | — | Regnet om for hånd (5/18, 6/18, 8/18, 9/18; 31.3.→13.6. = 74 dager = 10,6 uker; 34/226, 34/111) |
| Dom og begrunnelse | Utkast fra AI | Skjerpet: skilte «primærårsak» (falsifisert) fra «medvirkende» (støttet) og la til forbehold om migreringssporet | Dom bør vurderes av teammedlem før den står i fellesoversikten |

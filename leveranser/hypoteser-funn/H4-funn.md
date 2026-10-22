# H4 – Kapasitetskonflikt mellom linje og program er hovedårsaken

**Eier:** Person B  ·  **Dato:** 2026-10-22  ·  **Status:** FERDIG – SVEKKET
**Dom:** SVEKKET som *primærårsak*. Godt støttet som *forsterker* av H3.

*Hypotesen er definert i [`../02-hypoteser.md`](../02-hypoteser.md) (avsnitt H4). Ikke endre den der. Skriv funn her.*

## 1. Testbare påstander

| # | Påstand (fra «Hva må være sant?») | Test (kilde + beregning) | Utfall | Sikkerhet |
|---|---|---|---|---|
| 1 | Gapet på 49 FTE ligger på kritisk sti | HR-002: hele gapet ligger i de tre kritiske sporene. Data og migrering 21/46 = **46 %** mangler, test og integrasjon 18/54 = **33 %**, prosess og kundeovergang 10/38 = **26 %**. People og PMO har 0. Totalt 49/168 = 29 %. EM-132: 12 + 7 + 4 = **23 roller er kritiske neste åtte uker**, altså 23/49 = **47 %** av gapet. | Støtter | **Fakta** (HR-002 A + EM-132) |
| 2 | Forsinkelser faller i tid sammen med ressurstrekk og avganger | Gapet er dokumentert fra januar 2026 (OF-004: data og test under plan) og februar (168 − 126 = **42**, EM-127), og var 49 i uke 35. Trekk 11.5 og 1.7 (EM-141, EM-143). Programdirektøren anslår at trekkene kostet ca. 6 uker i data og test (EM-145). 12 avganger siden januar (HR-002). | Støtter for 2026 | **Sannsynlig.** Seks uker er et enkeltanslag (D) fra en part. |
| 3 | Fylles gapet, forkortes kritisk sti uten at beslutningsretten endres | (a) 2 av 4 prosessaker venter på beslutningsrett, og det løser ikke kapasitet (EM-117). (b) Lokalkunnskap om gamle avtaler og grensesnitt kan ikke kjøpes (EM-132, EM-143). (c) Konflikten løses ikke fordi ingen prioriterer. HR-001 gir «ingen automatisk prioritet», det ble bedt om prioriteringsbeslutning i mars (EM-129) og igjen i august (EM-133, EM-145), og backfill tok 148 dager (R-029 11.4 → EM-140 6.9). | **Motbevist / svekket** | **Sannsynlig** |
| 4 | SLA-fallet er størst der folk er avgitt | OPS-002: «størst i enheter som har avgitt erfarne fagpersoner», men også fravær (7,1 %), sesong og marked. EM-136: køen er størst i NO og DK, der flest er avgitt. SLA har falt 95,8 → 91,4 = −4,4 pp på sju måneder. | Støtter delvis | **Sannsynlig.** Ingen data per enhet i korpuset. |

## 2. Falsifiseringsforsøk

- **«Forsinkelsene oppsto før kapasitetsproblemet»:** **Delvis lyktes.** Profilering (frist 31.3.2025) og prosessdesign (30.6.2025) gled allerede i 2025. Det første dokumenterte FTE-gapet er fra januar–februar 2026. For 2025 har vi ingen bemanningsdata. BOARD-001 sier bare at linjekapasiteten «ikke [var] endelig verifisert», og OF-001 at oppstart skjedde etter tre av seks ukers mobilisering. Det kan ha vært et kapasitetsproblem fra start, men beslutningen om å starte uten verifisert kapasitet er en styringsbeslutning (H3). Kapasitetsgapet forklarer ikke de tidligste datasvakhetene (EM-069, okt. 2025) eller scope-veksten (EM-043, nov. 2025).
- **«Backfill hjelper ikke fordi lokalkunnskap mangler»:** **Lyktes delvis.** EM-132 sier «noen roller» kan fylles eksternt, men ikke lokalkunnskap. Innleide «kan ikke vurdere gamle avtaler» (EM-143). Penger alene løser altså bare en del av de 23 kritiske rollene. Hvor stor del er ikke tallfestet.
- **«Gapet er en regnefeil»:** Feilet. EM-130 presiserer at tallet gjelder tilgjengelig kapasitet og ikke ubesatte stillinger, og 37 personer over 120 % er bekreftet i HR-002.

## 3. «Hva ville fått oss til å endre mening?»

- **Tidsserie som viser at gapet kom etter de store forsinkelsene:** Lette i OF-002, OF-004–007, HR-002 og TH-019. **Delvis funnet.** Datofestede forsinkelser i 2025 kommer før første målte gap (feb. 2026). Det finnes ingen kapasitetsdata for 2025, så rekkefølgen er **ikke avgjørbar** for 2025.
- **At kritiske roller ikke kan fylles innen åtte uker:** **Delvis funnet** (EM-132, EM-143), men uten antall.

## 4. Alternative forklaringer testet

- **Styring (H3):** Kapasitetskonflikten er i stor grad *en følge* av at ingen har tatt prioriteringsbeslutningen. Linjen trekker folk tilbake fordi den bærer SLA-ansvaret alene (EM-141, EM-143), og finansieringen sto åpen i 148 dager. Dette passer bedre med H3 som rot og H4 som mekanisme.
- **Sirkel, ikke enveis årsak:** Trekk gir programforsinkelse, som forlenger dobbeltlandskapet, som igjen gir mer belastning i drift og nye trekk (EM-137, EM-144). Det forsterker effekten, men sier ikke hva som startet den.
- **Motivasjon og endringsmotstand:** Avvist som hovedforklaring. Puls 32/100 på «beslutninger tas raskt nok», og HR peker på prioritering og roller (HR-003, EM-200, EM-201).

## 5. Dom og begrunnelse

**SVEKKET som primærårsak.** Gapet er reelt, ligger på kritisk sti og svekker både programmet og drift (fakta). Men påstand 3 holder ikke. Å fylle gapet løser ikke saker som venter på beslutningsrett eller krever lokalkunnskap. Konflikten består fordi ingen har tatt prioriteringsbeslutningen. Forsinkelsene i 2025 kan heller ikke knyttes til et målt kapasitetsgap. H4 bør derfor brukes som **forsterker** under H3, og tiltakene (skjerming av de 23 rollene, finansiert backfill, ingen dobbeltallokering) bør inngå i reset-pakken. *Merk: H4 er tatt med i H3-funn §8, slik at fellesmøtet ser begge sammen.*

## 6. Kilder brukt

| Kilde-ID | Type | Hva den viser | Merknad |
|---|---|---|---|
| HR-001 | A | Matrise uten prioritetsregel | |
| HR-002 | A | Plan 168 / reelt 119 / gap 49 per fagområde; 37 > 120 %; 12 avganger | **EM-130 merker gapene annerledes** (21 data/integrasjon, 18 prosess/test, 10 endring/opplæring), mens HR-002 viser 0 gap i opplæring. HR-002 er primærdata og legges til grunn. |
| HR-003 | A (opinion) | Puls: prioritering og beslutninger er hovedtemaer | Ikke årsaksbevis |
| OF-004 | B | Bemanning i data og test under plan allerede i januar 2026 | |
| OF-009 / OF-010 | A | R-029 backfill 11.4 (frist 6.5); R-047 kapasitetsgap rød | |
| OF-013 | A | Recovery forutsatte bekreftet linjekapasitet; «intern kapasitet» oppgitt som avviksårsak | |
| BOARD-001 | A | Linjekapasitet ikke verifisert ved vedtak | |
| OPS-001 / OPS-002 | A | KPI-fall; størst der folk er avgitt, men også fravær, sesong og marked | |
| EM-127–133 | D | 168 mot 126 (feb.), 37 > 120 % (mars), 23 kritiske roller | 37 > 120 % står både i mars (EM-129) og august (HR-002). Sjekk om tallet er oppdatert. |
| EM-134–145 | D | Trekk mai og juli, ca. 6 uker kostnad, backfill 1,8 mill. i 4 uker | OF-011 viser backfill som åpen (56 d), men den ble godkjent 6.9 (EM-140) |

## 7. Åpne spørsmål / hva som mangler

- **Bemanning i 2025** (plan mot faktisk per kvartal), for å avgjøre årsaksrekkefølgen: Henrik Dahl eller Lene Falk.
- **Hvor mange av de 23 kritiske rollene som kan fylles eksternt innen åtte uker:** Henrik Dahl.
- **SLA per enhet mot antall avgitte personer**, for å skille OneFlow-effekt fra fravær og sesong: Ingrid Mørk.
- **Er 37 > 120 % et nytt tall i august, eller videreført fra mars?** HR.

## 8. Til fellesmøtet

*Ikke påkrevd (dom SVEKKET). H4 diskuteres som forsterker under H3, se [H3-funn.md](H3-funn.md) §8.*

## 9. AI-bruk *(del av leveransen «AI-arbeidslogg»)*

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Selv kontrollert mot original |
|---|---|---|---|
| Lese HR-001–003, OPS-001/002, OF-004/009/010/013, BOARD-001 og tråd TH-019–021, 031 i sin helhet | Tall og sitater | Forkastet 02-hypotesers tolkning av EM-130-kategoriene til fordel for HR-002 | _Person B fyller ut_ |
| Regne andeler (46/33/26 %, 23/49, 42 → 49, 148 dager) | Ja | – | _Kontroller regnestykkene_ |
| Vurdere årsaksrekkefølge 2025 mot 2026 | Konklusjonen «ikke avgjørbar» | – | _Bør vurderes av teamet_ |

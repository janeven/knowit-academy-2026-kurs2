# OneFlow – 90-dagersplan

*Bygger på [`03-hovedanbefaling.md`](03-hovedanbefaling.md) (beslutningene D1–D6) og funnfilene i [`hypoteser-funn/`](hypoteser-funn/00-oversikt.md). Samme tall som resten av leveransene. «Basislinje» er målt verdi fra korpuset, og «Mål» er **vårt forslag** som eier kalibrerer innen dag 14, med mindre kilden er oppgitt.*

**Tidsanker (casetid):** Dag 0 = styremøtet **fredag 18.9.2026**. Dag 7 = 25.9, dag 14 = 2.10, dag 21 = 9.10, **dag 28 = 16.10 (Port 1)**, dag 59 = 16.11 (Port 2), **dag 90 = 17.12 (Port 3)**. Faste punkter utenfra: styringsgruppen **22.9**, banken **25.9**, fornyelsene **15.10 / 31.10 / 30.11 / 15.12 / 31.12**, dataprofilering **31.10** (TECH-003), Bølge 1 cutover **18.12** (TECH-003, dagen etter dag 90) og styrets formelle sluttdato **31.12**.

---

## 1. Prioritering og logikk

Planen er sekvensert etter *hva som må på plass før noe annet virker*, ikke etter størrelse. Rotårsaken (H3) må løses først. Ellers bruker alle andre tiltak samme beslutningskø som har ligget stille i 35,5 dager.

| Prioritet | Hva | Hvorfor først | Tiltak |
|---|---|---|---|
| **P1 – Denne uken** (dag 0–7) | Gjør det mulig å beslutte og beskytt det som ikke kan erstattes | Uten beslutningsregime, scope-frys og skjermede nøkkelpersoner har ingenting annet effekt (H3, H4). Ingen av dem koster mye, og alle er lav-anger. | T1–T6 |
| **P2 – Dag 7–28** (frem til Port 1) | Skaff fakta og trygg kunder og penger | Må være klart før styret kan sette ny ramme. Fornyelser forfaller fra 15.10. | T7–T11 |
| **P3 – Dag 28–90** | Gjenoppbygg datagrunnlag og plan, og gjenoppstart kontrollert | Avhenger av beslutningene i P1 og fakta fra P2. | T12–T16 |
| **Gjennomgående** | Styring og åpenhet | Hver port er en reell stoppmulighet. | T17 |

---

## 2. Tiltak

*Ansvarlig = én person som svarer for resultatet (**A**). «Bidrar» er de som må levere. Navn og roller er hentet fra HR-001 og OF-014. Der vi foreslår en ny rolle, står det «forslag».*

### P1 – Denne uken (dag 0–7)

| ID | Tiltak | Ansvarlig / bidrar | Tid | Avhenger av | Forventet effekt | Mål for å lykkes |
|---|---|---|---|---|---|---|
| **T1** | **Scope-frys med unntaksprosess.** Fortsett og formaliser SG-vedtaket 10.9 (ingen nye forbedringsønsker). Unntak kun for regulatoriske, kontraktsmessige og driftskritiske behov, dokumentert. Triager de 47 oppsamlede endringene til «inn / ut / utsatt». | **Thomas Vik** (SG-leder) / Julie Nystad, Nora Steen | Vedtas 22.9. Triage ferdig dag 21 (9.10). | D2 (CEO-mandat) | Stopper kravveksten (47 endringer, 63 400 timer, 38 mill.). Oppfyller vilkåret for Convergents kreditt (T11). | **0** nye ønsker godkjent utenom dokumenterte unntak. **47/47** triagert dag 21 (bare 19 hadde full konsekvensanalyse). |
| **T2** | **Beslutningsregime.** Navngitt beslutningstaker per sakstype. **72 timers frist med automatisk eskalering til CEO.** Krav til innhold i beslutningsunderlag (alternativer og operativ konsekvens). Beslutningsloggen rapporteres ukentlig med eier og frist. | **Karin Eide** (CEO) / Julie Nystad (logg), Thomas Vik | Vedtas 22.9. Gjelder fra dag 7. | D2 | Fjerner hovedårsaken (H3). Beslutningene blokkerer i dag 10 av 18 uferdige integrasjoner og hele data- og testkjeden. | Kritiske saker avgjort innen **72 t** (basislinje: alle 12 tok >29 dager). **Median ≤ 7 dager** fra dag 28 (basislinje 35,5). Ingen sak eskalert to ganger. |
| **T3** | **Lukk de seks åpne kritiske sakene.** Bl.a. dataeier for kontraktsmaster (åpen ≥32 dager), ordre-til-faktura-eier, testmiljø 3 (31 dager), prisindeks/servicekreditt, scope-modell. De fire prosessene som har stått 36–52 dager skal avgjøres. | **Håkon Berg** (programdirektør) / deciders etter T2, Camilla Bruun, Nora Steen | Dag 0–14 (2.10) | T2 | Åpner avhengighetskjeden data → prosess → integrasjon → test → kunde (OF-012). | **6/6** åpne kritiske saker avgjort dag 14. Alle fire ventende prosesser avgjort dag 14. |
| **T4** | **Prioriteringsregel linje vs. program + skjerming av kritiske roller.** CEO fastsetter regelen (i dag «ingen automatisk prioritet», HR-001). Skjerm de **23** kritiske rollene (12 + 7 + 4), og fjern dobbeltallokering. Ingen flere tilbakeføringer til linjen uten CEO-beslutning. | **Karin Eide** (regel) / Eirik Solheim, Håkon Berg, Lene Falk, Henrik Dahl | Regel 22.9. Skjerming ferdig dag 14. | D2 | Stopper frem-og-tilbake-trekket (anslått seks ukers tap i data og test) og avgangene (12 siden januar). | **23/23** roller navngitt og skjermet dag 14. **0** nye tilbakeføringer. **0** nye avganger blant de 23 (basislinje: 12 avganger totalt, 5 i data/integrasjon). Personer over 120 %: 37 → **≤ 15** dag 28 → **0** dag 60. |
| **T5** | **Én formell eier av kunde- og inntektsrisiko + plan per fornyelse.** *Forslag:* Eirik Solheim som formell eier (koordinerer allerede operativt), Beate Høyer for fornyelsesoversikten. En lederplan per kunde. Avklar kundenavn først. | **Karin Eide** (utnevner 22.9) / Eirik Solheim, Beate Høyer, Mari Heggen, Ragnhild Moen | Eier utnevnt 22.9. Plan per kunde dag 7 (25.9). Årsakskoding dag 14. | Navneavklaring OPS-004 mot TH-022 | Sikrer at 146 mill. årlig kontraktsverdi (71 direkte OneFlow-signal, 34 indirekte, 41 pris/marked) har en eier før første frist 15.10. | **5/5** fornyelser med navngitt leder og plan dag 7. R-051 har eier dag 2. **Ingen** oppsigelse som begrunnes med faktura- eller portalfeil. Alle fem fornyelser besluttet før 31.12. |
| **T6** | **Rebaser økonomien og avklar kostnadsbroen.** Avklar om kreditten (34) allerede ligger i 395, så gapet er 77 eller 111. Bruk **472 netto (455–494)** i all rapportering fra dag 0. | **Thomas Vik** / Silje Tran | Bro avklart dag 7. Ny prognose dag 21. | Ingen | Fjerner de to tallene som forvirrer mest (395 mot 472, og +77 mot +111). Tallgrunnlag for ramme på Port 1. | Én tallserie i alle dokumenter dag 7. Brosummen avstemt til 472 dag 7. Ny prognose med scenarioer dag 21. |

### P2 – Dag 7–28 (frem til Port 1, 16.10)

| ID | Tiltak | Ansvarlig / bidrar | Tid | Avhenger av | Forventet effekt | Mål for å lykkes |
|---|---|---|---|---|---|---|
| **T7** | **Pause nye bølger og fakturakontroll i piloten.** Ikke åpne Bølge 2 og 3, og ikke utvid Bølge 1 utover 42 kunder, før kriteriene er oppfylt. Løs årsakene til manuell kontroll i pilotens 42 kunder (fakturamottaker, pris- og servicekredittregler, portal- og ordreavvik). | **Ragnhild Moen** / Ingrid Mørk, Camilla Bruun, Silje Tran | Dag 0–59. Gjenåpningsvurdering Port 2. | T3, T12 | Hindrer at problemet skalerer fra 42 til 286 kunder (5,7 × kundedriftens kapasitet på 50). | Fakturakorreksjon **7,8 % → < 2,5 %**. Manuell kontroll **17 → < 5** kunder (Ingrid Mørks krav, EM-097). Portal-/ordreavvik **8 → 0**. |
| **T8** | **Uavhengig teknisk verifikasjon av kjernen** (Nexus/ERP) og migreringsverktøyet. Skal også vurdere om de fire danske punktene kan modelleres. | **Amina Rahman** (bestiller) / ekstern part **som rapporterer direkte til CEO**, Lars Pettersen | Bestilt dag 7. Rapport dag 28 (16.10). | Ingen | Gjør H5 endelig. Fjerner den største usikkerheten bak «fortsett». | Rapport med klar konklusjon dag 28. **Uavhengighet:** CIO har selv skrevet reset-anbefalingen (TECH-002), så rapporten må ikke gå via henne. |
| **T9** | **Ekte NPV** på 472 / 128 / redusert kjerne, og kontroll av gevinstprofilen (FIN-001 summerer til 602, ikke 620). | **Thomas Vik** / Silje Tran | Dag 7–21 | T6 | Erstatter vår grovmodell (break-even 44–83 mill./år mot 128) med et tall Finance står inne for. | NPV for tre scenarioer dag 21. Beslutningsgrunnlag for Port 1. |
| **T10** | **Kritisk-sti-analyse** med tre scenarioer: beslutninger på 7 dager, leverandør i rute, full bemanning. Gir ny bottom-up plan og bekrefter eller revurderer 30.6.2027. | **Håkon Berg** / Julie Nystad, Lars Pettersen | Dag 7–21. Plan ferdig dag 28. | T3, T6 | Tallfester H3-effekten (ikke gjort i dag) og skiller H2/H3/H4. Gir styret en dato som er mer enn et fagestimat. | Analyse dag 21. Ny plan med sluttdato dag 28. Forskjellen mellom scenarioene er forklart. |
| **T11** | **Kommersielt spor mot Convergent.** Scope-frys og felles styrt plan som vilkår for kreditt. Skriftlig avklaring av verktøyforsinkelsen (6.5 mot 13.6). Krev bindende plan (den er «indikativ» i dag). | **Thomas Vik** / Ole Martin Kvale, Lars Pettersen | Dag 0–28 | T1 (frys må være på plass) | Sikrer kreditten (24–34 mill. betinget av frys og plan) og begrenser eksponeringen mot 506. | Skriftlig avtale om scope-frys og felles plan dag 21. **≥ 12** mill. kreditt skriftlig dag 28. Mål 24–34. Verktøyforsinkelse (5 eller 10,6 uker) fastslått dag 14. |

### P3 – Dag 28–90

| ID | Tiltak | Ansvarlig / bidrar | Tid | Avhenger av | Forventet effekt | Mål for å lykkes |
|---|---|---|---|---|---|---|
| **T12** | **Data og forretningsregler.** Navngi dataeier. Entydig struktur for fakturamottaker, prisindeks og servicekreditt. Rens etter reglene, ikke omvendt. | **Camilla Bruun** / dataeier (navngis i T3), Beate Høyer, Mikkel Sørensen | Dag 0–90. Dataprofilering ferdig 31.10 (planen, utfordres Port 1). | T3, T8 | Fjerner kilden til pilotavvikene (regler og eierskap, ikke plattform). Åpner for kundeovergang. | Kritiske objekter **14/27 → 27/27** innen planlagt dato. Duplikater **11,7 % → ≤ 4 %** dag 90 (krav til migrering < 2 %). Uklar fakturamottaker **8,4 % → ≤ 3 %**. |
| **T13** | **De fire danske kontraktspunktene** (indeksvarsling, servicevindu, separat fakturamottaker, oppsigelse). Endelig fagbekreftelse og design som unntak fra scope-frys. | **Beate Høyer** / Mikkel Sørensen, Nora Steen, Lars Pettersen | Bekreftet dag 21. Designet dag 45. | T1 (unntak), T8 | Åpner eller lukker H5 for Danmark. Må løses før dansk migrering (Bølge 3, i dag 30.6.2027). | **4/4** fagbekreftet dag 21. **4/4** designet og testet dag 59. |
| **T14** | **Prosess og integrasjoner.** Signer de gjenstående prosessene. Lukk de 18 uferdige integrasjonene, og prioriter de ti som er kundeskapt og venter på beslutning eller testdata. | **Nora Steen** (prosess), **Lars Pettersen** (integrasjon) / Camilla Bruun (testdata), Convergent | Dag 14–90 | T3, T11, T12 | Fjerner den tekniske kritiske stien. | Prosesser signert **9/23 → ≥ 16/23** dag 59 → **23/23** i ny plan. Integrasjoner uferdige **18 → ≤ 12** dag 45 → **≤ 8** dag 90. *Forbehold:* trenden har vært ca. 1 per måned (21 → 19 → 18), og målet forutsetter at T3 frigjør de kundeskapte. |
| **T15** | **Finansiert backfill og kundedrift.** Kartlegg hvilke av de 23 rollene som kan fylles eksternt (lokalkunnskap kan ikke kjøpes). Finansier backfill i drift utover 1,8 mill. / fire uker. Stabiliser SLA og kø. | **Thomas Vik** (finansiering) / Henrik Dahl, Eirik Solheim, Ingrid Mørk | Kartlegging dag 14. Backfill dag 14–56. | T4, T6 | Reduserer gapet (49 FTE, 37 over 120 %) og snur kundedriften. | Fylbare roller fylt dag 56. SLA **91,4 → ≥ 91,4** dag 28 → **≥ 93,0** dag 90 (juni-nivå). Svartid **132 → ≤ 91 sek.** Kø fra over 1 900 saker til synkende fra dag 28. |
| **T16** | **Kontrollert gjenoppstart.** Gå/ikke gå for Bølge 1 cutover (18.12) og for å åpne Bølge 2, basert på målte kriterier. Ingen bølge åpnes på dato alene. | **Håkon Berg** / Ragnhild Moen, Lars Pettersen, Ingrid Mørk | Port 2 (16.11) og Port 3 (17.12) | T7, T12, T14 | Gjør neste bølge til en beslutning med bevis, ikke en dato. | Alle kriterier oppfylt: korreksjon < 2,5 %, manuell kontroll < 5, ingen uløst fakturaeier, representativ test uten alvorlighetsgrad 1–2 for bølgen (i dag 38 av 286 uten slike feil). |

### Gjennomgående

| ID | Tiltak | Ansvarlig / bidrar | Tid | Avhenger av | Forventet effekt | Mål for å lykkes |
|---|---|---|---|---|---|---|
| **T17** | **Styring og åpenhet.** (a) Legg frem 472 for styret og banken (25.9), ikke 395. (b) Ukentlig CEO-rapport med én tallserie, begge baselines (original og recovery) og uredigerte avvik fra arbeidsstrømledere. (c) Kvartalsvis styrerapport med kostnadsprognose, gevinster, kundepåvirkning og de fem største risikoene (BOARD-002). (d) Tre porter for styret: dag 28, dag 59, dag 90. | **Karin Eide** / Thomas Vik (bank og styre), Julie Nystad (rapport) | Dag 0 og løpende | D1 | Gir styret og banken reelt beslutningsgrunnlag. Fanger avvik før de blir uker. Rapporteringen er i dag et funn, ikke en slutning om hensikt. | Bank og styre mottar 472 på dag 7. Ukentlig rapport fra dag 7. Portmøtene gjennomføres med stoppkriteriene som sakspunkt. |

---

## 3. Tidslinje og porter

| Når | Hendelse | Beslutning / leveranse |
|---|---|---|
| **Fre 18.9 (dag 0)** | Styremøte | D1–D6 godkjent. |
| **Tir 22.9** | Styringsgruppen | T1, T2, T4, T5 vedtas (OF-014 skulle ha behandlet reset, scope-modell og eierskap denne dagen). |
| **Fre 25.9 (dag 7)** | Bank | 472 legges frem. T5-plan per kunde. T6-bro avklart. Verifikasjon (T8) bestilt. |
| **Fre 2.10 (dag 14)** | Første kontrollpunkt | T3 og T4 ferdig. Verktøyforsinkelse avklart. Backfill-kartlegging ferdig. |
| **Tor 15.10** | Første fornyelse | Metrohandel (pris/marked, 23 mill.). |
| **Fre 16.10 (dag 28)** | **PORT 1** | Verifikasjon (T8), NPV (T9), kritisk sti (T10), kreditt (T11). Styret setter ny ramme og vurderer stoppkriteriene. |
| **Lør 31.10** | Fornyelse + dataprofilering | EnergiVest (42 mill., direkte OneFlow-signal). Dataprofilering planlagt ferdig (T12). |
| **Man 16.11 (dag 59)** | **PORT 2** | Gjenåpningskriterier (T7, T16), go/no-go for Bølge 1 cutover. |
| **Man 30.11** | Fornyelse | Nordbygg (34 mill., indirekte via ressurstrekk). |
| **Tir 15.12** | Fornyelse | Skandia (29 mill., direkte OneFlow-signal). |
| **Tor 17.12 (dag 90)** | **PORT 3** | Gjennomgang av alle mål. Bølge 1 cutover er planlagt 18.12. |
| **Tor 31.12** | Formell sluttdato (styret) | Svea Terminal (18 mill., marked). |

### Stoppkriterier ved Port 1 (fra hovedanbefalingen)

Planen endres hvis én av disse inntreffer: (1) verifikasjonen finner strukturelle arkitekturfeil, (2) NPV er negativ også for en redusert kjerne, (3) de fire danske punktene lar seg ikke modellere, (4) kritiske beslutninger fortsatt tar over 72 timer, eller (5) Convergent avviser scope-frys som vilkår. Da går saken tilbake til styret med alternativ C (redusert kjerne eller stopp) eller en kommersiell eskalering.

---

## 4. Avhengigheter (kritisk kjede)

```
D2 (CEO-mandat) ──► T2 beslutningsregime ──► T3 seks åpne saker ──┬─► T12 data/regler ──► T14 integrasjoner ──┐
                 └─► T1 scope-frys ───────► T11 Convergent-kreditt │                                          ├─► T16 gjenoppstart
                 └─► T4 skjerm 23 roller ─► T15 backfill ──────────┘   T13 DK-punkter ──────────────────────────┤   (Port 2/3)
T6 kostnadsbro ──► T9 NPV ─┐                                          T7 fakturakontroll pilot ──────────────────┘
T8 uavhengig verifikasjon ─┼─► PORT 1 (16.10) ──► ny ramme / stoppkriterier
T10 kritisk sti ───────────┘
```

**Avhengigheter som kan velte planen:** (1) D2 må vedtas 22.9. Alle P1-tiltak er blokkert uten CEO-mandat. (2) T1 må være på plass før T11. Uten frys faller kredittilbudet. (3) T4 (skjerming) må skje før T15 (backfill). Å fylle et gap uten prioriteringsregel gir samme tilbakeføring som i mai og juli.

---

## 5. Mål i ett blikk (basislinje → Port 1 → dag 90)

| Mål | Basislinje | Dag 28 | Dag 90 | Kilde for basislinje |
|---|---|---|---|---|
| Beslutningstid kritiske saker | Median 35,5 dager, 12/12 over mål | ≤ 72 t, median ≤ 7 dager | Vedlikeholdt | OF-011 |
| Åpne kritiske saker | 6 | 0 | 0 | OF-011 |
| Kritiske roller skjermet | 0/23 | 23/23 | 23/23 | EM-132 |
| Personer over 120 % | 37 | ≤ 15 | 0 | HR-002 |
| Uferdige integrasjoner | 18/64 | ≤ 14 (T14 delmål dag 45: ≤ 12) | ≤ 8 | TECH-005 |
| Prosesser signert | 9/23 | – | ≥ 16/23 (dag 59) → 23/23 i ny plan | EM-116/118 |
| Pilot fakturakorreksjon | 7,8 % | < 5 % | < 2,5 % | OPS-003 |
| Manuell fakturakontroll | 17 kunder | ≤ 10 | < 5 | OPS-003, EM-097 |
| SLA | 91,4 % | ≥ 91,4 % | ≥ 93,0 % | OPS-001 |
| Fornyelser med plan | 0/5 | 5/5 | 5/5 besluttet | OPS-004 |
| Leverandørkreditt skriftlig | 0 | ≥ 12 mill. | 24–34 mill. | EM-065, VEN-002 |
| Tall rapportert til styre og bank | 395 | 472 | 472 (oppdatert) | BOARD-004, FIN-005 |

---

## 6. Risiko for planen selv

| Risiko | Konsekvens | Håndtering |
|---|---|---|
| Programdirektøren og CIO er uenige om reset og frys (OF-014). | T1 og T11 forsinkes. Kreditten faller. | CEO avgjør 22.9 (D2), ikke SG-konsensus. |
| Drift «kan ikke avgi ytterligere kapasitet» (Eirik Solheim). | T4 og T5 konkurrerer om samme folk. | Backfill i drift (T15) finansieres før kritiske roller trekkes mer. Prioriteringsregelen settes av CEO. |
| Mange av de 23 rollene er lokalkunnskap som ikke kan kjøpes. | Backfill dekker bare en del. | Kartlegg dag 14. Behold nøkkelpersoner (0 avganger blant de 23) fremfor å erstatte dem. |
| Verifikasjonen (T8) peker på en strukturell feil. | Hovedanbefalingen må endres. | Port 1 er laget for dette (stoppkriterium 1). |
| Fornyelser forfaller før tiltakene virker (første 15.10, første med direkte signal 31.10). | Tap av kontraktsverdi. | T5 skjer i uke 1, men effekten av T7 kommer først etter Port 2. Aksepter at de to første fornyelsene avgjøres på lederplan, ikke på løst fakturakontroll. |

---

## 7. Kilder og åpne punkter

- Basislinjene er fra [`00-oversikt.md`](hypoteser-funn/00-oversikt.md) og funnfilene. Navn og roller fra HR-001 og OF-014. Fornyelsesverdier fra OPS-004. **Kundenavn er ikke brukt** (OPS-004 ≠ TH-022).
- **Åpent:** kritisk sti er ikke analysert (T10 skal gjøre det), hvor mange av de 23 rollene som kan fylles eksternt er ukjent (T15), og kreditt i 395 er uavklart (T6).

## 8. AI-bruk (til AI-arbeidsloggen)

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Må kontrolleres av teamet |
|---|---|---|---|
| Bryte hovedanbefalingen ned til tiltak med ansvarlig, tid, avhengigheter, effekt og mål | Basislinjer, datoer og navn fra kildene | **Alle målverdier (kolonnen «Mål») er AI-forslag**, ikke funn. Basislinjene er fra korpuset. Forkastet å navngi kunder og å love et NPV-tall. | (1) **Ansvarlige:** T5-forslaget om Eirik Solheim som formell eier og T8-oppsettet (ekstern part rapporterer til CEO) er vår vurdering. (2) **Datoene** er regnet fra 18.9 (casetid). (3) Mål som «≤ 8 integrasjoner dag 90», «duplikater ≤ 4 %» og «SLA ≥ 93,0 %» har ingen kilde og bør kalibreres av eierne. |

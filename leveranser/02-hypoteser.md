# OneFlow – konkurrerende hypoteser (Oppgave 2)

*Utgangspunkt: konsernsjefens mandat (4 spørsmål: status, årsaker, konsekvens, beslutninger) og korpuskartet under. Seks hypoteser som hver gir et ulikt svar på «hva er galt og hva må gjøres». H2–H5 konkurrerer om hva som er **primær årsak**. H1 er «offisiell linje» og H6 gjelder **konsekvensen**. Hypotesene utelukker ikke hverandre i virkeligheten, men er formulert skarpt for å kunne testes. Vurderingen («støtte i dag») bygger på det vi har lest, ikke på ferdig analyse.*

---

## Korpuskart – hva vi har og hvor godt vi kan stole på det

| Område | Filer | Hva de gir | Pålitelighet / fallgruver |
|---|---|---|---|
| **Program (OneFlow)** | OF-001 mandat, OF-002 roadmap, OF-003/013 recovery, OF-004–008 statusrapporter, OF-009/010 RAID, OF-011 beslutningslogg, OF-012 avhengigheter, OF-014 SG-referat | Plan, status, beslutningsflyt | Statusrapportene (B) er kuraterte (gul, omdefinerte milepæler). OF-008 er *ikke godkjent* utkast, men mest ærlig. Beslutningslogg og RAID er primærdata (A). |
| **Ledelse/styre** | BOARD-001–005, MGMT-001 | Hva styret vedtok og ble fortalt | Styrepakker (B) er selektive. Protokollene (A) viser hva styret faktisk visste og bestilte. Risikovedlegget mangler. |
| **Økonomi** | FIN-001–007 | Business case, bottoms-up, kontrollert prognose, gevinstavstemming | **FIN-005/007 (16.9) og FIN-006 er autoritative.** FIN-003/004 er mellomversjoner. FIN-002 er Cobalt-case. |
| **Teknologi** | TECH-001–005 | As-is, CIO-review, plan, datakvalitet, integrasjoner | TECH-004/005 (A). TECH-002 er *utkast* av en part med anbefaling. |
| **Drift og kunde** | OPS-001–005 | KPI, SLA, pilot, fornyelser, inntektsavstemming | (A) men blandet: OPS-005 summerer ulike kategorier. Kundenavn i OPS-004 ≠ e-post TH-022. |
| **HR** | HR-001–003 | Org, bemanning, puls | (A). Pulsmåling er opinion, ikke årsaksbevis. |
| **Leverandør** | VEN-001, VEN-002 | Kontrakt, leverandørens posisjon | VEN-002 er en *forhandlingsposisjon* (C). VEN-001 er kun utdrag. |
| **E-post** | 40 tråder (TH-001–031 relevante) | Hvem sa hva når. Viser uenighet og beslutningshistorikk | (D) enkeltsyn. Svarer ofte på spørsmål dokumentene ikke gjør. |
| **Støy** | TH-032–040, OTHER-001 (Aurora), `__MACOSX`, `.DS_Store`, CaseCorpus.zip | Rekruttering, kontorflytting, fest, PC-er, ESG, småsaker, reise | Skal *ikke* brukes som bevis. Aurora og TH-039 tester om vi feilattribuerer. |

**Tommelfingerregler for evidens:** kontrollert primærdata slår styrepakke; dato og versjon avgjør (FIN-005 > FIN-004 > FIN-003); to uavhengige kilder som stemmer (f.eks. TECH-005 og VEN-002 om 10 av 18 kundeskapte) veier tungt; enkeltuttalelser i e-post er hypoteser, ikke fakta.

---

## Oversikt

| # | Hypotese (kortversjon) | Støtte i dag | Hovedhandling hvis sann |
|---|---|---|---|
| **H1** | Situasjonen er håndterbar, og mye er rapporteringsstøy. Recovery fungerer; fortsett. | **Svært lav** | Fortsett recovery til 22. sept./slutten av september |
| **H2** | Primærårsak er leverandøren (Convergent). | **Lav–middels** (reell, men ikke dominerende) | Kommersiell eskalering, evt. bytte/reforhandle |
| **H3** | Primærårsak er Nordflows styring: beslutningsrett, porter, scope. | **Høy** | Konsernreset med beslutningsrett, portkriterier, scope-frys |
| **H4** | Primærårsak er kapasitetskonflikt mellom linje og program. | **Middels–høy** (sterk forsterker) | Skjermet kapasitet + finansiert backfill |
| **H5** | Løsningen/kjernen er ikke levedyktig i dagens form (teknologi/data/standardisering). | **Lav–middels** | Redesign, kraftig scope-kutt eller stopp |
| **H6** | Kunde-/inntektsskaden er større og mer akutt enn programkost, og må styre rekkefølgen. | **Middels** (avhenger av én ubekreftet kobling) | Kundesikring først, stans neste bølge, én eier |

Mest sannsynlig i virkeligheten: **H3 som kjerne, forsterket av H4, med H2 som reell, men mindre medvirkende årsak.** H6 avgjør rekkefølgen på tiltakene. H1 og H5 er de sterkeste «feilspor» vi bør kunne avvise med bevis, ikke bare med magefølelse.

---

## H1 – «Gul og håndterbar»: recovery virker, og avviket er mest definisjonsstøy

**Påstand.** Programmet er i hovedsak på vei mot 28. feb. 2027 og 395 mill. Forskjellene mot underlaget skyldes hovedsakelig ulike definisjoner (original vs. recovery, «teknisk klar» vs. «godkjent»). Kundeproblemene er enkeltsaker i linjen. Riktig grep er å fortsette og avgjøre reset først når leverandørkreditten er klar.

**Hva må være sant?**
- Når alle definisjoner normaliseres (godkjent, ikke teknisk klar), er sporene fortsatt innenfor ca. 4 uker av recovery-datoene.
- De 395 kan forsvares: bottoms-up (438/459/472) består av ubestilte og ufinansierte risikoer som sannsynligvis ikke inntreffer.
- Piloten viser at skalering til 286 er mulig uten ny runde med rensing og beslutninger.
- SLA-fallet er sesong/fravær, ikke ressursuttak til OneFlow.

**Kilder å undersøke.** OF-003/013 (forutsetningene for recovery), OF-007/008, TECH-003 (nåværende prognose), FIN-003–005, OPS-001/002/003, EM-010/013/168 (programdirektørens begrunnelse), EM-089.

**Hva kan falsifisere den?** Recovery-planen *forutsatte selv* 7-dagers beslutninger, stabile krav fra april, bekreftet linjekapasitet og ukentlig leverandørrecovery. Alle fire er brutt [OF-013, OF-011, EM-141–145]. TECH-003 viser Bølge 1 cutover 18. des. mot recovery 30. sept. (11 uker). Finans' kontrollerte tall er 472 og ikke 395 [EM-173]. Dette er allerede nok til å falsifisere H1 på kostnad og dato.

**Hva ville fått oss til å endre mening?** Hvis (a) en revidert, godkjent milepælsdefinisjon viser at sporene faktisk er innenfor 4 uker av recovery; (b) Silje Tran bekrefter at 472 er en risikosum og ikke forventet verdi; eller (c) Bølge 1 kan utvides til flere hundre kunder med korreksjonsrate <2,5 %. Ingen av disse er i korpuset.

**Handling hvis sann.** Fortsett recovery, beslutt reset etter kreditt.

---

## H2 – Leverandørhypotesen: Convergent er hovedårsaken

**Påstand.** Verktøyet kom for sent og feilet, arkitekter byttet, integrasjoner leveres med feil. Programforsinkelsen er hovedsakelig leverandørens ansvar og bør løses kommersielt (kreditt, evt. leverandørbytte).

**Hva må være sant?**
- Leverandørfeil står for mesteparten av de 18 uferdige integrasjonene og av kritisk sti-forsinkelse.
- Nordflows forsinkelser (beslutninger, testdata, scope) ville ikke ha gitt vesentlig forsinkelse *uavhengig* av leverandørens.
- Kontrakten gir Nordflow klart krav på kreditt nær 34 mill. (ikke 12).

**Kilder å undersøke.** VEN-001 (kundens forutsetninger, planjustering), VEN-002, TECH-005, EM-052–061 og EM-062–068 (kreditt), EM-098–105, EM-106–111 (testdata), RAID R-014.

**Hva kan falsifisere den?** I begge tellinger er **bare 5–6 av 18** integrasjoner leverandørskapte, og **9–10** kundeskapte [TECH-005, VEN-002, EM-104]. Convergent viser til elleve sene beslutninger (4–9 uker), 31 kundeskapte forsinkelseshendelser, og Nordflows plattformleder bekrefter at testdata kom over tre uker for sent [EM-055, EM-067, EM-108]. VEN-001 sier eksplisitt at kontrakten *ikke* kan tilskrive hele avviket én part. Prosess-, data- og beslutningssporene (som ikke er leverandørens) er 14–20 uker bak.

**Hva ville fått oss til å endre mening?** Hvis en uavhengig kritisk-sti-analyse viser at leverandørleveranser (verktøy, arkitektkontinuitet) alene flytter sluttdato mer enn 50 % av forsinkelsen, eller hvis verktøyforsinkelsen faktisk er ~10 uker og ikke 5 (verktøyet kom først 13. juni [EM-056]).

**Handling hvis sann.** Eskaler kommersielt, krev full kreditt, vurder bytte. **Merk:** Dette er også den hypotesen som er mest komfortabel for Nordflow internt, og derfor den som krever sterkest bevis.

---

## H3 – Styringshypotesen: roten er at Nordflow ikke styrer programmet

**Påstand.** Portkriteriene ble ikke håndhevet, beslutningsretten er uavklart, beslutninger tar 5× for lang tid, og scope vokser uten uttak. Teknologi, data og leverandør er i stor grad *følger* av dette. Uten å endre styringen vil et teknisk reset gi samme resultat om seks måneder.

**Hva må være sant?**
- Hovedtyngden av forsinkelsen kan føres tilbake til kritiske ventetider på Nordflow-beslutninger og uløste portkriterier.
- Beslutningstiden er systematisk lang (ikke noen få enkeltsaker) og skyldes uklar rett, ikke bare tung sak.
- Data- og testgapene skyldes manglende eier/regler, ikke manglende teknisk evne.
- Når beslutningsrett er avklart, kommer fremdrift (testes på de seks åpne sakene og de fire prosessene).

**Kilder å undersøke.** OF-001 (mandatets hull), OF-011 (35,5 dager median), OF-002 (roadmap godkjent med «ikke startet»), BOARD-002 (porter), EM-025–039, EM-112–118, EM-040–046, EM-035, EM-047–051, OF-014, TECH-004 (dataeier), VEN-002 (beslutningsforsinkelser).

**Hva kan falsifisere den?** Hvis beslutningene i loggen ikke ligger på kritisk sti (de gjør det: kontraktsmodell blokkerer tre integrasjoner og testdata [EM-027]). Eller hvis saker med klar beslutningsrett også tok lang tid (da er det kapasitet/kompleksitet, ikke rett). Eller hvis de 12 sakene forklarer lite av de 20/17/14 ukene. Nåværende evidens går den andre veien: ti av tolv saker >30 dager, og to ventet eksplisitt på «avklaring av beslutningsrett» [EM-117].

**Hva ville fått oss til å endre mening?** En sensitivitetsanalyse av kritisk sti som viser at selv med 7-dagers beslutninger ville sluttdato bare flyttet seg få uker (da er kapasitet eller teknologi dominerende). Eller at de fire siste ukenes gjenåpning av saker skyldes kvalitetsmangler i beslutningsunderlag og ikke manglende rett.

**Handling hvis sann.** Konsernreset (ikke IT-reset): navngitt beslutningstaker per type, beslutningsforum med 72 timers frist, scope-frys med unntaksprosess, håndhevede portkriterier, én samlet eier av kunde-/inntektsrisiko.

---

## H4 – Kapasitetshypotesen: folkene finnes ikke to steder samtidig

**Påstand.** Programmet og linjen trekker på de samme folkene. Dobbeltallokering, 49 FTE gap, 12 avganger og gjentatte ressurstrekk er den primære begrensningen. Beslutninger og data ville gått raskere med skjermede, finansierte roller. Dette forklarer også kundedrift-nedgangen.

**Hva må være sant?**
- De 49 manglende FTE-ene ligger på kritisk sti (23 kritiske roller ifølge HR [EM-132/133]).
- Forsinkelsene faller sammen i tid med ressurstrekk og avganger.
- Fylles gapet, forkortes kritisk sti uten at beslutningsrett endres.
- SLA-fallet er størst der folk er avgitt (delvis støttet [OPS-002]).

**Kilder å undersøke.** HR-002, EM-127–133 (kapasitet), EM-134–145 (SLA og ressurstrekk), EM-141–145 (når trekk skjedde), OF-010 R-047, OF-014 (Eiriks posisjon), OPS-001/002, HR-003.

**Hva kan falsifisere den?** Hvis de manglende rollene er ikke-kritiske, eller hvis tidligere perioder med full bemanning (januar 2025–jan. 2026) også ga forsinkelser (roadmap viste «ikke startet» på prosesseiere og 22 % profilering allerede ved start, så forsinkelsene *pre-dater* kapasitetsproblemene [OF-002]). Hvis backfillede personer ikke kan gjøre jobben fordi de mangler lokalkunnskap [EM-132]: da hjelper penger ikke.

**Hva ville fått oss til å endre mening?** Tidsserie som viser at 49-gapet oppsto *etter* de store forsinkelsene (årsak ← virkning snudd), eller at «tolv kritiske roller» ikke kan fylles internt/eksternt innen åtte uker.

**Handling hvis sann.** Beskytt de 23 kritiske rollene i fire uker, finansier backfill i drift (maks 1,8 mill. er godkjent, mer trengs), fjern dobbeltallokering, bind linjen til navngitte leveranser.

---

## H5 – Løsningshypotesen: kjernen/standardiseringen er ikke levedyktig slik den er designet

**Påstand.** Kompleksiteten i kontraktsvarianter (spesielt Danmark), datakvaliteten og dagens målarkitektur gjør full standardisering urealistisk innen rimelig tid og kostnad. Fortsetter vi, kaster vi gode penger etter dårlige. Alternativet er en radikalt redusert løsning, etappevis tilnærming eller stopp.

**Hva må være sant?**
- Plattformkjernen (Nexus, CRM/kontrakt, ERP-fakturering, identitet, portal) har strukturelle feil som ikke kan rettes ved governance.
- Lokale kontraktskrav (indeks, servicekreditt, fakturamottaker) lar seg ikke modellere i én felles struktur innen akseptabel tid.
- Piloten viste systematisk svikt og ikke teknisk lærekost.
- Total kostnad for å fullføre overstiger verdien (gevinst 128).

**Kilder å undersøke.** TECH-001/002/004/005, OF-012, EM-184–190 (CIO-review), OPS-003 (pilotutfall), FIN-005/006 (verdi), EM-119–126 (danske krav), EM-195 (full stopp-konsekvens), NPV-grunnlag i BOARD-001.

**Hva kan falsifisere den?** CIO vurderer kjernen som «levedyktig, ikke totalhavari», og plattformleder og test støtter det [TECH-002, EM-185, EM-190]. 46 av 64 integrasjoner er produksjonsklare, og piloten hadde «ingen systematisk totalhavari» [TECH-005, OPS-003]. Bare fire danske kontraktspunkter er dokumentert som reelle krav [EM-124]. Full stopp utløser avvikling, kontraktskost og minst to års dobbeltlandskap [EM-195]. Sunk cost taler *ikke* for å fortsette, men de rene driftskostnadene taler mot stopp.

**Hva ville fått oss til å endre mening?** (a) Uavhengig teknisk revisjon som finner arkitekturfeil i Nexus/ERP-kjernen; (b) en NPV-beregning på 472/128 som er klart negativ også for en redusert kjerne; (c) at de fire danske kontraktspunktene ikke lar seg modellere uten egen løsning; (d) en pilot som feiler systematisk også etter at data og regler er utbedret. CIO-reviewen er et *utkast* fra en part med en anbefaling, så den bør verifiseres uavhengig.

**Handling hvis sann.** Redesign eller stans. *Test først:* en 2–3 ukers uavhengig teknisk verifikasjon før noen irreversibel beslutning.

---

## H6 – Konsekvenshypotesen: kunde- og inntektsskaden dominerer og må styre rekkefølgen

**Påstand.** Den reelle kostnaden av OneFlow-situasjonen ligger i kunder og drift (churn, SLA, fornyelser, kreditter, linjekost) og ikke i programkostnaden. Kundebeskyttelse må derfor prioriteres foran programmets tidsplan, og neste bølge må stoppes til fakturakontroll er løst og noen eier risikoen.

**Hva må være sant?**
- Forverringen i SLA/churn skyldes i vesentlig grad OneFlow (ressursuttak, pilot, datafeil) og ikke sesong, fravær og marked.
- Minst noen av de tre fornyelsene med OneFlow-signaler går tapt hvis ingenting gjøres (105 mill. årsverdi).
- Eksponeringen vokser ved neste bølge (manuell kontroll skalerer ikke).
- Resultatrisikoen (3,6 bekreftet + inntil 7,2) er reell, ikke bare timing.

**Kilder å undersøke.** OPS-001–005, EM-134–140, EM-146–151, EM-152–165, EM-091–097, EM-230–236 (støy-avgrensning), OF-010 R-051/R-052, kundeøkonomi (ikke i korpuset).

**Hva kan falsifisere den?** Mari Heggen og Beate Høyer advarer mot å kalle hele 146 mill. en OneFlow-effekt; to av fem fornyelser er pris/marked [EM-149, OPS-004]. Driften sier selv at fravær (7,1 %), sesong og marked bidrar [OPS-002]. 16,8 mill. er i hovedsak timing, ikke tap [OPS-005]. Selv ved verste tolkning er den bekreftede resultateffekten liten (3,6 mill.) sammenlignet med programkost (+77 mill.). Vi har ingen kundelønnsomhetsdata.

**Hva ville fått oss til å endre mening?** At årsaksanalyse (årsakskoder, kundesamtaler) viser at flertallet av SLA-fallet og de tre fornyelsene har andre rotårsaker, eller at fornyelsene signeres uansett. Motsatt: at Metrohandel (15. okt.) eller EnergiVest (31. okt.) varsler oppsigelse med henvisning til fakturaproblemer, eller at pilotens 7,8 % faktisk er representativt.

**Handling hvis sann.** Stans Bølge 2 og utvidelse av Bølge 1 til kontrollen er løst. Navngi *én* eier av kunde-/inntektsrisiko. Lederplan per berørt kunde. Finansiert backfill i kundedrift. Skille OneFlow-effekt fra marked i all rapportering.

---

## Hvordan vi tester dem raskest (24-timers prioritering)

| Test | Skiller mellom | Kilde / hvem |
|---|---|---|
| Kritisk-sti-analyse: hva flytter sluttdato hvis (a) beslutninger tas på 7 dager, (b) leverandør leverer til tiden, (c) kapasitet er full? | H2 / H3 / H4 | Julie Nystad (PMO), Lars Pettersen |
| Avklar om 395 inneholder kreditt, og hva 41+22+19+29 består av | H1 og alle kostnadspåstander | Silje Tran (FIN-005, brotabell) |
| Verifiser verktøyforsinkelsen mot kontrakt og leveransedatoer (6. mai vs 13. juni) | H2 | Ole Martin Kvale, VEN-001 |
| Uavhengig teknisk verifikasjon av kjernen | H5 vs. H3 | Utenfor korpus; krever ekstern gjennomgang |
| Årsakskoding av SLA-fall og de tre fornyelsene | H6 | Ingrid Mørk, Mari Heggen |
| NPV på 472 og 128 (og på en redusert kjerne) | H5, alle handlingsalternativer | Silje Tran / Thomas Vik |
| Rekonsiler kundenavn OPS-004 mot TH-022 | H6 | Beate Høyer |

**Dersom bare én ting kan gjøres før styremøtet:** avklare kostnadsbroen (395 → 472) og at kundeeksponeringen ikke summeres uten overlappskontroll. Det er der avstanden mellom det styret tror og det som er kontrollert, er størst og lettest å dokumentere.

# Uavhengig review – CEO-brief, styrepresentasjon og AI-arbeidslogg

*Kortversjon: [`07-review-tldr.md`](07-review-tldr.md).*

*Gjennomført 2026-10-22 etter [`REVIEW_OPPDRAG.md`](REVIEW_OPPDRAG.md), av en separat AI-agent uten kontekst fra utformingen. Reviewet: `05-ceo-brief.pdf`, `06-styrepresentasjon.pdf` (med HTML-kilde) og `05-ai-arbeidslogg.pdf`/`.md`, etterprøvd mot `oppgave/CaseCorpus/`. Revieweren gir kritikk, ikke fasit. Gruppen må selv vurdere hvert punkt.*

> **Stikkprøvekontroll (Person B, mot originalkilder):** Disse funnene er bekreftet ordrett:
> - BOARD-005 §1: «CFO opplyste at prognosen inkluderer forventet leverandørkreditt».
> - EM-181: covenant holder «også ved 470».
> - EM-067: Convergent «reject a net claim of NOK 34m».
> - EM-068: «34 som krav, ikke som sikker kredit»; «skriftlig tilbud før styremøtet».
> - EM-151: Karin «Gjør det. Beate eier samlet oversikt, Eirik sikrer operative tiltak».
> - EM-005: «et redelig spenn».
> - FIN-004: intervallet 455–494 rundt 459, og dato-spennet 30.4–30.9.2027.
> - FIN-005: har ikke noe intervall.
> - CEO-briefens ordlyd på punkt 1, 2, 4, 5, 6, 7, 11 og 12.
>
> **Én feil i reviewen:** Under AI-arbeidsloggen står det at commit-hashene 618333f og e65a6bf ikke kan sjekkes. Det stemmer ikke. Mappen er et git-repo, og begge commitene finnes i `git log`.

## 1. Innledning

Revieweren har gått gjennom tre filer:

- `leveranser/05-ceo-brief.pdf` (2 sider)
- `leveranser/06-styrepresentasjon.pdf` (6 slides, med talenotater i `styrepresentasjon-kilde/slides/*.html`)
- `leveranser/05-ai-arbeidslogg.pdf`, som stemmer innholdsmessig med `.md`-filen

Påstandene er sporet bakover til `03-hovedanbefaling.md`, `04-90-dagersplan.md`, `01-situasjonsbilde.md` og `hypoteser-funn/*.md`, og deretter etterprøvd mot originalkildene i `oppgave/CaseCorpus/`. Revieweren leste FIN-003/004/005/006/007, OF-002/003/011, TECH-002/003/005, OPS-001/002/003/004, HR-001/002, VEN-001/002, BOARD-002/003/004/005 og OF-014 (PDF), og om lag 60 e-poster. Det gjelder blant annet alle e-poster sendt 12.–17.9. Summer og datoer er regnet om, og ukedager er sjekket.

**Dette stemmer mot kildene:**
- 318 + 91 = 409 (FIN-007)
- 472 og 506 (FIN-005, EM-173)
- 472 − 280 = 192
- 210 − 40 − 42 = 128 (FIN-006)
- 438 (FIN-003) og 459 (FIN-004)
- Medianen 35,5 ((35 + 36) / 2, OF-011)
- 46 og 18 av 64 integrasjoner (TECH-005)
- Bemanning 168 / 119 / 49, 37 over 120 % og 12 avganger (HR-002, EM-132)
- 23 kritiske roller = 12 + 7 + 4 (EM-132)
- Fornyelser 146 = 71 + 34 + 41 (OPS-004)
- SLA 95,8 → 91,4 og churn 5,0 → 6,7 (OPS-001)
- Backfill 1,8 mill. (EM-140)
- 11–26 uker bak recovery (TECH-003: 11,3 / 15,3 / 15,1 / 17,4 / 26,3 uker)
- Verktøyforsinkelse 74 dager = 10,6 uker
- Ukedager og dagtall: 18.9 er fredag (dag 0), 16.10 er dag 28, 16.11 dag 59 og 17.12 dag 90
- ICE-snittene på slide 4

Avvikene står nedenfor.

## 2. Hovedtabell

| Påstand (artefakt) | Støttende evidens | Motstridende evidens | Vurdering | Sikkerhet |
|---|---|---|---|---|
| **1.** «Kontrollert sluttkost er 472 mill.» / «forventet sluttkost» (Brief §1; Slide 1) | FIN-005 (sum netto 472); EM-172/173 (Finance-kontroll 16.9) | 472 forutsetter at hele kreditten på 34 kommer (FIN-005, kolonnen Kreditt). Ole Martin Kvale skriver at bare **12 er «nær sikkert»** (EM-065). CFO vil ha 34 «som krav, ikke som sikker kredit i beslutningsgrunnlaget» (EM-068, 15.9). Convergent **avviser** netto 34 (EM-067, 13.9). Teamets egen D5 sier «regn med 12». Med 12: 506 − 12 = **494**, altså toppen av intervallet. | Overskriften bygger på et kredittbeløp som teamet selv sier man ikke skal regne med. Vis 472 (full kreditt) / 494 (sikker kreditt) / 506 (ingen kreditt), eller bruk 494 som forsiktig base. `01-situasjonsbilde.md` hadde 494, men tallet er falt ut av brief og slides. | Høy |
| **2.** «Ligger kreditten (34) allerede i 395? Gapet er 77 eller 111» – åpent (Brief §6; notater slide 1; 03 §7) | EM-173: brosummen 395 + 41 + 22 + 19 + 29 = 506 er ikke internt konsistent | Formelle kilder sier tydelig at 395 inkluderer forventet kreditt: **BOARD-003** (avsnitt Økonomi og gevinster), **BOARD-004** (avsnitt Økonomi), **BOARD-005 §1** («CFO opplyste at prognosen inkluderer forventet leverandørkreditt») og EM-173. | Spørsmålet er stort sett besvart. Sammenlignet likt mot likt (begge med kreditt) er økningen **77**. 111 er nedsiden uten kreditt. Det som gjenstår er hvor *stor* kreditt 395 forutsatte, og den interne brofeilen i EM-173. Flytt punktet fra «vi vet ikke» til en presis setning. | Middels–høy |
| **3.** Intervall «455–494» rundt 472 (Brief §1; 03 D1) | EM-172 og EM-173 oppgir 455–494 | FIN-005 (CSV) har ikke noe intervall. **FIN-004** (august, base 459) har nøyaktig samme 455–494. | Det kan se ut som intervallet er arvet fra 459-prognosen og ikke regnet på nytt rundt 472. Bør bekreftes av Silje Tran. | Usikker |
| **4.** «Fullføring er mest sannsynlig 30. juni 2027» / «ny sluttdato» (Brief §1; Slide 1) | TECH-002 (CIO: «mest sannsynlig»), FIN-004 (base), TECH-003 (Bølge 3 Danmark) | EM-088 (Camilla Bruun): «full migrering **tidligst** juni 2027». FIN-004 har spennet 30.4–**30.9.2027**. EM-189 og TECH-002 viser at CIO-datoen forutsetter at **avansert planlegging og deler av portalen fases senere** (redusert omfang). EM-060: Convergents datoer er «indicative only» siden scope-frysen innen 15.9 ikke kom. Karin ber om «et redelig spenn» (EM-005). OF-002: stabilisering kommer etter den siste bølgen, så dette er ikke programmets sluttdato. | Presenteres sikrere enn kildene tillater. Gi et datospenn, og si at 30.6 forutsetter redusert omfang. Det må da avklares om anbefalingen *inkluderer* CIO-ens reduserte kjerne. «Ikke nå: redesign» står i spenning med dette. | Høy |
| **5.** «31.12 passeres uten at Bølge 1 er gjennomført» (Brief §4; Slide 1) | EM-087 og EM-088: piloten er ikke normalisert, ny begrenset bølge først i november | TECH-003 har Bølge 1 cutover i **nåværende prognose 18.12.2026**, altså før 31.12. 04 T16 planlegger selv go/no-go for 18.12. | Påstanden er enten feil eller upresis (gjelder den alle 286 kunder?). Den kan også være en følge av teamets egen pause i D3. Omformuler, og oppgi kilden. | Middels |
| **6.** «Prosess, integrasjon og data er 14–20 uker bak original plan [TECH-003, OF-008]» (Brief §2, Tid) | EM-088 (~20 uker), EM-104 (17 uker), EM-118, OF-008 | **TECH-003** viser 25,9–28,7 uker for bølgene og 82,7 uker for dataprofilering mot original. Arbeidsloggen pkt. 4 nr. 1 sier at «14–20 bak original» er *forkastet*. | Feil kildehenvisning, og i strid med det loggen sier ble gjort. Bruk EM-/OF-008-kildene for sporene, eller oppgi bølgeavviket fra TECH-003. | Høy |
| **7.** «Alle 12 kritiske beslutninger tok over fire ganger målet (median 35,5 mot 7)» (Brief §3; Slide 3) | OF-011: sortert 29…56, median 35,5, minste verdi 29 > 28 | 6 av 12 er **åpne**, så «tok» er feil ordbruk og medianen er høyresensurert. Backfill ble faktisk besluttet 6.9 (EM-140), så loggen er utdatert. Alle sakene er reist april–august 2026, *etter* recovery i mars 2026 (OF-003). EM-025 viser 17 åpne beslutninger i mai, så loggen er et utvalg. | Tallet er riktig, men beviset dekker bare en periode der forsinkelsen allerede hadde skjedd. Det forklarer ikke 2025. Formuler mer forsiktig. | Fakta: høy. Slutning: middels |
| **8.** «[Beslutningene] blokkerer 10 av 18 uferdige integrasjoner» (Brief §3; Slide 3; 04 T2) | TECH-005: 6 «beslutning/krav» + 4 «manglende testdata» = 10. VEN-002: 10. | EM-104 (Lars Pettersen, 9.9): 6 Convergent, **5** beslutning/prosess, 4 testdata/miljø, 3 scope. Testdata er et data- og eierskapsproblem, ikke de 12 beslutningene i OF-011. | Overdrevet årsakskobling. Korrekt er «10 av 18 er kundeskapt, 5–6 venter på beslutning». | Middels–høy |
| **9.** «Rotårsaken er vår egen styring» – H3 støttet (Slide 3, tittel; Brief §3) | OF-001 (ingen konfliktløsning), OF-002 (porter ikke oppfylt ved start), BOARD-002 (portkrav), EM-043/046 (scope 28 → 47 uten uttak), TECH-002 | H3-funn §1 rad 3: saker *med* klar eier tok like lang tid. EM-117: 2 av 4 saker ble sendt tilbake for svakt underlag. Sakene gjelder krevende fag- og dataspørsmål (dansk prisindeks, servicekreditt, dataeier). OF-003 nevner verktøy, prosess og kapasitet som årsaker. Kritisk sti er ikke analysert. | Dommen «støttet» er forsvarlig. Slidetittelen og «samlet» er for kategoriske. Forbeholdet står bare i bunnteksten. | Middels |
| **10.** «Leverandør: reell, men mindre – bare 5–6 av 18» / H2 «Falsifisert» (Brief §3; Slide 3) | VEN-002, TECH-005, EM-055 og EM-059 (begge parter peker på Nordflow-avhengigheter) | Målet er antall integrasjoner, ikke effekt på kritisk sti. Verktøyet lå på kritisk sti for Bølge 1 og var 5–10,6 uker sent (EM-052–056). Det feilet ved levering (EM-056). BOARD-003 (juni) kaller verktøyet «hovedflaskehals». | «Ikke vist som hovedårsak» er dekkende. «Falsifisert» er for sterkt så lenge kritisk sti ikke er analysert. | Middels |
| **11.** «Convergents kredittilbud (24–34) forutsetter scope-frys» / «faller bort uten frys» (Brief §4; Slide 1, 2 og 6) | VEN-002, Commercial proposal: «prepared to **discuss** credits 24–34 if scope is frozen …» | 24–34 er også Nordflows *eget* kravintervall (EM-062). **EM-067 (13.9, nyere):** Convergent avviser netto 34 med henvisning til 31 kundeskapte hendelser. Fristen for frys, 15.9, er passert (EM-060). CFO ba om skriftlig tilbud før styremøtet (EM-068). Noe slikt tilbud finnes ikke i korpuset. | Det finnes ikke noe «tilbud». Frys er nødvendig, men ikke tilstrekkelig. Slide 6-målet «24–34 skriftlig dag 90» virker optimistisk. | Høy |
| **12.** D1: «Ny ramme ved port … frem til da frigis kun forpliktet beløp» (Brief D1; Slide 2 D1) | FIN-005 (63 uforpliktet); BOARD-005 vedtak 2 (rammen er ikke endret) | Det forpliktede beløpet (409) er allerede **129 over** styrets ramme på 280. BOARD-002 ga CEO fullmakt bare «innenfor rammen». «Løpende drift» er ikke tallfestet (avledet ca. 15 mill./mnd). | Styret blir ikke bedt om å vedta et konkret beløp. Det trenger et midlertidig fullmaktsbeløp frem til 16.10, og må ta stilling til at rammen allerede er overskredet. | Høy |
| **13.** «Rapporter 472 til styre og bank» / «banken møtes 25.9» (Brief D1 og §4; Slide 1) | EM-181/183 (banken vil ha konsistente tall senest 18.9) | **EM-181 (Treasury):** covenant holder «også ved **470**», men headroom faller i Q1/Q2 hvis gevinstuttaket skyves. 472 ligger over 470, og 494/506 er ikke testet. Banken vil spørre etter en styregodkjent rebaseline. Dette mangler i brief, slides og 04. Det står bare i 01 og H6, der H6 feilaktig sier at det ikke er noen bindende begrensning. | Vesentlig utelatelse før bankmøtet. Legg til et tiltak om covenant-test på 472/494/506 (Thomas Vik/Treasury) før 25.9. | Høy (utelatelsen). Konsekvensen er usikker. |
| **14.** «7,8 % fakturakorreksjon (2,0 % i januar)» (Brief §2) | EM-094, OPS-003 | EM-094 sammenligner pilot mot *porteføljen* og advarer selv mot generalisering. Porteføljen var 4,9 % i august (OPS-001). Pilotkundene er ikke representative (EM-084). | Sammenligningen er skjev og ikke like mot like. Oppgi porteføljetallet for august, eller ta med forbeholdet. | Middels |
| **15.** «Servicen faller: SLA 91,4 %, churn 6,7 %, kø over 1 900» som OneFlow-effekt (Brief §2; Slide 1) | OPS-001; EM-136 (ressursuttak synlig) | OPS-002: «hele utviklingen kan ikke tilskrives programmet» (fravær 7,1 %, sesong, marked). Køtallet 1 900 er fra 1.7 (EM-143) og er 2,5 måneder gammelt. | Korrelasjon presentert uten forbehold. Legg til at programmet bare forklarer en del av fallet, og dater køtallet. | Middels |
| **16.** H6 «svekket»: målbar effekt ≤ 22 mill. mot +77 i programkost (Slide 3; 03 §3) | OPS-005, EM-159/163, OPS-002 (3,6 + 7,2 + 11,2 = 22) | Sammenligningen setter et engangsbeløp mot en kostnadsøkning og ser bort fra **71 mill. i årlig kontraktsverdi** med direkte OneFlow-signal (EnergiVest alene utgjør 42/år). Det er samme størrelsesorden som gevinsten på 128/år. | Regnestykket bærer ikke «svekket». Konklusjonen om å sekvensere bølgene og sikre kundene står seg likevel. | Middels |
| **17.** «Skjerming før backfill» og skjerm de 23 rollene (Slide 2; 04 §4; Brief D4: «1,8 mill. … for lite for 49 FTE») | EM-133 (Lene Falk), EM-145 | **EM-194 (COO):** «kundedrift må få finansiert backfill *før* vi låser folk». OF-014: drift «kan ikke avgi ytterligere kapasitet». EM-143: innleide kan ikke vurdere gamle avtaler. Beløpet på 1,8 mill. gjaldt backfill i *kundedrift* (EM-140), ikke programgapet på 49 FTE. | Rekkefølgen strider mot den operative kilden og truer SLA-målet og fornyelsene. Sammenligningen 1,8 mill. mot 49 FTE blander to ulike ting. | Høy |
| **18.** D3 «Én formell eier …», fornyelser med lederplan «0 av 5» (Brief D3; Slide 6; 04 T5) | OF-014 pkt. 5 (formell eier avklares 22.9) | **EM-151 (12.9):** Karin har allerede sagt «Gjør det». Beate eier oversikten og Eirik de operative tiltakene, med navngitt leder for de tre (EM-150). | Basislinjen «0 av 5» er ikke dokumentert, og delbeslutningen er tatt. Eierskapet er ulikt mellom artefaktene (se §3). | Middels |
| **19.** «Lukk de seks åpne kritiske sakene» (Slide 4 #1; 04 T3 og §5) | OF-011 (6 uten dato) | Backfill ble besluttet 6.9 (EM-140). En midlertidig scope-frys ble besluttet 10.9 (OF-014 vedtak 3). | Reelt er det 4–5 åpne saker. Oppdater fra OF-011 til dagens status. | Middels–høy |
| **20.** «Bottoms-up-tallene (438, 459) nådde ikke styret» (Brief §3; Slide 1) | BOARD-003: bottoms-up «ikke lagt ved» | BOARD-004 og BOARD-005 §1: ubesluttede forlengelsesposter lå i *risikovedlegget*, og CFO opplyste om dette muntlig. Vedlegget mangler i korpuset. | Godt belagt for juni. For august er påstanden for kategorisk, og teamet sier selv at vedlegget mangler. | Middels (usikker for august) |

## 3. Konsistens på tvers av artefaktene

| Tema | CEO-brief | Styrepresentasjon | 03 / 04 / logg | Avvik |
|---|---|---|---|---|
| Hva styret beslutter | Bare D1 = Styret. D2–D6 = CEO/CFO/CIO. | Slide 2: «styret i dag godkjenner … og beslutter seks ting» | 03 D2: «CEO (styret tar til orientering)» | Sliden gir et uriktig bilde av styrets rolle |
| Frister D4 / D5 / D6 | 22.9 / «Før frister» / «Nå» | 2.10 / 9.10 / 16.10 | 03: D6 «start umiddelbart». 04 T8: «bestilt dag 7» | Tre ulike frister |
| Port | «port etter 30 dager» | Port 1 = 16.10 (dag 28) | 03: «dag 30-porten». 04: dag 28. (Dag 30 = 18.10 er en søndag.) | Dag 28 eller dag 30 |
| Eier av kunderisiko | D3: CEO | Slide 4 #3: Eirik Solheim*. Slide 6: «måles av» Beate Høyer. | 04 T5: A = Karin Eide, Eirik som forslag | Tre ulike svar |
| Seks åpne saker | – | Slide 4 #1: Karin Eide | 04 T3: Håkon Berg | Ulik eier |
| Data / danske krav | – | Slide 4 #11: Camilla Bruun | 04 T12: Camilla. 04 T13: Beate Høyer. | Danske krav har fått ny eier |
| Integrasjoner / prosess | – | Slide 4 #12: Håkon Berg | 04 T14: Nora Steen / Lars Pettersen. Håkon har bare T16. | Ulik eier |
| Lederplan 5 av 5 | – | Slide 6: dag 28 | 04 T5: dag 7 (25.9) | Tre ukers forskjell |
| Referansedato | «ikke 28. februar» | Slide 1: «Vedtatt 31.12.2026» | 03: begge | Ulik sammenligningsbasis |
| Fornyelser | 15.10–31.12 | Slide 1: «før 31.12». Slide 5: bare 4 prikker, 31.12 mangler. | 04: 5 datoer inkl. 31.12 | Svea Terminal (31.12) faller ut |
| Kundenavn | Brukes ikke | Brukes ikke | 04 §3 navngir alle fem kundene, mens 04 §7 og 03 §7 sier at navn ikke skal brukes | Intern selvmotsigelse i 04 |
| «14–20 uker bak original» | Brukes, med henvisning til TECH-003 | – | Loggen pkt. 4 nr. 1: «Forkastet» | Loggen og briefen er uenige |
| Kreditt | 472 som hovedtall | «Krev 34, regn med 12», men 472 er overskriftstallet | 01: 494 med 12 | Selvmotsigende |
| Oppstart «denne uken» | – | Slide 4: de seks øverste. Slide 5: også #8 og #11 starter 18.9. | 04 P1 = T1–T6 (T7 pause hører til P2) | Ulik gruppering |
| «Åtte tall» | – | Slide 6-tittelen sier åtte, tabellen har 7 indikatorer | – | Liten feil |
| Loggens dekning | – | – | Loggen sier at presentasjonen «ikke er lagt i repoet» (den er det nå), og CEO-briefen er ikke dekket i det hele tatt | Loggen er utdatert |

## 4. Styrepresentasjonen som beslutningsgrunnlag

**Sterkt:** Tittelene er handlingsrettede, slide 2 har en beslutningstabell med eier og frist, «står og faller på» viser avhengighetene, og stoppkriteriene er tydelige.

**Svakt:**
- **Det er uklart hva styret konkret vedtar.** Det mangler en eksplisitt vedtakstekst («Styret vedtar … / slutter seg til …») med beløp. D1 har ingen midlertidig fullmakt (rad 12), og overskridelsen av rammen på 280 omtales ikke som noe styret må forholde seg til.
- **Det vises ikke noe usikkerhetsspenn.** Kostnaden presenteres som ett tall, 472, uten 494/506 som sensitivitet. Datoen presenteres uten spenn (rad 1 og 4). Karin ber eksplisitt om «et redelig spenn» (EM-005).
- **Alternativene A–D får ikke egen slide**, slik 03 §8 forutsetter. De får bare én linje («Ikke på bordet»). Styret ser dermed ikke hva det velger bort.
- **Bank og covenant mangler** (rad 13).
- **Slide 4 (ICE) og slide 5 (Gantt) er ledelsesdetaljer.** ICE-rangeringen kolliderer også med 04 sin avhengighetslogikk («sekvensert etter hva som må på plass før»).
- **Slide 3-tittelen er mer kategorisk enn analysen**, og forbeholdet står bare i bunnteksten.

## 5. AI-arbeidsloggen

- **Oppfyller kravet i form.** Pkt. 3–5 svarer på delegert / brukt / endret / forkastet, med 13 konkrete endringer. Loggen er ærlig om sine begrensninger: tomme kontrollkolonner, sekundærlesing av H2/H4/H6, og at samme AI både skrev og kontrollerte.
- **Svak på menneskelig kontroll.** Nesten alle endringene i pkt. 4 ser ut til å være AI-ens egne selvkorrigeringer. Det er ikke dokumentert noe en *person* forkastet, og vurderingen i fellesmøtet er «ikke dokumentert». «Beholdt hos mennesker» er en påstand uten belegg.
- **Hull i dekningen.** CEO-briefen er ikke omtalt. Avsnittet om presentasjonen er utdatert. Sammenslåingen fra 17 til 12 tiltak endret flere eiere uten at det står i loggen (se §3).
- **Etterprøvbarhet.** *(Revieweren skrev at commit-hashene ikke kunne sjekkes. Det er feil, se kontrollnoten øverst. Hashene finnes i git-loggen.)* Tidslinjen bruker 22.10.2026 mens casetiden er 17.9, og det bør forklares i én setning. Navnet staves både «Gurrich» og «Gürrich».
- **Ikke i tråd med leveransen.** Loggen sier at «14–20 uker bak original» er forkastet, men briefen bruker det (rad 6).

## 6. Avslutning

### 1) De tre viktigste rettelsene

1. **Kostnad, kreditt og bank.** Presenter 472 som «forutsetter full kreditt», med 494 (sikre 12) og 506 (ingen kreditt) ved siden av. Lukk spørsmålet om kreditt i 395 med BOARD-003, BOARD-004 og BOARD-005 (økningen likt mot likt er 77). Fjern ordet «tilbud» fra Convergent-omtalen (EM-067). Legg til en covenant-test før 25.9 (EM-181).
2. **Dato og omfang.** Oppgi et datospenn (FIN-004: 30.4–30.9.2027, EM-088: «tidligst») og at CIO-datoen forutsetter redusert kjerne (EM-189, TECH-002). Avklar om anbefalingen omfatter dette. Rett «31.12 uten Bølge 1» mot TECH-003 (18.12).
3. **Gjør vedtaket presist og harmoniser.** Skill styrevedtak (D1 med konkret midlertidig beløp og stillingtaken til at rammen på 280 er overskredet, tilslutning til CEO-mandatet) fra CEO-tiltak. Samkjør eiere og frister i brief, slides og 04. Snu eller begrunn rekkefølgen «skjerming før backfill» mot COO-kravet (EM-194, OF-014).

### 2) Bør kontrolleres før levering

- Kreditten: BOARD-003/004/005, EM-060, EM-065, EM-067, EM-068
- Bank: EM-181
- Datoen: FIN-004, EM-088, EM-189, TECH-002, TECH-003 (Bølge 1, 18.12)
- Intervallet 455–494: FIN-005 mot FIN-004 (spør Silje Tran)
- Integrasjonsårsaker: TECH-005 mot EM-104
- Åpne saker: OF-011 mot EM-140 og OF-014 vedtak 3
- Eierskap og lederplaner: EM-150, EM-151
- Drift og kapasitet: OPS-002 (årsaker til SLA-fallet), EM-094 (forbeholdet om piloten), EM-143 (køtallets dato), EM-194 (rekkefølge for backfill)
- Utvalget i beslutningsloggen: EM-025
- Påstanden om at 459 ikke nådde styret: BOARD-004/005

### 3) Sterkeste alternative hovedforklaring

Programmet ble *godkjent på et urealistisk grunnlag*. Svikten lå i estimering og godkjenning, kombinert med at Cobalts data og forretningsregler var mer kompliserte enn antatt. Langsomme beslutninger er da mer et symptom enn rotårsaken.

Belegg:
- Alle spor startet parallelt i januar 2025 (OF-001).
- Dataprofileringen var bare 22 % kartlagt ved godkjenning, og prosesseiere var «ikke startet» (OF-002).
- 40 mill. av gevinsten var dobbelttelt mot Cobalt og ble ikke avstemt ved vedtaket (BOARD-002, FIN-006). Business caset summerer dessuten til 602, ikke 620 (FIN-001; ikke kontrollert av Person B).
- Recovery-planen kom allerede i mars 2026, før perioden beslutningsloggen dekker (OF-003 mot OF-011).
- Saker med klar eier tok like lang tid, og saker ble sendt tilbake for svakt underlag (H3-funn, EM-117).

Hvis denne forklaringen holder, flytter ikke en 72-timersregel den kritiske stien. Hovedgrepet blir da omfangsreduksjon (CIO-ens reduserte kjerne) og en realistisk ny plan. Forklaringen overlapper delvis med H3 (godkjenning i strid med portkravene er også styring), men den gir en annen vekting av tiltakene. *Usikker: korpuset kan ikke avgjøre dette uten kritisk-sti-analyse.*

### 4) Er anbefalingene beslutningsklare?

Retningen er godt begrunnet og samsvarer med CIO, CFO og COO (EM-191–196, EM-195): ikke fortsett uendret, ikke stopp, gjennomfør et kontrollert reset med porter og stoppkriterier. Som styregrunnlag er det **ikke helt klart**:
- D1 mangler et konkret beløp og en konkret fullmakt.
- Overskriftstallet hviler på en kreditt motparten avviser.
- Bank og covenant er ikke behandlet.
- Datoen gis uten spenn og uten at forutsetningen om redusert omfang står.
- Eiere og frister spriker mellom artefaktene.
- Rekkefølgen for kapasitetstiltakene strider mot den operative kilden.

Alt dette kan rettes på noen timer, uten at anbefalingen endres.

---

**Gruppens ansvar:** Hvert vesentlig punkt vurderes og kontrolleres mot originalkilden. Endringene noteres i AI-arbeidsloggen (jf. `REVIEW_OPPDRAG.md`).

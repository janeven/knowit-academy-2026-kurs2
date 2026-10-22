# AI-arbeidslogg – OneFlow-caset

*Leveranse 5 av 5. Samler AI-bruken i hele arbeidet: hva vi delegerte til AI, hva vi brukte uendret, og hva vi endret eller forkastet. Kilder til loggen: seksjon 9 («AI-bruk») i hver funnfil under [`hypoteser-funn/`](hypoteser-funn/00-oversikt.md), commit-historikken i repoet (22.10.2026, 10:08–11:52) og arbeidsøkten som skrev [`03-hovedanbefaling.md`](03-hovedanbefaling.md), [`04-90-dagersplan.md`](04-90-dagersplan.md) og styrepresentasjonen.*

**Begrensning:** Loggen dekker det som er dokumentert i repoet og i denne økten. De andre teammedlemmenes egne Claude-økter er bare synlige gjennom det de selv skrev i funnfilene. Der noe ikke er dokumentert, står det «ikke dokumentert», og vi har ikke fylt hull med antakelser. Hvem som er Person A, B og C er utledet fra commit-forfatter (Jonas Gurrich: H2/H5, Even Ambjørnrud: H3/H4, ingmyh: H1/H6), og teamet bør bekrefte det.

---

## 1. Oppsummering

| | |
|---|---|
| **Arbeidsmåte** | AI som skeptisk analytiker, ikke som advokat for en hypotese. Arbeidsinstruksen ([`PROMPT-hypotesetest.md`](PROMPT-hypotesetest.md)) krevde at hver hypotese først ble forsøkt falsifisert, at påstander ble merket *fakta / sannsynlig / antakelse*, og at kilde-ID og regnestykke fulgte alt. |
| **Delegert til AI** | Lesing av hele corpuset (240 e-poster, 75 dokumenter/datasett), første situasjonsbilde og seks hypoteser, test av hver hypotese mot kildene, alle beregninger, utkast til dommer, felles tall, hovedanbefaling, 90-dagersplan og styrepresentasjon. |
| **Beholdt hos mennesker** | Fordeling av hypotesene på tre personer, vurdering av dommer før de gikk i fellesoversikten, valg av rotårsak/forsterker/symptom i fellesmøtet, og alle beslutninger om hva som skal sendes til CEO og styret. |
| **Viktigste mønster** | AI leverte raskt og bredt, men første utkast hadde flere tall og formuleringer som ikke tålte kontroll mot originalkildene. Minst ti av dem ble endret eller forkastet (pkt. 4). |
| **Ikke gjort ennå** | Uavhengig AI-review ([`REVIEW_OPPDRAG.md`](REVIEW_OPPDRAG.md) finnes, men ingen review er lagt inn i repoet). Se pkt. 7. |

---

## 2. Tidslinje (22.10.2026)

| Tid | Hva | Hvem (commit) | AI-rolle |
|---|---|---|---|
| 10:08–10:23 | Oppgave og firmapresentasjon lagt inn som Markdown | Even Ambjørnrud | Ikke dokumentert |
| 10:42 | [`01-situasjonsbilde.md`](01-situasjonsbilde.md) og [`02-hypoteser.md`](02-hypoteser.md) | Jonas Gurrich | Claude leste hele corpuset og skrev utkastene (beskrevet som «tidligere økt» i H2- og H5-loggene) |
| 10:54–10:56 | Arbeidsinstruks og funnmaler for parallell hypotesetest | Jonas Gurrich | Forfatter ikke dokumentert. Instruksen legger rammene for hvordan AI skal brukes (pkt. 3) |
| 11:08 | H2 og H5 | Jonas Gurrich (Person A) | Claude testet, regnet og skrev utkast |
| 11:09 | H3 og H4 | Even Ambjørnrud (Person B) | Claude testet, regnet og skrev utkast |
| 11:13 | H1 og H6 | ingmyh (Person C) | Claude testet, regnet og skrev utkast |
| 11:27 | Felles konklusjon, felles tall og rettinger i situasjonsbildet | Jonas Gurrich | AI sammenstilte. Rettingene er i pkt. 4 |
| 11:49 | Oppdrag til uavhengig AI-reviewer | ingmyh | Mandat for review, ikke selve reviewen |
| 11:52 | Hovedanbefaling og 90-dagersplan | Jonas Gürrich | AI syntetiserte fra funnfilene (pkt. 5) |
| Etter 11:52 | Styrepresentasjon på seks slides | – | AI bygde den. Den ligger som artefakt og er ikke lagt i repoet (pkt. 5) |

---

## 3. Hva vi delegerte, og hvordan vi kontrollerte det

| Fase | Delegert til AI | Brukt uendret | Endret / forkastet | Kontrollert mot original |
|---|---|---|---|---|
| **Situasjonsbilde og hypoteser** | Lese hele corpuset, bygge nåsituasjon, rotårsaker, konsekvens og seks konkurrerende hypoteser | Korpuskart, kildehierarki (A–D), hypotesenes struktur og «hva ville fått oss til å endre mening» | Fem påstander ble rettet i etterkant (pkt. 4, nr. 1–5) | Alle tall ble regnet på nytt fra CSV/MD/PDF i hypotesetestene |
| **H1 gul og håndterbar** | Lese kildene, regne i Python, skrive utkast | Datoer, tellinger og tabeller fra originalkildene. Formuleringen «hva H1 har rett i» | «14–20 uker bak original» som felles tall. Flagget at situasjonsbildet motsa OPS-003 om Bølge 1 | Alle beløp og datoer i §1 hentet fra originalfilene. `.xlsx` ble ikke åpnet (CSV brukt). Person C bør stikkprøve 409 mot 395, uker-tabellen og OF-011-medianen |
| **H2 leverandør** | Lese corpuset, beregne andeler og uker (awk), utkast til dom | Alle beregninger i teksten | Dommen skjerpet: «primærårsak» falsifisert, «medvirkende» støttet, med forbehold om migreringssporet | Alle tall re-verifisert mot originalfilene. Regnet om for hånd (5/18, 6/18, 8/18, 9/18, 74 dager = 10,6 uker, 34/226, 34/111) |
| **H3 styring** | Lese OF-/BOARD-/TECH-/VEN-kilder og tråder, regne median, snitt og 148 dager, klassifisere de 12 sakene, finne kildekonflikter | Sitater, tall, median 35,5, 10/18 og 148 dager | 02-hypotesers formulering «to ventet på beslutningsrett» som hele bildet forkastet (EM-117 sier 2 av 4). Klassifisering av klar/uklar beslutningsrett brukt kun som **antakelse** | Loggen kontrollert mot e-post (OF-011 mot EM-027/140) av AI. **Person B skulle fylle ut egen kontroll, og det er ikke gjort i filen** |
| **H4 kapasitet** | Lese HR-/OPS-/OF-kilder, regne andeler, vurdere årsaksrekkefølge 2025 mot 2026 | Tall og sitater. Konklusjonen «ikke avgjørbar» for 2025 | 02-hypotesers tolkning av EM-130-kategoriene forkastet til fordel for primærdata (HR-002) | Regnestykker (46/33/26 %, 23/49, 42→49, 148 dager) regnet av AI. **Person B skulle fylle ut egen kontroll, og det er ikke gjort i filen** |
| **H5 kjernen levedyktig** | Søke etter arkitekturvurderinger, bygge enkel forward-looking verdimodell (9 %, 3 og 5 år) | Kildehenvisninger og tall som utgangspunkt. Beregningen som illustrasjon | Modellen merket som **antakelse, ikke NPV**, med forbehold om sunk cost, linjekost og ramp-up. Dom satt til SVEKKET, ikke FALSIFISERT, fordi uavhengig verifikasjon mangler | Tall re-verifisert mot originalfilene. Regnestykket bør kjøres på nytt i regneark av et teammedlem |
| **H6 kunde og inntekt** | Lese OPS-/FIN-/BOARD-kilder og tråder, regne alle tall i Python | Tellinger og beløp. Nedbrytningen 71/34/41 | 27,6 mill. forkastet som tall. «105 mill. OneFlow-effekt» forkastet uten forbehold. «Ingen eier» rettet til «tre midlertidige eiere, ingen formell» | Alle regnestykker regnet på nytt. Person C bør stikkprøve 71/34/41, SLA-gapet og at EM-141/143 beskriver tilbakeføring til linjen |
| **Oversikt og felles tall** | Sammenstille dommer, felles konklusjon, avklarte tall og prioritert liste over det som må undersøkes | Rolleinndeling (rotårsak/forsterker/symptom) og tabellen over avklarte kildekonflikter | Fem rader merket **åpen** fordi corpuset ikke kan avgjøre dem (kreditt i 395, 382 mot 395, verktøyforsinkelse, kundenavn, Bølge 1 i drift) | Tall kontrollregnet fra originalfilene, ifølge oversikten. Teamets vurdering av dommene i fellesmøtet er ikke dokumentert |

---

## 4. Hva vi forkastet eller endret

*Dette er de konkrete tilfellene der AI-utkastet ikke ble brukt som det var. Kilde: AI-seksjonene og rettingene i commit `618333f`.*

| # | AI-utkast | Hva vi gjorde | Hvorfor | Hvor |
|---|---|---|---|---|
| 1 | «14–20 uker bak original» som ett felles tall | **Forkastet.** Brukes nå som «14–20 uker på sporene» og «26–31 uker for bølgene». Mot recovery: «11–26 uker» | TECH-003 gir 26–31 uker for bølgene og 82,7 for dataprofilering mot original. Tallet 14–20 bruker trolig en annen milepæl | H1 §7, 01-situasjonsbilde |
| 2 | «Ingenting av Bølge 1 er i drift» | **Endret** til «pilot på 42 er migrert, men Bølge 1 er ikke avsluttet» | Motstrid mellom TECH-003 (cutover 18.12) og OPS-003/EM-087 (42 migrert, 34 stabilisert) | H1 §7, 01-situasjonsbilde |
| 3 | «Fornyelser for opptil 105 mill. med OneFlow-effekt» | **Endret.** 146 mill. delt i 71 direkte, 34 indirekte og 41 pris/marked | To av fem fornyelser har pris/marked som hovedårsak. «105» slår sammen direkte og indirekte | H6, 00-oversikt |
| 4 | 27,6 mill. som inntektseksponering | **Forkastet.** Bruker 3,6 bekreftet, ≤ 7,2 mulig, 16,8 arbeidskapital og 11,2 linjekost | Summen blander arbeidskapital, bekreftet resultat og ikke-bokført risiko | H6, 00-oversikt |
| 5 | «Ingen eier» av kunde- og inntektsrisiko | **Endret** til «ingen formell eier, tre midlertidige» | OF-014 og EM-151 viser Eirik Solheim, finans og Beate Høyer | H6 |
| 6 | «To prosesser ventet på beslutningsrett» som hele bildet | **Forkastet** | EM-117 sier 2 av 4. De to andre ble sendt tilbake for manglende operativ konsekvens | H3 |
| 7 | Tolkning av EM-130-kategoriene for bemanningsgap | **Forkastet** til fordel for HR-002 | HR-002 er primærdata og merker gapene annerledes enn e-posten | H4 |
| 8 | H5 falsifisert | **Endret til SVEKKET** | Alle «levedyktig»-vurderingene kommer fra programmets egne folk og CIO. Ingen uavhengig verifikasjon | H5 |
| 9 | Forward-beregning (break-even 44–83 mill./år) som argument | **Brukt, men merket** som egen grovmodell og ikke NPV | Finance har ikke regnet NPV. Modellen utelater sunk cost, linjekost og ramp-up | H5, 00-oversikt |
| 10 | H2 falsifisert uten nyanse | **Skjerpet** til «primærårsak falsifisert, forsterker støttet» | Leverandørfeil er reelle (5–6 av 18, verktøy minst fem uker sent) | H2 |
| 11 | 382 mill. som tidligere prognose | **Ikke brukt.** Merket åpen | 382 står bare i e-poster fra juni. 395 står i styrepakkene | 00-oversikt |
| 12 | Klassifisering av de 12 beslutningene som «klar» eller «uklar» rett | **Brukt som antakelse**, ikke som funn | Det er AIs vurdering og bør gjennomgås av teamet | H3 |
| 13 | Rapporteringspraksis som rotårsak | **Ikke brukt som hypotese.** Beskrevet som fakta («hva dokumentene viser»), uten slutning om hensikt | Ikke testet som egen hypotese, og corpuset kan ikke avgjøre hensikt | 00-oversikt, 03-hovedanbefaling |

---

## 5. AI-bruk i hovedanbefalingen, 90-dagersplanen og presentasjonen

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Må kontrolleres av teamet |
|---|---|---|---|
| **Hovedanbefaling** ([`03`](03-hovedanbefaling.md)): syntese av seks funnfiler til en beslutning (D1–D6), alternativer og stoppkriterier | Dommer, tall og forbehold fra funnfilene | Forkastet «105 mill.» og «14–20 uker» som felles tall. Ikke brukt +77 eller +111 uten kreditt-forbehold | **D1-utformingen** (trinnvis frigivelse, port etter 30 dager) og **stoppkriteriene** er AI-forslag, ikke funn. At leverandørbytte ville kastet kredittilbudet er en slutning fra VEN-002. H2, H4 og H6 var lest via oversikten og ikke i full tekst da dokumentet ble skrevet |
| **90-dagersplan** ([`04`](04-90-dagersplan.md)): 17 tiltak med ansvarlig, tid, avhengigheter, effekt og mål | Basislinjer, datoer og navn fra kildene (HR-001, OF-014, OPS-004) | Ikke navngitt kunder. Lovet ikke noe NPV-tall | **Alle målverdier er AI-forslag.** Eirik Solheim som formell eier og ekstern verifikasjon som rapporterer til CEO er AIs vurdering. Mål som «≤ 8 integrasjoner» og «SLA ≥ 93,0 %» mangler kilde |
| **Styrepresentasjon** (6 slides, ikke i repoet): struktur, tekst og layout. ICE-prioritering av 12 tiltak | Alle tall fra 03, 04 og oversikten | Slått sammen 17 tiltak til 12. Kundenavn utelatt | **ICE-skårene er AIs vurdering.** Layout er ikke sjekket visuelt, så tekstpasning er ukontrollert. «Ca. 15 mill. i måneden» er avledet |
| **Git:** commit og push av 03 og 04 til `main` etter eksplisitt bestilling | Filene som skrevet | Hentet inn commit `e65a6bf` først (fast-forward). Ingen eksisterende fil endret | – |

---

## 6. Hva AI ikke kunne eller ikke har gjort

- **Uavhengig teknisk verifikasjon av kjernen** (H5). Alle vurderinger av «levedyktig» kommer fra interne parter.
- **Kritisk-sti-analyse.** Eneste test som rent skiller H2, H3 og H4 og tallfester H3. Ikke i corpuset.
- **Ekte NPV.** Bare grovmodell.
- **`.xlsx`-filene** ble ikke åpnet. CSV-versjonene er brukt.
- **Risikovedlegget til styrepakken 26.8** mangler, så vi vet ikke hva styret ble varslet om.
- **Årsakskoding** av SLA-fall og fornyelser, kundelønnsomhet og kontraktslengder finnes ikke.
- **Kostnadsbroen 395 → 472:** om kreditten ligger i 395 er åpent, så gapet er 77 eller 111 mill.

---

## 7. Det som gjenstår hos mennesker

| # | Hva | Hvem |
|---|---|---|
| 1 | **Kjør den uavhengige reviewen** ([`REVIEW_OPPDRAG.md`](REVIEW_OPPDRAG.md)) i en ny AI-samtale som ikke har deltatt i utformingen. Vurder hvert vesentlig punkt mot originalkildene, og **føre endringene inn i denne loggen** (oppdraget krever det) | Teamet |
| 2 | Fyll ut «Selv kontrollert»-kolonnen i H3 og H4 (står som plassholder for Person B) | Person B |
| 3 | Stikkprøver: 409 mot 395, uker-tabellen (TECH-003), OF-011-median (H1), 71/34/41 mot OPS-004, SLA-gapdekomponering mot OPS-001 (H6), klassifisering av 12 saker og OF-011 mot EM-027/140 (H3) | Person C, Person B |
| 4 | Kjør H5-regnestykket på nytt i regneark, og få Finance til å regne ekte NPV | Person A, Silje Tran |
| 5 | Kalibrer målverdiene i 04-90-dagersplanen og ICE-skårene med eierne | Teamet |
| 6 | Bekreft at Person A/B/C er riktig utledet, og fyll inn AI-bruk i oppgavefase og prompt-skriving der den er «ikke dokumentert» | Teamet |
| 7 | Legg styrepresentasjonen i repoet hvis den skal følge leveransene, og kontroller layouten visuelt | Teamet |

---

## 8. Læring: hva som fungerte, og hva som ikke gjorde det

**Fungerte:**
- **Falsifisering først.** Instruksen om å forsøke å motbevise hypotesen ga dommene H1 og H2 falsifisert og H5 svekket. 02-hypoteser forventet dette, men nå med tall og kilder bak i stedet for magefølelse, og H5 ble holdt igjen på «svekket» fordi uavhengig verifikasjon mangler.
- **Kildehierarki.** Primærdata (A) foran statusrapporter (B), parts-posisjoner (C) og enkeltuttalelser (D) fanget flere feil, bl.a. 27,6 mill. og 105 mill.
- **Vis regnestykket.** Gjorde at 14–20 uker og 82,7 uker kunne oppdages som uforenlige.
- **Merke antakelser.** Klassifiseringen av beslutningene og verdimodellen ble stående som antakelser og ikke som funn.

**Fungerte ikke, eller er risiko:**
- **Det første utkastet var for sikkert.** Situasjonsbildet inneholdt formuleringer som senere måtte rettes (pkt. 4, nr. 1–5), selv om det var skrevet etter å ha lest hele corpuset.
- **Samme AI skrev utkast og kontrollerte det.** Kontrollen er bedre enn ingenting, men ikke uavhengig. Den uavhengige reviewen gjenstår.
- **Plassholdere ble stående.** Kontrollkolonnen i H3 og H4 er ikke fylt ut av mennesker.
- **Sekundærkilder.** Hovedanbefalingen ble skrevet fra oversikten for H2, H4 og H6 og ikke fra full tekst.

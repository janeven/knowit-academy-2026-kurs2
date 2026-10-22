# OneFlow – hovedanbefaling og beslutning (til styremøtet)

*Grunnlag: [`01-situasjonsbilde.md`](01-situasjonsbilde.md), [`02-hypoteser.md`](02-hypoteser.md) og de seks funnfilene i [`hypoteser-funn/`](hypoteser-funn/00-oversikt.md). Alle tall er hentet fra «Avklarte kildekonflikter og felles tall» i [`00-oversikt.md`](hypoteser-funn/00-oversikt.md). Der korpuset ikke kan avgjøre et tall, står det som **åpent**. Dette dokumentet er kjernen som CEO-brief, lederpresentasjon, 90-dagersplan og evidenslogg skal bygges på.*

---

## 1. Anbefalingen i én setning

> **Styret bør i morgen godkjenne et kontrollert konsernreset av OneFlow: erkjenne 472 mill. og 30. juni 2027 som nytt utgangspunkt, flytte beslutningsretten fra programmet til CEO, og stanse nye migreringsbølger til fakturakontroll og eierskap er løst. Verken «fortsett uendret» eller «stopp programmet» er forsvarlige.**

Anbefalingen er et *konsernreset*, ikke et IT-reset. Årsaken er at den eneste hypotesen som holder som rotårsak (H3) er et Nordflow-internt styringsproblem. Et teknisk eller kommersielt reset alene vil gi samme resultat om seks måneder.

---

## 2. Beslutningene som må godkjennes

| # | Beslutning | Hvem beslutter | Når | Hviler på |
|---|---|---|---|---|
| **D1** | **Ny styringsprognose og åpenhet.** Trekk tilbake 395 mill. og 28.2.2027. Godta **472 mill. netto** (455–494) og **30.6.2027** som ny planleggingsforutsetning, og **128 mill./år fra 2029** (ikke 210 fra 2028). Rammen på 280 er ikke lenger gyldig. Ny ramme besluttes ved port etter 30 dager. Frem til da frigis kun forpliktet beløp (91) og løpende drift, og resten av det uforpliktede (63 netto) holdes tilbake. *Forslaget til trinnvis frigivelse er vår utforming, og CFO må bekrefte beløpene.* Fremover rapporteres 472 til styret og banken, ikke 395. | Styret | 18.9 | H1, H5 |
| **D2** | **Konsernreset av styring.** CEO overtar beslutningsretten for programmet: navngitt beslutningstaker per sakstype, **72 timers frist med automatisk eskalering til CEO**, krav til innhold i beslutningsunderlag (inkl. operativ konsekvens), **håndhevede portkriterier** (prosesseiere, dataprofilering, testdata, bemanning), **scope-frys** med unntaksprosess kun for juridiske, regulatoriske og kontraktsmessige krav. Prioriteringsregelen mellom linje og program fastsettes av CEO og forhandles ikke. | CEO (styret tar til orientering) | Styringsgruppen 22.9 | H3, H4 |
| **D3** | **Sekvensering og kundesikring.** Ikke åpne Bølge 2 og 3, og ikke utvid Bølge 1 utover pilotens 42 kunder før fakturakontroll og eierskap er løst og korreksjonsraten er under 2,5 % (pilot: 7,8 %). Utnevn **én formell eier** av kunde- og inntektsrisiko. Lag lederplan per berørt fornyelse (146 mill. i årsverdi, 71 direkte OneFlow-signal, første frist 15.10). | CEO | 22.9 | H1, H6 |
| **D4** | **Beskytt kapasiteten.** Skjerm de ~23 kritiske rollene i data, test og integrasjon, fjern dobbeltallokering, og finansier backfill i drift (godkjent så langt: maks 1,8 mill. i fire uker, og dette er for lite for et gap på 49 FTE). | CEO / CFO | 22.9 | H4 |
| **D5** | **Kommersielt spor mot Convergent.** Tilby scope-frys og felles styrt plan som vilkår for kreditten. Bruk 34 mill. som *krav* og ~12 mill. som «nær sikkert», aldri som innregnet kreditt. Ikke bytt leverandør. | CFO / CIO | Før leverandørens frister | H2 |
| **D6** | **Verifiser før irreversible valg.** Bestill uavhengig teknisk verifikasjon av kjernen (2–3 uker) og en reell NPV på 472 / 128 / redusert kjerne. Sett en port ved dag 30 med stoppkriterier (se pkt. 6). | CIO / CFO | Start umiddelbart | H5 |

**Det som ikke skal besluttes i morgen:** full stopp, leverandørbytte eller redesign av målarkitekturen. Disse alternativene har ikke støtte i funnene (pkt. 4). De skal heller ikke være utelukket for alltid, bare utløst av dag 30-porten.

---

## 3. Begrunnelse: hva hypotesetestene viser

| Hyp. | Dom | Hva det betyr for beslutningen |
|---|---|---|
| **H1** Gul og håndterbar | **Falsifisert** | Rapportert 395 holder ikke: **409 mill. er allerede påløpt eller forpliktet**. Alle spor er **11–26 uker bak recovery-planen**, som selv brukte de myke milepældefinisjonene, og alle fire forutsetningene i recovery-planen er brutt. → *D1: erkjenn 472 og juni 2027.* |
| **H3** Styring og beslutningsdisiplin | **Støttet** (rotårsak) | Programmet startet i strid med mandatets og styrets portkrav. Alle 12 kritiske saker tok mer enn fire ganger målet (**median 35,5 dager mot 7**), og de blokkerer 10 av 18 uferdige integrasjoner. Saker med klar eier tok like lang tid, så problemet er beslutningsdisiplin og ikke bare uklar rett. → *D2: frister, eskalering til CEO og håndhevede porter, ikke bare en ny RACI.* |
| **H4** Kapasitetskonflikt | **Svekket** (forsterker) | Gapet på 49 FTE (plan 168, reelt 119) er reelt og på kritisk sti. Det består fordi ingen tar prioriteringsbeslutningen. Å fylle gapet alene løser ikke saker som venter på beslutning eller lokalkunnskap. → *D4, men som støtte til D2.* |
| **H2** Leverandøren er hovedårsak | **Falsifisert** (primær) | Leverandørfeil står for 5–6 av 18 uferdige integrasjoner (28–33 %), og begge parter er enige om at minst halvparten er kundeskapt. Verktøyet var minst fem uker forsinket, og kontrakten gir ikke grunnlag for å tilskrive hele avviket Convergent. → *D5: bruk kreditten som forhandlingskort, ikke som forklaring.* |
| **H5** Kjernen er ikke levedyktig | **Svekket** (ikke falsifisert) | 46 av 64 integrasjoner er klare, bare 5–6 har kode- eller konfigurasjonsfeil, og ingen kilde sier at kjernen er ubrukelig. Vår grove forward-beregning gir break-even på 44–83 mill./år mot 128. Svakheten er at ingen har verifisert dette uavhengig, og fire danske kontraktspunkter er uavklarte. → *D6: fortsett på arbeidsantakelsen, men verifiser og sett port.* |
| **H6** Kunde- og inntektsskade dominerer | **Svekket** (konsekvens) | Målbar kunde- og resultateffekt er ≤ ~22 mill. mot +77 mill. i programkost. Fornyelsesrisikoen er likevel akutt i tid, og 71 av 146 mill. har direkte OneFlow-signal. → *D3: sekvensering og kundesikring, uavhengig av om H6 løftes.* |

**Mønsteret:** de to «ytre» forklaringene (leverandør og teknologi) holder ikke som hovedårsak. Den som holder er Nordflows egen beslutningsdisiplin, forsterket av en kapasitetskonflikt ingen har avgjort. Derfor må beslutningen ligge hos konsernledelsen.

---

## 4. Hvorfor ikke de andre alternativene

| Alternativ | Hva det innebærer | Hvorfor ikke |
|---|---|---|
| **A. Fortsett uendret** (H1) | Hold 395 og 28.2.2027, avvent kreditt og reset | Falsifisert på kost og dato. Styret får 395 selv om 472 er kontrollert, og vedtaket 26.8 (BOARD-005 pkt. 5) krever at vesentlige endringer legges frem uten å vente på ordinær syklus. CFO vurderer dette som alternativet med høyest gjennomføringsrisiko. |
| **B. Kontrollert konsernreset** | Pkt. 2 | **Anbefalt.** Treffer rotårsaken (H3), beholder en kjerne som alt tyder på er levedyktig (H5), og beskytter kundene mens det gjøres. |
| **C. Stopp eller redesign** (H5) | Avvikle eller radikalt redusere | Ikke støttet: kjernen er ikke vist ubrukelig, og stopp utløser avvikling, kontraktskost og minst to års dobbeltlandskap (CFO). Åpen for gjenvurdering ved dag 30-porten. |
| **D. Kommersiell eskalering eller leverandørbytte** (H2) | Krev full kreditt, bytt Convergent | Falsifisert som primærårsak. Et bytte ville ikke fjernet de 10 av 18 integrasjonene som er kundeskapt, og vil kaste bort kredittilbudet (24–34 mill.) som forutsetter scope-frys og felles plan. |

---

## 5. Hva som skjer hvis styret ikke beslutter

- **31.12.2026** passeres uten at Bølge 1 er gjennomført (en pilot på 42 er migrert, men selve bølgen er ikke avsluttet). Fullføring skyves til mest sannsynlig 30.6.2027.
- **Kostnaden** løper mot 506 mill. hvis kreditten uteblir. 154 mill. gjenstår å bruke, avledet til ca. 15 mill. i måneden.
- **Leverandørens kredittilbud** (24–34 mill.) forutsetter scope-frys og felles plan, og fristen 15.9 er passert.
- **Kunder:** fem fornyelser på 146 mill. forfaller 15.10–31.12 mens SLA (95,8 → 91,4 %) og churn (5,0 → 6,7 %) fortsatt forverres.
- **Mennesker:** 12 nøkkelpersoner har sluttet siden januar og 37 er over 120 % belastning. Lokalkunnskap kan ikke kjøpes inn.
- **Tillit:** banken møtes 25.9. Å legge frem 395 etter at 472 er kontrollert er en ansvarsrisiko for konsernledelsen.

---

## 6. Hva ville endre anbefalingen (stoppkriterier ved dag 30)

Anbefalingen forutsetter at kjernen er levedyktig, men det er en *arbeidsantakelse* som ikke er uavhengig verifisert. Styret bør derfor bli enig om disse utløserne på forhånd:

1. Uavhengig teknisk verifikasjon finner strukturelle arkitekturfeil i Nexus/ERP-kjernen → vurder redusert kjerne eller stopp (alternativ C).
2. En reell NPV på 472 / 128 er negativ også for en redusert kjerne → samme.
3. De fire danske kontraktspunktene (indeksvarsling, servicevindu, separat fakturamottaker, oppsigelse) lar seg ikke modellere → egen løsning eller utsatt Danmark-bølge.
4. Kritiske beslutninger fortsatt tar mer enn 72 timer etter dag 30 → CEO leder programmet selv.
5. Convergent avviser scope-frys som vilkår → kommersiell eskalering (D5 revurderes).

---

## 7. Forbehold: det vi ikke vet, og hvordan det håndteres i CEO-briefen

| Åpent punkt | Hva vi sier i mellomtiden | Eier |
|---|---|---|
| **Ligger kreditten (34) allerede i 395?** Gapet til 395 er enten 77 eller 111 mill. | «472 netto forutsetter full kreditt på 34. Uten kreditt er kostnaden 506.» Ikke bruk +77 eller +111 uten dette forbeholdet. | Silje Tran |
| **Kritisk-sti-effekten av H3 er ikke tallfestet.** H3 er støttet, ikke sterkt støttet. | Si at beslutningsdisiplin er *hovedårsak etter bevisene vi har*, og be PMO om en kritisk-sti-analyse. | Julie Nystad, Lars Pettersen |
| **Verktøyforsinkelsen:** fem uker (6.5) eller opptil 10,6 uker (13.6)? | «Minst fem uker.» Påvirker kredittkravet. | Lars Pettersen, Ole Martin Kvale |
| **Kundenavn på fornyelsene** (OPS-004 og TH-022 stemmer ikke). | Bruk totalen 146 / 71 / 34 / 41, ikke navn i styrepapirer. | Beate Høyer |
| **Rapporteringspraksis** er ikke testet som egen hypotese. | Skriv *hva dokumentene viser* (omdefinerte milepæler, baseline byttet uten styrebehandling, bølgekutt og bottoms-up ikke i styrepakken). Ikke slutt noe om hensikt. | Team |
| **NPV er ikke regnet.** Vår break-even (44–83 mill./år) er en grovmodell. | Kall den «grov indikasjon», ikke NPV. | Silje Tran / Thomas Vik |

*Styrets tidligere informasjon:* Finans hadde 438 (17.6) og 459 (18.8) da styret fikk 395. Risikovedlegget til styrepakken 26.8 er ikke i korpuset, så vi vet ikke hva styret ble varslet om.

---

## 8. Hvordan dette bindes til de fem leveransene

| Leveranse | Skal vise |
|---|---|
| **CEO-brief (2 sider)** | Pkt. 1 som overskrift, pkt. 2 som beslutningstabell, pkt. 3 (første linje per hypotese) som begrunnelse, pkt. 7 som forbehold. |
| **Lederpresentasjon (~6 slides)** | 1) Situasjonen, 2) Rotårsaker, 3) Konsekvens uten handling, 4) Alternativene A–D, 5) Anbefalingen D1–D6, 6) Stoppkriterier og neste 30 dager. |
| **90-dagersplan** | D1–D6 brutt ned i tiltak med ansvarlig, avhengighet og mål. Dag 30-porten er første milepæl. |
| **Evidenslogg** | Pkt. 3 og pkt. 7, med kildekvalitet (A–D) fra funnfilene. |
| **AI-arbeidslogg** | AI-seksjonene (§9) i hver funnfil, pluss at dette dokumentet er syntetisert av Claude fra funnfilene og må kontrolleres av teamet. |

---

## 9. AI-bruk (til AI-arbeidsloggen)

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Må kontrolleres av teamet |
|---|---|---|---|
| Syntese av hovedanbefaling fra de seks funnfilene, situasjonsbildet og hypotesene | Dommer, tall og stoppkriterier hentet fra funnfilene | Forkastet «105 mill. OneFlow-effekt» (brukt 71 direkte), «14–20 uker bak original» som felles tall (brukt «11–26 uker bak recovery»), og +77/+111 uten kreditt-forbehold | (1) **D1-utformingen** (trinnvis frigivelse, port etter 30 dager) og **stoppkriteriene i pkt. 6** er vår foreslåtte utforming, ikke funn fra korpuset. (2) At alternativ D (leverandørbytte) ville kastet kredittilbudet er en slutning fra VEN-002, ikke en kilde som sier det. (3) Kun H1, H3 og H5 er lest i sin helhet i denne økten. H2, H4 og H6 er brukt via oversikten ([`00-oversikt.md`](hypoteser-funn/00-oversikt.md)). |

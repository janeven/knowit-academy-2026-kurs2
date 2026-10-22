# OneFlow – situasjonsbilde (Oppgave 1)

*Grunnlag: hele CaseCorpus (240 e-poster i 40 tråder, 75 dokumenter/datasett). Siste datert kilde er 16. september 2026. Tall merket (A) er kontrollerte primærdata, (B) er ledelsens kuraterte statusrapporter, (C) er parts- eller utkastsposisjoner, (D) er enkeltuttalelser i e-post. Kilde-ID-er står i klammer.*

---

## Problemformulering (leveransen)

> **Dette er situasjonen i dag.** OneFlow er ikke «gul – stabiliserende», slik styret sist fikk høre (26. august). Programmet er 14–20 uker bak original plan på sporene prosess, integrasjon og data (målt mot sporenes egne milepæler), og 26–31 uker bak for migreringsbølgene (målt mot TECH-003), fullføring flytter seg fra 31. des 2026 til mest sannsynlig juni 2027, og kontrollert sluttkostnad er **472 mill. (455–494)**. Det er 77 mill. over de 395 som er rapportert og 192 mill. over styrets ramme på 280. Allerede påløpt (318) overstiger rammen. Varig årlig gevinst er korrigert fra 210 til **128 mill. fra 2029**. Samtidig forverres kundedriften månedlig (SLA 95,8 → 91,4 %, churn 5,0 → 6,7 %), og fem fornyelser på **146 mill.** i årsverdi forfaller innen 31. desember. Første migreringsbølge er skåret fra 286 til 42 kunder, og selv den har 7,8 % fakturakorreksjon.
>
> **Den skyldes i hovedsak** (1) et program som ble startet uten at portkriteriene var oppfylt: prosesseiere, dataprofilering, testdata og bemanning. Det ble deretter drevet av en beslutningsstruktur som ikke avgjør saker (median 35,5 dager mot mål 7) og et scope som vokste uten uttak. (2) Linje og program konkurrerer om de samme ~170 personene uten prioriteringsregel, så ressursene trekkes frem og tilbake mellom drift og program. (3) En leverandør som har reelle feil (verktøy fem uker forsinket, to arkitektbytter), men som bare forklarer en mindre del av gapet. (4) En rapporteringspraksis som har skjult størrelsen på avviket: milepæler er omdefinert, baseline er byttet uten styrebehandling, og bølgekuttet og bottoms-up-prognosene nådde ikke styret.
>
> **Hvis vi ikke handler nå** passerer styrets formelle sluttdato (31. des) uten at Bølge 1 er gjennomført (en pilot på 42 kunder er migrert og under hypercare, men selve bølgen er ikke avsluttet). Kostnaden løper mot 506 mill. hvis leverandørkreditten uteblir. Nøkkelpersonene i data og test, som ikke kan erstattes på kort sikt, slutter eller brenner ut. Leverandørens kredittilbud (24–34 mill.) faller bort fordi det forutsetter scope-frys og felles plan. Fornyelser for opptil 105 mill. avgjøres i oktober–desember mens kundeopplevelsen fortsatt går ned. Konsernet må i tillegg forklare banken og styret hvorfor 395 ble stående etter at 472 var kjent.

---

## Steg 1 – Nåsituasjon

### 1.1 Fremdrift

| Mål | Original plan (styrevedtatt) | Recovery baseline (intern, mars 2026) | Nåværende prognose (sept. 2026) |
|---|---|---|---|
| Sluttdato | 31.12.2026 (+ stabilisering Q1 2027) [BOARD-002] | 28.02.2027 [OF-013] | **30.06.2027** (CIO), Danmark 30.06.2027 [TECH-002, TECH-003] |
| Dataprofilering | 31.03.2025 | 30.04.2026 | 31.10.2026 (14/27 objekter godkjent) [TECH-003] |
| Bølge 1 cutover | 31.05.2026, 286 kunder | 30.09.2026 | **18.12.2026, 42 kunder** [TECH-003] |
| Bølge 2 (NO/SE) | 30.09.2026 | 15.12.2026 | 31.03.2027 |
| Bølge 3 (DK) | 31.12.2026 | 28.02.2027 | 30.06.2027 |

Status per spor (A):

- **Data/migrering:** 14 av 27 kritiske objekter godkjent (var 16 i juni; kriteriene ble skjerpet). Kundemaster har 11,7 % duplikater mot krav <2 % (12,4 % i mars). Fakturamottaker mangler eller er tvetydig i 8,4 % av aktive kontrakter. Sporet er ~20 uker bak original plan, og leder for data melder rød [TECH-004, EM-076, EM-088].
- **Prosess:** 9 av 23 ende-til-ende-prosesser er signert og har kontrollmodell. Sporet er ~14 uker bak. Fire prosesser har stått uten beslutning i 36–52 dager [EM-116, EM-118].
- **Plattform/integrasjon:** 18 av 64 kritiske integrasjoner er ikke produksjonsklare (21 i juni, 19 i august). Sporet er 11 uker bak recovery og 17 bak original [TECH-005, EM-104].
- **Kundeovergang:** Bølge 1 er skåret fra 286 til 42 kunder (−85 %). 34 av 42 er stabilisert, 8 har åpne portal- eller ordreavvik, og alle 42 ligger i manuell fakturakontroll [EM-078, EM-087, OPS-003].
- **Testgrunnlag:** I juli hadde test representative løp for 61 av 286 kunder, og bare 38 av disse var uten alvorlighetsgrad 1–2-feil. 14 av 73 testscenarioer mangler forventet resultat [EM-083, EM-110].

**Om statusfargen:** Samlet «gul» er en definisjonssak. «Teknisk klar for test» ble fra mars regnet som lukket milepæl, og Bølge 1 regnes «på plan» med redusert pilot [OF-003, OF-013, EM-085]. PMO foreslo **rød** i utkastet 14. sept. [OF-008], og dataleder nektet å skrive «følger plan» [EM-008]. Etter instruks fra programdirektør ble totalen holdt gul [EM-010, EM-011].

### 1.2 Økonomi

| Størrelse | Beløp (mill.) | Kilde / status |
|---|---|---|
| Styrets ramme (18.12.2024) | **280** (inkl. 28 reserve) | BOARD-002, FIN-001 (A) |
| Rapportert prognose til styret | **395** (ikke godkjent som ramme) | BOARD-003/004/005, OF-013 (B) |
| Bottoms-up juni | 438 | FIN-003 (A, ikke vist for styret) |
| Bottoms-up august v5 | 459 (455–494) | FIN-004 (A, ikke vist for styret) |
| **Kontrollert prognose 16.09** | **472 netto** (506 brutto − 34 antatt kreditt), intervall 455–494 | FIN-005, EM-173 (A) |
| Påløpt per 31.08 / forpliktet etter | **318** / 91 (sum 409), 63 gjenstår uforpliktet | FIN-005, FIN-007 (A) |
| Linjekost utenfor programmet (2026 hittil) | 11,2 (overtid, innleie, krediteringer, SLA-kreditter) | OPS-002 (A) |

Vurdering:

- **Rammen er allerede sprengt av påløpt kost** (318 > 280, +14 %). Med forpliktelser er det 409 (+46 %). Definisjonene (aktiverbar intern tid m.m.) bør sjekkes mot rammens definisjon, men retningen er entydig.
- **Brofaktorer fra 395 til 506 brutto** (Silje Tran): forlengelse 41, ekstra data/test 22, operativ stabilisering 19, øvrige risikoer netto 29 = 111. 395 + 111 = 506. Dette summerer til *brutto*, mens BOARD-004 sier at 395 inkluderer forventet kreditt. **Det er uklart om 395 allerede har kreditten i seg, og det må avklares før tallet brukes overfor styret.**
- **Leverandørkreditt:** Nordflows eget krav er 34. Ole Martin Kvale vurderer ~12 som nær sikkert og 12–22 til som forhandlingssak [EM-065]. Convergent tilbyr 24–34 *kun* mot scope-frys og felles styrt plan, avviser netto 34 og dokumenterer 31 kundeskapte forsinkelser [VEN-002, EM-067]. Uten kreditt er kostnaden 506. Med bare de «sikre» 12 er den 494, altså toppen av intervallet.
- **Rapporteringsgap:** Finans hadde 438 (17. juni) før styrepakken 24. juni og 459 (18. aug.) før styremøtet 26. aug. Begge ganger ble 395 stående [EM-167, EM-169, EM-170, EM-012]. Styret ble fortalt at ubesluttede forlengelses- og stabiliseringsposter lå *utenfor* prognosen, men størrelsen fremgår ikke av pakken [BOARD-004, BOARD-005].
- **Gevinster:**

| | Opprinnelig | Korrigert |
|---|---|---|
| Varig årlig gevinst | 210 fra 2028 | **128 fra 2029** |
| Dobbelttelling mot Cobalt-planen | – | −40 (26 bemanning + 14 innkjøp) |
| Øvrig nedjustering | – | −42 |

  Styret ba allerede i desember 2024 om linje-for-linje-avstemming. Den kom først i september 2026 [BOARD-002, FIN-006, EM-176–179]. Business casens NPV (+218 mill. ved 9 %) er ikke regnet om. Som illustrasjon alene: hvis gevinstprofilen skaleres ned til 128/210 (61 %) uten forskyvning, blir kumulativ brutto 2025–29 ≈ 378 mill., lavere enn ny kostnad på 472. Det er ikke en NPV-beregning, men viser at forutsetningen om lønnsomhet må regnes på nytt.

### 1.3 Teknologi

- **Utgangspunktet er komplekst:** tre ERP-varianter, fire CRM, to feltserviceplattformer, tre portaler og over 70 punktintegrasjoner. Dette forklarer *hvorfor* transformasjonen trengs, men ikke hvorfor programmet er forsinket [TECH-001].
- **Kjernen vurderes som levedyktig.** CIO: «ikke et totalhavari; bygg har gått foran stabile prosesser, data og scope.» Test og plattformleder støtter dette [TECH-002, EM-185, EM-196].
- **Årsak til de 18 uferdige integrasjonene** (to tellinger som stemmer overens om kundesiden):

| Kategori | TECH-005 (Nordflow, 9.9) | Convergent (VEN-002) |
|---|---|---|
| Leverandørfeil | 5 | 5 |
| Nordflow beslutning/krav + testdata | 6 + 4 = 10 | 10 |
| Delt ansvar/omarbeid | 3 | 3 |

  Plattformleder har en tredje telling (6/5/4/3) [EM-104]. Under alle tellinger er **minst halvparten kundeskapt**, og 28–33 % leverandørskapt.
- **Avhengighetskjeden** er data → prosessbeslutning → integrasjonskonfigurasjon → representative testdata → kundeovergang. Nexus alene gjør ikke migreringen klar [OF-012].
- **Migreringsverktøyet** skulle vært i test 31. mars. Alle kilder sier «fem uker forsinket» (leveranse 6. mai), men plattformleder skriver at verktøyet *kom 13. juni*, og at det da feilet på nordisk fakturavariant [EM-052, EM-055, EM-056]. Forsinkelsen kan altså være undervurdert. Dette bør sjekkes mot kontrakten og mot kredittkravet.

### 1.4 Drift

KPI-utvikling (A, OPS-001, målet gjelder 2026):

| KPI | Jan | Apr | Jun | **Aug** | Mål |
|---|---|---|---|---|---|
| SLA overholdt % | 95,8 | 94,9 | 93,2 | **91,4** | 97,0 |
| Førstegangsløsning % | 81,6 | 80,2 | 77,8 | **74,9** | 84,0 |
| Svartid (sek.) | 48 | 62 | 91 | **132** | 35 |
| Fakturakorrigering % | 2,0 | 2,4 | 3,3 | **4,9** | 1,2 |
| Fravær kundedrift % | 5,5 | 6,0 | 6,7 | **7,1** | <5,0 |

- Alle fem KPI-er går feil vei i hvert av de fire målepunktene (jan., apr., jun., aug.). Køen passerte 1 900 saker i juli [EM-143].
- **Årsaksforhold:** Fallet er størst der fagfolk er avgitt til OneFlow. Fravær (7,1 %), sesong og markedsforhold bidrar også, og driften sier selv at utviklingen ikke kan tilskrives programmet alene [OPS-002, EM-136].
- **Bemanning (uke 35):** plan 168 FTE, reelt 119, **gap 49** (data/migrering 21, test/integrasjon 18, prosess/kundeovergang 10). 37 personer er over 120 % belastning, og 12 nøkkelpersoner har sluttet siden januar [HR-002, EM-130, EM-132]. Gapet var der også i februar: bekreftede allokeringer var 126, ikke 168, fordi 50 %-ressurser ble talt i både linje og program [EM-127].
- **Ressurstrekk frem og tilbake:** Drift tok tilbake fire kundespesialister og tre testressurser i mai og igjen i juli. Håkon Berg anslår at dette kostet seks uker i data/test [EM-141, EM-143, EM-145]. Backfill-beslutningen sto åpen i 56 dager; Thomas Vik godkjente 6. sept. fire ukers backfill, maks 1,8 mill. [EM-140].
- Pulsmåling: «beslutninger tas raskt nok» 32/100, «planen er realistisk» 36/100, arbeidsbelastning 39/100. HR peker på prioritering og roller, ikke vilje, som hovedtema [HR-003, EM-197, EM-200].

### 1.5 Kunder

- **Pilot (42 kunder):** 17 trengte manuell fakturakontroll, 8 har portal-/ordreavvik, fakturakorreksjon 7,8 % (mot 2,0 % i porteføljen i januar). Ingen systematisk havari, kritiske tjenester ble holdt oppe, og minst én kunde melder at ny portal fungerer bedre. Utvalget er lite og *ikke representativt* [OPS-003, EM-084, EM-096].
- **Fornyelsesrisiko (OPS-004, 12. sept.):** fem kunder, 146 mill. årsverdi.

| Kunde | Verdi | Fornyelse | Signal | Vurdering |
|---|---|---|---|---|
| Metrohandel | 23 | 15.10 | Priskrav | Pris/konkurrent |
| EnergiVest | 42 | 31.10 | Faktura-/portalfeil | OneFlow |
| Nordbygg Eiendom | 34 | 30.11 | SLA/svartid | OneFlow/ressurstrekk |
| Skandia Industri | 29 | 15.12 | Manglende ordrestatus | OneFlow |
| Svea Terminal | 18 | 31.12 | Konkurrenttilbud | Marked |

  Tre av fem (105 mill. = 72 %) har OneFlow-signaler: **71 mill. direkte** (EnergiVest, Skandia) og **34 mill. indirekte** via ressurstrekk (Nordbygg). To (41 mill.) har andre hovedårsaker. **Kundenavnene i OPS-004 er ikke de samme som i e-posttråd TH-022** (Fjordkraft, ScanMarine, MedicoLog, Vestbygg, Arctiq), selv om totalen 146 og splitten «tre av fem» er lik. Det må avklares før kunder navngis i styrepapirer [EM-147–150].
- **Churn (annualisert):** 5,0 → 6,7 % (mål 4,3 %).
- **Inntekts-/regnskapseksponering (OPS-005):** 27,6 mill. er en *blandet* sum og bør ikke kalles tap.

| Post | Mill. | Natur |
|---|---|---|
| Fakturerbare ordre >45 dager | 16,8 (16,5 per 11.9) | Arbeidskapital/timing |
| Bekreftet kreditering (pilot) | 3,6 | Bekreftet resultateffekt |
| Mulig kontraktseksponering | 8,9 | Risiko, ikke bokført |
| Overlapp | −1,7 | Samme saker |
| **Reell resultatrisiko** | **3,6 + 7,2 = inntil 10,8** | |

  Av de 16,8 er 6,2 uavklart fakturamottaker og 3,4 venter pris-/kontraktsavklaring; resten er kundetvist (2,1) og ordinært etterslep (5,1) [EM-154].
- **Eierskap:** Ingen *formell* eier av samlet kunde- og inntektsrisiko. RAID R-051 har tom eier, og styringsgruppen 10. sept. utsatte det [OF-010, OF-014, EM-038]. Midlertidig: Eirik Solheim koordinerer operativt, finans følger beløp, og Beate Høyer eier oversikten over fornyelsene [EM-039, EM-151].

---

## Steg 2 – Foreløpige rotårsaker

Rangert etter hvor godt de er støttet av uavhengige kilder. Rotårsaker er *hvorfor*, forsterkere gjør det verre, og symptomer er det vi ser.

### Rotårsaker

**R1. Programmet startet uten at portkriteriene var oppfylt, og ble ikke stoppet.**
Mandatet krever at prosesseiere, dataprofilering, representative testdata og bemanning er bekreftet *før* bygg, og styret sa det eksplisitt i desember 2024 [OF-001, BOARD-002]. Likevel var prosesseiere ikke utpekt, dataprofilering var 22 % ferdig ved godkjent roadmap, og alle spor startet parallelt i januar 2025 med mobilisering på tre av seks uker [OF-001, OF-002]. Datakvalitetsproblemene (dubletter, fakturamottaker i fritekst) ble varslet i oktober 2025 [EM-069]. Dato ble satt før kvalitetskriterier [EM-186].

**R2. Beslutningsretten er uklar og beslutningene tas for sent.**
Mandatet sier ikke hvem som avgjør konflikter mellom prosesseier, program og land [OF-001]. Resultatet er at beslutningene i loggen tok median 35,5 dager mot mål 7. Ti av tolv kritiske saker brukte over 30 dager, og seks er fortsatt åpne [OF-011, EM-030]. Hver av dem blokkerer noe konkret: kontraktsmodell → tre integrasjoner og testdata, prisindeks → testscenario, ordre-til-faktura → kontrollmodell. Recovery-planen *forutsatte* 7-dagers beslutninger og skulle revurderes ved brudd [OF-013], men det ble ikke gjort. Uenigheten om hvem som kan fryse scope har selv forsinket reset-notatet [EM-035, OF-014].

**R3. Scope vokste uten uttak og uten full konsekvensanalyse.**
28 endringsønsker (sept. 2025) ble 47 (nov. 2025), og bare 19 hadde full kostnads-/tidsanalyse. Foreløpig effekt er 63 400 timer og 38 mill. Novembermøtet godkjente resten uten full analyse, og ingen funksjonalitet er tatt ut [EM-040, EM-043, EM-046]. Fire danske kontraktspunkter er reelle krav (indeksvarsling, servicevindu, separat fakturamottaker, oppsigelse). De øvrige ønskene har ikke funnet lov- eller kontraktsgrunnlag [EM-124, EM-126].

**R4. Linje og program konkurrerer om de samme menneskene uten prioriteringsregel.**
Matrisen «gir ingen automatisk prioritet» [HR-001], og planen telte 168 FTE der 126 var bekreftet. Tretti-syv personer er over 120 %, og tolv har sluttet. Linjeledere trekker ressurser tilbake for å berge SLA, og det forsinker programmet, som igjen forlenger dobbeltlandskapet og belastningen i drift [EM-129, EM-143, EM-144]. Dette er en selvforsterkende sirkel.

### Forsterkere

**F1. Rapporteringspraksis som skjuler avviket.** Baseline ble byttet fra original til recovery uten at styret behandlet en ny ramme [OF-013, BOARD-005]. Milepælsdefinisjonen ble endret fra «forretningsgodkjent» til «teknisk klar for test» [EM-024]. Gul total ble beholdt mot PMO og arbeidsstrømledere [EM-010, EM-017, OF-008]. Bølgekuttet (286 → 42) og bottoms-up-tallene ble holdt utenfor styrematerialet, og «detaljene tas muntlig dersom styret spør» [EM-013, BOARD-004]. Styrets krav om kvartalsvis rapportering av kostnadsprognose, gevinster, kundepåvirkning og de fem største risikoene er ikke oppfylt [BOARD-002, BOARD-005]. Dette forklarer *hvorfor ingen grep ble tatt tidligere*, ikke selve forsinkelsen. Dokumentene viser *hva* som ble gjort, ikke *hvorfor*, og vi trekker ingen slutning om hensikt.

**F2. Leverandørsvikt.** Verktøyet var fem uker forsinket (muligens mer, se 1.3), to arkitektbytter, 5–6 av 18 integrasjoner med leverandørfeil, og én defekt i mappingmotoren. Convergent aksepterer dette [VEN-002, EM-055, EM-111]. Samtidig dokumenterer Convergent at elleve designbeslutninger kom 4–9 uker for sent, at testdata kom over tre uker for sent (bekreftet av Nordflows plattformleder) og 31 kundeskapte forsinkelseshendelser [EM-055, EM-108]. Kontrakten gir ikke grunnlag for å tilskrive hele avviket én part [VEN-001].

**F3. Datakvalitet og uklare forretningsregler.** Feltet fakturamottaker, prisindeks og servicekreditt har ikke entydig struktur. Generell rensing løser ikke uklare regler, og det finnes ingen navngitt dataeier for kontraktsmaster (beslutningen har vært åpen i 32 dager) [TECH-004, OF-011].

**F4. Gevinstcasen var overoptimistisk fra start.** 40 mill. er dobbelttelt mot Cobalt-synergiplanen, og ytterligere 42 mill. er nedjustert eller forskjøvet [FIN-006]. Dette er ikke årsak til forsinkelsen, men til at *verdien* av å fullføre er lavere enn styret ble fortalt.

### Symptomer og støy (ikke rotårsaker)

- Fallende SLA, churn, fakturakorreksjoner, 1 900-saks-kø, 37 over 120 %, avganger.
- Lav motivasjon eller «endringsmotstand». Pulsmålingen peker på prioritering og kapasitet, og HR sier at lav motivasjon ikke forklarer de opprinnelige data-, scope- og beslutningsproblemene [HR-003, EM-201].
- **Project Aurora** (≈0,6 FTE delt arkitekt) forklarer ikke forsinkelsen [OTHER-001, EM-221].
- De vanlige kundesakene i tråd TH-039 og ESG-/kontor-/reisetrådene (TH-032–038, TH-040) har ikke med OneFlow å gjøre.
- Utsatt fakturering (16,8 mill.) er i hovedsak arbeidskapital og ikke tap.

---

## Steg 3 – Konsekvens av å ikke handle

Tidshorisont: beslutning om reset skal tas i styringsgruppen 22. sept., banken møtes 25. sept., og første fornyelse faller 15. okt.

| Område | Hva skjer uten handling | Forankring |
|---|---|---|
| **Styring og formelle rammer** | Styrets formelle sluttdato (31.12.2026) passeres om 3,5 måneder uten at Bølge 1 er gjennomført. Rammen er allerede overskredet i påløpt kost. Styrevedtaket 26. aug. krever at vesentlige endringer i kostnad, dato, omfang og kundeeksponering legges frem *uten å vente på ordinær syklus*. 472 og juni 2027 er slike endringer. | BOARD-005 pkt. 5 |
| **Kostnad** | 154 mill. gjenstår å bruke (91 forpliktet + 63 uforpliktet), ca. 15 mill. i måneden til juni 2027 (avledet). Uten kreditt 506, ved scope-vekst eller høyt scenario opptil 494 *med* kreditt, og dertil kommer ca. 11 mill. linjekost og voksende. | FIN-005, FIN-004, OPS-002 |
| **Leverandør** | Convergent bygger sin plan på scope-frys 15. sept. og lukkede kundebeslutninger. Datoen er passert, og planen er «indikativ». Kreditttilbudet (24–34) forutsetter frys og felles styrt plan. Uten handling mister vi forhandlingsposisjonen for opptil 34 mill. | EM-060, VEN-002 |
| **Kunder og inntekt** | Fornyelser for 146 mill. forfaller 15.10–31.12 (105 mill. med OneFlow-signaler, hvorav 71 direkte). SLA/churn-trenden (−0,6 til −0,9 pp SLA per måned, +0,24 pp churn per måned) gir naiv ekstrapolering mot ca. 88–89 % SLA og ca. 7,5–7,7 % churn ved årsslutt. Dette er ren lineær fremskriving og ikke en prognose. Neste bølge uten løst fakturakontroll skalerer problemer fra 42 til 286 kunder; manuell kontroll er håndterbar for 42, ikke for 286. | OPS-001, OPS-004, EM-078 |
| **Mennesker** | Nøkkelkunnskap om gamle kontrakter og grensesnitt kan ikke kjøpes inn eksternt. Tolv har sluttet på åtte måneder, 37 er over 120 %. Hver ny avgang forsinker kritisk sti og forsterker sirkelen mellom linje og program. | EM-132, EM-133, HR-002 |
| **Verdi** | Gevinsten er 128 (fra 2029), ikke 210 (fra 2028). Hver måneds forsinkelse forskyver den ytterligere, mens dobbeltlandskap og leverandørkost løper. Full stopp ville gi avvikling, kontraktskost og minst to års dobbeltlandskap, og er ikke et alternativ uten at kjernen er ubrukelig. | FIN-006, EM-195 |
| **Finansiering og tillit** | Treasury: covenant holder selv ved 470, men headroom blir «merkbart lavere» i Q1/Q2 hvis gevinstuttaket skyves. Banken vil spørre om styregodkjent rebaseline og leverandørkravet. Å møte banken og styret med 395 etter at 472 er kontrollert er en tillits- og ansvarsrisiko for konsernledelsen. | EM-181, EM-183 |

**Konklusjon:** Å fortsette uendret «ser ut til å ha høyest gjennomføringsrisiko» (CFO) [EM-195]. Ingen av de tre alternativene (fortsette, full stopp, kontrollert reset) er kostnadsfrie. Det eneste som er sikkert er at status quo ikke er stabilt.

---

## Åpne punkter og kildekonflikter å rydde før tallene brukes

1. Er leverandørkreditten allerede i 395? Brosummen (41+22+19+29=111) gir 506 brutto og ikke 472 netto.
2. Hvorfor 382 i Silje Trans e-poster (juni) men 395 i styrepakken [EM-166, EM-167]?
3. Verktøyforsinkelsen: «fem uker» (6. mai) mot ankomst 13. juni [EM-055, EM-056].
4. Kundenavn på de fem fornyelsene: OPS-004 mot e-posttråd TH-022.
5. Linjekost: 8,7 mill. (14. aug.) mot 11,2 mill. (OPS-002) er sannsynligvis tidsforskjell.
6. Hvem er CIO? Rolf Nygaard (mars, OF-013) mot Amina Rahman (HR-001, sept.), sannsynligvis personskifte.
7. Backfill står som åpen (56 dager) i OF-011, men ble godkjent 6. sept. (maks 1,8 mill., fire uker).
8. Datoer: oppgaven sier styremøte «i morgen» (18. sept.), Karin Eides e-post 14. sept. sier «torsdag» (17. sept.).
9. Risikovedlegget til styrepakke 26. aug. er ikke i korpuset, så vi vet ikke hvor detaljert styret ble varslet.
10. Ingen NPV er regnet om med 472/128. Illustrasjonen over er ikke en NPV.

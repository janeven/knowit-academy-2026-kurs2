# H5 – Kjernen/løsningen er ikke levedyktig i dagens form

**Eier:** Person A  ·  **Dato:** 2026-10-22  ·  **Status:** FERDIG – SVEKKET
**Dom:** **SVEKKET**: klart mer imot enn for, men *ikke endelig avvist* fordi (a) ingen uavhengig teknisk verifikasjon finnes i korpuset og (b) fire danske kontraktspunkter er fortsatt uavklarte.

*Hypotesen er definert i [`../02-hypoteser.md`](../02-hypoteser.md) (avsnitt H5). Sikkerhet: **fakta** = primærdata eller uavhengige kilder som er enige; **sannsynlig** = én god kilde; **antakelse** = ukontrollert eller min egen modell.*

## 1. Testbare påstander

| # | Påstand (fra «Hva må være sant?») | Test (kilde + beregning) | Utfall | Sikkerhet |
|---|---|---|---|---|
| 1 | Plattformkjernen (Nexus, CRM/kontrakt, ERP-fakturering, identitet, portal) har strukturelle feil som ikke kan rettes uten ny arkitektur | **46 av 64** kritiske integrasjoner er produksjonsklare (72 %). De 18 uferdige: bare **5–6 (8–9 % av 64)** er kode/konfigurasjonsfeil, resten venter på beslutning, krav, testdata eller endring [TECH-005, VEN-002, EM-104]. Konkrete feil er rettet raskt: hendelseskø i build 6.4 (EM-101), tre portalfeil fra cache/synk (EM-092), Vestbygg-caching lukket (EM-232/233). CIO: «ikke et totalhavari; bygg har gått foran stabile prosesser, data og scope» (TECH-002). Plattformleder: «levedyktig … å bytte plattform nå vil ikke reparere data eller beslutningsflyt» (EM-185). Test: bekrefter tallene (EM-190). **Motpunkter:** miljøstabilitet 76 % og 43 alvorlighetsgrad 1–2-feil i mars (EM-016); migreringsverktøyet feilet på nordisk fakturavariant og volumkjøring (EM-056); regresjonskapasitet lav fordi testmiljø 3 ikke er finansiert (OF-011, åpen 31 dager) | **Motbeviser** (men svakt bevismateriale) | **Sannsynlig.** Tallene er primærdata (A), men *alle* vurderingene av «levedyktig» kommer fra programmets egne folk og CIO (som anbefaler et reset, og dokumentet er et utkast). **Ingen uavhengig revisjon** |
| 2 | Lokale kontraktskrav (indeks, servicekreditt, fakturamottaker) lar seg ikke modellere i én felles struktur innen akseptabel tid | Bare **4** punkter er dokumentert som reelle kontraktskrav: indeksvarsling, servicevindu, separat fakturamottaker, oppsigelse [EM-122, EM-124]. For øvrige ønsker (portal, segmentmodell, godkjenningsgrenser) **foreligger design som møter dokumenterte behov** (EM-126); Danmark kan akseptere felles portal/segmentmodell hvis dispatch beholdes lokalt (EM-125). Leverandøren sier prisindeks krever «én regel per kontraktsfamilie», altså gjennomførbart når Danmark/Sverige-eksempler leveres (EM-101). **Men:** de 4 kontraktspunktene står «åpne til endelig fagbekreftelse» (EM-126) og «må løses før migrering» (EM-125). Prisindeks og servicekreditt mangler entydig struktur for flere danske avtaler (TECH-004) | **Motbeviser delvis** / uavklart for de 4 punktene | **Sannsynlig.** Ingen kilde sier at kravene *ikke kan* modelleres. Ingen kilde har heller vist at de *kan* (mangler dansk testdata) |
| 3 | Piloten viste systematisk svikt og ikke bare teknisk lærekost | Pilot 42 kunder: **ingen systematisk totalhavari**, kritiske tjenester opprettholdt manuelt (OPS-003). Men: **17 av 42 (40 %)** trengte manuell fakturakontroll, **8 av 42 (19 %)** har portal-/ordreavvik, fakturakorreksjon **7,8 %** (mot 2,0 % i januar og 4,9 % i hele porteføljen i august). Årsaker: uklart fakturamottakerfelt, pris-/servicekredittregler, identitetsmapping, uferdige integrasjoner. Teknisk rettet: portalcache (tre feil), to ordreavvik fra prisbok-integrasjon; «resten må spores mot masterdata» (EM-092). Kontraktsdata: av 61 pilotavtaler har 13 tom basisdato/avvikende indekskode/manglende SLA-regel (EM-162); av 18 migrerte avtaler hadde 6 prisindeks uten basisdato og 2 manglet servicekredittabell (EM-161) | **Motbeviser delvis** | **Sannsynlig.** Utvalget er lite og ikke representativt (EM-084). Hva som er *migrasjonsfeil* og hva som er *kildedata* er ikke skilt |
| 4 | Kostnad for å fullføre overstiger verdien (gevinst 128 mill.) | **Egen forward-looking beregning (antakelse):** gjenstående kost 154 mill. (91 forpliktet + 63 uforpliktet [FIN-005/007]), nåverdi ≈ **149** (9 %, midt ~5 mnd frem). Gevinst 128 mill./år fra 2029 (korrigert, FIN-006): nåverdi over 3 år = **279**, over 5 år = **428**. **Break-even årlig gevinst** = **68** (3 år) / **44** (5 år), altså 53 % / 35 % av 128. Stresstester: høy kost (494, gjenstår 176) gir break-even 78 / 51; uten kreditt (506, gjenstår 188) gir 83 / 54 | **Motbeviser** (under forutsetningene) | **Antakelse.** Min enkle modell. *Ikke* en NPV fra Finance. Se forbehold under |

**Forbehold til #4:** (i) sunk cost (318 mill.) er med vilje utelatt, siden spørsmålet er om det lønner seg å *fullføre*; (ii) 128 er allerede nedjustert −39 % fra 210 (FIN-006), og 42 mill. av nedjusteringen er «optimistiske antakelser», så ytterligere nedside er mulig; (iii) linjekost (11,2 mill. hittil i 2026, OPS-002), forsinkelse av gevinst utover 2029 og kostnaden av *ikke* å fullføre (dobbeltlandskap, avvikling, «minst to år», EM-195) er ikke modellert; (iv) benefits antas flate fra 2029 uten ramp-up. Konklusjon: marginen er stor nok til at feilene i modellen neppe snur retningen, men gruppen **bør be Silje Tran regne en ekte NPV** på 472 / 128 (CFO har allerede bedt om sensitivitet på 128, EM-179).

## 2. Falsifiseringsforsøk

- **Forsøk 1: finnes noen kilde som sier at kjernen er ubrukelig?** Nei. Jeg søkte korpuset (dokumenter og alle e-poster) etter vurderinger av arkitektur/plattform: CIO, plattformleder, testleder og styringsgruppen er enige om at kjernen er levedyktig. Eneste «negative» tekniske signaler er kvalitetspunkter (feilantall, miljøstabilitet, volumkjøring), ikke strukturelle.
- **Forsøk 2: er «forsinkede beslutninger» egentlig et *designproblem* (løsningen er for vanskelig å bestemme), og dermed H5 i forkledning?** Delvis støtte: to av fire langvarige prosessaker ble *sendt tilbake* fordi underlaget manglet operativ konsekvens (EM-117), og driftsdirektøren ber programmet «slutte å sende uferdige alternativer til linjen» (EM-031). Prosesseier for arbeidsordre avviste standardprosessen fordi piloten ga **11 minutter mer administrasjon per oppdrag** (EM-113); den ble løst med pilotunntak (EM-118). Dette er *fit-risiko* i standardmodellen, men i hovedsak vurdert som et styrings-/kvalitetsproblem, ikke at modellen er umulig. Merk at samme saker også viser uklar beslutningsrett (EM-117), så de kan ikke entydig tilskrives H5 *eller* H3.
- **Forsøk 3: er pilotens 40 %-andel manuell kontroll et tegn på arkitekturfeil?** Mesteparten av årsakene er data/regler (OPS-003, EM-092), ikke plattformfeil, og datakvalitetsrapporten sier at «generell datarensing alene løser ikke uklare forretningsregler» (TECH-004). Dette er *ikke* teknologi i snever forstand, men det betyr at en rask teknisk «fiks» uansett ikke løser det.
- **Forsøk 4: er stopp et realistisk alternativ?** CFO: full stopp utløser avvikling, kontraktskost og minst to år med dobbelt systemlandskap, og «det kan være riktig hvis kjernen er ubrukelig, men Aminas review sier det motsatte» (EM-195). Fortsette uendret har samtidig høyest gjennomføringsrisiko. Altså: alternativet til å fortsette på en *redusert* kjerne er ikke billig.

## 3. «Hva ville fått oss til å endre mening?»

| Observasjon som ville endret mening | Funnet? |
|---|---|
| (a) Uavhengig teknisk revisjon som finner arkitekturfeil i Nexus/ERP-kjernen | **Nei, ingen slik revisjon i korpuset.** CIO-reviewen er et utkast fra en part med en anbefaling (TECH-002). *Dette er svakheten som holder dommen på SVEKKET og ikke FALSIFISERT.* |
| (b) NPV på 472/128 som er klart negativ også for en redusert kjerne | **Nei.** Min grovmodell gir positiv margin (break-even 44–83 mill./år mot 128). Finance har ikke regnet NPV. |
| (c) De fire danske kontraktspunktene lar seg ikke modellere uten egen løsning | **Ikke avgjørbar.** Står åpne til endelig fagbekreftelse (EM-126). Ingen kilde sier de er umulige. |
| (d) Pilot som feiler systematisk også etter at data/regler er utbedret | **Ikke testbar ennå.** Data er ikke utbedret (14/27 objekter, 13 av 61 pilotavtaler med hull). |

## 4. Alternative forklaringer testet

- **H3 (styring):** forklarer hvorfor bygg gikk foran stabile krav: 47 endringer uten uttak (EM-043), 14 av 23 prosesser ikke godkjent (OF-010), beslutningskø median 35,5 dager (OF-011).
- **Data/forretningsregler:** forklarer mesteparten av pilotavvikene (OPS-003, TECH-004). Ikke en plattformfeil, men en forutsetning plattformen trenger.
- **H2 (leverandør):** forklarer 5–6 av 18 integrasjoner, men ikke at *kjernen* skulle være feil. Se [H2-funn.md](H2-funn.md).
- **Nordflows egen kompleksitet** (3 ERP, 4 CRM, 3 portaler, >70 punktintegrasjoner [TECH-001]) forklarer *hvorfor* transformasjonen er vanskelig, men dokumentet vurderer eksplisitt ikke programstyring eller leverandørprestasjon, så det er ikke bevis for at målarkitekturen er feil.

## 5. Dom og begrunnelse

**SVEKKET.** Tre av fire «må være sant»-punkter er motbevist eller svekket: bare 5–6 av 64 integrasjoner har kode-/konfigurasjonsfeil (46 er klare), ingen kilde hevder at kjernen er strukturelt ubrukelig, piloten ga ingen systematisk svikt, og min forward-looking beregning viser at fullføring lønner seg selv om gevinsten halveres. *Hvorfor ikke FALSIFISERT:* alle «levedyktig»-vurderinger kommer fra programmets egne folk og CIO (med reset-anbefaling), uavhengig verifikasjon mangler, og de fire danske kontraktspunktene er ikke bevist modellerbare. H5 bør derfor ikke løftes som rotårsak, men **«kjernen er levedyktig» bør stå som en arbeidsantakelse i anbefalingen**, med en 2–3 ukers uavhengig teknisk verifikasjon som del av resetet (jf. `02-hypoteser.md`, «Test først»).

## 6. Kilder brukt

| Kilde-ID | Type (A–D) | Hva den viser | Merknad (kvalitet, versjon, konflikt) |
|---|---|---|---|
| TECH-005 | A | 46/64 klare; 5/6/4/3 for 18 uferdige | Nordflows telling 9.9. Plattformleders egen telling avviker lite (6/5/4/3) |
| TECH-002 | C | CIO: kjernen levedyktig, 30.6.2027, 4-ukers reset | **Utkast**, anbefaler reset, ikke uavhengig |
| TECH-001 | A | As-is: 3 ERP, 4 CRM, 3 portaler, >70 integrasjoner | Sier selv at det ikke vurderer styring/leverandør |
| TECH-004 | A | Data: 14/27, 11,7 % duplikater, 8,4 % fakturamottaker; DK-regler uten struktur | Skiller regler fra rensing |
| OPS-003 | A | Pilot: 17/42 manuell, 8/42 avvik, 7,8 %, ingen systematisk havari | Lite og ikke representativt utvalg |
| OF-011 / OF-010 / OF-012 | A | Beslutningskø, rød RAID, avhengighetskjede, minimumskjerne | Avhengighetskart sier minimumskjerne kan fases uten å forkaste kjernen |
| FIN-005, FIN-007, FIN-006, FIN-001 | A | Kost 506/472, påløpt 318, gjenstår 154, gevinst 210→128 | Brutto/netto-bro uavklart (se `01-situasjonsbilde.md` §Åpne punkter) |
| OPS-002 | A | Linjekost 11,2 mill. | Utenfor programprognosen, utenfor min modell |
| EM-185, EM-186, EM-189, EM-190, EM-196 | D | Plattformleder, data, CIO og test: kjernen levedyktig | Interne parter |
| EM-122–126 | D | Fire reelle danske kontraktspunkter; design møter øvrige behov | Fagbekreftelse står åpen |
| EM-101, EM-092, EM-232/233 | D | Tekniske feil rettet raskt; prisindeks krever regel per familie | Leverandør- og programkilder |
| EM-161, EM-162 | D | Migrerte avtaler med manglende indeks-/SLA-felt | Ikke skilt mellom migrasjonsfeil og kildedata |
| EM-113, EM-117/118, EM-031, EM-016 | D | Fit-risiko (11 min), tilbakesendte beslutninger, miljøstabilitet 76 % | Enkeltuttalelser |
| EM-195 | D | CFO: full stopp = avvikling + ≥2 års dobbeltlandskap | Ikke tallfestet |

*Støy ikke brukt:* TH-032–040, OTHER-001 (Aurora).

## 7. Åpne spørsmål / hva som mangler

1. **Uavhengig teknisk verifikasjon** av Nexus/ERP-kjernen (2–3 uker). Må skaffes utenfor korpuset (ekstern arkitekt). Ansvarlig: **Amina Rahman** kan bestille.
2. **Ekte NPV** på 472 (455–494) og 128/år, og for en *redusert kjerne*. Ansvarlig: **Silje Tran / Thomas Vik**.
3. **De fire danske kontraktspunktene:** endelig fagbekreftelse og om de kan modelleres. Ansvarlig: **Beate Høyer, Mikkel Sørensen, Nora Steen**.
4. **Migrasjonsfeil vs kildedata** på de 13 av 61 pilotavtalene: hvor mange er feil i verktøyet (leverandør) og hvor mange var allerede feil i Cobalt? Ansvarlig: **Sander Lie / Mari Heggen**.
5. **Miljøstabilitet og feiltall i dag** (mars: 76 %, 43 sev 1–2; kun én gammel måling i korpuset). Ansvarlig: **Kjetil Børge**.

## 8. Til fellesmøtet *(fylles kun ut hvis dom er STØTTET eller STERKT STØTTET)*

*Ikke aktuelt: dommen er SVEKKET.* Funn som bør deles på tvers:

- **Til anbefalingen:** Bruk «kjernen er levedyktig» som arbeidsantakelse, men merk den eksplisitt som *ikke uavhengig verifisert*. Legg inn verifikasjon i 90-dagersplanen.
- **Til felles tall:** forward-looking break-even (44–83 mill./år) som *argument* for å fullføre, men merk den som egen grovmodell inntil Finance har regnet NPV.
- **Til H3/H4-eierne:** pilotens avvik og de langvarige prosessbeslutningene er i stor grad *regel- og eierproblemer* (data, kontraktsmodell), ikke teknologi. Det støtter at et teknisk reset alene ikke er nok (CIO sier det selv, TECH-002).

## 9. AI-bruk *(del av leveransen «AI-arbeidslogg»)*

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Selv kontrollert mot original |
|---|---|---|---|
| Lese hele korpuset og bygge hypoteser (tidligere økt); søke korpuset etter arkitektur-/plattformvurderinger | Kildehenvisninger og tall som *utgangspunkt* | — | Tallene i tabellene er re-verifisert mot originalfilene (MD/CSV/PDF) i denne økten |
| Bygge enkel forward-looking verdiberegning (diskontering 9 %, 3 og 5 års horisont) | Beregningen som illustrasjon | Merket som *antakelse*, ikke NPV; la til forbehold om sunk cost, linjekost og ramp-up | Regnestykket er enkelt (nåverdi av 128 over 3/5 år; break-even = nåverdi kost / annuitetsfaktor) og bør kjøres på nytt i regneark av teammedlem |
| Dom og begrunnelse | Utkast fra AI | Valgte SVEKKET fremfor FALSIFISERT fordi uavhengig verifikasjon mangler | Dommen bør vurderes av teammedlem før den står i fellesoversikten |

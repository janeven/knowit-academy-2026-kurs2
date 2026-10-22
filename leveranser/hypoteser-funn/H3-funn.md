# H3 – Styring og beslutningsrett er hovedårsaken

**Eier:** Person B  ·  **Dato:** 2026-10-22  ·  **Status:** LØFTES
**Dom:** STØTTET (men mekanismen må presiseres, se §2 og §5)

*Hypotesen er definert i [`../02-hypoteser.md`](../02-hypoteser.md) (avsnitt H3). Ikke endre den der. Skriv funn her.*

## 1. Testbare påstander

| # | Påstand (fra «Hva må være sant?») | Test (kilde + beregning) | Utfall | Sikkerhet |
|---|---|---|---|---|
| 1 | Ventetid på Nordflow-beslutninger ligger på kritisk sti | OF-011 «Effekt» per sak; OF-012 kritisk kjede starter med dataeier og prosessbeslutning; TECH-005: (6 beslutning/krav + 4 testdata) / 18 = **10/18 = 56 %** uferdige integrasjoner er kundeskapt. VEN-002 har samme 10/18. | Støtter | **Fakta** (A + uavhengig part C som stemmer) |
| 2 | Lang beslutningstid er systematisk, ikke enkeltsaker | OF-011, 12 saker. Sortert: 29, 30, 31, 32, 33, 35, 36, 37, 40, 44, 49, 56 → median (35+36)/2 = **35,5** (bekreftet). Snitt 452/12 = 37,7. Alle 12 > mål 7 (min 29). 6 av 12 åpne per ca. 12.9, altså høyresensurert, så den reelle medianen er høyere. Lukkede alene: median 38,5. | Støtter | **Fakta** for loggen. Men loggen er et utvalg, se §2. |
| 3 | Lang tid skyldes uklar beslutningsrett, ikke tung sak | (a) Grupperer de 12 etter om OF-001 gir klar eier. *Rett uklar* (prosesseier/program/land): kontraktsmodell, prisindeks, eier ordre-til-faktura, scope-frys, dataeier, servicekreditt → median **35**. *Rett formelt klar* (SG eier scope, økonomi og port): avansert planlegging, pilot-exit, backfill, portal, testmiljø, kredittmyndighet → median **35,5**. (b) EM-117: av fire prosesser venter 2 på beslutningsrett, 2 er sendt tilbake for manglende operativ konsekvens. | **Delvis motbevist** | Gruppering = *antakelse* (min klassifisering). EM-117 = sannsynlig. |
| 4 | Data- og testgap skyldes manglende eier og regler, ikke teknisk evne | TECH-004 (A): «navngi dataeier … rensing alene løser ikke uklare regler». Dataeier kontraktsmaster åpen ≥32 d (OF-011). Dansk testuttrekk forsinket fordi kontraktsfamiliene ikke var klassifisert (EM-107). 14 av 73 scenarioer mangler forventet resultat, og eier må være forretningen (EM-110). Men: «med dagens rensekapasitet» (EM-088), og data har 21 FTE gap (HR-002). | Støtter, delt med H4 | **Sannsynlig** |
| 5 | Når beslutningsretten avklares, kommer fremdrift | Kontraktsmodell besluttet 2.6; uferdige integrasjoner 21 (jun.) → 19 (aug.) → 18 (sep.) [EM-104, TECH-005], altså svak bedring. Arbeidsordre avklart etter eskalering 1.8 (EM-029, EM-118). Scope-frys delvis besluttet 10.9 (OF-014), for nytt til å måle. | Uavklart | **Ikke avgjørbar fra korpuset** |

## 2. Falsifiseringsforsøk

- **«Beslutningene ligger ikke på kritisk sti»:** Feilet. Hver sak i OF-011 har en konkret blokkerende effekt, og OF-012 plasserer dataeier og prosessbeslutning først i kjeden.
- **«Saker med klar beslutningsrett tok også lang tid»:** **Lyktes delvis.** Saker der styringsgruppen etter mandatet klart eier beslutningen (finansiering, scope, port) har samme median (35,5) som saker med uklar rett (35). Backfill er det tydeligste eksempelet. Den sto som risiko R-029 fra 11.4 med frist 6.5 (OF-009), og ble godkjent først 6.9 (EM-140). 11.4 → 6.9 = 19+31+30+31+31+6 = **148 dager**, selv om eieren (SG/CFO) var klar. Mekanismen er derfor bredere enn «uklar rett». Styringsgruppen avgjør ikke saker den eier. Dette er fortsatt styringssvikt, men tiltaket må være beslutningsdisiplin og frister, ikke bare en RACI.
- **«Underlaget er dårlig, ikke retten uklar»:** Delvis støttet. 2 av 4 prosessaker ble sendt tilbake for manglende operativ konsekvens (EM-117), og COO ber om ferdige alternativer (EM-031). Det trekker mot kvalitet og kapasitet i saksforberedelsen (H4).
- **«Forsinkelsen startet før styringsproblemet»:** Feilet. Den tidligste svikten er selv en styringsbeslutning. Programmet ble startet med prosesseiere «ikke startet», profilering 22 %, mobilisering på 3 av 6 uker og linjekapasitet «ikke endelig verifisert» (OF-001, OF-002, BOARD-001), mot styrets uttrykkelige portkrav (BOARD-002).
- **Scope:** 28 → 47 endringer, 19 analysert, 63 400 t / 38 mill., ingen uttak (EM-040, EM-043, EM-046). Bare fire danske punkter har kontraktsgrunnlag (EM-124). Dette støtter H3.

## 3. «Hva ville fått oss til å endre mening?»

- **Kritisk-sti-sensitivitet (hva om beslutningene tok 7 dager):** Søkte i OF-, TECH- og PMO-tråder. **Ikke funnet.** Ingen kritisk-sti-analyse finnes i korpuset. EM-189 sier at februar er utilrådelig «selv ved full leverandørbemanning». Det utelukker leverandørkapasitet, men ikke beslutninger eller intern kapasitet.
- **Gjenåpning skyldes kvalitet i underlaget, ikke manglende rett:** **Delvis funnet** (EM-117: 2 av 4; EM-031).

## 4. Alternative forklaringer testet

- **Leverandør (H2):** 5/18 integrasjoner (28 %). Verktøyet var 5 uker forsinket ifølge Convergent, men ankom 13.6 (EM-056). 31.3 → 13.6 = 74 dager ≈ **10,6 uker** frem til ankomst. Det er reelt, men forklarer ikke at prosess (14 uker) og data (20 uker) ligger bak.
- **Kapasitet (H4):** Sterk, men ikke uavhengig av H3. Konflikten består fordi ingen har tatt prioriteringsbeslutningen (HR-001: «ingen automatisk prioritet»; EM-129 mars, EM-133, EM-145). Se H4-funn.
- **Datakvalitet som eget teknisk problem:** Dubletter på 11,7–12,4 % er reelle, men TECH-004 og EM-071 knytter løsningen til regler og eierskap.

## 5. Dom og begrunnelse

**STØTTET.** Fire uavhengige kildetyper peker samme vei: mandatet mangler konfliktløsning (OF-001), loggen viser systematisk treghet (OF-011), styret krevde porter som ikke ble håndhevet (BOARD-002, OF-002), og både CIO og leverandøren peker på beslutninger og data (TECH-002, VEN-002). Hypotesen er ikke STERKT STØTTET, av tre grunner: (1) kritisk-sti-effekten er ikke tallfestet; (2) «uklar beslutningsrett» som mekanisme er for smal, siden saker med klar eier tar like lang tid; (3) beslutningsloggen er et utvalg.

## 6. Kilder brukt

| Kilde-ID | Type | Hva den viser | Merknad |
|---|---|---|---|
| OF-001 | A | Konfliktløsning mangler; mål 7 dager; porter før bygg; oppstart etter 3 av 6 uker | |
| OF-002 | A | Prosesseiere «ikke startet», profilering 22 % ved godkjenning | |
| OF-011 | A | 12 saker, median 35,5, 6 åpne | **Tittel 2025–2026, men alle sakene er reist fra april 2026.** EM-025 nevner 17 åpne i mai, så loggen er et utvalg. Backfill står åpen, men ble godkjent 6.9 (EM-140). Kontraktsmodell reist 19.4 i loggen, men 9.5 i EM-027. |
| OF-009 / OF-010 | A | R-029 backfill fra 11.4; R-031 uten eier i april; R-044 beslutningskø rød | |
| OF-012 | A | Kritisk kjede: dataeier → prosessbeslutning → integrasjon → test → kunde | |
| OF-013 | A | Recovery forutsatte 7 dager, stabile krav, linjekapasitet og leverandørrecovery; revurdering ved brudd | OF-003 (md) lister bare to forutsetninger. OF-013 er beslutningsreferatet og gjelder. |
| OF-014 | A | Beslutningsrett for scope er fortsatt uavklart 10.9; frist 22.9 | |
| BOARD-001 / BOARD-002 | A | Porter krevd; linjekapasitet og kontraktsvarianter ikke verifisert ved vedtak | |
| TECH-002 | C | CIO: bygg foran prosess, data og scope; krever 72 t beslutningsfrist | Utkast fra part med anbefaling |
| TECH-004 / TECH-005 | A | Dataeier mangler; 10/18 kundeskapte integrasjoner | |
| VEN-002 | C | Beslutninger 4–9 uker sene; 10/18 kundeskapte | Forhandlingsposisjon, men stemmer med TECH-005 |
| EM-025–031, EM-035, EM-040–046, EM-112–118, EM-107, EM-110, EM-140 | D | Uenighet om hvem som beslutter; underlagskvalitet; scope | EM-116 nevner fire prosesser som ikke kan gjenfinnes ved navn i OF-011 |

## 7. Åpne spørsmål / hva som mangler

- **Kritisk-sti-analyse** med scenario «beslutninger på 7 dager»: Julie Nystad (PMO) og Lars Pettersen.
- **Komplett beslutningslogg 2025–2026**, ikke bare de 12 kritiske: PMO.
- **Hvorfor styringsgruppen ikke avgjorde saker den eier** (backfill på 148 dager): Thomas Vik. Er årsaken manglende underlag, manglende mandat eller manglende budsjett?

## 8. Til fellesmøtet

- **Kjerneargument:** Programmet ble startet i strid med egne og styrets portkrav, og har siden kjørt uten en mekanisme som tvinger frem beslutninger. Alle 12 kritiske saker brukte over fire ganger målet. De blokkerer direkte 10 av 18 integrasjoner og hele data- og testkjeden. Kapasitetskonflikten (H4) består fordi ingen tar prioriteringsbeslutningen.
- **De to sterkeste motargumentene:** (1) Saker med klar eier tok like lang tid, så det er beslutnings*disiplin* i styringsgruppen, ikke bare uklar *rett*. (2) Halvparten av prosessakene ble sendt tilbake for svakt underlag, noe som trekker mot kapasitet (H4).
- **Bør undersøkes videre:** kritisk-sti-sensitivitet; komplett logg; hvorfor recovery-forutsetningene ble brutt uten revurdering (OF-013 pkt. 5).
- **Konsekvens for anbefalingen:** Reset må være et *konsernreset*. Det betyr navngitt beslutningstaker per sakstype og en frist (72 t) med automatisk eskalering til CEO. Krav til hva et beslutningsunderlag skal inneholde (operativ konsekvens), håndhevede porter og scope-frys med unntaksprosess. Prioriteringsregelen mellom linje og program må besluttes av CEO, ikke forhandles.
- **Rolle i totalbildet:** **Rotårsak.** H4 er forsterker (se H4-funn), H2 er medvirkende.

## 9. AI-bruk *(del av leveransen «AI-arbeidslogg»)*

| Oppgave delegert til AI | Brukt uendret | Endret / forkastet | Selv kontrollert mot original |
|---|---|---|---|
| Lese OF-001/002/003/009–014, BOARD-001/002, TECH-002/004/005, VEN-001/002 og tråd TH-003–008, 011, 013, 016–018, 029–030 i sin helhet | Sitater og tall | Forkastet 02-hypotesers formulering om at «to ventet på beslutningsrett» som hele bildet. EM-117 sier 2 av 4. | _Person B fyller ut: hvilke kilder du selv har åpnet_ |
| Regne median, snitt, 10/18 og 148 dager | Ja | – | _Kontroller regnestykkene_ |
| Gruppere de 12 sakene etter klar/uklar beslutningsrett | Nei, merket som antakelse | Klassifiseringen er en vurdering og bør sjekkes | _Bør gjennomgås av teamet_ |
| Finne kildekonflikter (logg mot e-post) | Ja | – | _Kontroller OF-011 mot EM-027/140_ |

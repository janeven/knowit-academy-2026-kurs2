# Prompt: test hypotesene om OneFlow (del med hele teamet)

Denne filen er en delt arbeidsinstruks. Hver teammedlem kjører den med sin egen Claude-økt, mot sine egne hypoteser, og skriver funn i sine egne filer. Slik kan vi jobbe parallelt uten å tråkke på hverandre.

## Fordeling (endre navnene i `hypoteser-funn/00-oversikt.md`)

| Person | Hypoteser | Hvorfor denne paringen |
|---|---|---|
| Person A | **H2** (leverandør) + **H5** (kjernen/løsningen) | Samme kilder: VEN-*, TECH-*, TH-009/010/015/016/029 |
| Person B | **H3** (styring/beslutningsrett) + **H4** (kapasitet) | Samme kilder: OF-001/011/014, HR-*, TH-005–008/017/019–021 |
| Person C | **H1** (gul og håndterbar) + **H6** (kunde/inntekt) | Samme kilder: FIN-*, OPS-*, BOARD-*, TH-002/022–028 |

Du kan bytte, men sørg for at alle seks er dekket og at ingen har dem alle.

## Slik starter du

Vi jobber kun på `main`, uten egne grener. Klone repoet (eller `git pull origin main` hvis du allerede har det), åpne det i Claude Code og lim inn teksten under, med riktig hypotesenummer. Hvis Windows klager på for lange filstier ved kloning, bruk `git clone -c core.longpaths=true <url>`.

---

### PROMPT (kopier fra her)

Jeg er med i et Knowit-team på tre som gir råd til Nordflows CEO om OneFlow-programmet. Vi har et situasjonsbilde (`leveranser/01-situasjonsbilde.md`) og seks konkurrerende hypoteser (`leveranser/02-hypoteser.md`). Vi fordeler hypotesene mellom oss og tester dem uavhengig. **Mine hypoteser er: `<H?>` og `<H?>`.**

**Arbeidsgrunnlag.** Les først `leveranser/01-situasjonsbilde.md` (spesielt «Åpne punkter og kildekonflikter») og `leveranser/02-hypoteser.md` (korpuskartet, og avsnittene for mine hypoteser). Kildene ligger i `oppgave/CaseCorpus/` (dokumenter per mappe, e-post i `E-post/TH-xxx/`). Oppgaven er beskrevet i `oppgave/Nordflow-oppgave.md`. Les kildene selv; ikke stol på vår egen oppsummering uten å kontrollere den mot originalen.

**Din rolle.** Du er en skeptisk analytiker, ikke en advokat for hypotesen. For hver hypotese skal du først forsøke å **falsifisere** den, deretter lete etter det som støtter den. Bekreftelsesskjevhet er hovedrisikoen her.

**For hver av mine hypoteser:**

1. **Formuler testbare påstander.** Ta utgangspunkt i «Hva må være sant?» i `02-hypoteser.md`, og gjør hver påstand om til noe som kan sjekkes mot kilder eller tall (f.eks. «≥50 % av de 18 uferdige integrasjonene er leverandørskapt»).
2. **Kjør testene.** Les de oppgitte kildene i sin helhet, regn selv på tallene (vis regnestykket), og sjekk datoer og versjoner. Bruk primærdata (A) foran statusrapporter (B), parts-posisjoner (C) og enkeltuttalelser (D). Se kildehierarkiet i `02-hypoteser.md`. Test også alternative forklaringer, ikke bare den du er satt til å undersøke.
3. **Test «hva ville fått oss til å endre mening?»** aktivt: søk i korpuset etter nettopp den observasjonen. Skriv ned om du fant den eller ikke.
4. **Skill fakta fra antakelser.** Merk hver konklusjon som *fakta* (to uavhengige kilder eller primærdata), *sannsynlig* (én god kilde) eller *antakelse/ukontrollert*. Merk kildekonflikter og versjonsforskjeller, og si hva som må avklares for å løse dem.
5. **Ignorer støy.** TH-032–040, OTHER-001 (Aurora), `__MACOSX`, `.DS_Store` og `CaseCorpus.zip` er ikke bevis, med mindre du kan vise at de berører OneFlow.
6. **Ikke finn opp.** Hvis kildene ikke kan avgjøre noe, skriv «ikke avgjørbar fra korpuset», og angi hvilken informasjon (og hvem) som trengs. Ikke fyll hull med antakelser som om de var funn.

**Dom per hypotese** (velg én, og begrunn kort):

| Dom | Betydning |
|---|---|
| **FALSIFISERT** | Minst ett sentralt «må være sant» er motbevist av primærdata/uavhengige kilder. |
| **SVEKKET** | Mer imot enn for, men ikke endelig avvist. |
| **USIKKER** | Kildene kan ikke avgjøre. Oppgi hva som mangler. |
| **STØTTET** | Flere uavhengige kilder støtter, og falsifiseringsforsøkene feilet. |
| **STERKT STØTTET** | Som støttet, og i tillegg tåler den de sterkeste motargumentene vi fant. |

**Skriv funnene** i `leveranser/hypoteser-funn/H<n>-funn.md` (én fil per hypotese, malen ligger der). Rediger *kun* dine egne funnfiler, og ikke `01-situasjonsbilde.md`, `02-hypoteser.md` eller andres filer. Hold hver fil til ca. én side pluss kildetabell.

**Hva skjer videre med dommen:**
- **FALSIFISERT/SVEKKET:** Noter funnet i filen (hvorfor, med kilder), sett status i `leveranser/hypoteser-funn/00-oversikt.md`, og gå videre. Ikke bruk mer tid.
- **USIKKER:** Skriv hva som må til for å avgjøre (kilde, person, beregning), og sett status. Vi tar det i fellesmøtet.
- **STØTTET/STERKT STØTTET:** **Løft til gruppen.** Sett status «LØFTES» i oversikten, og fyll ut seksjonen «Til fellesmøtet» i funnfilen (kjerneargument i 3–5 linjer, de to sterkeste motargumentene, hva som bør undersøkes videre, og hva det betyr for anbefalingen). Ikke gå videre til tiltak før gruppen har sett det.

**Til slutt:**
- Fyll ut «AI-bruk» nederst i hver funnfil: hva du delegerte til AI, hva du brukte uendret, hva du endret eller forkastet, og hva du selv kontrollerte mot originalkilden. Dette er en del av leveransen («AI-arbeidslogg»).
- Gi en kort oppsummering i chatten: dom per hypotese, de tre viktigste bevisene, og hva du er mest usikker på.
- Commit kun dine egne filer og push til `main`. Kjør `git pull --rebase origin main` rett før du pusher, og rediger bare *din rad* i oversikten og dine egne funnfiler, så unngår vi konflikter. Commit og push gjerne ofte (f.eks. etter hver hypotese).

### SLUTT PÅ PROMPT

---

## Fellesmøtet (etter parallell runde)

Når alle tre er ferdige, samles vi og går gjennom `hypoteser-funn/00-oversikt.md`.

1. Hver person presenterer dommer på 2 minutter per hypotese, og starter med det som falsifiserte *egne* antakelser.
2. Vi sammenligner de løftede hypotesene. De er sannsynligvis ikke gjensidig utelukkende (H3 og H4 kan begge være sanne). Vi avklarer **hvilken som er rotårsak, hvilken som er forsterker, og hvilken som er symptom**.
3. Vi avgjør hva som skal undersøkes videre, og hvem som tar det.
4. Vi oppdaterer felles tall (én sannhetskilde) før noe går inn i CEO-brief, lederpresentasjon, 90-dagersplan og evidenslogg. **Alle leveranser skal bruke samme tall.**
5. Vi løser kildekonfliktene som ble funnet (liste i `01-situasjonsbilde.md`), og logger dem i evidensloggen.

## Felles spilleregler

- **Kilde-ID på alt** (f.eks. `[TECH-005]`, `[EM-104]`). Påstander uten kilde regnes ikke som funn.
- **Beregninger vises** (inndata, formel, resultat). Ingen «ca.» uten forklaring.
- **Navngi usikkerhet.** Bruk «fakta / sannsynlig / antakelse».
- **Ingen skyld uten bevis.** Vi beskriver hva dokumentene viser, ikke hva noen ment. Dette er et råd til CEO, ikke en granskning.
- **Ikke bland kategorier**: programkost ≠ linjekost ≠ arbeidskapital ≠ resultatrisiko. Se `01-situasjonsbilde.md` §1.2 og §1.5.
- **Spør om du står fast.** Dersom en kilde mangler (f.eks. risikovedlegget til styrepakken 26. aug.), si det, og ikke gjett.

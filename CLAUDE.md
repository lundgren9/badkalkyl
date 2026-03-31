# CLAUDE.md – badkalkyl (projektkontext)

Filnamnet med **versaler** följer vanlig **Claude Code**-praxis (Anthropics CLI letar efter `CLAUDE.md` i projektroten).

## Vad den här filen är (och inte är)

**Nej** – varken webbläsaren eller Git läser den här filen automatiskt ”först”. Det finns ingen universell standard som tvingar alla verktyg att öppna den.

**Däremot** används `CLAUDE.md` ofta som **fast projektkontext för AI** och utvecklingsverktyg:

- **Cursor:** Regeln `.cursor/rules/badkalkyl-claude.mdc` är satt till `alwaysApply: true` och instruerar assistenten att följa **`CLAUDE.md`**. Övriga regler ligger under `.cursor/rules/`.
- **Claude Code** (Anthropics CLI): letar efter **`CLAUDE.md`** i projektroten — samma fil som här.

**Syfte med denna fil:** kort, beständig **projektinformation** (länkar, vad repot är, konventioner) så att du eller en assistent slipper leta.

Uppdatering: omdöpt från `Claude.md` till `CLAUDE.md` och kopplad till Cursor-regel `badkalkyl-claude.mdc`.

---

## Konvention: `.html` i repot ska visas **live** (GitHub Pages)

**Standard:** När du arbetar med eller beskriver **HTML-filer som ligger i det här repot**, utgå från att de ska **visas och länkas som publicerade sidor på GitHub Pages**, inte som rå källkod på `github.com/.../blob/...`.

- **Bas-URL:** `https://lundgren9.github.io/badkalkyl/`
- **Exempel:** `index.html` → `https://lundgren9.github.io/badkalkyl/` (eller `.../index.html`).  
  `github.html` → `https://lundgren9.github.io/badkalkyl/github.html`

**Undantag:** Om användaren **uttryckligen** vill granska blob-vy, diff, eller öppna en lokal fil — följ då det. Annars: **live först**.

Uppdatering: denna konvention tillagd på användarens önskemål.

---

## Konvention: redigera bara **`index.html`** (inte **`badkalkyl.html`**)

- **`index.html`** är den **aktiva** applikationsfilen (den som GitHub Pages använder som startsida och som ska utvecklas).
- **`badkalkyl.html`** är en **kopia** som fungerar som **referens / ”original”**-arkiv av hur `index.html` sett ut vid något tillfälle — den ska **inte** uppdateras av assistenten i vanliga fall.

**Instruktion till assistent:** Gör **alla** kod- och innehållsändringar i **`index.html`** (och i andra filer som användaren pekar ut). **Rör inte `badkalkyl.html`** om användaren **uttryckligen** inte ber dig ändra just den filen.

Uppdatering: konvention tillagd — `badkalkyl.html` är avsedd som fryst kopia, inte parallell källkod.

---

## Konvention: **inte** `git push` utan att användaren bett om det

Användaren vill **granska ändringar i Cursor** (diff, filer, ev. commit lokalt) **innan** något skickas till **GitHub**.

**Instruktion till assistent:** Kör **inte** `git push` (eller motsvarande som publicerar till `github.com`) som en automatisk uppföljning av en uppgift. **Undantag:** användaren skriver uttryckligen att du ska pusha, committa och pusha, eller ”lägg upp på GitHub”.

Lokala `git add` / `git commit` får användas om användaren ber om det; annars räcker det ofta att bara spara filer så att användaren själv committar och pushar när hen är nöjd.

Uppdatering: tillagd så att push alltid är ett medvetet steg för användaren.

---

## CLAUDE.md och en **PRD** — samma sak?

**Nej, inte riktigt** — de kan **komplettera** varandra.

- **`CLAUDE.md` (här):** tunn **navigations- och agentkontext**: vad repot är, länkar, teknik i korthet, **konventioner** (t.ex. HTML via Pages). Snabbt att läsa för en assistent. **Inte** en fullständig kravspecifikation.

- **PRD (Product Requirements Document):** beskriver **vad produkten ska uppnå** för användare/intressenter: mål, omfattning, prioriterade funktioner, användarscenarier, acceptanskriterier, ibland mått och version av krav. Ofta längre och mer formell.

**Rekommendation:** Behåll **`CLAUDE.md`** som ”var är vi, hur länkar vi, hur jobbar vi”. Lägg vid behov till en **`PRD.md`** (eller `docs/PRD.md`) om du vill ha **beständiga produktkrav** som AI och människor kan följa vid större ändringar — då kan `CLAUDE.md` kort **hänvisa** till PRD:en (`Se PRD.md för krav och scope`).

---

## Offentliga länkar (ömsesidigt kopplade)

- **Live-app** (GitHub Pages): https://lundgren9.github.io/badkalkyl/
- **Källkod** (repo, issues, kloning): https://github.com/lundgren9/badkalkyl

- **README.md** på GitHub länkar till live-sidan och beskriver repot.
- **`index.html`:** i **sidhuvudet** länk till repot, **`CLAUDE.md`** (projektkontext) och **Git/GitHub-hjälp** (`github.html`). Under **Teknikinformation** finns även repot, live-URL och `github.html`. (`badkalkyl.html` kan fortfarande likna denna fil men underhålls inte av assistenten — se konventionen ovan.)

---

## Kort om projektet

- **Simrishamns kommun** – badanläggningskalkyl: ansvar **40100**, verksamhet **3400**, **Kommun-BAS 26**.
- **Teknik:** huvudfil **`index.html`** med inbäddad CSS och JavaScript (ES6+); Chart.js och Google Fonts via CDN. Filen **`badkalkyl.html`** är arkivkopia — redigeras inte av assistenten utan särskild begäran.
- **Publicering:** GitHub Pages från repot [lundgren9/badkalkyl](https://github.com/lundgren9/badkalkyl).
- **Underlag PDF:** `260330_badanalys.pdf` – utfall och budget per **2026-03-30** (se README).
- **Git/GitHub-hjälp:** `github.html` + `github-doc.css` (läsbar sida via Pages, inte via blob-URL); källtext i `github.md`.

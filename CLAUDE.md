# CLAUDE.md – badkalkyl (projektkontext)

Filnamnet med **versaler** följer vanlig **Claude Code**-praxis (Anthropics CLI letar efter `CLAUDE.md` i projektroten).

## Vad den här filen är (och inte är)

**Nej** – varken webbläsaren eller Git läser den här filen automatiskt ”först”. Det finns ingen universell standard som tvingar alla verktyg att öppna den.

**Däremot** används `CLAUDE.md` ofta som **fast projektkontext för AI** och utvecklingsverktyg:

| Miljö | Vanlig praxis |
|--------|----------------|
| **Cursor** | Regeln `.cursor/rules/badkalkyl-claude.mdc` är satt till `alwaysApply: true` och instruerar assistenten att följa **`CLAUDE.md`** för länkar, publicering och projektomfattning. Övriga regler ligger under `.cursor/rules/`. |
| **Claude Code** (Anthropics CLI) | Letar efter **`CLAUDE.md`** i projektroten — samma fil som här. |

**Syfte med denna fil:** kort, beständig **projektinformation** (länkar, vad repot är) så att du eller en assistent slipper leta.

Uppdatering: omdöpt från `Claude.md` till `CLAUDE.md` och kopplad till Cursor-regel `badkalkyl-claude.mdc`.

---

## Offentliga länkar (ömsesidigt kopplade)

| Vad | URL |
|-----|-----|
| **Live-app** (GitHub Pages) | https://lundgren9.github.io/badkalkyl/ |
| **Källkod** (repo, issues, kloning) | https://github.com/lundgren9/badkalkyl |

- **README.md** på GitHub länkar till live-sidan och beskriver repot.
- **`index.html`** (och `badkalkyl.html`) har i **sidhuvudet** och under **Teknikinformation** länkar till både repot och live-adressen.

---

## Kort om projektet

- **Simrishamns kommun** – badanläggningskalkyl: ansvar **40100**, verksamhet **3400**, **Kommun-BAS 26**.
- **Teknik:** en huvudfil `index.html` med inbäddad CSS och JavaScript (ES6+); Chart.js och Google Fonts via CDN.
- **Publicering:** GitHub Pages från repot [lundgren9/badkalkyl](https://github.com/lundgren9/badkalkyl).
- **Underlag PDF:** `260330_badanalys.pdf` – utfall och budget per **2026-03-30** (se README).
- **Git/GitHub-hjälp:** `github.html` + `github-doc.css` (läsbar sida via Pages, inte via blob-URL); källtext i `github.md`.

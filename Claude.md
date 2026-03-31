# Claude.md – badkalkyl (projektkontext)

## Vad den här filen är (och inte är)

**Nej** – `Claude.md` är inte en fil som ”alla program” eller webbläsaren automatiskt läser först. Det finns ingen universell standard som garanterar det.

**Däremot** används liknande filer ofta som **kontext för AI-assistenter** eller utvecklingsverktyg, om du (eller verktyget) väljer att ta med dem:

| Miljö | Vanlig praxis |
|--------|----------------|
| **Cursor** | Primärt `.cursor/rules/` och regler du @-refererar; `AGENTS.md` i projektroten förekommer också. Inget tvingar Cursor att alltid läsa `Claude.md` – lägg den i chatten med @ om den ska användas aktivt. |
| **Claude Code** (Anthropics CLI) | Letar ofta efter **`CLAUDE.md`** (stora bokstäver) i projektroten. Om du använder det verktyget kan du kopiera innehållet dit eller länka mellan filerna. |

**Syfte med denna fil:** kort, beständig **projektinformation** (länkar, vad repot är) så att du eller en assistent slipper leta.

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

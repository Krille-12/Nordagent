# Nordagent Website — Claude Code Prompt

## Instruktion

Byg et komplet, responsivt website for virksomheden **Nordagent** med HTML + Tailwind CSS. Brug UI UX Pro Max skillen til at generere et design system først. Websitet skal have sprogskifter (dansk/engelsk). Start med den danske version.

---

## Design-retning: Nordisk æstetik

En stilart kendetegnet ved minimalisme, funktionalitet og elegance med fokus på lyse farver, naturlige materialer som lyst træ og læder samt rene linjer.

- **Farver**: Lyse, varme toner — off-white og cremede baggrunde, varme gråtoner, accenter i dæmpede naturtoner (sand, lyst træ, varm brun/cognac). Undgå mørke/kolde temaer.
- **Materialer/teksturer**: Subtile teksturer der hinter til lyst træ og læder — f.eks. bløde baggrundstexturer, varme skygger, afrundede kort med warmth.
- **Typografi**: Moderne sans-serif (Inter, Söhne, eller tilsvarende via Google Fonts). Stor, tydelig overskriftstypografi. Brødtekst der er behagelig at læse.
- **Layout**: Generøs spacing, rene linjer, klare sektioner. Intet visuelt støj.
- **Animationer**: Subtile fade-in og slide-up ved scroll. Ingen flashy effekter.
- **Stemning**: Troværdigt, roligt, professionelt — som et møde med en god rådgiver.

Kør dette som udgangspunkt for design system:
```bash
python3 skills/ui-ux-pro-max/scripts/search.py "nordic minimalist consulting professional clean" --design-system
```

---

## Sidestruktur og indhold

### 1. Navigation
- Logo: "Nordagent" (tekst-logo, clean sans-serif)
- Menu-items: Hvert item har SEPARATE spans for hvert sprog, f.eks.: `<span data-lang="da">Ydelser</span><span data-lang="en" style="display:none">Services</span>`. Vis KUN ét sprog ad gangen.
- Sprogskifter: DA / EN (flag-ikoner eller tekst-toggle)
- Sticky navbar med blur-baggrund ved scroll

### 2. Hero-sektion
- **Overskrift**: "Jeres medarbejdere bruger timer på opgaver, der kan klares på sekunder"
- **Undertekst**: "Nordagent bygger intelligente automationer og AI-agenter, der overtager det gentagne arbejde — så jeres team kan fokusere på det, der skaber værdi."
- **CTA-knap**: "Se hvad I kan spare" → scroller til eksempler
- **Sekundær CTA**: "Kontakt os" → scroller til kontakt
- Evt. subtil baggrundsgrafik/illustration i nordisk stil (geometrisk, abstrakt)

### 3. Problemet vi løser
- **Overskrift**: "Kender I det her?"
- Tre korte, genkendelige scenarier i et grid:
  - "Jeres bogholder copy-paster fakturaer manuelt — dag efter dag"
  - "Jeres sælger glemmer at følge op på nye leads"
  - "Jeres kundeservice svarer på de samme spørgsmål igen og igen"
- **Afslutning**: "Det behøver ikke være sådan. De fleste af de opgaver kan automatiseres i dag."

### 4. Konkrete eksempler (showcase-sektion)
- **Overskrift**: "Se hvad en AI-agent kan gøre for jer"
- Fire kort i et grid, hvert med ikon, titel, beskrivelse og en "Tid sparet"-indikator:

**Kort 1 — Den automatiske bogholder**
- Ikon: Dokument/faktura
- "En faktura lander i indbakken. AI'en læser beløb, CVR og kontonummer, bogfører det i jeres system, og giver besked på Teams hvis noget ser forkert ud."
- Gevinst: "15 min sparet pr. faktura"

**Kort 2 — Den intelligente kundeservice-agent**
- Ikon: Chat-boble
- "En kunde skriver en email. AI'en forstår om det er en reklamation, et spørgsmål eller en bestilling — og sender det til den rette person med et foreslået svar."
- Gevinst: "Responstid: fra timer til sekunder"

**Kort 3 — Selvkørende CRM-opfølgning**
- Ikon: Mennesker/netværk
- "En ny kunde oprettes i jeres CRM. Automatisk sendes en velkomstmail, sælgeren får en påmindelse om opfølgning dag 3, og ledelsen kan se status i realtid."
- Gevinst: "Ingen leads falder mellem to stole"

**Kort 4 — Datatjek på autopilot**
- Ikon: Database/søg
- "Jeres system slår automatisk CVR-numre op, tjekker om kunden er aktiv, og beriger jeres kundedata — uden at nogen løfter en finger."
- Gevinst: "Altid opdateret kundedata"

Hvert kort skal visuelt vise: Hvad sker der → Hvad gør AI'en → Hvad er gevinsten.

### 5. Sådan arbejder vi (proces-sektion)
- **Overskrift**: "Fra samtale til automation på få uger"
- Fire trin i en horisontal tidslinje eller vertikal stepper:
  1. **Gratis afklaring** — "Vi lytter til jeres hverdag og finder mulighederne"
  2. **Analyse** — "Vi identificerer de opgaver der æder mest tid"
  3. **Implementering** — "Vi bygger og tester løsningen sammen med jer"
  4. **Drift** — "I sparer tid fra dag ét — vi holder øje med at det kører"
- Hvert trin med nummer, ikon og kort beskrivelse

### 6. Hvorfor Nordagent
- **Overskrift**: "Derfor vælger virksomheder Nordagent"
- Fire argumenter i et grid med ikoner:
  - 🇪🇺 **GDPR-compliant** — "Jeres data bliver i EU. Altid."
  - 💰 **Ingen dyre licenser** — "Vi bygger på open source-teknologi"
  - 🎯 **Resultater, ikke teknik-snak** — "I betaler for den tid I sparer, ikke for buzzwords"
  - 🇩🇰 **Dansk rådgivning** — "Vi taler jeres sprog — både fagligt og bogstaveligt"

### 7. Om Nordagent
- **Overskrift**: "Mennesket bag Nordagent"
- Kort, personlig tekst (plads til foto):
  - "Nordagent er grundlagt af [Navn], med en baggrund i forretningsudvikling og en passion for at gøre teknologi tilgængeligt. Vi tror på, at automatisering ikke handler om at erstatte mennesker — men om at give dem tid til det arbejde, der virkelig betyder noget."
- Hold det varmt, ærligt og kort.

### 8. Kontakt
- **Overskrift**: "Lad os tage en snak"
- **Undertekst**: "Skriv til os — det koster ikke noget at høre, hvad der er muligt."
- Email-adresse (klikbar mailto-link)
- Simpel kontaktformular: Navn, Email, Virksomhed, Besked, Send-knap
- Formularen behøver ikke backend — brug mailto: eller vis en placeholder

### 9. Footer
- Nordagent logo
- Sprogskifter DA/EN
- CVR-nummer (placeholder: "CVR: XX XX XX XX")
- Link til privatlivspolitik
- © 2025 Nordagent

---

## Tekniske krav
- Single-page HTML + Tailwind CSS (CDN)
- Responsivt: mobil, tablet, desktop
- Smooth scroll til sektioner
- Sprogskifter: VIGTIGT — brug data-attributter (f.eks. data-lang="da" og data-lang="en") på SEPARATE elementer for hvert sprog. JavaScript toggler ved at sætte display:none på alle elementer med det inaktive sprog og display:"" på det aktive. Der må ALDRIG vises to sprog samtidig. Hvert tekstelement skal kun indeholde ét sprog. Eksempel: `<span data-lang="da">Ydelser</span><span data-lang="en" style="display:none">Services</span>`. Standard-sprog er dansk.
- Brug Lucide Icons eller Heroicons for ikoner
- Google Fonts import i head
- Semantisk HTML (header, main, section, footer)
- Tilgængelighed: kontrast min 4.5:1, ARIA labels, keyboard-navigerbart

---

## Engelsk version — KRITISK IMPLEMENTATIONSREGEL
ALLE tekstelementer skal have to separate child-elementer: et med data-lang="da" og et med data-lang="en". JavaScript toggler visibility. Der må ALDRIG stå to sprog synligt samtidig. 

Sprogskifter-funktionen:
```javascript
function setLanguage(lang) {
  document.querySelectorAll('[data-lang]').forEach(el => {
    el.style.display = el.dataset.lang === lang ? '' : 'none';
  });
}
// Default: dansk
document.addEventListener('DOMContentLoaded', () => setLanguage('da'));
```

Eksempler på engelske overskrifter:
- Hero: "Your team spends hours on tasks that take seconds to automate"
- Problemer: "Sound familiar?"
- Eksempler: "See what an AI agent can do for you"
- Proces: "From conversation to automation in weeks"
- Hvorfor: "Why businesses choose Nordagent"
- Om: "The person behind Nordagent"
- Kontakt: "Let's talk"

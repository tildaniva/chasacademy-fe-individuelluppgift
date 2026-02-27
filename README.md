# MyShop - Tillgänglighet och Prestandaoptimering

## Om projektet
En produktlistsida som har optimerats för tillgänglighet (WCAG) och prestanda (LCP).

## Filer
- `index.html` - Sidans HTML-struktur
- `styles.css` - Stilmall
- `script.js` - JavaScript med event handlers och testning

## Genomförda förbättringar

### Tillgänglighet
- Semantisk HTML-struktur (header, nav, main, section, footer)
- Korrekt rubrikhierarki (h1 → h2 → h3)
- Alt-texter på alla bilder
- Labels kopplade till formulärfält
- Knappar som `<button>` istället för `<div>`
- Synliga fokusindikatorer för tangentbordsnavigering
- Förbättrad färgkontrast (WCAG AA)

### Prestanda (LCP)
- Komprimerade bilder
- `loading="lazy"` på bilder under fold
- `fetchpriority="high"` på hero-bilden
- `width` och `height` på bilder för att undvika layout shift
- Script flyttat till slutet av body med `defer`
- Borttagen blockerande kod (simulateHeavyWork)

## Testning
Sidan testas automatiskt med axe-core vid laddning. Resultat visas i webbläsarens konsol.

LCP mäts med PerformanceObserver och loggas i konsolen.

## Köra lokalt
Öppna `index.html` med Live Server eller liknande.

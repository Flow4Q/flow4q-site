# Afspraken flow4q-site

Statische site voor www.flow4q.com, gehost op GitHub Pages vanaf de branch `main`. Geen build-stap: wat in de repo staat, is wat live staat.

## Structuur

- 18 losse HTML-pagina's in de root: `index.html`, `cases.html`, `privacy.html`, `voorwaarden.html` en 14 landingspagina's.
- Gedeelde stijl staat in `css/site.css`: kleurvariabelen, reset, body, nav en footer. Pagina-specifieke stijl blijft in het `<style>`-blok van de pagina zelf.
- Elke pagina laadt site.css met een versienummer: `<link rel="stylesheet" href="/css/site.css?v=1">`.

## Regels bij wijzigingen

- **Wijziging aan css/site.css**: verhoog `?v=` in alle 18 pagina's, anders blijft de browser de oude versie uit cache tonen.
- **Nav-HTML** is 18 keer identiek en moet dus 18 keer aangepast worden. Dat geldt ook voor de footer-HTML.
- **Geen build-stap** toevoegen. Geen includes, geen frameworks, geen preprocessors.
- **Altijd screenshots voor en na** maken, op desktop en mobiel, voor elke zichtbare wijziging.
- **Wachten op akkoord voor commit.** Toon eerst de wijziging, commit pas na expliciet akkoord, push alleen als daarom gevraagd wordt.

## Lokaal testen

```bash
npx -y serve -l 8080 .
```

Pagina's staan dan op http://localhost:8080/, bijvoorbeeld http://localhost:8080/voorraadbeheer-app.html.

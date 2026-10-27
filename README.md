# DealHunter – mobile Angebots-Web-App (Beta)

## Was diese erste Version kann
- Mobile Kachel-Startseite: PlayStation & Konsolen, Shop-Sales, Supermarktprospekte, Preisalarm, Elektronik und Wunschliste.
- Regionale Einstiegsquellen für Gaggenau/Rastatt.
- Händler- und Prospektlinks zu konkreten Quellen.
- Wunschliste und Preisalarme werden lokal im Browser auf diesem Gerät gespeichert.
- Manuelle Preisverlauf-Einträge; die App erfindet keine aktuellen Preise oder Lagerbestände.
- Externe Suchseiten öffnen sich in einem neuen Tab.

## Grenzen dieser Beta
- Die App crawlt Händlerseiten nicht und behauptet keine Live-Preise. Händlerlinks führen zu den Quellen, die dort aktuelle Daten anzeigen.
- Preisverlauf basiert in dieser Version auf manuell eingetragenen Preisen. Automatische Preisverläufe und Discord-Push brauchen einen separaten, sicher betriebenen Backend-/GitHub-Actions-Dienst mit konkreten Produkt-URLs und einem Discord-Webhook als GitHub Secret.
- `localStorage` ist browser- und gerätegebunden. Löschen von Website-Daten kann die Liste löschen.
- Links und Suchparameter können sich bei Händlern ändern; prüfe vor dem Veröffentlichen die Links auf deinem Gerät.
- Supermarkt-Angebote hängen oft von Filiale, PLZ und Laufzeit ab. Bitte im Prospekt/Shop nachprüfen.

## Verwendete Quellen
- KaufDA Gaggenau: https://www.kaufda.de/Filialen/Gaggenau/Supermarkt/v-c11
- weekli Gaggenau: https://www.weekli.de/gaggenau/supermaerkte/filialen
- Lidl Online-Prospekte: https://www.lidl.de/c/online-prospekte/s10005610
- REWE Angebote: https://www.rewe.de/angebote/
- EDEKA Angebote: https://www.edeka.de/angebote.jsp
- ALDI SÜD Angebote: https://www.aldi-sued.de/de/angebote.html
- Kaufland Angebote: https://filiale.kaufland.de/angebote.html
- PlayStation Direct: https://direct.playstation.com/de-de/
- MediaMarkt, Saturn, Amazon und idealo: Händler-/Suchseiten im App-Code.

Diese Links sind Startpunkte, keine Behauptung, dass ein konkretes Produkt gerade lieferbar ist.

## Veröffentlichung über GitHub Pages (iPhone)
1. Öffne GitHub in Safari und erstelle ein Repository `dealhunter` (für die einfachste GitHub-Free-Nutzung öffentlich).
2. Öffne das Repository → **Add file → Upload files** und lade `index.html` sowie `README.md` hoch. Committe die Dateien auf `main`.
3. Gehe zu **Settings → Pages**.
4. Unter **Build and deployment** wähle **Deploy from a branch**, Branch `main`, Ordner `/ (root)`, dann **Save**.
5. Warte einige Minuten und öffne die angezeigte Pages-URL. GitHub dokumentiert, dass Pages aus einem Repository eine statische Website mit `index.html` veröffentlichen kann: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
6. In Safari auf dem iPhone: Teilen → **Zum Home-Bildschirm**. Dann öffnest du DealHunter wie eine App.

## Discord-Preisalarm – nächste Ausbaustufe
Nicht den Discord-Webhook in `index.html` eintragen! Eine öffentlich zugängliche Website würde ihn preisgeben. Für echte Hintergrundalarme braucht es einen GitHub Actions Workflow, der die explizit konfigurierten Produktseiten prüft und `DISCORD_WEBHOOK_URL` nur aus **Settings → Secrets and variables → Actions** liest. Bestands-Parsing ist pro Händler unterschiedlich und sollte erst nach einem Test mit konkreten Produkt-URLs aktiviert werden.

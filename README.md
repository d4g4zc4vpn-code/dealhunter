# KANKA Beta 17 – Fußball kompakt

Änderungen:
- Die breite SportAPI-Ansicht mit `data-league="all"` wurde entfernt, damit nicht mehr unzählige Spiele angezeigt werden.
- Die Fußballseite konzentriert sich auf VfB Gaggenau 2001 und FC Rastatt 04.
- Platzierung, Punkte, letztes Ergebnis und nächstes Spiel werden kompakt gezeigt.
- Fenerbahçe/Galatasaray sowie Pokal & Europa sind eingeklappt und werden nur bei Bedarf geöffnet.
- Links zu FUSSBALL.DE führen zu den offiziellen Mannschaftsseiten mit aktuellen Tabellen und Ergebnissen.

Wichtig: Die zwei regionalen Ergebnis-Karten zeigen den geprüften Stand vom 28.10.2026 und sind statische Angaben. Für Live-Aktualisierungen die offiziellen Links öffnen; automatische Live-Daten brauchen eine verlässliche API/Backend-Lösung.

Upload: Repository-Hauptordner mit `index.html`, `manifest.webmanifest` und dem kompletten `assets/`-Ordner aktualisieren.


## Beta 18 – KANKA Einkaufsplaner
- Gemeinsamer Planungsansatz im bestehenden Haushalt-Bereich: Produktliste, Mengen und manuell erfasste Prospektangebote.
- Vergleich summiert die jeweils günstigsten erfassten Preise je Markt und zeigt die Preisabdeckung, damit unvollständige Warenkörbe nicht fälschlich als vollständige Gesamtsumme verstanden werden.
- Unterstützte Märkte: Lidl, Aldi Süd, Kaufland, REWE, EDEKA, PENNY, Netto, dm und Rossmann.
- Produkt-/Preisnotizen werden lokal im Browser gespeichert. Sie synchronisieren sich nicht automatisch zwischen Geräten.
- Externe Prospektseiten lassen sich nicht ohne Schnittstelle automatisch auslesen. Für automatisierte Angebote ist ein rechtlich geeigneter Datenanbieter und ein Backend nötig; API-Schlüssel dürfen nicht in die öffentliche HTML-Datei.

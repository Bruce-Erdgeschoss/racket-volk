# rationaleZahlen

Kleine DrRacket-Übung zur Modellierung rationaler Zahlen mithilfe einer eigenen Datenstruktur und einfacher Operationen wie Multiplikation, Addition, Vergleich und Ausgabe.

## Projektüberblick

- `rationaleZahlen`: Quelltext-Datei mit dem `#reader` der HtDP-Beginner-Sprache.
- `define-struct xy`: Repräsentiert rationale Zahlen als Zähler (`x`) und Nenner (`y`).
- Funktionen: `make-rat`, `numer`, `denom`, `mul-rat`, `add-rat`, `equal-rat?`, `print-rat` (inkl. Beispielen in den Kommentaren).

## Voraussetzungen

- Racket bzw. DrRacket (empfohlen) in einer Version, die den HtDP-Beginner-Reader enthält.
- Keine externen Bibliotheken; der Code verlässt sich ausschließlich auf die Beginner-Abstraktionen.

## Verwendung

1. Datei `rationaleZahlen` in DrRacket öffnen und mit „Run“ ausführen.
2. Alternativ per Terminal innerhalb des Repos:

   ```bash
   racket rationaleZahlen
   ```

   Anschließend lassen sich Werte interaktiv erstellen, z. B.:

   ```racket
   (define halb (make-rat 1 2))
   (define dreiviertel (make-rat 3 4))
   (print-rat (mul-rat halb dreiviertel)) ; => "3/8"
   ```

## Weiterentwicklungsideen

- Zusätzliche Tests bzw. `check-expect`-Beispiele ergänzen, um die aktuelle Implementierung abzusichern.
- Sicherstellen, dass Nenner != 0 ist und Ergebnisse stets gekürzt werden.
- Bekannte Fehler korrigieren (z. B. die Additionsfunktion nutzt aktuell zweimal den Zähler statt Zähler/Nenner zu kombinieren).
- Optional: Hilfsfunktionen wie `gcd` integrieren, damit Ausgaben automatisch gekürzt erscheinen.

## Lizenz

Keine explizite Lizenz hinterlegt; bei Bedarf ergänzen.

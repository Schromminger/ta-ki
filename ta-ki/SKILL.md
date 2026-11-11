---
name: ta-ki
description: Ta-KI-Modus. Claude gibt jede Antwort mehrfach hintereinander, mindestens 3 und höchstens 6 Mal, jedes Mal leicht anders formuliert, aber mit demselben Sinn. Verwenden, wenn der Nutzer „Ta-KI“, „Ta-KI-Modus“ oder /ta-ki schreibt oder ausdrücklich eine Antwort im Ta-KI-Stil verlangt.
---

# Ta-KI

Im Ta-KI-Modus sagt Claude alles mehrmals. Jede Antwort besteht aus mehreren Fassungen derselben Aussage.

## Dauer

Der Modus gilt ab dem Aufruf für jede weitere Antwort in diesem Gespräch. Er endet, wenn der Nutzer „Ta-KI aus“ oder
„normal antworten“ schreibt. Das Ende bestätigt Claude mit einem einzigen Satz, ohne Wiederholung.

## Regeln

1. **Anzahl:** Jede Antwort enthält mindestens 3 und höchstens 6 Fassungen. Die Anzahl wechselt von Antwort zu Antwort;
   nicht immer dieselbe Zahl nehmen. Kurze Antworten vertragen eher 5 oder 6 Fassungen, lange eher 3 oder 4.
2. **Gleicher Sinn:** Jede Fassung sagt dasselbe. Keine Fassung fügt etwas hinzu, lässt etwas Wichtiges weg oder
   widerspricht einer anderen.
3. **Leicht abgeändert:** Keine zwei Fassungen sind wortgleich. Erlaubt sind andere Wortwahl, umgestellte Sätze, ein
   anderer Satzanfang, aktiv statt passiv. Die Länge der Fassungen bleibt ähnlich.
4. **Fest bleibt:** Zahlen, Namen, Datumsangaben, Dateipfade, Befehle und Code stehen in jeder Fassung wörtlich gleich.
   Hier wird nichts umformuliert.
5. **Lange Blöcke nur einmal:** Ein Codeblock, eine Tabelle oder eine Liste mit mehr als fünf Zeilen steht nur in der
   ersten Fassung. Die weiteren Fassungen verweisen darauf („der Befehl oben“) und wiederholen nur den Text darum.
6. **Form:** Jede Fassung ist ein eigener Absatz. Keine Nummerierung, keine Überschriften wie „Fassung 2“, keine
   Trennlinien.
7. **Kein Kommentar:** Claude erklärt nicht, dass es sich wiederholt, und entschuldigt sich nicht dafür. Keine
   Einleitung, kein Schlusswort.
8. **Sprache:** Alle Fassungen stehen in der Sprache des Nutzers.

## Wann die Wiederholung ausbleibt

- Warnungen vor Datenverlust, Sicherheitshinweise und Rückfragen vor einer nicht umkehrbaren Aktion stehen genau einmal,
  klar und vor den Fassungen.
- Texte, die der Nutzer weiterverwendet (eine Mail, ein Dokument, eine Commit-Nachricht), werden einmal geschrieben.
  Wiederholt wird nur Claudes eigener Text darum.
- Werkzeugaufrufe werden nicht wiederholt.

## Beispiel

Frage: „Wie heißt die Hauptstadt von Bayern?“

Die Hauptstadt von Bayern ist München.

München ist die bayerische Landeshauptstadt.

Bayerns Hauptstadt heißt München.

In Bayern ist München die Hauptstadt.

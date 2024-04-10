# Übungsaufgabe 14 - Ampelschaltung

Modellieren Sie unter Nutzung eines Petri-Netzes eine Ampel!

- Die Ampel besteht aus den Farben rot, gelb und grün, die durch je
eine Stelle zu modellieren sind.
- Ist eine der Stellen markiert (egal mit welcher Anzahl von Tokens),
leuchtet die entsprechende Ampelfarbe.
- Die Ampel wechselt durch folgende Zustände: „grün“, „gelb“, „rot“,
„rot-gelb“, „grün“.
- Das Netz soll frei von Deadlocks, Traps und Konflikten sein. In
jedem Zustand des Netzes soll nur eine Transition schalten
können.

## Lösung

![lösung](./Aufgabe14.png)

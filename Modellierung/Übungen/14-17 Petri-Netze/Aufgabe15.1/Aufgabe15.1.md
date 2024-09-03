# Übungsaufgabe 15 - Uhr

Modellieren Sie unter Nutzung eines Petri-Netzes eine Uhr, so
dass an der jeweiligen Markierung die aktuelle Uhrzeit
ablesbar ist. Beachten Sie folgende Hinweise und
Rahmenbedingungen!

- Es soll eine 12-Stunden-Anzeige modelliert werden. Zusätzlich sollen die
Minuten 15, 30, 45, 00 ablesbar sein, die Stunden- „Anzeige“ wechselt jeweils
beim Übergang von 45 zu 00 Minuten. Die Stunden (von 0 bis 11) sollen jeweils
durch eine Stelle repräsentiert werden, ebenso soll es für die Minutenanzeige (00,
15, 30, 45) jeweils genau eine Stelle im Modell geben.
- Verwenden Sie in Ihrem Modell zunächst weder Kapazitäten noch Dimensionen.
- Stellen Sie sicher, dass in Ihrem Modell zu jedem Zeitpunkt nur genau eine
Transition schalten kann.
- Ergänzen Sie nun Ihr Petri-Netz um eine Stelle mit Kapazität,
welche die jeweilige Stunde „digital“ durch ihre Belegung mit
0 bis 11 Marken anzeigt.

## Lösung

![lösung](./Aufgabe15.1.png)

# Datenbanken - Übung 4

## 4.2)

1\. Fremdschlüsselbeschränkungen

- Beziehungen zwischen Tabellen

- Änderungen werden auch auf die Referenzen (pro wert) angewendet

2\. CASCADE-Optionen

- Erweiterung der Fremdschlüsselbeschränkungen

- Änderungen oder Löschungen werden auf andere Tabellen übertragen

3\. Prüfungen von Daten

- Erstellen von Integritätsprüfungen

- Es können Aktionen definiert werden die das tun (Daten überprüfen)

## 4.3)

a\)

1. Ergebnis: {3,3,5,7,7,10,10,10}

2. Bestellnummern aller Artikel

b\)

1. Ergebnis: {G. Hals, P. Schmidt, E. Meier}

2. Zeige alle Händler, die eine Bestellung aufgegeben haben.

c\)

1. Ergebnis: {13}

2. Händlernummer der Händler, die Artikel anbieten, aber keine
    Bestellung aufgegeben haben

d\)

1. Ergebnis: {3, 7, 10} (BNr)

> Bnr Hnr Datum Knr
>
> 3 7 01.12.2002 17
>
> 7 5 13.05.2003 17
>
> 10 5 01.09.2003 13

2. Daten aller Bestellungen vor dem 01.03.2003 oder nach dem 01.05.2003

e\)

1. Ergebnis:

<table style="width:100%;">
<colgroup>
<col style="width: 18%" />
<col style="width: 6%" />
<col style="width: 6%" />
<col style="width: 15%" />
<col style="width: 8%" />
<col style="width: 6%" />
<col style="width: 24%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th>Kunde (Name)</th>
<th>KNr</th>
<th>BNr</th>
<th>Datum</th>
<th>HNr</th>
<th>ANr</th>
<th>Bezeichnung</th>
<th>Anzahl</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>M. Mueller</td>
<td>13</td>
<td>10</td>
<td>01.09.2003</td>
<td>5</td>
<td><p>45</p>
<p>57</p>
<p>67</p></td>
<td><p>Steckernetzteil</p>
<p>TP-Kabel</p>
<p>Einbaukäfig</p></td>
<td><p>2</p>
<p>5</p>
<p>3</p></td>
</tr>
<tr class="even">
<td>A. Meier</td>
<td>17</td>
<td><p>3</p>
<p>7</p></td>
<td><p>01.12.2002</p>
<p>13.05.2003</p></td>
<td><p>7</p>
<p>5</p></td>
<td><p>57</p>
<p>67</p>
<p>67</p>
<p>45</p></td>
<td><p>TP-Kabel</p>
<p>Einbaukäfig</p>
<p>Einbaukäfig</p>
<p>Steckernetzteil</p></td>
<td><p>3</p>
<p>2</p>
<p>1</p></td>
</tr>
<tr class="odd">
<td>I. Schulze</td>
<td>23</td>
<td>5</td>
<td>27.04.2003</td>
<td>11</td>
<td>67</td>
<td>Einbaukäfig</td>
<td></td>
</tr>
</tbody>
</table>

2. Geben Sie alle Informationen zu Kunden, Bestellungen, Artikeln und
    der Anzahl der bestellten (aufgegeben) Artikel an, die in Beziehung
    zueinander stehen.

## 4.4)

a\) Namen aller Kunden: *π*<sub>Name</sub>​(Kunde)

b\) Bestellungen von Kunde Meier: *π*<sub>Bnr, Datum</sub>​(
*σ*<sub>Name</sub> = “Meier“ ​(Kunde ⋈ Bestellung))

c\) *π*<sub>Anr, Bez.</sub>​(Artikel − (*π*<sub>Anr</sub>​ (ist_auf ⋈
*σ*<sub>Datum</sub>= “13.05.2003“ (Bestellung ⋈ Artikel))))

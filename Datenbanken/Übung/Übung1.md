# Datenbanken - Übung 1

## 1. Datenbanken

**Datenbank**

Eine Datenbank ist ein strukturierter Datenbestand der vom
*Datenbankmanagementsystem (DBMS)* verwaltet wird. Die Speicherung der
Informationen findet meistens in Tabellenform statt.

**Datenbankmanagementsystem**

Das Datenbankmanagementsystem (kurz DBMS) ist die Software, die die
Datenbank verwaltet.

**Datenbanksystem**

Ein Datenbanksystem umfasst sowohl die Datenbank, als auch das DBMS.

## 2. Datenintegration und Redundanz

**Datenintegration** bedeutet, das Daten an einem zentralen Ort
gespeichert und verändert werden. Die Daten sind strukturiert. So kommt
es nicht zur **Datenredundanz** bei der Daten in vielfacher Form auf
verschiedenen Computern liegen und somit zum einen zusätzlicher Speicher
verbraucht wird, für Daten die nicht mehr aktuell sein könnten. Jedes
System verwaltet seine Daten selbst.

## 3. Transaktion

Eine Transaktion besteht aus mehreren Teilaktionen, bei denen in
mehreren Tabellen parallel Daten verändert werden. Die kleinen Aktionen
müssen erfolgreich abgeschlossen sein, bevor die Transaktion als fertig
angesehen werden kann.

Beispiel:

- In Tabelle1 stehen die Ausgaben und Einnahmen von Person1

- In Tabelle2 stehen die Ausgaben und Einnahmen von Person2

- Person1 überweist nun Person2 einen Betrag (Transaktion)

- Dafür müssen mehrere Teilaktionen ausgeführt werden:

  - Person1 wird der Betrag abgezogen

  - Person2 wird der Betrag gutgeschrieben

- Erst wenn beide Teilaktionen erfolgreiche sind, ist die Transaktion
  abgeschlossen

## 4. Synchronisation und Persistenz

**Synchronisation** bedeutet, dass mehrere Transaktionen gleichzeitig
koordiniert werden können (durch den DBMS).

**Persistenz** bedeutet, das Daten solange gespeichert werden können,
bis der DBMS sie explizit löscht.

## 5. Data Dictionary

Im Katalog befinden sich Metadaten, indem alle Definitionen und
Darstellungsregeln für alle Daten hinterlegt sind. Auch Beziehungen
zwischen Datenobjekten sind aufgelistet. Ziel ist das die Daten nicht
redundant gespeichert werden.

## 6. Fallbeispiele

<table>
<colgroup>
<col style="width: 34%" />
<col style="width: 32%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Beispiel</th>
<th>Pro DBMS</th>
<th>Contra DBMS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>a) Der Student Lukas Meier will seine CDs verwalten.</td>
<td><p>- Die Daten der CD’s können effizient verwaltet werden</p>
<p>- Ein DBMS hilft ihm einfache abfragen zu erstellen</p></td>
<td><p>- für die Anwendung zu komplex und überdimensioniert</p>
<p>- erhöhter Wartungsaufwand durch Updates und
Sicherheitspatches</p></td>
</tr>
<tr class="even">
<td><p>b) Die Supermarktkette LIDI</p>
<p>will für Auswertungszwecke</p>
<p>sämtliche von Ihren Kunden getätigten Einkäufe speichern.</p></td>
<td><p>- Effiziente Datenspeicherung</p>
<p>- Echtzeit-Berichterstattung über Lagerbestände</p>
<p>- Ein DBMS bietet gleichzeitig Mechanismen zum Datenschutz</p></td>
<td><p>- Daten müssen bereinigt werden, da alte Daten irrelevant sein
können</p>
<p>- Regelmäßige Wartung und Aktualisierung</p></td>
</tr>
<tr class="odd">
<td>c) Die Studentenplattform webunihelp.de soll um ein Forum erweitert
werden.</td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>d) Das Prüfungsamt der Fakultät Informatik will sämtliche erbrachten
Leistungen von Studenten elektronisch verwalten.</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

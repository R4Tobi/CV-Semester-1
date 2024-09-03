# Datenbanken - Übung 2

## 1. Anforderungen von Codd an ein DBMS

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codd’sche Regel</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Integration</p>
<ul>
<li><p>Einheitliche, nichtredundante Datenverwaltung</p></li>
</ul></td>
<td><p>Anstelle von vielen, nicht genormten Speichern von Daten, werden
Daten an einem zentralen System strukturiert gespeichert.</p>
<p>Statt vielen Benutzern die Kundendaten auf ihren Rechnern speichern
und gelegentlich mal austauschen, werden Daten so zentral gespeichert,
dass sie für jeden Aktuell einsehbar sind und in Echtzeit verändert
werden können.</p></td>
</tr>
<tr class="even">
<td><p>Operationen</p>
<ul>
<li><p>Speichern, Suchen, Ändern</p></li>
</ul></td>
<td>Damit Anwendungen auf die Daten zugreifen können, muss das DBMS
Daten ändern, speichern, löschen und suchen müssen.</td>
</tr>
<tr class="odd">
<td><p>Katalog</p>
<ul>
<li><p>Zugriffe auf Datenbankbeschreibungen in Data Dictionary</p></li>
</ul></td>
<td><p>Der Katalog sorgt dafür, das Abfragen und Operationen richtig
ausgeführt werden.</p>
<p>Tabellenstrukturen und Metadaten werden hier gesichert.</p></td>
</tr>
<tr class="even">
<td><p>Benutzersichten</p>
<ul>
<li><p>Unterschiedliche Anwendungen brauchen unterschiedliche Sichten
auf den Datenbestand</p></li>
</ul></td>
<td>Berechtigungsverwaltung.</td>
</tr>
<tr class="odd">
<td><p>Integritätssicherung</p>
<ul>
<li><p>Korrektheit des Dateninhalts</p></li>
</ul></td>
<td>Damit die Daten in der Datenbank Korrekt sind muss das DBMS die
Daten vor einer Änderung validieren, z.B. auf den Datentyp oder die
Zeichenlänge.</td>
</tr>
<tr class="even">
<td><p>Datenschutz</p>
<ul>
<li><p>Ausschluss unautorisierter Zugriffe</p></li>
</ul></td>
<td>Das DBMS muss Zugriffe, die nicht vom System oder autorisierten
Clients kommen unterbinden, damit die Daten geschützt bleiben und nicht
in die falschen Hände geraten.</td>
</tr>
<tr class="odd">
<td><p>Transaktionen</p>
<ul>
<li><p>Mehrere DB-Operationen als Funktionseinheit</p></li>
</ul></td>
<td>Wenn in mehreren Tabellen Änderungen gemacht werden, und diese
voneinander abhängen muss sichergestellt werden das alle Änderungen
durchgeführt werden. (Alles-oder-nichts-Prinzip)</td>
</tr>
<tr class="even">
<td><p>Synchronisation</p>
<ul>
<li><p>Parallele Transaktionen Koordinieren</p></li>
</ul></td>
<td>Sollten mehrere Anwendungen gleichzeitig eine Transaktion ausführen
wollen, muss das DBMS in der Lage sein beide parallel durchzuführen ohne
die Daten zu verfälschen.</td>
</tr>
<tr class="odd">
<td><p>Datensicherung</p>
<ul>
<li><p>Wiederherstellung von Daten nach einem Systemabsturz</p></li>
</ul></td>
<td>Die beste Datenspeicherung bringt nichts, wenn kein Backup
existiert, in dem regelmäßig der gesamte Datenbestand gespeichert wird,
damit die Daten im Fall eines Festplattenfehlers nicht verloren
gehen.</td>
</tr>
</tbody>
</table>

## 2. Datenbankmodell und Datenbankschema

Das **Datenbankmodell** ist die theoretische Grundlage für ein DBS, und
bestimmt über die Struktur der Datenbank. Beispielsweise ob die Form der
Datenbank ein relationales Modell (Tabelle) ist.

Das **Datenbankschema** reguliert, wie Daten organisiert sind. Dazu
zählen die Namen der Tabellen, die Felder und Datentypen in den Modellen
und die Beziehungen zwischen den Modellen.

Das Datenbankmodell definiert wie die Daten in der Datenbank gespeichert
werden und wie sie verknüpft sind. Das Datenbankschema hilft dem
Programmierer dabei Anwendungen, die mit der Datenbank interagieren, zu
bauen.

## 3. 3-Ebenen-Schema (ANSI-SPARC-Architektur)

\- Unterteilt in 3 Ebenen

1\. Sicht auf die Daten, bzw. auf die interne Ebene

2\. konzeptionelle Ebene ist die Gesamtsicht auf die Daten (ohne
Einschränkung)

3\. Benutzersichten auf die Daten beschreiben die externe Ebene

**Externe Ebene**

Enthält die Benutzersichten auf die Daten einen Ausschnitt aus den
Gesamtdaten. Je nach Anwendung/Anwender werden verschiedene Daten
offengelegt. Verwaltet wird diese Ebene durch den Datenbankentwickler.

**Konzeptionelle Ebene**

Diese Ebene ist die Gesamtübersicht über alle Daten, Relationen, Abläufe
und Logiken. Ziel der konzeptionellen Ebene ist die Redundanzfreie
Speicherung von Daten. Diese Ebene wird ebenfalls primär vom
Datenbankentwickler verwaltet.

**Interne Ebene**

In dieser Ebene geht es um die physikalische Implementierung.
Informationen zu Datenstrukturen auf physikalischen Speicher und
Zugriffsmechanismen werden hier verwaltet. Diese Ebene wird vom
Datenbankadministrator verwaltet.

## 4. Datenunabhängigkeit

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr class="header">
<th>Physische Datenunabhängigkeit</th>
<th>Die physische Organisation der Daten (Form und Träger) soll ohne
Auswirkungen auf die Logische Struktur der Daten und ohne Einfluss auf
die Anwendungsprogramme geändert werden können. (Bsp.: Serverumzug)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Logische Datenunabhängigkeit</td>
<td>Die globale Struktur der Daten (Verknüpfungen) soll unabhängig von
den Anwendungen organisiert werden. Eine logische Änderung soll die
Anwendungsprogramme nicht beeinflussen.</td>
</tr>
</tbody>
</table>

## 5. DDL, DML und QL

Die **DDL (Datendefinitionssprache)** wird verwendet um Daten im DBS zu
beschreiben, zu ändern oder zu löschen. (CREATE, ALTER, DROP, TRUNCATE,
COMMENT, RENAME) | Datenbankadministrator

Die **DML (Datenmanipulationssprache)** wird verwendet um Daten im DBS
einzufügen, zu aktualisieren, und abzurufen. (SELECT, INSERT, UPDATE,
DELETE) | Anwendungsprogrammierer

Die **QL (Abfragesprache)** wird verwendet um Daten aus dem DBS
abzurufen. (SELECT) | Endnutzer

## 6. DBMS-Fallbeispiele

<table>
<colgroup>
<col style="width: 27%" />
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 6%" />
<col style="width: 15%" />
<col style="width: 10%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Codd’sche Regel</th>
<th>MySQL</th>
<th>Excel</th>
<th>LSF</th>
<th>IBM DB2</th>
<th>iTunes</th>
<th>MS SQLServer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Integration</td>
<td>x</td>
<td></td>
<td>x</td>
<td>x</td>
<td></td>
<td>x</td>
</tr>
<tr class="even">
<td>Operationen</td>
<td>x</td>
<td>x</td>
<td>x</td>
<td>x</td>
<td></td>
<td>x</td>
</tr>
<tr class="odd">
<td>Katalog</td>
<td>x</td>
<td></td>
<td>x</td>
<td>x</td>
<td></td>
<td>x</td>
</tr>
<tr class="even">
<td>Benutzersichten</td>
<td>x</td>
<td>x</td>
<td>x</td>
<td>x</td>
<td>x</td>
<td>x</td>
</tr>
<tr class="odd">
<td>Integritätssicherung</td>
<td>x</td>
<td></td>
<td>x</td>
<td>x</td>
<td></td>
<td>x</td>
</tr>
<tr class="even">
<td>Datenschutz</td>
<td>x</td>
<td></td>
<td>x</td>
<td>x</td>
<td>x</td>
<td>x</td>
</tr>
<tr class="odd">
<td>Transaktionen</td>
<td>x</td>
<td></td>
<td>x</td>
<td>x</td>
<td>x</td>
<td>x</td>
</tr>
<tr class="even">
<td>Synchronisation</td>
<td>X</td>
<td></td>
<td>x</td>
<td>x</td>
<td></td>
<td>x</td>
</tr>
<tr class="odd">
<td>Datensicherung</td>
<td>x</td>
<td>x</td>
<td>x</td>
<td>x</td>
<td></td>
<td>x</td>
</tr>
</tbody>
</table>

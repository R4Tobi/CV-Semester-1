# Datenbanken - Übung7

## Definition

Zwei Attributmengen sind dann voneinander abhängig, wenn ein Wert einen
eindeutigen Wert der anderen vorgibt.

Bsp.:

A: B: A -\> B

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 6%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 8%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th>70</th>
<th>F</th>
<th></th>
<th>F</th>
<th>46</th>
<th></th>
<th>F</th>
<th>70</th>
<th>46</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>71</td>
<td>G</td>
<td></td>
<td>G</td>
<td>47</td>
<td></td>
<td>G</td>
<td>71</td>
<td>47</td>
</tr>
<tr class="even">
<td>72</td>
<td>H</td>
<td></td>
<td>H</td>
<td>48</td>
<td></td>
<td>H</td>
<td>72</td>
<td>48</td>
</tr>
<tr class="odd">
<td>73</td>
<td>I</td>
<td></td>
<td>I</td>
<td>49</td>
<td></td>
<td>I</td>
<td>73</td>
<td>49</td>
</tr>
<tr class="even">
<td>74</td>
<td>J</td>
<td></td>
<td>J</td>
<td>4A</td>
<td></td>
<td>J</td>
<td>74</td>
<td>4A</td>
</tr>
</tbody>
</table>

Über Schlüssel werden Datensätze identifiziert. Mit einem
Primärschlüssel <u>eindeutig</u> (F, G, H, I, J).

Die Funktionale Abhängigkeit {A2, A3} -\> A1 bedeutet, dass die
Kombination von Werten in A2 und A3 eindeutig den Wert in A1 bestimmt,
wenn wir eine Relation erstellen für die das nicht gilt, hat man eine
Lösung.

z.B. r = {(1, 1, 1, x), (2, 2, 2, y), (3, 3, 3, z)}

x, y und z sind ganze Zahlen die A1, A2 und A3 repräsentieren.

## Schlüsselbestimmung

**Einzelattribut-Schlüssel**

- A wäre möglich, da A-\>B und ED -\> A

- B, C, D, E sind keine Kandidaten, da sie nicht alle anderen Attribute
  bestimmen

**Schrittweise hinzufügen**

- AB wäre möglich, weil A-\>B und ED-\>A alle anderen Attribute bestimmt

- BC wäre möglich, da BC-\>E und A-\>B die anderen Attribute bestimmt

- ABC wäre möglich, weil AB, BC möglich sind

- ABCD kann ein Schlüssel sein, weil BC-\>E und ED-\>A, und ABC bereits
  ein Schlüssel ist

- ABCDE (Menge aller Attribute) kann ebenfalls Schlüssel sein

Die möglichen Schlüssel sind also ABCD.

## Schlüsselbestimmung

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 75%" />
</colgroup>
<thead>
<tr class="header">
<th>F -&gt; (CD -&gt; BEF) -&gt; ABC</th>
<th>F ist ein möglicher Schlüssel – damit auch alle Schlüssel die F
enthalten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AD -&gt; BC -&gt; BEF</td>
<td>AD ist ein Möglicher Schlüssel</td>
</tr>
<tr class="even">
<td>AF -&gt; BCCD -&gt; BE</td>
<td>AF ist ein möglicher Schlüssel</td>
</tr>
<tr class="odd">
<td>ABD -&gt; BC -&gt; BEF</td>
<td>ABD ist ein möglicher Schlüssel</td>
</tr>
<tr class="even">
<td>ABF -&gt; BCCDBE</td>
<td>ABF ist ein möglicher Schlüssel</td>
</tr>
<tr class="odd">
<td colspan="2">Alle Schlüssel die F oder AD in sich haben sind
verwendbare Schlüssel (ACDE, ACD, usw.)</td>
</tr>
</tbody>
</table>

## Überführung in Boyce-Codd-Normalform

--

## 5

--

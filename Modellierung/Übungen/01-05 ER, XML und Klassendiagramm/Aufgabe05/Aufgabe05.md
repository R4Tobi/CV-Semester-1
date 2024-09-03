# Übungsaufgabe 5 - Rechnung

Nutzen Sie XML (Version 1.0) um die folgende Rechnung eines Onlinehändlers zu beschreiben:

- Eine Rechnung beinhaltet den Kunden, die Rechnungspositionen und Daten zur Lieferung
- Der Kunde hat eine Kundennummer (1234), einen Namen (Max Mustermann), eine Adresse (Musterstrasse 17, 12345 Musterdorf) und einen Status (Goldkunde)
- Die Rechnungspositionen sind:
- Artikelname (T-Shirt schwarz), Artikelnummer (5), Anzahl (3), Preis in Euro (10)
- Artikelname (T-Shirt blau), Artikelnummer (8), Anzahl (5), Preis in Euro (10)
- Die Lieferung hat ein Bestelldatum (02.01.2034), eine zugesagte Lieferdeadline (09.01.2034) und wird von einem Versanddienstleister (Deutsche Post) realisiert.

## Lösung

```xml
<Rechnung>
    <Kunde>
        <Kundennummer>1234</Kundennummer>
        <Name>Max Mustermann</Name>
        <Adresse>Musterstrasse 17, 12345 Musterdorf</Adresse>
        <Status>Goldkunde</Status>
    </Kunde>
    <Rechnungspositionen>
        <Position>
            <Artikelname>T-Shirt schwarz</Artikelname>
            <Artikelnummer>5</Artikelnummer>
            <Anzahl>3</Anzahl>
            <Preis>10</Preis>
        </Position>
        <Position>
            <Artikelname>T-Shirt blau</Artikelname>
            <Artikelnummer>8</Artikelnummer>
            <Anzahl>5</Anzahl>
            <Preis>10</Preis>
        </Position>
    </Rechnungspositionen>
    <Lieferung>
        <Bestelldatum>02.01.2034</Bestelldatum>
        <ZugesagteLieferdeadline>09.01.2034</ZugesagteLieferdeadline>
        <Versanddienstleister>Deutsche Post</Versanddienstleister>
    </Lieferung>
</Rechnung>
```

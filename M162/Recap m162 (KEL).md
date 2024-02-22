### Wissenstreppe

Die Wissenstreppe beschreibt die Transformation von Daten zu Informationen, Wissen, und schließlich Weisheit. Hier sind die Stufen der Reihe nach, illustriert am Beispiel eines Wechselkurses:

1. **Zeichen/Daten:** Rohdaten oder Fakten, z.B. `1.13`, `EUR`, `USD`.
2. **Informationen:** Kontextualisierte Daten, z.B. "1.13 USD ist der Wechselkurs für 1 EUR am 22.02.2024."
3. **Wissen:** Verarbeitete Informationen, Analyse, z.B. "Der Wechselkurs von EUR zu USD ist im Vergleich zum Vormonat um 0.02 gestiegen."
4. **Verständnis:** Tieferes Einsicht, Ursachen, z.B. "Der Anstieg des Wechselkurses könnte auf eine Stärkung der europäischen Wirtschaft zurückzuführen sein."
5. **Weisheit:** Angewandtes Wissen und Verständnis, Entscheidungen, z.B. "Basierend auf der aktuellen Entwicklung könnte es eine gute Zeit sein, in Euro zu investieren."

### Netzwerk-Beziehungen im logischen Modell

Netzwerk-Beziehungen im logischen Modell werden üblicherweise durch Entitäten und Relationen abgebildet, z.B. mittels ER-Diagrammen (Entity-Relationship-Diagramme), wo Entitäten durch Knoten und die Beziehungen zwischen diesen durch Kanten repräsentiert werden.

### Anomalien in einer Datenbasis

Anomalien in einer Datenbasis beziehen sich auf Inkonsistenzen oder Fehler in den Daten. Es gibt mehrere Arten:

- **Einfügeanomalie:** Schwierigkeiten beim Hinzufügen neuer Daten aufgrund der Struktur der Datenbank.
- **Löschanomalie:** Verlust von Daten über eine Entität beim Löschen von Informationen einer anderen Entität.
- **Änderungsanomalie:** Inkonsistenzen, die durch die Änderung von Daten in einer Datenbank entstehen.

### Redundante Daten

Redundante Daten sind mehrfach vorkommende Daten in einer Datenbank. Sie können zu Inkonsistenzen führen, aber auch zur Verbesserung der Abfrageleistung oder zur Gewährleistung der Datenintegrität durch Redundanz beitragen.

### Datenstrukturierung

Bei der Datenstrukturierung können **Daten** und **Beziehungen** strukturiert werden. Die Strukturierung kann in Kategorien wie **unstrukturiert**, **semi-strukturiert** und **strukturiert** unterteilt werden. In einer Datenbank müssen Daten **strukturiert** sein, um effiziente Abfragen, Speicherung und Analyse zu ermöglichen. Dies umfasst die Definition von Tabellen, Spalten und Datentypen sowie die Beziehungen zwischen den Tabellen.

![Mitarbeitertabelle](https://gitlab.com/ch-tbz-it/Stud/m164/-/raw/main/10_Auftraege_und_Uebungen/00_Start/Recap_Fragen/Tabelle_labelled.png "Mitarbeitertabelle")

1. **Tabellenname**: Der Name der Tabelle in der Datenbank, hier bezeichnet als "Mitarbeiter".

2. **Spalten/Attribute**: Die einzelnen Spalten der Tabelle werden durch diese Linien markiert und repräsentieren die Attribute der Datenbanktabelle. Die Attribute in dieser Tabelle sind "MitarbeiterId", "Vorname", "Nachname", "Alter" und "Abteilungskürzel".

3. **Primärschlüssel (Primary Key)**: Diese Linie könnte darauf hinweisen, dass "MitarbeiterId" als Primärschlüssel dient – ein einzigartiges Identifikationsmerkmal für jeden Datensatz in der Tabelle.

4. **Datensatz/Zeile (Record/Row)**: Diese Linie deutet auf einen einzelnen Datensatz oder eine Zeile in der Tabelle hin. Jeder Datensatz ist eine einzelne Einheit, die Informationen über einen Mitarbeiter enthält.

5. **Fußzeile/Bemerkungsbereich**: Hier könnte eine Fußzeile oder ein Bereich für Bemerkungen oder zusätzliche Informationen über die Tabelle angegeben sein, obwohl dies in der Praxis nicht üblich ist.

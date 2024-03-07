# SQL Grundbefehle und Konzepte

## Datenbanken anzeigen und auswählen

- **Liste aller Datenbanken anzeigen:** `SHOW DATABASES;`
- **Mit einer Datenbank verbinden:** `USE «datenbankname»;`

## Tabellenoperationen

- **Liste aller Tabellen in einer Datenbank anzeigen:** `SHOW TABLES;`
- **Struktur einer Tabelle anzeigen:** `DESCRIBE «tabellenname»;` oder `DESC «tabellenname»;`

## Datenbank und Tabelle erstellen und löschen

- **Neue Datenbank erzeugen:** `CREATE DATABASE «DatenbankName»;`
- **Datenbank löschen:** `DROP DATABASE «DatenbankName»;`
- **Neue Tabelle erzeugen:** `CREATE TABLE «TabellenName» («Spalte1» «Datentyp», «Spalte2» «Datentyp», ...);`
- **Tabelle löschen:** `DROP TABLE «TabellenName»;`

## Erweiterte Befehle

- **Modifier IF (NOT) EXISTS:** Verhindert Fehlermeldungen beim Erstellen oder Löschen einer Datenbank/Tabelle, wenn die Bedingung (nicht) erfüllt ist.
- **Struktur einer Tabelle ändern:** `ALTER TABLE «TabellenName» ...;` (gefolgt von spezifischen Anweisungen wie `ADD COLUMN`, `DROP COLUMN`, `MODIFY COLUMN`, etc.)

## Datentypen und Constraints

- **Integer-Typen in MariaDB/MySQL:** `TINYINT`, `SMALLINT`, `MEDIUMINT`, `INT`, `BIGINT`.
- **Datentyp für einen Primärschlüssel:** Meistens `INT` oder `BIGINT` mit dem Modifier `AUTO_INCREMENT`.
- **Datentyp für einen Fremdschlüssel:** Sollte der gleiche Datentyp sein wie der Primärschlüssel der referenzierten Tabelle.
- **Naming Conventions:** Benennungsregeln für Datenbankobjekte zur Konsistenz und Lesbarkeit.
- **Eigenschaften für automatischen Integer Primärschlüssel:** `INT AUTO_INCREMENT PRIMARY KEY`.
- **Fremdschlüssel definieren:** `FOREIGN KEY («FremdschlüsselSpalte») REFERENCES «Referenztabelle» («PrimärschlüsselSpalte»).`
- **Verhindern von NULL-Werten:** `NOT NULL` in der Spaltendefinition.
- **Standard-Wert für ein Feld definieren:** `DEFAULT '«Standardwert»'`.
- **Eindeutigkeit festlegen:** `UNIQUE` Schlüsselwort in der Spaltendefinition.
- **Für einen längeren Text:** `TEXT`
- **Aktuelle Zeit:** `NOW()`
- **Fremdschlüssel hinzufügen:** `ALTER TABLE «customer» ADD FOREIGN KEY («fk_zip_id») REFERENCES «zip»(«id»);`

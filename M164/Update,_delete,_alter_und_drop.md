# Update,_delete,_alter_und_drop

-- Vervollständigen des Namens für Regisseur Cohen
UPDATE regisseure
SET name = 'Etan Cohen'
WHERE name = 'Cohen';

-- Korrektur der Laufzeit für den Film "Angst"
UPDATE filme
SET dauer = 120
WHERE titel = 'Angst';

-- Umbenennen der Tabelle von "DVD" zu "bluray_sammlung"
RENAME TABLE dvd TO bluray_sammlung;

-- Hinzufügen einer neuen Spalte "Preis"
ALTER TABLE bluray_sammlung
ADD COLUMN Preis DECIMAL(10,2);

-- Entfernen des Films "Angriff auf Rom"
DELETE FROM filme
WHERE titel = 'Angriff auf Rom' AND regisseur = 'Steven Burghofer';

-- Umbenennen der Spalte "filme" zu "kinofilme"
ALTER TABLE filme
RENAME COLUMN filme TO kinofilme;

-- Löschen der Spalte "Nummer"
ALTER TABLE filme
DROP COLUMN Nummer;

-- Löschen der Tabelle, da der Filmverleih geschlossen wurde
DROP TABLE filme;

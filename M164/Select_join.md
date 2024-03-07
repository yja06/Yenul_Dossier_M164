# Select join

```sql

-- a) Geben Sie Name, Postleitzahl und Wohnort aller Kunden aus.
SELECT k.Name, o.Postleitzahl, o.Wohnort
FROM kunden k
INNER JOIN orte o ON k.Ort_ID = o.ID;

-- b) Geben Sie Name und Wohnort aller Kunden aus, die die Postleitzahl 79312 haben.
SELECT k.Name, o.Wohnort
FROM kunden k
INNER JOIN orte o ON k.Ort_ID = o.ID
WHERE o.Postleitzahl = '79312';

-- c) Geben Sie Name und Wohnort aller Kunden aus, die in Emmendingen wohnen.
SELECT k.Name, o.Wohnort
FROM kunden k
INNER JOIN orte o ON k.Ort_ID = o.ID
WHERE o.Wohnort = 'Emmendingen';

-- d) Geben Sie Name, Wohnort und Einwohnerzahl für alle Kunden aus, die in einem Ort mit mehr als 70000 Einwohnern wohnen.
SELECT k.Name, o.Wohnort, o.Einwohnerzahl
FROM kunden k
INNER JOIN orte o ON k.Ort_ID = o.ID
WHERE o.Einwohnerzahl > 70000;

-- e) Geben Sie alle Orte aus, die weniger als 1000000 Einwohner haben.
SELECT o.Wohnort
FROM orte o
WHERE o.Einwohnerzahl < 1000000;

-- f) Geben Sie Kundename und Ortname aus für alle Kunden, die in Orten mit einer Einwohnerzahl zwischen 100.000 und 1.500.000 leben.
SELECT k.Name, o.Wohnort
FROM kunden k
INNER JOIN orte o ON k.Ort_ID = o.ID
WHERE o.Einwohnerzahl BETWEEN 100000 AND 1500000;

-- g) Geben Sie Kundename, Postleitzahl und Ortname aus für alle Kunden, deren Name ein "e" enthält und alle Orte, die ein "u" oder ein "r" enthalten.
SELECT k.Name, o.Postleitzahl, o.Wohnort
FROM kunden k
INNER JOIN orte o ON k.Ort_ID = o.ID
WHERE k.Name LIKE '%e%' AND (o.Wohnort LIKE '%u%' OR o.Wohnort LIKE '%r%');

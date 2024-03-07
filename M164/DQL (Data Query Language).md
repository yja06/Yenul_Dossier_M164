# DQL (Data Query Language)

```sql
-- a. Lassen Sie sich mit SELECT alle Datensätze Ihrer DVD-Sammlung ausgeben.
SELECT * FROM dvd_sammlung;

-- b. Erstellen Sie eine Anweisung, die alle Filmtitel und die jeweils zugehörige Nummer ausgibt.
SELECT nummer, titel FROM filme;

-- c. Erstellen Sie eine Anweisung, die alle Filmtitel und den jeweils zugehörigen Regisseur ausgibt.
SELECT titel, regisseur FROM filme;

-- d. Erstellen Sie eine Liste mit allen Filmen von Quentin Tarantino.
SELECT titel FROM filme WHERE regisseur = 'Quentin Tarantino';

-- e. Erstellen Sie eine Liste mit allen Filmen von Steven Spielberg.
SELECT titel FROM filme WHERE regisseur = 'Steven Spielberg';

-- f. Erstellen Sie eine Liste aller Filme, in denen der Regisseur den Vornamen "Steven" hat.
SELECT titel FROM filme WHERE regisseur LIKE 'Steven%';

-- g. Erstellen Sie eine Liste mit allen Filmen, die länger als 2 Stunden sind.
SELECT titel FROM filme WHERE dauer > 120;

-- h. Erstellen Sie eine Liste mit allen Filmen, die von Tarantino oder von Spielberg gedreht wurden.
SELECT titel FROM filme WHERE regisseur IN ('Quentin Tarantino', 'Steven Spielberg');

-- i. Suchen Sie alle Filme heraus, die von Tarantino gedreht wurden und kürzer als 90 Minuten sind.
SELECT titel FROM filme WHERE regisseur = 'Quentin Tarantino' AND dauer < 90;

-- j. Sie erinnern sich an einen Film, in dessen Titel "Sibirien" vorkam. Suchen Sie ihn.
SELECT titel FROM filme WHERE titel LIKE '%Sibirien%';

-- k. Lassen Sie sich alle Teile von "Das große Rennen" ausgeben.
SELECT titel FROM filme WHERE titel LIKE 'Das große Rennen%';

-- l. Lassen Sie sich eine Liste aller Filme ausgeben, sortiert nach Regisseur.
SELECT titel FROM filme ORDER BY regisseur;

-- m. Lassen Sie sich eine Liste aller Filme ausgeben, sortiert nach Regisseur, dann nach Filmtitel.
SELECT titel, regisseur FROM filme ORDER BY regisseur, titel;

-- n. Lassen Sie sich eine Liste aller Filme von Tarantino ausgeben, die längsten zuerst.
SELECT titel FROM filme WHERE regisseur = 'Quentin Tarantino' ORDER BY dauer DESC;

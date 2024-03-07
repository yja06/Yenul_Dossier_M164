# DDL CREATE -Relations-

```sql

-- Datenbank erstellen, falls sie noch nicht existiert
CREATE DATABASE IF NOT EXISTS DDL;
USE DDL;

-- Tabelle für Fahrer zuerst erstellen, weil andere Tabellen darauf verweisen könnten
CREATE TABLE IF NOT EXISTS tbl_Fahrer (
    ID_Fahrer INT AUTO_INCREMENT PRIMARY KEY,
    Vorname VARCHAR(30) NOT NULL,
    Nachname VARCHAR(30) NOT NULL,
    Geb_datum DATE
);

-- Tabelle für Busse, benötigt Referenz auf Fahrer
CREATE TABLE IF NOT EXISTS tbl_Bus (
    ID_Bus INT AUTO_INCREMENT PRIMARY KEY,
    Bezeichnung VARCHAR(30) NOT NULL,
    Kennzeichen VARCHAR(30) NOT NULL UNIQUE,
    Anzahl_Plätze VARCHAR(30) NOT NULL,
    FK_Fahrer INT,
    CONSTRAINT fk_bus_fahrer FOREIGN KEY (FK_Fahrer)
        REFERENCES tbl_Fahrer (ID_Fahrer)
);

-- Tabelle für Projekte, kann ein Unterprojekt eines anderen Projekts sein
CREATE TABLE IF NOT EXISTS tbl_Projekt (
    ID_Projekt INT AUTO_INCREMENT PRIMARY KEY,
    Bezeichnung VARCHAR(30) NOT NULL,
    Budget DECIMAL(10, 2),
    FK_Unter_Projekt INT,
    CONSTRAINT fk_projekt_unterprojekt FOREIGN KEY (FK_Unter_Projekt)
        REFERENCES tbl_Projekt (ID_Projekt)
);

-- Tabelle für Passagiere, benötigt Referenz auf Busse
CREATE TABLE IF NOT EXISTS tbl_Passagier (
    ID_Passagier INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(30) NOT NULL,
    Platznummer VARCHAR(30),
    FK_Bus INT NOT NULL,
    CONSTRAINT fk_passagier_bus FOREIGN KEY (FK_Bus)
        REFERENCES tbl_Bus (ID_Bus)
);

-- Tabelle für Ausweise, benötigt Referenz auf Passagiere
CREATE TABLE IF NOT EXISTS tbl_Ausweis (
    ID_Ausweis INT AUTO_INCREMENT PRIMARY KEY,
    Nummer VARCHAR(30) NOT NULL,
    Art INT,
    FK_Inhaber INT NOT NULL,
    CONSTRAINT fk_ausweis_inhaber FOREIGN KEY (FK_Inhaber)
        REFERENCES tbl_Passagier (ID_Passagier)
);

-- Erstellen von Indexen für die Fremdschlüssel
CREATE INDEX idx_fk_bus_fahrer ON tbl_Bus (FK_Fahrer);
CREATE INDEX idx_fk_passagier_bus ON tbl_Passagier (FK_Bus);
CREATE INDEX idx_fk_ausweis_inhaber ON tbl_Ausweis (FK_Inhaber);

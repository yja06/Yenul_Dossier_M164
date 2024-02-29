# Tablespace und Tablespace Architecture

Ein Tablespace ist ein Speicherort in einer Datenbank, an dem die tatsächlichen Daten, die den Datenbankobjekten zugrunde liegen, aufbewahrt werden. Er bietet eine Abstraktionsebene zwischen physischen und logischen Daten und dient der Zuweisung von Speicher für alle von der DBMS verwalteten Segmente (wie Tabellendaten und Indizes). Ein Tablespace kann nach seiner Erstellung bei der Erstellung von Datenbanksegmenten namentlich referenziert werden&#8203;``【oaicite:2】``&#8203;.

Oracle unterteilt eine Datenbank in eine oder mehrere logische Speichereinheiten, die als Tablespaces bezeichnet werden. Jeder Tablespace besteht aus einer oder mehreren Dateien, den sogenannten Datafiles, die die Datenobjekte der Datenbank physisch auf einem Datenträger speichern. Oracle speichert Daten logisch in Tablespaces und physisch in den mit den entsprechenden Tablespaces verknüpften Datafiles&#8203;``【oaicite:1】``&#8203;.

PostgreSQL ermöglicht es Datenbankadministratoren, Orte im Dateisystem zu definieren, an denen die Dateien, die Datenbankobjekte darstellen, gespeichert werden können. Durch die Verwendung von Tablespaces kann ein Administrator das Layout der Festplatte einer PostgreSQL-Installation steuern. Tablespaces sind ein integraler Bestandteil des Datenbankclusters und hängen von Metadaten im Hauptdatenverzeichnis ab. Sie können nicht als autonome Datensammlung behandelt werden und sind nicht auf einen anderen Datenbankcluster übertragbar oder individuell sicherbar&#8203;``【oaicite:0】``&#8203;.

# Partition

Eine Partition in Datenbanksystemen ist eine Technik zur Aufteilung von Tabellen oder Indizes in kleinere, leichter zu verwaltende Teile, während die Partitionen für den Benutzer transparent bleiben. Dies kann die Leistung verbessern, die Verwaltung vereinfachen und die Wartung von großen Datensätzen erleichtern.

# Storage Engine in einer Datenbank

Eine Storage Engine ist eine Komponente einer Datenbank, die bestimmt, wie Daten auf der Festplatte gespeichert und abgerufen werden. Sie ist verantwortlich für die Speicherung, das Abfragen und die Manipulation der Daten. Verschiedene Storage Engines bieten unterschiedliche Funktionen, wie z.B. Transaktionsunterstützung, Fehlertoleranz und Optimierungen für bestimmte Abfragetypen oder Datenstrukturen.

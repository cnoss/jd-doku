# Dokumente zur Akkreditierung der F07 Studiengänge

Eine HTML Repräsentation von diesen Dokumenten findet sich unter [https://cghartung.github.io/F07_Studiengaenge/](https://cghartung.github.io/F07_Studiengaenge/)

Zum Anlegen und Pflegen der Dokumente gibt es folgende relevante Verzeichnisse:

```
_selbstbericht-elektrotechnik
_selbstbericht-technische-informatik
_module (in Arbeit)

```

Außerdem das Dokument zum Auflösen der Namenkürzel:

```
_data/people.yml

```

## Selbstberichte (_selbstbericht-STUDIENGANG)

Hier liegen die Markdown Dateien für die Selbstberichte. Für jeden Studiengang gibt es ein eigenes Verzeichnis. Neue Studiengänge müssen in der _config.yml eingetragen werden. Beim lokalen Betrieb muss danach jekyll gestoppt und mit *jekyll serve* neu gestartet werden.

```
---
title: Präambel
aktueller-bearbeiter:
bearbeiterhistorie:
comment:
status: draft
reviewed-von:
---
```

Im Front Matter haben sich die oben abgebildeten Felder bewährt. Davon ist *title* jedoch das einzige Pflichtfeld.

Jede Markdown Datei im Wurzelverzeichnis repräsentiert ein Kapitel. Es können aber auch Unterverzeichnisse angelegt werden, die weitere Markdown Dateien enthalten können. Diese werden dann als Unterkapitel abgebildet.

Inhalte, die in mehreren Selbstberichten gleich sind, können über Symlinks den verschiedenen Selbstberichten zugeordnet werden. 

## Module (_module)

Hier liegen die Markdown Dateien für die Module. Für jedes Modul sollte eine eine Markdown Datei angelegt werden.

```
---
title: Coding Essentials 1
modulverantwortlich: sb, rw
kuerzel: ce-1
studiensemester: 1
sprache: deutsch
kreditpunkte: 10
voraussetzungen-nach-pruefungsordnung: keine
empfohlene-voraussetzungen: 
state: active
---
```

Auch hier muss im Front Matter ein Kürzel für das entsprechende Modul hinterlegt werden. Die Verknüpfung mit einem Kompetenzbereich erfolgt über die "assigned-to" Eigenschaft, die auf das Kürzel des entsprechenden Kompetenzbereichs verweisen muss. Es können mehrere Kompetenzbereiche kommagetrennt aufgeführt werden.

Darüber hinaus sind folgende Daten im Front Matter anzugeben:

| Feld | Funktion |
| --- | --- |
| title | Name des Moduls |
| modulverantwortlich | Namenkürzel des oder der (kommagetrennt) Dozenten. Zur Auflösung der Namenskürzel ist ein entsprechender Eintrag in der "people.yml" im Verzeichnis "_data" notwendig. |
| kuerzel | Kürzel für das Modul |
| studiensemester | In welchem Studiensemester wird das Modul angeboten? |
| sprache | na, was wohl? |
| kreditpunkte | Wie viele Kreditpunkte sind dem Moduk zugeordnet? |
| voraussetzungen-nach-pruefungsordnung | Welche Module müssen abgeschlossen sein, damit dieses Modul belegt werden kann. Bitte hier auch die Namenskürzel der vorausgesetzten Module verwenden. |
| state | Ist das Modul derzeit aktiv (active) oder nicht (passive)? |

Zu den bereits bekannten Daten im Front Matter kommt hier nur das Feld "parent" hinzu. Hierüber wird die Verknüpfung mit dem Modul hergestellt. Wer hätte es gedacht, auch hier wird das Kürzel des Moduls verwendet.

## Fragen

Bei Fragen bitte Anregungen bitte an christian.noss@th-koeln.de wenden.


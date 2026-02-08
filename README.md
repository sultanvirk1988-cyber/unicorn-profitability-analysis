# Unicorn – Profitabilitätsanalyse

Diese Case Study untersucht die Profitabilität des Unicorn-Datensatzes entlang von Zeit, Regionen, Produktkategorien und einzelnen Bestellungen.

Ziel der Analyse ist es zu verstehen, **wodurch der Gesamtgewinn entsteht**:
ob durch eine stabile, breit verteilte Performance – oder durch wenige, stark wirkende Ausreißer.
Der Fokus liegt dabei auf Entscheidungsrelevanz und Nachvollziehbarkeit.

Der Analyseprozess folgt einem klaren, aufeinander aufbauenden Workflow:

**SQL → Spreadsheet-Analyse → Tableau-Dashboard**

---

## Ausgangsfrage

Die Analyse geht unter anderem folgenden übergeordneten Fragen nach:

- Ist der Gewinn über Zeit und Regionen hinweg stabil oder stark volatil?
- Welche Kategorien und Subkategorien treiben den Großteil der Profitabilität?
- Wo entstehen strukturelle Verluste?
- Wie aussagekräftig sind Durchschnittswerte im Vergleich zu Medianen und Verteilungen?
- Welche Muster sind für Management-Entscheidungen tatsächlich relevant?

---

## Datengrundlage

Die Analyse basiert auf dem *Unicorn Orders Datensatz* (Masterschool-Projekt), der Informationen zu folgenden Bereichen enthält:

- Kund:innen, Produkte und Bestellungen  
- Kategorien, Subkategorien und Hersteller  
- Umsatz, Rabatt, Gewinn und Mengen  
- Zeitliche und geografische Merkmale (Bestell- und Versanddaten, Region, Stadt, Bundesstaat)

Für die Spreadsheet-Analyse wurde ein vereinheitlichter CSV-Datensatz verwendet, der sich in der Struktur bewusst von der relationalen Datenbank unterscheidet. Diese Unterschiede wurden analytisch berücksichtigt.

---

## Analyseansatz & Workflow

### 1. SQL-Exploration  
**Ordner:** `/01_sql/`

Die SQL-Analyse diente dazu, das Datenmodell zu verstehen und zentrale Strukturen zu validieren.

Dazu gehörten unter anderem:
- Plausibilitätsprüfungen zum Datenumfang (z. B. Kund:innen, Städte, Produkte)
- Erste Gewinnaggregation nach Jahr, Monat, Stadt und Region
- Analyse von Gewinnkonzentration und Volatilität
- Identifikation besonders profitabler bzw. verlustbringender Segmente
- Überprüfung von Extremwerten bei Mengen und Umsätzen

SQL bildete die analytische Grundlage für alle weiteren Schritte und half dabei, relevante Fragestellungen gezielt zu vertiefen.

---

### 2. Spreadsheet-Analyse  
**Ordner:** `/02_spreadsheet/`

Im nächsten Schritt wurden die SQL-Ergebnisse mithilfe von Spreadsheets vertieft, überprüft und erweitert.

Der Fokus lag auf:
- Berechneten Kennzahlen (z. B. Stückpreise vor Rabatt, Lieferdauer)
- Pivot-Analysen nach Region, Kategorie, Hersteller und Kundensegment
- Analyse von Gewinnverteilungen auf Bestell-Ebene
- Vergleich von Median und Durchschnitt zur Identifikation schiefer Verteilungen
- Klassifikation von Bestellungen (z. B. „High“, „Low“, „Loss“) anhand klar definierter Kriterien
- Einsatz von bedingten Formatierungen zur Mustererkennung

Zusätzlich wurden dynamische Auswertungen (Dropdowns, Filter, Index-Match-Logiken) genutzt, um Analysepfade flexibel nachvollziehbar zu machen.

Diese Phase diente vor allem dazu, **Annahmen zu validieren**, Ausreißer sichtbar zu machen und Erkenntnisse für die Visualisierung vorzubereiten.

---

### 3. Tableau-Analyse & Dashboard  
**Ordner:** `/03_tableau/`

In Tableau wurden die gewonnenen Erkenntnisse zu einer zusammenhängenden, entscheidungsorientierten Geschichte verdichtet.

Der analytische Fokus lag auf:
- Profitabilitätsunterschieden nach Region, Stadt und Kategorie
- Zeitlicher Entwicklung und Volatilität des Gewinns
- Identifikation besonders relevanter Monate und Segmente
- Einordnung von Ausreißern im Kontext der Gesamtverteilung

Das Dashboard:
- kombiniert mehrere Visualisierungen zu einem klaren Analysefluss
- nutzt Filter und Interaktivität gezielt
- ist ohne technische Erklärung verständlich
- richtet sich bewusst an eine **Business- bzw. Management-Perspektive**

Ein Screenshot des Dashboards ist zur schnellen Orientierung enthalten.

---

### 4. Executive Summary  
**Ordner:** `/04_report/`

Die Executive Summary fasst die Analyseergebnisse zusammen und übersetzt sie in klare, entscheidungsrelevante Aussagen.
Der Fokus liegt auf Einordnung, Wirkung und möglichen Implikationen – nicht auf technischer Umsetzung.

---

## Zentrale Erkenntnisse

- Der Gesamtgewinn ist **stark konzentriert** und wird von wenigen Kategorien und Subkategorien getragen.
- Die Kategorie *Technology* generiert den Großteil des Gewinns, während *Furniture* strukturelle Verluste verursacht.
- Der monatliche Gewinn ist volatil: Verluste in einzelnen Monaten werden durch wenige sehr starke Monate kompensiert.
- Die Mehrheit der Bestellungen erzeugt **nur geringe oder nahezu keine Gewinne**.
- Der Median-Gewinn pro Bestellung liegt deutlich unter dem Durchschnitt, was auf stark schiefe Verteilungen und Ausreißer hinweist.

---

## Ergebnisse & Inhalte

- SQL-Abfragen zur Exploration und Aggregation  
- Spreadsheet-Analysen zur Vertiefung, Validierung und Klassifikation  
- Tableau-Dashboard zur Visualisierung zentraler Muster  
- Executive Summary mit Einordnung und Handlungsperspektive  

---

## Reproduzierbarkeit

1. SQL-Logik im Ordner `/01_sql/` einsehen  
2. Spreadsheet-Dateien im Ordner `/02_spreadsheet/` öffnen  
3. Tableau `.twbx` Datei in Tableau Desktop laden  
4. Executive Summary im Ordner `/04_report/` lesen  

---

## Verwendete Tools

- SQL  
- Excel / Google Sheets  
- Tableau  
- GitHub zur Dokumentation und Strukturierung

---

## Autor

Sultan Virk  
Angehender Data Analyst

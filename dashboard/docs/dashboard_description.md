# Dashboard Beschreibung – Verlagerungsmodell Güterverkehr

Das Dashboard visualisiert die multimodalen Verkehrsdaten (Straße, Schiene, Wasserstraße, Wetter, OSM) und zeigt Potenziale zur Verkehrsverlagerung auf.

---

## 1. Ziele des Dashboards

- Darstellung der Verkehrslasten auf Straße, Schiene und Wasserstraße  
- Identifikation von Engpässen und Kapazitätsproblemen  
- Analyse von Zusammenhängen zwischen Verkehr, Wetter und Infrastruktur  
- Unterstützung datenbasierter Entscheidungen zur Verkehrsverlagerung  

---

## 2. Hauptseiten des Dashboards

### 2.1 Übersicht
- Gesamtverkehr Straße (Tages‑, Wochen‑, Monatswerte)
- Vergleich Straße vs. Schiene vs. Wasserstraße
- KPI‑Kacheln (siehe `kpi_definitions.md`)
- Zeitreihen und Trendanalysen

### 2.2 Straßenseite (BASt)
- Verkehrsmengen pro Zählstelle
- Peak‑Zeiten
- Lkw‑Anteil
- Kartenvisualisierung der Zählstellen
- Qualitätskennzeichen

### 2.3 Schienenseite (DB)
- Zugfrequenzen pro Abschnitt
- Verspätungsindikatoren
- Infrastrukturkarte (Bahnhöfe, Strecken)

### 2.4 Wasserstraße (Pegel Online)
- Wasserstände
- Trends
- Pegelkarte

### 2.5 Wetter (DWD)
- Temperatur, Niederschlag, Wind
- Einfluss auf Verkehrsmengen

### 2.6 Infrastruktur (OSM)
- Straßennetz
- Schienennetz
- Erreichbarkeitsanalysen

---

## 3. Interaktive Elemente

- Filter: Datum, Region, Verkehrsträger, Wochentag  
- Drill‑Down: Stunde → Tag → Woche → Monat  
- Karteninteraktionen: Klick auf Zählstelle / Bahnhof / Pegel  

---

## 4. Datenbasis

Die Daten werden aus `data/processed/` geladen und im Power BI Datenmodell verknüpft (siehe `data_model.md`).

---

## 5. Zielgruppe

- Verkehrsplaner  
- Logistikunternehmen  
- Behörden  
- Wissenschaftliche Analysen  

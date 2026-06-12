# Datenmodell – Verlagerungsmodell Güterverkehr

Dieses Dokument beschreibt das Datenmodell, das im Power BI Dashboard verwendet wird.

---

## 1. Überblick

Das Datenmodell besteht aus fünf zentralen Faktentabellen und mehreren Dimensionstabellen:

- **Faktentabellen**
  - Verkehr Straße (BASt)
  - Verkehr Schiene (DB)
  - Wasserstände (Pegel Online)
  - Wetterdaten (DWD)
  - Infrastruktur (OSM)

- **Dimensionstabellen**
  - Datum
  - Uhrzeit
  - Standort (Zählstelle, Bahnhof, Pegel)
  - Region
  - Verkehrsträger

---

## 2. Tabellenstruktur

### 2.1 Faktentabelle: Straße (BASt)

| Spalte | Beschreibung |
|--------|--------------|
| datetime | Zeitstempel |
| zst_id | Zählstelle |
| kfz_total | Gesamtverkehr |
| lkw_anteil | Anteil schwerer Fahrzeuge |
| qualitaet | Qualitätskennzeichen |

### 2.2 Faktentabelle: Schiene (DB)

| Spalte | Beschreibung |
|--------|--------------|
| datetime | Zeitstempel |
| station_id | Bahnhof |
| zugfrequenz | Anzahl Züge |
| verspaetung | Durchschnittliche Verspätung |

### 2.3 Faktentabelle: Wasserstraße

| Spalte | Beschreibung |
|--------|--------------|
| datetime | Zeitstempel |
| pegel_id | Pegel |
| wasserstand | Wasserstand |
| trend | Trendindikator |

### 2.4 Faktentabelle: Wetter

| Spalte | Beschreibung |
|--------|--------------|
| datetime | Zeitstempel |
| station_id | Wetterstation |
| temperatur | Temperatur |
| niederschlag | Niederschlag |
| wind | Windgeschwindigkeit |

---

## 3. Beziehungen

- Datum 1:n Straße  
- Datum 1:n Schiene  
- Datum 1:n Pegel  
- Datum 1:n Wetter  
- Standortdimension verknüpft Zählstellen, Bahnhöfe, Pegel über räumliche Zuordnung  

---

## 4. Ziel des Datenmodells

- Einheitliche Zeitbasis  
- Räumliche Konsistenz  
- Direkte Vergleichbarkeit der Verkehrsträger  
- Grundlage für KPIs und Visualisierungen  


# Preprocessing – Datenaufbereitung im Verlagerungsmodell Güterverkehr

Dieses Dokument beschreibt die Schritte der Datenaufbereitung für alle im Projekt verwendeten Datensätze (Straße, Schiene, Wasserstraße, Wetter, OSM). Ziel ist eine harmonisierte, analysierbare und modellierbare Datenbasis für das Verlagerungsmodell.

---

## 1. Übersicht der Preprocessing‑Pipeline

Die Datenaufbereitung besteht aus fünf zentralen Schritten:

1. **Import & Standardisierung**
2. **Bereinigung & Qualitätskontrolle**
3. **Transformation & Harmonisierung**
4. **Feature Engineering**
5. **Export in die Modell‑ und Dashboard‑Struktur**

Diese Schritte werden für jeden Datensatz individuell durchgeführt und anschließend zusammengeführt.

---

## 2. Preprocessing der BASt‑Straßendaten

### 2.1 Import
- Einlesen der Rohdaten (Richtungsaggregierte Rohdaten 2025)
- Einlesen der Metadaten (Zählstelleninformationen)
- Zusammenführen über `Zst`

### 2.2 Bereinigung
- Entfernen unplausibler Werte (`K_* = d`)
- Ersetzen geschätzter Werte (`K_* = c`) durch Interpolation (optional)
- Konvertieren von Datum (`YYMMDD`) in `datetime`
- Entfernen leerer Fahrtrichtungen

### 2.3 Transformation
- Aggregation auf:
  - Stundenebene
  - Tagesebene
  - Wochenebene
- Berechnung von Gesamtverkehr:
  - `KFZ_total = KFZ_R1 + KFZ_R2`
- Harmonisierung der Spaltennamen (snake_case)

### 2.4 Feature Engineering
- Verkehrsklassen (leicht, mittel, schwer)
- Tageszeitkategorien (Peak, Off‑Peak)
- Wochentagskategorien (Werktag, Wochenende)
- Rolling Averages (3h, 24h)

---

## 3. Preprocessing der DB‑Schienendaten

### 3.1 Import
- Betriebsstellenverzeichnis
- Zugbewegungen / Verspätungsdaten (falls genutzt)

### 3.2 Bereinigung
- Entfernen fehlerhafter Koordinaten
- Vereinheitlichung der Stationsnamen
- Entfernen von Duplikaten

### 3.3 Transformation
- Zeitstempel in `datetime`
- Mapping auf Streckenabschnitte
- Aggregation auf:
  - Stunden
  - Tage

### 3.4 Feature Engineering
- Zugfrequenz pro Abschnitt
- Durchschnittliche Verspätung
- Belastungsindikatoren (z. B. Züge pro Stunde)

---

## 4. Preprocessing der Pegel‑Online‑Daten (Wasserstraße)

### 4.1 Import
- Pegelstände (API oder CSV)

### 4.2 Bereinigung
- Entfernen fehlender Werte
- Trendbereinigung (optional)
- Harmonisierung der Pegelnamen

### 4.3 Transformation
- Zeitstempel vereinheitlichen
- Aggregation auf Stunden/Tage

### 4.4 Feature Engineering
- Wasserstandskategorien (niedrig / normal / hoch)
- Trendindikatoren

---

## 5. Preprocessing der DWD‑Wetterdaten

### 5.1 Import
- Temperatur, Niederschlag, Wind, Sonnenscheindauer

### 5.2 Bereinigung
- Entfernen fehlerhafter Messwerte
- Interpolation fehlender Zeitpunkte

### 5.3 Transformation
- Harmonisierung der Stations‑IDs
- Mapping auf nächstgelegene Zählstelle (Haversine‑Distanz)

### 5.4 Feature Engineering
- Wetterkategorien (trocken, nass, extrem)
- Temperaturbänder
- Windstärke‑Klassen

---

## 6. Preprocessing der OSM‑Netzwerkdaten

### 6.1 Import
- Straßennetz (highway)
- Schien

# Projektübersicht

Dieses Dokument beschreibt die Gesamtarchitektur des Projekts „Verlagerungsmodell Güterverkehr“.

---

## 1. Datenquellen

Das Projekt integriert Daten aus fünf Bereichen:

- Straße (BASt)
- Schiene (DB Open Data)
- Wasserstraße (Pegel Online)
- Wetter (DWD)
- Infrastruktur (OSM)

---

## 2. Datenpipeline

1. **Datenimport**  
   Laden der Rohdaten aus verschiedenen Quellen.

2. **Preprocessing**  
   - Bereinigung  
   - Harmonisierung  
   - Zeitstempel  
   - Geodatenverarbeitung  

3. **Feature Engineering**  
   - Verkehrsklassen  
   - Aggregationen  
   - Wetter‑Features  
   - Infrastruktur‑Features  

4. **Modellierung**  
   - Explorative Analysen  
   - Korrelationen  
   - Regressionsmodelle  
   - Szenarien  

5. **Dashboard**  
   Visualisierung der Ergebnisse in Power BI.

---

## 3. Ordnerstruktur

```plaintext
docs/
    data/          # Data Dictionaries
    project/       # Architektur, Preprocessing, Modellierung
dashboard/
    powerbi/       # PBIX Datei
    docs/          # Dashboard Dokumentation
data/
    raw/           # Originaldaten
    processed/     # Bereinigte Daten
notebooks/
    01_data_exploration.ipynb
    02_preprocessing.ipynb
src/
    data/          # Loader
    preprocessing/
    modeling/


# verlagerungsmodell-gueterverkehr
Open-Data-Projekt zur Analyse von Verkehrsverlagerungen im multimodalen Güterverkehr (Straße/Schiene/Wasserstraße)

Dieses Projekt untersucht, wie sich der Güterverkehr in Deutschland zwischen Straße, Schiene und Wasserstraße verlagert, wenn Störungen auftreten (z.B. Baustellen, Hochwasser, Streckensperrungen)

# Ziele:
- Aufbau eines multimodalen Verkehrsnetzmodells
- Analyse heterogener Open-Data-Quellen
- Modellierung von Verkehrsverlagerungen
- Entwicklung eines ML-Modells zur Prognose
- Simulation von Störungsszenarien
- Interaktive Visualisierung (Dashboard)

# Datenquellen:
- BASt Verkehrsmengendaten (Straße)
  Die Rohdaten stammen aus den „Richtungsaggregierten Rohdaten der   automatischen 
  Dauerzählstellen“ der BASt (BAB (Autobahnen) / Jahr   2025).
  Download: https://www.bast.de/DE/Publikationen/Daten/Verkehrstechnik/DZ-Richtung.html
- Deutsche Bahn Open Data (Schiene)
- Pegel Online (Wasserstraße)
- DWD Wetterdaten
- OpenStreetMap / OpenRailwayMap

## 📘 Data Dictionary

Die Beschreibung aller Spalten der BASt‑Rohdaten und Metadaten befindet sich im Ordner [`docs/`](docs/).

- [Data Dictionary – Rohdaten](docs/data_dictionary_raw.md)
- [Data Dictionary – Metadaten](docs/data_dictionary_meta.md)

# Technologien:
- Python, Pandas, GeoPandas
- scikit-learn, PyTorch
- Streamlit Dashboard
- GitHub Actions

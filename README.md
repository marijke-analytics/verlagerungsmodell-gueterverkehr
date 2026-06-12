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

## 🚚 Datenquellen

Das Projekt nutzt mehrere offene Datenquellen:

- **BASt Verkehrsmengendaten (Straße)**  
  Richtungsaggregierte Rohdaten der automatischen Dauerzählstellen (Autobahnen, 2025).  
  Quelle: https://www.bast.de/DE/Publikationen/Daten/Verkehrstechnik/DZ-Richtung.html

- **Deutsche Bahn Open Data (Schiene)**  
  Betriebsstellen, Zugbewegungen, Verspätungsdaten.

- **Pegel Online (Wasserstraße)**  
  Wasserstände, Trends, Pegelstandorte.

- **DWD Wetterdaten**  
  Temperatur, Niederschlag, Wind, Sonnenscheindauer.

- **OpenStreetMap / OpenRailwayMap**  
  Straßennetz, Schienennetz, Infrastrukturattribute.

---

## 📘 Dokumentation

Alle Data Dictionaries und weiterführenden Dokumente befinden sich im Ordner [`docs/`](docs/).

### Datensätze
- [BASt Rohdaten 2025](docs/data/bast_raw_2025.md)
- [BASt Metadaten 2025](docs/data/bast_meta_2025.md)
- [Deutsche Bahn](docs/data/db_rail.md)
- [Pegel Online](docs/data/pegel_online.md)
- [DWD Wetter](docs/data/dwd_weather.md)
- [OSM Netzwerkdaten](docs/data/osm_network.md)

### Projektstruktur
- [Projektarchitektur](docs/project/architecture.md)
- [Preprocessing](docs/project/preprocessing.md)
- [Modellierung](docs/project/modeling.md)

---

## 📊 Dashboard

Das interaktive Dashboard (Power BI) befindet sich im Ordner [`dashboard/`](dashboard/).

Dokumentation:
- [Dashboard Beschreibung](dashboard/docs/dashboard_description.md)
- [KPI Definitionen](dashboard/docs/kpi_definitions.md)
- [Datenmodell](dashboard/docs/data_model.md)

---
##  Technologien:
- Python, Pandas, GeoPandas
- scikit-learn, PyTorch
- Streamlit Dashboard
- GitHub Actions

## 📁 Repository-Struktur

```plaintext
verlagerungsmodell_gueterverkehr/
│
├── data/                # Roh-, Zwischen- und verarbeitete Daten
├── notebooks/           # Jupyter Notebooks
├── src/                 # Python-Module (Daten, Preprocessing, Modellierung)
├── dashboard/           # Power BI Dashboard + Dokumentation
└── docs/                # Data Dictionaries + Projektbeschreibung



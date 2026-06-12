# verlagerungsmodell-gueterverkehr
Open-Data-Projekt zur Analyse von Verkehrsverlagerungen im multimodalen Güterverkehr (Straße/Schiene/Wasserstraße)

Dieses Projekt untersucht, wie sich der Güterverkehr in Deutschland zwischen Straße, Schiene und Wasserstraße verlagert, wenn Störungen auftreten (z.B. Baustellen, Hochwasser, Streckensperrungen)

Ziele:
- Aufbau eines multimodalen Verkehrsnetzmodells
- Analyse heterogener Open-Data-Quellen
- Modellierung von Verkehrsverlagerungen
- Entwicklung eines ML-Modells zur Prognose
- Simulation von Störungsszenarien
- Interaktive Visualisierung (Dashboard)

Datenquellen:
- BASt Verkehrsmengendaten (Straße)
  (https://www.bast.de/DE/Publikationen/Daten/Verkehrstechnik/DZ-Richtung.html?nn=427910) - Jahr: 2025
- Deutsche Bahn Open Data (Schiene)
- Pegel Online (Wasserstraße)
- DWD Wetterdaten
- OpenStreetMap / OpenRailwayMap

Technologien:
- Python, Pandas, GeoPandas
- scikit-learn, PyTorch
- Streamlit Dashboard
- GitHub Actions

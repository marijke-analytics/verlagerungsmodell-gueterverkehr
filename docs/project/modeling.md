# Modellierung – Verlagerungsmodell Güterverkehr

Dieses Dokument beschreibt die Modellierungsansätze, die im Projekt verwendet werden.

---

## 1. Ziel der Modellierung

- Identifikation von Einflussfaktoren auf Verkehrsmengen  
- Analyse von Zusammenhängen zwischen Verkehr, Wetter und Infrastruktur  
- Entwicklung eines Modells zur Abschätzung von Verlagerungspotenzialen  

---

## 2. Explorative Modellierung

### 2.1 Korrelationsanalysen
- Verkehr ↔ Wetter
- Verkehr ↔ Infrastruktur
- Verkehr ↔ Tageszeit / Wochentag

### 2.2 PCA (Principal Component Analysis)
- Reduktion der Dimensionalität
- Identifikation dominanter Einflussgrößen

---

## 3. Prädiktive Modellierung

### 3.1 Regressionsmodelle
- Lineare Regression
- Random Forest Regression
- Gradient Boosting

### 3.2 Zielvariablen
- Gesamtverkehr
- Lkw‑Anteil
- Zugfrequenz
- Wasserstand

---

## 4. Szenarienmodellierung

### 4.1 Wetter‑Szenarien
- Starkregen
- Hitze
- Sturm

### 4.2 Infrastruktur‑Szenarien
- Ausbau Schiene
- Engpass Straße
- Niedriger Wasserstand

---

## 5. Validierung

- Train/Test‑Split  
- Cross‑Validation  
- Fehlermaße: RMSE, MAE, R²  

---

## 6. Output der Modellierung

- Prognosen für Verkehrsmengen  
- Verlagerungspotenziale  
- Input für das Dashboard  



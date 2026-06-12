# KPI Definitionen – Verlagerungsmodell Güterverkehr

Dieses Dokument beschreibt alle im Dashboard verwendeten KPIs.

---

## 1. KPIs Straße (BASt)

### 1.1 Gesamtverkehr
**Definition:** Summe aller Fahrzeuge pro Zeitintervall  
**Formel:** `KFZ_R1 + KFZ_R2`

### 1.2 Lkw‑Anteil
**Definition:** Anteil schwerer Fahrzeuge am Gesamtverkehr  
**Formel:** `(LoA + Lzg + Sat + Son) / KFZ_total`

### 1.3 Peak‑Stunde
**Definition:** Stunde mit höchstem Verkehrsaufkommen  
**Formel:** `MAX(KFZ_total)`

---

## 2. KPIs Schiene (DB)

### 2.1 Zugfrequenz
**Definition:** Anzahl Züge pro Stunde  
**Formel:** `COUNT(train_id)`

### 2.2 Durchschnittliche Verspätung
**Definition:** Mittelwert aller Verspätungen  
**Formel:** `AVG(delay)`

---

## 3. KPIs Wasserstraße (Pegel Online)

### 3.1 Wasserstandskategorie
**Definition:** Klassifikation nach Pegelwert  
**Kategorien:** niedrig / normal / hoch

### 3.2 Trendindikator
**Definition:** Veränderung des Wasserstands  
**Formel:** `value(t) - value(t-1)`

---

## 4. KPIs Wetter (DWD)

### 4.1 Niederschlagsintensität
**Definition:** Niederschlag pro Stunde  
**Formel:** `RR`

### 4.2 Temperaturband
**Definition:** Klassifikation in Temperaturzonen  
**Bänder:** kalt / mild / warm / heiß

---

## 5. Multimodale KPIs

### 5.1 Verlagerungspotenzial
**Definition:** Differenz zwischen Straßenlast und Schienenkapazität  
**Formel:** `KFZ_total - zugkapazitaet`

### 5.2 Infrastruktur‑Erreichbarkeit
**Definition:** Distanz zur nächsten Schiene / Wasserstraße  
**Formel:** Haversine‑Distanz  


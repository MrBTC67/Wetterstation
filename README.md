# Wetterstation Kirchheide

Ein modernes, webbasiertes Dashboard zur Echtzeit-Visualisierung von Wetterdaten. Die Anwendung verarbeitet Daten einer Wetterstation (z. B. via MicroPython/ESP32) aus einer Firebase Realtime Database und stellt diese interaktiv dar.

## Features

### 🌡️ Echtzeit-Messwerte
* **Temperatur & Luftfeuchte:** Anzeige der aktuellen Werte sowie der Min/Max-Temperaturen des gewählten Zeitraums.
* **Frost-Warnung:** Ein dynamischer Frost-Alarm (pulsierendes Icon) aktiviert sich automatisch bei Temperaturen $\le 3°C$.
* **Taupunkt-Berechnung:** Automatische Berechnung des Taupunkts zur Bestimmung der Kondensationsgefahr.

### 📈 Interaktive Diagramme (Chart.js)
* **Dynamische Verläufe:** Visualisierung von Temperatur, Helligkeit (Lux) und Niederschlag.
* **Intelligente Farbgebung:** * Temperatur-Graphen ändern ihre Farbe je nach Bereich (von Blau/Violett bei Frost bis Rot bei Hitze).
    * Helligkeits-Graphen markieren sonnige Abschnitte farblich.
* **Zeitraum-Steuerung:** Jedes Diagramm kann individuell auf **4h, 12h, 24h oder 7 Tage** umgeschaltet werden.

### 🌧️ Niederschlag & Sonne
* **Regen-Statistik:** Direkte Auswertung der Regenmenge pro Tag, Monat und Jahr ($l/m²$).
* **Sonnenstunden:** Berechnung der täglichen, monatlichen und jährlichen Sonnenstunden basierend auf einem Helligkeits-Schwellenwert.

### 🔮 Luftdruck & Prognose
* **Barometer-Trend:** Anzeige des aktuellen Luftdrucks ($hPa$) und der Änderungsrate pro Stunde.
* **Wetter-Trend:** Lokale Kurzfrist-Prognose (Beständig, Heiter oder Regen/Wind) basierend auf der Luftdruck-Tendenz.

## Technische Details

* **Frontend:** HTML5, CSS3 (Modernes Glassmorphism-Design), JavaScript (ES6).
* **Datenquelle:** Firebase Realtime Database Integration.
* **Bibliotheken:** [Chart.js](https://www.chartjs.org/) für die Datenvisualisierung.
* **Aktualisierung:** Automatischer Datenabgleich alle 60 Sekunden ohne Seiten-Refresh.
* **Responsive:** Optimiert für Desktop und mobile Endgeräte (Smartphones/Tablets).

## Installation

1. Kopiere die `index.html` auf deinen Webserver oder lokal auf deinen Rechner.
2. Stelle sicher, dass die Firebase-URL im `<script>`-Bereich korrekt auf deine Datenbank verweist.
3. Öffne die Datei in einem modernen Webbrowser.

---
*Projekt von Klaus – Stand April 2026*

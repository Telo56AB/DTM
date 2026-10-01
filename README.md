# Visualisierung von Geodaten (DTM)

**Berliner Hochschule für Technik · SoSe 2026**  
**Aleksandr Bondarchuk**

In diesem Repository sind die Ergebnisse der einzelnen Übungsprojekte aus dem Modul *Visualisierung von Geodaten* zusammengefasst.

---

## EP.01 | Choroplethenkarten – Bevölkerungsverteilung in Berlin

### Umsetzung
Die Berliner Bevölkerungsdaten werden in mehreren Choroplethenkarten gegenübergestellt. Gezeigt werden absolute Bevölkerungszahlen sowie Bevölkerungsdichten mit unterschiedlichen Klassifikationen wie Jenks, Quantilen und gleichen Intervallen. Dadurch wird sichtbar, wie stark Bezugsgröße und Klasseneinteilung das Kartenbild beeinflussen.

### Kurzbewertung
Choroplethenkarten ermöglichen einen schnellen räumlichen Vergleich. Gleichzeitig können Flächengröße und gewählte Klassengrenzen die Wahrnehmung der Verteilung deutlich verändern.

![EP01](assets/EP01_Bevoelkerung_Berlin.png)

---

## EP.02 | Gitterchoroplethenkarten – Kirschbäume in Berlin

### Umsetzung
Die Standorte der Berliner Kirschbäume wurden auf ein regelmäßiges Hexagongitter mit 500 m Seitenlänge aggregiert. Die Anzahl der Bäume pro Hexagon wird durch eine abgestufte Rotfärbung dargestellt.

### Kurzbewertung
Das regelmäßige Gitter macht räumliche Konzentrationen unabhängig von administrativen Grenzen gut vergleichbar. Das Ergebnis hängt jedoch von Größe und Lage des Gitters ab.

![EP02](assets/EP02_Kirschbaeume_Hexagon.png)

---

## EP.03 | Punktrasterkarten – Kirschbäume in Berlin

### Umsetzung
Für die zweite Darstellung der Kirschbaumdaten wurden die zuvor aggregierten Werte nicht mehr als gefüllte Gitterflächen, sondern mit Blütensymbolen dargestellt. Die Abstufung von Weiß bis Violett hebt Bereiche mit unterschiedlichen Konzentrationen hervor.

### Kurzbewertung
Punktsymbole vermitteln Verteilungen sehr anschaulich und lassen sich gestalterisch flexibel einsetzen. Bei vielen Symbolen kann die Karte jedoch schnell unruhig wirken.

![EP03](assets/EP03_Kirschbaeume_Punktraster.png)

---

## EP.04 | Value-by-Alpha Mapping – Parlamentswahl in Ungarn

### Umsetzung
Die Ergebnisse der ungarischen Parlamentswahl werden für Fidesz und Tisza nach Wahlkreisen dargestellt. Die große Karte kombiniert die Richtung und Stärke des Stimmenvorsprungs, während zwei zusätzliche Choroplethenkarten die Stimmenanteile der beiden Parteien getrennt zeigen.

### Kurzbewertung
Value-by-Alpha-Darstellungen können mehrere Informationen in einer Karte verbinden. Sehr schwache oder ähnliche Farbabstufungen sind allerdings schwieriger zu unterscheiden.

![EP04](assets/EP04_Ungarn_ValueByAlpha.png)

---

## EP.05 | Ursprung–Ziel-Karte – Outgoing Studierende der BHT

### Umsetzung
Die Karte zeigt internationale Hochschulbeziehungen der BHT für Outgoing-Studierende im Jahr 2024. Berlin bildet den Ursprung; die Partnerhochschulen werden über Verbindungslinien angebunden. Linienstärke und Farbe zeigen die Zahl der Studierenden, auch Verbindungen mit dem Wert 0 bleiben sichtbar. Die Darstellung nutzt eine auf Berlin zentrierte orthographische Projektion.

### Kurzbewertung
Ursprung–Ziel-Karten machen Verbindungen und deren Stärke schnell verständlich. Bei vielen Zielen können sich Linien überlagern, außerdem werden Gebiete am Rand einer orthographischen Projektion stärker verzerrt.

![EP05](assets/EP05_Ursprung_Ziel_BHT.png)

---

## EP.06 | Tilemaps – Digitale Höhenmodelle

### Berlin
Ein digitales Höhenmodell von Berlin wurde auf regelmäßige Rasterzellen reduziert. Die Farbskala von Grün über Gelb bis Orange zeigt unterschiedliche Höhen und macht größere Reliefstrukturen schnell sichtbar.

![EP06 Berlin](assets/EP06_Berlin_Tilemap.png)

### Deutschland
Für die Deutschlandkarte wurden Höhenwerte eines digitalen Geländemodells auf regelmäßige Kacheln übertragen und im Lego-Stil visualisiert. Die vereinfachte Darstellung hebt großräumige Höhenunterschiede hervor, reduziert dabei aber lokale Details.

![EP06 Deutschland](assets/EP06_Deutschland_Tilemap.png)

---

## EP.07 | Animation in QGIS – Geminiden über Dänemark

### Umsetzung
Die Animation zeigt den Geminiden-Meteorschauer über Dänemark am 13.12.2025 von 20:00 bis 23:59 UTC. Die Meteore werden zeitlich gesteuert und minutengenau eingeblendet, sodass ihre räumliche und zeitliche Verteilung nachvollziehbar wird.

### Kurzbewertung
Animationen eignen sich sehr gut für zeitabhängige Ereignisse. Einzelne Zeitpunkte lassen sich jedoch schlechter direkt miteinander vergleichen als bei mehreren statischen Karten.

![EP07 Standbild](assets/EP07_Geminiden_Daenemark_Standbild.png)

![EP07 Animation](assets/EP07_Geminiden_Daenemark.gif)

---

## EP.08 | Mesh-Daten – Windgeschwindigkeit über Europa

### Umsetzung
Die Animation zeigt die Entwicklung der Windgeschwindigkeit über Europa vom 21. bis 31. Oktober 2025. Im Mittelpunkt steht die räumliche Entwicklung starker Windfelder während des Sturms Benjamin. Stromlinien machen Strömungsrichtung und Veränderungen der Windfelder über mehrere Tage sichtbar.

### Kurzbewertung
Die animierte Darstellung vermittelt die Dynamik eines Wetterereignisses besonders anschaulich. Für das genaue Ablesen einzelner Messwerte ist sie dagegen weniger geeignet als eine klassische quantitative Karte.

![EP08 Animation](assets/EP08_Wind_Europa.gif)

---

## EP.09 | 2,5D- und 3D-Gebäudemodelle

### 2,5D – Jena
Für Jena wurde ein offizieller LoD1-Gebäudedatensatz des Thüringer Landesamtes für Bodenmanagement und Geoinformation verwendet. Die Gebäude werden anhand der im Datensatz enthaltenen `measuredHeight` extrudiert. So entsteht eine räumliche Darstellung auf Basis amtlicher Gebäudehöhen.

![EP09 2.5D Jena](assets/EP09_Jena_2_5D.png)

### 3D – Chemnitz Hauptbahnhof
Für das Umfeld des Chemnitzer Hauptbahnhofs wurde ein offizieller LoD2-Datensatz von GeoSN verwendet. Die Darstellung nutzt die vorhandenen 3D-Geometrien mit ihren Z-Koordinaten; Dach-, Wand- und Bodenflächen wurden für eine bessere Lesbarkeit getrennt symbolisiert.

![EP09 3D Chemnitz](assets/EP09_Chemnitz_3D.png)

### Kurzbewertung
2,5D-Modelle sind vergleichsweise einfach und ressourcenschonend, vereinfachen aber die Gebäudeform. LoD2-Modelle zeigen reale Dach- und Wandgeometrien deutlich genauer, benötigen dafür jedoch komplexere Daten und mehr Rechenleistung.

---

**Software:** QGIS 3.40.11 Bratislava

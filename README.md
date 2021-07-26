# Physical Computing Endabgabe

Hier das Repo zu meiner Endabgabe im Seminar Physical Computing bei Peter Ehses.

##### Jannis Steinhauer | Sommersemester 21 | Intermedia Design

<br>

## About

Ziel dieses Projektes ist es, mit Hilfe des Mikrocontrollers _ESP32_, ein LED-Panel zu steuern, um einen Lauftext wiederzugeben.
Da das ESP32 mit einem Wlan-Chip ausgestattet ist, wird die Apparatur mit Hilfe eines Akkus versorgt, um sie gegebenenfalls portabel und Remote-Steuerbar zu machen.
Das ganze Konstrukt wird dann in einer 3D-gedruckten Box untergebracht.

![##](##)
![##](##)

<br>

## Step 1

### Komponenten

##### Folgende Komponenten werden für das Projekt benötigt:

* 1x [ESP32 NodeMCU](https://www.az-delivery.de/products/esp32-developmentboard)
* 1x [MAX7219 LED-Panel 4 in 1](https://www.amazon.de/AZDelivery-MAX7219-8x32-Parent/dp/B07Z95ZTQN)
* 1x [Battery Expansion Shield, 18650](https://www.amazon.de/gp/product/B086W7326Q/ref=ppx_yo_dt_b_asin_title_o07_s00?ie=UTF8&psc=1)
* 1x [18650 Li-ion Akku](https://www.akkuteile.de/lithium-ionen-akkus/18650/samsung/samsung-inr18650-20s-2000mah-max-30a-konstant-3-6v-3-7v-li-ion-akku_100684)
* 1x Doppelseitiges PCB
* 2x PCB Mount
* 1x Pin Head Strip 
* 9x Kabel
* 2x Schrumpfschlauch
* Etwas Isolierband
* Schmirgelpapier (120er Körnung)
* Sprühfarbe nach Wahl

_[(PCB-Komponenten im Set)](https://www.amazon.de/-/en/dp/B08TMMZPWT/ref=sr_1_5?dchild=1&keywords=perfboard&qid=1627310477&sr=8-5)_

### Software

##### Folgende Software wird im Projekt genutzt:

* PlattformIO IDE
* MD_Parola-Libary
* MD_MAX72XX-Libary
* Rhino7 (CAD)
* PrusaSlicer

### Tools

##### Folgende Tools werden im Projekt verwendet:

* Lötkolben und Lötzinn
* 3D-Drucker
* Heisklebepistole
* Schleifpaper
* Feile

<br>

## Step 2 INCOMPLETE

### Schaltplan und Zusammenbau der Hardware

##### Der Schaltplan hat folgendes Layout:

![_##_](##)

_Bitte löten Sie die Kabel wie auf dem Schaltplan beschrieben._


##### Zusammenbau:

* Schritt 1: Löten Sie die 2 PCB Mounts wie auf dem Bild gezeigt
* Schritt 2: Löten Sie die Kabel wie auf dem Bild auf das PCB
* Schritt 3: Demontieren Sie das erste LED-Panel von der Platine und entfernen Sie den Pinstecker
* Schritt 4: Löten Sie die Pins im 90° Winkel zur Platine wie auf dem Bild gezeigt
* Schritt 5: Löten Sie die Pins am 5V und GND Pol des Battery Shields (siehe Bild)
* Schritt 6: Stecken Sie das ESP32 auf das PCB Mount
* Schritt 7: Verbinden Sie alle Kabel wie im Code gezeigt. (siehe ESP32 Pinout)
* Schritt 8: Verbinden Sie alle Komponenten mit Kabeln
* Schritt 9: Legen sie den Li-ion Akku in das Battery Shield <br> **WICHTIG: Achten Sie auf die richtige Ausrichtung des Akkus (+ zu + und - zu -)**

<br>

## Step 3

### Code

##### In diesem Repository befinden sich alle benötigten Dateien um den Code-Teil des Projektes zu realisieren.

[Download Code als zip-Datei ##](##)

_Sidenotes_: 
* Alle Dateien des Repositories müssen in einem Ordner lokal gespeichert werden, die Dateistruktur darf nicht verändert werden.
* Nutzen Sie einen Code-Editor wie beispielsweise [Visual Studio Code](https://code.visualstudio.com/) (VSC) um den Code zu editieren.
* Nutzen Sie die IDE von PlattformIO, welche in VSC installiert werden kann (Plugin), um den Code auf den ESP32 zu hochzuladen.
* Sollten Sie Probleme beim Einrichten von PlattformIO in VSC haben, schauen Sie in die [Dokumentation](https://docs.platformio.org/en/latest/integration/ide/vscode.html).
* **Die einzige Datei die verändert werden sollte ist die _main.cpp_ im _src_ - Ordner**

<br>

## Step 4

### 3D-Modell

##### Rhino7

Das [Casing wurde als 3D-Modell in Rhino7 erstellt](https://drive.google.com/file/d/1GuevXauV8vqbjhybcov0RX2tvitX1TXp/view?usp=sharing) und jeweils als [Case-Bottom](https://drive.google.com/file/d/1lbmdixJKzBxGtuH2gYP01l1wQrOFi1sH/view?usp=sharing) und [Case-Top](https://drive.google.com/file/d/1oV4DrCb4L1Zor5Irk_gMIY47h2J9fne2/view?usp=sharing) im .stl-Format exportiert. <br>
_Alle Dateien können heruntergeladen und in den entsprechenden Programmen modifiziert werden._

##### PrusaSlicer

Casing-Bottom und Casing-Top werden anschließend in PrusaSlicer importiert, um einen 3D-druckbares Modell zu generieren. Für den Ender 3 Pro 3D-Drucker ist bereits eine [fertiger G-Code](https://drive.google.com/file/d/1KjzhNtuQ0tgyJUDDB1J4HIN_AcjvYdh_/view?usp=sharing) angelegt. <br>
_Um aus den .stl-Dateien einen G-Code für einen anderen 3D-Drucker zu generieren, schauen Sie in die [Dokumentation von PrusaSlicer](https://github.com/prusa3d/PrusaSlicer)_

<br>

## Step 5

### Finish

##### Zusammenbau der Komponenten

Das 3D-gedruckte Casing kann jetzt mit 120er Körnung Schmirgelpapier von Druckfehlern befreit werden, danach kann die angeraut und dann mit Sprühfarbe eingefärbt werden.
Legen Sie nach dem Trocknen das LED-Panel in die Halterung und fixieren Sie das Panel mit etwas Isolierband.
Richten Sie die Komponenten anschließend auf dem Boden des Casings aus, dass Sie passen und isolieren Sie den Akku von angrenzender Elektronik mit Isolierband. Kleben Sie anschließend die Komponenten auf dem Boden des Casings mit Hilfe der Heißklebepistole fest.

<br>

# Misc

### Verwendete Tutorials Übersicht

[Text Scrolling Display | MAX7219 Dot Matrix 4-in-1| Arduino](https://www.youtube.com/watch?v=lcrQet0ga-k)

### Reflektion der Ziele

##### These

Als Webentwickler macht mir coden Spaß, zudem bin ich relativ technikbegeistert und neugierig wie Technik generell funktioniert. In meinem Projekt wollte erste Berührungspunkte mit dem Thema Microcontroller und elektronischen Komponenten sammeln, um herauszufinden, ob mir dieses Gebiet gefällt und ich mich weiter in diese Richtung entwickeln will. Außerdem wollte ich ein besseres Verständnis dafür entwickeln wie Technik von Grund auf funktioniert.

##### Fazit

Ich konnte definitiv ein besseres Verständnis dafür bekommen, wie Technik aufgebaut ist und funktioniert. Microcontroller finde ich sehr spannend und ich kann mir gut vorstellen, mich hobbymäßig mehr in dem Bereich auszuleben.
Dennoch muss ich sagen, dass der Einstieg nicht gerade einfach ist, da man anfangs einfach nur akzeptiert, dass eine Komponente/ein Code jetzt so funktioniert, aber nicht weiß wieso.

### Verlauf des Entstehungsprozesses INCOMPLETE

##### Erstes Mal das Panel mit der Libary ausprobiert (_ src: Youtube_)
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

##### Erstes Mal richtige Libary mit Lauftext zum laufen gebracht (_ src: Youtube_)
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

##### 3D-Druck Anfang (14 Stunden Druck) (_ src: Youtube_)
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

##### Placeholder (_ src: Youtube_)
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)


### Nächste Schritte (nicht geplant)

* Weitere Funktionen für das LED-Panel austesten (Uhr)
* Den Apparat mit WLan ausstatten

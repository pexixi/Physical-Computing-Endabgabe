
# Physical Computing Endabgabe

Hier das Repo zu meiner Endabgabe im Seminar Physical Computing bei Peter Ehses.

##### Jannis Steinhauer | Sommersemester 21 | Intermedia Design

<br>

## About

Ziel dieses Projektes ist es, mit Hilfe des Mikrocontrollers _ESP32_, ein LED-Panel zu steuern, um einen Lauftext wiederzugeben.
Da das ESP32 mit einem Wlan-Chip ausgestattet ist, wird die Apparatur mit Hilfe eines Akkus versorgt, um sie gegebenenfalls portabel und remote-steuerbar zu machen.
Das ganze Konstrukt wird dann in einem 3D-gedruckten Gehäuse untergebracht.

![Frontview](https://i.imgur.com/c2CKlla.jpg)
![Frontview offenes Gehäuse](https://i.imgur.com/evBwEmW.jpg)
![Innenansicht Gehäuse](https://i.imgur.com/oumAU7L.jpg)

<br>

## Step 1

### Komponenten

#### Folgende Komponenten werden für das Projekt benötigt:

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

#### Folgende Software wird im Projekt genutzt:

* [PlattformIO](https://platformio.org/)
* [MD_Parola-Library](https://platformio.org/lib/show/1389/MD_Parola)
* [MD_MAX72XX-Library](https://platformio.org/lib/show/5631/MD_MAX72XX)
* [Fusion360 (CAD)](https://www.autodesk.de/products/fusion-360/personal)
* [PrusaSlicer](https://www.prusa3d.de/prusaslicer/)

### Tools

#### Folgende Tools werden im Projekt verwendet:

* Lötkolben und Lötzinn
* 3D-Drucker
* Heisklebepistole

<br>

## Step 2

### Schaltplan und Zusammenbau der Hardware

#### Schaltplan:

![Schaltplan](https://i.imgur.com/u6TIvw4.png)

<br>

#### Pinout AZ-Delivery ESP32:

![Pinout ESP32](https://i.imgur.com/lMDQXF4.png)

_Bitte löten Sie die Kabel wie auf dem Schaltplan beschrieben._


### Zusammenbau:

* Schritt 1: Löten Sie die zwei PCB Mounts auf das PCB (siehe Abb. 1 und 2)

##### Abb 1
![Abb 1](https://i.imgur.com/qVwpAJD.png)

##### Abb 2
![Abb 2](https://i.imgur.com/J8BxMbJ.png)
<br>

* Schritt 2: Löten Sie die Kabel an das PCB (siehe Abb. 3)

##### Abb 3
![Abb 3](https://i.imgur.com/mvvYrfw.png)
<br>

* Schritt 3: Demontieren Sie das erste LED-Panel von der Platine und entfernen Sie den Pinstecker
<br>

* Schritt 4: Löten Sie die Pins im 90° Winkel zur Platine (siehe Abb. 4)
##### Abb 4
![Abb 4](https://i.imgur.com/YWQJju5.png)
<br>

* Schritt 5: Löten Sie die Pins am 5V und GND Pol des Battery Shields (siehe Abb. 5)
##### Abb 5
![Abb 5](https://i.imgur.com/YbEGsFS.png)
<br>

* Schritt 6: Stecken Sie das ESP32 auf das PCB Mount (siehe Abb. 6)

##### Abb 6
![Abb 6](https://i.imgur.com/8wwh0zU.png)
<br>

* Schritt 8: Verbinden Sie alle Komponenten mit Kabeln
<br>

* Schritt 9: Legen sie den Li-ion Akku in das Battery Shield <br> **WICHTIG: Achten Sie auf die richtige Ausrichtung des Akkus (+ zu + und - zu -)**
<br>

## Step 3

### Code

#### In diesem Repository befinden sich alle benötigten Dateien um den Code-Teil des Projektes zu realisieren.

[Download Code als zip-Datei](https://github.com/pexixi/Physical-Computing-Endabgabe/archive/refs/heads/main.zip)

_Sidenotes_: 
* Alle Dateien des Repositories müssen in einem Ordner lokal gespeichert werden, die Dateistruktur darf nicht verändert werden.
* Nutzen Sie einen Code-Editor wie beispielsweise [Visual Studio Code](https://code.visualstudio.com/) (VSC) um den Code zu editieren.
* Nutzen Sie die IDE von PlattformIO, welche in VSC installiert werden kann (Plugin), um den Code auf den ESP32 zu hochzuladen.
* Sollten Sie Probleme beim Einrichten von PlattformIO in VSC haben, schauen Sie in die [Dokumentation](https://docs.platformio.org/en/latest/integration/ide/vscode.html).
* **Die einzige Datei die verändert werden sollte ist die _main.cpp_ im _src_ - Ordner**

### Install Software

* Schritt 1: Wenn Sie die IDE von PlattformIO benutzen, starten Sie ein neues Projekt und wählen Sie ihren Microcontroller aus
* Schritt 2: Installieren Sie  die Libraries _MD_PAROLA_ und _MD_MAX72XX_ über PlattformIO in ihr Projekt
* Schritt 3: Kopieren Sie die Dateien aus dem Repo in den Projektordner
* Schritt 4: Bearbeiten Sie die main.cpp-Datei nach Ihrem belieben
* Schritt 5: [Builden Sie das Projekt](https://docs.platformio.org/en/latest/core/quickstart.html#process-project)
* Schritt 6: [Laden Sie das Projekt auf den ESP32](https://docs.platformio.org/en/latest/core/quickstart.html#process-project)
<br>

## Step 4

### 3D-Modell

#### Fusion360

Das Casing wurde als 3D-Modell in Fusion360 erstellt und als [.f3z-Datei für weitere Konfigurationen](https://drive.google.com/file/d/1JD8DKZzHgL9R7PYdTcOIQCFAfEy4mTFu/view?usp=sharing) bzw. als [Case-Bottom](https://drive.google.com/file/d/12Amgk3q4uACBWGeh2aorHHYebmk8sI24/view?usp=sharing) und [Case-Top](https://drive.google.com/file/d/1RedVauzBIqDiYhcPsK67nbPZa154sME3/view?usp=sharing) im .stl-Format für einen Slicer exportiert. <br>
_Alle Dateien können heruntergeladen und in entsprechenden Programmen modifiziert werden._

![Assembly 1](https://imgur.com/YmZyLP6.png)
![Assembly 2](https://imgur.com/8rsKGCR.png)
![Assembly 3](https://imgur.com/rqFNzdl.png)
![Assembly 4](https://imgur.com/KwiUSJY.png)

#### PrusaSlicer

Casing-Bottom und Casing-Top werden anschließend in PrusaSlicer importiert, um einen 3D-druckbares Modell zu generieren. Für den Ender 3 Pro 3D-Drucker ist bereits eine [fertiger G-Code](https://drive.google.com/file/d/1LTSdZjHYtXzgyWq_We8hQhu_QRHT8Dq6/view?usp=sharing) angelegt. <br>
_Um aus den .stl-Dateien einen G-Code für einen anderen 3D-Drucker zu generieren, schauen Sie in die [Dokumentation von PrusaSlicer](https://github.com/prusa3d/PrusaSlicer)_

![G-Code-Modell in PrusaSlicer](https://imgur.com/l1lSUjz.png)

<br>

## Step 5

### Finish

#### Zusammenbau der Komponenten

Das 3D-gedruckte Casing kann jetzt mit 120er Körnung Schmirgelpapier von Druckfehlern befreit werden, danach kann die Oberfläche angeraut und mit Sprühfarbe eingefärbt werden.
Legen Sie nach dem Trocknen das LED-Panel in die Halterung und fixieren Sie das Panel gegebenenfalls mit etwas Isolierband.
Richten Sie die Komponenten anschließend auf dem Boden des Casings aus, dass Sie passen und isolieren Sie den Akku, wenn nötig, von angrenzender Elektronik mit Isolierband. Kleben Sie anschließend die Komponenten auf dem Boden des Casings mit Hilfe einer Heißklebepistole fest.

<br>

# Misc

### Verwendete Tutorials

* [Text Scrolling Display | MAX7219 Dot Matrix 4-in-1| Arduino (Youtube)](https://www.youtube.com/watch?v=lcrQet0ga-k)
* [Matrix LED 32x8 - 4 Modules 8x8 with MAX7219 (GrabCAD)](https://grabcad.com/library/matrix-led-32x8-4-modules-8x8-with-max7219-1)

### Reflektion der Ziele

#### These

Als Webentwickler macht mir Coden spaß, zudem bin ich relativ technikbegeistert und neugierig wie Technik generell funktioniert. In meinem Projekt wollte ich erste Berührungspunkte mit dem Thema Microcontroller und elektronischen Komponenten sammeln, um herauszufinden, ob mir dieses Gebiet gefällt und ich mich weiter in diese Richtung entwickeln will. Außerdem wollte ich ein besseres Verständnis dafür entwickeln wie Technik von Grund auf funktioniert.

#### Fazit

Ich konnte definitiv ein besseres Verständnis dafür bekommen, wie Technik aufgebaut ist und funktioniert. Microcontroller finde ich sehr spannend und ich kann mir gut vorstellen, mich hobbymäßig mehr in dem Bereich auszuleben.
Dennoch muss ich sagen, dass der Einstieg nicht gerade einfach ist, da man anfangs einfach nur akzeptiert, dass eine Komponente/ein Code jetzt so funktioniert, aber nicht weiß wieso.

### Verlauf des Entstehungsprozesses

#### Erstes Mal das Panel mit Library ausprobiert (Youtube)
[![Thumbnail](https://img.youtube.com/vi/kx7GaSJh67w/0.jpg)](https://www.youtube.com/watch?v=kx7GaSJh67w)

#### Erstes Mal richtige Library mit Lauftext zum Laufen gebracht (Youtube)
[![Thumbnail](https://img.youtube.com/vi/GreU7p_BqmY/0.jpg)](https://www.youtube.com/watch?v=GreU7p_BqmY)

#### 3D-Druck (Anfang von 16 Stunden drucken) (Youtube)
[![Thumbnail](https://img.youtube.com/vi/_AsuDvulLv0/0.jpg)](https://www.youtube.com/watch?v=_AsuDvulLv0)

#### Fertiger 3D-Druck
![Thumbnail](https://i.imgur.com/396HDb0.jpg)
![Thumbnail](https://i.imgur.com/0Tot4Vi.jpg)
![Thumbnail](https://i.imgur.com/cMy0D1a.jpg)

#### Fertiger 3D-Druck mit Elektronik
![Thumbnail](https://i.imgur.com/8WCQTdx.jpg)
![Thumbnail](https://i.imgur.com/YFGhRfT.jpg)

#### Gehäuse lackieren
![Thumbnail](https://i.imgur.com/2rADNki.jpg)
![Thumbnail](https://i.imgur.com/ZQNhOjF.jpg)


### Nächste Schritte (nicht geplant für Endabgabe)

* Weitere Funktionen für das LED-Panel austesten (Uhr)
* Den Apparat mit WLan ausstatten



Einführung in die Fernerkundung - Tag 2 - SNAP


## 2 Einstieg in SNAP

### Allgemeine Hinweise

•Es empfiehlt sich für die Übungen immer einen eigenen lokalen Ordner anzulegen und zu verwenden (z.B. **…\FE_Kurs\02_SNAP**). Ich rate ausdrücklich von der Verwendung des Desktops und der "Dokumente" oder ähnlicher Ordner ab, die insbesondere bei späteren Aufgaben mit R zu Problemen führen können. 

Im Idealfall sollte man bei der Ordnererstellung darauf achten keine Sonderzeichen (wie z.B. "ä", "ü", "ö", "ß", "%" usw.) zu verwenden

**Daten:**

• Komprimierter Datensatz Sentinel_2_Wien.zip (die gepackte Datei enthält ein Subset einer Sentinel-2-Szene aus dem März 2026; nach dem Entpacken sollte zum einen eine Datei im SNAP-eigenen DIMAP Format zu sehen sein, so wie ein Ordner, der die eigentlichen Daten enthält)

• Die Daten finden sich auf BOKUlearn im entsprechenden Ordner für die Übungen von heute..

▪ Bitte die Daten herunterladen und im eigenen Ordner abspeichern - achtet darauf, dass ihr den Ordner wiederfinden könnt.

▪ Anschließend können die Daten entpackt werden


### 2.1 Lernziele

• Erstes Kennenlernen von SNAP
• Laden von Satellitenbildern in SNAP
• Navigation innerhalb des Satellitenbildes
• Erste Visualisierung von Satellitenbildern sowie Anzeigen von Spektralinformationen



### 2.2 Start und Öffnen von Rasterdaten

![Abbildung 1: Starten von ESA SNAP im Startmenü](Fig_01.png)

**Abbildung 1: Starten von ESA SNAP im Startmenü**

• Wir starten in dem wir SNAP starten. Dafür wählen wir: Start > ESA SNAP > SNAP Desktop. Falls eine Desktopverknüpfung auf Ihrem Rechner vorhanden ist, können Sie auch diese doppelklicken.

Nachdem sich SNAP geöffnet hat, können wir nun das zur Verfügung gestellte Sentinel-2 Satellitenbild öffnen, welches eine Szene von Wien zeigt.

• Hierfür gibt es zwei Optionen, zum einen kann das Bild über **FILE > OPEN PRODUCT** geöffnet werden. Falls  mit der ersten Option das Bild im richtigen Ordner nicht angezeigt wird, kann man unter Files of type > All Files wählen und dann sollte das Bild zu sehen sein. Eine weitere Option ist es die Datei **subset_0_of_S2A_MSIL1C_20260314T095051_N0512_R079_T33UWP_20260314T132917** direkt via "drag & drop" in den Product Explorer von SNAP zu ziehen.

• Als nächsten Schritt öffnen wir einen einzelnen Spektralkanal des Satellitenbildes. Dafür öffnen wir zuerst im Product Explorer den Reiter Bands und machen dann entweder einen Rechtsklick auf das Band 2 und wählen "Open Image Window" oder alternativ führen wir einen Doppelklick auf das Band 2 aus.

![Abbildung 2: Laden von Band 2 des Sentinel-2 Satellitenbildes](Fig_02.png)

**Abbildung 2: Laden von Band 2 des Sentinel-2 Satellitenbildes**

Sie sollten nun rechts im großen Visualisierungsbereich eine Visualisierung des Spektralkanals sehen. Im nächsten Schritt lernen wir, wie wir innerhalb des Satellitenbildes navigieren können.

### 2.3 Navigieren und zoomen im Satellitenbild

Für die Navigation und räumliche Orientierung in SNAP gibt es einige hilfreiche Tools. In manchen Fällen kann es interessant sein zu überprüfen an welcher Stelle der Welt sich das aktuell geladene Satellitenbild befindet. In den Standarteinstellungen findet sich hierfür in der Benutzeroberfläche links unten ein Reiter namens "WorldView" (markiert mit 2 in Abbildung 3). Hier werden die Grenzen des Satellitenbilde auf der Weltkugel dargestellt.

Für die Navigation innerhalb des visualisierten Satellitenbildes gibt es im Reiter "Navigation" verschiedene gängige Tools:

- Zoom-Buttons: Durch (mehrfaches) klicken des plus oder minus buttons (markiert mit 1 in Abbildung 3) kann man in das Satellitenbild hinein- oder herauszoomen. Alternativ kann man auch mit dem Mausrad zoomen.
 
- Panning tool: Mit dem Panning tool (markiert mit 1 in Abbildung 3) kann man den aktuell sichtbaren Bildausschnitt verändern

![Abbildung 3: Navigation in SNAP ](Fig_03.png)

**Abbildung 3: Navigation in SNAP**


### 2.4 Anzeigen der Spektralsignaturen

Neben der räumlichen Orientierung ist es natürlich wichtig zu erfahren, welche Werte in jedem Pixel der Satellitenszene enthalten sind.

Tool: Pixel Info (z.B. Suche via Search rechts oben in SNAP)

• Via Selection tool (siehe Toolbar) können einzelne Pixel ausgewählt werden (markiert mit 1 in Abbildung 4). 

• In der Pixel Info wird unter „Bands“ der im Pixel enthaltene Wert für den geladenen Spektralkanal (hier: B2) angezeigt (markiert mit 2 in Abbildung 4).

• Die rechte Spalte zeigt die Einheit an, hier: dl = dimensionless.

⇒  Der angegebene Pixelwert stellt den Reflexionsgrad (auch Reflektanz, engl. reflectance) dar.

![Abbildung 4: Anzeigen von Pixelwerten ](Fig_04.png)

**Abbildung 4: Anzeigen von Pixelwerten**

Aufgabe: Suchen Sie nun beispielhafte Pixelwerte für den Spektralkanal B2 und den Spektralkanal B8 für die folgenden Landbedeckungen/ Landnutzungen heraus und notieren Sie sich diese (siehe Tabelle in Abbildung 5).

![Abbildung 5: Übersicht über die zu extrahierenden Pixelwerte](Fig_05.png)

**Abbildung 5: Übersicht über die zu extrahierenden Pixelwerte**

• **TIPP 1:** Öffnen Sie auch den Spektralkanal B8 im Product Explorer mit einem Doppelklick.

• **TIPP 2**: Sie können sich beide Spektralkanäle auch parallel ansehen:
 Wählen Sie dafür in der Toolbar Tile Horizontally aus (markiert mit 5 in Abbildung 4).
 Die beiden parallelen Views können dann synchronisiert werden via (Menüleiste) VIEW > SYNCHRONIZE IMAGE VIEWS.

![Abbildung 6: Synchronisation der Visualisierungen einzelner Ansichten](Fig_06.png)

**Abbildung 6: Synchronisation der Visualisierungen einzelner Ansichten**

• **TIPP 3**: Sie können dafür das Pin Placing Tool (markiert mit 3 in Abbildung 4)) verwenden und an den gewünschten Stellen einen Pin platzieren. Um die Pixelwerte der einzelnen Pins ablesen zu können, klicken Sie mit dem Selection Tool Ihren Pin an (er ist dann gelb markiert) und setzen Sie im Pixel Info-Fenster das Häkchen für Snap to selected pin (markiert mit 4 in Abbildung 4)). Sie können so für ein und dasselbe Pixel die Werte von mehreren Spektralkanälen ablesen.



### 2.5 Farbdarstellung
Bisher haben Sie sich die Spektralkanäle einzeln und in Graustufen ansehen können. Um Ihr Satellitenbild auch in Farbe sehen zu können, müssen mehrere Spektralkanäle miteinander kombiniert werden. Das ist in SNAP über ein Tool möglich, das für die 3 verschiedenen „Farbkanonen“ (Rot, Grün, Blau) am Bildschirm die jeweiligen Spektralkanäle der Sentinal-2-Szene auswählt.

Wichtig: Ihr Bildschirm kann nur die Farben Rot, Grün und Blau über die sogenannten „Farbkanonen“ mischen. Deshalb können auch nur maximal drei Spektralkanäle Ihres mehrkanaligen Datensatzes gleichzeitig dargestellt werden. Additive Farbmischung! Für die Farbdarstellung am Monitor können Sie die Spektralkanäle Ihres mehrkanaligen Datensatzes frei kombinieren – Sie müssen nur jeweils einen Spektralkanal auf eine Monitor-Farbkanone „legen“.

Wir wollen uns die Sentinel-2-Szene zuerst in einer Echtfarbdarstellung ansehen, danach in einer Falschfarbdarstellung.

#### 2.5.1 Echtfarbdarstellung
Aufgabe: Öffnen Sie ein sogenanntes Echtfarbkomposit in SNAP.

So funktioniert’s:

• Rechtsklick auf den Datensatz im Product Explorer > Open RGB Image Window (Abbildung 7)

![Abbildung 7: Aufrufen der Echtfarbendarstellung in SNAP](Fig_07.png)

**Abbildung 7: Aufrufen der Echtfarbendarstellung in SNAP**

• Es öffnet sich folgendes Fenster (Abbildung 8):
- Sentinel 2 MSI Natural Colors => entspricht der Echtfarbdarstellung
- hier kann die rote Farbkanone (R) Ihres Bildschirms angesprochen werden
- hier kann die grüne Farbkanone (G) Ihres Bildschirms angesprochen werden
- hier kann die blaue Farbkanone (B) Ihres Bildschirms angesprochen werden

![Abbildung 8: Echtfarbendarstellung in SNAP](Fig_08.png)

**Abbildung 8: Echtfarbendarstellung in SNAP**

• Überprüfen Sie, ob die ausgewählten Spektralkanäle (hier B4, B3 und B2) den notwendigen Spektralbereichen des Lichts entsprechen (Red = Spektralkanal für Rotes Licht, Green = Spektralkanal für Grünes Licht, Blue = Spektralkanal für Blaues Licht; TIPP: siehe Hausaufgabe 1).

• Passen Sie die ausgewählten Spektralkanäle ggf. an und klicken Sie auf „OK“.

• Es öffnet sich ein neuer Viewer mit dem Namen „Sentinel 2 MSI Natural Colors RGB“.


#### 2.5.2 Falschfarbdarstellung
Neben den Echtfarbkompositen werden in der Fernerkundung und allgemein bei der Arbeit mit Satellitendaten gern Falschfarbkomposite verwendet. Hier werden Kanalkombinationen gewählt, die nicht unserem gewohnten Sehen in Rot-Grün-Blau entsprechen.

Falschfarbkomposite haben den Vorteil, dass wir auch die Spektralkanäle visualisieren können, deren Spektralbereiche wir Menschen natürlicherweise nicht sehen können. Diese für uns nicht sichtbaren Spektralbereiche, z.B. das Nahe Infrarot, haben aber eine herausragende Bedeutung in vielen Anwendungsbereichen, z.B. bei Arbeiten zur Vegetationsvitalität.

Aufgabe: Stellen Sie ein Falschfarbkomposit dar.

So funktioniert’s:

• Rechtsklick auf den Datensatz im Product Explorer > Open RGB Image Window

• Unter Profile > False-color Infrared RGB auswählen.

- Welche Spektralkanäle werden ausgewählt?

- Welchen Wellenlängenbereichen des Lichts entsprechen diese (siehe Hausaufgabe 1)?


### 2.6 Export des Bildes als GeoTIFF

Als letzten Schritt des SNAP-Tutorials werden wir das Satellitenbild nun noch als GeoTiff exportieren. Die Standart-Vorgehensweise für diesen Schritt ist in Abbildung 10 dargestellt. Wir müssen hierfür zuerst das Bild welches wir exportieren wollen im "Product Explorer"-Fenster anwählen und dann **"File -> Export -> GeoTiff / BigTiff"**


![Abbildung 9: Export Satellitenbild zu GeoTiff in SNAP](Fig_09.png)

**Abbildung 9: Export Satellitenbild zu GeoTiff in SNAP**

In unserem Fall, führt dies zu einer Fehlermeldung (siehe Abbildung 10). Diese Fehlermeldung erscheint, da unser aktuelles Satellitenbild aus Bändern mit verschiedenen räumlichen Auflösungen besteht. Wir ihr in eurer Hausaufgabe 1 bereits recherchiert hattet, gibt es bei Sentinel-2 bestimmte Bänder mit 10 m Pixelgröße, weitere mit 20 m Pixelgröße, und schließlich welche mit 60 m Pixelgröße. Eine Geotiff-Datei kann hiermir nicht umgehen und erwartet ein Bild in dem alle Bänder dieselbe Pixelgröße haben. 

![Abbildung 10: Fehlermeldung - Export nicht möglich](Fig_10.png)

**Abbildung 10: Fehlermeldung - Export nicht möglich**

Um den Export dennoch zu ermöglichen, werden wir nun zwei weitere Schritte implementieren:

1. Wir werden nur die Bänder mit 10 m und 20 m Pixelgröße beibehalten
2. Wir werden alle übriggebliebenen Bänder auf 10 m "resamplen" - d.h., für die Bänder mit 20 m Pixelgröße wird die räumliche Auflösung künstlich erhöht.

Für den ersten Schritt wählen wir im Product Explorer erneut das Satellitenbild an (falls nicht sowieso schon markiert) und wählen dann im Hauptmenü **"Raster -> Subset"**. Im nun erscheinenden Fenster wählen wir zuerst den Reiter **Band Subset** (markiert mit 1 in Abbildung 11). Hier selektieren wir zuerst **Select None** (markiert mit 2 in Abbildung 11) und danach wählen wir manuell alle Bänder aus, die entweder 10 m oder 20 m Pixelgröße haben (siehe Abbildung 11). Wir bestätigen mit **OK**.

![Abbildung 11: Erstellung eines Band-Subsets in SNAP](Fig_11.png)

**Abbildung 11: Erstellung eines Band-Subsets in SNAP**


Daraufhin erscheint sofort ein neues Produkt in der **"Product Explorer"** Ansicht. Dies geschieht ohne Zeitverzögerung, da SNAP die eigentliche Erstellung des Subsets noch nicht durchführt sondern nur die "Regel" abspeichert. Erst wenn das Satellitenbild gespeichert oder exportiert wird, wird die eigentliche Prozessierung durchgeführt.

Für den zweiten Schritt wählen wir das soeben erstelle neue Produkt an und wählen dann **Raster -> Geometric -> Resampling**. Im erscheinenden neuen Fenster wählen wir den Reiter **Resampling Parameters** (markiert mit 1 in Abbildung 12). Hier sehen wir verschiedene Auswahlmöglichkeiten wie wir das Resampling durchführen können. Für den aktuellen Fall sind die Einstellungen bereits in Ordnung so wie sie sind und wir bestätigen mit **OK**. Daraufhin erscheint wiederum ein neues Produkt im "Product Explorer".

![Abbildung 12: Resampling von Satellitenbildern in SNAP](Fig_11.png)

**Abbildung 12: Resampling von Satellitenbildern in SNAP**

Wenn wir dieses neu erstelle Produkt jetzt anwählen und dann wiederum versuchen das Satellitenbild zu exportieren (siehe oben), sollte es funktionieren. Bitte speichern Sie das Bild mit dem Dateinamen "Sentinel_2_Wien_Maerz_2026.tif" in ihren Ordner. Das Bild werden wir kommende Woche in R weiterverwenden.


Das waren die Inhalte der zweiten Sitzung „Einführung in SNAP“.
Wenn Sie dieses Handout durchgearbeitet haben, haben Sie

✓ die Benutzeroberfläche von SNAP kennengelernt,
✓ sich damit beschäftigt, wie Sie in Ihrem Sentinel-2-Satellitenbild räumlich navigieren können,
✓ kennengelernt, wie einzelne Spektralkanäle in Rasterdatensätzen gespeichert sind,
✓ für unterschiedliche Wellenlängenbereiche Pixelwerte für verschiedene Landbedeckungen abgerufen und
✓ verschiedene Farbkomposite erstellt.
✓ Das Satellitenbild als Geotiff-Datei exportiert.

## HAUSAUFGABE





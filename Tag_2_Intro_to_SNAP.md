
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

Um in das Bild hineinzuzoomen gibt es in der Hauptmenü-Leiste einen Zoom button (markiert mit 1 in Abbildung 3). Nachdem dieser ausgewählt wurde, kann man mit der Maus ein Rechteck in der aktuellen Visualisierung zeichnen und die Visualisierung zoomt dann auf diesen Ausschnitt.

Mit dem Panning tool (markiert mit 1 in Abbildung 3) kann man den aktuell sichtbaren Bildausschnitt verändern indem man mit der Maus klickt, hält und dann die Maus in eine entsprechende Richtung zieht.

Für die Navigation innerhalb des visualisierten Satellitenbildes gibt es im Reiter "Navigation" (markiert mit 1 in Abbildung 3a) weitere Tools:

- Zoom-Buttons: Durch (mehrfaches) klicken des plus oder minus buttons (markiert mit 2 in Abbildung 3a) kann man in das Satellitenbild hinein- oder herauszoomen. Alternativ kann man auch mit dem Mausrad zoomen.
 

![Abbildung 3: Navigation in SNAP 1](Fig_03.png)

**Abbildung 3: Navigation in SNAP - Teil 1**

![Abbildung 3: Navigation in SNAP ]2(Fig_03a.png)

**Abbildung 3a: Navigation in SNAP - Teil 2**



### 2.4 Anzeigen von Pixelwerten

Die Visualisierung eines einzelnen Spektralkanals ermöglicht uns wertvolle räumliche und Textur-Information im Bild zu erfassen, gleichzeitig ist die Darstellung der im Satellitenbild vorhandenen Spektralinformation momentan auf einen einzelnen Kanal beschränkt und wir können die genauen Pixelwerte nicht sehen. Im Folgenden werden wir lernen, wie wir uns die jeweiligen SPektralwerte von einzelnen Pixeln anzeigen lassen können.

Hierfür werden wir zuerst das "Pixel Info" Fenster öffnen (falls dieses nicht bereits geöffnet ist). Die können wir erreichen in dem wir rechts oben in der "Search" Leiste (markiert mit 0 in Abbildung 4) "pixel info" eingeben und klicken. Dann sollte ein zusätzlicher Reiter im "Product Explorer" Fenster erscheinen (markiert mit 2 in Abbildung 4). 

Mit dem "Selection tool" (markiert mit 1 in Abbildung 4) können wir mit dem Mauszeiger über einen bestimmten Teil des Bildes fahren und in der Pixel Info wird unter „Bands“ der im Pixel enthaltene Wert für den aktuell geladenen Spektralkanal (hier: B2) angezeigt (markiert mit 5 in Abbildung 4).

Die rechte Spalte zeigt die Einheit an. Im gegebenen Fall handelt es sich um eine atmosphärische korrigierte Satellitenbildszene, und die Einheit "dl" steht für "dimensionless". Tatsächlich stellt der angegebene Pixelwert  den Reflexionsgrad (auch Reflektanz, engl. reflectance) dar, d.h., der prozentuale Anteil der einfallenden elektromagnetischen Strahlung der von der räumlichen Bezugsfläche auf der Erdoberfläche (dem Pixel) in Richtung des Sensors zurückgestrahlt wurde.

![Abbildung 4: Anzeigen von Pixelwerten ](Fig_04.png)

**Abbildung 4: Anzeigen von Pixelwerten**

Um etwas systematischer die Reflektanzen bestimmter Pixel im Bild untersuchen zu können, ist es auch möglich mit dem Pin-placing tool (markiert mit 3 in Abbildung 4) bestimmte Pixel zuerst zu markieren, diese dann mit dem Auswahlwerkzeug (markiert mit 1 in Abbildung 4) zu selektieren und sich dann den Pixelwert des aktuell ausgewählten Pixels über die Option "Snap to selected pin" (markiert mit 4 in Abbildung 4) anzeigen zu lassen.


### 2.5 Farbdarstellung

Bisher haben wir nur einen einzelnen Spektralkanal visualisiert, der dann notwendigerweise als Graustufenbild dargestellt wird. Um ein Farbbild zu erhalten, müssen mindestens 2 (in der Regel aber 3) Spektralkanäle verwendet werden. Für die Visualisierung eines Farbbildes verwendet ein Computer-Monitor drei Farbkanäle. Dies entspricht 3 LED-Einheiten im monitor, die in der Lage sind blaues (B), grünes (G) und rotes (R) Licht auszugeben. Alle anderen Farben werden aus der Kombination und Gewichtung der drei Farben erzeugt. 

D.h., für die Visualisierung muss ich dem Computer mitteilen welche Spektralkanäle des Satellitenbildes ich welchem Farbkanal des Monitors zuordnen möchte. In SNAP gibt es hier einige Standardeinstellungen, die es ermöglichen die gängigsten Visualisierungen eines Sentinel-2 Bildes schnell umsetzen. Eine benutzerdefinierte Definition welche Spektralkanäle welchen Farnkanälen zugeordnet werden ist allerdings auch problemlos und einfach möglich.

Die zwei typischsten Visualisierungen sind das RGB-Echtfarbenkomposit und das CIR-Falschfarbenkomposit.

#### 2.5.1 RGB-Echtfarbenkomposit

Ein RGB-Echtfarbenkomposit hat es zum Ziel die Spektralkanäle des Satellitenbildes so den Farbkanälen zuzuordnen, damit das Satellitenbild in einer Form visualisiert wird, wie ein menschliches Auge es wahrnehmen würde, wenn es die Erdoberfläche an Bord des Satelliten beobachten würde.

Ein Echtfarbenkomposit kann in SNAP wie folgt geöffnet werden:

Rechtsklick auf das Satellitenbild im Product Explorer und Auswahl der Option: **Open RGB Image Window** (Abbildung 7)

![Abbildung 7: Aufrufen der Echtfarbendarstellung in SNAP](Fig_07.png)

**Abbildung 7: Aufrufen der Echtfarbendarstellung in SNAP**

Es öffnet sich ein neues Fenster (siehe Abbildung 8) in dem wir die Option **Sentinel 2 MSI Natural Colors** wählen. 

Die automatische Zuordnung bei dieser Option ist wie folgt:

Blauer Farbkanal ==> Sentinel-2 Band 2 (blauer Wellenlängenbereich)
Grüner Farbkanal ==> Sentinel-2 Band 3 (grüner Wellenlängenbereich)
Roter Farbkanal ==> Sentinel-2 Band 4 (roter Wellenlängenbereich)


![Abbildung 8: Echtfarbendarstellung in SNAP](Fig_08.png)

**Abbildung 8: Echtfarbendarstellung in SNAP**

Es ist wichtig darauf zu achten, dass diese Zuordnung nur automatisiert richtig erfolgt, wenn die Wellenlängenbereiche im Satellitenbild richtig definiert sind. Ist dies nicht der Fall, kann es hier zu Problemen kommen. In unserem Fall, sollte nach Bestätigen der Option das Satellitenbild als Farbbild visualisiert werden (vergleich Abbildung 8).


#### 2.5.2 Falschfarbdarstellung


Neben den RGB-Echtfarbendarstellung ist die zweihäufigste verwendete Visualisierung das CIR-Falschfarbenkomposit. Dabei steht CIR für "Color Infrared". Die CIR-Falschfarbendarstellung ist insbesondere für die Analyse und Interpretation von Vegetation interessant, da in dieser Visualisierungsvariante der Spektralkanal, welcher Informationen im Nahen Infrarot enthält sichtbar gemacht wird. 

Um eine CIR-Visualisierung zu erstellen führen wir wiederum einen Rechtsklick auf das Satellitenbild aus und wählen **Open RGB Image Window** (Abbildung 7).

Es öffnet sich ein neues Fenster (siehe Abbildung 8) in dem wir die Option **Sentinel 2 MSI False Color Infrared** wählen. 

Die automatische Zuordnung bei dieser Option ist wie folgt:

Blauer Farbkanal ==> Sentinel-2 Band 3 (grüner Wellenlängenbereich)
Grüner Farbkanal ==> Sentinel-2 Band 4 (roter Wellenlängenbereich)
Roter Farbkanal ==> Sentinel-2 Band 8 (naher Infrarot Wellenlängenbereich)

Bemerkenswert ist hierbei, dass das Band 8 gewählt wird und nicht das Band 5, 6 oder 7. Die Bänder 5, 6 und 7 liegen ebenfalls alle im nahen Infrarotbereich (und könnten dementsprechend gewählt werden und würden farblich einen ähnlichen visuellen Eindruck erzielen), sie haben allerdings eine räumliche AUflösung (Pixelgröße) von 20 m, wohingegen das Band 8 eine höhere räumliche Auflösung von 10 m besitzt. Da das grüne und das rote Band bei Sentinel-2 ebenfalls 10 m Auflösung besitzen, ist es sinnvoll das Band 8 zu wählen, um von der deutlich erhöhten Bildschärfe und dem höheren Detailreichtum zu profitieren.

### 2.6 Export des Bildes als GeoTIFF

Als letzten Schritt des ersten SNAP-Tutorials werden wir das Satellitenbild nun noch als GeoTiff exportieren. Dies ist ein weit genutztes Bildformat, welches sich problemlos in anderen Softwareumgebungen öffnen lässt wohingegen das aktuell verwendete DIMAP-Format ein SNAP-spezifisches Format ist, welches nur von SNAP geöffnet werden kann. Die Standart-Vorgehensweise für diesen Schritt ist in Abbildung 9 dargestellt. Wir müssen hierfür zuerst das Bild welches wir exportieren wollen im "Product Explorer"-Fenster anwählen und dann **"File -> Export -> GeoTiff / BigTiff"**


![Abbildung 9: Export Satellitenbild zu GeoTiff in SNAP](Fig_09.png)

**Abbildung 9: Export Satellitenbild zu GeoTiff in SNAP**

In unserem Fall, führt dies zu einer Fehlermeldung (siehe Abbildung 10). Diese Fehlermeldung erscheint, da unser aktuelles Satellitenbild aus Bändern mit verschiedenen räumlichen Auflösungen besteht. Wir wir bereits kurz erfahren hatten, gibt es bei Sentinel-2 bestimmte Bänder mit 10 m Pixelgröße, weitere mit 20 m Pixelgröße, und schließlich auch drei Bänder mit 60 m Pixelgröße. Eine Geotiff-Datei kann hiermir nicht umgehen und erwartet ein Bild in dem alle Bänder dieselbe Pixelgröße haben. 

![Abbildung 10: Fehlermeldung - Export nicht möglich](Fig_10.png)

**Abbildung 10: Fehlermeldung - Export nicht möglich**

Um den Export dennoch zu ermöglichen, werden wir nun zwei weitere Schritte ausführen:

1. Wir werden nur die Bänder mit 10 m und 20 m Pixelgröße beibehalten
2. Wir werden alle übriggebliebenen Bänder auf 10 m "resamplen" - d.h., für die Bänder mit 20 m Pixelgröße wird die räumliche Auflösung künstlich erhöht.

Für den ersten Schritt wählen wir im Product Explorer erneut das Satellitenbild an (falls nicht sowieso schon markiert) und wählen dann im Hauptmenü **"Raster -> Subset"**. Im nun erscheinenden Fenster wählen wir zuerst den Reiter **Band Subset** (markiert mit 1 in Abbildung 11). Hier selektieren wir zuerst **Select None** (markiert mit 2 in Abbildung 11) und danach wählen wir manuell alle Bänder aus, die entweder 10 m oder 20 m Pixelgröße haben (siehe Abbildung 11). Wir bestätigen mit **OK**.

![Abbildung 11: Erstellung eines Band-Subsets in SNAP](Fig_11.png)

**Abbildung 11: Erstellung eines Band-Subsets in SNAP**


Daraufhin erscheint sofort ein neues Produkt in der **"Product Explorer"** Ansicht. Dies geschieht ohne Zeitverzögerung, da SNAP die eigentliche Erstellung des Subsets noch nicht durchführt sondern nur die "Regel" abspeichert. Erst wenn das Satellitenbild final gespeichert oder exportiert wird, wird die eigentliche Prozessierung durchgeführt.

Für den zweiten Schritt wählen wir das soeben erstelle neue Produkt an und wählen dann **Raster -> Geometric -> Resampling**. Im erscheinenden neuen Fenster wählen wir den Reiter **Resampling Parameters** (markiert mit 1 in Abbildung 12). Hier sehen wir verschiedene Auswahlmöglichkeiten wie wir das Resampling durchführen können. Für den aktuellen Fall sind die Einstellungen bereits in Ordnung so wie sie sind und wir bestätigen mit **OK**. Daraufhin erscheint wiederum ein neues Produkt im "Product Explorer".

![Abbildung 12: Resampling von Satellitenbildern in SNAP](Fig_11.png)

**Abbildung 12: Resampling von Satellitenbildern in SNAP**

Wenn wir dieses neu erstelle Produkt jetzt anwählen und dann wiederum versuchen das Satellitenbild zu exportieren (siehe oben), sollte es funktionieren. Bitte speichern Sie das Bild mit dem Dateinamen "Sentinel_2_Wien_Maerz_2026.tif" in ihren Ordner. Das Bild werden wir kommende Woche in R weiterverwenden.


## HAUSAUFGABE





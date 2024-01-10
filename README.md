# RobotsUnite-Tunnel
## -	Hardware (Aufbau der Holzbox):
1.	Maße der verschiedenen Bauelemente
   Für den Bau der Holzkiste haben wir mit 10 Bauteile gerechnet, damit die Kiste stabil ist, allen Anforderungen entspricht und die erwünschten Funktionsweisen umgesetzt werden können.

  	Verwendet haben wir dafür:
  	- 4x Seitenwände (50x65cm)
    - 2x für Deckel und Boden (50x50cm)
    -	1x zweiter Boden für den Elektronikabteil (47x47cm)
    -	2x Schiebetüre (37x37cm)
    -	1x Klappe für den Deckel (40x40cm)

2. Maße der Ausschnitte
   Ausschnitte haben wir an allen Seitenteilen der Holzkiste zur Stabilisierung vorgenommen (siehe Stabilisierung der Box).
   Außerdem haben wir mittig in den Deckel ein 40x40cm großes Quadrat geschnitten um die Klapptüre für die Technikbox zu realisieren. +
   Für die Schiebetüren haben wir ein 35,5x34 cm (Höhe x Breite) großes Rechteck herausgeschnitten.
   Damit die Schiebetüren auf- und zufahren können mussten an der rechten Außenwand Einschnitte vorgenommen werden. Diese wurden passgenau zum Türaufbau gewählt. 

3. Stabilisierung der Box
   Um die Holzkiste sehr stabil zu bauen haben wir uns ein simples System überlegt. Hierzu haben wir an jeder Außenkante der einzelnen Holzplatten die Hälfte der Seite um jeweils 1,5cm ausgesägt und die andere Hälfte unberührt gelassen. Somit hat sich ein recht einfaches, aber effizientes Stecksystem ergeben, welches nach der Verschraubung sich als sehr stabil und robust erwiesen hat.

4.	Aufteilung der Box in Arena- und Technikabteil
   Die Holzkiste wird in einen Arena- und Technikabteil aufgeteilt.
  	Die Arena befindet sich in den unteren zwei Dritteln der Kiste und kann über die beiden verbauten Schiebetüren betreten und genutzt werden. Die Technik im oberen Drittel der Kiste ist einfach über den klappbaren Deckel auf der Oberseite der Box erreichbar. Im inneren der Kiste haben wir einen zweiten Boden verbaut, um die beiden Abteile abzutrennen.
  	Um den zweiten Boden einzubauen, werden zwei Querstreben in der Kiste verschraubt. Auf diesen wird der zweite Boden angebracht.
  	Bis auf die verbauten Motoren für die elektrischen Schiebetüren und die Leuchttaster für das Öffnen und Schließen dieser befinden sich alle elektrischen Bauteile in dem Technikabteil. Diese Aufteilung haben wir vorgenommen, um so gut wie alle Elektrischen Bauteile vom Rest der Box abtrennen zu können, um so mögliche Elektrounfälle zu vermeiden.

5.	Schiebetürmechanismus (3D-Druck und Modell der Zahnradschiene und Zahnrad)
   Die verbauten Schiebetüren wurden ein kleines bisschen Größer als der Ausschnitt an der Vorder- und Rückseite gewählt. Damit wollen wir gewährleisten, dass die Türen bündig am Gehäuse anliegen und seitlich nicht durch Schlitze hindurchgeschaut werden kann.  
Außerdem wurde am Boden eine Aussparung eingefräst, in dieser wir eine Führungsschiene verlegt haben. Somit verhindern wir, dass sich die Holztüren verhaken können.  
Damit sich die Türen leicht öffnen und schließen haben wir uns für den Verbau von Schubauszügen entschieden. Diese lassen sich sehr leicht und ohne großen Kraftaufwand bewegen.
Um die Türen elektrisch antreiben zu können wurde eine 37cm lange Zahnradschienen mit dem passenden Zahnrad 3D-Drucker gedruckt. Die Schienen werden mittig an der Schiebetürinnenseite, an den dafür vorgesehenen Laschen befestigt. Das Zahnrad wird passgenau an den Elektromotoren befestigt. Letztendlich wird der Motor in der Kiste so angebracht, dass sich das Zahnrad passend in der Zahnradschiene bewegt um die Schiebetüren auf- und zufahren lassen zu können. 
Damit die Schiebetüre problemlos aufgehen kann haben wir an der rechten Seitenwand passend Ausschnitte vorgenommen (siehe Maße der Ausschnitte). 

6.	Aufbauplan




## Hardware (Aufbau der Elektrik):
1.	Verwendete Bauteile und deren Funktion
Siemens LOGO 8: 
Diese verwendet, um alle nötigen Programmierungen für das Projekt vorzunehmen. Realisiert werden damit der Schiebetürmechanismus, die Leuchttaster, der Single- und Multimode und die ausgedachten Rätsel. Die Programmierungen wurden mit Siemens LOGO!Soft Comfort vorgenommen. 


Netzteil (24V):
Das 24V-Netzteil welche einen maximalen Ausgangsstrom von 4,5A hat wurde ausgewählt, da es alle verbauten Bauteile mit dem nötigen Strom versorgen kann. Ein weiterer Grund für ein 24V-Netzteil ist, dass es mit den allermeisten Bauteilen kompatibel ist. Außerdem kann bei der Gleichspannung unter 60V auf einen Schutz gegen direktes Berühren verzichtet werden. 


Sicherungen:
Wir nutzen Schmelzsicherungen, weil diese klein und kompakt sind. Außerdem kann man diese flexibel anpassen und falls nötig nochmals zu einem späteren Zeitpunkt den abzusichernden Strom einstellen. Insgesamt werden in dem Projekt fünf Sicherungen verbaut. Jeweils eine Sicherung für die Spannungsversorgung der LOGO, für die Eingänge, welche in die Logo führen, die ersten vier Relais Ausgänge der LOGO, für die Motorsteuerung und eine Sicherung für die LEDs der Leuchtdrucktaster. 


Relais:
In unserer Schaltung verwenden wir Relais, um die Motoren anzusteuern. Pro Drehrichtung des Motors werden 3 Relais verwendet. Ein Relais dient als Sicherung, sodass nicht durch falsches Bedienen der Motor gleichzeitig in den Rechts- und Linkslauf gelangen kann, wodurch ein Kurzschluss entstehen würde. Dies funktioniert in dem man das Relais als Öffner verwendet und in Reihe zum Spulenkontakt des zweikanaligen Relais verschaltet. Das Zweite Relais ist in Reihe zum ersten Relay und wird durch den Endlagentaster gesteuert. Dadurch kann man sicher gehen, dass der Motor aufhört, wenn die Endlage erreicht wurde.
Das dritte Relais ist 2-kanalig, wodurch es uns möglich ist, einfach und sicher zwischen den beiden Leitungen des Motors zu wechseln, um ein Richtungswechsel zu ermöglichen.


Elektromotor: 
Für jede Schiebetüre wurde ein 12V Getriebemotor verbaut. Die Geschwindigkeit des Motors kann über die Spannungswandler und das Verwenden verschiedener Zahnradgrößen passend eingestellt werden. Die Elektromotoren werden in dem Arenaabteil verbaut, die dafür verwendeten Spannungswandler im Technikabteil. 


Endlagentaster: 
An jeder Schiebetüre werden jeweils zwei Endlagentaster angebracht. Diese sollen einerseits den Öffnungs- und andererseits den Schließvorgang stoppen. Sobald die Schiebetüre den Endlagentaster betätigt stoppt der Motor und die Türe gerät in Stillstand. Somit soll vermieden werden, dass die Schiebetüre zu weit auffährt und aus der Führung springt, oder zu weit nach innen fährt und der Motor durch zu spätes Abschalten zerstört wird. 


Spannungswandler: 
Die Spannungswandler werden dafür verwendet, um die 24V vom Netzteil auf die nur teilweise maximal benötigten 12V für die Leuchttaster und Elektromotoren zu wandeln. Auf den Spannungswandlern befindet sich eine Digitale Anzeige, mit dieser man sehr einfach die Passenden Werte einstellen kann. 
Die Spannungswandler werden in einer selbstentworfenen 3D-Druck Box im Technikabteil der Holzkiste verbaut. 


Leuchtdrucktaster: 
Insgesamt wurden vier Leuchttaster verbaut, um die Schiebetüren steuern zu können. Außerhalb der Kiste wurden jeweils auf der Vorder- und Rückseite ein Taster verbaut und im inneren der Kiste genauso. Je nach Auswahl des Rätsels müssen die Leuchttaster verschieden betätigt werden, um ins Innere und dann wieder aus der Kiste herauszukommen. 
Die Leuchtaster sind dauerhaft im Leuchtbetrieb, wenn sich die Schiebtüren bewegen, dann blinken die Taster mit 2 Herz. 



2.	Verkabelungen und Montage der Bauteile in der Technikbox (Aufbauplan)

In der Technikbox wird die Siemens LOGO 8, das passende Erweiterungsmodul, die Relais und die Sicherungen auf einer 35mm breiten Hutschiene verbaut. 

Die Spannungswandler werden in einer 3D gedruckten Box fest verbaut. Die zwei Spannungswandler, welche für die beiden Motoren zuständig sind wurden auf 7,9V eingestellt. Der Spannungswandler für die LED-Beleuchteten Drucktaster wurde auf 10V eingestellt. 

Die sechs verbauten Klemmbausteine wurden auch auf einer Hutschiene angebracht. Die Klemmbausteine sind für die Masse der LOGO und den einzelnen Relais, den Masse für die Leuchtdrucktaster, die Spannungsversorgung der Leuchtdrucktaster, Spannungsversorgung von der LOGO zu den Relais, Ausgang aller Taster, Endlagentaster und Schaltern und für den Eingang über das Netzteil und weitergehende Leitungen um das Gesamt System zu versorgen.

Die Taster um die verschiedenen Modi und Quizes auswählen zu können wurden auch in einem 3D-Modell verbaut und anschließend in dem Technikabteil der Holzkiste verbaut und verdrahtet. 

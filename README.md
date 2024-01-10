# RobotsUnite-Tunnel
## Hardware (Aufbau der Holzbox):
1.	**Maße der verschiedenen Bauelemente**

Für den Bau der Holzkiste haben wir mit 10 Bauteile gerechnet, damit die Kiste stabil ist, allen Anforderungen entspricht und die erwünschten Funktionsweisen umgesetzt werden können.

Verwendet haben wir dafür:
   - 4x Seitenwände (50x65cm)
   - 2x für Deckel und Boden (50x50cm)
   - 1x zweiter Boden für den Elektronikabteil (47x47cm)
   - 2x Schiebetüre (37x37cm)
   - 1x Klappe für den Deckel (40x40cm)

3. Maße der Ausschnitte

Ausschnitte haben wir an allen Seitenteilen der Holzkiste zur Stabilisierung vorgenommen (siehe Stabilisierung der Box).
   Außerdem haben wir mittig in den Deckel ein 40x40cm großes Quadrat geschnitten um die Klapptüre für die Technikbox zu realisieren. +
   Für die Schiebetüren haben wir ein 35,5x34 cm (Höhe x Breite) großes Rechteck herausgeschnitten.
   Damit die Schiebetüren auf- und zufahren können mussten an der rechten Außenwand Einschnitte vorgenommen werden. Diese wurden passgenau zum Türaufbau gewählt. 

4. Stabilisierung der Box

Um die Holzkiste sehr stabil zu bauen haben wir uns ein simples System überlegt. Hierzu haben wir an jeder Außenkante der einzelnen Holzplatten die Hälfte der Seite um jeweils 1,5cm ausgesägt und die andere Hälfte unberührt gelassen. Somit hat sich ein recht einfaches, aber effizientes Stecksystem ergeben, welches nach der Verschraubung sich als sehr stabil und robust erwiesen hat.

5. Aufteilung der Box in Arena- und Technikabteil

Die Holzkiste wird in einen Arena- und Technikabteil aufgeteilt.
Die Arena befindet sich in den unteren zwei Dritteln der Kiste und kann über die beiden verbauten Schiebetüren betreten und genutzt werden. Die Technik im oberen Drittel der Kiste ist einfach über den klappbaren Deckel auf der Oberseite der Box erreichbar. Im inneren der Kiste haben wir einen zweiten Boden verbaut, um die beiden Abteile abzutrennen.
Um den zweiten Boden einzubauen, werden zwei Querstreben in der Kiste verschraubt. Auf diesen wird der zweite Boden angebracht.
Bis auf die verbauten Motoren für die elektrischen Schiebetüren und die Leuchttaster für das Öffnen und Schließen dieser befinden sich alle elektrischen Bauteile in dem Technikabteil. Diese Aufteilung haben wir vorgenommen, um so gut wie alle Elektrischen Bauteile vom Rest der Box abtrennen zu können, um so mögliche Elektrounfälle zu vermeiden.

8.	Schiebetürmechanismus (3D-Druck und Modell der Zahnradschiene und Zahnrad)
   Die verbauten Schiebetüren wurden ein kleines bisschen Größer als der Ausschnitt an der Vorder- und Rückseite gewählt. Damit wollen wir gewährleisten, dass die Türen bündig am Gehäuse anliegen und seitlich nicht durch Schlitze hindurchgeschaut werden kann.  
Außerdem wurde am Boden eine Aussparung eingefräst, in dieser wir eine Führungsschiene verlegt haben. Somit verhindern wir, dass sich die Holztüren verhaken können.  
Damit sich die Türen leicht öffnen und schließen haben wir uns für den Verbau von Schubauszügen entschieden. Diese lassen sich sehr leicht und ohne großen Kraftaufwand bewegen.
Um die Türen elektrisch antreiben zu können wurde eine 37cm lange Zahnradschienen mit dem passenden Zahnrad 3D-Drucker gedruckt. Die Schienen werden mittig an der Schiebetürinnenseite, an den dafür vorgesehenen Laschen befestigt. Das Zahnrad wird passgenau an den Elektromotoren befestigt. Letztendlich wird der Motor in der Kiste so angebracht, dass sich das Zahnrad passend in der Zahnradschiene bewegt um die Schiebetüren auf- und zufahren lassen zu können. 
Damit die Schiebetüre problemlos aufgehen kann haben wir an der rechten Seitenwand passend Ausschnitte vorgenommen (siehe Maße der Ausschnitte). 

9.	Aufbauplan




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


## Software (Programmierungen):
1.	Verwendung der Siemens LOGO 8:

Zur Programmierung der Siemens Logo 8 verwenden wir die dazu passende Software LOGO!Soft Comfort. Mit dieser kann man ohne großartige Programmiervorkenntnisse ein Programm schreiben, welches von der Logo ausgeführt werden soll. Das Ganze wird mittels der Grafischen Benutzeroberfläche realisiert. Das Programm wird mit Logikgattern wie UND, ODER, NOR, usw. geschrieben. Man verbindet die einzelnen Gatter mit dem Pfad, um die Logik zu erstellen. Für eine bessere Übersichtlichkeit kann man die Linien auftrennen. Dabei wird am Anfang und Ende einer Verbindung ein grüner Pfeil eingefügt und die vielen unübersichtlichen Verbindungslinien entfernt. Um die Zugehörigkeiten der Pfeile nachvollziehen zu können, werden die Pfeile immer passend nach Ihrem Gegenstück benannt (Siehe Abbildung). 
So kann der Code in einzelne Netzwerke aufgeteilt werden ohne dass es zu unübersichtlichen Verbindungsknäulen kommt. Um die Lesbarkeit des Programmcodes stark zu erhöhen, haben wir das Konzept durchgehend angewendet. 



2.	Inputs der Siemens LOGO 8:
Die hier für das Projekt verwendete Siemens Logo 8 hat standartmäßig 8 Inputs zur Verfügung. 
Da wir für unser Realisiertes Projekt mehr Inputs benötigen, verwenden wir noch zusätzlich ein Erweiterungsmodul. 
In der nebenstehenden Abbildung sieht man in Gelb die von uns festgelegten und verwendeten  Inputs, welche aufsteigend nummeriert sind. 
Die Inputnummerierung stimmt mit der Nummer auf der Logo überein. Außerdem wurden die Inputs noch beschriftet, damit beim Programmieren leichter nachvollzogen werden kann, wofür der Input verwendet wird. Die Grünen Pfeile stehen für die weiteren Verwendungsorte im Programm. 

3.	Outputs der Siemens LOGO 8:

Um die Schiebetüren steuern zu können, werden vier Outputs an der Siemens LOGO 8 benötigt. Für jeden Output ist die Steuerung sehr ähnlich aufgebaut. Es ändern sich hauptsächlich die Signale, welche verwendet werden. Zu Beginn wurden zwei Oder-Gatter verwendet, da in LOGO!Soft die Gatter nur 4 Eingänge zur Verfügung stellen. Da wir zur vollständigen Realisierung mehr als vier Eingänge benötigen, verwenden wir zwei ODER-Gatter in Reihe. Die Eingänge, welche in die Oder-Gatter gehen, kommen jeweils von vorher Programmierten Code Teilen, wo entschieden wird, dass die Tür sich bewegen soll. Weiter geht das Signal in ein RS-Glied, welches das Signal so lange hält, bis ihm gesagt wird, das es aufhören soll. Zum Stoppen wird das Signal von den verbauten Endlagentaster verwendet, womit der Zustand der Tür bestimmt werden kann. Der Ausgang des RS-Glied geht an den Output der LOGO, wo die Motorsteuerung mit Hilfe von Relais gesteuert wird. 
Mehr dazu kann im vorliegenden Verdrahtungsplan eingesehen werden. 
















4.	Programmierung des Betriebsbeginns: 

Diese 2 Programmausschnitte sind dafür da, die Schiebetüren der Holzkiste in die nötige Startposition zu bringen. 
Wenn die LOGO Strom bekommt und der Programmablauf startet, wird der Blaue Merker aktiviert. Dieser lässt beide Türen schließen, um mögliche Fehlpositionen, welche beim Transport oder dem Aufbau entstanden sein könnten zu beheben (also die Tür ist weder vollständig geschlossen noch geöffnet). 
In der linken Abbildung wird noch auf die Eingänge der Rätsel Auswahl geachtet. Zu Beginn sind bei jedem Rätsel beide Schiebetüren geschlossen weshalb, auf den Einschaltmoment der Inputs für die Rätsel Auswahl geachtet wird, um die Türen zu schließen. 
Die rechte Abbildung zeigt den Programmausschnitt, welcher die Türen der Kiste in die Startposition für den Single- und Team-Modus bringt. Da zu Beginn der beiden Modis die Türen zu keinem Zeitpunkt gelichzeitig geöffnet oder geschlossen sind, wird bei der Auswahl eines Rätsels die geöffnete Türe geschlossen. 


5.	Programmierungen zu Single-Team-Modus 

Verwendet man das Projekt im einfachen Single- und Team-Modus, ohne ein Rätsel auszuwählen dann wird das Parkour Element als einfacher Durchgang genutzt. 

Der hier abgebildete Code ist oben und unten symmetrisch aufgebaut.










  	Hier wird geschaut, in welcher Stellung sich die Schiebetüren befinden. 

 	Für den Single-Modus wird nur geschaut, ob einer der Taster an der Außenseite der Holzkiste  gedrückt wurde. 
 	Für den Team-Modus wird geschaut, ob 2 Taster gleichzeitig gedrückt werden. 
Außerdem gibt es eine Abfrage, ob der Schalter für den dafür nötigen Teammodus gedrückt wurde. 
Die beiden Programmteile oben kommen in ein Oder-Gatter. Dieses Signal geht in ein Und-Gatter, welches den aktuellen Zustand der Türen aufnimmt, um dann die Türen anzusteuern 

 	Hier wird darauf geachtet, dass kein Rätsel aktiv ist. 
In den unteren Eingang des UND-Gatters kommen die Signale von dem Kasten oben drüber. Der Ausgang steuert die Türen 







6.	Programmierungen zu den Rätseln 

Für das Projekt haben wir uns drei verschiedene Rätselarten ausgesucht. Alle Rätsel haben den gleichen Anfang (siehe Abbildung). Dieser Programmteil ist dafür da den richtigen Programmabschnitt zu auszuwählen. Außerdem kann so verhindert werden, dass zwei Rätsel gleichzeitig ausgewählt werden können. 





Rätsel 1:
 
In der folgenden Abbildung sieht man den Programmcode für das ersten auswählbare Rätsel. Das hier verwendete UND-Gatter ist dafür verantwortlich das beide Türen zu sind und die Kiste in Ihrer Grundstellung steht. Dieses Signal geht in ein weiteres UND-Gatter, in diesem drauf geachtet wird, dass immer nur der richtige Schalter gedrückt wird. Daraufhin wird das RS-Glied aktiviert. Dieses wird sofort resettet, wenn der gedrückte Taster losgelassen wird. Danach wird geschaut, ob der nächste Taster zusätzlich gedrückt wird und der Taster mindestes eine Sekunde gedrückt wird damit sich alle Türen öffnen. 

Rätsel 2:
 
Im zweiten Rätsel wird gezählt, wie oft die beiden äußeren Taster gedrückt werden. Wenn beide Taster mindesten 2-mal gedrückt wurden, geben sie das Signal weiter zum UND-Gatter, welches dann die beiden Schiebetüren öffnet. Danach werden die Zähler wieder resettet, damit das Rätsel für den nächsten Durchgang bereit ist.

Rätsel 3:
 
Im dritten Rätsel wird mittels des oben gezeigten Programmcode geschaut, ob die Taster in der richtigen Reihenfolge gedrückt wurden. Realisiert wird der ganze Vorgang durch in Reihe geschaltete RS-Glieder. Erforderlich sind vier Tastendrücke, weshalb vier RS-Glieder benötigt werden. Bei einer Falsch Eingabe werden alle RS-Glieder resettet und die Eingabekombination muss von neuem gestartet werden. Bei richtiger Eingabe öffnen sich die Schiebetüren und das Rätsel resettet, damit es für den nächsten Durchgang bereit ist.



7.	Schließen der Schiebetüren:


Damit im Rätsel Modus die Türen wieder von außen schließen kann ist folgender Programmausschnitt verantwortlich. Wenn irgendein Rätsel ausgewählt wurde und irgendein Taster bei offenen Türen gedrückt wird, schließen sich alle Schiebetüren. Somit befindet das ganze Projekt wieder in Ausgangsstellung. Dies kann verwendet werden, um das Rätsel für den nächsten Durchgang vorzubereiten, oder um die Türen für den Transport zu schließen.



8.	Schiebtüre von Kisteninneren steuern:


Dieser Programmteil wird in jedem Rätsel verwendet. So wird realisiert, dass die Türen von innen immer geöffnet und geschlossen werden können. Das obere UND-Gatter öffnet die Türen, wenn sie zu sind und das untere UND-Gatte schließt sie, wenn sie offen sind.




9.	Lampensteuerung 

Sobald die Box eingeschaltet wird und die Bauteile Strom bekommen, leuchten die Lampen dauerhaft. Situationsbedingt blinken die Leuchtdrucktaster, um den Nutzern Rückmeldung zu bestimmten Ausführungen zu geben. 
Die Lampen sollen mit 1Hz blinken, wenn sich die Schiebtüren öffnen oder schließen. 
Wenn das Rätsel 3 in der falschen Reihenfolge ausgeführt wird und somit ein Fehler entsteht, dann blinken die Lampen für 2 Sekunden schnell mit 5Hz.




Wenn sich die Tür bewegt, schauen wir auf das Signal mit welchen die Tür gesteuert wird. Solange dafür ein Signal da ist, macht der Impulsgeber daraus ein Blinken mit 1Hz.










Falls eine falsche Eingabe im dritten Rätsel getätigt wurde, wird das Resett Signal auch an diesen Programmausschnitt weitergeleitet. Dieser aktiviert das RS-Glied, wodurch ein Impulsgeber mit 5Hz aktiviert wird. Dieser funktioniert solange das RS-Glied aktiv ist. Abgeschaltet wird das RS-Glied wenn die Einschaltverzögerung, welche auf 2 Sekunden eingestellt ist, aktiviert wird.


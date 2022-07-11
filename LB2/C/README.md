### Container
Container sind eine Alternativ zu normalen virtuellen Maschinen. Container virtualisieren Anwendungen. Die Anwendungen sind voneinander getrennt, auch wenn sie auf demselben Rechner und Betriebssystem ausgeführt werden. Sie wissen gegenseitig nichts von ihrer Existenz und können nicht auf Daten anderer Container zugreifen. Im Gegensatz zu klassischen virtuellen Maschinen emulieren Container kein eigenes Betriebssystem, sondern nutzen das des Host-Systems. Im Container sind alle zur Ausführung benötigten Dateien, Konfigurationen, Abhängigkeiten und Bibliotheken vorhanden.
### Docker
Eine der bekanntesten Container-Lösungen ist Docker. Docker ist eine Open-Source-Software, die 2013 erstmals veröffentlicht wurde und die benötigten Funktionen zur Virtualisierung der Anwendungen und Isolierung der Container auf einem Host-System bereitstellt.

#### Docker-Images
Sammlung von Software, die als Container ausgeführt werden soll, der eine Reihe von Anweisungen zum Erstellen eines Containers enthält, der auf der Docker-Plattform ausgeführt werden kann. Bilder können nicht geändert werden, und Änderungen an einem Image erfordern die Erstellung eines neuen Images.

### Deklarativ vs Imperativ
Beim deklarativen Aufsetzen von Containern geht es darum, dem Container einen genauen Ablauf zu vermitteln, welcher der Container ausführt. 

Beim imperativen Aufsetzen von Containern wird das erwartete Resultat definiert, nicht die hierfür nötigen Schritte. 
### Persistent
Persistent steht für anhaltend, dauernd. Bei Containern bedeutet dies, das der Container heruntergefahren werden kann und die Daten trotzdem da bleiben. Somit muss man sich keine Sorgen um Datenverluste machen. 
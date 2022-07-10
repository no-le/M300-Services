# Docker build apache2

Als aller erstes haben wir uns dem Apache2 image gewidmet. Für das haben wir uns dem Wissen ,das wir uns mit den Videos von Marcel Bernet über den Zeitraum des Modules aneigen konnten, bedient.

Dafür haben wir also als erstes das ubuntu Standard Image gepullt mit dem Befehl:

`docker pull ubuntu`

Danach haben wir ein neues Verzeichnis erstellt, damit wir mithilfe von einem Dockerfile unser Image erstellen können.
Mit dem Befehl `mkdir apache2` haben wir das getan.

Danach gingen wir mit dem Befehl `cd apache2` in das Verzeichnis und haben das Dockerfile mit `sudo nano Dockerfile` erstellt.

Der Inhalt unseres Dockerfiles ist relativ simpel gehalten:

```
  FROM ubuntu #Hierbei geht man einfach von dem gepullten ubuntu Image aus
  RUN apt-get update && apt-get install -y apache2 #Hier wird apache2 installiert
  CMD ["apachectl", "-D", "FOREGROUND"] #Bei dieser Linie wird sichergestellt das apache2 automatisch gestartet wird
  EXPOSE 80 #Und zu guter letzt wird noch der Port 80 "freigegeben"
```

## Super digger

asd

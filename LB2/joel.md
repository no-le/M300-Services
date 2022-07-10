# Docker build apache2

Als aller erstes haben wir uns dem Apache2 image gewidmet. Für das haben wir uns dem Wissen ,das wir uns mit den Videos von Marcel Bernet über den Zeitraum des Modules aneigen konnten, bedient.

Dafür haben wir also als erstes das apache2 Standard Image gepullt mit dem Befehl:

`docker pull apache2`

Danach haben wir ein neues Verzeichnis erstellt, damit wir mithilfe von einem Dockerfile unser Image erstellen können.
Mit dem Befehl `mkdir apache2` haben wir das getan.

Danach gingen wir mit dem Befehl `cd apache2` in das Verzeichnis und haben das Dockerfile mit `sudo nano Dockerfile` erstellt.

Der Inhalt unseres Dockerfiles ist relativ simpel gehalten:
`
FROM ubuntu
RUN apt-get update && apt-get install -y apache2
CMD ["apachectl", "-D", "FOREGROUND"]
EXPOSE 80
`

## Super digger

asd

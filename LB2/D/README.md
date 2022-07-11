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
Nachdem dieses also auch erstellt wurde, können wir nun also mit folgendem Befehl, das Docker Image erstellen:
`docker build -t ijoeli/apache2:1.0 .`

Wenn dieses erstellt ist, pushen wir diese noch in das eigene Dockerhub Repository mit diesem Befehl:
`docker push ijoeli/apache2:1.0`

Falls man sich vorher nicht schon eingeloggt hat, muss man dies noch tun, damit man die Berechtigungen dazu hat mit dem Befehl:
`docker login --username=eigenerUsername`

Jetzt ist also das Image im eigenen Repository drin und man kann damit seine eigenen Container nun erstellen:
`docker run -d --name apache2 --hostname apache2 -p 8080:80 ijoeli/apache2:1.0`

## Docker build mysql

Bei mysql sind wir fast gleich vorgegangen wie bei dem apache2 image, nur dass man dort nicht mit dem ubuntu Image arbeitet.

Auch haben wir hier wieder ein neues Verzeichnis erstellt und darin ein Dockerfile.
`mkdir mysql`
`cd mysql`
`sudo nano Dockerfile`

Der Inhalt dieses Dockerfiles sieht auch ein bisschen anderst aus:
```
  FROM mysql # Hierbei geht man einfach von dem normalen mysql Image aus

  ENV MYSQL_ROOT_PASSWORD Password1 # Hier setzen wir das Passwort für den mysql root

  EXPOSE 3306 # Und hier wird der Port 3306 "freigegeben"
```

Wie auch schon vorhin, können wir nun das Image erstellen, und dies dann in das persönliche Repository auf Dockerhub pushen:
`docker build -t ijoeli/mysql:1.0 .`
`docker push ijoeli/mysql:1.0`

Mit diesem Image können wir nun auch einen eigenen Container erstellen und das wie folgt:
`docker run -d --name apache2 --hostname apache2 -p 6603:3306 ijoeli/mysql:1.0`

## Docker Build phpmyadmin


## Docker Compose
Zu guter letzt, haben wir unserem Docker Compose file gewidmet. Als aller erstes müssen wir docker-compose einmal installieren, da es nicht auf den TBZ-VM's vorinstalliert ist:
`apt-install docker-compose`

Danach haben wir auch wieder ein neues Verzeichnis erstellt mit dem Namen compose, und darin ein .yaml file erstellt, da docker-compose damit arbeitet:
`mkdir compose`
`cd compose`
`sudo nano docker-compose.yaml`

Das docker-compose file haben wir mit ein paar Recherchen und eigenen Inputs so erstellt, das es für uns passt:

```
version: '1'

services:
  apache2:
    image: ijoeli/apache2:1.1
    container_name: apache2
    ports:
      - 8888:80
    volumes:
      - apache2:/var/www/html
  db:
    image: ijoeli/mysql:1.0
    container_name: mysql
    environment:
      MYSQL_ROOT_PASSWORD: Password1
      MYSQL_DATABASE: test_db
      MYSQL_USER: test_db
      MYSQL_PASSWORD: Password1
    ports:
      - "6603:3306"
    volumes:
      - mysql:/var/lib/mysql
  phpmyadmin:
    image: phpmyadmin/phpmyadmin
    container_name: phpmyadmin
    links:
      - db
    environment:
      PMA_HOST: db
      PMA_PORT: 3306
      PMA_ARBITRARY: 1
    restart: always
    ports:
      - 8081:80
volumes:
  mysql:
  apache2:
```

In dem docker-compose file wird mithilfe der Volumes auch direkt sichergestellt, dass die wichtigen Services persistent sind.

[Zurück zur Übersicht](../README.md)
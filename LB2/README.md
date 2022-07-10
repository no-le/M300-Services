# Einleitung

In dieser LB2, die dank dem TOB und einigen technischen Problemen mit den VM's sehr verkürzt wurde, werden wir ein eigenes Dockerimage erstellen und dies auf Dockerhub pushen. Wir haben uns dafür entschieden, einen Apache Webserver via Docker aufzusetzen. Diesen verbinden wir dann mit einer MySQL Datenbank. Die Container werden persisitent und deklarativ aufgsetzt. 

## Inhaltsverszeichnis

## Beschreib der genutzten Services
In diesem Kapitel werden die genutzten Services vorgestellt.
### Apache 2
Der Apache HTTP Webserver ist ein open-source Webserver für eine Vielzahl an Betriebssystemene inklusive UNIX und Windows. Veröffentlicht wurde der Apache Webserver in 1995 und seit April 1996 ist er der meistgenutzte Webserver im gesamten Internet. Finden Sie mehr zu Apache über diesen Link:

https://httpd.apache.org/


Passend dazu wurde Apache schon oft in Modulen der TBZ eingesetzt. Dies ist ebenfalls ein Grund für die Auswahl dieses Services. 

### MySQL Datenbank
MySQL ist ein relationales Open Source Datebankverwaltungssystem welches von Oracle entwickelt und unterstützt wird. Eingeführt wurde es wie Apache im Jahre 1995. Seit 2010 gehört MySQL zur Oracle Corporation. Finden Sie mehr zu MySQL über diesen Link:

https://www.mysql.com/de/


Auch hier ist uns der Service bekannt. In den meisten Datenbankmodulen mussten wir mit MySQL arbeiten. 

### PhPmyAdmin



## Beschreib Container und Docker
In diesem Kapitel werden Container sowie einige wichtige Begriffe dazu erklärt. 
### Container
Container sind eine Alternativ zu normalen virtuellen Maschinen. Container virtualisieren Anwendungen. Die Anwendungen sind voneinander getrennt, auch wenn sie auf demselben Rechner und Betriebssystem ausgeführt werden. Sie wissen gegenseitig nichts von ihrer Existenz und können nicht auf Daten anderer Container zugreifen. Im Gegensatz zu klassischen virtuellen Maschinen emulieren Container kein eigenes Betriebssystem, sondern nutzen das des Host-Systems. Im Container sind alle zur Ausführung benötigten Dateien, Konfigurationen, Abhängigkeiten und Bibliotheken vorhanden. Es entsteht ein abgegrenztes Paket mit der Laufzeitumgebung der jeweiligen Applikation. 
### Docker
Eine der bekanntesten Container-Lösungen ist Docker. Docker ist eine Open-Source-Software, die 2013 erstmals veröffentlicht wurde und die benötigten Funktionen zur Virtualisierung der Anwendungen und Isolierung der Container auf einem Host-System bereitstellt.

### Deklarativ vs Imperativ

### Persistent

## Dokumentation

Text

## Testing

Text

## Quellen

Text

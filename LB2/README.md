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

### phpMyAdmin
phpMyAdmin ist eine gratis Webanwendung für die Verwaltung von MySQL und MariaDB Datenbanken. Die Tabellen der Datenbanken werden mit einem GUI verwaltet. Mit dem Verwaltungstool kann man unter anderem: Tabellen und Datensätze erstellen, bearbeiten, löschen, Daten(banken) importieren und exportieren und SQL Anweisungen direkt ausführen. Finden Sie mehr zu phpMyAdmin über diesen Link:

https://www.phpmyadmin.net/

Mit phpMyAdmin haben wir beide noch keine grossen Erfahrungen. 
## Beschreib Container und Docker
In diesem Kapitel werden Container sowie einige wichtige Begriffe dazu erklärt. 
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
Persistent steht für anhaltend, dauernd. Bei Containern bedeutet dies, das Container heruntergefahren werden können und die Daten trotzdem da bleiben. Somit muss man sich keine Sorgen um Datenverluste machen. 

## Dokumentation

Text

## Testing

Text

## Quellen

Text

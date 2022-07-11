## Apache2

| Testfall NR.  | Beschreibung |  Vorgehen  |  Voraussetzung / Umfeld  |  Erwartetes Resulat  |  OK / nicht OK  |  Aufgetretene Fehler / Bemerkungen  |
|----------|-------------|-------|-----|-----|-----|-----|
| 1 | Läuft der Container? | docker ps | Docker-Compose hat funktioniert. | Container läuft. | OK | x |
| 2 | Zugriff von Aussen. | Portforwarding einrichten. | Portforwarding richtig konfiguriert. | Man kommt auf die Seite. | OK | x |


## MySQL

| Testfall NR.  | Beschreibung |  Vorgehen  |  Voraussetzung / Umfeld  |  Erwartetes Resulat  |  OK / nicht OK  |  Aufgetretene Fehler / Bemerkungen  |
|----------|-------------|-------|-----|-----|-----|-----|
| 1 | Läuft der Container? | docker ps | Docker-Compose hat funktioniert. | Container läuft. | OK | x |
| 2 | Portforwarding mit HeidiSQL. | Portforwarding einrichten. | Portforwarding richtig konfiguriert. | Datenbanken werden angezeigt. | OK | x |


## phpMyAdmin

| Testfall NR.  | Beschreibung |  Vorgehen  |  Voraussetzung / Umfeld  |  Erwartetes Resulat  |  OK / nicht OK  |  Aufgetretene Fehler / Bemerkungen  |
|----------|-------------|-------|-----|-----|-----|-----|
| 1 | Läuft der Container? | docker ps | Docker-Compose hat funktioniert. | Container läuft. | OK | x |
| 2 | Zugriff von Aussen. | Portforwarding einrichten. | Portforwarding richtig konfiguriert. | Man kommt auf die Seite. | OK | x |




## Projekt Angebot - IT-Installation 
## Lernfeld 8


# Phase 1: Anwendungsfalldiagramm
![alt text](https://github.com/wpavelev/Projekt_it_installation_lf8/blob/main/Uml-use-case.jpg?raw=true, "Anwendungsfalldiagramm")


# Phase 2: Einrichtung der gemeinsamen Dokumentenablage
Für die Zusammenarbeit wird die Plattform GitHub genutzt. Jedes Teammitglied erstellt sich ein Nutzerprofil, um über die Plattform arbeiten zu können. 

Es wird ein privates Repository auf der GitHub – Plattform erstellt. Jedes Teammitglied wird zur Mitarbeit eingeladen („*Contributor*“). Damit erhält jeder Lese- & Schreibzugriff.

Sofern notwendig wird Git auf der lokalen Maschine installiert und eingerichtet.

Das leere Repository wird mit `git clone` lokal bereitgestellt. Damit ersparen wir uns das Erstellen eines lokalen Repos und das Verbinden mit dem Remote. Die Bisher erstellen Dateien werden in den lokalen Ordner kopiert.
Es erfolgt ein Init-Commit, um die Dateien in das Remote-Repository zu laden
```
git clone <repo>
git add -A
git commit -m „init“
git push
```
Jedes Mitglied kann nun die Dateien per `git clone` abrufen und am Projekt von seinem System aus arbeiten.


# Phase 3: Sequenzdiagramm
![alt text](https://github.com/wpavelev/Projekt_it_installation_lf8/blob/main/Sequenzdiagramm.jpg?raw=true, "Sequenzdiagramm")

# Phase 4: MKDocs 
Um einen eigenen kleinen MKDocs Server zu erstellen, haben wir eine Virtuelle Maschine mit CentOS 9 aufgesetzt.
Die Installation von MKDocs auf den Server konnte mit wenigen Befehlen gemacht werden.
Als erstes haben wir überprüft und sichergestellt, dass Python und der Python Paket Manager (PIP) auf dem Server vorhanden waren.
Da Python auf den meisten Linux Distributionen vorinstalliert ist, konnten wir direkt mit der Installation von MKDocs starten.
Um mit PIP neue Pakete abrufen zu können, mussten wir jedoch noch schnell den Schul-Proxy hinzufügen. 
Dies haben wir wie folgt getan:
```
set http_proxy=http://kjs-03.lan.dd-schulen.de:3128
```
Danach war der Proxy eingebunden.


Wir haben mit 
```
python -m pip install mkdocs mkdocs-material
```
die MKDocs Bibliothek installiert. 

Durch die Befehlszeile von MKDocs, konnten wir mit 
```
mkdocs new projekt_it_installation
``` 
ein neues Projekt anlegen.



Danach mussten wir nur noch die Kofigurationsdatei (mkdocs.yml) auf unsere Bedürfnisse anpassen.
In die Datei haben wir folgendes eingetragen: 
```
site_name: Projekt IT-Installation Lernfeld 8
nav:
 - index.md
```

Mit ``` mkdocs serve ``` konnten wir den MkDoc-Server (welcher automatisch mitgeliefert wurde) starten 
und uns unsere Dokumentation betrachten.

![alt text](https://github.com/wpavelev/Projekt_it_installation_lf8/blob/main/mkdocs_server.PNG?raw=true, "MKDocServer")
![alt text](https://github.com/wpavelev/Projekt_it_installation_lf8/blob/main/mkdocs_server_interface.PNG?raw=true, "MKDocs gerendert")

Wir haben uns aus bequemlichkeit und aus Gründen, der Einfachheit entschieden nur die Markdown-Dateien auf GitHub hochgeladen.


# Phase 5: 
•	Welche Daten werden dargestellt? \
&emsp; o	Grundriss \
&emsp; o	IT-Komponenten \
&emsp; o	IT-Komponenten vorhanden? \
•	Wie werden Daten in den Datenquellen dargestellt? \
&emsp; o	Grundriss			               .dxf, .dwg, .pdf, .ifc, Papier \
&emsp; o	IT-Komponenten		           Excel, Datenbank \
&emsp; o	IT-Komponenten vorhanden? 	Datenbank \
•	Wie können diese importiert und sinnvoll weiterverarbeitet werden? \
&emsp; o	Grundriss			               AutoCAD, M4Personal, Scanner \
&emsp; o	IT-Komponenten		           Excel, MSSQL \
&emsp; o	IT-Komponenten vorhanden?	 MSSQL \
•	Welche Metainformationen sind zur Datenquelle vorhanden? \
&emsp; o	Grundriss			               Erstellungsdatum, Autor, Dateiname \
&emsp; o	IT-Komponenten		           Erstellungsdatum, Autor, Dateiname \
&emsp; o	IT-Komponenten vorhanden?	 Erstellungsdatum, Autor, Dateiname \
•	Wer darf die Dateien nutzen? \
&emsp; o	Grundriss			               Bearbeiter (Lesen, Schreiben), Kunde (Lesen) \
&emsp; o	IT-Komponenten 		          Bearbeiter (Lesen, Schreiben, Ändern),	Verkaufsabteilung (Lesen, Schreiben) \
&emsp; o	IT-Komponenten vorhanden? 	Bearbeiter (Lesen, Schreiben, Ändern), Verkaufsabteilung (Lesen) \
•	Datenformat für unseren Fall \
&emsp; o	Grundriss 			              .dxf, .ifc, .dwg \
&emsp; o	IT-Komponenten 		          Datenbank \
&emsp; o	IT-Komponenten vorhanden? 	Datenbank \


*Aufgrund von Krankheit mehrer Gruppemitglieder, waren wir zeitlich sehr beschränkt! \
Im Durchschnitt waren nur 2 von 4 Mitglieder anwesend.*


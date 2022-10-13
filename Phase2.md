# Phase 2: Einrichtung der gemeinsamen Dokumentenablage
Für die Zusammenarbeit wird die Plattform GitHub genutzt. Jedes Teammitglied erstellt sich ein Nutzerprofil, um über die Plattform arbeiten zu können. 

Es wird ein privates Repository auf der GitHub – Plattform erstellt. Jedes Teammitglied wird zur Mitarbeit eingeladen („*Contributor*“). Damit erhält jeder Lese- & Schreibzugriff.

Sofern notwendig wird Git auf der lokalen Maschine installiert und eingerichtet.

Das leere Repository wird mit `git clone` lokal bereitgestellt. Damit ersparen wir uns das Erstellen eines lokalen Repos und das Verbinden mit dem Remote. Die Bisher erstellen Dateien werden in den lokalen Ordner kopiert.
Es erfolgt ein Init-Commit, um die Dateien in das Remote-Repository zu laden
```
git clone <Repo>
git add -A
git commit -m „init“
git push
```
Jedes Mitglied kann nun die Dateien per git clone abrufen und am Projekt von seinem System aus arbeiten.

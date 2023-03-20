# M300-Services #
## Plattform übergreifende Dienste in ein Netzwerk integrieren ##
***
### Vorbereitung ###
- Git Account erstellt
- Git Client herunterladen
- Virtualbox herunterladen
- Visualstudio Code herunterladen
- Vagrant herunterladen
***
## Bash und Git ##
### Repository erstellen ###
1. Innerhalb der Willkommens-Seite auf Start a project klicken
2. Unter Repository name einen Name definieren ** M300-Services **
3. *Optional:* kurze Beschreibung eingeben: Plattform übergreifende Dienste in ein Netzwerk integrieren
4. Radio-Button bei Public belassen
5. Haken bei Initialize this repository with a README setzen
6. Auf Create repository klicken
7. SSH-Key erstellen (lokal)
***
### SSH KEY erstellen ###
1. ssh-keygen -t rsa -b 4096 -C ~~E-Mail-Adresse von Git-Hub~~ "cyrill.kaelin@edu.tbz.ch"
  
   anschliessend kommt die Meldung: Neuer SSH-Key wird erstellt Generating public/private rsa key pair.
2. Bei der Abfrage, unter welchem Namen der Schlüssel gespeichert werden soll, die Enter-Taste drücken (für Standard):
   Enter a file in which to save the key (~/.ssh/id_rsa): [Press enter]
3. Nun kann ein Passwort für den Key festgelegt werden. Ich empfehle dieses zu setzen und anschliessend dem SSH-Agent zu hinterlegen, 
   sodass keine erneute Eingabe     (z.B. beim Pushen) notwendig ist:
   Enter passphrase (empty for no passphrase): [Passwort] 
   Enter same passphrase again: [Passwort wiederholen]
  **Mein Passwort** *12345678*
  ***
### SSH-Key dem SSH-Agent hinzufügen ###

1. Anmelden unter www.github.com
2. Auf Benutzerkonto klicken (oben rechts) und den Punkt Settings aufrufen
3. Unter den Menübereichen auf der linken Seite zum Abschnitt *SSH und GPG keys * wechseln
4  Auf *New SSH key* klicken
5. Im Formular unter Title eine Bezeichnung vergeben: **Meine Bezeichnung**  *MB SSH-KEY*
6. Den Key im Ordner C:\Users\cyrill.kaelin.CYKA-CHZH-LAP03\.ssh\id_rsa.pub kopieren und mit CTRL + V einfügen und auf Add SSH key klicken
7. Der Schlüssel (SSH-Key) sollte nun in der übergeordneten Liste auftauchen
***
## Git-Client ##
![Git-CLient](https://github.com/mc-b/M300/raw/master/images/Git_36x36.png)

### Git-Client Konfigruation ###
1. Git Bash öffnen
2. Github Grundkonfiguration
```
$ git config --global user.name "<cyrillkaelin>"
$ git config --global user.email "<cyrill.kaelin@edu.tbz.ch>" 
```
### Standard Commands
```
$ cd                               # Change Directory
$  git status                      # Geänderte Datei(en) werden rot aufgelistet
$  git add -A                      # Fügt alle Dateien zum "Upload" hinzu
$  git status                      # Der Status ist nun grün > Dateien sind Upload-bereit (Optional) 
$  git commit -m "Mein Kommentar"  # Upload wird "commited" > Kommentar zu Dokumentationszwecken ist dafür notwendig
$  git status                      # Dateien werden nun als "zum Pushen bereit" angezeigt
$  git push                        #Upload bzw. Push wird durchgeführt
```
***
## Virtualbox ##
1. Iso-Datei herunterladen
2. Manuelle Konfiguration
3. VM aufgezogen
4. 
![Ubuntu VM](https://github.com/cyrillkaelin/M300-Services/blob/main/Bilder/Virtualbox_ubuntu.png)
***
## Vagrant ##
### Wie funktioniert Vagrant ###
Im Prinzip handelt es sich bei Vagrant um ein Werkzeug, das Software zur Virtualisierung wie VirtualBox oder VMware fernsteuern kann. Auf dem Weg ermöglicht es das automatisierte Erstellen von virtuellen Maschinen an Hand einer zuvor erzeugten Konfigurationsdatei.

Vagrant kann anhand eines vorgefertigten Json file, alles übernehmen und sämtliche VMs automatisch erstellen.

### Einrichtung ###
1. Ordner für Vagrant erstellt
```
$ cd C:\
$ mkdir M300
$ cd M300
$ mkdir Vagrant
$ cd Vagrant
```
2. Im VisualstudioCode kann ein Vagrantfile im Json Format erstellt werden, wo alles definiert werden kann
- RAM
- CPU's
- Speicherkapazität
- ISO
- Was für Apps installiert werden.

3. Vagrantfile, dass man erstellt hat, kann nun eingespielt werden
```
$ vagrant init Dateiname        #Vagrantfile erzeugen
$ vagrant up --provider virtualbox  #Provider, in dem die Virtuelle Maschine erzeugt wird angeben  
```
4. VM erscheint nun im Virtualbox

### Repository hinzufügen und Pushen ###
1. Visual Studio Code öffnen
2. Änderungen an entsprechenden Dateien des lokalen Repositorys vornehmen oder neu Dateien in den Ordner kopieren
3. In der linken Leiste das Symbol mit einer "1" aufrufen
Unter dem Abschnitt Changes die betroffenen Files bezüglich ihres Changes "stagen" (Stage Changes)
Nachricht hinterlegen (Message) und Haken (Commit) setzen
Bei den 3 Punkten (...) die Funktion Push aufrufen
Warten, bis Dateien vollständig gepusht wurden


# Reflexion #
Ich habe noch nie mit Vagrant gearbeitet und wusste auch nicht dass man VMs automatisiert erstellen kann.
Durch Vagrant kann ich nun virtuelle Maschinen schnell und einfach erstellen und konfigurieren, um Anwendungen zu testen und Umgebungen zu errichten.
Die Automatisierung mit Vagrant bitte viele Vorteile wie zum Beispiel die Wiederholbarkeit, Zeitersparnis, Flexibilität und Portabilität.
Ich finde das Modul bis jetzt sehr nützlich und hilfreich in der Berufswelt


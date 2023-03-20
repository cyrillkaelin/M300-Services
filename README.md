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
![Ubuntu VM] (https://github.com/cyrillkaelin/M300-Services/blob/main/Bilder/Virtualbox_ubuntu.png)


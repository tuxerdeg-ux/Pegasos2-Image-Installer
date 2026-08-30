# Pegasos2-Image-Installer
Pegasos2 Image Installer

installer-Boot:

ist noch Beta:
Partitionierung muss noch einmal überarbeitet werden.
In der jetztigen Version bitte nur mit leeren Festplatten ausführen.
NFS mount ist eingebaut.
CDrom/DVD sollte auch funktinieren (nicht weiter getestet)
DHCP funktioniert nur mit 100MBit - Schnittstelle

Kopiert die Datei auf eine Partition und startet diese.
Boot-Beispiel:

Ihr landet in einer Console dort könnt ihr den Installer starten.
Eingabe:
./scripte/pegasos2_installer.sh

Dort mountet ihr bitte erst eurer NFS Laufwerk.
Ist es gemountet, könnt ihr eine Festplatte einrichten.
Hier wird zurzeit daran gearbeitet, weil der Pegasos2 im gegensatz zum Efika NICHT von einer Fat31 Partition booten kann.
Mein Ratschlag zur zeit:

200M > Eingabe bei vfat Partition
2G > Swap
>= 4G bei rootfs

Sollte Rest übrig sein bitte mit "NO" nicht partitionieren.

Zurück ins Menü und Partition wiederherstellen/sichern wählen.
Partition auswählen 
Image auswählen.
Sollte die Partition grösser als die Ursprungpartition sein, wird nach dem aufspielen die Partition angepasst

Gegebenfalls könnt ihr dann die fstab noch anpassen.

Bei Fragen,Wünsche,Anträge,Spenden bin ich erreichbar auf a1k:
https://www.a1k.org/forum/index.php?threads/98210/


Images:
für beide gilt:

boot hd:1 boot/peg2_714 root=/dev/sdaX (optional: console=ttyS0,115200)

Auf Grund einer Änderung im Kernel 7.x funktioniert 100MBit - Schnittstelle des Pegasos2.
Ich habe einige Module mitbauen lassen damit auch 1GBit Netzwerkkarten funktionieren.

Beide System setzten eine leere 4GB Partition vorraus.
Für Mate bitte eine grössere Partition bereitstellen, da es sehr knapp bemessen ist.
Hier rate ich zu eine Partition die doppelt so gross ist.

Aus der Peg2_mini_K714 kann jeder User sein eignes Debian zusammenstellen.

Es gibt bei beiden Systemen zur Zeit nur einen User:
Login: root
Passwort: 123456

Ihr müsst also einen eigenen User noch einrichten.



Peg2_mini_K714:

- Kernel 7.1.4
- VIA-IDE/SATA, USB, VIA-Rhine-Netzwerk
- Radeon 9000 Grafik (lokaler Monitor über radeonfb)
- VIA82xx-Sound (mit funktionierender Audioausgabe)
- FireWire als Modul (ist aber auf der modprob blacklist)
- Debian 13 mit systemd, SSH, NFS-Client

Peg2_mate_K714:
- VIA-IDE/SATA, USB, VIA-Rhine-Netzwerk
- Radeon 9000 Grafik (lokaler Monitor über radeonfb)
- VIA82xx-Sound (mit funktionierender Audioausgabe)
- FireWire als Modul (ist aber auf der modprob blacklist)
- Debian 13 mit systemd, SSH, NFS-Client
- Mate installiert


Sollte etwas fehken hier in der Doku, reiche ich es nach.

  

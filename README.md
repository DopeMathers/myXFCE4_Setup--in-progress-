# myXFCE4_Setup--in-progress-
Der Einfachheit halber können alle Pacman Pakete gleichzeitig installiert werden:
sudo pacman -Syu vim git gimp xdotool grub-costumizer snapd noto-fonts powerline-fonts ttf-font-awesome screenfetch gnome-online-accounts thunderbird chromium discord vlc gvfs numlockx

[b]GRUND EINSTELLUNGEN:[/b]

-[ ] Erster Schritt VIM installieren: sudo pacman -Syu vim \n
	-> VIM in bash.rc schreiben:
	-> In Terminal: sudo nano /etc/bash.bashrc
	-> Ans Ende der Datei: export EDITOR="/usr/bin/vim"  (wird gebraucht für pacaur)
-[ ] Erster Schritt ist zu Prüfen ob git installiert ist oder dies zu tun: sudo pacman -Syu git
-[ ] Zweiter Schritt sollte Prüfen ob Gimp installiert ist oder dies tun: sudo pacman -Syu gimp
-[ ] Dritter Schritt sollte Prüfen ob xdotool installiert ist oder dies tun: sudo pacman -Syu xdotool
-[ ] Vierter Schritt sollte Prüfen ob Grub Costumizer installiert ist oder dies tun: sudo pacman -Syu grub-costumizer
-[ ] Fünfter Schritt prüfen ob pacaur installiert oder dies tun: git clone 
	https://aur.archlinux.org/pacaur.git
-[ ] cd pacaur/
-[ ] in Terminal: makepkg -rsi 
	(ggf. Abhängigkeiten installieren)
-[ ] sudo pacman -Syu numlockx
	-> numlockx on
	->/etc/lightdm/lightdm.conf
		[Seat:*]
		greeter-setup-script=/usr/bin/numlockx on
-[ ] Sechster Schritt snap installieren: sudo pacman -Syu snapd
-[ ] (Sechster Schritt prüfen ob Spotify installiert ist oder dies tun: git clone
	https://aur.archlinux.org/spotify.git)

 Schriftsätze Installieren:
-[ ] Evnt. installieren Notofonts: sudo pacman -Syu noto-fonts
-[ ] Font installieren: git clone https://github.com/blaisck/sfwin.git
	Entpacken und mit: sudo mv * /usr/share/fonts
-[ ] Powerline Fonts installieren: sudo pacman -Syu powerline-fonts
-[ ] Font awesome installieren: sudo pacman -Syu ttf-font-awesome
	
-[ ] SanFrancisco Regular in Terminal, Fensterverwaltung und Erscheinungsbild festlegen (Schriftgröße 11)

Terminal einrichten:
-[ ] Einstellungen -> xfce-terminal
-[ ] Vorgegebener Titel kann man wählen wie man möchte (Kommando~Zentrale)
-[ ] Aufklapp
	->Fenster offen lassen wenn es den fokus verliert
	->Fenster immer im Vordergrund halten
	-> Breite 100%
	-> Höhe 40%
	-> Deckkraft 60%
-[ ] Farben
	-> Text Farbe: #45BE0D
-[ ]  Aussehen Deckkraft 0,75
-[ ] Terminal öffnen und installiere: sudo pacman -Syu screenfetch
	-> sudo nano /etc/bash.bashrc
	-> am Ende hinzufügen:
	-> screenfetch

Simbole einrichten:
-[ ] Icons installieren: https://www.gnome-look.org/p/1012338/
	Entpacken und mit: sudo mv * /usr/share/icons
	Anwendungen -> Einstellungen -> Erscheinungsbild -> Simbole

Leiste einrichten:
-[ ] Leiste 2 löschen (wird später durch Plank ersetzt)
-[ ] Leiste 1 Größe auf 40
-[ ] Leiste 1 Objekte:
	Whisker-Menü, Starter (Eclipse), Trennelement (Strich), Arbeitsfläschen switcher, Trennelement(Strich), Trennelement (Durchsichtig gedehnt), Allgemeine Überwachung (Fenstertitel), Trennelement (Druchsichtig gedehnt), Trennelement (Strich), (Allgemeine Überwachung (Spotify prev), Allgemeine Überwachung (Spotify-Panel), Allgemeine Überwachung (Spotify next)), Trennelement (Strich), Wetterbericht, Benachrichtigungsfläche, PulseAudio, Uhr, Trennelement (Strich), Aktionsknöpfe (Abmelden...)
-[ ] Benötigte Tools laden: 
	XFCE-Tweaks installieren: git clone https://github.com/marcusscomputer/xfcetweaks.git
	(Spotify-Control installieren Teil 1: git clone https://github.com/jonseppanen/slotify.git)
	(Spotify-Control installieren Teil2: git clone https://github.com/xtonousou/xfce4-genmon-scripts.git)
-[ ] (xfce4_genmon: spotify-panel.sh bei #panel einfügen -> INFO+="<click>spotify</click>" anpassen)
-[ ] Tools ausführbar machen -> In Verzeichniss wechseln und Terminal aufrufen -> chmod 755 *
-[ ] Fenstertitel: /usr/share/xfcetweaks/windowtitle
-[ ] (Spotify prev: /usr/share/xfcetweaks/spotify_genmon/spotify-prev.sh)
-[ ] (Spotify-Panel: /usr/share/xfcetweaks/xfce4_genmon/spotify-panel.sh)
-[ ] (Spotify-next: /usr/share/xfcetweaks/spotify_genmon/spotify-next.sh)
-[ ] Whiskermenu icon: https://www.google.com/search?q=menu+icon&sxsrf=ALeKk02yV_vv6XCOfrEOueWNseWBLDm1ZA:1602798324430&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjBlpiGybfsAhWrAGMBHXuJDi0Q_AUoAXoECBUQAw&biw=812&bih=683#imgrc=BahmAusqqeMgYM (Mit Gimp Alphakanal hinzufügen, alle Durchsichtigen stellen makieren und wegradieren)
	-> Rechtsklick auf Whiskermenü -> Eigenschaften -> Leistenknopf -> Symbol

Arbeitsflächen einrichten: 
-[ ] Rechtsklick auf Switcher -> Eigenschaften -> Haken raus bei Miniaturansicht
-[ ] Einstellungen -> Arbeitsflächen
-[ ] Festlegen der Anzahl an Arbeitsflächen (5: Home, Coding, Entertainment, Browsen, Gaming)
	-> https://fontawesome.com/v4.7.0/cheatsheet/ (Hier kann man sich Simbole raussuchen)
	-> Gewünschtes Simbol kopieren -> Name der Arbeitsfläche, zwei mal space Simbol einfügen
	zwei mal space.
	-> Für jede Arbeitsfläche wiederholen
-[ ] Deckkraft betreten = 100% verlassen = 70%

Whiskermenü einrichten:
-[ ] Rechtsklick auf Menü -> Eigenschaften -> 
-[ ] Aussehen -> Hintergrunddeckkraft 90%
-[ ] Verhalten -> Kategoriewechsel druch Darüberfahren
-[ ] Befehle -> Benutzerwechsel raus
	-> Abmelden
	-> Herunterfahren
	-> Abmelden... raus
	-> Menü bearbeiten raus
	-> Profil bearbeiten raus

Leiste 2 einrichten: 
-[ ] Plank Dock installieren: https://www.linuxuprising.com/2019/12/a-guide-to-using-plank-dock-on-linux.html
sudo pacman -S plank
-[ ] Plank-Dock-Theme installieren: https://www.gnome-look.org/p/1408781/
	
-[ ] Gewünschte Anwendungen öffnen und bei Icon im Plankdock -> Rechtsklick
	-> Haken bei "Im Dock behalten"
-[ ] Mit jeder Anwendung die ins Dock soll wiederholen
-[ ] Rechtsklick am Rand vom Dock -> Symbolvergrößerung aktivieren, bei Thema BigSur auswählen
-[ ] Verhalten -> Allen Fenstern ausweichen

Leiste 3 einrichten: 
-[ ] Neue Leiste -> Größe 0, automatisch anpassen -> Schreibtischleiste - Leiste rechts mittig -> Leiste sperren
-[ ] Leiste 3 Objekte: 
	Trennelement (Strich), Allgemeine Überwachung (Batterie), Trennelement (Strich), Wavelan, Netzwerkmonitor, Trennelement (Strich), Überwachung Systemlast, CPU Diagramm, CPU Frequenz, Trennelement (Strich), Überwachung Systemlast, Allgemeine Überwachung (CPU), Trennelement (Strich), Allgemeine Überwachung (Uhr), Trennelement (Strich)
-[ ] Batterie: /usr/share/xfcetweaks/xfce4_genmon/battery-panel.sh
-[ ] CPU: /usr/share/xfcetweaks/xfce4_genmon/cpu-panel.sh
-[ ] Uhr: /usr/share/xfcetweaks/xfce4_genmon/datetime-panel.sh
-[ ] Deckkraft betreten = 100% verlassen = 80%

Theme installieren und aktivieren:
-[ ]  Theme installieren: https://www.gnome-look.org/p/1334194/ (Ich benutz die Variante Dark)
-[ ] Entpack und kopieren nach:
	sudo mv * /usr/share/themes
-[ ] Einstellungen -> Erscheinungsbild -> Themes
-[ ] XFCE Theme: https://www.gnome-look.org/p/1187179/ (Matcha-aliz)
-[ ] Entpacken und kopieren nach: 
	sudo mv * /usr/share/themes
-[ ] Einstellungen -> Fensterverwaltung -> Themes

Fenstereinstellungen: 
-[ ] Einstellungen -> Feineinstellungen der Fensterverwaltung -> Komposit
-[ ] Deckkraft von inaktiven fenstern 5-10% verringern
-[ ] Deckkraft beim verschieben auf ca 60%

Grub-Theme installieren:
-[ ]  Grub-Theme installieren: https://www.gnome-look.org/p/1414997/
-[ ] Entpacken
-[ ] In gewünschten Ordner verschieben 
-[ ] Terminal öffnen und:
	sudo bash install.sh

Tastaturkürzel:
-[ ] Einstellungen -> Tastatur -> Tastenkürzel für Anwendungen
	-> xfce4-appfinder auf super+alt(Links) (super=windows taste)
	-> filemanager auf super+e (ruht von Windows da ruft der Explorer auf)
	-> xfce4-terminal --drop-down auf strg+q
	-> xflock4 auf super+L
	-> xfce4-terminal auf strg+t

Hintergrundbild einrichten:
-[ ] //noch machen

ERWEITERTE EINSTELLUNGEN:

 Dmlight-Theme installieren:
//Bisher noch nichts tolles gefunden!

Plymouth configurieren:
-[ ] Terminal: pacaur -S plymouth
-[ ] Terminal: sudo nano /etc/mkinitcpio.conf
-[ ] HOOKS=(base udev plymouth ...)  speichern und close
-[ ] Terminal: sudo mkinitcpio -p linux
-[ ] Terminal: sudo nano /etc/default/grub
-[ ] GRUB_CMDLINE_LINUX_DEFAULT="loglevel3 quiet splash rd.udev.log_priority=3 vt.gloabl_cursor_default=0"
-[ ] Speichern und schließen
-[ ] Terminal: sudo grub-mkconfig -o /boot/grub/grib.cfg
-[ ] Theme herunterladen: https://www.gnome-look.org/p/1180617/
-[ ] Entpacken und nach: sudo mv * /usr/share/plymouth/themes
-[ ] Terminal: sudo plymouth-set-default-theme -R themename
-[ ] Terminal: sudo systemctl disable lightdm (Order entsprechender displaymgr)
-[ ] Terminal: sudo systemctl enable lightdm-plymouth.service

GoogleDrive einbinden:
-[ ]  Gnome-Accounts für GDrive: sudo pacman -Syu gnome-online-accounts 
	->  Gnome-Accounts setup: sudo gnome-control-center online-accounts
	-> Und google verknüpfen

 Java installieren:
-[ ] Download: https://jdk.java.net/15/
-[ ] Download: https://gluonhq.com/products/javafx/
-[ ] Entpacken in Ordner z.B. Java
-[ ] Terminal:
/home/user/Java/jdk-15/bin/jlink --output jdfx-15 --module-path  /home/user/Java/javafx-jmods-15 --add-modules java.base,java.compiler,java.datatransfer,java.desktop,java.instrument,java.logging,java.management,java.management.rmi,java.naming,java.net.http,java.prefs,java.rmi,java.scripting,java.se,java.security.jgss,java.security.sasl,java.smartcardio,java.sql,java.sql.rowset,java.transaction.xa,java.xml.crypto,java.xml,jdk.accessibility,jdk.aot,jdk.attach,jdk.charsets,jdk.compiler,jdk.crypto.cryptoki,jdk.crypto.ec,jdk.dynalink,jdk.editpad,jdk.hotspot.agent,jdk.httpserver,jdk.incubator.foreign,jdk.incubator.jpackage,jdk.internal.ed,jdk.internal.jvmstat,jdk.internal.le,jdk.internal.opt,jdk.internal.vm.ci,jdk.internal.vm.compiler,jdk.internal.vm.compiler.management,jdk.jartool,jdk.javadoc,jdk.jcmd,jdk.jconsole,jdk.jdeps,jdk.jdi,jdk.jdwp.agent,jdk.jfr,jdk.jlink,jdk.jshell,jdk.jsobject,jdk.jstatd,jdk.localedata,jdk.management.agent,jdk.management.jfr,jdk.management,jdk.naming.dns,jdk.naming.rmi,jdk.net,jdk.nio.mapmode,jdk.sctp,jdk.security.auth,jdk.security.jgss,jdk.unsupported.desktop,jdk.unsupported,jdk.xml.dom,jdk.zipfs,javafx.base,javafx.controls,javafx.fxml,javafx.graphics,javafx.media,javafx.swing,javafx.web
-[ ] Danach kann jdfx-15 wie folgt installiert werden:
-[ ] Terminal: sudo cp jdfx-15 /usr/lib/jvm/jdfx-15
-[ ] Installieieren:
	sudo archlinux-java set jdfx-15

 Eclipse installieren:
-[ ] Eclipse downloaden: https://www.eclipse.org/downloads/
-[ ] Terminal: sudo chown -R $USER:$USER /opt/eclipse 
-[ ] Launcher-Symbol einrichten:
 	-> erstelle Datei eclipse.desktop und öffnen mit edito/mousepad
	-> 	[Desktop Entry]
		Name=Eclipse 
		Type=Application
		Exec=/opt/eclipse/eclipse
		Terminal=false
		Icon=/opt/eclipse/icon.xpm
		Comment=Integrated Development Environment
		NoDisplay=false
		Categories=Development
		Name[en]=eclipse
-[ ] Terminal: sudo mv eclipse.desktop /usr/share/applications/
	(Java muss installiert sein damit Eclipse startet)

Simplenote installieren:
-[ ] Simplenote-linux-1.21.1-x86_64.AppImage herunterladen:
	https://github.com/Automattic/simplenote-electron/releases/tag/v1.21.1
-[ ] Simplenote icon downloaden: https://www.google.com/search?q=simplenote+icon&sxsrf=ALeKk02762HzCvHEV0KNnyT78rs6Oh0Q9w:1602870823428&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjO4rOQ17nsAhUHA2MBHeNnCVUQ_AUoAXoECAsQAw&biw=952&bih=918#imgrc=jW9KbTn0ZoSZcM
-[ ] Bild eventuell in gimp bearbeiten
-[ ] Simplenote.AppImage verschieben: sudo mv Simplenote.AppImage /opt/simplenotes/
-[ ] Icon verschieben: sudo mv simple-note.png /opt/simplenotes/
-[ ] Launchericon einrichten:
	->erstelle Datei simplenote.desktop und mit editor/mousepad öffnen
	-> [Desktop Entry]
	Name=Simplenote
	Type=Application
	Exec=/opt/simplenotes/simplenote.AppImage
	Terminal=false
	Icon=/opt/simplenotes/simple-note.png
	Comment=Note App
	NoDisplay=false
	Categories=Notes
	Name[en]=simplenote
-[ ] Terminal: sudo mv simplenotes.desktop /usr/share/applications/

 Thunderbird einrichten & Theme installieren:
-[ ] Installieren: sudo pacman -Syu thunderbird
-[ ] In E-Mail Accounts einloggen
-[ ] Theme runterladen:
	https://addons.thunderbird.net/de/thunderbird/complete-themes/

Chrome einrichten:
-[ ] Terminal: sudo pacman -Syu chromium
-[ ] extensions: https://chrome.google.com/webstore/search/icloud?hl=de
-[ ] Theme: https://chrome.google.com/webstore/detail/just-black/aghfnjkcakhmadgdomlmlhhaocbkloab?hl=de

 Discord installieren:
-[ ] Terminal: sudo pacman -S discord
-[ ] Einloggen

 Whatsapp installieren:
-[ ] Terminal: snap install whatsdesk
-[ ] Einloggen

 VLC installieren & VLC Theme installieren:
-[ ] Terminal: sudo pacman -Syu vlc
-[ ] VLC Theme downloaden und installieren:
	https://www.videolan.org/vlc/skins.html

Android Tablet als zweit Bildschirm einrichten:
-[ ] Siehe Anleitung: Android as second screen

Links zusammengefasst:
SanFramcisco Font: https://github.com/blaisck/sfwin
Font awesome Symbole: https://fontawesome.com/v4.7.0/cheatsheet/
Theme(Gnome): https://www.gnome-look.org/p/1334194/
Icons: https://www.gnome-look.org/p/1012338/
XFCE Tweaks: https://github.com/marcusscomputer/xfcetweaks.git
Spotify: https://aur.archlinux.org/spotify.git
Spotify-Panel: https://github.com/jonseppanen/slotify.git
Spotify-Controll: https://github.com/xtonousou/xfce4-genmon-scripts.git
Grub-Theme: https://www.gnome-look.org/p/1414997/
Plank-Dock: https://www.linuxuprising.com/2019/12/a-guide-to-using-plank-dock-on-linux.html
Plank-Dock-Theme: https://www.gnome-look.org/p/1408781/
Simplenote: https://github.com/Automattic/simplenote-electron/releases/tag/v1.21.1

Alle Rechte liegen bei den jeweiligen erstellern, alle Links sind Links zu den Originalquellen. Besonderer Dank gilt Marcus-s und seinem Video XFCE von Null auf Cool... 

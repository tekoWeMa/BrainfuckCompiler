## Raspberry PI Einrichtung

Für die Visuelle demo benötigen wir einen Host. Wir haben uns hier für ein Raspberry PI entschieden, da dieses einfach zu warten ist und wenig Platz benötigt.<br />

Mit Hilfe von Raspberry PI Imager kann das gewünschte Betriebssystem installiert werden. Wir verwenden das PI OS 64-bit und schreiben dieses auf die Micro SD Karte.
Bei erfolgreichem schreiben des Betriebssystems können wir die SD Karte einsetzen und mit einem USB-C den Raspberry Pi Computer mit Strom versorgen.

## Raspberry Konfiguration

Mittels HDMI können wir den Desktop des Betriebssystem anzeigen lassen und die ersten Konfigurationen vornehmen. <br />

Mittels Setupmanager wählen wir als erstes die korrekte Region, Zeitzone und Sprache. Danach setzen wir ein Passwort sowie den Namen für den User. Wir benennen ihn nach unserem Projekt, also sugu. Wir benötigen den Namen und Passwort später, wenn wir via SSH darauf zugreifen wollen. <br />

Wir setzen den Haken für das Screen Setup um optimierte Auflösungen zu erhalten für den Bildschirm. Da wir Ethernet verwenden, müssen wir uns nicht mit einem W-LAN verbinden. <br />

Sobald wir mit einem Netzwerk verbunden sind, können wir im Setupmanager ein Update der Software durchführen.

## SSH einschalten

Um auf unseren User zugreifen zu können, müssen wir SSH aktivieren. Dafür klicken wir auf dem Desktop auf das Raspberry logo, wählen **Preferences** und dann **Raspberry PI Configuration**. Unter dem **Interfaces** Tab können wir SSH anwählen.
![](Raspi-Interface.png)
![](SSH.png)

## Statische IP vergeben

Um mit keinen Komplikationen konfrontiert zu werden, vergeben wir dem Raspberry PI eine Statische IP Addresse. Dafür öffnen wir das Terminal auf dem Desktop. Mittels ``ifconfig`` können wir die momentan zugeweiste IP des netzwerkes ansehen. In unserem Fall ist dies **192.168.1.17**.<br />Mittels ``sudo nano /etc/dhcpcd.conf`` können wir direkt in die config file unsere gewünschte IP Addresse schreiben. Dies machen wir wiefolgt:

```
interface eth0
static ip_address=192.168.1.17
static routers=192.168.1.1
static domain_name_servers=8.8.8.8 8.8.4.4

```

Einstellungen mit ``Ctrl + o`` schreiben und den Editor mit ``Ctrl + x`` verlassen. Danach den Raspi neustarten:

``sudo reboot``

## Installation Tinkerforge software

### Brick Daemon (brickd)

Der Brick Daemon ist ein Daemon (bzw. Service für Windows) der als eine Brücke zwischen [Bricks](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricks)/[Bricklets](https://www.tinkerforge.com/de/doc/Primer.html#primer-bricklets) und den [API Bindings](https://www.tinkerforge.com/de/doc/Software/API_Bindings.html#api-bindings) für die verschiedenen Programmiersprachen fungiert.

Der Daemon leitet Daten zwischen der USB Verbindung und den TCP/IP Sockets hin und her. Bei der Benutzung der API Bindings wird eine TCP/IP Verbindung zum Brick Daemon hergestellt. Dieses Konzept erlaubt es Bindings für nahezu jede Programmiersprache ohne Abhängigkeiten zu erstellen. Dadurch ist es möglich Bricks und Bricklets über eingebettete Geräte wie Smartphones zu programmieren, die nur spezifische Programmiersprachen unterstützten.

Zusätzlich ist es möglich den PC auf dem der Brick Daemon läuft von dem PC auf dem der Benutzercode läuft zu trennen. Dadurch ist das Steuern über ein Smartphone oder auch über das Internet möglich.

# Brick Daemon Installation auf Linux

**Voraussetzungen**: libusb 1.0.6 oder neuer

Der [Brick Daemon](https://www.tinkerforge.com/de/doc/Software/Brickd.html#brickd) kann auf einer Debian basierten Distribution (Ubuntu, Mint, etc.) aus einer `.deb` Datei installiert werden. Für Arch Linux steht im AUR das Paket [brickd](https://aur.archlinux.org/packages/brickd/) zur Verfügung. Auf anderen Distributionen kann der Brick Daemon aus dem Quelltext installiert werden.

## Debian Paket

Das Brick Daemon Debian Paket steht im [APT Repository](https://download.tinkerforge.com/apt/) bereit, kann aber auch händisch installiert werden.

### APT Repository

Zuerst entsprechend der [Anleitung](https://www.tinkerforge.com/de/doc/Software/APT_Repository.html#apt-repository) das APT Repository hinzufügen. Dann das Brick Daemon Paket installieren:

sudo apt install brickd

Der Brick Daemon wird nach der Installation und beim Hochfahren des Systems automatisch gestartet.

### Händische Installation

Als erstes muss das passende Brick Daemon `.deb` von der [Download-Seite](https://www.tinkerforge.com/de/doc/Downloads.html#downloads-tools) heruntergeladen werden. Nach einem Rechtsklick auf die Datei kann "Open with GDebi Package Installer" ausgewählt werden:

![](res/Pasted%20image%2020230217111112.png)

Klick auf "Install Package":

![](res/Pasted%20image%2020230217111134.png)

Fertig:

![](res/Pasted%20image%2020230217111159.png)
